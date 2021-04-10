---
title: Messaggio di WM_CAP_SEQUENCE (VFW. h)
description: Il \_ \_ messaggio sequenza di WM Cap avvia il flusso di video e l'acquisizione audio in un file. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro capCaptureSequence.
ms.assetid: 33d53abc-e37e-48c6-bfc8-9cd02fde5cb6
keywords:
- WM_CAP_SEQUENCE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- WM_CAP_SEQUENCE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2ef945510d0d71f1aa0e0cb5827288a613f5991
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964363"
---
# <a name="wm_cap_sequence-message"></a>\_ \_ Messaggio sequenza Cap WM

Il **messaggio \_ \_ sequenza di WM Cap** avvia il flusso di video e l'acquisizione audio in un file. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**capCaptureSequence**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequence) .


```C++
WM_CAP_SEQUENCE 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione è riuscita o **false** in caso contrario.

Se si verifica un errore e viene impostata una funzione di callback di errore utilizzando il messaggio di errore di richiamata di [**WM \_ Cap \_ set \_ \_**](wm-cap-set-callback-error.md) , viene chiamata la funzione di callback dell'errore.

## <a name="remarks"></a>Commenti

Se si desidera modificare i parametri che controllano l'acquisizione di flussi, utilizzare il messaggio di [**\_ installazione della sequenza di \_ serie \_ \_ WM Cap**](wm-cap-set-sequence-setup.md) prima di avviare l'acquisizione.

Per impostazione predefinita, la finestra di acquisizione non consente l'esecuzione di altre applicazioni durante l'acquisizione. Per eseguire l'override di questa impostazione, impostare il membro **fYield** della struttura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) su **true** oppure installare una funzione di callback yield.

Durante l'acquisizione di flussi, la finestra di acquisizione può facoltativamente inviare notifiche all'applicazione di tipi specifici di condizioni. Per installare le procedure di callback per queste notifiche, usare i messaggi seguenti:

-   [**\_errore di \_ callback del set di estremità WM \_ \_**](wm-cap-set-callback-error.md)
-   [**\_stato di \_ callback per set di estremità WM \_ \_**](wm-cap-set-callback-status.md)
-   [**\_rendimento di \_ \_ callback set di estremità \_ WM**](wm-cap-set-callback-yield.md)
-   [**\_VIDEOSTREAM di \_ \_ callback set di estremità \_ WM**](wm-cap-set-callback-videostream.md)
-   [**\_WAVESTREAM di \_ \_ callback set di estremità \_ WM**](wm-cap-set-callback-wavestream.md)

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

 

 





