# 2019-Deep-Space-Regular-Season

Welcome. This package contains the entirety of FRC Team 7520 Minekee's robot code, last updated during the 2019 FRC Canada Ontario Provincial Championship. Because our team was short on time and inexperienced ~~and lazy~~, you may find that our code is "incomplete"; that is to say, our code only deals with SmartDashboard, our robot's drivetrain (thanks to team 5406 Celt-X for helping us out with that), and our robot's motor controllers and pneumatics system. Hopefully, our code will come with computer vision and sensor support by the time the offseason competitions begin and in the coming years. To take our performance to the next level, we also need to get a firm grasp on how to use subsystems and commands properly in our code. **Just so you know, our team uses the command-based robot template as the base for our program.**  

### Required Installations
Programming in the FRC requires a ton of software/application/library downloads, and I know how much you like to install stuff, so I'm giving you a list of what you need to have on your computer before you start coding: 
- **2019 NI Update Suite:** Because you really can't code without it, you should install this first. Going in, you should know that it comes in .zip format while requiring a password to unzip. A new version is released every year.
- **WPILib Installer:** As a team, we think this package is as much of a godsend as it was a pain to install. After you install, you're provided with libraries and API's for every piece of hardware used in the FRC as well as a special version of VS Code geared towards coding for FRC. **Don't install VS Code separately** unless you like making things hard for yourself. On the other hand, if you're part of a Labview team --and there are few out there-- you would need to install Labview from NI.
- **2019 FRC Radio Configuration Utility:** Radios (robot wifi hubs) have to be configured both before and after competitions, so us programming nerds use this software to set up our radios.
- **CTRE Phoenix Toolsuite:** Our team uses CTRE (a company) CAN devices like the VictorSPX and the TalonSRX --both of which are motor controllers-- and we can code and configure such items thanks to this handy third-party toolsuite. 
- **Kauai Labs:** Any team using a NavX or other items from Kauai Labs (another company) needs to install the corresponding libraries from Kauai Labs' website. Hooray for third-party software. 

### Programming Guides
Anyone who is looking to code and thinks they can dedicate some time to programming (even if they really can't) should check out the following resources: 
- https://wpilib.screenstepslive.com/s/currentCS gives a complete overview of what goes into making a robot for the FRC.
- https://wpilib.screenstepslive.com/s/currentCS/m/java has all the information you need on programming specifically with Java; the page even contains a downloadable PDF for programmers who like having one comprehensive guide that is easier to access when offline.
- https://wpilib.screenstepslive.com/s/currentCS/m/vision is dedicated specifically to vision; as vision greatly boosts teams' capabilities during matches, it may be useful to have this sort of knowledge.

### Code Structure
If you're looking to pull our robot code (located in `src/main/.../robot` ), know that it can be broken up into four main components: 
```
 commands
 sensors
 subsystems
 Robot.java
```
- In the `commands` folder, you'll find a bunch of command programs, which are basically instructions to particular robot parts, such as the drivetrain, the intake, the climbing, etc. on how to execute certain actions. Sadly, they are mostly empty and/or unused. 
- Although we didn't employ them, you'll see two files in the `sensors` folder: `LimitSensors.java` seeks to return values (true or false) from limit switch sensors placed on our robot, and `NavX.java` has a lot of functions that are supposed to be used with feedback from the NavX on top of our RIO.  
- The files in the `subsystems` folder are essentially blueprints for our hardware, as these subsystem files outline every function we'd want our hardware to have. Our command programs aim to utilize these subsystem functions to perform actions. 
- `Robot.java` is the big kahuna. During matches, everything our robot does comes from Robot.java. Anything that's part of the other three components will be incorporated into this program if we find use for it. 

And that's all. As mentioned in the first paragraph, many tweaks and improvements are yet to come. With the experience we've gained this year, our performance will be less sucky the next time we compete, though we did do pretty well for a rookie team. Here's to hoping for a functional, subsystem-using command system and finally putting some long-needed vision in our code.  
