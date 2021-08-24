---
title: dp3 - vs
description: Calcola il prodotto del punto a tre componenti dei registri di origine. | dp3 - vs
ms.assetid: a5263a18-ed53-41eb-85ca-2cff872e03d8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bf65f77a60ea7ac19ef5ea204f916387c65c3bee08c89ea274e800f650ef241d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119673871"
---
# <a name="dp3---vs"></a>dp3 - vs

Calcola il prodotto del punto a tre componenti dei registri di origine.

## <a name="syntax"></a>Sintassi



| dp3 dst, src0, src1 |
|---------------------|



 

dove

-   dst è il registro di destinazione.
-   src0 è un registro di origine.
-   src1 è un registro di origine.

## <a name="remarks"></a>Commenti



| Versioni di vertex shader | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| dp3                    | x    | x    | x    | x     | x    | x     |



 

Il frammento di codice seguente illustra le operazioni eseguite:


```
dest.w = (src0.x * src1.x) + (src0.y * src1.y) + (src0.z * src1.z);
dest.x = dest.y = dest.z = dest.w;
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni per vertex shader](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




