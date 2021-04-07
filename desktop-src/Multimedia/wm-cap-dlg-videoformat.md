---
title: Messaggio di WM_CAP_DLG_VIDEOFORMAT (VFW. h)
description: Il \_ \_ \_ messaggio VIDEOFORMAT di WM Cap DLG Visualizza una finestra di dialogo in cui l'utente può selezionare il formato video.
ms.assetid: 3b44507e-3806-467f-877a-e9992d1337cb
keywords:
- WM_CAP_DLG_VIDEOFORMAT messaggi multimediali di Windows
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
ms.openlocfilehash: 8d244c4c141845d4ede66804918514e091872e89
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964095"
---
# <a name="wm_cap_dlg_videoformat-message"></a>\_ \_ Messaggio VIDEOFORMAT WM Cap DLG \_

Il messaggio **VIDEOFORMAT di WM \_ Cap \_ DLG \_** Visualizza una finestra di dialogo in cui l'utente può selezionare il formato video. La finestra di dialogo Formato video può essere usata per selezionare le dimensioni dell'immagine, la profondità dei bit e le opzioni di compressione hardware. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**capDlgVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideoformat) .


```C++
WM_CAP_DLG_VIDEOFORMAT 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione è riuscita o **false** in caso contrario.

## <a name="remarks"></a>Commenti

Quando il messaggio viene restituito, le applicazioni potrebbero dover aggiornare la struttura [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) perché l'utente potrebbe aver modificato le dimensioni dell'immagine.

La finestra di dialogo Formato video è univoca per ogni driver di acquisizione. Alcuni driver di acquisizione potrebbero non supportare la finestra di dialogo Formato video. Le applicazioni possono determinare se il driver di acquisizione supporta questo messaggio controllando il membro **fHasDlgVideoFormat** di [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps).

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

 

 





