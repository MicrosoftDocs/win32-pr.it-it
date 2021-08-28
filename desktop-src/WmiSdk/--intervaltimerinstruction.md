---
description: Genera eventi a intervalli, in modo analogo a un messaggio WM \_ TIMER Windows programmazione.
ms.assetid: 0895a743-a0dd-4833-a2bf-0196369e18b9
ms.tgt_platform: multiple
title: __IntervalTimerInstruction classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __IntervalTimerInstruction
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 17f0c55edceb3c5fb009f49ae97e3765ec3e0255a82f8c75e133344379c24d90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640761"
---
# <a name="__intervaltimerinstruction-class"></a>\_\_Classe IntervalTimerInstruction

La **\_ \_ classe di sistema IntervalTimerInstruction** genera eventi a intervalli, in modo simile a un messaggio WM \_ TIMER Windows programmazione. Un consumer di eventi si registra per ricevere eventi timer di intervallo creando una query di eventi che fa riferimento a questa classe. A causa del comportamento del sistema operativo, non ci sono garanzie che gli eventi verranno recapitati esattamente all'intervallo richiesto.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class __IntervalTimerInstruction : __TimerInstruction
{
  uint32  IntervalBetweenEvents;
  boolean SkipIfPassed = FALSE;
  string  TimerId;
};
```

## <a name="members"></a>Members

La **\_ \_ classe IntervalTimerInstruction** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **\_ \_ classe IntervalTimerInstruction** ha queste proprietà.

<dl> <dt>

**IntervalBetweenEvents**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**unità**](standard-qualifiers.md) (millisecondi)
</dt> </dl>

Numero di millisecondi tra la generazione di eventi.

</dd> <dt>

**SkipIfPassed**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se **TRUE,** questo evento deve essere ignorato se l'intervallo è già passato. Il valore predefinito è **FALSE.** Questa proprietà viene ereditata da [**\_ \_ TimerInstruction.**](--timerinstruction.md)

<dt>

FALSE
</dt> <dd>

Quando WMI o il consumer diventano nuovamente disponibili, verrà generato e ricevuto un evento di notifica.

</dd> <dt>

true
</dt> <dd>

L'evento timer non si verifica se WMI non è disponibile per generarlo all'intervallo di tempo appropriato o se il consumer che richiede di ricevere l'evento non è disponibile.

</dd> </dl>

</dd> <dt>

**TimerId**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **Chiave**](standard-qualifiers.md)
</dt> </dl>

Identificatore univoco per **\_ \_ questo oggetto IntervalTimerInstruction.** Questa proprietà viene ereditata da [**\_ \_ TimerInstruction.**](--timerinstruction.md)

</dd> </dl>

## <a name="remarks"></a>Commenti

La **\_ \_ classe IntervalTimerInstruction** è derivata da [**\_ \_ TimerInstruction.**](--timerinstruction.md)

La query di evento immessa per la registrazione per un evento timer a intervalli è in genere basata sulla **proprietà TimerId.** Gli eventi di notifica generati da un evento timer a intervalli contengono la proprietà **NumFirings** che contiene dati che riflettono il numero di eventi generati durante l'impossibilità di ricevere gli eventi. Se **SkipIfPassed è** impostato su **TRUE,** le informazioni vengono rimosse.

Il valore della **proprietà IntervalBetweenEvents** deve essere ragionevolmente grande. Se è troppo piccolo, WMI potrebbe ignorarlo e non generare l'evento a causa di limitazioni in alcuni sistemi operativi.

WMI genera l'evento timer intervallo creando un'istanza della [**\_ \_ classe TimerEvent.**](--timerevent.md)

Per ricevere questi eventi timer in un consumer di eventi temporaneo, eseguire [**IWbemServices::ExecNotificationQuery con**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) la stringa di query dell'evento seguente:


```sql
SELECT * FROM __TimerEvent WHERE TimerID = "MyEvent"
```



Per ricevere questi eventi timer in un consumer di eventi permanente, è necessario caricare la query precedente in un filtro eventi, definire un consumer logico e creare un'associazione da filtro a consumer per il filtro e il consumer. Per altre informazioni, vedere [Ricezione di eventi in qualsiasi momento.](receiving-events-at-all-times.md)

## <a name="examples"></a>Esempio

La dichiarazione MOF seguente illustra come generare un evento timer di intervallo con la proprietà key impostata su "MyEvent" ogni 10 secondi:


```mof
instance of __IntervalTimerInstruction
{
  TimerId = "MyEvent";     // inherited from __TimerInstruction
  SkipIfPassed = FALSE;    // also inherited
  IntervalBetweenEvents = 10000;
};
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>       |
| Server minimo supportato<br/> | Windows Server 2008<br/> |
| Spazio dei nomi<br/>                | Tutti gli spazi dei nomi WMI<br/>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_\_TimerInstruction**](/windows/desktop/WmiSdk/--timerinstruction)
</dt> <dt>

[Classi di sistema WMI](wmi-system-classes.md)
</dt> <dt>

[Ricezione di eventi programmati o ripetuti](receiving-a-timed-or-repeating-event.md)
</dt> </dl>

 

