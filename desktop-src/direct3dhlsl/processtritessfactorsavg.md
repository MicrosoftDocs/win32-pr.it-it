---
title: Funzione ProcessTriTessFactorsAvg
description: Genera i fattori a tessitori corretti per una tri patch. | Funzione ProcessTriTessFactorsAvg
ms.assetid: 005a63b6-f35d-42d6-bb29-f4ebb374080e
keywords:
- Funzione ProcessTriTessFactorsAvg HLSL
topic_type:
- apiref
api_name:
- ProcessTriTessFactorsAvg
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2d119ee7011bbd4a03a2a2c8247b9df9e95f983e07ffd3ab3e4603a3a3eaa7de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067771"
---
# <a name="processtritessfactorsavg-function"></a>Funzione ProcessTriTessFactorsAvg

Genera i fattori a tessitori corretti per una tri patch.

## <a name="syntax"></a>Sintassi

``` syntax
void ProcessTriTessFactorsAvg(
  in  float3 RawEdgeFactors,
  in  float InsideScale,
  out float3 RoundedEdgeTessFactors,
  out float RoundedInsideTessFactor,
  out float UnroundedInsideTessFactor
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*RawEdgeFactors* \[ Pollici\]
</dt> <dd>

Tipo: **float3**

Fattori a tessitore dei bordi, passati nella fase del tessellatore.

</dd> <dt>

*InsideScale* \[ Pollici\]
</dt> <dd>

Tipo: **float**

Fattore di scala applicato ai fattori a squaratura UV calcolati dalla fase a squaratura. L'intervallo consentito per InsideScale è compreso tra 0,0 e 1,0.

</dd> <dt>

*RoundedEdgeTessFactors* \[ Cambio\]
</dt> <dd>

Tipo: **float3**

Fattori a tessellazione degli bordi arrotondati calcolati dalla fase del tessellatore.

</dd> <dt>

*RoundedInsideTessFactor* \[ Cambio\]
</dt> <dd>

Tipo: **float**

Fattori a tessellazione calcolati dalla fase a tessellatore e arrotondati.

</dd> <dt>

*UnroundedInsideTessFactor* \[ Cambio\]
</dt> <dd>

Tipo: **float**

Fattori a tessellazione UV originali, non riepilognati, calcolati dalla fase a tessellazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Genera i fattori a tessellazione corretti per una tri patch, calcolando il fattore a tessellazione interno come la media dei fattori a tessellazione degli bordi, che viene quindi ridimensionata da InsideScale. Il risultato viene quindi arrotondato in base alla modalità di partizionamento, ma i risultati non arrotondati sono disponibili usando il parametro UnroundedInsideTessFactor.

### <a name="minimum-shader-model"></a>Modello di shader minimo

Questa funzione è supportata nei modelli di shader seguenti.



| Modello di shader                                                                | Supportato |
|-----------------------------------------------------------------------------|-----------|
| [Modello shader 5 e](d3d11-graphics-reference-sm5.md) modelli di shader superiori | sì       |



 

Questa funzione è supportata nei tipi di shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        | x    |        |          |       |         |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni intrinseche](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Modello shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




