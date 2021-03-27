---
title: DP3-vs
description: Calcola il prodotto del punto a tre componenti dei registri di origine. | DP3-vs
ms.assetid: a5263a18-ed53-41eb-85ca-2cff872e03d8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 81580401f25ddcf7ce1c1d53475d0c3beba74a89
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104234631"
---
# <a name="dp3---vs"></a>DP3-vs

Calcola il prodotto del punto a tre componenti dei registri di origine.

## <a name="syntax"></a>Sintassi



| DP3 DST, src0, src1 |
|---------------------|



 

dove

-   DST è il registro di destinazione.
-   src0 è un registro di origine.
-   src1 è un registro di origine.

## <a name="remarks"></a>Commenti



| Versioni vertex shader | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| dp3                    | x    | x    | x    | x     | x    | x     |



 

Il frammento di codice seguente mostra le operazioni eseguite:


```
dest.w = (src0.x * src1.x) + (src0.y * src1.y) + (src0.z * src1.z);
dest.x = dest.y = dest.z = dest.w;
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni vertex shader](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




