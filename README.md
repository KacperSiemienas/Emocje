# Emocje
Poniższy program przedstawia kilka emocji wykonanych dla robota gazebo. Kod napisany jest w środowisku Matlab. 
Aby mozna było zobaczyć efekt poniższego kodu należy w pierwszej kolejności połączyć się z gazebo.
Kod zatytułowany RESET służy do zerowania pozycji robota.
Dwie pierwsze linijki kodu muszą zostać wykonane tylko raz, więc najlpiej je zakomentować po pierwszym uruchomieniu
lub wpisać je w command window i następnie także zakomentować.
Po wyborze emocji, którą ma zaprezentować robota należy zakomentować wszystkie inne linijki nie dotyczące wybranej pozycji. 








rosinit


rostopic list



% RESET

cam1=rossubscriber('/darwin/camera/image_raw')
im1=receive(cam1)
imshow(readImage(im1))
lewareka = rospublisher('/darwin/j_high_arm_l_position_controller/command');
prawareka = rospublisher('/darwin/j_high_arm_r_position_controller/command');
szyja = rospublisher('/darwin/j_tilt_position_controller/command');
prawynadgarstek = rospublisher('/darwin/j_gripper_r_position_controller/command');
lewynadgarstek = rospublisher('/darwin/j_gripper_l_position_controller/command');
lewybark = rospublisher('/darwin/j_shoulder_l_position_controller/command');
prawybark = rospublisher('/darwin/j_shoulder_r_position_controller/command');
leweprzedramie = rospublisher('/darwin/j_low_arm_l_position_controller/command');
praweprzedramie = rospublisher('/darwin/j_low_arm_r_position_controller/command');
prawybark_m = rosmessage(prawybark.MessageType);
lewybark_m = rosmessage(lewybark.MessageType);
lewynadgarstek_m = rosmessage(lewynadgarstek.MessageType);
prawynadgarstek_m = rosmessage(prawynadgarstek.MessageType);
leweprzedramie_m = rosmessage(leweprzedramie.MessageType);
praweprzedramie_m = rosmessage(praweprzedramie.MessageType);
szyja_m = rosmessage(szyja.MessageType);
lewareka_m = rosmessage(lewareka.MessageType);
prawareka_m = rosmessage(prawareka.MessageType);
leweprzedramie_m.Data = 0;
praweprzedramie_m.Data = 0;
prawynadgarstek_m.Data = 0;
lewynadgarstek_m.Data = 0;
prawybark_m.Data = 0;
lewybark_m.Data = 0;
szyja_m.Data = 0;
lewareka_m.Data = 0;
prawareka_m.Data = 0;
send(szyja,szyja_m)
send(lewareka,lewareka_m)
send(prawareka,prawareka_m)
send(prawynadgarstek,prawynadgarstek_m)
send(lewynadgarstek,lewynadgarstek_m)
send(lewybark,lewybark_m)
send(prawybark,prawybark_m)
send(leweprzedramie,leweprzedramie_m)
send(praweprzedramie,praweprzedramie_m)

% Wesoły

cam1=rossubscriber('/darwin/camera/image_raw')
im1=receive(cam1)
imshow(readImage(im1))
lewareka = rospublisher('/darwin/j_high_arm_l_position_controller/command');
prawareka = rospublisher('/darwin/j_high_arm_r_position_controller/command');
szyja = rospublisher('/darwin/j_tilt_position_controller/command');
szyja_m = rosmessage(szyja.MessageType);
lewareka_m = rosmessage(lewareka.MessageType);
prawareka_m = rosmessage(prawareka.MessageType);
szyja_m.Data = 0;
lewareka_m.Data = -1.3;
prawareka_m.Data = -1.3;
send(szyja,szyja_m)
send(lewareka,lewareka_m)
send(prawareka,prawareka_m)

% Smutny

cam1=rossubscriber('/darwin/camera/image_raw')
im1=receive(cam1)
imshow(readImage(im1))
lewareka = rospublisher('/darwin/j_high_arm_l_position_controller/command');
prawareka = rospublisher('/darwin/j_high_arm_r_position_controller/command');
szyja = rospublisher('/darwin/j_tilt_position_controller/command');
prawynadgarstek = rospublisher('/darwin/j_gripper_r_position_controller/command');
lewynadgarstek = rospublisher('/darwin/j_gripper_l_position_controller/command');
lewynadgarstek_m = rosmessage(lewynadgarstek.MessageType);
prawynadgarstek_m = rosmessage(prawynadgarstek.MessageType);
szyja_m = rosmessage(szyja.MessageType);
lewareka_m = rosmessage(lewareka.MessageType);
prawareka_m = rosmessage(prawareka.MessageType);
szyja_m.Data = -0.5
prawynadgarstek_m.Data = -1
lewynadgarstek_m.Data = -1
lewareka_m.Data = 1.5
prawareka_m.Data = 1.5
send(lewareka,lewareka_m)
send(prawareka,prawareka_m)
send(prawynadgarstek,prawynadgarstek_m)
send(lewynadgarstek,lewynadgarstek_m)
send(szyja,szyja_m)

% Zakłpotoany

cam1=rossubscriber('/darwin/camera/image_raw')
im1=receive(cam1)
imshow(readImage(im1))
szyja = rospublisher('/darwin/j_tilt_position_controller/command');
lewareka = rospublisher('/darwin/j_high_arm_l_position_controller/command');
prawareka = rospublisher('/darwin/j_high_arm_r_position_controller/command');
leweprzedramie = rospublisher('/darwin/j_low_arm_l_position_controller/command');
praweprzedramie = rospublisher('/darwin/j_low_arm_r_position_controller/command');
lewybark = rospublisher('/darwin/j_shoulder_l_position_controller/command');
prawybark = rospublisher('/darwin/j_shoulder_r_position_controller/command');
prawybark_m = rosmessage(prawybark.MessageType);
lewybark_m = rosmessage(lewybark.MessageType);
leweprzedramie_m = rosmessage(leweprzedramie.MessageType);
praweprzedramie_m = rosmessage(praweprzedramie.MessageType);
szyja_m = rosmessage(szyja.MessageType);
lewareka_m = rosmessage(lewareka.MessageType);
prawareka_m = rosmessage(prawareka.MessageType);
prawybark_m.Data = -1.5
lewareka_m.Data = -0.6
prawareka_m.Data = 0
lewybark_m.Data = -1.4
leweprzedramie_m.Data = -2.3
praweprzedramie_m.Data = 2.3
szyja_m.Data = -0.5
send(prawybark,prawybark_m)
send(lewareka,lewareka_m)
send(prawareka,prawareka_m)
send(lewybark,lewybark_m)
send(leweprzedramie,leweprzedramie_m)
send(praweprzedramie,praweprzedramie_m)
send(szyja,szyja_m)

