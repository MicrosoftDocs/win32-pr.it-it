---
title: Texture3D
description: Texture3D
ms.assetid: a3640aac-b503-4716-8bc6-105e96bea03c
keywords:
- HLSL Texture3D
topic_type:
- apiref
api_name:
- Texture3D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 50b12f2184f6eca0fd7a68feb3e96d8d6fc65a61
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104045622"
---
# <a name="texture3d"></a>Texture3D

Il tipo Texture3D ([esistente nel modello Shader 4](dx-graphics-hlsl-to-type.md)) più le variabili di risorsa. Questo oggetto texture supporta i metodi seguenti, oltre ai metodi in Shader Model 4.



| Metodo                                                                  | Descrizione                                                                                |
|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**GetDimensions**](sm5-object-texture3d-getdimensions.md)             | Ottiene le dimensioni della risorsa.                                                              |
| [**Caricamento**](texture3d-load.md)                                          | Legge i dati della trama.                                                                        |
| [**MIPS. Operatore\[\]\[\]**](sm5-object-texture3d-mipsoperatorindex.md) | Ottiene una variabile di risorsa di sola lettura.                                                        |
| [**Operatore\[\]**](sm5-object-texture3d-operatorindex.md)              | Ottiene una variabile di risorsa di sola lettura.                                                        |
| [**Esempio**](texture3d-sample.md)                                      | Campiona una trama.                                                                         |
| [**SampleBias**](texture3d-samplebias.md)                              | Esegue il campionamento di una trama, dopo aver applicato il valore di distorsione al livello mipmap.                      |
| [**SampleGrad**](texture3d-samplegrad.md)                              | Campiona una trama utilizzando una sfumatura per influenzare il modo in cui viene calcolata la posizione di esempio. |
| [**SampleLevel**](texture3d-samplelevel.md)                            | Esegue il campionamento di una trama sul livello mipmap specificato.                                           |



 

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

 

 




