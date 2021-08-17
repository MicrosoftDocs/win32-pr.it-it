---
title: frc - vs
description: Restituisce la parte frazionaria di ogni componente di input. | frc - vs
ms.assetid: 6b6a4475-b665-4de0-9423-88ea8103e606
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b2ecc6a1c903f78fb7c03442809f792e3ddb984d04975d3f5ecb0b5c918f7ab4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117907644"
---
# <a name="frc---vs"></a>frc - vs

Restituisce la parte frazionaria di ogni componente di input.

## <a name="syntax"></a>Sintassi



| frc dst, src |
|--------------|



 

dove

-   dst è il registro di destinazione.
-   src è un registro di origine.

## <a name="remarks"></a>Commenti



| Versioni vertex shader | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| Frc                    | x    | x    | x    | x     | x    | x     |



 

Nel frammento di codice seguente viene illustrato concettualmente il funzionamento dell'istruzione .


```
dest.x = src.x - (float)floor(src.x);
dest.y = src.y - (float)floor(src.y);
dest.z = src.z - (float)floor(src.z);
dest.w = src.w - (float)floor(src.w);
```



La funzione floor converte l'argomento passato all'intero più grande minore o uguale all'argomento . Viene convertito in un valore float e quindi sottratto dal valore originale. Il valore frazionario risultante è compreso tra 0,0 e 1,0.

Per la versione 1 1, le maschere di scrittura consentite sono \_ .y e .xy (.x non è consentito).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni per vertex shader](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




