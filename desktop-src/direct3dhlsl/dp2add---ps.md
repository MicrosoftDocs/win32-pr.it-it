---
title: dp2add-PS
description: Esegue un prodotto 2D a virgola e un'aggiunta scalare.
ms.assetid: 4226ee34-2e68-4536-b171-68f3b967182e
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 88d3d28cc64bdb7caa1b7456e87711c3dbee2b13
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104117185"
---
# <a name="dp2add---ps"></a>dp2add-PS

Esegue un prodotto 2D a virgola e un'aggiunta scalare.

## <a name="syntax"></a>Sintassi


```
dp2add dst, src0, src1, src2.{x|y|z|w}
```



Dove:

-   DST è un registro di destinazione.
-   src0, src1 e src2 sono tre registri di origine.
-   {x \| y \| z \| w} è la replica obbligatoria swizzle in src2.

## <a name="remarks"></a>Commenti



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| dp2add                |      |      |      |      | x    | x    | x     | x    | x     |



 

Il valore scalare per Aggiungi viene scelto dalla replica swizzle in src2.

Il frammento di codice seguente mostra le operazioni eseguite.


```
dest = src0.r * src1.r + src0.g * src1.g + src2.replicate_swizzle
// The scalar result is replicated to the write mask components
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




