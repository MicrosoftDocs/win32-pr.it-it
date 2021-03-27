---
title: Oggetto TextureCube
description: Il tipo TextureCube (esistente nel modello Shader 4) più le variabili di risorsa. Questo oggetto texture supporta questi metodi, oltre ai metodi in Shader Model 4.
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
ms.openlocfilehash: 939c79895ae1c24665fc70d6b6cf2ced19854e2b
ms.sourcegitcommit: 5724b38883e518ac565e1b266defa85ad0941bb2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "104132138"
---
# <a name="texturecube-object"></a>Oggetto TextureCube

Il tipo **TextureCube** ([esistente nel modello Shader 4](dx-graphics-hlsl-to-type.md)) più le variabili di risorsa. Questo oggetto texture supporta questi metodi, oltre ai metodi in Shader Model 4.

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'oggetto **TextureCube** dispone di questi metodi.



| Metodo                                                      | Descrizione                                                                                                                                             |
|:------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Raccogliere**](texturecube-gather.md)                         | Restituisce i quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare.<br/>                                                                |
| [**GatherAlpha**](texturecube-gatheralpha.md)               | Restituisce i componenti alfa dei quattro valori Texel che verrebbero usati in un'operazione di filtraggio bilineare.<br/>                                        |
| [**GatherBlue**](texturecube-gatherblue.md)                 | Restituisce i componenti blu dei quattro valori Texel che verrebbero usati in un'operazione di filtraggio bilineare.<br/>                                         |
| [**GatherCmp**](texturecube-gathercmp.md)                   | Per quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare, restituisce il confronto rispetto a un valore di confronto.<br/>                      |
| [**GatherCmpAlpha**](texturecube-gathercmpalpha.md)         | Per quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare, restituisce un confronto tra il relativo componente alfa e un valore di confronto.<br/> |
| [**GatherCmpBlue**](texturecube-gathercmpblue.md)           | Per quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare, restituisce un confronto tra il relativo componente blu e un valore di confronto.<br/>  |
| [**GatherCmpGreen**](texturecube-gathercmpgreen.md)         | Per quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare, restituisce un confronto tra il relativo componente verde e un valore di confronto.<br/> |
| [**GatherCmpRed**](texturecube-gathercmpred.md)             | Per quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare, restituisce un confronto tra il relativo componente rosso e un valore di confronto.<br/>   |
| [**GatherGreen**](texturecube-gathergreen.md)               | Restituisce i componenti verdi dei quattro valori Texel che verrebbero usati in un'operazione di filtraggio bilineare.<br/>                                        |
| [**GatherRed**](texturecube-gatherred.md)                   | Restituisce i componenti rossi dei quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare.<br/>                                          |
| [**Esempio**](texturecube-sample.md)                         | Campiona una trama.<br/>                                                                                                                                  |
| [**SampleBias**](texturecube-samplebias.md)                 | Esegue il campionamento di una trama, dopo aver applicato il valore di distorsione al livello mipmap.<br/>                                                                               |
| [**SampleCmp**](texturecube-samplecmp.md)                   | Campiona una trama, usando un valore di confronto per rifiutare gli esempi.<br/>                                                                                      |
| [**SampleCmpLevelZero**](texturecube-samplecmplevelzero.md) | Esegue il campionamento di una trama (solo livello mipmap 0), usando un valore di confronto per rifiutare gli esempi.<br/>                                                                |
| [**SampleGrad**](texturecube-samplegrad.md)                 | Campiona una trama utilizzando una sfumatura per influenzare il modo in cui viene calcolata la posizione di esempio.<br/>                                                          |
| [**SampleLevel**](texturecube-samplelevel.md)               | Esegue il campionamento di una trama sul livello mipmap specificato.<br/>                                                                                                    |



 

## <a name="remarks"></a>Commenti

### <a name="minimum-shader-model"></a>Modello Shader minimo

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

 

 





