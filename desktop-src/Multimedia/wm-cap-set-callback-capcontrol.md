---
title: Messaggio di WM_CAP_SET_CALLBACK_CAPCONTROL (VFW. h)
description: Il \_ messaggio WM Cap \_ set \_ callback \_ CAPCONTROL imposta una funzione di callback nell'applicazione che fornisce un controllo di registrazione preciso. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro capSetCallbackOnCapControl.
ms.assetid: 1e93ed7b-8205-45fe-bdcf-efe3f709f728
keywords:
- WM_CAP_SET_CALLBACK_CAPCONTROL messaggi multimediali di Windows
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
ms.openlocfilehash: 7fda38bbc79461b7c5ccaf9b3a32c2c3a0f9e3e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301817"
---
# <a name="wm_cap_set_callback_capcontrol-message"></a>\_ \_ \_ Messaggio CAPCONTROL di richiamata di WM Cap Set \_

Il messaggio **WM \_ Cap \_ set \_ callback \_ CAPCONTROL** imposta una funzione di callback nell'applicazione che fornisce un controllo di registrazione preciso. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**capSetCallbackOnCapControl**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackoncapcontrol) .


```C++
WM_CAP_SET_CALLBACK_CAPCONTROL 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*
</dt> <dd>

Puntatore alla funzione di callback, di tipo [**capControlCallback**](/windows/desktop/api/Vfw/nc-vfw-capcontrolcallback). Specificare **null** per questo parametro per disabilitare una funzione di callback installata in precedenza.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito **positivo o negativo** se è in corso un'acquisizione di streaming o una sessione di acquisizione a frame singolo.

## <a name="remarks"></a>Commenti

Viene usata una singola funzione di callback per concedere all'applicazione un controllo preciso sui momenti in cui l'acquisizione di flussi inizia e viene completata. La finestra di acquisizione chiama innanzitutto la procedura con *nState* impostato su CONTROLCALLBACK \_ preroll dopo che tutti i buffer sono stati allocati e tutte le altre preparazioni di acquisizione sono state completate. Ciò consente all'applicazione di preregistrare le origini video, restituendo la funzione di callback nel momento esatto in cui viene avviata la registrazione. Un valore restituito **true** dalla funzione di callback continua l'acquisizione e il valore restituito di **false** Annulla l'acquisizione. Una volta avviata l'acquisizione, questa funzione di callback verrà chiamata spesso con *nState* impostato su CONTROLCALLBACK Capture \_ per consentire all'applicazione di terminare l'acquisizione restituendo **false**.

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

 

 





