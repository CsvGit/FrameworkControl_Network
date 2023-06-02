# Disclaimer

This is a personal guide not a peer reviewed journal or a sponsored publication. We make no representations as to accuracy, completeness, correctness, suitability, or validity of any information and will not be liable for any errors, omissions, or delays in this information or any losses injuries, or damages arising from its display or use. All information is provided on an as is basis. It is the reader’s responsibility to verify their own facts.

The views and opinions expressed in this guide are those of the authors and do not necessarily reflect the official policy or position of any other agency, organization, employer or company. Assumptions made in the analysis are not reflective of the position of any entity other than the author(s) and, since we are critically thinking human beings, these views are always subject to change, revision, and rethinking at any time. Please do not hold us to them in perpetuity.

# Instruction

## TE2000:
• >= 1.12.758.8

## Package manager:

Add nuget.org to Nugget package manager if not already added.

![Image_NugetOrg](https://github.com/CsvGit/FrameworkControl_Network/assets/115890823/922d9da7-3b53-4bdb-b2a3-706d3d4c01f1)

## Guide:
1. Create an HMI project.

![Image1](https://github.com/CsvGit/FrameworkControl_Network/assets/115890823/1ed89c48-e3f9-4abd-8398-ca192d672f8b)

2. Install the packages from NuGet Package Manager.

![Image2](https://github.com/CsvGit/FrameworkControl_Network/assets/115890823/874df757-d203-40a9-b6be-853132a6e372)

3. Drag the TcHmiNetworkControl from Toolbox into a page.

![Image3](https://github.com/CsvGit/FrameworkControl_Network/assets/115890823/eb5ecabf-d2dc-413d-a156-abeab45f73ca)

4. Drag the TcHmiNodeControl from Toolbox into the TcHmiNetworkControl. 

![Image4](https://github.com/CsvGit/FrameworkControl_Network/assets/115890823/594fdb95-0553-478d-8d77-40832405ed1b)

5. Add one more TcHmiNodeControl. Document Outline window can be handy.

![Image5](https://github.com/CsvGit/FrameworkControl_Network/assets/115890823/96801fae-8ea3-45b5-b1d5-d63bec007613)

6. On the TcHmiNetworkControl you can adjust the referesh-rate of the animation by 
GlobalIntervalTime.

![Image6](https://github.com/CsvGit/FrameworkControl_Network/assets/115890823/edd03b64-625d-45c1-834c-8ee4eb4baf62)

7. Mark a child node and write the name of its parent. For example - TcHmiNodeControl_Parent
name to create an hierarchy connection.

![Image7](https://github.com/CsvGit/FrameworkControl_Network/assets/115890823/15302bbf-ee10-46a5-9f26-fb070b200351)

8. On the parent node link your PLC variable to the BottomValue attribute. When the parent node 
has value > 0 then flow direction is parent to child. Once the value < 0 then flow direction is child 
to parent. 

![Image8](https://github.com/CsvGit/FrameworkControl_Network/assets/115890823/87c219eb-270b-4358-82e9-6db1422787f0)

9. The BottomDescription is the field for unit. The BottomDivFactor is the factor used to rescale the 
displayed value in the Node.

![Image9](https://github.com/CsvGit/FrameworkControl_Network/assets/115890823/99702816-f793-4a48-b68b-8e2e6358861f)


10. The SumChildren attribute makes the parent node sum the value from child nodes in lower 
hierarchy. Now when the child node has value > 0 then flow direction is child to parent. Once the value < 0 then flow direction is parent to child.

![Image10](https://github.com/CsvGit/FrameworkControl_Network/assets/115890823/ac06c4b2-59ed-43aa-bfdc-c9305e7f7311)

11. Images can be added through the CenterImage attribute.

![Image11](https://github.com/CsvGit/FrameworkControl_Network/assets/115890823/44677689-82cb-4f6c-9616-1d78c59c4176)

12. The ConnectionColor attribute changes the color of the animation between a node and its 
parent node. Can be changed to display different colors depending on value added.

![Image12](https://github.com/CsvGit/FrameworkControl_Network/assets/115890823/d1af0e11-ba0e-4b98-bbbf-cc199c94e6ea)


