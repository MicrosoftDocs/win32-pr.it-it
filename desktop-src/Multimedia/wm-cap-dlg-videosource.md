---
title: WM_CAP_DLG_VIDEOSOURCE messaggio (Vfw.h)
description: Il messaggio WM \_ CAP \_ DLG VIDEOSOURCE visualizza una finestra di dialogo in cui l'utente \_ può controllare l'origine video.
ms.assetid: 8dc2f271-1f48-4e63-badf-9f3322063018
keywords:
- WM_CAP_DLG_VIDEOSOURCE messaggio Windows Multimediali
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
ms.openlocfilehash: 7a1f05d7e3dc421759229adffa4ecc4b78affc26f1b4244887b017614c2ab4d2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119803881"
---
# <a name="wm_cap_dlg_videosource-message"></a>Messaggio \_ WM CAP \_ DLG \_ VIDEOSOURCE

Il **messaggio WM CAP \_ \_ DLG \_ VIDEOSOURCE** visualizza una finestra di dialogo in cui l'utente può controllare l'origine video. La finestra di dialogo Origine video potrebbe contenere controlli che selezionano origini di input. modificare la tonalità, il contrasto e la luminosità dell'immagine; e modificare la qualità del video prima di digitalizzare le immagini nel buffer dei fotogrammi. È possibile inviare questo messaggio in modo esplicito o usando la macro [**capDlgVideoSource.**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideosource)


```C++
WM_CAP_DLG_VIDEOSOURCE 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Valore restituito

Restituisce **TRUE se** l'operazione ha esito positivo o FALSE **in** caso contrario.

## <a name="remarks"></a>Commenti

La finestra di dialogo Origine video è univoca per ogni driver di acquisizione. Alcuni driver di acquisizione potrebbero non supportare una finestra di dialogo Origine video. Le applicazioni possono determinare se il driver di acquisizione supporta questo messaggio controllando il membro **fHasDlgVideoSource** della [**struttura CAPDRIVERCAPS.**](/windows/win32/api/vfw/ns-vfw-capdrivercaps)

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

 

 





