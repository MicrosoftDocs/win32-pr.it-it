---
title: Posizione registro
description: Questo registro di output del vertex shader contiene dati di posizione per vertice.
ms.assetid: 98f71027-d94b-4dd0-a6b6-4b263954eff9
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 89470bb920db7c612b21cefb2c44c2c89d48ce28
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711086"
---
# <a name="position-register"></a>Posizione registro

Questo registro di output del vertex shader contiene dati di posizione per vertice.



| Versioni vertex shader | 1\_1 | 2 \_ 0 | 2 \_ SW | 2 \_ x | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|-------|------|------|-------|
| Posizione registro      | x    | x    | x     | x    | x    | x     |



 

Un registro è costituito da proprietà che determinano il comportamento di ogni registro.



| Proprietà        | Descrizione |
|-----------------|-------------|
| Nome            | oPos        |
| Conteggio           | 1 vettore    |
| Autorizzazioni di I/O | Sola scrittura. |



 

Il valore è la posizione nello spazio di ritaglio omogeneo. Questo valore deve essere scritto dal vertex shader.

Esempio


```
    dcl_position v0
    
    def c40, 0.0f,0.0f,0.0f,0.0f;
    // transform into projection space
    m4x4 r0,v0,c8
    max r0.z,c40.z,r0.z //clamp to 0
    max r0.w,c12.x,r0.w //clamp to near clip plane
    mov oPos,r0   
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registri vertex shader](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




