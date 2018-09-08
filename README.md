# HFSS_dipole_antenna

<hr>

Author : 林奎良(KuiLiang Lin), 王廷瑋

Director : Professor 廖文照 

This project was hold at National Taiwan University and Science and Technology, 2013.

Content below is only a small part of the project.

1. Abstract

   天線基本上可以分成兩大類型,全像天線與指向天線，在自由空間內，任何天線都向各個方向輻射能量，但是特定的架構會使天線在某個方向上獲得較大方向性，而其它方向的能量輻射則可以忽略
   
   通過增加附加導體棒或線圈並改變其長度、間距和方位（或者改變天線波束方向），可以製造出擁有既定特性的天線。在廣播和通信中偶極天線是最簡單和最廣泛使用的一類天線。它由兩個相同的導電元件組合而成且通常是雙側對稱，天線的兩部分間可當作發射器或接收器。偶極天線的每一側都會接到一個導體，而單極天線則是一側與導體連接，另一側則接地
   
   偶極天線最常見的形式是兩個筆直的電線或導體置於同一軸線上，然後饋線連接到兩個相鄰端部。偶極天線為諧振天線，藉由電流來回不斷的流動而產生輻射。因此，偶極天線元件的長度是由所使用的無線電波的波長而決定。最常見的形式是半波長偶極天線，其中天線元件長度約1/4波長，所以整個天線的長度是半波長
   
   巴倫(Balun)是用來平衡不平衡系統。偶極天線正常運作，雙臂上的電流應該是相等的。然而當同軸電纜直接連接到偶極天線時，電流將不會再相等。理論上傳輸線的電流應該是幅度相等的流動在內導體和外導體上且中心導體連接到其中一支dipole arm。然而，沿外導體內側的電流有兩個路徑選項：它可以沿著dipole arm或同軸電纜外導體的外側向下流動(標記成IC)
   
   在理想的情況下，此dipole antenna的同軸電纜外導體外側電流應為零。在這種情況下，沿dipole arm流到同軸電纜外部導體的電流，將等於另一支dipole arm的電流。一個理想的天線特性，兩端的dipole arm所流過的電流相等為平衡的區域。但同軸電纜的電流並不會配合理想偶極天線的電流特性，可能沿著同軸電纜的外部，導致不平衡的操作，這是不平衡的部分
   
   解決這個問題的其中一個方法就是加上巴倫。巴倫強制不平衡傳輸線正確饋入一個平衡的元件。這將迫使IC為零，這種方式通常被稱為current choke

2. HFSS - Structure
   
   Basic

   <img src="https://raw.githubusercontent.com/KuiLiangLin/HFSS_dipole_antenna/master/HFSS_structure_1.jpg" height="100%" width="100%" >
   
   Cross Balun Dipole Antenna
   
   <img src="https://raw.githubusercontent.com/KuiLiangLin/HFSS_dipole_antenna/master/HFSS_structure_2.jpg" height="100%" width="100%" >
   
   Cross Dipole Antenna

   <img src="https://raw.githubusercontent.com/KuiLiangLin/HFSS_dipole_antenna/master/HFSS_structure_3.jpg" height="100%" width="100%" >
   
3. HFSS - S parameter

   S11 - 頻寬為0.9GHz~ 0.96GHz，中心頻率為0.93GHz，頻寬率百分比為6.5%
   
   <img src="https://raw.githubusercontent.com/KuiLiangLin/HFSS_dipole_antenna/master/S11.jpg" height="100%" width="100%" >
    
   S12- 頻寬為0.89GHz~ 0.96GHz，中心頻率為0.93GHz。頻寬率百分比為7.5%
   
   <img src="https://raw.githubusercontent.com/KuiLiangLin/HFSS_dipole_antenna/master/S12.jpg" height="100%" width="100%" >

   S11 with Balun - S11與S22的頻寬約為0.87GHz~ 0.97GHz，中心頻率約為0.92GHz
   
   <img src="https://raw.githubusercontent.com/KuiLiangLin/HFSS_dipole_antenna/master/B_S11.jpg" height="100%" width="100%" >
   
   S12 with Balun - -30dB以下頻寬0.6GHz~0.9GHz中心頻率0.75GHz
   
   <img src="https://raw.githubusercontent.com/KuiLiangLin/HFSS_dipole_antenna/master/B_S12.jpg" height="100%" width="100%" >
   
4. Far Field Gain with Balun
   
   將天線置於電波暗室中量測其場型分佈。Ｅ_theta是由座標軸z往xy面發射的分量，Ｅ_phi是在xy面上的分量，即為兩個極化方向，並且二者垂直，而可從中觀察其輻射效率、增益，相較於2D的polar plot，Ｅtheta與Ｅphi圖提供了觀察者天線在空間中場型與輻射的分布狀況。
   
   由於theta與phi為正交極化關係，若將兩張圖片疊加起來則可得到E total
   
   HFSS - Gain Total
   
   <img src="https://raw.githubusercontent.com/KuiLiangLin/HFSS_dipole_antenna/master/HFSS_B_gain_total.jpg" height="100%" width="100%" >
   
   Anechoic Chamber - Gain Theta
   
    <img src="https://raw.githubusercontent.com/KuiLiangLin/HFSS_dipole_antenna/master/chamber_E_theta.jpg" height="100%" width="100%" >
  
   Anechoic Chamber - Gain Phi
   
   <img src="https://raw.githubusercontent.com/KuiLiangLin/HFSS_dipole_antenna/master/chamber_E_phi.jpg" height="100%" width="100%" >
   



















