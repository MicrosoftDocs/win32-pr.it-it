---
description: Costanti usate per impostare la priorità di una risorsa in SetPriority.
ms.assetid: 98886349-883f-41c3-870b-e4a639977760
title: D3D9_RESOURCE_PRIORITY (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3D9_RESOURCE_PRIORITY_MINIMUM
- D3D9_RESOURCE_PRIORITY_LOW
- D3D9_RESOURCE_PRIORITY_NORMAL
- D3D9_RESOURCE_PRIORITY_HIGH
- D3D9_RESOURCE_PRIORITY_MAXIMUM
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 367d50292b283cc7a0dcdef42b2e2c270099e314dc61c8d590e7ef2a1091a4f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119751331"
---
# <a name="d3d9_resource_priority"></a>PRIORITÀ DELLE RISORSE D3D9 \_ \_

Costanti utilizzate per impostare la priorità di una risorsa in [**SetPriority.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dresource9-setpriority)



| Costante/valore                                                                                                                                                                                                                                                                     | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="D3D9_RESOURCE_PRIORITY_MINIMUM"></span><span id="d3d9_resource_priority_minimum"></span><dl> <dt>**D3D9 \_ RESOURCE \_ PRIORITY \_ MINIMUM**</dt> <dt>0x28000000</dt> </dl> | La risorsa ha la priorità più bassa possibile. Questa costante contrassegna la risorsa come inutilizzata e per la rimuovere. La risorsa deve essere sgomberata non appena un'altra risorsa richiede lo spazio di memoria che la risorsa occupa.<br/>                                                                                                                                                                                                              |
| <span id="D3D9_RESOURCE_PRIORITY_LOW"></span><span id="d3d9_resource_priority_low"></span><dl> <dt>**D3D9 \_ PRIORITÀ \_ DELLE RISORSE BASSA \_ 0x50000000**</dt> <dt></dt> </dl>             | La risorsa è pianificata con priorità bassa. La posizione della risorsa non è critica e il sistema operativo esegue un lavoro minimo per trovare una posizione per la risorsa. Contrassegnare una risorsa come con priorità bassa consente ad altre risorse più critiche di occupare la memoria più veloce.<br/>                                                                                                                                                      |
| <span id="D3D9_RESOURCE_PRIORITY_NORMAL"></span><span id="d3d9_resource_priority_normal"></span><dl> <dt>**D3D9 \_ PRIORITÀ \_ \_ DELLE**</dt> <dt>RISORSE NORMALE 0x78000000</dt> </dl>    | La risorsa è pianificata con priorità normale. La posizione della risorsa è importante per le prestazioni, ma non è fondamentale. Il sistema operativo deve provare a inserire la risorsa contrassegnata come normale nella posizione preferita della risorsa anziché una risorsa con priorità bassa. In genere, le trame sono contrassegnate come normali.<br/>                                                                                                     |
| <span id="D3D9_RESOURCE_PRIORITY_HIGH"></span><span id="d3d9_resource_priority_high"></span><dl> <dt>**D3D9 \_ PRIORITÀ \_ DELLE RISORSE ALTA \_ 0xa0000000**</dt> <dt></dt> </dl>          | La risorsa è pianificata con priorità alta. Il posizionamento della risorsa è fondamentale per le prestazioni. Il sistema operativo tenta sempre di inserire la risorsa contrassegnata come alta nella posizione preferita della risorsa anziché una risorsa con priorità bassa o con priorità normale. In genere, le destinazioni di rendering sono contrassegnate come elevate.<br/>                                                                                                         |
| <span id="D3D9_RESOURCE_PRIORITY_MAXIMUM"></span><span id="d3d9_resource_priority_maximum"></span><dl> <dt>**D3D9 \_ VALORE MASSIMO \_ \_ PRIORITÀ RISORSA**</dt> <dt>0xc8000000</dt> </dl> | La risorsa ha la priorità massima possibile. Questa costante contrassegna la priorità della risorsa come aggiunta in modo pinned. Una risorsa aggiunta in modo soft viene rimosso dalla memoria solo se non esiste un altro modo per risolvere il requisito di memoria di un buffer DMA. Il sistema operativo tenta di suddividere un buffer DMA in base alle dimensioni minime e di eviti tutte le altre risorse non bloccate e non bloccate in modo soft prima che venga esenti da una risorsa bloccata in modo soft. <br/> |



## <a name="remarks"></a>Commenti

I valori diversi **da D3D9 \_ RESOURCE PRIORITY \_ \_ MINIMUM** e **D3D9 \_ RESOURCE PRIORITY \_ \_ MAXIMUM** vengono considerati hint dall'utilità di pianificazione.

È possibile utilizzare livelli di priorità diversi da quelli definiti in precedenza in questo argomento. Ad esempio, contrassegnare una risorsa con un livello di priorità 0x78000001 indica che la priorità della risorsa è leggermente superiore alla normale.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3d9types.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
