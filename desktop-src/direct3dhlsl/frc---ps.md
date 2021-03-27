---
title: FRC-PS
description: Restituisce la parte frazionaria di ogni componente di input. | FRC-PS
ms.assetid: 378bc516-c81e-4538-8d6f-987536b19467
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a16dd518333efa1dce878c1418547bc0527d1d64
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353416"
---
# <a name="frc---ps"></a>FRC-PS

Restituisce la parte frazionaria di ogni componente di input.

## <a name="syntax"></a>Sintassi



| FRC DST, src |
|--------------|



 

dove

-   DST è il registro di destinazione.
-   src è un registro di origine.

## <a name="remarks"></a>Commenti



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| FRC                   |      |      |      |      | x    | x    | x     | x    | x     |



 

Il frammento di codice seguente mostra concettualmente il funzionamento dell'istruzione.


```
dest.x = src.x - (float)floor(src.x);
dest.y = src.y - (float)floor(src.y);
dest.z = src.z - (float)floor(src.z);
dest.w = src.w - (float)floor(src.w);
```



La funzione floor converte l'argomento passato all'intero più grande che è minore o uguale all'argomento. Viene convertito in un valore float, quindi viene sottratto il valore originale. Il valore frazionario risultante è compreso tra 0,0 e 1,0.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




