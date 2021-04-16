---
description: Specifica le istruzioni per la generazione di eventi timer per i consumer.
ms.assetid: b08edb25-bedf-4014-a835-4050f5749479
ms.tgt_platform: multiple
title: Classe __TimerInstruction
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __TimerInstruction
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 5c6bbbf905a141fb7e9e3621c78709fd78999393
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350096"
---
# <a name="__timerinstruction-class"></a>\_\_Classe TimerInstruction

La classe di sistema astratta **\_ \_ TimerInstruction** specifica le istruzioni per la generazione di [eventi timer](receiving-a-timed-or-repeating-event.md) per i consumer.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[abstract]
class __TimerInstruction : __EventGenerator
{
  boolean SkipIfPassed = FALSE;
  string  TimerId;
};
```

## <a name="members"></a>Members

La classe **\_ \_ TimerInstruction** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **\_ \_ TimerInstruction** dispone di queste proprietà.

<dl> <dt>

**SkipIfPassed**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrive se verrà generato un evento di notifica e che riceverà quando un consumer diventerà disponibile.

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

Stringa univoca assegnata dall'utente che identifica questo particolare evento del timer. Per evitare conflitti di denominazione con altri identificatori del timer, è possibile usare il formato stringa di un GUID di tipo DCE (Distributed computer Environment). Questa proprietà fa parte dell'istanza di [**\_ \_ TimerEvent**](--timerevent.md) che rappresenta l'evento.

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **\_ \_ TimerInstruction** deriva da [**\_ \_ EventGenerator**](--eventgenerator.md).

Le sottoclassi **\_ \_ TimerInstruction** sono [**\_ \_ AbsoluteTimerInstruction**](--absolutetimerinstruction.md), utilizzate dai consumer per la registrazione per un evento timer assoluto e [**\_ \_ IntervalTimerInstruction**](--intervaltimerinstruction.md), utilizzate per la registrazione per un evento timer intervallo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>       |
| Server minimo supportato<br/> | Windows Server 2008<br/> |
| Spazio dei nomi<br/>                | Tutti gli spazi dei nomi WMI<br/>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_\_EventGenerator**](/windows/desktop/WmiSdk/--eventgenerator)
</dt> <dt>

[Classi di sistema WMI](wmi-system-classes.md)
</dt> </dl>

 

