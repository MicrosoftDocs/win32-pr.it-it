---
title: Funzione ProcessQuadTessFactorsMax
description: Genera i fattori a tessellazione corretti per una patch quad. | Funzione ProcessQuadTessFactorsMax
ms.assetid: a0c91430-db25-49c9-bcc8-d2be1d0e6f6c
keywords:
- Funzione ProcessQuadTessFactorsMax HLSL
topic_type:
- apiref
api_name:
- ProcessQuadTessFactorsMax
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 58cfa3f9e6dd69210da18d672acd2b56ad73e34be9cf2c5d8b179181e636050f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067781"
---
# <a name="processquadtessfactorsmax-function"></a>Funzione ProcessQuadTessFactorsMax

Genera i fattori a tessellazione corretti per una patch quad.

## <a name="syntax"></a>Sintassi

``` syntax
void ProcessQuadTessFactorsMax(
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

Genera i fattori a tessellazione corretti per una patch quad, calcolando i fattori a tessellazione interna come il massimo dei fattori a tessellazione dei bordi. I fattori a tesse interno saranno valori identici determinati dal massimo di tutti e quattro i bordi ridimensionati da InsideScale. Il risultato viene quindi arrotondato in base alla modalità di partizionamento, ma i risultati non arrotondati sono disponibili usando il parametro *UnroundedInsideTessFactors.*

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

 

 




