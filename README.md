# Transportation_Problem

East Food company has 4 warehouses that are in Savannah, Charleston, Columbus, and Jacksonville.  The company ships goods from these warehouses to the nearby cities.  The table 4 shows the distances between warehouses and cities, in miles.  Table 5 shows the quantities that warehouse cities supply.  Table 6 shows the demand in cities. <br /> <br />

![Table 4](https://user-images.githubusercontent.com/59415488/177019361-dc1208b6-1261-4d63-a421-f4cd6e377ebc.jpg)
![Table 5](https://user-images.githubusercontent.com/59415488/177019367-2a7b0766-eb58-48af-97eb-2a872352c340.jpg)
![Table 6](https://user-images.githubusercontent.com/59415488/177019370-2f43e3e8-379e-4430-aec0-c6200a151660.jpg)

## Problem Formation

The transportation proble decides from which supplier to which retailer and the quantity to transport. <br />
![Pic 001](https://user-images.githubusercontent.com/59415488/177240184-b156a520-df10-4d57-add2-999cf3fd14f8.jpg)

## Variables

Suppliers	i=1,2,3,4
  1. Savannah	&emsp;	2. Charleston	&emsp;	3. Columbus	&emsp;	4. Jacksonville

Retailers	j=1,2,3,4,5,6,7,8,9,10,11,12,13,14,15
  ..1. Tifton	&emsp;	2. Augusta	&emsp;	3. Atlanta	&emsp;	4. Chattanooga
  ..5. Macon	&emsp;	6. Valdosta	&emsp;	7. Florence	&emsp;	8. Greenville
  ..9. Hilton Head	&emsp; 10. Statesboro	&emsp; 11. Summerville	&emsp; 12. Aikens
  ..13. Waycross	&emsp; 14. Pooler		&emsp; 15. Jessup
  
![Pic 002](https://user-images.githubusercontent.com/59415488/177240325-b893c4db-573a-4279-b28a-dbcb4b54cbd7.jpg)
<br /> <br />
## Constraints
Constraints are formed for every demand node and supply node. The are of the following form: <br />
Demand Node: &emsp; ∑<sub>i</sub><sup>n</sup>x<sub>ij</sub> ≥ d<sub>j</sub>


Demand	d<sub>j</sub> where j=1,2,3,4,5,6,7,8,9,10,11,12,13,14,15
..1. 2000	&emsp; 2. 20000	&emsp; 3. 49000	&emsp; 4. 18000	&emsp; 5. 16000
..6. 6000	&emsp; 7. 4000	&emsp; 8. 7000	&emsp; 9. 4000	&emsp; 10. 4000
..11. 6000	&emsp; 12. 3000	&emsp; 13. 2000	&emsp; 14. 3000	&emsp; 15. 1000

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

Min z = 173x<sub>11</sub> + 121x<sub>12</sub> + 249x<sub>13</sub> + 366x<sub>14</sub> + 166x<sub>15</sub> + 187x<sub>16</sub> + 179x<sub>17</sub> + 259x<sub>18</sub> + 31x<sub>19</sub> + 55x<sub>110</sub> + 100x<sub>111</sub> + 126x<sub>112</sub> + 124x<sub>113</sub> + 10x<sub>114</sub> + 69x<sub>115</sub> + 271x<sub>21</sub> + 169x<sub>22</sub> + 299x<sub>23</sub> + 416x<sub>24</sub> + 263x<sub>25</sub> + 285x<sub>26</sub> + 136x<sub>27</sub> + 213x<sub>28</sub> + 98x<sub>29</sub> + 131x<sub>210</sub> + 26x<sub>211</sub> + 134x<sub>212</sub> + 222x<sub>213</sub> + 107x<sub>214</sub> + 166x<sub>215</sub> + 126x<sub>31</sub> + 247x<sub>32</sub> + 108x<sub>33</sub> + 221x<sub>34</sub> + 98x<sub>35</sub> + 174x<sub>36</sub> + 394x<sub>37</sub> + 253x<sub>38</sub> + 278x<sub>39</sub> + 207x<sub>310</sub> +
        339x<sub>311</sub> + 270x<sub>312</sub> + 199x<sub>313</sub> + 240x<sub>314</sub> + 210x<sub>315</sub> + 166x<sub>41</sub> + 256x<sub>42</sub> + 346x<sub>43</sub> + 463x<sub>44</sub> + 270x<sub>45</sub> + 121x<sub>46</sub> + 310x<sub>47</sub> + 380x<sub>48</sub> + 171x<sub>49</sub> + 175x<sub>410</sub> +   231x<sub>411</sub> + 257x<sub>412</sub> + 77x<sub>413</sub> + 132x<sub>414</sub> + 101x<sub>415</sub><br />

s.t. <br /> <br />
x<sub>11</sub> + x<sub>12</sub> + x<sub>13</sub> + x<sub>14</sub> + x<sub>15</sub> + x<sub>16</sub> + x<sub>17</sub> + x<sub>18</sub> + x<sub>19</sub> + x<sub>110</sub> + x<sub>111</sub> + x<sub>112</sub> + x<sub>113</sub> + x<sub>114</sub> + x<sub>115</sub>  ≤200000 <br />
x<sub>21</sub> + x<sub>22</sub> + x<sub>23</sub> + x<sub>24</sub> + x<sub>25</sub> + x<sub>26</sub> + x<sub>27</sub> + x<sub>28</sub> + x<sub>29</sub> + x<sub>210</sub> + x<sub>211</sub> + x<sub>212</sub> + x<sub>213</sub> + x<sub>214</sub> + x<sub>215</sub>  ≤100000 <br />
x<sub>31</sub> +x<sub>32</sub> + x<sub>33</sub> + x<sub>34</sub> + x<sub>35</sub> + x<sub>36</sub> + x<sub>37</sub> + x<sub>38</sub> + x<sub>39</sub> + x<sub>310</sub> + x<sub>311</sub> + x<sub>312</sub> + x<sub>313</sub> + x<sub>314</sub> + x<sub>315</sub>  ≤50000 <br />
x<sub>41</sub> + x<sub>42</sub> + x<sub>43</sub> + x<sub>44</sub> + x<sub>45</sub> + x<sub>46</sub> + x<sub>47</sub> + x<sub>48</sub> + x<sub>49</sub> + x<sub>410</sub> + x<sub>411</sub> + x<sub>412</sub> + x<sub>413</sub> + x<sub>414</sub> + x<sub>415</sub>  ≤50000 <br />
x<sub>11</sub> + x<sub>21</sub> + x<sub>31</sub> + x<sub>41</sub>  ≥2000 <br /> 		
x<sub>12</sub> + x<sub>22</sub> + x<sub>32</sub> + x<sub>42</sub>   ≥20000 <br />
x<sub>13</sub> + x<sub>23</sub> + x<sub>33</sub> + x<sub>43</sub>  ≥49000 <br />		
x<sub>14</sub> + x<sub>24</sub> + x<sub>34</sub> + x<sub>44</sub>  ≥18000 <br />
x<sub>15</sub> + x<sub>25</sub> + x<sub>35</sub> + x<sub>45</sub>  ≥16000 <br />		
x<sub>16</sub> + x<sub>26</sub> + x<sub>36</sub> + x<sub>46</sub>  ≥6000 <br />
x<sub>17</sub> + x<sub>27</sub> + x<sub>37</sub> + x<sub>47</sub>  ≥4000 <br />		
x<sub>18</sub> + x<sub>28</sub> + x<sub>38</sub> + x<sub>48</sub>   ≥7000 <br />
x<sub>19</sub> + x<sub>29</sub> + x<sub>39</sub> + x<sub>49</sub>  ≥4000 <br />		
x<sub>110</sub> + x<sub>210</sub> + x<sub>310</sub> + x<sub>410</sub>  ≥4000 <br />
x<sub>111</sub> + x<sub>211</sub> + x<sub>311</sub> + x<sub>411</sub>  ≥6000	<br />
x<sub>112</sub> + x<sub>212</sub> + x<sub>312</sub> + x<sub>412</sub>  ≥3000 <br />
x<sub>113</sub> + x<sub>213</sub> + x<sub>313</sub> + x<sub>413</sub>  ≥2000	<br />
x<sub>114</sub> + x<sub>214</sub> + x<sub>314</sub> + x<sub>414</sub>  ≥3000 <br />
x<sub>115</sub> + x<sub>215</sub> + x<sub>315</sub> + x<sub>415</sub>  ≥1000 <br />
x<sub>11</sub>, x<sub>12</sub>, x<sub>13</sub>, x<sub>14</sub>, x<sub>15</sub>, x<sub>16</sub>, x<sub>17</sub>, x<sub>18</sub>, x<sub>19</sub>, x<sub>110</sub>, x<sub>111</sub>, x<sub>112</sub>, x<sub>113</sub>, x<sub>114</sub>, x<sub>115</sub>, x<sub>21</sub>, x<sub>22</sub>, x<sub>23</sub>, x<sub>24</sub>, x<sub>25</sub>, x<sub>26</sub>, x<sub>27</sub>, x<sub>28</sub>, x<sub>29</sub>, x<sub>210</sub>, x<sub>211</sub>, x<sub>212</sub>, x<sub>213</sub>, x<sub>214</sub>, x<sub>215</sub>, x<sub>31</sub>, x<sub>32</sub>, x<sub>33</sub>, x<sub>34</sub>, x<sub>35</sub>, x<sub>36</sub>, x<sub>37</sub>, x<sub>38</sub>, x<sub>39</sub>, x<sub>310</sub>, x<sub>311</sub>, x<sub>312</sub>, x<sub>313</sub>, x<sub>314</sub>, x<sub>315</sub>, x<sub>41</sub>, x<sub>42</sub>, x<sub>43</sub>, x<sub>44</sub>, x<sub>45</sub>, x<sub>46</sub>, x<sub>47</sub>, x<sub>48</sub>, x<sub>49</sub>, x<sub>410</sub>, x<sub>411</sub>, x<sub>412</sub>, x<sub>413</sub>, x<sub>414</sub>, x<sub>415</sub>   ≥ 0  

