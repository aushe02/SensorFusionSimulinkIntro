# SensorFusionSimulinkIntro

## [Video 1](https://www.youtube.com/watch?v=6qV3YjFppuc&list=PL8z3JLwN_PhGPR0FMGy1xcl_kja2HBIQV&index=1&t=2s)
* Sensor Fusion - Combinding two or more data sources in a way that generates a better understanding of the system
* Physical World -> Sense -> Percieve -> Plan -> Act
  * Sense   
  * Percieve
    * self-awareness: localization and positioning
    * situational awareness: detection and tracking 
  * Plan
  * Act
* 4 Applications for sensor fustion
  * Increase the quality of the data
    * Sensor data is noisy ex use two accel and fuse data together 4 sensors = 1/2 noise
    * Reduce noise with two different sensor types ex gyro and mag (Common filter ex Kalman Filter)
  * Increase Relibility
    * Backup if a sensor fails
    * Could use three sensors have to be careful of single failure that can happen to all sensors (GPS, wind model)
  * It can be used to estimate unmeasured states
    * Gyro and Accel to measure distance
  * Used to increase coverage areas
    * Cars with multiple proximity sensors   

## [Video 2](https://www.youtube.com/watch?v=0rlvvYgmTvI&list=PL8z3JLwN_PhGPR0FMGy1xcl_kja2HBIQV&index=2)
* Focus on using magnetometer, accelerometer, gyro
* Orientation is decribed as a rotation
  * Referance frame
  * Specify rotation
    * Roll, pitch yaw
    * Direction cosine matrix (DCM)
    * Quaternion
    * Represent a 3d rotation between two coordinate frames
* North, East, Down
* Mag
  * Hard iron source - generates own magnetic field
    * Magnet
    * Coil  
    * Distortion circle
  * Soft iron source - does not generate it's own magnetic field is magnetic
    *  Nail
    *  Structural elements
    *  Distortion oval
  * Mag Calibration 
    * Perfect system would be a cirlce correct by finding offset using transformation matrix and bias
    * Phone move in circle before using compass
  * Fix corrupting linear acceleration
    * Run through model to extimate linear acceleration
      * Drone
      * ignore outside of threshold
  * Add a gyro to measure angular rate of system   
  * Mag, accel, and gyro packed together as IMU
  * Gryo Measurment
    * equation
  * Dead reckoning
    * Downsides
      * Need to know inital orientation
      * Sensors aren't perfect still have noise (need more than 2 sensors)
  * Use sensor fusion to combind accel + mag + gryo
    * Algorithms
      * Complementary
      * Kalman
      * Madgwick
      * Mahony
     * Initalize Altitude
     * Use mag field and gravity to correct gryo drift
     * Accel + mag |-----------------------------------------------------------| gyro               

## [Video 3](https://www.youtube.com/watch?v=hN8dL55rP5I&t=0s)

## [Video 4](https://www.youtube.com/watch?v=hJG08iWlres&t=0s)

## [Video 5](https://www.youtube.com/watch?v=IIt1LHIHYc4&t=0s)
