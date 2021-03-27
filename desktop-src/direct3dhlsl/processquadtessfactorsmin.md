---
title: ProcessQuadTessFactorsMin (funzione)
description: Genera i fattori a mosaico corretti per una patch quad. | ProcessQuadTessFactorsMin (funzione)
ms.assetid: 19cbd807-e379-4ee3-beba-55e35e4bcbcf
keywords:
- Funzione ProcessQuadTessFactorsMin HLSL
topic_type:
- apiref
api_name:
- ProcessQuadTessFactorsMin
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 57eff10af1bf53b2a659cde6b7e036b5391c3ea6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981154"
---
# <a name="processquadtessfactorsmin-function"></a>ProcessQuadTessFactorsMin (funzione)

Genera i fattori a mosaico corretti per una patch quad.

## <a name="syntax"></a>Sintassi

``` syntax
void ProcessQuadTessFactorsMin(
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

Genera i fattori a mosaico corretti per una patch quad, calcolando i fattori interni a mosaico come minimo dei fattori di mosaico perimetrale. I fattori interni di Tess saranno valori identici determinati dal minimo di tutti e quattro i bordi ridimensionati da InsideScale. Il risultato viene quindi arrotondato in base alla modalità di partizionamento, ma i risultati non arrotondati sono disponibili tramite il parametro UnroundedInsideTessFactors.

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

 

 




