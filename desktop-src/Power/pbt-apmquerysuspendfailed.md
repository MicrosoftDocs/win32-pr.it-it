---
description: Notifica alle applicazioni che l'autorizzazione per sospendere il computer è stata negata.
ms.assetid: 0f68628f-9d38-45ca-9487-95bf62075e00
title: Evento PBT_APMQUERYSUSPENDFAILED (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1544cd5ed94ae0228c739e2ddb576b0bd77146eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312036"
---
# <a name="pbt_apmquerysuspendfailed-event"></a>\_Evento APMQUERYSUSPENDFAILED PBT

\[PBT \_ APMQUERYSUSPENDFAILED è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Il supporto per questo evento è stato rimosso in Windows Vista. In alternativa, usare [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) .\]

Notifica alle applicazioni che l'autorizzazione per sospendere il computer è stata negata. Questo evento viene trasmesso se un'applicazione o un driver ha restituito la **\_ richiesta broadcast \_ Deny** a un evento [PBT \_ APMQUERYSUSPEND](pbt-apmquerysuspend.md) precedente.

Una finestra riceve questo evento tramite il messaggio [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) . I parametri *wParam* e *lParam* sono impostati come descritto di seguito.


```C++
LRESULT 
CALLBACK 
WindowProc( HWND   hwnd,    // handle to window
            UINT   uMsg,    // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMQUERYSUSPENDFAILED
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

| Valore                                                                                                                                                                                                                                                          | Significato                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMQUERYSUSPENDFAILED"></span><span id="pbt_apmquerysuspendfailed"></span><dl> <dt>**PBT \_ APMQUERYSUSPENDFAILED**</dt> <dt>2 (0x2)</dt> </dl> | Identificatore dell'evento.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Riservati deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Le applicazioni in genere rispondono a questo evento riprendendo il normale funzionamento.

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

[Risparmio energia](power-management-portal.md)
</dt> <dt>

[Eventi di risparmio energia](power-management-events.md)
</dt> <dt>

[\_APMQUERYSUSPEND PBT](pbt-apmquerysuspend.md)
</dt> <dt>

[**\_POWERBROADCAST WM**](wm-powerbroadcast.md)
</dt> </dl>

 

 




