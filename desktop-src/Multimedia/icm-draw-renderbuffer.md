---
title: Messaggio di ICM_DRAW_RENDERBUFFER (VFW. h)
description: Il \_ \_ messaggio RENDERBUFFER per il progetto ICM notifica a un driver di rendering di creare i frame passati. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro ICDrawRenderBuffer.
ms.assetid: b21be12c-b8a5-49ea-b6b3-d2eb0077a8e9
keywords:
- ICM_DRAW_RENDERBUFFER messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- ICM_DRAW_RENDERBUFFER
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccb02a1fbe334547b9679970ac7598df23237f12
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964687"
---
# <a name="icm_draw_renderbuffer-message"></a>\_ \_ Messaggio RENDERBUFFER per il progetto ICM

Il **messaggio \_ \_ RENDERBUFFER per il progetto ICM** notifica a un driver di rendering di creare i frame passati. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**ICDrawRenderBuffer**](/windows/desktop/api/Vfw/nf-vfw-icdrawrenderbuffer) .


```C++
ICM_DRAW_RENDERBUFFER 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce alcun valore.

## <a name="remarks"></a>Commenti

Utilizzare questo messaggio con hardware che esegue la decompressione, la temporizzazione e il disegno asincroni.

Questo messaggio viene in genere usato per eseguire un'operazione di ricerca quando il driver deve essere indicato in modo specifico per visualizzare ogni fotogramma video passato anziché riprodurre una sequenza di fotogrammi video.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Gestione compressione video](video-compression-manager.md)
</dt> <dt>

[Messaggi di compressione video](video-compression-messages.md)
</dt> </dl>

 

 





