---
title: RSQ-vs
description: Calcola la radice quadrata reciproca (solo positivo) del valore scalare di origine. | RSQ-vs
ms.assetid: 1ac37dad-0cea-41af-8dae-f299896462b1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f477d6f7d8a7ff94472c689bf5844183e2f016ee
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981799"
---
# <a name="rsq---vs"></a>RSQ-vs

Calcola la radice quadrata reciproca (solo positivo) del valore scalare di origine.

## <a name="syntax"></a>Sintassi



| RSQ DST, src |
|--------------|



 

dove

-   DST è il registro di destinazione.
-   src è un registro di origine. Il registro di origine richiede l'uso esplicito di swizzle di replica, ovvero è necessario specificare esattamente uno dei componenti con estensione x, y, z, w swizzle (o. r,. g,. b,. a equivalenti).

## <a name="remarks"></a>Commenti



| Versioni vertex shader | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| RSQ                    | x    | x    | x    | x     | x    | x     |



 

Nel frammento di codice seguente vengono illustrate le operazioni eseguite.


```
float f = abs(src0);
if (f == 0)
    f = FLT_MAX
else
{
    if (f != 1.0)
        f = 1.0/(float)sqrt(f);
}

dest.z = dest.y = dest.z = dest.w = f;
```



Il valore assoluto viene prelevato prima dell'elaborazione.

La precisione deve essere un errore assoluto di almeno 1,0/(2 ² ²) nell'intervallo (1,0, 4,0) perché le implementazioni comuni separano mantissa ed esponente.

Se l'origine non include indici, viene usato il componente x. L'output deve essere esattamente 1,0 se l'input è esattamente 1,0. Un'origine di 0,0 restituisce un valore infinito.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni vertex shader](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




