---
title: MM_MCINOTIFY messaggio (Mmsystem.h)
description: Il messaggio MM \_ MCINOTIFY notifica a un'applicazione che un dispositivo MCI ha completato un'operazione. I dispositivi MCI inviano questo messaggio solo quando viene usato \_ il flag MCI NOTIFY.
ms.assetid: a0840130-2969-4ce5-b098-3e45401eebb1
keywords:
- MM_MCINOTIFY messaggio Windows Multimediali
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
ms.openlocfilehash: fc03ab0406542472871f35ca3ff619d4d9a6f35725b9322a4c11bc73bc29a5aa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807511"
---
# <a name="mm_mcinotify-message"></a>MM \_ MCINOTIFY message

Il **messaggio MM \_ MCINOTIFY** notifica a un'applicazione che un dispositivo MCI ha completato un'operazione. I dispositivi MCI inviano questo messaggio solo quando viene usato \_ il flag MCI NOTIFY.


```C++
MM_MCINOTIFY 
wParam = (WPARAM) wFlags 
lParam = (LONG) lDevID
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="wFlags"></span><span id="wflags"></span><span id="WFLAGS"></span>*Wflags*
</dt> <dd>

Motivo della notifica. Vengono definiti i valori seguenti:



| Requisito | Valore |
|-------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| NOTIFICA MCI \_ \_ INTERROTTA    | Il dispositivo ha ricevuto un comando che ha impedito il rispetto delle condizioni correnti per l'avvio della funzione di callback. Se un nuovo comando interrompe il comando corrente e richiede anche la notifica, il dispositivo invia solo questo messaggio e non MCI \_ NOTIFY \_ SUPERSEDED |
| MCI \_ NOTIFY \_ FAILURE    | Si è verificato un errore del dispositivo durante l'esecuzione del comando.                                                                                                                                                                                                            |
| NOTIFICA MCI \_ \_ RIUSCITA | Le condizioni che avviano la funzione di callback sono state soddisfatte.                                                                                                                                                                                                                 |
| MCI \_ NOTIFY \_ SUPERSEDED | Il dispositivo ha ricevuto un altro comando con il flag "notify" impostato e le condizioni correnti per l'avvio della funzione di callback sono state sostituite.                                                                                                                           |



 

</dd> <dt>

<span id="lDevID"></span><span id="ldevid"></span><span id="LDEVID"></span>*lDevID*
</dt> <dd>

Identificatore del dispositivo che avvia la funzione di callback.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore in caso contrario.

## <a name="remarks"></a>Commenti

Per altre informazioni sul flag MCI \_ NOTIFY, vedere [Flag Notify](the-notify-flag.md).

Un dispositivo restituisce il flag MCI \_ NOTIFY SUCCESSFUL con MM \_ **\_ MCINOTIFY** al termine dell'azione per un comando. Ad esempio, un dispositivo audio CD usa questo flag per la notifica per il comando [**play**](play.md) ( [**MCI \_ PLAY**](mci-play.md)) al termine della riproduzione del dispositivo. Il **comando** di riproduzione ha esito positivo solo quando raggiunge la posizione finale specificata o raggiunge la fine del contenuto multimediale. Analogamente, i comandi [**seek**](seek.md) ( [**MCI \_ SEEK**](mci-seek.md)) e [**record**](record.md) ( MCI RECORD ) non restituiscono [**MCI \_**](mci-record.md)NOTIFY SUCCESSFUL finché non raggiungono la posizione finale specificata o non raggiungono la fine \_ del \_ supporto.

Un dispositivo restituisce il flag MCI NOTIFY ABORTED con \_ \_ MM **\_ MCINOTIFY** solo quando riceve un comando che ne impedisce il rispetto delle condizioni di notifica. Ad esempio, il [**comando play**](play.md) non  interrompe la notifica per un comando di riproduzione precedente a condizione che il nuovo comando non cambi la direzione di riproduzione o cambi la posizione finale. I [**comandi seek**](seek.md) e [**record**](record.md) si comportano in modo analogo. MCI non invia inoltre MCI NOTIFY ABORTED quando la riproduzione o la registrazione viene sospesa con il \_ \_ comando [**pause**](pause.md) ( [**MCI \_ PAUSE).**](mci-pause.md) [**L'invio del comando resume**](resume.md) ( [**MCI \_ RESUME**](mci-resume.md)) consente di continuare a soddisfare le condizioni di callback.

Quando l'applicazione richiede una notifica per un comando, controllare la restituzione dell'errore delle funzioni [**mciSendString**](/previous-versions//dd757161(v=vs.85)) o [**mciSendCommand.**](/previous-versions//dd757160(v=vs.85)) Se queste funzioni rilevano un errore e restituiscono un valore diverso da zero, MCI non imposta la notifica per il comando.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Mmsystem.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Mci](mci.md)
</dt> <dt>

[Messaggi MCI](mci-messages.md)
</dt> <dt>

[**Pausa**](pause.md)
</dt> <dt>

[**Giocare**](play.md)
</dt> <dt>

[**Registrazione**](record.md)
</dt> <dt>

[**riassumere**](resume.md)
</dt> <dt>

[**Cercare**](seek.md)
</dt> </dl>

 

