---
title: EvaluateAttributeSnapped (funzione)
description: Valuta in corrispondenza del baricentro del pixel con un offset.
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
ms.openlocfilehash: 70a9389ed9e9f4fff16f82610cb611bc4da2c7a3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104992896"
---
# <a name="evaluateattributesnapped-function"></a>EvaluateAttributeSnapped (funzione)

Valuta in corrispondenza del baricentro del pixel con un offset.

## <a name="syntax"></a>Sintassi

``` syntax
numeric EvaluateAttributeSnapped(
  in attrib numeric value,
  in 
            int2 offset
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*valore* \[ di in\]
</dt> <dd>

Tipo: formato **numerico attrib**

Valore di input.

</dd> <dt>

*offset* \[ in\]
</dt> <dd>

Tipo: **int2**

Offset 2D dal centro pixel mediante una griglia 16x16.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'intervallo per il parametro *offset* deve essere definito dal codice byte seguente.

Vengono utilizzati solo i 4 bit meno significativi dei primi due componenti (U, V) dell'offset pixel. La conversione dal punto fisso a 4 bit a float è la seguente (MSB... LSB), in cui MSB è una parte della frazione e determina il segno:

-   1000 =-0,5 f (-8/16)
-   1001 =-0.4375 f (-7/16)
-   1010 =-0.375 f (-6/16)
-   1011 =-0.3125 f (-5/16)
-   1100 =-0,25 f (-4/16)
-   1101 =-0.1875 f (-3/16)
-   1110 =-0,125 f (-2/16)
-   1111 =-0.0625 f (-1/16)
-   0000 = 0,0 f (0/16)
-   0001 = 0.0625 f (1/16)
-   0010 = 0,125 f (2/16)
-   0011 = 0.1875 f (3/16)
-   0100 = 0,25 f (4/16)
-   0101 = 0.3125 f (5/16)
-   0110 = 0.375 f (6/16)
-   0111 = 0.4375 f (7/16)

> [!Note]  
> I bordi sinistro e superiore di un pixel sono inclusi nell'offset; Tuttavia, i bordi inferiore e destro non sono inclusi. Tutti gli altri bit nei valori di offset integer a 32 bit vengono ignorati.

 

Un'implementazione può assumere l'offset fornito dallo shader e ottenere un valore a punto fisso a 32 bit completo (28,4), che si estende sull'intervallo valido, eseguendo il calcolo seguente:


```
iU = (iU<<28)>>28  // keep lowest 4 bits and sign extend, which yields [-8..7]
```



Se un'implementazione deve eseguire il mapping dell'offset a un offset a virgola mobile, viene eseguito il calcolo seguente:


```
fU = ((float)iU)/16
```



### <a name="minimum-shader-model"></a>Modello Shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                                                | Supportato |
|-----------------------------------------------------------------------------|-----------|
| [Shader Model 5](d3d11-graphics-reference-sm5.md) e versioni successive shader Models | sì       |



 

Questa funzione è supportata nei tipi di shader seguenti:



| Vertice | Hull | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     |         |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni intrinseche](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Modello Shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




