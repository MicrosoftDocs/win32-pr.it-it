---
title: WM_CAP_SEQUENCE_NOFILE messaggio (Vfw.h)
description: Il messaggio WM \_ CAP \_ SEQUENCE \_ NOFILE avvia l'acquisizione di video in streaming senza scrivere dati in un file. È possibile inviare questo messaggio in modo esplicito o tramite la macro capCaptureSequenceNoFile.
ms.assetid: 60cbcb62-3bfa-4182-a049-1e3cb2ede423
keywords:
- WM_CAP_SEQUENCE_NOFILE messaggio Windows Multimediali
topic_type:
- apiref
api_name:
- WM_CAP_SEQUENCE_NOFILE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d9344b53a52caa2e536483a339439a6d942ff1fea0313767d0e1be520c09b48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118940729"
---
# <a name="wm_cap_sequence_nofile-message"></a>Messaggio WM \_ CAP \_ SEQUENCE \_ NOFILE

Il **messaggio WM CAP SEQUENCE \_ \_ \_ NOFILE** avvia l'acquisizione di video in streaming senza scrivere dati in un file. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**capCaptureSequenceNoFile.**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequencenofile)


```C++
WM_CAP_SEQUENCE_NOFILE 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Valore restituito

Restituisce **TRUE in** caso di esito positivo o FALSE **in** caso contrario.

## <a name="remarks"></a>Commenti

Questo messaggio è utile in combinazione con le funzioni di callback del flusso video o del flusso audio waveform che consentono all'applicazione di usare direttamente i dati audio e video.

Se si vogliono modificare i parametri che controllano l'acquisizione di streaming, usare il messaggio [**WM CAP SET SEQUENCE \_ \_ \_ \_ SETUP**](wm-cap-set-sequence-setup.md) prima di avviare l'acquisizione.

Per impostazione predefinita, la finestra di acquisizione non consente ad altre applicazioni di continuare l'esecuzione durante l'acquisizione. Per eseguire l'override, impostare il membro **fYield** della struttura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) su **TRUE** oppure installare una funzione di callback yield.

Durante l'acquisizione in streaming, la finestra di acquisizione può facoltativamente inviare notifiche all'applicazione di tipi specifici di condizioni. Per installare le procedure di callback per queste notifiche, usare i messaggi seguenti:

-   [**ERRORE DI \_ CALLBACK WM CAP \_ SET \_ \_**](wm-cap-set-callback-error.md)
-   [**WM \_ CAP \_ SET \_ CALLBACK \_ STATUS**](wm-cap-set-callback-status.md)
-   [**WM \_ CAP \_ SET \_ CALLBACK \_ YIELD**](wm-cap-set-callback-yield.md)
-   [**WM \_ CAP \_ SET \_ CALLBACK \_ VIDEOSTREAM**](wm-cap-set-callback-videostream.md)
-   [**WM \_ CAP \_ SET \_ CALLBACK \_ WAVESTREAM**](wm-cap-set-callback-wavestream.md)

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

 

 





