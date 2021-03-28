---
title: Texture1D
description: Texture1D
ms.assetid: 5f6fd0e4-a73e-4d13-b3a0-c884b7912581
keywords:
- HLSL Texture1D
topic_type:
- apiref
api_name:
- Texture1D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8b8a60706ea2752109cdda9907ffe7c654efe531
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103955999"
---
# <a name="texture1d"></a>Texture1D

Un tipo di trama 1D ([presente in Shader Model 4](dx-graphics-hlsl-to-type.md)) più le variabili di risorsa. Questo oggetto texture supporta i metodi seguenti, oltre ai metodi in Shader Model 4.



| Metodo                                                                  | Descrizione                                                                                |
|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**GetDimensions**](sm5-object-texture1d-getdimensions.md)             | Ottiene le dimensioni della risorsa.                                                              |
| [**Caricamento**](texture1d-load.md)                                          | Legge i dati della trama.                                                                        |
| [**Operatore\[\]**](sm5-object-texture1d-operatorindex.md)              | Ottiene una variabile di risorsa di sola lettura.                                                        |
| [**MIPS. Operatore\[\]\[\]**](sm5-object-texture1d-mipsoperatorindex.md) | Ottiene una variabile di risorsa di sola lettura.                                                        |
| [**Esempio**](texture1d-sample.md)                                      | Campiona una trama.                                                                         |
| [**SampleBias**](texture1d-samplebias.md)                              | Esegue il campionamento di una trama, dopo aver applicato il valore di distorsione al livello mipmap.                      |
| [**SampleCmp**](texture1d-samplecmp.md)                                | Campiona una trama, usando un valore di confronto per rifiutare gli esempi.                             |
| [**SampleCmpLevelZero**](texture1d-samplecmplevelzero.md)              | Esegue il campionamento di una trama (solo livello mipmap 0), usando un valore di confronto per rifiutare gli esempi.       |
| [**SampleGrad**](texture1d-samplegrad.md)                              | Campiona una trama utilizzando una sfumatura per influenzare il modo in cui viene calcolata la posizione di esempio. |
| [**SampleLevel**](texture1d-samplelevel.md)                            | Esegue il campionamento di una trama sul livello mipmap specificato.                                           |



 

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

 

 




