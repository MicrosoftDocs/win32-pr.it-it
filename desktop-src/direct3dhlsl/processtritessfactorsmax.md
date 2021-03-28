---
title: ProcessTriTessFactorsMax (funzione)
description: Genera i fattori a mosaico corretti per una patch Tri. | ProcessTriTessFactorsMax (funzione)
ms.assetid: a24cc1a8-5e6e-4963-b36b-e2265475580e
keywords:
- Funzione ProcessTriTessFactorsMax HLSL
topic_type:
- apiref
api_name:
- ProcessTriTessFactorsMax
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b5c17fe1dd9f3457a4104178e61af3589ba9f72d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104530654"
---
# <a name="processtritessfactorsmax-function"></a>ProcessTriTessFactorsMax (funzione)

Genera i fattori a mosaico corretti per una patch Tri.

## <a name="syntax"></a>Sintassi

``` syntax
void ProcessTriTessFactorsMax(
  in  float3 RawEdgeFactors,
  in  float InsideScale,
  out float3 RoundedEdgeTessFactors,
  out float RoundedInsideTessFactor,
  out float UnroundedInsideTessFactor
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*RawEdgeFactors* \[ in\]
</dt> <dd>

Tipo: **float3**

Fattori a mosaico perimetrale passati alla fase mosaico.

</dd> <dt>

*InsideScale* \[ in\]
</dt> <dd>

Tipo: **float**

Fattore di scala applicato ai fattori a mosaico UV calcolati dalla fase a mosaico. L'intervallo consentito per InsideScale è compreso tra 0,0 e 1,0.

</dd> <dt>

*RoundedEdgeTessFactors* \[ out\]
</dt> <dd>

Tipo: **float3**

Fattori arrotondati a mosaico perimetrale calcolati dalla fase mosaico.

</dd> <dt>

*RoundedInsideTessFactor* \[ out\]
</dt> <dd>

Tipo: **float**

Fattori a mosaico calcolati dalla fase mosaico e arrotondati.

</dd> <dt>

*UnroundedInsideTessFactor* \[ out\]
</dt> <dd>

Tipo: **float**

Fattori a mosaico UV originali, non arrotondati calcolati dalla fase di suddivisione a mosaico.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Genera i fattori a mosaico corretti per una patch Tri, calcolando il fattore a mosaico interno come massimo dei fattori di mosaico perimetrale, che viene quindi ridimensionato da InsideScale. Il risultato viene quindi arrotondato in base alla modalità di partizionamento, ma i risultati non arrotondati sono disponibili tramite il parametro UnroundedInsideTessFactor.

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

 

 




