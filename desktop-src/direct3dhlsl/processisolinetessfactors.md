---
title: Funzione ProcessIsolineTessFactors
description: Genera i fattori a trama arrotondata per un'isolinea.
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
ms.openlocfilehash: 34c6f4d579ee7fbaee9416d7a607e3856a7793021cca7149723d3d6e5a2b4a49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986291"
---
# <a name="processisolinetessfactors-function"></a>Funzione ProcessIsolineTessFactors

Genera i fattori a trama arrotondata per un'isolinea.

## <a name="syntax"></a>Sintassi

``` syntax
void ProcessIsolineTessFactors(
  in  float RawDetailFactor,
  in  float RawDensityFactor,
  out float RoundedDetailFactor,
  out float RoundedDensityFactor
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*RawDetailFactor* \[ Pollici\]
</dt> <dd>

Tipo: **float**

Fattore di dettaglio desiderato.

</dd> <dt>

*RawDensityFactor* \[ Pollici\]
</dt> <dd>

Tipo: **float**

Fattore di densità desiderato.

</dd> <dt>

*RoundedDetailFactor* \[ Cambio\]
</dt> <dd>

Tipo: **float**

Fattore di dettaglio arrotondato a un intervallo che può essere usato dal tessellatore.

</dd> <dt>

*RoundedDensityFactor* \[ Cambio\]
</dt> <dd>

Tipo: **float**

Fattore di densità arrotondato a un intervallo che può essere usato dal tessellatore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

### <a name="minimum-shader-model"></a>Modello shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                                                | Supportato |
|-----------------------------------------------------------------------------|-----------|
| [Modelli shader modello 5](d3d11-graphics-reference-sm5.md) e versioni successive | sì       |



 

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

 

 




