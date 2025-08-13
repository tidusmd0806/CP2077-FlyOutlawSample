######################################################
### This file is not required for the mod to work. ###
######################################################

The purpose of this text file is to allow mod developers to create a new Aerial Vehicle (such as an ent or mesh file) 
and fly that entity using the “Drive an Aerial Vehicle” mechanism.

The three main files required are AV flight profile (in json format in this hierarchy) 
- The items are described below.
- TweakXL yaml file (see yaml comments for how to make it)
- Asset file for the new AV (the entity must be based on a regular or armed vehicle)

Here is an overview of the contents of the json file. (All coordinates are relative to the center of the vehicle.)
- name: any name
- tweakdb_id: Specify the TweakDBID of the one that is not _dummy
- display_name_lockey: localized key for the vehicle name
- type: list of vehicle appearance names
- flight_mode: (0)AV (1)Helicopter
- actual_allocated_door: Name of the seat adjacent to the door to be opened or closed.
- active_seat: List of seats to be displayed in the interaction
- actual_allocated_seat: List of actual seat names (must be the same number as active_seat)
- fpp_camera: Whether to enable the fpp camera during the ride.
- camera_distance_ratio: The ratio of the magnification to the normal camera distance. Set for each seat.
- camera_center_offset: Offset of the camera center position. Set for each seat.
- entry_point: Coordinates of the center of the space where the interaction is displayed during boarding.
- entry_area_radius: Radius of the space where the interaction is displayed during boarding.
- exit_point: The point at which the passenger teleports when exiting the vehicle.
- exit_duration: Delay before exiting. This is used to wait for the door to open.
- minimum_distance_to_ground: distance between the vehicle and the ground.
- combat_door: No problem with the sample as is.
- crystal_dome: presence of crystal dome.
- landing_vfx: Whether vfx is used for landing or not.
- projection_offset: Offset of landing_vfx
- engine_audio_name: No problem with the sample as is.
- manual_speed_meter: No problem with the sample as is.
- manual_rpm_meter: No problem with the sample as is.
- collision_check_side_distance: Distance from the center of the vehicle to the door. Used for collision detection in autonomous driving.
- collision_check_front_distance: The distance from the center of the vehicle to the front end. Used for collision detection in autonomous driving.
- collision_check_rear_distance: The distance from the center of the vehicle to the rear end. Used for collision detection in autonomous driving.
- armed: Armed or not armed
