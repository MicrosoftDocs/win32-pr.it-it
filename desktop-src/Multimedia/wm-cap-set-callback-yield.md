---
title: WM_CAP_SET_CALLBACK_YIELD messaggio (Vfw.h)
description: Il messaggio WM \_ CAP SET CALLBACK YIELD imposta una funzione di callback \_ \_ \_ nell'applicazione. AVICap chiama questa procedura quando la finestra di acquisizione produce durante l'acquisizione di streaming. È possibile inviare questo messaggio in modo esplicito o usando la macro capSetCallbackOnYield.
ms.assetid: d978dc3b-4336-46a4-85ae-7d588a63489b
keywords:
- WM_CAP_SET_CALLBACK_YIELD messaggio Windows Multimediali
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_YIELD
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee12db79a9e4808442618ca295694611aa9e098a87c8f72b25f04360e156c8a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118622236"
---
# <a name="wm_cap_set_callback_yield-message"></a>Messaggio WM \_ CAP \_ SET CALLBACK \_ \_ YIELD

Il **messaggio WM CAP SET CALLBACK \_ \_ \_ \_ YIELD** imposta una funzione di callback nell'applicazione. AVICap chiama questa procedura quando la finestra di acquisizione produce durante l'acquisizione di streaming. È possibile inviare questo messaggio in modo esplicito o usando la macro [**capSetCallbackOnYield.**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonyield)


```C++
WM_CAP_SET_CALLBACK_YIELD 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*
</dt> <dd>

Puntatore alla funzione di callback yield di [**tipo capYieldCallback**](/windows/desktop/api/Vfw/nc-vfw-capyieldcallback). Specificare **NULL per** questo parametro per disabilitare una funzione di callback yield installata in precedenza.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE se** l'operazione ha esito positivo o **FALSE** se è in corso un'acquisizione di streaming o una sessione di acquisizione a frame singolo.

## <a name="remarks"></a>Commenti

Le applicazioni possono facoltativamente impostare una funzione di callback yield. La funzione di callback yield viene chiamata almeno una volta per ogni fotogramma video acquisito durante l'acquisizione dello streaming. Se è installata una funzione di callback yield, verrà chiamata indipendentemente dallo stato del membro **fYield** della [**struttura CAPTUREPARMS.**](/windows/win32/api/vfw/ns-vfw-captureparms)

Se si usa la funzione di callback yield, deve essere installata prima di avviare la sessione di acquisizione e deve rimanere abilitata per la durata della sessione. Può essere disabilitato al termine dell'acquisizione dello streaming.

Le applicazioni in genere eseguono un tipo di elaborazione dei messaggi nella funzione di callback costituita da un ciclo [PeekMessage](/windows/win32/api/winuser/nf-winuser-peekmessagea), [TranslateMessage](/windows/win32/api/winuser/nf-winuser-translatemessage), [DispatchMessage,](/windows/win32/api/winuser/nf-winuser-dispatchmessage) come nel ciclo di messaggi di una [funzione WinMain.](/windows/win32/api/winbase/nf-winbase-winmain) La funzione di callback yield deve anche filtrare e rimuovere i messaggi che possono causare problemi di reentrancy.

Un'applicazione restituisce in **genere TRUE** nella procedura yield per continuare l'acquisizione di streaming. Se una funzione di callback yield restituisce **FALSE,** la finestra di acquisizione arresta il processo di acquisizione.

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

 

