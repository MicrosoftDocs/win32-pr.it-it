---
title: Texture2D
description: Texture2D
ms.assetid: e4f9cfd8-65e6-4375-8f87-736bca32cad4
keywords:
- HLSL Texture2D
topic_type:
- apiref
api_name:
- Texture2D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f0c9b73d66f1c5a38b077b241df8e5859b706e2f
ms.sourcegitcommit: 5724b38883e518ac565e1b266defa85ad0941bb2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "104981015"
---
# <a name="texture2d"></a>Texture2D

Il tipo Texture2D ([esistente nel modello Shader 4](dx-graphics-hlsl-to-type.md)) più le variabili di risorsa. Questo oggetto texture supporta i metodi seguenti, oltre ai metodi in Shader Model 4.



| Metodo                                                                 | Descrizione                                                                                                                                        |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Raccogliere**](texture2d-gather.md)                                      | Restituisce i quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare.                                                                |
| [**GatherRed**](texture2d-gatherred.md)                                | Restituisce i componenti rossi dei quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare.                                          |
| [**GatherGreen**](texture2d-gathergreen.md)                            | Restituisce i componenti verdi dei quattro valori Texel che verrebbero usati in un'operazione di filtraggio bilineare.                                        |
| [**GatherBlue**](texture2d-gatherblue.md)                              | Restituisce i componenti blu dei quattro valori Texel che verrebbero usati in un'operazione di filtraggio bilineare.                                         |
| [**GatherAlpha**](texture2d-gatheralpha.md)                            | Restituisce i componenti alfa dei quattro valori Texel che verrebbero usati in un'operazione di filtraggio bilineare.                                        |
| [**GatherCmp**](texture2d-gathercmp.md)                                | Per quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare, restituisce il confronto rispetto a un valore di confronto.                      |
| [**GatherCmpRed**](texture2d-gathercmpred.md)                          | Per quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare, restituisce un confronto tra il relativo componente rosso e un valore di confronto.   |
| [**GatherCmpGreen**](texture2d-gathercmpgreen.md)                      | Per quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare, restituisce un confronto tra il relativo componente verde e un valore di confronto. |
| [**GatherCmpBlue**](texture2d-gathercmpblue.md)                        | Per quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare, restituisce un confronto tra il relativo componente blu e un valore di confronto.  |
| [**GatherCmpAlpha**](texture2d-gathercmpalpha.md)                      | Per quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare, restituisce un confronto tra il relativo componente alfa e un valore di confronto. |
| [**GetDimensions**](sm5-object-texture2d-getdimensions.md)             | Ottiene le dimensioni della risorsa.                                                                                                                       |
| [**Caricamento**](texture2d-load.md)                                          | Legge i dati della trama.                                                                                                                                 |
| [**MIPS. Operatore\[\]\[\]**](sm5-object-texture2d-mipsoperatorindex.md) | Ottiene una variabile di risorsa di sola lettura.                                                                                                                 |
| [**Operatore\[\]**](sm5-object-texture2d-operatorindex.md)              | Ottiene una variabile di risorsa di sola lettura.                                                                                                                 |
| [**Esempio**](texture-sample-overload.md)                               | Campiona una trama.                                                                                                                                  |
| [**SampleBias**](texture2d-samplebias.md)                              | Esegue il campionamento di una trama, dopo aver applicato il valore di distorsione al livello mipmap.                                                                               |
| [**SampleCmp**](texture2d-samplecmp.md)                                | Campiona una trama, usando un valore di confronto per rifiutare gli esempi.                                                                                      |
| [**SampleCmpLevelZero**](texture2d-samplecmplevelzero.md)              | Esegue il campionamento di una trama (solo livello mipmap 0), usando un valore di confronto per rifiutare gli esempi.                                                                |
| [**SampleGrad**](texture2d-samplegrad.md)                              | Campiona una trama utilizzando una sfumatura per influenzare il modo in cui viene calcolata la posizione di esempio.                                                          |
| [**SampleLevel**](texture2d-samplelevel.md)                            | Esegue il campionamento di una trama sul livello mipmap specificato.                                                                                                    |



 

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

 

 




