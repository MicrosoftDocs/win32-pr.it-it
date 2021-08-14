---
title: WM_CAP_SET_CALLBACK_CAPCONTROL messaggio (Vfw.h)
description: Il messaggio WM CAP SET CALLBACK CAPCONTROL imposta una funzione \_ di callback \_ \_ \_ nell'applicazione fornendo un controllo di registrazione preciso. È possibile inviare questo messaggio in modo esplicito o usando la macro capSetCallbackOnCapControl.
ms.assetid: 1e93ed7b-8205-45fe-bdcf-efe3f709f728
keywords:
- WM_CAP_SET_CALLBACK_CAPCONTROL messaggio Windows Multimediali
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_CAPCONTROL
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70e5786ef67fe66c7ad0dac463824dcd49bfb34e4c8239ddca74ed60e3861bea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118369519"
---
# <a name="wm_cap_set_callback_capcontrol-message"></a>Messaggio \_ CAP SET CALLBACK \_ \_ \_ CAPCONTROL WM

Il **messaggio WM CAP SET CALLBACK \_ \_ \_ \_ CAPCONTROL** imposta una funzione di callback nell'applicazione fornendo un controllo di registrazione preciso. È possibile inviare questo messaggio in modo esplicito o usando la macro [**capSetCallbackOnCapControl.**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackoncapcontrol)


```C++
WM_CAP_SET_CALLBACK_CAPCONTROL 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*
</dt> <dd>

Puntatore alla funzione di callback, di [**tipo capControlCallback.**](/windows/desktop/api/Vfw/nc-vfw-capcontrolcallback) Specificare **NULL per** questo parametro per disabilitare una funzione di callback installata in precedenza.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE se** l'operazione ha esito positivo o **FALSE** se è in corso un'acquisizione di flusso o una sessione di acquisizione a frame singolo.

## <a name="remarks"></a>Commenti

Una singola funzione di callback viene usata per fornire all'applicazione un controllo preciso sui momenti in cui l'acquisizione di streaming inizia e viene completata. La finestra di acquisizione chiama prima la procedura con *nState* impostato su CONTROLCALLBACK PREROLL dopo che tutti i buffer sono stati allocati e tutte le altre operazioni di preparazione \_ dell'acquisizione sono state completate. In questo modo, l'applicazione può pre-registrare le origini video, tornando dalla funzione di callback nel momento esatto in cui la registrazione deve iniziare. Un valore restituito **TRUE dalla** funzione di callback continua l'acquisizione e un valore restituito **FALSE** interrompe l'acquisizione. Dopo l'inizio dell'acquisizione, questa funzione di callback verrà chiamata di frequente con *nState* impostato su CONTROLCALLBACK CAPTURING per consentire all'applicazione di terminare l'acquisizione \_ restituisce **FALSE.**

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

 

 





