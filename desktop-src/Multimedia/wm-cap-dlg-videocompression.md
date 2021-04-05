---
title: Messaggio di WM_CAP_DLG_VIDEOCOMPRESSION (VFW. h)
description: Il \_ messaggio VIDEOCOMPRESSION di WM Cap \_ DLG \_ Visualizza una finestra di dialogo in cui l'utente può selezionare un compressore da usare durante il processo di acquisizione.
ms.assetid: 526e4b5d-49a4-4bb5-92d6-cdd567636354
keywords:
- WM_CAP_DLG_VIDEOCOMPRESSION messaggi multimediali di Windows
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
ms.openlocfilehash: d851f73df7adbc205585eb7c69ad9d4d969aba66
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048333"
---
# <a name="wm_cap_dlg_videocompression-message"></a>\_ \_ Messaggio VIDEOCOMPRESSION WM Cap DLG \_

Il messaggio **VIDEOCOMPRESSION di WM \_ Cap \_ DLG \_** Visualizza una finestra di dialogo in cui l'utente può selezionare un compressore da usare durante il processo di acquisizione. L'elenco dei commutatori disponibili può variare a seconda del formato video selezionato nella finestra di dialogo Formato video del driver di acquisizione. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**capDlgVideoCompression**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideocompression) .


```C++
WM_CAP_DLG_VIDEOCOMPRESSION 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione è riuscita o **false** in caso contrario.

## <a name="remarks"></a>Commenti

Utilizzare questo messaggio con i driver di acquisizione che forniscono frame solo nel \_ formato RGB bi. Questo messaggio è particolarmente utile nell'operazione di acquisizione step per combinare l'acquisizione e la compressione in un'unica operazione. La compressione dei frame con un commediatore software come parte di un'operazione di acquisizione in tempo reale è molto probabilmente troppo dispendiosa in termini di tempo.

La compressione non influisce sui frame copiati negli Appunti.

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

 

 





