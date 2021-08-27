---
title: Registro delle posizioni
description: Questo registro di output del vertex shader contiene dati sulla posizione per vertice.
ms.assetid: 98f71027-d94b-4dd0-a6b6-4b263954eff9
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: cda82431990ed3ea545adfcc5e6eb2801be0607d8bac45aa1bcd8c0e121f3d68
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023901"
---
# <a name="position-register"></a>Registro delle posizioni

Questo registro di output del vertex shader contiene dati sulla posizione per vertice.



| Versioni vertex shader | 1\_1 | 2 \_ 0 | 2 \_ sw | 2 \_ x | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|-------|------|------|-------|
| Registro delle posizioni      | x    | x    | x     | x    | x    | x     |



 

Un registro è costituito da proprietà che determinano il comportamento di ogni registro.



| Proprietà        | Descrizione |
|-----------------|-------------|
| Nome            | Opos        |
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

 

 




