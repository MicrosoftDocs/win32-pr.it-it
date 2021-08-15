---
title: mova - vs
description: Spostare i dati da un registro a virgola mobile al registro indirizzi, a0.
ms.assetid: 929a0670-f337-4d6d-a7e7-d285e7dc8ae1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: dec849009ee47b4aaef1bc3766e2b141a8a6ccf5e17b16a370c6ea8284eaf957
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986331"
---
# <a name="mova---vs"></a>mova - vs

Spostare i dati da un registro a virgola mobile al registro [indirizzi](dx9-graphics-reference-asm-vs-registers-address.md), a0.

## <a name="syntax"></a>Sintassi



| mova dst, src |
|---------------|



 

dove

-   dst deve essere il [registro indirizzi](dx9-graphics-reference-asm-vs-registers-address.md), a0.
-   src è un registro di origine.

## <a name="remarks"></a>Commenti



| Versioni di vertex shader | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| Mova                   |      | x    | x    | x     | x    | x     |



 

Sposta i dati a virgola mobile in un registro integer. I valori vengono convertiti da virgola mobile usando l'arrotondamento al più vicino.

Il registro indirizzi è l'unico registro di destinazione consentito.

Il frammento di codice seguente illustra le operazioni eseguite.


```
if(dest is an integer register)
{
    int intSrc = RoundToNearest(src);
    dest = intSrc;
}
else
{
    dest = src;
}
```



Per le versioni 2 \_ x e successive, il registro indirizzi è un vettore di componenti. Pertanto, qualsiasi maschera di scrittura è consentita.


```
mova a0.xz, r0
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni per vertex shader](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




