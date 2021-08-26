---
title: abs - vs
description: Calcola il valore assoluto. | abs - vs
ms.assetid: d3b4cf06-dc87-4c71-aa2d-5ade4cf98caa
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 59ba7ad170df49b252140b14452862bdf14c2b713ac457548c8f085a0fb50881
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120025091"
---
# <a name="abs---vs"></a>abs - vs

Calcola il valore assoluto.

## <a name="syntax"></a>Sintassi

**abs dst, src**

dove

- dst è il registro di destinazione.
- src è un registro di origine.

## <a name="remarks"></a>Commenti



| Versioni di vertex shader | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| abs                    |      | x    | x    | x     | x    | x     |



 

Questa istruzione funziona come illustrato di seguito.


```
dest.x = abs(src.x)
dest.y = abs(src.y)
dest.z = abs(src.z)
dest.w = abs(src.w)
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni per vertex shader](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




