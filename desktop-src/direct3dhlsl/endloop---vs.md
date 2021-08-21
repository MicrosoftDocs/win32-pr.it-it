---
title: endloop - vs
description: Fine di un ciclo... blocco endloop.
ms.assetid: fd7df120-a927-4a66-b152-6ce5247446e4
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: cdd9158d12ecc29073526833a7a4ca5eec03100558a9ebdc711822c7ca74c9bc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119949891"
---
# <a name="endloop---vs"></a>endloop - vs

Fine di un [ciclo](loop---vs.md)... blocco endloop.

## <a name="syntax"></a>Sintassi



| endloop |
|---------|



 

## <a name="remarks"></a>Commenti



| Versioni di vertex shader | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| endloop                |      | x    | x    | x     | x    | x     |



 

Questa istruzione funziona come illustrato di seguito.


```
LoopCounter += LoopStep;
LoopInterationCount = LoopIterationCount - 1;
if (LoopIterationCount > 0)
    Continue execution at the StartLoopOffset
```



endloop deve seguire l'ultima istruzione di [un ciclo , rispetto al](loop---vs.md) blocco .

## <a name="example"></a>Esempio


```
loop aL, i3
    add r1, r0, c2[ aL ]
endloop
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni per vertex shader](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




