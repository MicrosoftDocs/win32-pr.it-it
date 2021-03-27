---
title: ProcessIsolineTessFactors (funzione)
description: Genera i fattori a mosaico arrotondati per un oggetto oline.
ms.assetid: 0816b3e0-cb03-4a7a-9732-e84c637b3d48
keywords:
- Funzione ProcessIsolineTessFactors HLSL
topic_type:
- apiref
api_name:
- ProcessIsolineTessFactors
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 10da0e5bf0f2138c57da3fcfe962bc6a88800068
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718820"
---
# <a name="processisolinetessfactors-function"></a>ProcessIsolineTessFactors (funzione)

Genera i fattori a mosaico arrotondati per un oggetto oline.

## <a name="syntax"></a>Sintassi

``` syntax
void ProcessIsolineTessFactors(
  in  float RawDetailFactor,
  in  float RawDensityFactor,
  out float RoundedDetailFactor,
  out float RoundedDensityFactor
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*RawDetailFactor* \[ in\]
</dt> <dd>

Tipo: **float**

Fattore di dettaglio desiderato.

</dd> <dt>

*RawDensityFactor* \[ in\]
</dt> <dd>

Tipo: **float**

Fattore di densità desiderato.

</dd> <dt>

*RoundedDetailFactor* \[ out\]
</dt> <dd>

Tipo: **float**

Il fattore di dettaglio arrotondato è stato fissato a un intervallo che può essere utilizzato da mosaico.

</dd> <dt>

*RoundedDensityFactor* \[ out\]
</dt> <dd>

Tipo: **float**

Il fattore di densità arrotondato fissato a un rangethat può essere utilizzato da mosaico.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

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

 

 




