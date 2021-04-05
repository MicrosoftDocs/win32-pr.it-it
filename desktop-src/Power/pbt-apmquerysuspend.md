---
description: Richiede l'autorizzazione per sospendere il computer. È necessario che l'applicazione preposta alla concessione delle autorizzazioni effettui tutti i preparativi per la sospensione prima della restituzione.
ms.assetid: 83cb0fdc-437e-4d03-87f0-6a416281c0d5
title: Evento PBT_APMQUERYSUSPEND (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 277e4faf7617037b917dedab3193e421a381166a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881717"
---
# <a name="pbt_apmquerysuspend-event"></a>\_Evento APMQUERYSUSPEND PBT

\[PBT \_ APMQUERYSUSPEND è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Il supporto per questo evento è stato rimosso in Windows Vista. In alternativa, usare [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) .\]

Richiede l'autorizzazione per sospendere il computer. È necessario che l'applicazione preposta alla concessione delle autorizzazioni effettui tutti i preparativi per la sospensione prima della restituzione.

Una finestra riceve questo evento tramite il messaggio [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) . I parametri *wParam* e *lParam* sono impostati come descritto di seguito.


```C++
LRESULT 
CALLBACK 
WindowProc( HWND   hwnd,    // handle to window
            UINT   uMsg,    // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMQUERYSUSPEND
            LPARAM lParam); // action flags
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

| Valore                                                                                                                                                                                                                                        | Significato                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMQUERYSUSPEND"></span><span id="pbt_apmquerysuspend"></span><dl> <dt>**PBT \_ APMQUERYSUSPEND**</dt> <dt>0 (0x0)</dt> </dl> | Identificatore dell'evento.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Flag di azione. Se il bit 0 è 1, l'applicazione può richiedere all'utente le istruzioni per la preparazione della sospensione. in caso contrario, l'applicazione deve essere preparata senza interazione dell'utente. Tutti gli altri valori di bit sono riservati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** per concedere la richiesta di sospensione. Per negare la richiesta, restituire la **\_ query broadcast \_ Deny**.

## <a name="remarks"></a>Commenti

Un'applicazione deve elaborare questo evento il più rapidamente possibile. L'applicazione può richiedere all'utente indicazioni su come prepararsi per la sospensione solo se è impostato il bit 0 nel parametro *Flags* . Tuttavia, se questo messaggio viene emesso perché l'utente sta chiudendo il coperchio del portatile, non sarà possibile richiedere l'intervento dell'utente. Le applicazioni devono rispettare il fatto che l'utente si aspetta un certo comportamento quando chiude il coperchio del portatile oppure preme il pulsante di alimentazione e consente la riuscita della transizione.

Il sistema consente circa 20 secondi prima che un'applicazione rimuova il messaggio [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) che invia l' \_ evento PBT APMQUERYSUSPEND dalla coda di messaggi dell'applicazione. Se un'applicazione non rimuove il messaggio dalla coda in meno di 20 secondi, il sistema presuppone che l'applicazione sia in uno stato non reattivo e che l'applicazione accetti la richiesta di sospensione. Le operazioni delle applicazioni che non elaborano le code di messaggi potrebbero essere interrotte. Dopo la rimozione del messaggio dalla coda di messaggi, un'applicazione può richiedere il tempo necessario per eseguire le operazioni necessarie prima di entrare nello stato di sospensione. Tutte le operazioni che potrebbero richiedere più di 20 secondi devono essere eseguite in questo momento, perché il sistema consente solo 20 secondi per il completamento delle operazioni durante l'elaborazione del [ \_ APMSUSPEND PBT](pbt-apmsuspend.md) .

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

[\_APMSUSPEND PBT](pbt-apmsuspend.md)
</dt> <dt>

[**\_POWERBROADCAST WM**](wm-powerbroadcast.md)
</dt> </dl>

 

 




