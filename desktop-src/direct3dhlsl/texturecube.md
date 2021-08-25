---
title: Oggetto TextureCube
description: Tipo TextureCube (così come esiste nel modello shader 4) più variabili di risorsa. Questo oggetto trama supporta questi metodi oltre ai metodi nel modello shader 4.
ms.assetid: BC96D7BB-992E-48CC-A774-E211E1BB1720
keywords:
- Oggetto TextureCube HLSL
- Oggetto TextureCube HLSL, descritto
topic_type:
- apiref
api_name:
- TextureCube
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4d9cab13ec3ca86e17586e2fea27e7e60cf14a552abfdd405d3ea3da8c8195a3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119892471"
---
# <a name="texturecube-object"></a>Oggetto TextureCube

**Tipo TextureCube** ([così come esiste nel modello shader 4)](dx-graphics-hlsl-to-type.md)e variabili di risorsa. Questo oggetto trama supporta questi metodi oltre ai metodi nel modello shader 4.

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'oggetto TextureCube** dispone di questi metodi.



| Metodo                                                      | Descrizione                                                                                                                                             |
|:------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Raccogliere**](texturecube-gather.md)                         | Restituisce i quattro valori texel che verrebbero usati in un'operazione di filtro bi lineare.<br/>                                                                |
| [**GatherAlpha**](texturecube-gatheralpha.md)               | Restituisce i componenti alfa dei quattro valori texel che verrebbero usati in un'operazione di filtro bi-lineare.<br/>                                        |
| [**GatherBlue**](texturecube-gatherblue.md)                 | Restituisce i componenti blu dei quattro valori texel che verrebbero usati in un'operazione di filtro bi-lineare.<br/>                                         |
| [**GatherCmp**](texturecube-gathercmp.md)                   | Per quattro valori texel che verrebbero usati in un'operazione di filtro bi lineare, restituisce il confronto con un valore di confronto.<br/>                      |
| [**GatherCmpAlpha**](texturecube-gathercmpalpha.md)         | Per quattro valori texel che verrebbero usati in un'operazione di filtro bi lineare, restituisce un confronto del relativo componente alfa con un valore di confronto.<br/> |
| [**GatherCmpBlue**](texturecube-gathercmpblue.md)           | Per quattro valori texel che verrebbero usati in un'operazione di filtro bi lineare, restituisce un confronto tra il componente blu e un valore di confronto.<br/>  |
| [**GatherCmpGreen**](texturecube-gathercmpgreen.md)         | Per quattro valori di texel che verrebbero usati in un'operazione di filtro bi lineare, restituisce un confronto tra il componente verde e un valore di confronto.<br/> |
| [**GatherCmpRed**](texturecube-gathercmpred.md)             | Per quattro valori texel che verrebbero usati in un'operazione di filtro bi lineare, restituisce un confronto tra il relativo componente rosso e un valore di confronto.<br/>   |
| [**GatherGreen**](texturecube-gathergreen.md)               | Restituisce i componenti verdi dei quattro valori texel che verrebbero usati in un'operazione di filtro bi-lineare.<br/>                                        |
| [**GatherRed**](texturecube-gatherred.md)                   | Restituisce i componenti rossi dei quattro valori texel che verrebbero usati in un'operazione di filtro bi-lineare.<br/>                                          |
| [**Esempio**](texturecube-sample.md)                         | Campio una trama.<br/>                                                                                                                                  |
| [**SampleBias**](texturecube-samplebias.md)                 | Campita una trama, dopo aver applicato il valore di distorsione al livello mipmap.<br/>                                                                               |
| [**SampleCmp**](texturecube-samplecmp.md)                   | Campio una trama, usando un valore di confronto per rifiutare i campioni.<br/>                                                                                      |
| [**SampleCmpLevelZero**](texturecube-samplecmplevelzero.md) | Campio una trama (solo livello mipmap 0), usando un valore di confronto per rifiutare i campioni.<br/>                                                                |
| [**SampleGrad**](texturecube-samplegrad.md)                 | Campionare una trama usando una sfumatura per influenzare il modo in cui viene calcolata la posizione del campione.<br/>                                                          |
| [**SampleLevel**](texturecube-samplelevel.md)               | Campita una trama a livello di mipmap specificato.<br/>                                                                                                    |



 

## <a name="remarks"></a>Commenti

### <a name="minimum-shader-model"></a>Modello di shader minimo

Questo oggetto è supportato nei modelli di shader seguenti.



| Modello di shader                                                                | Supportato |
|-----------------------------------------------------------------------------|-----------|
| [Modello shader 5 e](d3d11-graphics-reference-sm5.md) modelli di shader superiori | sì       |



 

Questo oggetto è supportato per i tipi di shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetti modello shader 5](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 





