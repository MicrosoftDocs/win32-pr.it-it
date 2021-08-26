---
title: Funzione Process2DQuadTessFactorsMin
description: Genera i fattori a tessellazione corretti per una patch quad. | Funzione Process2DQuadTessFactorsMin
ms.assetid: 45adf78a-9386-4460-97df-59d7739a1eee
keywords:
- Funzione Process2DQuadTessFactorsMin HLSL
topic_type:
- apiref
api_name:
- Process2DQuadTessFactorsMin
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 77f62ff1b55b9c0c36a70bd64f2b0d5ad95be747d5fd11cae33e82eb896d21d2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067901"
---
# <a name="process2dquadtessfactorsmin-function"></a>Funzione Process2DQuadTessFactorsMin

Genera i fattori a tessellazione corretti per una patch quad.

## <a name="syntax"></a>Sintassi

``` syntax
void Process2DQuadTessFactorsMin(
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

Fattori a tessitore dei bordi, passati nella fase del tessellatore.

</dd> <dt>

*InsideScale* \[ Pollici\]
</dt> <dd>

Tipo: **float2**

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

Genera i fattori a tessellazione corretti per una patch quad, calcolando i fattori a tessellazione interna come minimo dei fattori a tessellazione dei bordi. L'utente e V all'interno dei fattori a tessellazione vengono calcolati in modo indipendente usando i valori minimi dei lati opposti del dominio, quindi vengono ridimensionati da InsideScale. Il risultato viene quindi arrotondato in base alla modalità di partizionamento, ma i risultati non arrotondati sono disponibili usando il parametro UnroundedInsideTessFactors.

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

 

 




