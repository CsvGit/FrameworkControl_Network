# Disclaimer

This is a personal guide not a peer reviewed journal or a sponsored publication. We make no representations as to accuracy, completeness, correctness, suitability, or validity of any information and will not be liable for any errors, omissions, or delays in this information or any losses injuries, or damages arising from its display or use. All information is provided on an as is basis. It is the reader’s responsibility to verify their own facts.

The views and opinions expressed in this guide are those of the authors and do not necessarily reflect the official policy or position of any other agency, organization, employer or company. Assumptions made in the analysis are not reflective of the position of any entity other than the author(s) and, since we are critically thinking human beings, these views are always subject to change, revision, and rethinking at any time. Please do not hold us to them in perpetuity.

# Instruction

## TE2000:
• >= 1.12.758.8

## Package manager:

Add nuget.org to Nugget package manager if not already added.

![Image_NugetOrg](https://github.com/CsvGit/FrameworkControl_Network/assets/115890823/54a4da6a-f4d3-4926-bc20-879216f28426)

## Guide:
1. Create an HMI project.

![Image1](https://github.com/CsvGit/FrameworkControl_Network/assets/115890823/49ff63b5-b8dd-4467-9f5e-40fcaf4f7d83)

2. Install the packages from NuGet Package Manager.

![Image2](https://github.com/CsvGit/FrameworkControl_Network/assets/115890823/9da90357-05af-4bf8-92ac-f65452334b74)

3. Drag the TcHmiNetworkControl from Toolbox into a page.

![Image3](https://github.com/CsvGit/FrameworkControl_Network/assets/115890823/8f410f21-4166-4346-9213-1c46aa3269f3)

4. Drag the TcHmiNodeControl from Toolbox into the TcHmiNetworkControl. 

![Image4](https://github.com/CsvGit/FrameworkControl_Network/assets/115890823/ff38bd34-ffbf-4715-84a3-da7b8d79034d)

5. Add one more TcHmiNodeControl. Document Outline window can be handy.

![Image5](https://github.com/CsvGit/FrameworkControl_Network/assets/115890823/7eade1a2-0f19-491d-8875-04bf199c8ea7)

6. On the TcHmiNetworkControl you can adjust the referesh-rate of the animation by 
GlobalIntervalTime.

![Image6](https://github.com/CsvGit/FrameworkControl_Network/assets/115890823/8e14a4d5-8080-4cbd-9e64-60b9546d1adf)

7. Mark a child node and write the name of its parent. For example - TcHmiNodeControl_Parent
name to create an hierarchy connection.

![Image7](https://github.com/CsvGit/FrameworkControl_Network/assets/115890823/79b413f4-b2a5-43d1-9033-8310cfa9fab9)

8. On the parent node link your PLC variable to the BottomValue attribute. When the parent node 
has value > 0 then flow direction is parent to child. Once the value < 0 then flow direction is child 
to parent. 

![Image8](https://github.com/CsvGit/FrameworkControl_Network/assets/115890823/5ffcad75-bc00-434e-867e-cbf6b1d60761)

9. The BottomDescription is the field for unit. The BottomDivFactor is the factor used to rescale the 
displayed value in the Node.

![Image9](https://github.com/CsvGit/FrameworkControl_Network/assets/115890823/6a758040-cc42-4cc7-a2dd-3900ed3eb748)

10. The SumChildren attribute makes the parent node sum the value from child nodes in lower 
hierarchy. Now when the child node has value > 0 then flow direction is child to parent. Once the value < 0 then flow direction is parent to child.

![Image10](https://github.com/CsvGit/FrameworkControl_Network/assets/115890823/b0dd7e2d-0457-4c4b-83d2-08bb2dd76c7e)

11. Images can be added through the CenterImage attribute.

![Image11](https://github.com/CsvGit/FrameworkControl_Network/assets/115890823/9a9eaf03-48f7-4499-8a15-b08443b6ab7c)

12. The ConnectionColor attribute changes the color of the animation between a node and its 
parent node. Can be changed to display different colors depending on value added.

![Image12](https://github.com/CsvGit/FrameworkControl_Network/assets/115890823/a7054d62-a886-43d9-a48c-4d1c624982ec)
