---
title: Texture2DArray
description: Texture2DArray
ms.assetid: 78ab2feb-4d67-4f6f-bffe-48d55183ce28
keywords:
- Texture2DArray HLSL
topic_type:
- apiref
api_name:
- Texture2DArray
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: aab6e5c0a500a9f34cbd4e418a35e96687650f3df863e1fe77576c66ade718e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023401"
---
# <a name="texture2darray"></a>Texture2DArray

Tipo Texture2DArray ([così come esiste nel modello shader 4)](dx-graphics-hlsl-to-type.md)più variabili di risorsa. Questo oggetto trama supporta i metodi seguenti oltre ai metodi nel modello shader 4.



| Metodo                                                                      | Descrizione                                                                                                                                         |
|-----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Raccogliere**](texture2darray-gather.md)                                      | Restituisce i quattro valori texel che verrebbero usati in un'operazione di filtro bi lineare.                                                                |
| [**GatherRed**](texture2darray-gatherred.md)                                | Restituisce i componenti rossi dei quattro valori texel che verrebbero usati in un'operazione di filtro bi-lineare.                                          |
| [**GatherGreen**](texture2darray-gathergreen.md)                            | Restituisce i componenti verdi dei quattro valori texel che verrebbero usati in un'operazione di filtro bi-lineare.                                        |
| [**GatherBlue**](texture2darray-gatherblue.md)                              | Restituisce i componenti blu dei quattro valori texel che verrebbero usati in un'operazione di filtro bi-lineare.                                         |
| [**GatherAlpha**](texture2darray-gatheralpha.md)                            | Restituisce i componenti alfa dei quattro valori texel che verrebbero usati in un'operazione di filtro bi-lineare.                                        |
| [**GatherCmp**](texture2darray-gathercmp.md)                                | Per quattro valori texel che verrebbero usati in un'operazione di filtro bi lineare, restituisce il confronto con un valore di confronto.                      |
| [**GatherCmpRed**](texture2darray-gathercmpred.md)                          | Per quattro valori texel che verrebbero usati in un'operazione di filtro bi lineare, restituisce un confronto tra il relativo componente rosso e un valore di confronto.   |
| [**GatherCmpGreen**](texture2darray-gathercmpgreen.md)                      | Per quattro valori di texel che verrebbero usati in un'operazione di filtro bi lineare, restituisce un confronto tra il componente verde e un valore di confronto. |
| [**GatherCmpBlue**](texture2darray-gathercmpblue.md)                        | Per quattro valori texel che verrebbero usati in un'operazione di filtro bi lineare, restituisce un confronto tra il componente blu e un valore di confronto.  |
| [**GatherCmpAlpha**](texture2darray-gathercmpalpha.md)                      | Per quattro valori texel che verrebbero usati in un'operazione di filtro bi lineare, restituisce un confronto del relativo componente alfa con un valore di confronto. |
| [**GetDimensions**](sm5-object-texture2darray-getdimensions.md)             | Ottiene le dimensioni della risorsa.                                                                                                                       |
| [**Caricamento**](texture2darray-load.md)                                          | Legge i dati della trama.                                                                                                                                 |
| [**Mips. Operatore\[\]\[\]**](sm5-object-texture2darray-mipsoperatorindex.md) | Ottiene una variabile di risorsa di sola lettura.                                                                                                                 |
| [**Operatore\[\]**](sm5-object-texture2darray-operatorindex.md)              | Ottiene una variabile di risorsa di sola lettura.                                                                                                                 |
| [**Esempio**](texture2darray-sample.md)                                      | Campio una trama.                                                                                                                                  |
| [**SampleBias**](texture2darray-samplebias.md)                              | Campita una trama, dopo aver applicato il valore di distorsione al livello mipmap.                                                                               |
| [**SampleCmp**](texture2darray-samplecmp.md)                                | Campio una trama, usando un valore di confronto per rifiutare i campioni.                                                                                      |
| [**SampleCmpLevelZero**](texture2darray-samplecmplevelzero.md)              | Campio una trama (solo livello mipmap 0), usando un valore di confronto per rifiutare i campioni.                                                                |
| [**SampleGrad**](texture2darray-samplegrad.md)                              | Campionare una trama usando una sfumatura per influenzare il modo in cui viene calcolata la posizione del campione.                                                          |
| [**SampleLevel**](texture2darray-samplelevel.md)                            | Campita una trama a livello di mipmap specificato.                                                                                                    |



 

## <a name="minimum-shader-model"></a>Modello di shader minimo

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

 

 




