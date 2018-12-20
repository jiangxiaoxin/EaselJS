# FauxCanvas

Can be passed to a Stage in place of a Canvas element in order to eliminate the browser-specific cost of drawing graphics to screen, and thereby isolate the time spent in EaselJS.
Still rough, and may be missing methods or properties that are necessary for certain features in EaselJS. See the code and example for more details.

	var stage = new createjs.Stage(new FauxCanvas(500, 400));

	这个类有什么用？他根本不具备绘图的能力呀，要了干嘛呢？
	
	它把所有跟绘图有关的属性和方法都置空了，也就是在传入Stage后，项目开始要各种计算以用来绘图显示的时候，它走的都是空方法，这样的调用有何意义？还做了测试，跟真正的canvas去比较消耗的时间,玩呢？
