---
title: CMP-PS
description: Scegliere src1 se src0 0. In caso contrario, scegliere src2. Il confronto viene eseguito per canale.
ms.assetid: 8fabd548-3f5e-4b78-bf1e-16e4f1548ccd
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: da3da1062d02e995876a1f67e5c4e19518774760
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104046081"
---
# <a name="cmp---ps"></a>CMP-PS

Scegliere src1 se src0 >= 0. In caso contrario, scegliere src2. Il confronto viene eseguito per canale.

## <a name="syntax"></a>Sintassi



| CMP DST, src0, src1, src2 |
|---------------------------|



 

dove

-   DST è il registro di destinazione.
-   src0 è un registro di origine.
-   src1 è un registro di origine.
-   src2 è un registro di origine.

## <a name="remarks"></a>Commenti



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| CMP                   |      | x    | x    | x    | x    | x    | x     | x    | x     |



 

Esistono alcune limitazioni aggiuntive per le versioni 1 \_ 2 e 1 \_ 3:

-   Ogni shader può utilizzare fino a un massimo di tre istruzioni CMP.
-   Il registro di destinazione non può essere uguale a uno dei registri di origine.

Questo esempio esegue un confronto a quattro canali.


```
ps_1_4
def c0, -0.6, 0.6, 0, 0.6
def c1  0,0,0,0
def c2  1,1,1,1

mov r1, c1
mov r2, c2

cmp r0, c0, r1, r2   // r0 is assigned 1,0,0,0 based on the following:

// r0.x = c2.x because c0.x < 0
// r0.y = c1.y because c0.y >= 0
// r0.z = c1.z because c0.z >= 0
// r0.w = c1.w because c0.w >= 0
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




