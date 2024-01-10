# Lab 2: Joint Creation and Hierarchy Setup:

## Assets
If you would like to look at the assets used in this lab, you can find them in the [Assets](../Assets/) folder found in the root directory of this repository.

### Files
- `Character_Rig.ma`
- `Trebuchet.ma`

## Youtube Link
[![Lab 2](https://i9.ytimg.com/vi/pCONenaOqdo/mq1.jpg?sqp=CLTi-KwG-oaymwEmCMACELQB8quKqQMa8AEB-AHUBoAC4AOKAgwIABABGFkgWShZMA8%3D&rs=AOn4CLDb3u4Ja7Xtcq6veM4ZFXmM8pELMQ&retry=4)](https://youtu.be/pCONenaOqdo)

## Character Rig Recap
The character rig is a bipedal rig with a few extra features. The rig has FK, IK, and RK controls for the arms and legs. With an additional IK twist system to help the limbs deform correctly. There are also attributes that perform some joint actions through the use of driven keys tied to the Transorm_Ctrl and the Foot_Ctrl's.
<details>
    <summary>Joint Hierarchy: Character Rig</summary>

<pre><code>|- COG_FK_Jnt
     |-- Spine_01_FK_Jnt
          |-- Spine_02_FK_Jnt
               |-- Spine_03_FK_Jnt
                    |-- Head_01_FK_Jnt
                         |-- Head_02_FK_Jnt
                              |-- Head_03_FK_Jnt
                    |-- L_Clav_FK_Jnt
                         |-- L_Arm_01_FK_Jnt
                              |-- L_Arm_02_FK_Jnt
                                   |-- L_Arm_03_FK_Jnt
                         |-- L_Arm_01_IK_Jnt
                              |-- L_Arm_02_IK_Jnt
                                   |-- L_Arm_03_IK_Jnt
                         |-- L_Arm_01_RK_Jnt
                              |-- L_Arm_02_RK_Jnt
                                   |-- L_Arm_03_RK_Jnt
                                        |-- L_Hand_FK_Jnt
                                             |-- L_Finger_01_Knuckle_01_FK_Jnt
                                                  |-- L_Finger_01_Knuckle_02_FK_Jnt
                                                       |-- L_Finger_01_Knuckle_03_FK_Jnt
                                                            |-- L_Finger_01_Knuckle_04_FK_Jnt
                                             |-- L_Finger_02_Knuckle_01_FK_Jnt
                                                  |-- L_Finger_02_Knuckle_02_FK_Jnt
                                                       |-- L_Finger_02_Knuckle_03_FK_Jnt
                                                            |-- L_Finger_02_Knuckle_04_FK_Jnt
                                             |-- L_Finger_03_Knuckle_01_FK_Jnt
                                                  |-- L_Finger_03_Knuckle_02_FK_Jnt
                                                       |-- L_Finger_03_Knuckle_03_FK_Jnt
                                                            |-- L_Finger_03_Knuckle_04_FK_Jnt
                                             |-- L_Finger_04_Knuckle_01_FK_Jnt
                                                  |-- L_Finger_04_Knuckle_02_FK_Jnt
                                                       |-- L_Finger_04_Knuckle_03_FK_Jnt
                                                            |-- L_Finger_04_Knuckle_04_FK_Jnt
                                             |-- L_Finger_05_Knuckle_01_FK_Jnt
                                                  |-- L_Finger_05_Knuckle_02_FK_Jnt
                                                       |-- L_Finger_05_Knuckle_03_FK_Jnt
                                                            |-- L_Finger_05_Knuckle_04_FK_Jnt
                                   |-- L_ForeArm_Twist_01_Jnt
                                   |-- L_ForeArm_Twist_02_Jnt
                              |-- L_Upper_Arm_Twist_01_Jnt
                              |-- L_Upper_Arm_Twist_02_Jnt
                              |-- L_Upper_Arm_Twist_01_Corrective_Jnt
                    |-- R_Clav_FK_Jnt
                         |-- R_Arm_01_FK_Jnt
                              |-- R_Arm_02_FK_Jnt
                                   |-- R_Arm_03_FK_Jnt
                         |-- R_Arm_01_IK_Jnt
                              |-- R_Arm_02_IK_Jnt
                                   |-- R_Arm_03_IK_Jnt
                         |-- R_Arm_01_RK_Jnt
                              |-- R_Arm_02_RK_Jnt
                                   |-- R_Arm_03_RK_Jnt
                                        |-- R_Hand_FK_Jnt
                                             |-- R_Finger_01_knuckle_01_FK_Jnt
                                                  |-- R_Finger_01_knuckle_02_FK_Jnt
                                                       |-- R_Finger_01_knuckle_03_FK_Jnt
                                                            |-- R_Finger_01_knuckle_04_FK_Jnt
                                             |-- R_Finger_02_knuckle_01_FK_Jnt
                                                  |-- R_Finger_02_knuckle_02_FK_Jnt
                                                       |-- R_Finger_02_knuckle_03_FK_Jnt
                                                            |-- R_Finger_02_knuckle_04_FK_Jnt
                                             |-- R_Finger_03_knuckle_01_FK_Jnt
                                                  |-- R_Finger_03_knuckle_02_FK_Jnt
                                                       |-- R_Finger_03_knuckle_03_FK_Jnt
                                                            |-- R_Finger_03_knuckle_04_FK_Jnt
                                             |-- R_Finger_04_knuckle_01_FK_Jnt
                                                  |-- R_Finger_04_knuckle_02_FK_Jnt
                                                       |-- R_Finger_04_knuckle_03_FK_Jnt
                                                            |-- R_Finger_04_knuckle_04_FK_Jnt
                                             |-- R_Finger_05_knuckle_01_FK_Jnt
                                                  |-- R_Finger_05_knuckle_02_FK_Jnt
                                                       |-- R_Finger_05_knuckle_03_FK_Jnt
                                                            |-- R_Finger_05_knuckle_04_FK_Jnt
                                   |-- R_ForeArm_Twist_01_Jnt
                                   |-- R_ForeArm_Twist_02_Jnt
                              |-- R_Upper_Arm_Twist_01_Jnt
                              |-- R_Upper_Arm_Twist_02_Jnt
                              |-- R_Upper_Arm_Twist_01_Corrective_Jnt
     |-- Pelvis_FK_Jnt
          |-- L_Leg_Clav_FK_Jnt
               |-- L_Leg_01_FK_Jnt
                    |-- L_Leg_02_FK_Jnt
                         |-- L_Leg_03_FK_Jnt
                              |-- L_Foot_01_FK_Jnt
                                   |-- L_Foot_02_FK_Jnt
                                        |-- L_Foot_03_FK_Jnt
               |-- L_Leg_01_IK_Jnt
                    |-- L_Leg_02_IK_Jnt
                         |-- L_Leg_03_IK_Jnt
                              |-- L_Foot_01_IK_Jnt
                                   |-- L_Foot_02_IK_Jnt
                                        |-- L_Foot_03_IK_Jnt
               |-- L_Leg_01_RK_Jnt
                    |-- L_Leg_02_RK_Jnt
                         |-- L_Leg_03_RK_Jnt
                              |-- L_Foot_01_RK_Jnt
                                   |-- L_Foot_02_RK_Jnt
                                        |-- L_Foot_03_RK_Jnt
                         |-- L_Lower_Leg_Twist_01_Jnt
                         |-- L_Lower_Leg_Twist_02_Jnt
                    |-- L_Upper_Leg_Twist_01_Jnt
                    |-- L_Upper_Leg_Twist_02_Jnt
                    |-- L_Upper_Leg_Twist_01_Corrective_Jnt
          |-- R_Leg_Clav_FK_Jnt
               |-- R_Leg_01_FK_Jnt
                    |-- R_Leg_02_FK_Jnt
                         |-- R_Leg_03_FK_Jnt
                              |-- R_Foot_01_FK_Jnt
                                   |-- R_Foot_02_FK_Jnt
                                        |-- R_Foot_03_FK_Jnt
               |-- R_Leg_01_IK_Jnt
                    |-- R_Leg_02_IK_Jnt
                         |-- R_Leg_03_IK_Jnt
                              |-- R_Foot_01_IK_Jnt
                                   |-- R_Foot_02_IK_Jnt
                                        |-- R_Foot_03_IK_Jnt
               |-- R_Leg_01_RK_Jnt
                    |-- R_Leg_02_RK_Jnt
                         |-- R_Leg_03_RK_Jnt
                              |-- R_Foot_01_RK_Jnt
                                   |-- R_Foot_02_RK_Jnt
                                        |-- R_Foot_03_RK_Jnt
                         |-- R_Lower_Leg_Twist_01_Jnt
                         |-- R_Lower_Leg_Twist_02_Jnt
                    |-- R_Upper_Leg_Twist_01_Jnt
                    |-- R_Upper_Leg_Twist_02_Jnt
                    |-- R_Upper_Leg_Twist_01_Corrective_Jnt </code></pre>
</details>

## Trebuchet Rig Recap
The trebuchet rig is a simple rig that has a few extra features. The rig has FK controls for the base, arm, counterweights and ammo slide. The rig also has some point constraints to some locators that are used to help control the pointing and pivoting of the counterweights that allow for individual control of each counterweight.
<details>
    <summary>Joint Hierarchy: Trebuchet Rig</summary>

<pre><code>|- COG_Jnt
     |-- Base_01_FK_Jnt
          |-- Base_02_FK_Jnt
               |-- Ammo_Slide_01_FK_Jnt
               |-- Arm_01_FK_Jnt
                    |-- Arm_02_HELPER_Jnt
                    |-- L_Weight_01_FK_Jnt
                    |-- R_Weight_01_FK_Jnt
                    |-- L_Weight_01_RK_Jnt
                         |-- L_Weight_02_HELPER_Jnt
                         |-- L_Weight_03_HELPER_Jnt
                    |-- R_Weight_01_RK_Jnt
                         |-- R_Weight_02_HELPER_Jnt
                         |-- R_Weight_03_HELPER_Jnt
               |-- L_Ring_01_FK_Jnt
                    |-- L_Ring_01_HELPER_Jnt
               |-- R_Ring_01_FK_Jnt
                    |-- R_Ring_01_HELPER_Jnt
</code></pre>
</details>