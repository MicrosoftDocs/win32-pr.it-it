---
description: Notifica alle applicazioni che il sistema ha ripreso il funzionamento.
ms.assetid: f2997905-26c9-4884-ae79-64df5ce6bc55
title: PBT_APMRESUMECRITICAL evento (WinUser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f13214a97e99954d0649df0647bdf6ee3823b91926c0f2f2dc1212fa780a7b6c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961708"
---
# <a name="pbt_apmresumecritical-event"></a>Evento PBT \_ APMRESUMECRITICAL

\[PBT APMRESUMECRITICAL è disponibile per l'uso nei \_ sistemi operativi specificati nella sezione Requisiti. Il supporto per questo evento è stato rimosso in Windows Vista. In [alternativa, usare \_ PBT APMRESUMEAUTOMATIC.](pbt-apmresumeautomatic.md)\]

Notifica alle applicazioni che il sistema ha ripreso il funzionamento. Questo evento può indicare che alcune o tutte le applicazioni non hanno ricevuto un evento [ \_ APMSUSPEND PBT.](pbt-apmsuspend.md) Ad esempio, questo evento può essere trasmesso dopo una sospensione critica causata da una batteria in errore.

Una finestra riceve questo evento tramite il [**messaggio WM \_ POWERBROADCAST.**](wm-powerbroadcast.md) I *parametri wParam* *e lParam* vengono impostati come descritto di seguito.


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

*Hwnd* 
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

Riservato; deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Poiché si verifica una sospensione critica senza notifica precedente, le risorse e i dati precedentemente disponibili potrebbero non essere presenti quando l'applicazione riceve questo evento. L'applicazione deve tentare di ripristinare il proprio stato al meglio della propria capacità. In una sospensione critica, il sistema mantiene lo stato della DRAM e dei dischi rigidi locali, ma potrebbe non mantenere connessioni di rete. Un'applicazione potrebbe dover intervenire rispetto ai file aperti in rete prima della sospensione critica.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                                              |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                                     |
| Fine del supporto client<br/>    | Windows XP<br/>                                                                                    |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                                           |
| Intestazione<br/>                   | <dl> <dt>WinUser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Eventi di riattivazione del sistema](system-wake-up-events.md)
</dt> <dt>

[Eventi di risparmio energia](power-management-events.md)
</dt> <dt>

[**WM \_ POWERBROADCAST**](wm-powerbroadcast.md)
</dt> </dl>

 

 




