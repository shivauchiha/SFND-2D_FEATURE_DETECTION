Write up for MP0.

----------------------MP1-------------------
This problem is tackled by observing the size of the buffer , when we know the buffer has exceeded
the size limit we drop one image and add one more image.
checking is done using if conditional statements , where as the removing and pushing of image is done using 
vector functions push_back and erase.

---------------------MP2--------------------
The selectability template was already given by the starter code . we basically check for what detector name does the string object Detector type has we basically implement as set of if else control statements by using string types .compare() function.
Under each if conditions we instantiate a detector object whose type is determined by detectortype string object. using opencv docs we can find class definition and fuctionalities of respective detectors. Usually all detectors have function called detect() which is called to compute keypoints and returned by reference to main code.
--------------------MP3---------------------
This is important because it reduces unnecessary computations when performing description operation how ? well we only need to track keypoints associated with vechile in the front for ttc , we dont need to track roads . Thus we usually try to remove keypoints outside the bounding box enclosing the vehicle. In our case the bounding box was explicitly given , However i assume in future these bounding boxes will be given by a DNN.
The filtering of points outside bounding box is done by using .contains() function of a cv::rect object. If it satisfies the keypoint is pushed into vector and this replaces the original keypoint vector.
--------------------MP4----------------------
This similar to what was done in MP2 check the decriptortype string object and accordingly instantiate the extractor class object the information regarding the function can be found in opencv documentation.All extractor class share compute() option which computes the required descriptor.
--------------------MP5&MP6----------------------
Flann is implemented by instantiation a FLANNBASED descriptor matcher , The depending upon selectortype given by user a match()/knnmatch() is called they represent nearest neighbour and k nearest neigbour match function respectively.
The distance ratio filter looks at the distance of a candidate matched key points the pairs with minimum distance is chosen as best candidate.In our case a threshold of 0.8 was applied.good for removing false positives.
-------------------------------------------
MP7&MP8&MP9  are analysed in xlxs file MP7.XLSX ,MP8&9.XLSX . The results are recorded as excel and the analysis and decision logic is explained within the textbox placed within the respective xlsx files.  


Thank you for your time !

