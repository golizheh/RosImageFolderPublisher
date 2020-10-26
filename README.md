# ROS Image Publisher

This node publishes all the images contained in an specified folder, in the specified topic.
The images will be published in BGR8 format.

## Setup

1. Clone this repo `git clone https://github.com/golizheh/RosImageFolderPublisher`
1. Change to repo dir `cd RosImageFolderPublisher`
1. Execute `catkin_make`
1. Source the workspace `source devel/setup.bash`

If you want to integrate this into another catkin workspace, just copy the `image_folder_publisher` into the `src` target workspace.

## How to Launch

Once in a sourced terminal, execute:
`rosrun image_folder_publisher image_folder_publisher.py`

### Example

`rosrun image_folder_publisher image_folder_publisher.py _image_folder:=/PATH/Images _topic_name=/image_topic`

## Notes

* Invalid files will be skipped. The supported image formats will correspond to the ones supported by CvBridge and OpenCV.
* Publish Rate will depend on the speed of the Hard disk. 
