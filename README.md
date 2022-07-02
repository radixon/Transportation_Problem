# Transportation_Problem

East Food company has 4 warehouses that are in Savannah, Charleston, Columbus, and Jacksonville.  The company ships goods from these warehouses to the nearby cities.  The table 4 shows the distances between warehouses and cities, in miles.  Table 5 shows the quantities that warehouse cities supply.  Table 6 shows the demand in cities. <br /> <br />

##Variables

Suppliers	i=1,2,3,4
  1. Savannah	&emsp;	2. Charleston	&emsp;	3. Columbus	&emsp;	4. Jacksonville

Retailers	j=1,2,3,4,5,6,7,8,9,10,11,12,13,14,15
  1. Tifton	&emsp;	2. Augusta	&emsp;	3. Atlanta	&emsp;	4. Chattanooga
  5. Macon	&emsp;	6. Valdosta	&emsp;	7. Florence	&emsp;	8. Greenville
  9. Hilton Head	&emsp; 10. Statesboro	&emsp; 11. Summerville	&emsp; 12. Aikens
  13. Waycross	&emsp; 14. Pooler		&emsp; 15. Jessup

<br /> <br />
## Constraints

Demand	d_j where j=1,2,3,4,5,6,7,8,9,10,11,12,13,14,15
1. 2000	&emsp; 2. 20000	&emsp; 3. 49000	&emsp; 4. 18000	&emsp; 5. 16000
6. 6000	&emsp; 7. 4000	&emsp; 8. 7000	&emsp; 9. 4000	&emsp; 10. 4000
11. 6000	&emsp; 12. 3000	&emsp; 13. 2000	&emsp; 14. 3000	&emsp; 15. 1000

x<sub>11</sub> + x<sub>21</sub> + x<sub>31</sub> + x<sub>41</sub>  ≥ 2000 <br />	
x<sub>12</sub> + x<sub>22</sub> + x<sub>32</sub> + x<sub>42</sub>  ≥20000 <br />
x<sub>13</sub> + x<sub>23</sub> + x<sub>33</sub> + x<sub>43</sub>  ≥49000 <br />		
x<sub>14</sub> + x<sub>24</sub> + x<sub>34</sub> + x<sub>44</sub>  ≥18000 <br />
x<sub>15</sub> + x<sub>25</sub> + x<sub>35</sub> + x<sub>45</sub>  ≥16000 <br />		
x<sub>16</sub> + x<sub>26</sub> + x<sub>36</sub> + x<sub>46</sub>  ≥6000 <br />
x<sub>17</sub> + x<sub>27</sub> + x<sub>37</sub> + x<sub>47</sub>  ≥4000 <br />		
x<sub>18</sub> + x<sub>28</sub> + x<sub>38</sub> + x<sub>48</sub>  ≥7000 <br />
x<sub>19</sub> + x<sub>29</sub> + x<sub>39</sub> + x<sub>49</sub>  ≥4000 <br />		
x<sub>110</sub> + x<sub>210</sub> + x<sub>310</sub> + x<sub>410</sub>  ≥4000 <br />
x<sub>111</sub> + x<sub>211</sub> + x<sub>311</sub> + x<sub>411</sub>  ≥6000 <br />
x<sub>112</sub> + x<sub>212</sub> + x<sub>312</sub> + x<sub>412</sub>  ≥3000 <br />
x<sub>113</sub> + x<sub>213</sub> + x<sub>313</sub> + x<sub>413</sub>  ≥2000 <br />	
x<sub>114</sub> + x<sub>214</sub> + x<sub>314</sub> + x<sub>414</sub>  ≥3000 <br />
x<sub>115</sub> + x<sub>215</sub> + x<sub>315</sub> + x<sub>415</sub>  ≥1000 <br />
<br /> <br />

Supply	s<sub>i</sub> &emsp; where i=1,2,3,4
1. 200000	&emsp; 2. 100000	&emsp; 3. 50000	&emsp; 4. 50000

x<sub>11</sub> + x<sub>12</sub> + x<sub>13</sub> + x<sub>14</sub> + x<sub>15</sub> + x<sub>16</sub> + x<sub>17</sub> + x<sub>18</sub> + x<sub>19</sub> + x<sub>110</sub> + x<sub>111</sub> + x<sub>112</sub> + x<sub>113</sub> + x<sub>114</sub> + x<sub>115</sub>  ≤ 200000 <br /> 
x<sub>21</sub> + x<sub>22</sub> + x<sub>23</sub> + x<sub>24</sub> + x<sub>25</sub> + x<sub>26</sub> + x<sub>27</sub> + x<sub>28</sub> + x<sub>29</sub> + x<sub>210</sub> + x<sub>211</sub> + x<sub>212</sub> + x<sub>213</sub> + x<sub>214</sub> + x<sub>215</sub>  ≤ 100000 <br /> 
x<sub>31</sub> +x<sub>32</sub> + x<sub>33</sub> + x<sub>34</sub> + x<sub>35</sub> + x<sub>36</sub> + x<sub>37</sub> + x<sub>38</sub> + x<sub>39</sub> + x<sub>310</sub> + x<sub>311</sub> + x<sub>312</sub> + x<sub>313</sub> + x<sub>314</sub> + x<sub>315</sub> ≤ 50000 <br /> 
x<sub>41</sub> + x<sub>42</sub> + x<sub>43</sub> + x<sub>44</sub> + x<sub>45</sub> + x<sub>46</sub> + x<sub>47</sub> + x<sub>48</sub> + x<sub>49</sub> + x<sub>410</sub> + x<sub>411</sub> + x<sub>412</sub> + x<sub>413</sub> + x<sub>414</sub> + x<sub>415</sub> ≤ 50000 <br /> 


## Objective

Minimize the distance of traveling from node i to j.

Min z= ∑<sub>i</sub>∑<sub>j</sub>c<sub>ij</sub> x<sub>ij</sub> 

c<sub>11</sub>=173 	&emsp; c<sub>21</sub>=271	&emsp; c<sub>31</sub>=126	&emsp; c<sub>41</sub>=166 <br />
c<sub>12</sub>=121 	&emsp; c<sub>22</sub>=169	&emsp; c<sub>32</sub>=247	&emsp; c<sub>42</sub>=256 <br />
c<sub>13</sub>=249 	&emsp; c<sub>23</sub>=299	&emsp; c<sub>33</sub>=108	&emsp; c<sub>43</sub>=346 <br />
c<sub>14</sub>=366 	&emsp; c<sub>24</sub>=416	&emsp; c<sub>34</sub>=221	&emsp; c<sub>44</sub>=463 <br />
c<sub>15</sub>=166 	&emsp; c<sub>25</sub>=263	&emsp; c<sub>35</sub>=98	&emsp; c<sub>45</sub>=270 <br />
c<sub>16</sub>=187 	&emsp; c<sub>26</sub>=285	&emsp; c<sub>36</sub>=174	&emsp; c<sub>46</sub>=121 <br />
c<sub>17</sub>=179 	&emsp; c<sub>27</sub>=136	&emsp; c<sub>37</sub>=394	&emsp; c<sub>47</sub>=310 <br />
c<sub>18</sub>=259 	&emsp; c<sub>28</sub>=213	&emsp; c<sub>38</sub>=253	&emsp; c<sub>48</sub>=380 <br />
c<sub>19</sub>=31 	&emsp; c<sub>29</sub>=98	&emsp; c<sub>39</sub>=278	&emsp; c<sub>49</sub>=171 <br />
c<sub>110</sub>=55 	&emsp; c<sub>210</sub>=131	&emsp; c<sub>310</sub>=207	&emsp; c<sub>410</sub>=175 <br />
c<sub>111</sub>=100 &emsp; c<sub>211</sub>=26	&emsp; c<sub>311</sub>=339	&emsp; c<sub>411</sub>=231 <br />
c<sub>112</sub>=126 &emsp; c<sub>212</sub>=134	&emsp; c<sub>312</sub>=270	&emsp; c<sub>412</sub>=257 <br />
c<sub>113</sub>=124 &emsp; c<sub>213</sub>=222	&emsp; c<sub>313</sub>=199	&emsp; c<sub>413</sub>=77 <br />
c<sub>114</sub>=10 	&emsp; c<sub>214</sub>=107	&emsp; c<sub>314</sub>=240	&emsp; c<sub>414</sub>=132 <br />
c<sub>115</sub>=69 	&emsp; c<sub>215</sub>=166	&emsp; c<sub>315</sub>=210	&emsp; c<sub>415</sub>=101 <br />

## Formulation

Min z= 173x_11+ 121x_12+249x_13+366x_14+166x_15+187x_16+179x_17+259x_18+31x_19+55x_110+100x_111+126x_112+124x_113+10x_114+69x_115+271x_21+ 169x_22+299x_23+416x_24+263x_25+285x_26+136x_27+213x_28+98x_29+131x_210+26x_211+134x_212+222x_213+107x_214+166x_215+126x_31+247x_32+108x_33+221x_34+98x_35+174x_36+394x_37+253x_38+278x_39+207x_310+339x_311+270x_312+199x_313+240x_314+210x_315+166x_41+256x_42+346x_43+463x_44+270x_45+121x_46+310x_47+380x_48+171x_49+175x_410+231x_411+257x_412+77x_413+132x_414+101x_415

s.t.
x_11+ x_12+x_13+x_14+x_15+x_16+x_17+x_18+x_19+x_110+x_111+x_112+x_113+x_114+x_115  ≤200000 
x_21+ x_22+x_23+x_24+x_25+x_26+x_27+x_28+x_29+x_210+x_211+x_212+x_213+x_214+x_215  ≤100000 
x_31+x_32+x_33+x_34+x_35+x_36+x_37+x_38+x_39+x_310+x_311+x_312+x_313+x_314+x_315  ≤50000 
x_41+ x_42+x_43+x_44+x_45+x_46+x_47+x_48+x_49+x_410+x_411+x_412+x_413+x_414+x_415  ≤50000 
x_11+ x_21+ x_31+ x_41  ≥2000 		
x_12+ x_22+ x_32+ x_42  ≥20000 
x_13+ x_23+ x_33+ x_43  ≥49000 		
x_14+ x_24+ x_34+ x_44  ≥18000 
x_15+ x_25+ x_35+ x_45  ≥16000 		
x_16+ x_26+ x_36+ x_46  ≥6000 
x_17+ x_27+ x_37+ x_47  ≥4000 		
x_18+ x_28+ x_38+ x_48  ≥7000 
x_19+ x_29+ x_39+ x_49  ≥4000 		
x_110+ x_210+ x_310+ x_410  ≥4000 
x_111+ x_211+ x_311+ x_411  ≥6000	
x_112+ x_212+ x_312+ x_412  ≥3000 
x_113+ x_213+ x_313+ x_413  ≥2000	
x_114+ x_214+ x_314+ x_414  ≥3000 
x_115+ x_215+ x_315+ x_415  ≥1000 
x_11,x_12,x_13,x_14,x_15,x_16,x_17,x_18,x_19,x_110,x_111,x_112,x_113,x_114,x_115, 
x_21,x_22,x_23,x_24,x_25,x_26,x_27,x_28,x_29,x_210,x_211,x_212,x_213,x_214,x_215, 
x_31,x_32,x_33,x_34,x_35,x_36,x_37,x_38,x_39,x_310,x_311,x_312,x_313,x_314,x_315, 
x_41,x_42,x_43,x_44,x_45,x_46,x_47,x_48,x_49,x_410,x_411,x_412,x_413,x_414,x_415   ≥0  

