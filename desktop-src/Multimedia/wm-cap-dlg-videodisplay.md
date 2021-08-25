---
title: WM_CAP_DLG_VIDEODISPLAY messaggio (Vfw.h)
description: Il messaggio WM CAP DLG VIDEODISPLAY visualizza una finestra di dialogo in cui l'utente \_ può impostare o modificare \_ \_ l'output video.
ms.assetid: 151056f5-a9d1-4594-a8d7-32d4675ae3d6
keywords:
- WM_CAP_DLG_VIDEODISPLAY messaggio Windows Multimediali
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
ms.openlocfilehash: 16afffbf1d3450670b99d26303627771aa4bd3399a252cd16a68bc690012f541
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119803871"
---
# <a name="wm_cap_dlg_videodisplay-message"></a>Messaggio \_ WM CAP \_ DLG \_ VIDEODISPLAY

Il **messaggio WM CAP \_ \_ DLG \_ VIDEODISPLAY** visualizza una finestra di dialogo in cui l'utente può impostare o modificare l'output video. Questa finestra di dialogo può contenere controlli che influiscono su tonalità, contrasto e luminosità dell'immagine visualizzata, nonché l'allineamento dei colori chiave. È possibile inviare questo messaggio in modo esplicito o usando la macro [**capDlgVideoDisplay.**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideodisplay)


```C++
WM_CAP_DLG_VIDEODISPLAY 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Valore restituito

Restituisce **TRUE se** l'operazione ha esito positivo o FALSE **in** caso contrario.

## <a name="remarks"></a>Commenti

I controlli in questa finestra di dialogo non influiscono sui dati video digitalizzati. influiscono solo sull'output o sulla rivisualizzazione del segnale video.

La finestra di dialogo Visualizzazione video è univoca per ogni driver di acquisizione. Alcuni driver di acquisizione potrebbero non supportare una finestra di dialogo Visualizzazione video. Le applicazioni possono determinare se il driver di acquisizione supporta questo messaggio controllando il membro **fHasDlgVideoDisplay** della [**struttura CAPDRIVERCAPS.**](/windows/win32/api/vfw/ns-vfw-capdrivercaps)

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

 

 





