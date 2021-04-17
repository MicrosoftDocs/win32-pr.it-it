---
title: Messaggio di WM_CAP_DLG_VIDEOSOURCE (VFW. h)
description: Il \_ \_ \_ messaggio VIDEOSOURCE di WM Cap DLG Visualizza una finestra di dialogo in cui l'utente può controllare l'origine video.
ms.assetid: 8dc2f271-1f48-4e63-badf-9f3322063018
keywords:
- WM_CAP_DLG_VIDEOSOURCE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- WM_CAP_DLG_VIDEOSOURCE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38e8ae7e3d619964a547fbe0db4517fd1e7d277f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476222"
---
# <a name="wm_cap_dlg_videosource-message"></a>\_ \_ Messaggio VIDEOSOURCE WM Cap DLG \_

Il messaggio **VIDEOSOURCE di WM \_ Cap \_ DLG \_** Visualizza una finestra di dialogo in cui l'utente può controllare l'origine video. La finestra di dialogo origine video potrebbe contenere controlli che selezionano origini di input; modificare la tonalità, il contrasto e la luminosità dell'immagine; e modificare la qualità del video prima di digitalizzare le immagini nel buffer del frame. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**capDlgVideoSource**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideosource) .


```C++
WM_CAP_DLG_VIDEOSOURCE 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione è riuscita o **false** in caso contrario.

## <a name="remarks"></a>Commenti

La finestra di dialogo origine video è univoca per ogni driver di acquisizione. Alcuni driver di acquisizione potrebbero non supportare una finestra di dialogo di origine video. Le applicazioni possono determinare se il driver di acquisizione supporta questo messaggio controllando il membro **fHasDlgVideoSource** della struttura [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Acquisizione video](video-capture.md)
</dt> <dt>

[Messaggi di acquisizione video](video-capture-messages.md)
</dt> </dl>

 

 





