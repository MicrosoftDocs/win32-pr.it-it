---
title: ConsumeStructuredBuffer
description: Un buffer di input che viene visualizzato come flusso da cui lo shader può effettuare il pull dei valori. Solo i buffer strutturati possono assumere tipi T che sono strutture.
ms.assetid: 373bdd97-6186-4bce-99bf-738a153234f6
keywords:
- HLSL ConsumeStructuredBuffer
topic_type:
- apiref
api_name:
- ConsumeStructuredBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: af7a670713dc5b63839702a04a632dda61ebfa43
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104993597"
---
# <a name="consumestructuredbuffer"></a>ConsumeStructuredBuffer

Un buffer di input che viene visualizzato come flusso da cui lo shader può effettuare il pull dei valori. Solo i buffer strutturati possono assumere tipi T che sono strutture.



| Metodo                                                                    | Descrizione                                 |
|---------------------------------------------------------------------------|---------------------------------------------|
| [**Utilizzo**](sm5-object-consumestructuredbuffer-consume.md)             | Rimuove un valore dalla fine del buffer. |
| [**GetDimensions**](sm5-object-consumestructuredbuffer-getdimensions.md) | Ottiene le dimensioni della risorsa.               |



 

Il formato UAV associato a questa risorsa deve essere creato con il formato DXGI \_ formato \_ sconosciuto.

È necessario che l'UAV associato a questa risorsa sia stato creato con l' [**\_ \_ \_ \_ aggiunta del flag UAV del buffer D3D11**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag).

Per ulteriori informazioni sull'utilizzo dei buffer strutturati, vedere entrambe le sezioni: [Accodamento e utilizzo del buffer](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources) e del [buffer strutturato](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources).

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

 

 