---
title: mova-vs
description: Spostare i dati da un registro a virgola mobile nel registro degli indirizzi, a0.
ms.assetid: 929a0670-f337-4d6d-a7e7-d285e7dc8ae1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9ac29bf0d74b4eb2cb6cb86bdf6b070cf56823eb
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104976474"
---
# <a name="mova---vs"></a>mova-vs

Spostare i dati da un registro a virgola mobile nel [Registro degli indirizzi](dx9-graphics-reference-asm-vs-registers-address.md), a0.

## <a name="syntax"></a>Sintassi



| mova DST, src |
|---------------|



 

dove

-   DST deve essere il [Registro degli indirizzi](dx9-graphics-reference-asm-vs-registers-address.md), a0.
-   src è un registro di origine.

## <a name="remarks"></a>Commenti



| Versioni vertex shader | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| mova                   |      | x    | x    | x     | x    | x     |



 

Sposta i dati a virgola mobile in un registro di tipo Integer. I valori vengono convertiti da virgola mobile usando l'arrotondamento al più vicino.

Il registro indirizzi è l'unico registro di destinazione consentito.

Nel frammento di codice seguente vengono illustrate le operazioni eseguite.


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



Per le versioni 2 \_ x e successive, il registro degli indirizzi è un vettore di componenti. Pertanto, qualsiasi maschera di scrittura è consentita.


```
mova a0.xz, r0
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni vertex shader](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




