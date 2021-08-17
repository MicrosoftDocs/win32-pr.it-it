---
title: Texture1D
description: Texture1D
ms.assetid: 5f6fd0e4-a73e-4d13-b3a0-c884b7912581
keywords:
- Texture1D HLSL
topic_type:
- apiref
api_name:
- Texture1D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 382ac1e436eff4108a2179aeefd4395fbc52c7af304bb719cbadf87a3c1f3d3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117724872"
---
# <a name="texture1d"></a>Texture1D

Un tipo di trama 1D ( così come esiste nel modello[shader 4)](dx-graphics-hlsl-to-type.md)più le variabili di risorsa. Questo oggetto trama supporta i metodi seguenti oltre ai metodi nel modello shader 4.



| Metodo                                                                  | Descrizione                                                                                |
|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**GetDimensions**](sm5-object-texture1d-getdimensions.md)             | Ottiene le dimensioni della risorsa.                                                              |
| [**Caricamento**](texture1d-load.md)                                          | Legge i dati della trama.                                                                        |
| [**Operatore\[\]**](sm5-object-texture1d-operatorindex.md)              | Ottiene una variabile di risorsa di sola lettura.                                                        |
| [**Mips. Operatore\[\]\[\]**](sm5-object-texture1d-mipsoperatorindex.md) | Ottiene una variabile di risorsa di sola lettura.                                                        |
| [**Esempio**](texture1d-sample.md)                                      | Campio una trama.                                                                         |
| [**SampleBias**](texture1d-samplebias.md)                              | Campita una trama, dopo aver applicato il valore di distorsione al livello mipmap.                      |
| [**SampleCmp**](texture1d-samplecmp.md)                                | Campio una trama, usando un valore di confronto per rifiutare i campioni.                             |
| [**SampleCmpLevelZero**](texture1d-samplecmplevelzero.md)              | Campio una trama (solo livello mipmap 0), usando un valore di confronto per rifiutare i campioni.       |
| [**SampleGrad**](texture1d-samplegrad.md)                              | Campionare una trama usando una sfumatura per influenzare il modo in cui viene calcolata la posizione del campione. |
| [**SampleLevel**](texture1d-samplelevel.md)                            | Campita una trama a livello di mipmap specificato.                                           |



 

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

 

 




