---
title: Funzione EvaluateAttributeAtCentroid
description: Valuta in corrispondenza del centroide pixel.
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
ms.openlocfilehash: 867f7dadc2ccf7d86eed602dd9e65d07be7558f0a8a00426e3a45bc1c2c97a3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119744041"
---
# <a name="evaluateattributeatcentroid-function"></a>Funzione EvaluateAttributeAtCentroid

Valuta in corrispondenza del centroide pixel.

## <a name="syntax"></a>Sintassi

``` syntax
numeric EvaluateAttributeAtCentroid(
  in attrib numeric value
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*value* \[ Pollici\]
</dt> <dd>

Tipo: **attrib numeric**

Valore di input.

</dd> </dl>

## <a name="remarks"></a>Commenti

La modalità di interpolazione può **essere lineare** **o lineare senza \_ \_ prospettiva** sulla variabile. **L'uso di centroid** **o sample** viene ignorato. Sono consentiti anche attributi con interpolazione costante, nel qual caso l'indice di esempio viene ignorato.

### <a name="minimum-shader-model"></a>Modello shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                                                | Supportato |
|-----------------------------------------------------------------------------|-----------|
| [Modelli shader modello 5](d3d11-graphics-reference-sm5.md) e versioni successive | sì       |



 

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

 

 




