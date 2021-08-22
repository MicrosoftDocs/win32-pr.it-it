---
title: Funzione EvaluateAttributeSnapped
description: Valuta in corrispondenza del centroide pixel con un offset.
ms.assetid: f5085016-0e94-49bb-96b6-42fa15c30b9f
keywords:
- Funzione EvaluateAttributeSnapped HLSL
topic_type:
- apiref
api_name:
- EvaluateAttributeSnapped
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5408b2c8133947b948bc42eb6ff0c725584b0cf2c60ccf0731a9d584d3c898a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118512018"
---
# <a name="evaluateattributesnapped-function"></a>Funzione EvaluateAttributeSnapped

Valuta in corrispondenza del centroide pixel con un offset.

## <a name="syntax"></a>Sintassi

``` syntax
numeric EvaluateAttributeSnapped(
  in attrib numeric value,
  in 
            int2 offset
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*value* \[ Pollici\]
</dt> <dd>

Tipo: **attrib numeric**

Valore di input.

</dd> <dt>

*offset* \[ Pollici\]
</dt> <dd>

Tipo: **int2**

Offset 2D dal centro pixel usando una griglia 16x16.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'intervallo per *il parametro offset* deve essere definito dal codice byte seguente.

Vengono usati solo i 4 bit meno significativi dei primi due componenti (U, V) dell'offset in pixel. La conversione dal punto fisso a 4 bit a float è la seguente (MSB... LSB), dove MSB è sia una parte della frazione che determina il segno:

-   1000 = -0,5f (-8 / 16)
-   1001 = -0,4375f (-7 / 16)
-   1010 = -0,375f (-6 / 16)
-   1011 = -0,3125f (-5 / 16)
-   1100 = -0,25f (-4 / 16)
-   1101 = -0,1875f (-3 / 16)
-   1110 = -0,125f (-2 / 16)
-   1111 = -0,0625f (-1 / 16)
-   0000 = 0,0f ( 0 / 16)
-   0001 = 0,0625f ( 1 /16)
-   0010 = 0,125f ( 2 /16)
-   0011 = 0,1875f ( 3 /16)
-   0100 = 0,25f ( 4 /16)
-   0101 = 0,3125f ( 5 /16)
-   0110 = 0,375f ( 6 /16)
-   0111 = 0,4375f ( 7 /16)

> [!Note]  
> I bordi sinistro e superiore di un pixel sono inclusi nell'offset. Tuttavia, i bordi inferiore e destro non sono inclusi. Tutti gli altri bit nell'intero a 32 bit vengono ignorati.

 

Un'implementazione può prendere l'offset fornito dallo shader e ottenere un valore a virgola fissa a 32 bit completo (28,4), che si estende sull'intervallo valido, eseguendo il calcolo seguente:


```
iU = (iU<<28)>>28  // keep lowest 4 bits and sign extend, which yields [-8..7]
```



Se un'implementazione deve eseguire il mapping dell'offset a un offset a virgola mobile, esegue il calcolo seguente:


```
fU = ((float)iU)/16
```



### <a name="minimum-shader-model"></a>Modello di shader minimo

Questa funzione è supportata nei modelli di shader seguenti.



| Modello di shader                                                                | Supportato |
|-----------------------------------------------------------------------------|-----------|
| [Modello shader 5 e](d3d11-graphics-reference-sm5.md) modelli di shader superiori | sì       |



 

Questa funzione è supportata nei tipi di shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     |         |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni intrinseche](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Modello shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




