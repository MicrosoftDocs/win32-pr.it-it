---
title: ProcessQuadTessFactorsAvg (funzione)
description: Genera i fattori a mosaico corretti per una patch quad. | ProcessQuadTessFactorsAvg (funzione)
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
ms.openlocfilehash: 36a50dd971161f3e03514947db447774da5b6a62
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995653"
---
# <a name="processquadtessfactorsavg-function"></a>ProcessQuadTessFactorsAvg (funzione)

Genera i fattori a mosaico corretti per una patch quad.

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

*RawEdgeFactors* \[ in\]
</dt> <dd>

Tipo: **float4**

Fattori a mosaico perimetrale passati alla fase mosaico.

</dd> <dt>

*InsideScale* \[ in\]
</dt> <dd>

Tipo: **float**

Fattore di scala applicato ai fattori a mosaico UV calcolati dalla fase a mosaico. L'intervallo consentito per InsideScale è compreso tra 0,0 e 1,0.

</dd> <dt>

*RoundedEdgeTessFactors* \[ out\]
</dt> <dd>

Tipo: **float4**

Fattori arrotondati a mosaico perimetrale calcolati dalla fase mosaico.

</dd> <dt>

*RoundedInsideTessFactors* \[ out\]
</dt> <dd>

Tipo: **float2**

Fattori a mosaico arrotondati calcolati dalla fase mosaico per i bordi interni.

</dd> <dt>

*UnroundedInsideTessFactors* \[ out\]
</dt> <dd>

Tipo: **float2**

Fattori a mosaico calcolati dalla fase mosaico per i bordi interni.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Genera i fattori a mosaico corretti per una patch quad, calcolando i fattori interni a mosaico come media dei fattori di mosaico perimetrale. I fattori di Tess interni saranno valori identici determinati dalla media di tutti e quattro i bordi ridimensionati in base a InsideScale. Il risultato viene quindi arrotondato in base alla modalità di partizionamento, ma i risultati non arrotondati sono disponibili tramite il parametro UnroundedInsideTessFactors.

### <a name="minimum-shader-model"></a>Modello Shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                                                | Supportato |
|-----------------------------------------------------------------------------|-----------|
| [Shader Model 5](d3d11-graphics-reference-sm5.md) e versioni successive shader Models | sì       |



 

Questa funzione è supportata nei tipi di shader seguenti:



| Vertice | Hull | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        | x    |        |          |       |         |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni intrinseche](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Modello Shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




