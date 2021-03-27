---
title: Texture2DArray
description: Texture2DArray
ms.assetid: 78ab2feb-4d67-4f6f-bffe-48d55183ce28
keywords:
- HLSL Texture2DArray
topic_type:
- apiref
api_name:
- Texture2DArray
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f1aefa9171ed634934ea5e1306973fe3b22abdfa
ms.sourcegitcommit: 5724b38883e518ac565e1b266defa85ad0941bb2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "104980999"
---
# <a name="texture2darray"></a>Texture2DArray

Il tipo Texture2DArray ([esistente nel modello Shader 4](dx-graphics-hlsl-to-type.md)) più le variabili di risorsa. Questo oggetto texture supporta i metodi seguenti, oltre ai metodi in Shader Model 4.



| Metodo                                                                      | Descrizione                                                                                                                                         |
|-----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Raccogliere**](texture2darray-gather.md)                                      | Restituisce i quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare.                                                                |
| [**GatherRed**](texture2darray-gatherred.md)                                | Restituisce i componenti rossi dei quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare.                                          |
| [**GatherGreen**](texture2darray-gathergreen.md)                            | Restituisce i componenti verdi dei quattro valori Texel che verrebbero usati in un'operazione di filtraggio bilineare.                                        |
| [**GatherBlue**](texture2darray-gatherblue.md)                              | Restituisce i componenti blu dei quattro valori Texel che verrebbero usati in un'operazione di filtraggio bilineare.                                         |
| [**GatherAlpha**](texture2darray-gatheralpha.md)                            | Restituisce i componenti alfa dei quattro valori Texel che verrebbero usati in un'operazione di filtraggio bilineare.                                        |
| [**GatherCmp**](texture2darray-gathercmp.md)                                | Per quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare, restituisce il confronto rispetto a un valore di confronto.                      |
| [**GatherCmpRed**](texture2darray-gathercmpred.md)                          | Per quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare, restituisce un confronto tra il relativo componente rosso e un valore di confronto.   |
| [**GatherCmpGreen**](texture2darray-gathercmpgreen.md)                      | Per quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare, restituisce un confronto tra il relativo componente verde e un valore di confronto. |
| [**GatherCmpBlue**](texture2darray-gathercmpblue.md)                        | Per quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare, restituisce un confronto tra il relativo componente blu e un valore di confronto.  |
| [**GatherCmpAlpha**](texture2darray-gathercmpalpha.md)                      | Per quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare, restituisce un confronto tra il relativo componente alfa e un valore di confronto. |
| [**GetDimensions**](sm5-object-texture2darray-getdimensions.md)             | Ottiene le dimensioni della risorsa.                                                                                                                       |
| [**Caricamento**](texture2darray-load.md)                                          | Legge i dati della trama.                                                                                                                                 |
| [**MIPS. Operatore\[\]\[\]**](sm5-object-texture2darray-mipsoperatorindex.md) | Ottiene una variabile di risorsa di sola lettura.                                                                                                                 |
| [**Operatore\[\]**](sm5-object-texture2darray-operatorindex.md)              | Ottiene una variabile di risorsa di sola lettura.                                                                                                                 |
| [**Esempio**](texture2darray-sample.md)                                      | Campiona una trama.                                                                                                                                  |
| [**SampleBias**](texture2darray-samplebias.md)                              | Esegue il campionamento di una trama, dopo aver applicato il valore di distorsione al livello mipmap.                                                                               |
| [**SampleCmp**](texture2darray-samplecmp.md)                                | Campiona una trama, usando un valore di confronto per rifiutare gli esempi.                                                                                      |
| [**SampleCmpLevelZero**](texture2darray-samplecmplevelzero.md)              | Esegue il campionamento di una trama (solo livello mipmap 0), usando un valore di confronto per rifiutare gli esempi.                                                                |
| [**SampleGrad**](texture2darray-samplegrad.md)                              | Campiona una trama utilizzando una sfumatura per influenzare il modo in cui viene calcolata la posizione di esempio.                                                          |
| [**SampleLevel**](texture2darray-samplelevel.md)                            | Esegue il campionamento di una trama sul livello mipmap specificato.                                                                                                    |



 

## <a name="minimum-shader-model"></a>Modello Shader minimo

Questo oggetto è supportato nei modelli shader seguenti.



| Modello di shader                                                                | Supportato |
|-----------------------------------------------------------------------------|-----------|
| [Shader Model 5](d3d11-graphics-reference-sm5.md) e versioni successive shader Models | sì       |



 

Questo oggetto è supportato per i tipi di shader seguenti:



| Vertice | Hull | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetti Shader Model 5](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




