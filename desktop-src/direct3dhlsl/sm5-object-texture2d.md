---
title: Texture2D
description: Texture2D
ms.assetid: e4f9cfd8-65e6-4375-8f87-736bca32cad4
keywords:
- Texture2D HLSL
topic_type:
- apiref
api_name:
- Texture2D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ad13843dd74ab7cc188c3ab37d76df978f2a5fbd4bc6c292cfddfdf7c5841b33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118789377"
---
# <a name="texture2d"></a>Texture2D

Tipo Texture2D ([così come esiste nel modello shader 4)](dx-graphics-hlsl-to-type.md)più variabili di risorsa. Questo oggetto trama supporta i metodi seguenti oltre ai metodi nel modello shader 4.



| Metodo                                                                 | Descrizione                                                                                                                                        |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Raccogliere**](texture2d-gather.md)                                      | Restituisce i quattro valori texel che verrebbero usati in un'operazione di filtro bi lineare.                                                                |
| [**GatherRed**](texture2d-gatherred.md)                                | Restituisce i componenti rossi dei quattro valori texel che verrebbero usati in un'operazione di filtro bi-lineare.                                          |
| [**GatherGreen**](texture2d-gathergreen.md)                            | Restituisce i componenti verdi dei quattro valori texel che verrebbero usati in un'operazione di filtro bi-lineare.                                        |
| [**GatherBlue**](texture2d-gatherblue.md)                              | Restituisce i componenti blu dei quattro valori texel che verrebbero usati in un'operazione di filtro bi-lineare.                                         |
| [**GatherAlpha**](texture2d-gatheralpha.md)                            | Restituisce i componenti alfa dei quattro valori texel che verrebbero usati in un'operazione di filtro bi-lineare.                                        |
| [**GatherCmp**](texture2d-gathercmp.md)                                | Per quattro valori texel che verrebbero usati in un'operazione di filtro bi lineare, restituisce il confronto con un valore di confronto.                      |
| [**GatherCmpRed**](texture2d-gathercmpred.md)                          | Per quattro valori texel che verrebbero usati in un'operazione di filtro bi lineare, restituisce un confronto tra il relativo componente rosso e un valore di confronto.   |
| [**GatherCmpGreen**](texture2d-gathercmpgreen.md)                      | Per quattro valori di texel che verrebbero usati in un'operazione di filtro bi lineare, restituisce un confronto tra il componente verde e un valore di confronto. |
| [**GatherCmpBlue**](texture2d-gathercmpblue.md)                        | Per quattro valori texel che verrebbero usati in un'operazione di filtro bi lineare, restituisce un confronto tra il componente blu e un valore di confronto.  |
| [**GatherCmpAlpha**](texture2d-gathercmpalpha.md)                      | Per quattro valori texel che verrebbero usati in un'operazione di filtro bi lineare, restituisce un confronto del relativo componente alfa con un valore di confronto. |
| [**GetDimensions**](sm5-object-texture2d-getdimensions.md)             | Ottiene le dimensioni della risorsa.                                                                                                                       |
| [**Caricamento**](texture2d-load.md)                                          | Legge i dati della trama.                                                                                                                                 |
| [**Mips. Operatore\[\]\[\]**](sm5-object-texture2d-mipsoperatorindex.md) | Ottiene una variabile di risorsa di sola lettura.                                                                                                                 |
| [**Operatore\[\]**](sm5-object-texture2d-operatorindex.md)              | Ottiene una variabile di risorsa di sola lettura.                                                                                                                 |
| [**Esempio**](texture-sample-overload.md)                               | Campio una trama.                                                                                                                                  |
| [**SampleBias**](texture2d-samplebias.md)                              | Campita una trama, dopo aver applicato il valore di distorsione al livello mipmap.                                                                               |
| [**SampleCmp**](texture2d-samplecmp.md)                                | Campio una trama, usando un valore di confronto per rifiutare i campioni.                                                                                      |
| [**SampleCmpLevelZero**](texture2d-samplecmplevelzero.md)              | Campio una trama (solo livello mipmap 0), usando un valore di confronto per rifiutare i campioni.                                                                |
| [**SampleGrad**](texture2d-samplegrad.md)                              | Campionare una trama usando una sfumatura per influenzare il modo in cui viene calcolata la posizione del campione.                                                          |
| [**SampleLevel**](texture2d-samplelevel.md)                            | Campita una trama a livello di mipmap specificato.                                                                                                    |



 

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

 

 




