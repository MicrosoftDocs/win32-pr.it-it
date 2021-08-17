---
title: Funzione EvaluateAttributeAtSample
description: Valuta in corrispondenza della posizione dell'esempio indicizzato.
ms.assetid: b5886004-5960-461d-a0d2-f4c3b0d09d94
keywords:
- Funzione EvaluateAttributeAtSample HLSL
topic_type:
- apiref
api_name:
- EvaluateAttributeAtSample
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 29191a3790afee2d37fee3d2ee8fb58673ff487af178bd8b1e2b33f26f1ec44c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982481"
---
# <a name="evaluateattributeatsample-function"></a>Funzione EvaluateAttributeAtSample

Valuta in corrispondenza della posizione dell'esempio indicizzato.

## <a name="syntax"></a>Sintassi

``` syntax
numeric EvaluateAttributeAtSample(
  in attrib numeric value,
  in uint sampleindex
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*value* \[ Pollici\]
</dt> <dd>

Tipo: **attrib numeric**

Valore di input.

</dd> <dt>

*sampleindex* \[ Pollici\]
</dt> <dd>

Tipo: **uint**

Percorso di esempio.

</dd> </dl>

## <a name="remarks"></a>Commenti

La modalità di interpolazione può **essere lineare** **o lineare senza \_ \_ prospettiva** sulla variabile. L'uso **di centroid** **o sample** viene ignorato. Sono consentiti anche attributi con interpolazione costante, nel qual caso l'indice di esempio viene ignorato.

### <a name="minimum-shader-model"></a>Modello di shader minimo

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

 

 




