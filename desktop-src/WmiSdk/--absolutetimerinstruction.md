---
description: Determina la generazione di un evento in una data specifica a un'ora specifica.
ms.assetid: bcb64c81-3b40-4665-a880-a100629656e0
ms.tgt_platform: multiple
title: __AbsoluteTimerInstruction classe
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
ms.openlocfilehash: 0797366a95931bec67805c9acd94e52fcab72669fe021efe6907e771a373db46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118821166"
---
# <a name="__absolutetimerinstruction-class"></a>\_\_Classe AbsoluteTimerInstruction

La **\_ \_ classe di sistema AbsoluteTimerInstruction** determina la generazione di un evento in una data specifica a un'ora specifica. Un consumer di eventi si registra per ricevere un evento timer assoluto creando un'istanza di questa classe. L'evento viene generato una volta.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

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

La **\_ \_ classe AbsoluteTimerInstruction** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **\_ \_ classe AbsoluteTimerInstruction** ha queste proprietà.

<dl> <dt>

**EventDateTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Stringa a lunghezza fissa in [formato DMTF che](date-and-time-format.md) specifica quando viene generato il timer.

</dd> <dt>

**SkipIfPassed**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se **TRUE,** l'evento timer si verifica se WMI non è in grado di generarlo all'intervallo di tempo corretto o se il consumer che richiede di ricevere l'evento non è disponibile. Se **TRUE,** l'evento non si verificherà. Il valore predefinito è **FALSE.** Quando WMI o il consumer diventa disponibile, viene generato e ricevuto un evento di notifica. Questa proprietà viene ereditata da [**\_ \_ TimerInstruction**](--timerinstruction.md).

<dt>

FALSE
</dt> <dd>

Quando WMI o il consumer diventa nuovamente disponibile, verrà generato e ricevuto un evento di notifica.

</dd> <dt>

true
</dt> <dd>

L'evento timer non si verifica se WMI non è disponibile per generarlo all'intervallo di tempo appropriato o se il consumer che richiede di ricevere l'evento non è disponibile.

</dd> </dl>

</dd> <dt>

**TimerId**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](standard-qualifiers.md)
</dt> </dl>

Stringa univoca assegnata dall'utente che identifica un evento timer specifico. Per evitare conflitti di denominazione con altri identificatori timer, è possibile usare la forma stringa di un GUID di tipo ambiente computer distribuito. Questa proprietà viene ereditata da [**\_ \_ TimerInstruction**](--timerinstruction.md).

</dd> </dl>

## <a name="remarks"></a>Commenti

La **\_ \_ classe AbsoluteTimerInstruction** è derivata da [**\_ \_ TimerInstruction**](--timerinstruction.md).

WMI genera l'evento timer assoluto creando un'istanza della [**\_ \_ classe TimerEvent.**](--timerevent.md)

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

[Ricezione di eventi temporati o ripetuti](receiving-a-timed-or-repeating-event.md)
</dt> <dt>

[Ricezione di eventi in qualsiasi momento](receiving-events-at-all-times.md)
</dt> <dt>

[Ricezione di eventi per la durata dell'applicazione](receiving-events-for-the-duration-of-your-application.md)
</dt> </dl>

 

