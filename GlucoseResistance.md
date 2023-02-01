### **Altered glucose metabolism**

The glucose metabolism can be altered in many ways, but two are very common. Pancreas not producing insulin and tissues being resistant to insulin. In this section you can change the model in such way and compare the output with the typical response you saw above.

In the liver, an important effect of insulin resistance is glycogenolysis not begin (that much) decreased by insulin. You can add this effect by increasing the 'IR liver' parameter.

In the muscle, insulin resistance means smaller glucose uptake and storage. You can reduce the muscle's sensitivity to insulin and the maximum insulin effect. Muscle glycogenolysis insulin resistance is separate and works like in the liver.

You can also decrease the pancreas' ability to release insulin.

For comparison, you can run both the altered (left graphs) and the typical (right graphs) metabolisms side by side.

Altered metabolism
<bdl-fmi id="fmi3" mode="continuous" src="GlucoseMetabolism_WholyBodyAlt.js" fminame="GlucoseMetabolism_WholyBodyAlt" tolerance="0.000001" starttime="0" fstepsize="10" guid="{0de8e515-f2d6-4555-a73a-3e1b90234ee4}" valuereferences="905971310,905971311,905971309,905971213,905971259,905971225,905971257" valuelabels="venous_glu,venous_ins,glucagon_C,liver_gly_to_g6p,muscle_glu_out,liver_glu_out,muscle_gly_to_g6p" inputs="id1,16777464,1,70,t;id2,16777218,1,10,t;id3,16777284,1,1,t;id4,16777216,1,1,t;id5,16777217,1,1,t;id6,16777219,1,1,t" inputlabels="glu_dose,ins_shift_liver,muscle.ins_shift,ins_res_r,ins_res_pr,alt_ins_release"></bdl-fmi>

Typical metabolism
<bdl-fmi id="fmi4" mode="continuous" src="GlucoseMetabolism_WholyBodyAlt.js" fminame="GlucoseMetabolism_WholyBodyAlt" tolerance="0.000001" starttime="0" fstepsize="10" guid="{0de8e515-f2d6-4555-a73a-3e1b90234ee4}" valuereferences="905971310,905971311,905971309,905971213,905971259,905971225,905971257" valuelabels="venous_glu,venous_ins,glucagon_C,liver_gly_to_g6p,muscle_glu_out,liver_glu_out,muscle_gly_to_g6p" inputs="id1,16777464,1,70,t" inputlabels="glu_dose"></bdl-fmi>


<bdl-range id="id2" title="IR liver" min="1" max="3" default="0" step="0.001"></bdl-range>

<bdl-range id="id6" title="Pancreas Ins. Production" min="0.1" max="1" default="1" step="0.1"></bdl-range>

<bdl-range id="id3" title="IR Muscle Glycogenolysis" min="0" max="2" default="0" step="0.2"></bdl-range>

<bdl-range id="id5" title="Muscle Insulin Max. Effect" min="0" max="1" default="1" step="0.1"></bdl-range>

<bdl-range id="id4" title="Muscle Ins. Insensivity" min="0" max="5" default="0" step="0.1"></bdl-range>


Glycogen breakdown needs to be reduced based on glucose levels. Reducing the sensitivity to insulin of this process still allows for full suppression during very high glucose levels, but during normal glucose levels the glycogen breakdown is too high. This causes increased blood glucose levels.

<bdl-chartjs-time width="300" height="200" fromid="fmi3" labels="Liver glycogen breakdown" initialdata="" refindex="3"
refvalues="1" min = 0 max = 300 ></bdl-chartjs-time><bdl-chartjs-time width="300" height="200" fromid="fmi4" labels="Liver glycogen breakdown" initialdata="" refindex="3"
refvalues="1"
min = 0 max = 300></bdl-chartjs-time>

Similarly to the liver, muscle can also show insulin resistance. This can be seen through reduced uptake and storage. You can see the changes you made in the glycogen breakdown and in the total uptake of glucose.

<bdl-chartjs-time width="300" height="200" fromid="fmi3" labels="Breakdown, Uptake" initialdata="" refindex="6,4"
refvalues="2" min = 0 max = 400 ></bdl-chartjs-time><bdl-chartjs-time width="300" height="200" fromid="fmi4" labels="Breakdown, Uptake" initialdata="" refindex="6,4"
refvalues="2"
min = 0 max = 400></bdl-chartjs-time>


You can have an overview of the blood glucose and insulin in these graphs. The units are chosen to fit glucose and insulin into one graph.

<bdl-chartjs-time width="300" height="200" fromid="fmi3" labels="Glucose, Insulin" initialdata="" refindex="0"
refvalues="2" min = 0 max = 10 convertors="1,87;1,1.3"></bdl-chartjs-time><bdl-chartjs-time width="300" height="200" fromid="fmi4" labels="Glucose, Insulin" initialdata="" refindex="0"
refvalues="2"
convertors="1,87;1,1.3"
min = 0 max = 10></bdl-chartjs-time>

