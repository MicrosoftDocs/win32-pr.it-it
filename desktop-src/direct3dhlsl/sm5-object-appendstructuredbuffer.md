---
title: AppendStructuredBuffer
description: Buffer di output visualizzato come flusso a cui è possibile aggiungere lo shader. Solo i buffer strutturati possono assumere tipi T che sono strutture.
ms.assetid: 377b0358-0f9d-4021-9140-19c3d1bfed38
keywords:
- HLSL AppendStructuredBuffer
topic_type:
- apiref
api_name:
- AppendStructuredBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6c140052c861c8da3df6378fc3bc49816998c130
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728186"
---
# <a name="appendstructuredbuffer"></a>AppendStructuredBuffer

Buffer di output visualizzato come flusso a cui è possibile aggiungere lo shader. Solo i buffer strutturati possono assumere tipi T che sono strutture.



| Metodo                                                                   | Descrizione                               |
|--------------------------------------------------------------------------|-------------------------------------------|
| [**Accodamento**](sm5-object-appendstructuredbuffer-append.md)               | Aggiunge un valore alla fine del buffer. |
| [**GetDimensions**](sm5-object-appendstructuredbuffer-getdimensions.md) | Ottiene le dimensioni della risorsa.             |



 

Il formato UAV associato a questa risorsa deve essere creato con il formato DXGI \_ formato \_ sconosciuto.

È necessario che l'UAV associato a questa risorsa sia stato creato con l' [**\_ \_ \_ \_ aggiunta del flag UAV del buffer D3D11**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag).

Per ulteriori informazioni su un buffer strutturato di Accodamento, vedere entrambe le sezioni: [Accodamento e utilizzo del buffer](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources) e del [buffer strutturato](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources).

## <a name="minimum-shader-model"></a>Modello Shader minimo

Questo oggetto è supportato nei modelli shader seguenti.



| Modello di shader                                                                | Supportato |
|-----------------------------------------------------------------------------|-----------|
| [Shader Model 5](d3d11-graphics-reference-sm5.md) e versioni successive shader Models | sì       |



 

Questo oggetto è supportato per i tipi di shader seguenti:



| Vertice | Hull | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetti Shader Model 5](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 