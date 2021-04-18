---
description: Notifica alle applicazioni che il sistema ha ripreso l'operazione.
ms.assetid: f2997905-26c9-4884-ae79-64df5ce6bc55
title: Evento PBT_APMRESUMECRITICAL (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ef4a76e163f2e61e723f4df6572254e8ef89b40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312034"
---
# <a name="pbt_apmresumecritical-event"></a>\_Evento APMRESUMECRITICAL PBT

\[PBT \_ APMRESUMECRITICAL è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Il supporto per questo evento è stato rimosso in Windows Vista. In alternativa, usare [PBT \_ APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) .\]

Notifica alle applicazioni che il sistema ha ripreso l'operazione. Questo evento può indicare che alcune o tutte le applicazioni non hanno ricevuto un evento [PBT \_ APMSUSPEND](pbt-apmsuspend.md) . Questo evento, ad esempio, può essere trasmesso dopo una sospensione critica causata da una batteria in errore.

Una finestra riceve questo evento tramite il messaggio [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) . I parametri *wParam* e *lParam* sono impostati come descritto di seguito.


```C++
LRESULT 
CALLBACK 
WindowProc( HWND   hwnd,    // handle to window
            UINT   uMsg,    // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMRESUMECRITICAL
            LPARAM lParam); // zero
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*HWND* 
</dt> <dd>

Handle per la finestra.

</dd> <dt>*uMsg*</dt> <dd> 

| Valore                                                                                                                                                                                                                                                                   | Significato                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <dt>**[**WM \_ POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt> </dl> | Identificatore del messaggio.<br/> |



 

</dd> <dt>*wParam*</dt> <dd> 

| Valore                                                                                                                                                                                                                                              | Significato                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMRESUMECRITICAL"></span><span id="pbt_apmresumecritical"></span><dl> <dt>**PBT \_ APMRESUMECRITICAL**</dt> <dt>6 (0x6)</dt> </dl> | Identificatore dell'evento.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Riservati deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Poiché si verifica una sospensione critica senza notifica precedente, le risorse e i dati precedentemente disponibili potrebbero non essere presenti quando l'applicazione riceve questo evento. L'applicazione deve tentare di ripristinare il proprio stato al meglio della propria capacità. In una sospensione critica, il sistema gestisce lo stato della DRAM e dei dischi rigidi locali, ma non può mantenere le connessioni nette. È possibile che un'applicazione debba intervenire in relazione ai file aperti in rete prima della sospensione critica.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Fine del supporto client<br/>    | Windows XP<br/>                                                                                    |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                                           |
| Intestazione<br/>                   | <dl> <dt>WinUser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Eventi di riattivazione del sistema](system-wake-up-events.md)
</dt> <dt>

[Eventi di risparmio energia](power-management-events.md)
</dt> <dt>

[**\_POWERBROADCAST WM**](wm-powerbroadcast.md)
</dt> </dl>

 

 




