---
title: Modificatori di istruzioni (riferimento di HLSL VS)
description: Modificatori di istruzione
ms.assetid: b713d847-c858-4492-918c-7a105f751624
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 573f2ef618c4cd29092fb38fb4c805bdeeecc219
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/23/2019
ms.locfileid: "104472075"
---
# <a name="instruction-modifiers-hlsl-vs-reference"></a>Modificatori di istruzioni (riferimento di HLSL VS)

I modificatori di istruzione influiscono sul risultato dell'istruzione prima che venga scritto nel registro di destinazione.

## <a name="_sat"></a>\_Sat

Satura (o clamp) il risultato dell'istruzione in \[ 0, 1 \] intervallo prima della scrittura nel registro di destinazione.

Ad esempio:


```
add_sat dst, src0, src1
```



Dove:

DST = morsetto \_ compreso tra \_ 0 \_ e \_ 1 (src0 + src1)

Il \_ modificatore di istruzioni Sat non costa nessun slot di istruzione aggiuntivo.

Se supportato, il \_ modificatore di istruzioni Sat può essere usato con qualsiasi istruzione tranne: [FRC-vs](frc---vs.md), [SinCos-vs](sincos---vs.md)e [texldl-vs](texldl---vs.md).



| Versioni vertex shader | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| \_Sat                  |      |      |      |       | x    | x     |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni vertex shader](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




