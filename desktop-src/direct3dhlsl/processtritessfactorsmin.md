---
title: Funzione ProcessTriTessFactorsMin
description: Genera i fattori a tessitori corretti per una tri patch. | Funzione ProcessTriTessFactorsMin
ms.assetid: fa1e19c2-fadf-42d4-9574-834eaf871393
keywords:
- Funzione ProcessTriTessFactorsMin HLSL
topic_type:
- apiref
api_name:
- ProcessTriTessFactorsMin
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 09cb10f8adac68511a5b4bb5b469ab3e4f630aab0b9a58b539100914f0668114
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023741"
---
# <a name="processtritessfactorsmin-function"></a>Funzione ProcessTriTessFactorsMin

Genera i fattori a tessitori corretti per una tri patch.

## <a name="syntax"></a>Sintassi

``` syntax
void ProcessTriTessFactorsMin(
  in  float3 RawEdgeFactors,
  in  float InsideScale,
  out float3 RoundedEdgeTessFactors,
  out float RoundedInsideTessFactors,
  out float UnroundedInsideTessFactors
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

*RoundedInsideTessFactors* \[ Cambio\]
</dt> <dd>

Tipo: **float**

Fattori a tessellazione arrotondati calcolati dalla fase a tessellatore per i bordi interni.

</dd> <dt>

*UnroundedInsideTessFactors* \[ Cambio\]
</dt> <dd>

Tipo: **float**

Fattori a tessellazione calcolati dalla fase a tessellatore per i bordi interni.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Genera i fattori a tessellazione corretti per una tri patch, calcolando il fattore a tessellazione interno come minimo dei fattori a tessellazione dei bordi, che viene quindi ridimensionato da InsideScale. Il risultato viene quindi arrotondato in base alla modalità di partizionamento, ma i risultati non arrotondati sono disponibili usando il parametro UnroundedInsideTessFactor.

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

 

 




