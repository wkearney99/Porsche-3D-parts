// button/plug for under the wind flaps of a 2018 Porsche Targa

// 1-Dome, 2-Flat
type = 2;

/* [cap parameters] */

cap_diameter = 11;
// size of the top part

cap_height = 3;
// height only if it's flat, otherwise it's just a half-sphere with no edge

shaft_diameter = 4;
// How wide is the hole?

shaft_height = 2;
// How thick is the material it's going through  

barb_flange_diameter = 6;
// diameter of the point on the bottom

barb_point_depth = 4;
// depth of the point on the bottom

/* [Hidden] */
$fn = 100;
// smoothness of the circle edges higher may mean more time-consuming prints.

// go to the zero starting point
translate([0,0,0])

// Make the part that goes through the material
cylinder(d=shaft_diameter, h=shaft_height);

//Make the cap, on top (spehere or cylinder)
translate([0,0,shaft_height])
    intersection(){
        if (type==1) {
            sphere(d=cap_diameter);
        } else {
            cylinder(d=cap_diameter, h=cap_height);
        }
        
        translate([0,0,cap_diameter/2])
        cube(size=cap_diameter, center=true);
        }
// make point on the bottom
translate([0,0,-barb_point_depth])
    intersection(){
            cylinder(barb_point_depth, r1=0, r2=barb_flange_diameter/2);
        }
