---
title: WM_CAP_SEQUENCE messaggio (Vfw.h)
description: Il messaggio WM \_ CAP \_ SEQUENCE avvia l'acquisizione di video e audio in streaming in un file. È possibile inviare questo messaggio in modo esplicito o tramite la macro capCaptureSequence.
ms.assetid: 33d53abc-e37e-48c6-bfc8-9cd02fde5cb6
keywords:
- WM_CAP_SEQUENCE messaggio Windows Multimediali
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
ms.openlocfilehash: 023fd22d79fdfcd1df1f44b2862814ed809fd93c43ab9cd7122414ee1e27db39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117800266"
---
# <a name="wm_cap_sequence-message"></a>Messaggio \_ WM CAP \_ SEQUENCE

Il **messaggio WM CAP \_ \_ SEQUENCE** avvia l'acquisizione di video e audio in streaming in un file. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**capCaptureSequence.**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequence)


```C++
WM_CAP_SEQUENCE 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Valore restituito

Restituisce **TRUE in** caso di esito positivo o FALSE **in** caso contrario.

Se si verifica un errore e viene impostata una funzione di callback di errore usando il messaggio DI ERRORE [**CALLBACK \_ SET \_ \_ SET \_ WM,**](wm-cap-set-callback-error.md) viene chiamata la funzione di callback dell'errore.

## <a name="remarks"></a>Commenti

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

 

 





