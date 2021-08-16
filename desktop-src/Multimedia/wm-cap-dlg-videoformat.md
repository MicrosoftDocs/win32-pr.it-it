---
title: WM_CAP_DLG_VIDEOFORMAT messaggio (Vfw.h)
description: Il messaggio WM CAP DLG VIDEOFORMAT visualizza una finestra di dialogo in cui l'utente \_ può selezionare il formato \_ \_ video.
ms.assetid: 3b44507e-3806-467f-877a-e9992d1337cb
keywords:
- WM_CAP_DLG_VIDEOFORMAT messaggio Windows Multimediali
topic_type:
- apiref
api_name:
- WM_CAP_DLG_VIDEOFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbaa58e99c6a07db9109a0b1a6dae25de8abd46fef2631eb539961de16455ec0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118135400"
---
# <a name="wm_cap_dlg_videoformat-message"></a>Messaggio WM \_ CAP \_ DLG \_ VIDEOFORMAT

Il **messaggio WM CAP \_ \_ DLG \_ VIDEOFORMAT** visualizza una finestra di dialogo in cui l'utente può selezionare il formato video. La finestra di dialogo Formato video può essere usata per selezionare le dimensioni dell'immagine, la profondità in bit e le opzioni di compressione hardware. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**capDlgVideoFormat.**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideoformat)


```C++
WM_CAP_DLG_VIDEOFORMAT 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Valore restituito

Restituisce **TRUE se** l'operazione ha esito positivo o FALSE **in** caso contrario.

## <a name="remarks"></a>Commenti

Al termine di questo messaggio, le applicazioni potrebbero dover aggiornare la [**struttura CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) perché l'utente potrebbe aver modificato le dimensioni dell'immagine.

La finestra di dialogo Formato video è univoca per ogni driver di acquisizione. Alcuni driver di acquisizione potrebbero non supportare una finestra di dialogo Formato video. Le applicazioni possono determinare se il driver di acquisizione supporta questo messaggio controllando il membro **fHasDlgVideoFormat** di [**CAPDRIVERCAPS.**](/windows/win32/api/vfw/ns-vfw-capdrivercaps)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Acquisizione video](video-capture.md)
</dt> <dt>

[Messaggi di acquisizione video](video-capture-messages.md)
</dt> </dl>

 

 





