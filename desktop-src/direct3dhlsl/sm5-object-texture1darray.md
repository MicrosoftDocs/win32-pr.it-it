---
title: Texture1DArray
description: Texture1DArray
ms.assetid: 3d793423-3d79-48c1-aa78-f9d93b79e0b6
keywords:
- Texture1DArray HLSL
topic_type:
- apiref
api_name:
- Texture1DArray
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 11573dc84c46149073ca3a7e192ed8541d9cfd4a78494a43f6130a7999534880
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118508677"
---
# <a name="texture1darray"></a>Texture1DArray

Tipo Texture1DArray ([così come esiste nel modello shader 4)](dx-graphics-hlsl-to-type.md)e variabili di risorsa. Questo oggetto trama supporta i metodi seguenti oltre ai metodi nel modello shader 4.



| Metodo                                                                       | Descrizione                                                                                |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**GetDimensions**](sm5-object-texture1darray-getdimensions.md)             | Ottiene le dimensioni della risorsa.                                                              |
| [**Caricamento**](texture1darray-load.md)                                          | Legge i dati della trama.                                                                        |
| [**Mips. Operatore\[\]\[\]**](sm5-object-texture1darray-mipsoperatorindex.md) | Ottiene una variabile di risorsa di sola lettura.                                                        |
| [**Operatore\[\]**](sm5-object-texture1darray-operatorindex.md)              | Ottiene una variabile di risorsa di sola lettura.                                                        |
| [**Esempio**](texture1darray-sample.md)                                      | Campio una trama.                                                                         |
| [**SampleBias**](texture1darray-samplebias.md)                              | Campita una trama, dopo aver applicato il valore di distorsione al livello mipmap.                      |
| [**SampleCmp**](texture1darray-samplecmp.md)                                | Campio una trama, usando un valore di confronto per rifiutare i campioni.                             |
| [**SampleCmpLevelZero**](texture1darray-samplecmplevelzero.md)              | Campio una trama (solo livello mipmap 0), usando un valore di confronto per rifiutare i campioni.       |
| [**SampleGrad**](texture1darray-samplegrad.md)                              | Campionare una trama usando una sfumatura per influenzare il modo in cui viene calcolata la posizione del campione. |
| [**SampleLevel**](texture1darray-samplelevel.md)                            | Campita una trama a livello di mipmap specificato.                                           |



 

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

 

 




