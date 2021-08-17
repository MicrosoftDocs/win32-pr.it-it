---
title: ConsumeStructuredBuffer
description: Buffer di input visualizzato come flusso da cui lo shader può estrarre valori. Solo i buffer strutturati possono usare tipi T che sono strutture.
ms.assetid: 373bdd97-6186-4bce-99bf-738a153234f6
keywords:
- ConsumeStructuredBuffer HLSL
topic_type:
- apiref
api_name:
- ConsumeStructuredBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7e4e0530c98b78f9b18b0934874fb5a082779694ced2f171293d0a38dc458a08
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986091"
---
# <a name="consumestructuredbuffer"></a>ConsumeStructuredBuffer

Buffer di input visualizzato come flusso da cui lo shader può estrarre valori. Solo i buffer strutturati possono usare tipi T che sono strutture.



| Metodo                                                                    | Descrizione                                 |
|---------------------------------------------------------------------------|---------------------------------------------|
| [**Utilizzo**](sm5-object-consumestructuredbuffer-consume.md)             | Rimuove un valore dalla fine del buffer. |
| [**GetDimensions**](sm5-object-consumestructuredbuffer-getdimensions.md) | Ottiene le dimensioni della risorsa.               |



 

Il formato UAV associato a questa risorsa deve essere creato con il formato DXGI \_ FORMAT \_ UNKNOWN.

L'UAV associato a questa risorsa deve essere stato creato con [**D3D11 \_ BUFFER \_ UAV \_ FLAG \_ APPEND**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag).

Per altre informazioni sull'utilizzo di buffer strutturati, vedere entrambe le sezioni: [accodare e utilizzare buffer](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources) e [buffer strutturato.](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources)

## <a name="minimum-shader-model"></a>Modello di shader minimo

Questo oggetto è supportato nei modelli di shader seguenti.



| Modello di shader                                                                | Supportato |
|-----------------------------------------------------------------------------|-----------|
| [Modello shader 5 e](d3d11-graphics-reference-sm5.md) modelli di shader superiori | sì       |



 

Questo oggetto è supportato per i tipi di shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetti modello shader 5](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 