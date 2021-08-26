---
title: Funzione ProcessQuadTessFactorsAvg
description: Genera i fattori a tessellazione corretti per una patch quad. | Funzione ProcessQuadTessFactorsAvg
ms.assetid: 3af1dad3-1923-45f3-9908-ca403e7f0cfe
keywords:
- Funzione ProcessQuadTessFactorsAvg HLSL
topic_type:
- apiref
api_name:
- ProcessQuadTessFactorsAvg
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 601036c20651da03de15fe4de807ccb6e9d73f5e0b6fc9c1cefc48ccb48b9147
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067791"
---
# <a name="processquadtessfactorsavg-function"></a>Funzione ProcessQuadTessFactorsAvg

Genera i fattori a tessellazione corretti per una patch quad.

## <a name="syntax"></a>Sintassi

``` syntax
void ProcessQuadTessFactorsAvg(
  in  float4 RawEdgeFactors,
  in  float InsideScale,
  out float4 RoundedEdgeTessFactors,
  out float2 RoundedInsideTessFactors,
  out float2 UnroundedInsideTessFactors
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*RawEdgeFactors* \[ Pollici\]
</dt> <dd>

Tipo: **float4**

Fattori a tessitore dei bordi, passati nella fase del tessellatore.

</dd> <dt>

*InsideScale* \[ Pollici\]
</dt> <dd>

Tipo: **float**

Fattore di scala applicato ai fattori a squaratura UV calcolati dalla fase a squaratura. L'intervallo consentito per InsideScale è compreso tra 0,0 e 1,0.

</dd> <dt>

*RoundedEdgeTessFactors* \[ Cambio\]
</dt> <dd>

Tipo: **float4**

Fattori a tessellazione degli bordi arrotondati calcolati dalla fase del tessellatore.

</dd> <dt>

*RoundedInsideTessFactors* \[ Cambio\]
</dt> <dd>

Tipo: **float2**

Fattori a tessellazione arrotondati calcolati dalla fase a tessellatore per i bordi interni.

</dd> <dt>

*UnroundedInsideTessFactors* \[ Cambio\]
</dt> <dd>

Tipo: **float2**

Fattori a tessellazione calcolati dalla fase a tessellatore per i bordi interni.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Genera i fattori a tessellazione corretti per una patch a quad, calcolando i fattori a tessellazione interna come media dei fattori a tessellazione dei bordi. I fattori interni della tesse saranno valori identici determinati dalla media di tutti e quattro i bordi ridimensionati da InsideScale. Il risultato viene quindi arrotondato in base alla modalità di partizionamento, ma i risultati non arrotondati sono disponibili usando il parametro UnroundedInsideTessFactors.

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

 

 




