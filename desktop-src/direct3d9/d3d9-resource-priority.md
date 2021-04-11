---
description: Costanti utilizzate per impostare la priorità di una risorsa in priorità.
ms.assetid: 98886349-883f-41c3-870b-e4a639977760
title: D3D9_RESOURCE_PRIORITY (D3d9types. h)
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
ms.openlocfilehash: 1ae5a54c7645db63b1023c3571f8181f4ee2daec
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104234969"
---
# <a name="d3d9_resource_priority"></a>\_Priorità delle risorse d3d9 \_

Costanti utilizzate per impostare la priorità di una risorsa in [**priorità**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dresource9-setpriority).



| Costante/valore                                                                                                                                                                                                                                                                     | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="D3D9_RESOURCE_PRIORITY_MINIMUM"></span><span id="d3d9_resource_priority_minimum"></span><dl> <dt>**D3d9 \_ 0x28000000 \_ priorità \_ minima risorsa**</dt> <dt></dt> </dl> | La risorsa ha la priorità più bassa possibile. Questa costante contrassegna la risorsa come inutilizzata e per la rimozione. La risorsa deve essere rimossa non appena un'altra risorsa richiede lo spazio di memoria occupato dalla risorsa.<br/>                                                                                                                                                                                                              |
| <span id="D3D9_RESOURCE_PRIORITY_LOW"></span><span id="d3d9_resource_priority_low"></span><dl> <dt>**D3d9 \_ \_Priorità \_ bassa della risorsa**</dt> <dt>0x50000000</dt> </dl>             | La risorsa è pianificata con priorità bassa. Il posizionamento della risorsa non è critico e il sistema operativo esegue un lavoro minimo per trovare una posizione per la risorsa. Contrassegnare una risorsa come priorità bassa consente ad altre risorse più importanti di occupare la memoria più veloce.<br/>                                                                                                                                                      |
| <span id="D3D9_RESOURCE_PRIORITY_NORMAL"></span><span id="d3d9_resource_priority_normal"></span><dl> <dt>**D3d9 \_ 0x78000000 \_ \_ normale priorità risorsa**</dt> <dt></dt> </dl>    | La risorsa è pianificata con priorità normale. La posizione della risorsa è importante per le prestazioni, ma non è fondamentale. Il sistema operativo deve provare a collocare la risorsa contrassegnata come normale nella posizione preferita della risorsa invece che in una risorsa con priorità bassa. In genere, le trame sono contrassegnate come normali.<br/>                                                                                                     |
| <span id="D3D9_RESOURCE_PRIORITY_HIGH"></span><span id="d3d9_resource_priority_high"></span><dl> <dt>**D3d9 \_ Priorità di risorsa \_ \_ elevata**</dt> <dt>0xA0000000</dt> </dl>          | La risorsa è pianificata con priorità alta. La posizione della risorsa è essenziale per le prestazioni. Il sistema operativo tenta sempre di collocare la risorsa contrassegnata come elevata nella posizione preferita della risorsa invece che con una risorsa con priorità bassa o con priorità normale. In genere, le destinazioni di rendering sono contrassegnate come High.<br/>                                                                                                         |
| <span id="D3D9_RESOURCE_PRIORITY_MAXIMUM"></span><span id="d3d9_resource_priority_maximum"></span><dl> <dt>**D3d9 \_ 0xc8000000 \_ priorità \_ massima risorsa**</dt> <dt></dt> </dl> | La risorsa ha la massima priorità possibile. Questa costante contrassegna la priorità della risorsa come aggiunta temporaneamente. Una risorsa aggiunta temporaneamente viene rimossa dalla memoria solo se non è possibile risolvere il requisito di memoria di un buffer DMA. Il sistema operativo tenta di suddividere un buffer DMA fino alla dimensione minima e di rimuovere tutte le altre risorse che non sono bloccate e non aggiunte temporaneamente prima di rimuovere una risorsa aggiunta temporaneamente. <br/> |



## <a name="remarks"></a>Commenti

Valori diversi dalla **\_ priorità della risorsa d3d9 \_ \_ Minimum** e la **\_ \_ priorità \_ massima della risorsa d3d9** vengono considerati come hint dall'utilità di pianificazione.

È possibile utilizzare livelli di priorità diversi dai valori definiti in precedenza in questo argomento. Ad esempio, contrassegnare una risorsa con un livello di priorità di 0x78000001 indica che la priorità delle risorse è leggermente superiore al normale.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
