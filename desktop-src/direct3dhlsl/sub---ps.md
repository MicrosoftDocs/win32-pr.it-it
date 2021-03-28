---
title: Sub-PS
description: Sottrae le origini. | Sub-PS
ms.assetid: e130724f-63bf-4d7f-bc9f-6a4441a788b8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4998892aa06eff55632600a9c2f7fe359c11f830
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103761608"
---
# <a name="sub---ps"></a>Sub-PS

Sottrae le origini.

## <a name="syntax"></a>Sintassi



| Sub DST, src0, src1 |
|---------------------|



 

dove

-   DST è il registro di destinazione.
-   src0 è un registro di origine.
-   src1 è un registro di origine.

## <a name="remarks"></a>Commenti



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| sub                   | x    | x    | x    | x    | x    | x    | x     | x    | x     |



 

Questa istruzione esegue la sottrazione mostrata in questa formula.


```
dest = src0 - src1
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




