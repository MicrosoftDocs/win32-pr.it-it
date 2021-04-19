---
description: Causa la generazione di un evento in una data specifica in un momento specifico.
ms.assetid: bcb64c81-3b40-4665-a880-a100629656e0
ms.tgt_platform: multiple
title: Classe __AbsoluteTimerInstruction
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __AbsoluteTimerInstruction
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 5f4f55e635e42ec34e9b3558a0784d319e4d91ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319808"
---
# <a name="__absolutetimerinstruction-class"></a>\_\_Classe AbsoluteTimerInstruction

La classe di sistema **\_ \_ AbsoluteTimerInstruction** causa la generazione di un evento in una data specifica in un momento specifico. Un consumer di eventi registra per ricevere un evento timer assoluto creando un'istanza di questa classe. L'evento viene generato una sola volta.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class __AbsoluteTimerInstruction : __TimerInstruction
{
  datetime EventDateTime;
  boolean  SkipIfPassed = FALSE;
  string   TimerId;
};
```

## <a name="members"></a>Members

La classe **\_ \_ AbsoluteTimerInstruction** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **\_ \_ AbsoluteTimerInstruction** dispone di queste proprietà.

<dl> <dt>

**EventDateTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Stringa a lunghezza fissa nel [formato DMTF](date-and-time-format.md) che specifica quando il timer viene attivato.

</dd> <dt>

**SkipIfPassed**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se **true**, l'evento timer si verifica se WMI non è in grado di generarlo all'intervallo di tempo corretto oppure se il consumer che richiede la ricezione dell'evento non è disponibile. Se **true**, l'evento non si verificherà. Il valore predefinito è **false**. Quando WMI o il consumer diventano disponibili, viene generato e ricevuto un evento di notifica. Questa proprietà viene ereditata da [**\_ \_ TimerInstruction**](--timerinstruction.md).

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

Stringa univoca assegnata dall'utente che identifica un evento timer specifico. Per evitare conflitti di denominazione con altri identificatori del timer, è possibile utilizzare il formato stringa di un GUID di stile dell'ambiente del computer distribuito. Questa proprietà viene ereditata da [**\_ \_ TimerInstruction**](--timerinstruction.md).

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **\_ \_ AbsoluteTimerInstruction** deriva da [**\_ \_ TimerInstruction**](--timerinstruction.md).

WMI genera l'evento del timer assoluto creando un'istanza della classe [**\_ \_ TimerEvent**](--timerevent.md) .

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
</dt> <dt>

[Ricezione di eventi in qualsiasi momento](receiving-events-at-all-times.md)
</dt> <dt>

[Ricezione di eventi per la durata dell'applicazione](receiving-events-for-the-duration-of-your-application.md)
</dt> </dl>

 

