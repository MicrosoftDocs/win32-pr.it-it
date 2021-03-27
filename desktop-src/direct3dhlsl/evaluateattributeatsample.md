---
title: EvaluateAttributeAtSample (funzione)
description: Valuta in corrispondenza della posizione di esempio indicizzata.
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
ms.openlocfilehash: b183f86599d08a6892e33c169b938dc09a2b55de
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718142"
---
# <a name="evaluateattributeatsample-function"></a>EvaluateAttributeAtSample (funzione)

Valuta in corrispondenza della posizione di esempio indicizzata.

## <a name="syntax"></a>Sintassi

``` syntax
numeric EvaluateAttributeAtSample(
  in attrib numeric value,
  in uint sampleindex
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*valore* \[ di in\]
</dt> <dd>

Tipo: formato **numerico attrib**

Valore di input.

</dd> <dt>

*sampleindex* \[ in\]
</dt> <dd>

Tipo: **uint**

Percorso di esempio.

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

 

 




