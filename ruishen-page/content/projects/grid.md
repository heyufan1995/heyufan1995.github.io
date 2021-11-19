{
  "title": "Paradigm Design for Grid Cell Study",
  "date": "2016-11-01",
  "image": "/img/grid-city.png",
  "description": "This is my bachelor graduation project in 2016. Inspired by the paper \"<em>Grid-cell representations in mental simulation\"</em> published in August 2016, I was thinking if grid-like representations can be activated given more abstract and simple cues, and can be detected using fMRI. The motivation was to simplify the original experimental paradigm and make it possible to use in wider clinical trails and measurements. I first implemented the navigation task in virtual-reality city using Unity3D, repeated the results in the paper. Then based on my assumption, I designed a modified paradigm using PyQt, which only kept the location relationship in previous task and represented them in 2D plane, without other 3D visual cues. I was awarded Outstanding Graduation Project in June 2017.",
  "tags": ["Grid Cell","fMRI","Paradigm Design","Unity3D","Python","PyQt","Matlab","SPM","DPABI"],
  "fact": "",
  "featured":true
}
<h3>Overview</h3>
<p>
This is my bachelor graduation project in 2016. Inspired by Bellmund's paper "<em>Grid-cell representations in mental simulation"</em> published in August 2016, I was thinking if grid-like representations can be activated given more abstract and simple cues, and can be detected using fMRI. The motivation was to simplify the original experimental paradigm from the paper, in order to make it possible to use in wider clinical trails and measurements. In my graduation project, I first implemented the navigation task in virtual-reality city using Unity3D. By analyzing fMRI signals of subjects conducting the task, we observed the sinusoidal signals as a function of moving direction successfully, which confirmed the recent published discovery of grid cell firing pattern. Then I designed a modified paradigm using PyQt based on my assumption, which only kept the location relationship in previous task and represented them in 2D plane, without other 3D visual cues. we collected fMRI data of 10 subjects and conducted the same analyzation using DPABI and SPM, among which 9 subjects had positive activation. I was awarded Outstanding Graduation Project in June 2017.
</p>

<h3>Spatial navigation in virtual reality environment</h3>
<p>
<div style="width: 30%; float: right;"><video controls autoplay="yes" width="100%" poster="/img/grid-car.png" src="/files/task3D.mp4"></video></div>
This spatial navigation task was based on the experiment in Bellmund's paper "<em>Grid-cell representations in mental simulation"</em>. I created a virtual reality environment using Unity3D, computer graphics engine. In this city-view virtual reality environment, we put objects (sculpture, car, phone booth, etc.) at vertices (red points) of hexagons as shown in Fig 1, and we set an another object (billboard) at the center of the city (yellow point) as the departure location. Subjects explore the virtual reality city and memorize the location of the objects in the training phase. In the testing phase, they conduct spatial memory task illustrated in Fig 2, and their brain signals are recorded using fMRI in the meantime. We repeated the results in the paper, suggesting that the activation pattern has highest similarity when imagine spatial direction at 0 degree modulo 60 degree condition, and has lowest similarity at 30 degree modulo 60 degree condition.
</p>
<figure>
	<img height=280 src="/img/grid-cityview.png" alt="overview of virtual reality city">
	<figcaption>Fig 1. Overview of the virtual reality city</figcaption>
</figure>
<figure>
	<img height=280 src="/img/grid-citytask.png" alt="VR city navigation task">
	<figcaption>Fig 2. Spatial navigation task in virtual reality environment</figcaption>
</figure>
<h3>Spatial memory task with 2D abstract cues</h3>
<p>
<div style="width: 40%; float: right; text-align: center">
	<img src="/img/grid-2dview.png" alt="overview of virtual reality city">
	<figcaption>Fig 3. Overview of the 2D environment</figcaption>
</div>
In this spatial memory task, we kept the location relationship of the objects and illustrated then using only 2D abstract cues (basic geometric shape) as shown in Fig 3. We used yellow circle representing the refference object, red circles representing the target objects, green circles at the center of the view representing the location of subjects themselves, and the green triangular pointing their facing direction. In the training phase, subjects can move and rotate in the 2D abstract environment as shown in Fig 4. Only a limited view (area in the big sector) is available during their movement while the remaining part is shaded. In the testing phase, subjects first learn the location relationship between reference object (yellow circle), target object (red circle) and themselves (green circle). Then a reference object will appear on the screen and subject need to adjust their facing direction according to previouly learned relationship. After that, subjects need to estimate the position of the target object based on their current facing direction. In the feedback phase, subject provide their confidence level and the correct direction of objects will appear on the screen. This paradigm was implemented using PyQt.
</p>
<figure>
	<img height=150 width=180 src="/img/grid-move.gif" loop=infinite alt="Training phase of 2D abstract environment (move)">
	<img height=150 width=180 src="/img/grid-rotate.gif" loop=infinite alt="Training phase of 2D abstract environment (rotate)">
	<figcaption>Fig 4. Training phase of 2D abstract environment (move/rotate)</figcaption>
</figure>
<figure>
	<img height=150 src="/img/grid-learn.gif" loop=infinite alt="Testing phase of 2D spatial memory task (learn)">
	<img height=150 src="/img/grid-test.gif" loop=infinite alt="Testing phase of 2D spatial memory task (test)">
	<figcaption>Fig 5. Testing phase of 2D spatial memory task (learn/test)</figcaption>
</figure>
<div style="width: 100%; text-align: center">
	<img height=400 src="/img/grid-2dtask.jpg" alt="Spatial memory task with 2D abstract cues">
	<figcaption>Fig 6. Spatial memory task with 2D abstract cues</figcaption>
</div>
<h3>fMRI recording</h3>
<p>
We collected fMRI data of 10 subjects and conducted analyzation using DPABI and SPM, among which 9 subjects had significat activation (P=0.01) at entorhinal cortex (EC) during the spatial memory task in 2D abstract environment. Fig 7 shows an example EC activation of a subject.
</p>
<div style="width: 60%; float:left; text-align: center;">
	<img height=250 src="/img/grid-fmri.png" alt="fmri recordings">
	<img height=250 src="/img/grid-fmrico.png" alt="fmri recordings">
	<figcaption>Fig 7. fMRI recordings of entorhinal cortex (P=0.01)</figcaption>
</div>
<div style="width: 40%; float: right; text-align: center;">
	<img height=250 src="/img/grid-fmrimod.png" alt="VR city navigation task">
	<figcaption>Fig 8. Angle modulo 60 degree activation pattern</figcaption>
</div>
<p>
We compare the correlation coefficients of EC activations of trial pairs respect to their angular difference (in modulo 60 degree condition) of sampled testing directions. The results in Fig 8 show that angular difference at 0 degree has highest similarity, while angular difference at 30 degree has lowest similarity. The firing rate of the hypothetical response of the grid cell as a function of direction, showing a 60 degree modulation. According to this grid cell model, we can expect 60 degree modulation of fMRI pattern similarity values when comparing trial pairs based on the angular difference of their sampled testing directions. Our results satisfied the expectation.
</p>