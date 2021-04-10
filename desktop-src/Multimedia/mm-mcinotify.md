---
title: Messaggio MM_MCINOTIFY (mmsystem. h)
description: Il \_ messaggio mm MCINOTIFY notifica a un'applicazione che un dispositivo MCI ha completato un'operazione. I dispositivi MCI inviano questo messaggio solo quando \_ viene usato il flag di notifica MCI.
ms.assetid: a0840130-2969-4ce5-b098-3e45401eebb1
keywords:
- MM_MCINOTIFY messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MM_MCINOTIFY
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96ee62c4a2b6e17bf5ad6d719dcb7d6e992a2f2e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120458"
---
# <a name="mm_mcinotify-message"></a>\_Messaggio MCINOTIFY mm

Il messaggio **mm \_ MCINOTIFY** notifica a un'applicazione che un dispositivo MCI ha completato un'operazione. I dispositivi MCI inviano questo messaggio solo quando \_ viene usato il flag di notifica MCI.


```C++
MM_MCINOTIFY 
wParam = (WPARAM) wFlags 
lParam = (LONG) lDevID
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="wFlags"></span><span id="wflags"></span><span id="WFLAGS"></span>*wFlags*
</dt> <dd>

Motivo della notifica. Vengono definiti i valori seguenti:



| Requisito | Valore |
|-------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_notifica MCI \_ interrotta    | Il dispositivo ha ricevuto un comando che impedisce che le condizioni correnti per avviare la funzione di callback vengano soddisfatte. Se un nuovo comando interrompe il comando corrente e richiede anche la notifica, il dispositivo invia solo questo messaggio e non la \_ notifica MCI \_ sostituita |
| \_errore di notifica MCI \_    | Si è verificato un errore del dispositivo durante l'esecuzione del comando da parte del dispositivo.                                                                                                                                                                                                            |
| \_notifica MCI \_ riuscita | Le condizioni che avviano la funzione di callback sono state soddisfatte.                                                                                                                                                                                                                 |
| \_notifica MCI \_ sostituita | Il dispositivo ha ricevuto un altro comando con il flag "notify" impostato e le condizioni correnti per l'avvio della funzione di callback sono state sostituite.                                                                                                                           |



 

</dd> <dt>

<span id="lDevID"></span><span id="ldevid"></span><span id="LDEVID"></span>*lDevID*
</dt> <dd>

Identificatore del dispositivo che avvia la funzione di callback.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore.

## <a name="remarks"></a>Commenti

Per ulteriori informazioni sul flag di \_ notifica MCI, vedere [il flag di notifica](the-notify-flag.md).

Un dispositivo restituisce il \_ flag MCI Notify \_ successful con **mm \_ MCINOTIFY** quando viene completata l'azione per un comando. Ad esempio, un dispositivo audio CD utilizza questo flag per la notifica del comando [**Play**](play.md) ( [**MCI \_ Play**](mci-play.md)) al termine della riproduzione del dispositivo. Il comando **Play** ha esito positivo solo quando raggiunge la posizione finale specificata o raggiunge la fine del supporto. Analogamente, i comandi [**Seek**](seek.md) ( [**MCI \_ Seek**](mci-seek.md)) e [**record**](record.md) ( [**MCI \_ record**](mci-record.md)) non restituiscono la \_ notifica MCI \_ riuscita fino a raggiungere la posizione finale specificata o raggiungere la fine del supporto.

Un dispositivo restituisce il \_ \_ flag di notifica di MCI interrotto con **mm \_ MCINOTIFY** solo quando riceve un comando che impedisce che soddisfi le condizioni di notifica. Ad esempio, il comando [**Play**](play.md) non interrompe la notifica per un comando **Play** precedente, purché il nuovo comando non modifichi la direzione della riproduzione o modifichi la posizione finale. I comandi [**Seek**](seek.md) e [**record**](record.md) si comportano in modo analogo. MCI non invia inoltre notifiche MCI \_ \_ interrotte quando la riproduzione o la registrazione viene sospesa con il comando [**Sospendi**](pause.md) (pausa [**MCI \_**](mci-pause.md)). L'invio del comando [**Resume**](resume.md) ( [**MCI \_ Resume**](mci-resume.md)) consente loro di continuare a soddisfare le condizioni di callback.

Quando l'applicazione richiede una notifica per un comando, controllare la restituzione dell'errore delle funzioni [**mciSendString**](/previous-versions//dd757161(v=vs.85)) o [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) . Se queste funzioni riscontrano un errore e restituiscono un valore diverso da zero, MCI non imposterà la notifica per il comando.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Mmsystem. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Messaggi MCI](mci-messages.md)
</dt> <dt>

[**pause**](pause.md)
</dt> <dt>

[**Play**](play.md)
</dt> <dt>

[**record**](record.md)
</dt> <dt>

[**riprendere**](resume.md)
</dt> <dt>

[**cercare**](seek.md)
</dt> </dl>

 

