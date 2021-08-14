---
title: rsq - vs
description: Calcola la radice quadrata reciproca (solo positiva) dello scalare di origine. | rsq - vs
ms.assetid: 1ac37dad-0cea-41af-8dae-f299896462b1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 937f89a018943d9ab8f74a4a328316d5d68dca7d48730a06b80814dacbd8ed68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118510908"
---
# <a name="rsq---vs"></a>rsq - vs

Calcola la radice quadrata reciproca (solo positiva) dello scalare di origine.

## <a name="syntax"></a>Sintassi



| rsq dst, src |
|--------------|



 

dove

-   dst è il registro di destinazione.
-   src è un registro di origine. Il registro di origine richiede l'uso esplicito di replicate swizzle, ovvero esattamente uno dei componenti .x, .y, .z, .w swizzle (o .r, .g, .b, .a equivalenti) deve essere specificato.

## <a name="remarks"></a>Commenti



| Versioni di vertex shader | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| Rsq                    | x    | x    | x    | x     | x    | x     |



 

Il frammento di codice seguente illustra le operazioni eseguite.


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



Il valore assoluto viene assunto prima dell'elaborazione.

La precisione deve essere almeno 1,0/(2²²) errore assoluto nell'intervallo (1.0, 4.0) perché le implementazioni comuni separeranno mantissa ed esponente.

Se source non ha pedi, viene usato il componente x. L'output deve essere esattamente 1,0 se l'input è esattamente 1,0. Un'origine 0,0 restituisce infinito.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni per vertex shader](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




