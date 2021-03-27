---
title: EvaluateAttributeAtCentroid (funzione)
description: Restituisce il baricentro del pixel.
ms.assetid: 6735b3f4-765f-4cd9-9f38-326a52709021
keywords:
- Funzione EvaluateAttributeAtCentroid HLSL
topic_type:
- apiref
api_name:
- EvaluateAttributeAtCentroid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ee95c7f2f202dfd0065e5e9c30003cc46fd29281
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104397726"
---
# <a name="evaluateattributeatcentroid-function"></a>EvaluateAttributeAtCentroid (funzione)

Restituisce il baricentro del pixel.

## <a name="syntax"></a>Sintassi

``` syntax
numeric EvaluateAttributeAtCentroid(
  in attrib numeric value
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*valore* \[ di in\]
</dt> <dd>

Tipo: formato **numerico attrib**

Valore di input.

</dd> </dl>

## <a name="remarks"></a>Commenti

La modalità di interpolazione può essere **lineare** o **lineare \_ senza alcuna \_ prospettiva** sulla variabile. L'uso **di centro** o **campione** viene ignorato. Sono consentiti anche gli attributi con interpolazione costante. in questo caso, l'indice di esempio viene ignorato.

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

 

 




