# PLL-OSU-180nm-PDK
**Design of PLL using OSU 180nm PDK**

![image](https://user-images.githubusercontent.com/92794189/137905301-931cca11-2a86-4da9-9463-8f77f6ea9b0f.png)
* [Table of contents](#gh-md-toc)
   * [**Introduction**](#table-of-contents)
   * [**Proposed PLL Circuit**](#installation)
   * [**Prelayout**](#installation)
   * [**PostLayout**](#usage)
   * [**Conclusion**](#stdin)

**Introduction**

PLL is Phase Locked loop which comprises of mainly Phase frequency detector (PFD), Low pass filter (LPF), Voltage cotrolled oscillator (VCO) and Frequency divider (FD).The main application of PLL as on chip multiplier is to increase or multiply the output frequency since the frequency generated by the crystal oscillator is not sufficient to increasing the processor speed. The task of each block is PLL are as follows:(i) PFD: There are two inputs in PFD, it mainly compares the phases/frequencies of the signals. (ii) LPF:Converts the pulsating output to a constant DC signal. (iii) VCO: Depending upon the voltage of the input signal the frquency of the output signal varies. (iv) FD: The frquency of the output signal is divided by the number of times it is increased. Particular in the circuit discussed below the frequency of the sigal is increased by eight times. Figure shown below is the basic block diagram of a PLL.

![image](https://user-images.githubusercontent.com/92794189/137946255-366f9d4c-726a-465a-bc7c-3cc6dc326aa2.png)
 
 **Proposed PLL Circuit**
 
 ![image](https://user-images.githubusercontent.com/92794189/137950158-e6da70cd-f031-42c5-a071-43d4f97335e2.png)
 
 **Prelayout**
 
 Inverter is one of the fundamental circuits used in desining any kind of complex circuit. The circuit design shown below:
 
 ![image](https://user-images.githubusercontent.com/92794189/137951622-72e18c8c-2536-4677-b391-2830ec0e3c38.png)
  
     Inverter Circuit
 
 ![image](https://user-images.githubusercontent.com/92794189/137951397-10ae7556-8a73-4fb1-8635-1d49e9c19685.png)
 
                    Inverter code for simulation in ngspice
                    
 ![Inverter Output](https://user-images.githubusercontent.com/92794189/137951684-9311ef22-6218-424e-becb-e7d5d3996943.PNG)
            
                    Output Waveform in ngspice
                    
 ![image](https://user-images.githubusercontent.com/92794189/137953277-3c67786b-4b2d-4bc3-85f9-a5776ede7e85.png)
  
          Circuit of PFD 
 ![image](https://user-images.githubusercontent.com/92794189/137954021-238b4a2b-b0e3-4045-b5a0-ff9b470f510a.png)
 
            Sample of PFD Code for simulation in ngspice
 
 ![PFD Output](https://user-images.githubusercontent.com/92794189/137953438-742ac560-5c75-4758-9a33-650ed16a5562.PNG)

             Simulated Output of PFD in ngspice
             
 ![image](https://user-images.githubusercontent.com/92794189/137956981-218d8436-c07b-4642-b5a3-93c3095d0776.png)

             PFD, Charge Pump and LPF

![image](https://user-images.githubusercontent.com/92794189/137955263-2fb31e60-3da1-4906-9d43-e5fb3ae1ffdf.png)

            Simulated Ouput of Charge Pump, LPF along with PFD in ngspice
            
  VCO is designed using ring oscillator.
  
  ![image](https://user-images.githubusercontent.com/92794189/137957877-de4fd8ea-78db-4a94-96d1-dc22354ab073.png)

            VCO Circuit
            
 ![VCO Output](https://user-images.githubusercontent.com/92794189/137957433-f519a37b-c390-4b16-b531-cd33e6eee050.PNG)
 
           Simulated Ouput of VCO in ngspice
           
 ![image](https://user-images.githubusercontent.com/92794189/137958235-c8737f0f-1d35-431e-9461-ba17ee7237e9.png)
 
           Frequency Divider Circuit
           
 ![image](https://user-images.githubusercontent.com/92794189/137958636-f8d468d6-a2a4-4326-8b79-6e6ba33820fa.png)
 
          Simulated Output of Frequency Divider Circuit in ngSpice
          
 ![image](https://user-images.githubusercontent.com/92794189/137959399-2bfaad45-6846-4e27-ae91-251305432b46.png)
 
          PLL Circuit
          
 ![image](https://user-images.githubusercontent.com/92794189/137959946-29191376-c3f5-4ad4-ac2b-fe832aea3974.png)

        PLL Output
        
  ![image](https://user-images.githubusercontent.com/92794189/137960792-4647d963-cce6-43c6-8c30-56797ff11b3e.png)

          Output Frequencies increased by 8 times
          
 **PostLayout**
 
 ![PFD_Layout](https://user-images.githubusercontent.com/92794189/137959730-e30a0ebc-68e2-400b-a6ce-9e2e322cef39.PNG)
            
            PFD Layout
            
 ![PFD postlayout output](https://user-images.githubusercontent.com/92794189/137960908-19085c0a-fc5f-4057-8f71-f6f6cd4d6ddd.PNG)

             PFD Post Layout Output          

 ![VCO_Layout](https://user-images.githubusercontent.com/92794189/137961071-1484c907-363b-4400-a392-2e93665450d6.PNG)

            VCO Layout
            
 ![Post Layout VCO Output](https://user-images.githubusercontent.com/92794189/137961169-caadb75a-3109-4e1c-8515-e1e6a12297f4.PNG)
           
           Post Layout VCO Output
           
 ![Freq_Div_8_Layout](https://user-images.githubusercontent.com/92794189/137961260-5fa75f89-f210-44a6-8795-56a86a3576fa.PNG)
 
          Frequency Divider Layout
          
 ![Freq_Div_8_Post Layout_Output](https://user-images.githubusercontent.com/92794189/137961332-f42711b9-2025-46af-a0fb-58983ad65e6c.PNG)

          Post Layout Frequency Divider Output

![Final PLL_Layout](https://user-images.githubusercontent.com/92794189/137961415-bd5fc8c9-453d-4bf8-acee-4ca8bd0fc9de.PNG)

          PLL Layout
          
![PLL_Post Layout Output](https://user-images.githubusercontent.com/92794189/137961487-cb46af12-568c-4478-9718-7dc8077bd906.PNG)

          PLL Post Layout Output
          
**Conclusion**

A PLL design is presented which has the ability to increase the frequency upto eight times and at the same time the SoC could be used as only VCO with the help of a control bit.


**References:**

1. https://github.com/parasgidd/avsdpll_3v3
2. F. M Gardener, Phaselock Techniques, 2nd edition, New York: Wiley, 1979.
3. F. M. Gardner, “Charge-pump phase-lock loops,” IEEE Trans. Commun., vol. COM-28, no. 11, pp. 1849–1858, Nov. 1980
4. B. Razavi, "Design of Monolithic Phase-Locked Loops and Clock Recovery Circuits - A Tutorial," in Monolithic Phase-Locked Loops and Clock Recovery Circuits: Theory and Design, Wiley-IEEE Press, pp. 1-39,1996.

**Acknowlegement**

I would like to thank the following persons for giving me the platform and technical knowledge to create this report.

**Kunal P Ghosh**

**Parash Gidd**

            
