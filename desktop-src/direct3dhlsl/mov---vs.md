---
title: MOV-vs
description: Spostare i dati a virgola mobile tra i registri.
ms.assetid: bf013ab2-593e-4201-ba75-faebd0c9f97a
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 00f207261ad8ba6ac83360c40bc6008530292816
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "103719453"
---
# <a name="mov---vs"></a>MOV-vs

Spostare i dati a virgola mobile tra i registri.

## <a name="syntax"></a>Sintassi



| MOV DST, src |
|--------------|



 

dove

-   DST è il registro di destinazione.
-   src è un registro di origine.

## <a name="remarks"></a>Commenti



| Versioni vertex shader | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| MOV                    | x    | x    | x    | x     | x    | x     |



 

Può essere usato per i dati a virgola mobile. Per la versione di Visual Studio \_ 1 \_ , può essere usata anche per scrivere il registro degli indirizzi. Quando viene usato per aggiornare i registri indirizzi, i valori vengono convertiti da virgola mobile usando l'arrotondamento al più vicino.

Nel frammento di codice seguente vengono illustrate le operazioni eseguite.


```
if(dest is an integer register)
{
    int intSrc = RoundToNearest(src.w);
    dest = intSrc;
}
else
{
    dest = src;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni vertex shader](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




