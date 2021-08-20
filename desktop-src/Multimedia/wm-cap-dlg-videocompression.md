---
title: WM_CAP_DLG_VIDEOCOMPRESSION messaggio (Vfw.h)
description: Il messaggio WM \_ CAP \_ DLG VIDEOCOMPRESSION visualizza una finestra di dialogo in cui l'utente può selezionare un \_ oggetto da usare durante il processo di acquisizione.
ms.assetid: 526e4b5d-49a4-4bb5-92d6-cdd567636354
keywords:
- WM_CAP_DLG_VIDEOCOMPRESSION messaggio Windows Multimediali
topic_type:
- apiref
api_name:
- WM_CAP_DLG_VIDEOCOMPRESSION
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 816aeb26455ba375b4446edc275ec4fbaa318b67b1fea64bd6049760f45d8235
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118135444"
---
# <a name="wm_cap_dlg_videocompression-message"></a>Messaggio WM \_ CAP \_ DLG \_ VIDEOCOMPRESSION

Il **messaggio WM CAP \_ \_ DLG \_ VIDEOCOMPRESSION** visualizza una finestra di dialogo in cui l'utente può selezionare un elemento da usare durante il processo di acquisizione. L'elenco dei file disponibili può variare in base al formato video selezionato nella finestra di dialogo Formato video del driver di acquisizione. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**capDlgVideoCompression.**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideocompression)


```C++
WM_CAP_DLG_VIDEOCOMPRESSION 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Valore restituito

Restituisce **TRUE in** caso di esito positivo o FALSE **in** caso contrario.

## <a name="remarks"></a>Commenti

Usare questo messaggio con driver di acquisizione che forniscono frame solo nel formato \_ RGB BI. Questo messaggio è particolarmente utile nell'operazione di acquisizione passaggio per combinare l'acquisizione e la compressione in una singola operazione. La compressione dei fotogrammi con un software come parte di un'operazione di acquisizione in tempo reale è molto probabilmente troppo dispendiosa in termini di tempo.

La compressione non influisce sui frame copiati negli Appunti.

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

 

 





