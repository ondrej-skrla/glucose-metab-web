### **Glucose gets cycled**

The higher glucose uptake also produces higher lactate concentration in the blood. This increased lactate concentration means that tissues like liver will take in more lactate and if not inhibited by insulin, they will produce glucose from it. This cycling of glucose to lactate and back is called the Cori cycle and in this case serves as a buffer - another way to deal with excessive glucose.

<bdl-fmi id="fmi2" mode="continuous" src="GlucoseMetabolism_WholyBodyAlt.js" fminame="GlucoseMetabolism_WholyBodyAlt" tolerance="0.001" starttime="0" fstepsize="10" guid="{0de8e515-f2d6-4555-a73a-3e1b90234ee4}" valuereferences="905971271,905971264,905971265,905971266,905971272,905971226,905971310,905971022" valuelabels="adipose_glu_out,adipose_g6p_to_g3p,adipose_g3p_to_pyr,adipose_pyr_to_lac,adipose_lac_out,liver_lac_out,venous_glu,heart_lac_C" inputs="id1,16777464,1,70,t" inputlabels="glu_dose"></bdl-fmi>

<bdl-range id="id1" title="glucose dose [g]" min="0" max="70" default="35" step="5"></bdl-range>

To give an overview, below is the venous glucose concentration. 

<bdl-chartjs-time width="300" height="200" fromid="fmi2" labels="Venous Glucose" initialdata="" refindex="6" refvalues="1" min = 40 max = 600 ></bdl-chartjs-time>

One of the tissues that are affected by insulin to uptake more glucose is the adipose tissue. However, adipose tissue cannot store that much glucose and releases it as lacate. The process of converting glucose to lactate is called glycolysis. You can see how the initial inflow of glucose leads to the increased outflow (more negative) of lactate.

<bdl-chartjs-time width="300" height="200" fromid="fmi2" labels="Glucose in, G6P to G3P, PYR to LAC, Lactate out" initialdata="" refindex="0,1,3,4" refvalues="4"></bdl-chartjs-time>

This extra lactate is one of the reasons for the increased lactate arterial levels.

<bdl-chartjs-time width="300" height="200" fromid="fmi2" labels="Arterial lactate" initialdata="" refindex="7"
refvalues="1"
min = 9
max = 15></bdl-chartjs-time>

As described in the beggining, you can see that liver takes up more lactate. Some of this lactate will be used to produce glucose, closing the loop.

<bdl-chartjs-time width="300" height="200" fromid="fmi2" labels="Liver lactate in" initialdata="" refindex="5" min="25" max="40"
refvalues="1"></bdl-chartjs-time>
