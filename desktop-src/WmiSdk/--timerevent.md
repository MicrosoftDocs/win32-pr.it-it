---
description: Segnala un evento generato da WMI in risposta a una richiesta degli utenti per un evento timer intervallo o un evento timer assoluto.
ms.assetid: 5ae29312-cfda-42c9-a154-e5bb31819be0
ms.tgt_platform: multiple
title: Classe __TimerEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __TimerEvent
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 2de8967110568e968bb241ebbf4942bf1504b332
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319315"
---
# <a name="__timerevent-class"></a>\_\_Classe TimerEvent

La classe di sistema **\_ \_ TimerEvent** segnala un evento generato da WMI in risposta alla richiesta di un utente per un evento timer intervallo o un evento timer assoluto. Un evento timer intervallo è un evento che si verifica a intervalli regolari. Un evento timer assoluto è un evento che si verifica in un momento specifico. Gli eventi del timer possono verificarsi in qualsiasi spazio dei nomi.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class __TimerEvent : __Event
{
  uint32 NumFirings;
  uint8  SECURITY_DESCRIPTOR[];
  string TimerId;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a>Members

La classe **\_ \_ TimerEvent** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **\_ \_ TimerEvent** dispone di queste proprietà.

<dl> <dt>

**NumFirings**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero di volte in cui l'evento si è verificato prima del recapito di una notifica al consumer.

</dd> <dt>

**descrittore di sicurezza \_**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **Uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrittore utilizzato dal provider di eventi per determinare gli utenti che possono ricevere l'evento. Questa proprietà viene ereditata dall' [**\_ \_ evento**](--event.md).

</dd> <dt>

**ORA di \_ creazione**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Valore univoco che indica l'ora in cui è stato generato l'evento. Si tratta di un valore a 64 bit che rappresenta il numero di intervalli di 100-nanosecondi dopo il 1 ° gennaio 1601. Le informazioni sono nel formato UTC (Coordinated Universal Time). Questa proprietà viene ereditata dall' [**\_ \_ evento**](--event.md).

Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> <dt>

**TimerId**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Istanza della sottoclasse [**\_ \_ TimerInstruction**](--timerinstruction.md) che ha causato l'attivazione di questo evento da parte di WMI. I consumer specificano un'identificazione del timer nella proprietà **timerId** della sottoclasse **\_ \_ TimerInstruction** creata per la registrazione.

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **\_ \_ TimerEvent** è derivata dall' [**\_ \_ evento**](--event.md).

I consumer di eventi registrano un evento timer assoluto creando un'istanza della classe di sistema [**\_ \_ AbsoluteTimerInstruction**](--absolutetimerinstruction.md) . Si registrano per un evento timer intervallo creando un'istanza della classe di sistema [**\_ \_ IntervalTimerInstruction**](--intervaltimerinstruction.md) .

Durante il normale funzionamento, la proprietà **NumFirings** è impostata su 1. Quando non è possibile raggiungere l'utente o l'intervallo di attivazione è molto più rapido della possibilità di recapitare l'evento, **NumFirings** è impostato su un numero maggiore di 1. Quando **NumFirings** è maggiore di 1, WMI unisce automaticamente molti eventi timer nello stesso evento. Questa Unione è simile a ciò che accade con i messaggi del [**\_ timer WM**](/windows/desktop/winmsg/wm-timer) nella programmazione Windows.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>       |
| Server minimo supportato<br/> | Windows Server 2008<br/> |
| Spazio dei nomi<br/>                | Tutti gli spazi dei nomi WMI<br/>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_\_Evento**](/windows/desktop/WmiSdk/--event)
</dt> <dt>

[Classi di sistema WMI](wmi-system-classes.md)
</dt> <dt>

[Ricezione di eventi temporizzati o ripetuti](receiving-a-timed-or-repeating-event.md)
</dt> <dt>

[Ricezione di eventi in qualsiasi momento](receiving-events-at-all-times.md)
</dt> <dt>

[Ricezione di eventi per la durata dell'applicazione](receiving-events-for-the-duration-of-your-application.md)
</dt> </dl>

 

