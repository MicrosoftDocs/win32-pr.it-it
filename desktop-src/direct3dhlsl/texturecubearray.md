---
title: Oggetto TextureCubeArray
description: Tipo TextureCubeArray (così come esiste nel modello shader 4) più variabili di risorsa. Questo oggetto trama supporta questi metodi oltre ai metodi in Shader Model 4.
ms.assetid: 62AAF0F9-D552-4FFA-B681-749D6DC205BD
keywords:
- Oggetto TextureCubeArray HLSL
- Oggetto TextureCubeArray HLSL , descritto
topic_type:
- apiref
api_name:
- TextureCubeArray
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a0b5687e26ebb8a80dbd75e5849ad95de29dacec90c64e660e59dce71c796b0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118786169"
---
# <a name="texturecubearray-object"></a>Oggetto TextureCubeArray

**Tipo TextureCubeArray** ([così come esiste nel modello shader 4](dx-graphics-hlsl-to-type.md)) più variabili di risorsa. Questo oggetto trama supporta questi metodi oltre ai metodi in Shader Model 4.

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'oggetto TextureCubeArray** dispone di questi metodi.



| Metodo                                                           | Descrizione                                                                                                                                              |
|:-----------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Raccogliere**](texturecubearray-gather.md)                         | Restituisce i quattro valori texel che verrebbero usati in un'operazione di filtro bi-lineare.<br/>                                                                |
| [**GatherAlpha**](texturecubearray-gatheralpha.md)               | Restituisce i componenti alfa dei quattro valori texel che verrebbero usati in un'operazione di filtro bi-lineare.<br/>                                        |
| [**GatherBlue**](texturecubearray-gatherblue.md)                 | Restituisce i componenti blu dei quattro valori texel che verrebbero usati in un'operazione di filtro bi-lineare.<br/>                                         |
| [**GatherCmp**](texturecubearray-gathercmp.md)                   | Per quattro valori texel che verrebbero usati in un'operazione di filtro bi-lineare, restituisce il confronto con un valore di confronto.<br/>                      |
| [**GatherCmpAlpha**](texturecubearray-gathercmpalpha.md)         | Per quattro valori texel che verrebbero usati in un'operazione di filtro bi-lineare, restituisce un confronto tra il componente alfa e un valore di confronto.<br/> |
| [**GatherCmpBlue**](texturecubearray-gathercmpblue.md)           | Per quattro valori texel che verrebbero usati in un'operazione di filtro bi-lineare, restituisce un confronto tra il componente blu e un valore di confronto.<br/>  |
| [**GatherCmpGreen**](texturecubearray-gathercmpgreen.md)         | Per quattro valori texel che verrebbero usati in un'operazione di filtro bi-lineare, restituisce un confronto tra il componente verde e un valore di confronto.<br/> |
| [**GatherCmpRed**](texturecubearray-gathercmpred.md)             | Per quattro valori texel che verrebbero usati in un'operazione di filtro bi-lineare, restituisce un confronto tra il componente rosso e un valore di confronto.<br/>   |
| [**GatherGreen**](texturecubearray-gathergreen.md)               | Restituisce i componenti verdi dei quattro valori texel che verrebbero usati in un'operazione di filtro bi-lineare.<br/>                                        |
| [**GatherRed**](texturecubearray-gatherred.md)                   | Restituisce i componenti rossi dei quattro valori texel che verrebbero usati in un'operazione di filtro bi-lineare.<br/>                                          |
| [**Esempio**](texturecubearray-sample.md)                         | Esempi di una trama.<br/>                                                                                                                                  |
| [**SampleBias**](texturecubearray-samplebias.md)                 | Campionamento di una trama, dopo l'applicazione del valore di distorsione al livello mipmap.<br/>                                                                               |
| [**SampleCmp**](texturecubearray-samplecmp.md)                   | Esempi di una trama, usando un valore di confronto per rifiutare gli esempi.<br/>                                                                                      |
| [**SampleCmpLevelZero**](texturecubearray-samplecmplevelzero.md) | Esempi di una trama (solo livello mipmap 0), usando un valore di confronto per rifiutare i campioni.<br/>                                                                |
| [**SampleGrad**](texturecubearray-samplegrad.md)                 | Campionare una trama usando una sfumatura per influenzare il modo in cui viene calcolata la posizione del campione.<br/>                                                          |
| [**SampleLevel**](texturecubearray-samplelevel.md)               | Campionamento di una trama al livello mipmap specificato.<br/>                                                                                                    |



 

## <a name="remarks"></a>Commenti

### <a name="minimum-shader-model"></a>Modello shader minimo

Questo oggetto è supportato nei modelli shader seguenti.



| Modello di shader                                                                | Supportato |
|-----------------------------------------------------------------------------|-----------|
| [Modelli shader modello 5](d3d11-graphics-reference-sm5.md) e versioni successive | sì       |



 

Questo oggetto è supportato per i tipi di shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetti modello shader 5](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 





