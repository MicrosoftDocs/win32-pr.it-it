---
title: Texture1DArray
description: Texture1DArray
ms.assetid: 3d793423-3d79-48c1-aa78-f9d93b79e0b6
keywords:
- HLSL Texture1DArray
topic_type:
- apiref
api_name:
- Texture1DArray
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 39cea5692e29ead74ba20c4a35ab8d43a1b19d42
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104045852"
---
# <a name="texture1darray"></a>Texture1DArray

Il tipo Texture1DArray ([esistente nel modello Shader 4](dx-graphics-hlsl-to-type.md)) più le variabili di risorsa. Questo oggetto texture supporta i metodi seguenti, oltre ai metodi in Shader Model 4.



| Metodo                                                                       | Descrizione                                                                                |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**GetDimensions**](sm5-object-texture1darray-getdimensions.md)             | Ottiene le dimensioni della risorsa.                                                              |
| [**Caricamento**](texture1darray-load.md)                                          | Legge i dati della trama.                                                                        |
| [**MIPS. Operatore\[\]\[\]**](sm5-object-texture1darray-mipsoperatorindex.md) | Ottiene una variabile di risorsa di sola lettura.                                                        |
| [**Operatore\[\]**](sm5-object-texture1darray-operatorindex.md)              | Ottiene una variabile di risorsa di sola lettura.                                                        |
| [**Esempio**](texture1darray-sample.md)                                      | Campiona una trama.                                                                         |
| [**SampleBias**](texture1darray-samplebias.md)                              | Esegue il campionamento di una trama, dopo aver applicato il valore di distorsione al livello mipmap.                      |
| [**SampleCmp**](texture1darray-samplecmp.md)                                | Campiona una trama, usando un valore di confronto per rifiutare gli esempi.                             |
| [**SampleCmpLevelZero**](texture1darray-samplecmplevelzero.md)              | Esegue il campionamento di una trama (solo livello mipmap 0), usando un valore di confronto per rifiutare gli esempi.       |
| [**SampleGrad**](texture1darray-samplegrad.md)                              | Campiona una trama utilizzando una sfumatura per influenzare il modo in cui viene calcolata la posizione di esempio. |
| [**SampleLevel**](texture1darray-samplelevel.md)                            | Esegue il campionamento di una trama sul livello mipmap specificato.                                           |



 

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

 

 




