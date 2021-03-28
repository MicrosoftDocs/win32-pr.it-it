---
title: RCP-vs
description: Calcola il reciproco del valore scalare di origine. | RCP-vs
ms.assetid: be638a42-b693-461d-ab0a-3a6c0fa1acfc
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 145a998cbca9dc3721d9c7d6ba251d539286a3f1
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104982010"
---
# <a name="rcp---vs"></a>RCP-vs

Calcola il reciproco del valore scalare di origine.

## <a name="syntax"></a>Sintassi



| RCP DST, src |
|--------------|



 

dove

-   DST è il registro di destinazione.
-   src è un registro di origine. Il registro di origine richiede l'uso esplicito di swizzle di replica, ovvero è necessario specificare esattamente uno dei componenti con estensione x, y, z, w swizzle (o. r,. g,. b,. a equivalenti).

## <a name="remarks"></a>Commenti



| Versioni vertex shader | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
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



L'output deve essere esattamente 1,0 se l'input è esattamente 1,0. Un'origine di 0,0 restituisce un valore infinito.

La precisione deve essere un errore assoluto di almeno 1,0/(2 ² ²) nell'intervallo (1,0, 2,0) perché le implementazioni comuni separano mantissa ed esponente.

Se l'origine non contiene pedici, viene usato il componente x.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni vertex shader](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




