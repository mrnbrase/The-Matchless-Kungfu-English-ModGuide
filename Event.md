## 1- First We go to the file locaiotn "Event" by going to the "Content/EditorContent/Event"

## 2- from there We Create a New Event By clicking Right Mouse button and going to the:

![image](https://github.com/mrnbrase/The-Matchless-Kungfu-English-ModGuide/assets/5586194/ce411169-38e0-408d-bc97-df4a7f0e3198)


## 3- Give the event file a name then open it.
## Copy all the Code in the FIle >>> Nodes_i_Used.md <<< and Past it in the Event Screen.

![image](https://github.com/mrnbrase/The-Matchless-Kungfu-English-ModGuide/assets/5586194/d06b72d3-143d-4eed-b850-40ffd5d1d0a3)


## 4- now we will start doing my mod "Call to Me".


## There will be 3 type of event:
![image](https://github.com/mrnbrase/The-Matchless-Kungfu-English-ModGuide/assets/5586194/9a9f09f9-1a18-48a0-bef6-be9418c013f6)


A. **LOD Node Event:**
   - This mod focuses on elements outside of the player's view, handling things like NPC power growth and replenishing the NPC shop. It's designed to manage activities that occur in the game world but are not directly visible to the player.

B. **Simple Event:**
   - Simple events are utilized for actions that don't involve dialogues and occur within the player's area. This category is suitable for tasks such as changing stats or summoning an NPC to the player's location.

C. **Dialogue Event:**
   - Dialogue events are specifically tailored for interactions involving conversations between the player and NPCs. This event type is perfect for scenarios where dialogues play a crucial role in conveying information or advancing the storyline.

## 5- The mod we will make is a "Simple Event" so we just need to call NPC from our Sect to our location
## so we will drag the Simple event node and drop it to the screen:
![image](https://github.com/mrnbrase/The-Matchless-Kungfu-English-ModGuide/assets/5586194/1ff06ca4-f3f1-40da-b32a-74d0cedff8c3)


![image](https://github.com/mrnbrase/The-Matchless-Kungfu-English-ModGuide/assets/5586194/a17f2d6b-aeea-467c-9799-5de736f19364)


1. **Interrupting Action:**
   - This is to interrupt the player and cancel the action the player is in if it's true and the event got triggered.

2. **Event Identification:**
   - Here you type the event name just so you know when the event triggers; it's the one you are working on.

3. **Testing and Control:**
   - To [Disable], [Enable], [Disable all other events and keep this event Enable for testing in the Mode Tool] (only pick the last if you are testing the event).

4. **Trigger Limit:**
   - This is how many times the event can trigger; -1 means no limit.

5. **Global or Specific:**
   - Whether it is a global event (1: global, 0: counted separately for different roles).

6. **Forced Execution:**
   - Forced execution (events that interrupt other current executions) - try avoiding using this; it will give it priority but it could break other events.

7. **Cool Time (Seconds):**
   - This is the cooldown time (in seconds) of the event; how long until it triggers again.

8. **Event Duration (Seconds):**
   - This is how long the event will be running (in seconds) each time the event is running. So if you make it 10 seconds, the event will cancel itself in the middle of the event after 10 seconds and will restart.

9. **Player Stat Dependency:**
   - This is for the event to be able to trigger it in a player stat. If I only have "walk," then if I start "jumping," the event will not trigger.

10. **End Game Stat Compatibility:**
    - If the event can be run at the end game HMS.
-


## Now Explaining the Event Node:

![image](https://github.com/mrnbrase/The-Matchless-Kungfu-English-ModGuide/assets/5586194/0bc5c985-ccd9-4a24-b635-7a1bf286ad1a)

1. **Adding Event Condition:**
   - In this step, we set the event condition. For example, if we want the event to trigger when the player sits on the throne, we define that condition here.

2. **Selecting NPC and Sect Check:**
   - At this stage, we choose the NPC for the event and set conditions for each NPC to check if they belong to the same sect as the player. This ensures the right NPCs are involved.

3. **Action Event:**
   - In this step, we define the action event. Depending on the scenario, it could involve NPCs talking with the player, giving items, or any other action we want to incorporate into the event.


## What you need:

![image](https://github.com/mrnbrase/The-Matchless-Kungfu-English-ModGuide/assets/5586194/7153eeb5-a529-4514-bf4e-109050894d2a)


<details>
<summary>Click to expand/collapse(Copy the Code inside and past it to get the image above)</summary>


```javascript
Begin Object Class=/Script/EventEditor.EventGraphNode_Precondition Name="EventGraphNode_Precondition_4"
   Begin Object Class=/Game/EditorContent/Event/Precondition/EP_CanEventByBehaviors.EP_CanEventByBehaviors_C Name="EP_CanEventByBehaviors_C_0"
   End Object
   Begin Object Name="EP_CanEventByBehaviors_C_0"
      可执行事件的行为列表(8)=(TableName="behavior_relation",Label="经营坐班",ValueOfInt=-1,ValueOfString="behavior_160")
      可执行事件的行为列表(9)=(TableName="behavior_relation",Label="坐宝座",ValueOfInt=-1,ValueOfString="behavior_152")
      可执行事件的行为列表(10)=(TableName="behavior_relation",Label="吹箫",ValueOfInt=-1,ValueOfString="behavior_198")
      可执行事件的行为列表(11)=(TableName="behavior_relation",Label="驻足",ValueOfInt=-1,ValueOfString="behavior_130")
      可执行事件的行为列表(12)=(TableName="behavior_relation",Label="站岗",ValueOfInt=-1,ValueOfString="behavior_212")
      可执行事件的行为列表(13)=(TableName="behavior_relation",Label="睡觉·床",ValueOfInt=-1,ValueOfString="behavior_102")
      可执行事件的行为列表(14)=(TableName="behavior_relation",Label="睡觉·草席",ValueOfInt=-1,ValueOfString="behavior_123")
      可执行事件的行为列表(15)=(TableName="behavior_relation",Label="打招呼",ValueOfInt=-1,ValueOfString="behavior_1039")
      可执行事件的行为列表(16)=(TableName="behavior_relation",Label="乞讨行为",ValueOfInt=-1,ValueOfString="behavior_116")
      可执行事件的行为列表(17)=(TableName="behavior_relation",Label="游泳",ValueOfInt=-1,ValueOfString="behavior_swim")
      InputList(0)=None
      NodeGuid=C87C4D2C4BB92CEDA9C60FAD5B328C09
      EventGraphNode=EventGraphNode_Precondition'"EventGraphNode_Precondition_4"'
   End Object
   EventNode=EP_CanEventByBehaviors_C'"EP_CanEventByBehaviors_C_0"'
   NodePosX=1792
   NodePosY=-1088
   NodeGuid=C87C4D2C4BB92CEDA9C60FAD5B328C09
   CustomProperties Pin (PinId=ECC677194DD171A65FCB998298466954,PinName="被检查的角色实体",PinType.PinCategory="Input",PinType.PinSubCategory="Public",PinType.PinSubCategoryObject=None,PinType.PinSubCategoryMemberReference=(),PinType.PinValueType=(),PinType.ContainerType=None,PinType.bIsReference=False,PinType.bIsConst=False,PinType.bIsWeakPointer=False,PinType.bIsUObjectWrapper=False,LinkedTo=(EventGraphNode_Input_22 3DD94DCD45F770B5D0053A920C72D77A,),PersistentGuid=00000000000000000000000000000000,bHidden=False,bNotConnectable=False,bDefaultValueIsReadOnly=False,bDefaultValueIsIgnored=False,bAdvancedView=False,bOrphanedPin=False,)
   CustomProperties Pin (PinId=810E1D1641719C9D90FE4CA16125037A,PinName="前置条件",PinType.PinCategory="Precondition",PinType.PinSubCategory="Private",PinType.PinSubCategoryObject=None,PinType.PinSubCategoryMemberReference=(),PinType.PinValueType=(),PinType.ContainerType=None,PinType.bIsReference=False,PinType.bIsConst=False,PinType.bIsWeakPointer=False,PinType.bIsUObjectWrapper=False,LinkedTo=(EventGraphNode_CP_And_2 0487985F419F9D855E1FD684D28D3C0E,),PersistentGuid=00000000000000000000000000000000,bHidden=False,bNotConnectable=False,bDefaultValueIsReadOnly=False,bDefaultValueIsIgnored=False,bAdvancedView=False,bOrphanedPin=False,)
End Object
Begin Object Class=/Script/UnrealEd.EdGraphNode_Comment Name="EdGraphNode_Comment_2"
   CommentColor=(R=0.000000,G=0.128237,B=1.000000,A=1.000000)
   NodePosX=1248
   NodePosY=-1184
   NodeWidth=944
   NodeHeight=416
   NodeComment="To Make Sure That The Actor we are calling are not doing anything Important"
   NodeGuid=DABEBF6A4B1915DD4CE6B69BCFE79B6A
End Object
Begin Object Class=/Script/EventEditor.EventGraphNode_Input Name="EventGraphNode_Input_22"
   Begin Object Class=/Game/EditorContent/Event/Input/EI_GetFilterActor.EI_GetFilterActor_C Name="EI_GetFilterActor_C_3"
   End Object
   Begin Object Name="EI_GetFilterActor_C_3"
      Field="target"
      NodeGuid=38DE950C4DC0C46FBA0A8DB3F94013C5
      EventGraphNode=EventGraphNode_Input'"EventGraphNode_Input_22"'
   End Object
   EventNode=EI_GetFilterActor_C'"EI_GetFilterActor_C_3"'
   NodePosX=1280
   NodePosY=-1088
   NodeGuid=38DE950C4DC0C46FBA0A8DB3F94013C5
   CustomProperties Pin (PinId=3DD94DCD45F770B5D0053A920C72D77A,PinName="输入器",Direction="EGPD_Output",PinType.PinCategory="Input",PinType.PinSubCategory="Private",PinType.PinSubCategoryObject=None,PinType.PinSubCategoryMemberReference=(),PinType.PinValueType=(),PinType.ContainerType=None,PinType.bIsReference=False,PinType.bIsConst=False,PinType.bIsWeakPointer=False,PinType.bIsUObjectWrapper=False,LinkedTo=(EventGraphNode_Precondition_4 ECC677194DD171A65FCB998298466954,),PersistentGuid=00000000000000000000000000000000,bHidden=False,bNotConnectable=False,bDefaultValueIsReadOnly=False,bDefaultValueIsIgnored=False,bAdvancedView=False,bOrphanedPin=False,)
End Object
Begin Object Class=/Script/EventEditor.EventGraphNode_Precondition Name="EventGraphNode_Precondition_5"
   Begin Object Class=/Game/EditorContent/Event/Precondition/EP_IsInCage.EP_IsInCage_C Name="EP_IsInCage_C_1"
   End Object
   Begin Object Name="EP_IsInCage_C_1"
      IsReverse=True
      InputList(0)=None
      NodeGuid=591BAB8248D367D231DAC7A081953164
      EventGraphNode=EventGraphNode_Precondition'"EventGraphNode_Precondition_5"'
   End Object
   EventNode=EP_IsInCage_C'"EP_IsInCage_C_1"'
   NodePosX=1920
   NodePosY=-912
   NodeGuid=591BAB8248D367D231DAC7A081953164
   CustomProperties Pin (PinId=695E617646F731E49FC4A49C7587A555,PinName="目标对象",PinType.PinCategory="Input",PinType.PinSubCategory="Public",PinType.PinSubCategoryObject=None,PinType.PinSubCategoryMemberReference=(),PinType.PinValueType=(),PinType.ContainerType=None,PinType.bIsReference=False,PinType.bIsConst=False,PinType.bIsWeakPointer=False,PinType.bIsUObjectWrapper=False,LinkedTo=(EventGraphNode_Input_23 3DD94DCD45F770B5D0053A920C72D77A,),PersistentGuid=00000000000000000000000000000000,bHidden=False,bNotConnectable=False,bDefaultValueIsReadOnly=False,bDefaultValueIsIgnored=False,bAdvancedView=False,bOrphanedPin=False,)
   CustomProperties Pin (PinId=37F2E98F406FF7F922424DB28A55FDF3,PinName="前置条件",PinType.PinCategory="Precondition",PinType.PinSubCategory="Private",PinType.PinSubCategoryObject=None,PinType.PinSubCategoryMemberReference=(),PinType.PinValueType=(),PinType.ContainerType=None,PinType.bIsReference=False,PinType.bIsConst=False,PinType.bIsWeakPointer=False,PinType.bIsUObjectWrapper=False,LinkedTo=(EventGraphNode_CP_And_2 024CE2B44C5619FBE6D40783D3B20FFE,),PersistentGuid=00000000000000000000000000000000,bHidden=False,bNotConnectable=False,bDefaultValueIsReadOnly=False,bDefaultValueIsIgnored=False,bAdvancedView=False,bOrphanedPin=False,)
End Object
Begin Object Class=/Script/EventEditor.EventGraphNode_CP_And Name="EventGraphNode_CP_And_2"
   Begin Object Class=/Script/Event.EventNode_CP_And Name="EventNode_CP_And_5"
   End Object
   Begin Object Name="EventNode_CP_And_5"
      PreconditionList(0)=EP_CanEventByBehaviors_C'"EventGraphNode_Precondition_4.EP_CanEventByBehaviors_C_0"'
      PreconditionList(1)=EP_IsInCage_C'"EventGraphNode_Precondition_5.EP_IsInCage_C_1"'
      NodeGuid=176C93F04A8B9B909364428600603AEF
      EventGraphNode=EventGraphNode_CP_And'"EventGraphNode_CP_And_2"'
   End Object
   EventNode=EventNode_CP_And'"EventNode_CP_And_5"'
   NodePosX=1296
   NodePosY=-944
   NodeGuid=176C93F04A8B9B909364428600603AEF
   CustomProperties Pin (PinId=69197B0C466A02AD911A908C4E30B307,PinName="前置条件",PinType.PinCategory="Precondition",PinType.PinSubCategory="Private",PinType.PinSubCategoryObject=None,PinType.PinSubCategoryMemberReference=(),PinType.PinValueType=(),PinType.ContainerType=None,PinType.bIsReference=False,PinType.bIsConst=False,PinType.bIsWeakPointer=False,PinType.bIsUObjectWrapper=False,LinkedTo=(EventGraphNode_CP_And_5 AD2205BE424F8A88B3033496257C718B,),PersistentGuid=00000000000000000000000000000000,bHidden=False,bNotConnectable=False,bDefaultValueIsReadOnly=False,bDefaultValueIsIgnored=False,bAdvancedView=False,bOrphanedPin=False,)
   CustomProperties Pin (PinId=0487985F419F9D855E1FD684D28D3C0E,PinName="前置条件",Direction="EGPD_Output",PinType.PinCategory="Precondition",PinType.PinSubCategory="Private",PinType.PinSubCategoryObject=None,PinType.PinSubCategoryMemberReference=(),PinType.PinValueType=(),PinType.ContainerType=None,PinType.bIsReference=False,PinType.bIsConst=False,PinType.bIsWeakPointer=False,PinType.bIsUObjectWrapper=False,LinkedTo=(EventGraphNode_Precondition_4 810E1D1641719C9D90FE4CA16125037A,),PersistentGuid=00000000000000000000000000000000,bHidden=False,bNotConnectable=False,bDefaultValueIsReadOnly=False,bDefaultValueIsIgnored=False,bAdvancedView=False,bOrphanedPin=False,)
   CustomProperties Pin (PinId=024CE2B44C5619FBE6D40783D3B20FFE,PinName="前置条件",Direction="EGPD_Output",PinType.PinCategory="Precondition",PinType.PinSubCategory="Private",PinType.PinSubCategoryObject=None,PinType.PinSubCategoryMemberReference=(),PinType.PinValueType=(),PinType.ContainerType=None,PinType.bIsReference=False,PinType.bIsConst=False,PinType.bIsWeakPointer=False,PinType.bIsUObjectWrapper=False,LinkedTo=(EventGraphNode_Precondition_5 37F2E98F406FF7F922424DB28A55FDF3,),PersistentGuid=00000000000000000000000000000000,bHidden=False,bNotConnectable=False,bDefaultValueIsReadOnly=False,bDefaultValueIsIgnored=False,bAdvancedView=False,bOrphanedPin=False,)
End Object
Begin Object Class=/Script/EventEditor.EventGraphNode_Input Name="EventGraphNode_Input_23"
   Begin Object Class=/Game/EditorContent/Event/Input/EI_GetFilterActor.EI_GetFilterActor_C Name="EI_GetFilterActor_C_4"
   End Object
   Begin Object Name="EI_GetFilterActor_C_4"
      Field="target"
      NodeGuid=759F64EA45F343884E52C5A287CB8D14
      EventGraphNode=EventGraphNode_Input'"EventGraphNode_Input_23"'
   End Object
   EventNode=EI_GetFilterActor_C'"EI_GetFilterActor_C_4"'
   NodePosX=1552
   NodePosY=-944
   NodeGuid=759F64EA45F343884E52C5A287CB8D14
   CustomProperties Pin (PinId=3DD94DCD45F770B5D0053A920C72D77A,PinName="输入器",Direction="EGPD_Output",PinType.PinCategory="Input",PinType.PinSubCategory="Private",PinType.PinSubCategoryObject=None,PinType.PinSubCategoryMemberReference=(),PinType.PinValueType=(),PinType.ContainerType=None,PinType.bIsReference=False,PinType.bIsConst=False,PinType.bIsWeakPointer=False,PinType.bIsUObjectWrapper=False,LinkedTo=(EventGraphNode_Precondition_5 695E617646F731E49FC4A49C7587A555,),PersistentGuid=00000000000000000000000000000000,bHidden=False,bNotConnectable=False,bDefaultValueIsReadOnly=False,bDefaultValueIsIgnored=False,bAdvancedView=False,bOrphanedPin=False,)
End Object
```
</details>

## English is not my first language sorry if i butcher it :).
## Check youtube VIdeo below:
[![Video Title](https://img.youtube.com/vi/E43eZcV0NgY/0.jpg)](https://youtu.be/E43eZcV0NgY)
