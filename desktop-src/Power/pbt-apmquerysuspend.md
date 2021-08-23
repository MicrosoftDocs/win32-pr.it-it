---
description: Richiede l'autorizzazione per sospendere il computer. È necessario che l'applicazione preposta alla concessione delle autorizzazioni effettui tutti i preparativi per la sospensione prima della restituzione.
ms.assetid: 83cb0fdc-437e-4d03-87f0-6a416281c0d5
title: PBT_APMQUERYSUSPEND evento (WinUser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e8063ce68a88c8a39cb6f9ab8a4f559aed41242eaae25fab616ace8793b16ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143384"
---
# <a name="pbt_apmquerysuspend-event"></a>Evento PBT \_ APMQUERYSUSPEND

\[PBT \_ APMQUERYSUSPEND è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Il supporto per questo evento è stato rimosso in Windows Vista. In [**alternativa, usare SetThreadExecutionState.**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate)\]

Richiede l'autorizzazione per sospendere il computer. È necessario che l'applicazione preposta alla concessione delle autorizzazioni effettui tutti i preparativi per la sospensione prima della restituzione.

Una finestra riceve questo evento tramite il [**messaggio WM \_ POWERBROADCAST.**](wm-powerbroadcast.md) I *parametri wParam* *e lParam* vengono impostati come descritto di seguito.


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

*Hwnd* 
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

Flag di azione. Se il bit 0 è 1, l'applicazione può richiedere all'utente indicazioni su come prepararsi per la sospensione. In caso contrario, l'applicazione deve prepararsi senza interazione dell'utente. Tutti gli altri valori di bit sono riservati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE per** concedere la richiesta di sospensione. Per negare la richiesta, restituire **BROADCAST \_ QUERY \_ DENY**.

## <a name="remarks"></a>Commenti

Un'applicazione deve elaborare questo evento il più rapidamente possibile. L'applicazione può richiedere all'utente istruzioni su come preparare la sospensione solo se è impostato il bit 0 nel parametro *Flags.* Tuttavia, se questo messaggio viene generato perché l'utente sta chiudendo il portatile, non sarà possibile chiedere conferma all'utente. Le applicazioni devono rispettare che l'utente si aspetta un determinato comportamento quando chiude il lunodico portatile o preme il pulsante di alimentazione e consente la transizione.

Il sistema consente circa 20 secondi a un'applicazione di rimuovere il messaggio [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) che invia \_ l'evento PBT APMQUERYSUSPEND dalla coda di messaggi dell'applicazione. Se un'applicazione non rimuove il messaggio dalla coda in meno di 20 secondi, il sistema presuppone che l'applicazione sia in uno stato non reattivo e che l'applicazione accetti la richiesta di sospensione. Le operazioni delle applicazioni che non elaborano le code di messaggi potrebbero essere interrotte. Dopo aver rimosso il messaggio dalla coda di messaggi, un'applicazione può richiedere il tempo necessario per eseguire le operazioni necessarie prima di entrare nello stato di sospensione. Tutte le operazioni che potrebbero richiedere più di 20 secondi devono essere eseguite in questo momento, poiché il sistema consente solo 20 secondi per il completamento delle operazioni durante l'elaborazione [PBT \_ APMSUSPEND.](pbt-apmsuspend.md)

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

[PBT \_ APMSUSPEND](pbt-apmsuspend.md)
</dt> <dt>

[**WM \_ POWERBROADCAST**](wm-powerbroadcast.md)
</dt> </dl>

 

 




