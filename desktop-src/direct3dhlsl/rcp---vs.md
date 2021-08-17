---
title: rcp - vs
description: Calcola il reciproco dello scalare di origine. | rcp - vs
ms.assetid: be638a42-b693-461d-ab0a-3a6c0fa1acfc
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d9ec2c011e4f365f7cedc1191522836db098da976c4ce3c5153169a1d87f180d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119672301"
---
# <a name="rcp---vs"></a>rcp - vs

Calcola il reciproco dello scalare di origine.

## <a name="syntax"></a>Sintassi



| rcp dst, src |
|--------------|



 

dove

-   dst è il registro di destinazione.
-   src è un registro di origine. Il registro di origine richiede l'uso esplicito dello swizzle di replica, ovvero è necessario specificare esattamente uno dei componenti .x, .y, .z, .w swizzle (o .r, .g, .b, .a equivalents).

## <a name="remarks"></a>Commenti



| Versioni vertex shader | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| rcp                    | x    | x    | x    | x     | x    | x     |



 

Nel frammento di codice seguente vengono illustrate le operazioni eseguite.


```
float f = src0;
if(f == 0.0f)
{
    f = FLT_MAX;
}
else 
{
    if(f != 1.0)
    {
        f = 1/f;
    }
}

dest = f;
```



L'output deve essere esattamente 1,0 se l'input è esattamente 1,0. Un'origine di 0,0 restituisce infinito.

La precisione deve essere almeno un errore assoluto di 1,0/(2°) nell'intervallo (1.0, 2.0) perché le implementazioni comuni separano mantissa ed esponente.

Se l'origine non ha pedi, viene usato il componente x.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni per vertex shader](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




