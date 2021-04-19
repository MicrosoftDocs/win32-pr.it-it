---
description: Genera eventi a intervalli, in modo analogo a un \_ messaggio del timer WM nella programmazione Windows.
ms.assetid: 0895a743-a0dd-4833-a2bf-0196369e18b9
ms.tgt_platform: multiple
title: Classe __IntervalTimerInstruction
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
ms.openlocfilehash: 20dd1c9fb2d009de4d8d957b4d5980cc6d6ff45e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317593"
---
# <a name="__intervaltimerinstruction-class"></a>\_\_Classe IntervalTimerInstruction

La classe di sistema **\_ \_ IntervalTimerInstruction** genera eventi a intervalli, in modo analogo a un \_ messaggio del timer WM nella programmazione Windows. Un consumer di eventi registra per ricevere eventi timer intervallo creando una query di eventi che fa riferimento a questa classe. A causa del comportamento del sistema operativo, non vi sono garanzie che gli eventi vengano recapitati esattamente all'intervallo richiesto.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

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

La classe **\_ \_ IntervalTimerInstruction** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **\_ \_ IntervalTimerInstruction** dispone di queste proprietà.

<dl> <dt>

**IntervalBetweenEvents**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**unità**](standard-qualifiers.md) (millisecondi)
</dt> </dl>

Numero di millisecondi tra la generazione di eventi.

</dd> <dt>

**SkipIfPassed**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se **true**, l'evento deve essere ignorato se l'intervallo è già stato superato. Il valore predefinito è **false**. Questa proprietà viene ereditata da [**\_ \_ TimerInstruction**](--timerinstruction.md).

<dt>

FALSE
</dt> <dd>

Quando WMI o il consumer diventano nuovamente disponibili, viene generato e ricevuto un evento di notifica.

</dd> <dt>

true
</dt> <dd>

L'evento timer non si verifica se WMI non è disponibile per generarlo all'intervallo di tempo appropriato oppure se il consumer che richiede la ricezione dell'evento non è disponibile.

</dd> </dl>

</dd> <dt>

**TimerId**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](standard-qualifiers.md)
</dt> </dl>

Identificatore univoco per questo oggetto **\_ \_ IntervalTimerInstruction** . Questa proprietà viene ereditata da [**\_ \_ TimerInstruction**](--timerinstruction.md).

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **\_ \_ IntervalTimerInstruction** deriva da [**\_ \_ TimerInstruction**](--timerinstruction.md).

La query di eventi immessa per la registrazione per un evento timer intervallo è in genere basata sulla proprietà **timerId** . Gli eventi di notifica generati da un evento timer intervallo contengono la proprietà **NumFirings** che contiene i dati che riflettono il numero di eventi generati durante il periodo in cui non è stato possibile ricevere gli eventi. Se **SkipIfPassed** è impostato su **true**, tali informazioni vengono ignorate.

Il valore della proprietà **IntervalBetweenEvents** deve essere ragionevolmente grande. Se è troppo piccolo, WMI potrebbe ignorarlo e non generare l'evento a causa di limitazioni in alcuni sistemi operativi.

WMI genera l'evento timer interval creando un'istanza della classe [**\_ \_ TimerEvent**](--timerevent.md) .

Per ricevere questi eventi del timer in un consumer di eventi temporaneo, eseguire [**IWbemServices:: ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) con la stringa di query di evento seguente:


```sql
SELECT * FROM __TimerEvent WHERE TimerID = "MyEvent"
```



Per ricevere questi eventi timer in un consumer di eventi permanenti, è necessario caricare la query precedente in un filtro eventi, definire un consumer logico e creare un'associazione da filtro a consumer per il filtro e il consumer. Per ulteriori informazioni, vedere [ricezione di eventi in qualsiasi momento](receiving-events-at-all-times.md).

## <a name="examples"></a>Esempio

Nella dichiarazione MOF seguente viene illustrato come generare un evento timer intervallo con la proprietà chiave impostata su "" ".


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

[Ricezione di eventi temporizzati o ripetuti](receiving-a-timed-or-repeating-event.md)
</dt> </dl>

 

