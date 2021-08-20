---
title: Funzione Process2DQuadTessFactorsAvg
description: Genera i fattori a tessellazione corretti per una patch quad. | Funzione Process2DQuadTessFactorsAvg
ms.assetid: 7f96f634-0ad5-4037-a08e-b0b99b89cd91
keywords:
- Funzione Process2DQuadTessFactorsAvg HLSL
topic_type:
- apiref
api_name:
- Process2DQuadTessFactorsAvg
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 838bdb30e6e91a7bfd4aa5e643d2f731642b81acd8dd3a17d583f1383732e10f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117906385"
---
# <a name="process2dquadtessfactorsavg-function"></a>Funzione Process2DQuadTessFactorsAvg

Genera i fattori a tessellazione corretti per una patch quad.

## <a name="syntax"></a>Sintassi

``` syntax
void Process2DQuadTessFactorsAvg(
  in  float4 RawEdgeFactors,
  in  float2 InsideScale,
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

Fattori a tessellazione del bordo, passati nella fase a tessellatore.

</dd> <dt>

*InsideScale* \[ Pollici\]
</dt> <dd>

Tipo: **float2**

Fattore di scala applicato ai fattori a tessellazione UV calcolati dalla fase a tessellazione. L'intervallo consentito per InsideScale è compreso tra 0,0 e 1,0.

</dd> <dt>

*RoundedEdgeTessFactors* \[ Cambio\]
</dt> <dd>

Tipo: **float4**

Fattori arrotondati di a tessellazione dei bordi calcolati dalla fase a tessellatore.

</dd> <dt>

*RoundedInsideTessFactors* \[ Cambio\]
</dt> <dd>

Tipo: **float2**

Fattori a tassellamento arrotondati calcolati dalla fase a tessellatore per i bordi interni.

</dd> <dt>

*UnroundedInsideTessFactors* \[ Cambio\]
</dt> <dd>

Tipo: **float2**

Fattori a tassellamento calcolati dalla fase a tessellatore per i bordi interni.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Genera i fattori a tessellazione corretti per una patch quad, calcolando i fattori a tessellazione interna come media dei fattori a tessellazione del bordo. I fattori di tessellazione di you e V all'interno vengono calcolati in modo indipendente usando la media dei lati opposti del dominio, quindi vengono ridimensionati da InsideScale. Il risultato viene quindi arrotondato in base alla modalità di partizionamento, ma i risultati non arrotondati sono disponibili usando il parametro UnroundedInsideTessFactors.

### <a name="minimum-shader-model"></a>Modello di shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                                                | Supportato |
|-----------------------------------------------------------------------------|-----------|
| [Modello shader 5 e](d3d11-graphics-reference-sm5.md) modelli shader superiori | sì       |



 

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

 

 




