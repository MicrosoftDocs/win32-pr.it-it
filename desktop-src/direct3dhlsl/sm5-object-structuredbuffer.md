---
title: StructuredBuffer
description: Buffer di sola lettura che può assumere un tipo T che è una struttura.
ms.assetid: fe2ec0b8-0e19-42b6-9dad-c992ecdeb19e
keywords:
- HLSL StructuredBuffer
topic_type:
- apiref
api_name:
- StructuredBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 524078780ac28d691c4999491bed146a04d34439
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104993408"
---
# <a name="structuredbuffer"></a>StructuredBuffer

Buffer di sola lettura che può assumere un tipo T che è una struttura.



| Metodo                                                             | Descrizione                            |
|--------------------------------------------------------------------|----------------------------------------|
| [**GetDimensions**](sm5-object-structuredbuffer-getdimensions.md) | Ottiene le dimensioni della risorsa.          |
| [**Caricamento**](structuredbuffer-load.md)                              | Legge i dati del buffer.                     |
| [**Operatore\[\]**](sm5-object-structuredbuffer-operatorindex.md)  | Restituisce una variabile di risorsa di sola lettura. |



 

Il formato UAV associato a questa risorsa deve essere creato con il formato DXGI \_ formato \_ sconosciuto.

Per ulteriori informazioni sui [buffer strutturati](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources), vedere il materiale di panoramica.

## <a name="minimum-shader-model"></a>Modello Shader minimo

Questo oggetto è supportato nei modelli shader seguenti.



| Modello di shader                                                                                                                                                                                                            | Supportato |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| [Shader Model 5](d3d11-graphics-reference-sm5.md) e High shader Models Shader Model [4](dx-graphics-hlsl-sm4.md) (disponibile per il calcolo e i pixel shader in Direct3D 11 su alcuni dispositivi Direct3D 10).<br/> | sì       |



 

Questo oggetto è supportato per i tipi di shader seguenti.



| Vertice | Hull | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetti Shader Model 5](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

