---
title: Messaggio di WM_CAP_SET_CALLBACK_YIELD (VFW. h)
description: Il \_ messaggio WM Cap \_ set \_ callback \_ yield imposta una funzione di callback nell'applicazione. AVICap chiama questa procedura quando la finestra di acquisizione viene restituita durante l'acquisizione di flussi. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro capSetCallbackOnYield.
ms.assetid: d978dc3b-4336-46a4-85ae-7d588a63489b
keywords:
- WM_CAP_SET_CALLBACK_YIELD messaggi multimediali di Windows
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
ms.openlocfilehash: b95c9ba0be7a0abeb99c0590e255adb0bd442343
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301010"
---
# <a name="wm_cap_set_callback_yield-message"></a>\_ \_ \_ Messaggio prodotto di callback \_ set di estremità WM

Il messaggio **WM \_ Cap \_ set \_ callback \_ yield** imposta una funzione di callback nell'applicazione. AVICap chiama questa procedura quando la finestra di acquisizione viene restituita durante l'acquisizione di flussi. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**capSetCallbackOnYield**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonyield) .


```C++
WM_CAP_SET_CALLBACK_YIELD 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*
</dt> <dd>

Puntatore alla funzione di callback Yield, di tipo [**capYieldCallback**](/windows/desktop/api/Vfw/nc-vfw-capyieldcallback). Specificare **null** per questo parametro per disabilitare una funzione di callback yield precedentemente installata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito **positivo o negativo** se è in corso l'acquisizione di flussi o una sessione di acquisizione a singolo frame.

## <a name="remarks"></a>Commenti

Le applicazioni possono facoltativamente impostare una funzione di callback yield. La funzione yield callback viene chiamata almeno una volta per ogni fotogramma video acquisito durante l'acquisizione di flussi. Se una funzione di callback yield è installata, verrà chiamata indipendentemente dallo stato del membro **fYield** della struttura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) .

Se viene utilizzata la funzione yield callback, è necessario installarla prima di avviare la sessione di acquisizione e deve rimanere abilitata per la durata della sessione. Può essere disabilitato al termine dell'acquisizione di streaming.

Le applicazioni in genere eseguono un tipo di elaborazione dei messaggi nella funzione di callback costituito da un ciclo [PeekMessage](/windows/win32/api/winuser/nf-winuser-peekmessagea), [TranslateMessage](/windows/win32/api/winuser/nf-winuser-translatemessage), [DispatchMessage](/windows/win32/api/winuser/nf-winuser-dispatchmessage) , come nel ciclo di messaggi di una funzione [WinMain](/windows/win32/api/winbase/nf-winbase-winmain) . La funzione yield callback deve inoltre filtrare e rimuovere messaggi che possono causare problemi di rientranza.

Un'applicazione in genere restituisce **true** nella procedura yield per continuare l'acquisizione di flussi. Se una funzione di callback Yield restituisce **false**, la finestra di acquisizione interrompe il processo di acquisizione.

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

 

