Download Link: https://assignmentchef.com/product/solved-network-addresses-design-in-its-entirety
<br>
A.    Subnetting

Subnetting is a process of breaking a large network into small networks known as subnets. Subnetting happens when we extend the default boundary of the subnet mask. Basically we borrow host bits to create networks (i.e., subnets).

We have been assigned the network address <strong>199</strong>.1.2.0.  Based on the chart below, we know this is a Class C address.  This is determined by observing the first octet of the IP address, which is 199.  This octet falls in between 192 and 223.




<table border="1" width="624" cellspacing="0" cellpadding="0">

 <tbody>

  <tr>

   <td valign="top" width="312"><p align="center"><strong>Class</strong></td>

   <td valign="top" width="312"><p align="center"><strong>Octet Decimal Range</strong></td>

  </tr>

  <tr>

   <td valign="top" width="312">A</td>

   <td valign="top" width="312">1 – 126</td>

  </tr>

  <tr>

   <td valign="top" width="312">B</td>

   <td valign="top" width="312">128 – 191</td>

  </tr>

  <tr>

   <td valign="top" width="312">C</td>

   <td valign="top" width="312">192 – 223</td>

  </tr>

 </tbody>

</table>




Each class has a predefined default subnet mask that tells us the octets, which are already part of the network portion, as well as how many bits we have available to work with.




<table border="1" width="624" cellspacing="0" cellpadding="0">

 <tbody>

  <tr>

   <td valign="top" width="170"><p align="center"><strong>Class</strong></td>

   <td valign="top" width="198"><p align="center"><strong>Subnet Mask</strong></td>

   <td valign="top" width="256"><p align="center"><strong>Format</strong></td>

  </tr>

  <tr>

   <td valign="top" width="170">A</td>

   <td valign="top" width="198">255.0.0.0</td>

   <td valign="top" width="256">Network.Host.Host.Host</td>

  </tr>

  <tr>

   <td valign="top" width="170">B</td>

   <td valign="top" width="198">255.255.0.0</td>

   <td valign="top" width="256">Network.Network.Host.Host</td>

  </tr>

  <tr>

   <td valign="top" width="170">C</td>

   <td valign="top" width="198">255.255.255.0</td>

   <td valign="top" width="256">Network.Network.Network.Host</td>

  </tr>

 </tbody>

</table>

<strong>CIDR (Classless Inter Domain Routing)</strong>

CIDR is a slash notation of the subnet mask.  CIDR tells us the number of on bits in a network address.

●     Class A has default subnet mask 255.0.0.0. that means first octet of the subnet mask has all on bits. In slash notation it would be written as /8, means address has 8 bits on.

●     Class B has default subnet mask 255.255.0.0. that means first two octets of the subnet mask have all on bits. In slash notation it would be written as /16, means address has 16 bits on.

●     Class C has default subnet mask 255.255.255.0. that means first three octets of the subnet mask have all on bits. In slash notation it would be written as /24, means address has 24 bits on.

<strong>Scenario</strong>

<span lang="EN">The building will house four computer labs that will be used for instruction. In the building diagrams above, the labs are labeled Classroom #2 and Classroom #4 on the first floor and Classroom #1 and Classroom #5 on the second floor; each computer lab will have a closet. Each lab will have 25 computers: 23 student computers, 1 instructor computer, and 1 server in the closet for instructional use.</span>

<span lang="EN">In addition, there will be a Student Computer Lab that will provide computer access to students to do their homework. There will be 25 computers in this lab and a server in the closet. To allow students access to library resources, the library will also have 20 computers for the general public to use and 5 computers for library staff.</span>

<span lang="EN">There needs to be separation between students, staff, and public access networks.  The open Wi-Fi also needs to be separate from the other three groupings.</span>

<span lang="EN">Finally, there are various offices in the building. Each of these offices will have one computer for staff use, with the exception of the admissions office, which will have five computers. There will be two server rooms, one on the first floor and one on the second floor.</span>

<strong>Methodology</strong>

Given the aforementioned scenario, we are going to use the 192.168.0.0/24 network and create a total of 8 subnets, with 25 hosts on each subnet.  The chart below describes structures the scenario to include each subnet and required hosts.




<table border="1" width="624" cellspacing="0" cellpadding="0">

 <tbody>

  <tr>

   <td valign="top" width="312"><p align="center"><strong>Subnet Description</strong></td>

   <td valign="top" width="312"><p align="center"><strong>Required Hosts</strong></td>

  </tr>

  <tr>

   <td valign="top" width="312">Students in Classroom 1 Computer Lab</td>

   <td valign="top" width="312">23 Computers</td>

  </tr>

  <tr>

   <td valign="top" width="312">Students in Classroom 2 Computer Lab</td>

   <td valign="top" width="312">23 Computers</td>

  </tr>

  <tr>

   <td valign="top" width="312">Students in Classroom 3 Computer Lab</td>

   <td valign="top" width="312">23 Computers</td>

  </tr>

  <tr>

   <td valign="top" width="312">Students in Classroom 4 Computer Lab</td>

   <td valign="top" width="312">23 Computers</td>

  </tr>

  <tr>

   <td valign="top" width="312">Students in Student Computer Lab</td>

   <td valign="top" width="312">24 Computers</td>

  </tr>

  <tr>

   <td valign="top" width="312">Public Access network</td>

   <td valign="top" width="312">20 Computers</td>

  </tr>

  <tr>

   <td valign="top" width="312">Equipment</td>

   <td valign="top" width="312">xx Network Peripherals (servers access points) Computers</td>

  </tr>

  <tr>

   <td valign="top" width="312">Staff Office / Admissions Network</td>

   <td valign="top" width="312">xx Computers</td>

  </tr>

 </tbody>

</table>

(Using the How to Subnet a Network Video provided in CMIT 265 LEO – Content – UMUC Network Design Proposal, <strong>complete the following chart</strong>.)




<table border="1" width="624" cellspacing="0" cellpadding="0">

 <tbody>

  <tr>

   <td valign="top" width="121"><p align="center"><strong>Subnet</strong></td>

   <td valign="top" width="138"><p align="center"><strong>Network Address</strong></td>

   <td valign="top" width="228"><p align="center"><strong>Host Address Range</strong></td>

   <td valign="top" width="137"><p align="center"><strong>Broadcast Address</strong></td>

  </tr>

  <tr>

   <td colspan="4" valign="top" width="624">Subnet Mask: 255.255.255._____</td>

  </tr>

  <tr>

   <td valign="top" width="121">Classroom 1</td>

   <td valign="top" width="138"><p align="center">192.168.0.0</td>

   <td valign="top" width="228"><p align="center">192.168.0.1 – 192.168.0.30</td>

   <td valign="top" width="137"><p align="center">192.168.0.31</td>

  </tr>

  <tr>

   <td valign="top" width="121">Classroom 2</td>

   <td valign="top" width="138"><p align="center">192.168.0.__</td>

   <td valign="top" width="228"><p align="center">192.168.0.__ – 192.168.0.__</td>

   <td valign="top" width="137"><p align="center">192.168.0.__</td>

  </tr>

  <tr>

   <td valign="top" width="121">Classroom 3</td>

   <td valign="top" width="138"><p align="center">192.168.0.__</td>

   <td valign="top" width="228"><p align="center">192.168.0.__ – 192.168.0.__</td>

   <td valign="top" width="137"><p align="center">192.168.0.__</td>

  </tr>

  <tr>

   <td valign="top" width="121">Classroom 4</td>

   <td valign="top" width="138"><p align="center">192.168.0.96</td>

   <td valign="top" width="228"><p align="center">192.168.0.97 – 192.168.0.126</td>

   <td valign="top" width="137"><p align="center">192.168.0.127</td>

  </tr>

  <tr>

   <td valign="top" width="121">Student Computer Lab</td>

   <td valign="top" width="138"><p align="center">192.168.0.128</td>

   <td valign="top" width="228"><p align="center">192.168.0.129 – 192.168.0.158</td>

   <td valign="top" width="137"><p align="center">192.168.0.127</td>

  </tr>

  <tr>

   <td valign="top" width="121">Equipment</td>

   <td valign="top" width="138"><p align="center">192.168.0.__</td>

   <td valign="top" width="228"><p align="center">192.168.0.__ – 192.168.0.__</td>

   <td valign="top" width="137"><p align="center">192.168.0.__</td>

  </tr>

  <tr>

   <td valign="top" width="121">Library Lab (Public Access)</td>

   <td valign="top" width="138"><p align="center">192.168.0.__</td>

   <td valign="top" width="228"><p align="center">192.168.0.__ – 192.168.0.__</td>

   <td valign="top" width="137"><p align="center">192.168.0.__</td>

  </tr>

  <tr>

   <td valign="top" width="121">Staff Network</td>

   <td valign="top" width="138"><p align="center">192.168.0.__</td>

   <td valign="top" width="228"><p align="center">192.168.0.__ – 192.168.0.__</td>

   <td valign="top" width="137"><p align="center">192.168.0.__</td>

  </tr>

 </tbody>

</table>

Rubric Name: Network Design Proposal Part 2

5/5 - (1 vote)

<table class="d_t" summary="">

 <tbody>

  <tr>

   <td class="d_tl d_tm d_tn"></td>

   <td class="d_tl d_tm d_tn">

    <table id="z_n" class="d_g d_gd" summary="This table lists criteria and criteria group names in the first column. The first row lists level names and includes scores if the rubric uses a numeric scoring method. A similar row starts any additional criteria group. If the rubric uses a numeric scoring method, the overall score is in the last two rows: the second last row gives the overall level names and scores; the last row gives the overall score for each level.">

     <tbody>

      <tr class="fgskip">

       <td></td>

       <td></td>

       <td></td>

       <td></td>

       <td></td>

      </tr>

      <tr class="d_gh">

       <th class="d_hch d_gw d_gc" scope="col">Competencies Section 2</th>

       <th class="d_hch d_gw d_gc" scope="col"><label>Level 3 90-100%</label></th>

       <th class="d_hch d_gw d_gc" scope="col"><label>Level 2 80-89%</label></th>

       <th class="d_hch d_gw d_gc" scope="col"><label>Level 1: Minimally Proficient 70 – 79%</label></th>

       <th class="d_hch d_gw d_gc" scope="col"><label>Not proficient</label></th>

      </tr>

      <tr>

       <th class="d_gt d_ich" scope="row"><label>Develop a proposal to design a network infrastructure based on business needs.</label></th>

       <td class="d_gc d_gt"></td>

       <td class="d_gc d_gt"></td>

       <td class="d_gc d_gt"></td>

       <td class="d_gc d_gt"></td>

      </tr>

      <tr class="d_gh">

       <th class="d_hch d_gw d_gc" scope="col">Overall Score</th>

       <th class="d_hch d_gw d_gc" scope="col"><label>Level 5</label></th>

       <th class="d_hch d_gw d_gc" scope="col"><label>Level 4</label></th>

       <th class="d_hch d_gw d_gc" scope="col"><label>Level 3</label></th>

       <th class="d_hch d_gw d_gc" scope="col"><label>L</label></th>

      </tr>

     </tbody>

    </table></td>

  </tr>

 </tbody>

</table>

<strong><em>Comprehensive understanding of how to subnet a network</em></strong>




<em>P</em><em>r</em><em>ovides subnetting information using standard C class subnetting to account for all major subnets required, and <strong>all</strong> answers are correct.</em>




<strong><em>Proficient</em></strong><em>understanding of how to subnet a network</em>




<em>P</em><em>r</em><em>ovides subnetting information using standard C class subnetting to account for all major subnets required, and <strong>most</strong> answers are correct.</em>

<strong><em>B</em></strong><strong><em>asic</em></strong> <em>understanding of how to subnet a network</em>


