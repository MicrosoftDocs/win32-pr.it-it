---
title: Texture3D
description: Texture3D
ms.assetid: a3640aac-b503-4716-8bc6-105e96bea03c
keywords:
- Texture3D HLSL
topic_type:
- apiref
api_name:
- Texture3D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7b5c715f5f2bb7edfaa149cf0da77db5fbca8d47636b6f84fd07071c3b75186e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119788321"
---
# <a name="texture3d"></a>Texture3D

Tipo Texture3D ([così come esiste nel modello shader 4)](dx-graphics-hlsl-to-type.md)più variabili di risorsa. Questo oggetto trama supporta i metodi seguenti oltre ai metodi nel modello shader 4.



| Metodo                                                                  | Descrizione                                                                                |
|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**GetDimensions**](sm5-object-texture3d-getdimensions.md)             | Ottiene le dimensioni della risorsa.                                                              |
| [**Caricamento**](texture3d-load.md)                                          | Legge i dati della trama.                                                                        |
| [**Mips. Operatore\[\]\[\]**](sm5-object-texture3d-mipsoperatorindex.md) | Ottiene una variabile di risorsa di sola lettura.                                                        |
| [**Operatore\[\]**](sm5-object-texture3d-operatorindex.md)              | Ottiene una variabile di risorsa di sola lettura.                                                        |
| [**Esempio**](texture3d-sample.md)                                      | Campio una trama.                                                                         |
| [**SampleBias**](texture3d-samplebias.md)                              | Campita una trama, dopo aver applicato il valore di distorsione al livello mipmap.                      |
| [**SampleGrad**](texture3d-samplegrad.md)                              | Campionare una trama usando una sfumatura per influenzare il modo in cui viene calcolata la posizione del campione. |
| [**SampleLevel**](texture3d-samplelevel.md)                            | Campita una trama a livello di mipmap specificato.                                           |



 

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

 

 




