---
description: hi
slug: oop-research-1
public: true
layout: ../../layouts/BlogPost.astro
title: งานค้นคว้าครั้งที่ 1
createdAt: 1667278497226
updatedAt: 1667292857953
tags:
  - Java
heroImage: /posts/oop-research-1_thumbnail.png
---
## OOP ย่อมาจากคำว่าอะไร และมีลักษณะอย่างไร
**OOP** ย่อมาจากคำว่า `Object-Oriented Programming` โดยที่ทุกอย่างภายในโปรแกรม จะถือว่าเป็น Object หนึ่งๆ โดยที่ข้อมูลจะอยู่ในลักษณะของ `fields`, `properties` หรือ `attributes` และโค้ดจะอยู่ในลักษณะของ `procedures` หรือ `method` โดยที่เราสามารถที่จะสร้างหรือลบออบเจ็กต์ต่างๆภายในโปรแกรมได้ แต่จะมี modifier ทำหน้าที่ในการป้องกันออบเจ็กต์บางตัวเพื่อป้องกันการเข้าถึงหรือการแก้ไข โดยที่คลาสจะมีออบเจ็กต์ต่างๆอยู่ภายใน
![oop-intro](/posts/oop-research-1_oop-intro.png)
## ประโยชน์ของการเขียนโปรแกรมเชิงวัตถุคืออะไร
ประโยชน์ของการเขียนโปรแกรมเชิงวัตถุคือ เราสามารถนำโค้ดกลับมาใช้ใหม่ได้อย่างมีประสิทธิภาพ เพราะทุกอย่างถูกเก็บไว้เป็นคลาสๆหรือออบเจ็กต์อยู่แล้ว และเราสามารถที่จะเขียนโค้ดที่น้อยลงได้ และมีระเบียบมากขึ้น เนื่องด้วยหลักการของ Inheritance ที่จะมีคลาสหลัก หรือ Superclass ที่ทำหน้าที่กำหนด Template หรือหลักการในการเขียนไว้แล้ว และเราก็สามารถที่จะ extend หรือขยาย Superclass ออกมาเพื่อใช้งานได้ทันที
![inheritance](/posts/oop-research-1_inheritance.png)
## มีภาษาใดบ้างที่สนับสนุนการเขียนโปรแกรมเชิงวัตถุพร้อมอธิบายลักษณะของภาษาในข้อที่ 3 โดยเลือกมา 1 ภาษา ว่ามีความเป็นโปรแกรมเชิงวัตถุอย่างไร
- Java
- Typescript
- C#
 
โดยที่ Typescript ใช้ Javascript เป็นฐานอีกที และถูกสร้างมาเพื่อเพิ่มหลักการ `Typing`, `interfaces`, และ `classes` ขึ้นมา
ตัวอย่างเช่น

```tsx
// src/components/card.tsx
import React, { ReactNode, Component } from 'react'

type Props = {
  children: {
    header: ReactNode
    media: ReactNode
    content: ReactNode
    actions: ReactNode
  }
}

export class Card extends Component<Props> { // Inheritance ที่ Inherit มาจากคลาส Component กลายเป็นคลาส Card
  render() { // เมธอด render
    const { header, content, media, actions } = this.props.children

    return (
      <div className="card bg-orange-200 dark:bg-zinc-700 hover:bg-orange-300 dark:hover:bg-zinc-800">{header}</div>
      <div className="card bg-orange-200 dark:bg-zinc-700 hover:bg-orange-300 dark:hover:bg-zinc-800">{content}</div>
      <div className="card bg-orange-200 dark:bg-zinc-700 hover:bg-orange-300 dark:hover:bg-zinc-800">{media}</div>
      <div className="card bg-orange-200 dark:bg-zinc-700 hover:bg-orange-300 dark:hover:bg-zinc-800">{actions}</div>
    )
  }
}
```

## ยกตัวอย่างวัตถุที่นักเรียนเกี่ยวข้องในชีวิตประจำวัน เพื่ออธิบายถึง วัตถุ(Object) คุณสมบัติ (Attributes) และพฤติกรรม (Behavior) มา 2 วัตถุ
- มนุษย์ โดยที่
  - Class: มนุษย์ โดยมีรากฐานมาจากอฟริกา โดยที่กลายมาเป็นสิ่งมีชีวิตเลี้ยงลูกด้วยนมที่ทำหน้าที่ต่างๆ
  - Object: มนุษย์
  - Attributes: ชื่อ อายุ ความสูง น้ำหนัก
  - Behavior: เดิน พูด กิน นอน
- เครื่องดูดฝุ่น
  - Class: เครื่องดูดฝุ่นเป็นอุปกรณ์ทางอิเล็กทรอนิกส์ที่ทำหน้าที่ดูดอากาศเข้าไปในเครื่องเพื่อที่จะดูดฝุ่นเข้าไป
  - Object: เครื่องดูดฝุ่น
  - Attributes: ความจุ ขนาด
  - Behavior: ดูดฝุ่น เก็บไปยังถุง
 
## จงแยกองค์ประกอบของวัตถุนี้ออกเป็นส่วน ๆ ว่าประกอบด้วยส่วนประกอบอะไรบ้าง โดยใส่ภาพประกอบแต่ละชิ้นส่วนให้ดูด้วย
### Mechanical Pencil - ดินสอกด
![mech-pencil](/posts/oop-research-1_mech-pencil.png)
- cap - ฝาปุ่มกด
- identification seal - ที่ครอบ
- end stopper - ตัวป้องกันใส้ดินสอไม่ให้ไหล
- lead tank - จุดเก็บใส้ดินสอ
- chuck - ปลายดินสอกดที่ขยับได้
- plunger - ปลายรองไส้ดินสอ
- Inner Barrel - จุดหยุดไส้

### RC Car - รถบังคับวิทยุ
![rc](/posts/oop-research-1_rc.png)
- Water Resistance ESC - วงจรควบคุมความเร็วรถบังคับ
- Brushed Motor - 