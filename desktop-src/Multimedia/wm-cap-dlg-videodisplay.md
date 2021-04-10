---
title: Messaggio di WM_CAP_DLG_VIDEODISPLAY (VFW. h)
description: Il \_ \_ \_ messaggio VIDEODISPLAY di WM Cap DLG Visualizza una finestra di dialogo in cui l'utente può impostare o modificare l'output del video.
ms.assetid: 151056f5-a9d1-4594-a8d7-32d4675ae3d6
keywords:
- WM_CAP_DLG_VIDEODISPLAY messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- WM_CAP_DLG_VIDEODISPLAY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 378d80923f9c0b7eda65fac83809e30626d53406
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964188"
---
# <a name="wm_cap_dlg_videodisplay-message"></a>\_ \_ Messaggio VIDEODISPLAY WM Cap DLG \_

Il messaggio **VIDEODISPLAY di WM \_ Cap \_ DLG \_** Visualizza una finestra di dialogo in cui l'utente può impostare o modificare l'output del video. Questa finestra di dialogo può contenere controlli che interessano la tonalità, il contrasto e la luminosità dell'immagine visualizzata, nonché l'allineamento del colore della chiave. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**capDlgVideoDisplay**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideodisplay) .


```C++
WM_CAP_DLG_VIDEODISPLAY 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione è riuscita o **false** in caso contrario.

## <a name="remarks"></a>Commenti

I controlli in questa finestra di dialogo non influiscono sui dati video digitati; che interessano solo l'output o la rivisualizzazione del segnale video.

La finestra di dialogo visualizzazione video è univoca per ogni driver di acquisizione. Alcuni driver di acquisizione potrebbero non supportare una finestra di dialogo per la visualizzazione video. Le applicazioni possono determinare se il driver di acquisizione supporta questo messaggio controllando il membro **fHasDlgVideoDisplay** della struttura [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) .

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

 

 





