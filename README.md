# Multizone Recovery Demo
![image](https://github.com/yalezhang2021/MultiZoneRecovery-demo/assets/74490220/06c2d0d7-e0f4-4cfc-95eb-af69fd1b2c0a)
![image](https://github.com/yalezhang2021/MultiZoneRecovery-demo/assets/74490220/9bab2681-97b5-4606-960a-dc11e52f86a4)
![image](https://github.com/yalezhang2021/MultiZoneRecovery-demo/assets/74490220/8af6c587-f7f4-47a6-b475-223615996aa9)


1. This simple system has 4 sections and 3 pallets running on it.![屏幕截图 2024-01-09 010906.png](https://github.com/yalezhang2021/MultiZoneRecovery-demo/blob/master/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202024-01-09%20010906.png?raw=true)

2. Now section 3 is disabled, the original system will stop work immediately. But we get a new requirement, they want the other enabled part still work at this situation...

![屏幕截图 2024-01-09 010946.png](https://github.com/yalezhang2021/MultiZoneRecovery-demo/blob/master/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202024-01-09%20010946.png?raw=true)

3. So I need create a new case for "partially recovery" in the work flow, and when the other 2 pallets move back to their recovery positions, and not all sections enabled, go to this state. For that i need upgrade the recovery positions and check the boundary of the enabled part, determine the recovery sequence and the directions, then let them recovery. This part is complex, luckily I can reuse many existed functions in the source code :)

![屏幕截图 2024-01-09 011136.png](https://github.com/yalezhang2021/MultiZoneRecovery-demo/blob/master/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202024-01-09%20011136.png?raw=true)

4. If the situation meets the recovery conditions, then do the recovery. After the 2 pallets go back to their recovery positions, they will move foreword again automatically and end to the boundary. 

![屏幕截图 2024-01-09 011223.png](https://github.com/yalezhang2021/MultiZoneRecovery-demo/blob/master/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202024-01-09%20011223.png?raw=true)
