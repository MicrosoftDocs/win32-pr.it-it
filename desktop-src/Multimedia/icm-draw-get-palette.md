---
title: Messaggio di ICM_DRAW_GET_PALETTE (VFW. h)
description: Il \_ messaggio della \_ \_ tavolozza di estrazione di ICM richiede a un driver di rendering di restituire una tavolozza.
ms.assetid: 02a9df7d-e0b9-4bde-9cda-c36d2a10a23c
keywords:
- ICM_DRAW_GET_PALETTE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- ICM_DRAW_GET_PALETTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a03f3658d2a2653f940e18e9b82b7cc3d7690ad2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047979"
---
# <a name="icm_draw_get_palette-message"></a>\_Messaggio della \_ tavolozza di estrazione di ICM \_

Il messaggio della **\_ \_ \_ tavolozza di estrazione di ICM** richiede a un driver di rendering di restituire una tavolozza.


```C++
ICM_DRAW_GET_PALETTE 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valore restituito

Il driver deve restituire uno dei seguenti: un handle della tavolozza utilizzata, **null** se non è presente un handle da restituire oppure ICERR non \_ supportato se non supporta le tavolozze.

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

 

 





