---
title: Modificatori di istruzione (informazioni di riferimento su HLSL VS)
description: Modificatori di istruzioni
ms.assetid: b713d847-c858-4492-918c-7a105f751624
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b2bdad90d13fe960c0d7a5cabfbb508d8abba890e8114c6d4ae1e47d1977e7d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119695"
---
# <a name="instruction-modifiers-hlsl-vs-reference"></a>Modificatori di istruzione (informazioni di riferimento su HLSL VS)

I modificatori di istruzione influiscono sul risultato dell'istruzione prima che venga scritta nel registro di destinazione.

## <a name="_sat"></a>\_Sab

Satura il risultato dell'istruzione a \[ 0,1 prima di scrivere nel registro di \] destinazione.

Ad esempio:


```
add_sat dst, src0, src1
```



Dove:

dst = chiusura \_ tra \_ 0 \_ e \_ 1(src0 + src1)

Il \_ modificatore di istruzione sat non costa slot di istruzioni aggiuntivi.

Se supportato, il modificatore di istruzione sat può essere usato con qualsiasi istruzione ad eccezione \_ di [frc - vs](frc---vs.md), [sincos - vs](sincos---vs.md)e [texldl - vs](texldl---vs.md).



| Versioni di vertex shader | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| \_Sab                  |      |      |      |       | x    | x     |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni per vertex shader](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




