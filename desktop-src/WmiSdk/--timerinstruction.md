---
description: Specifica le istruzioni sulla modalità di generazione degli eventi timer per i consumer.
ms.assetid: b08edb25-bedf-4014-a835-4050f5749479
ms.tgt_platform: multiple
title: __TimerInstruction classe
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
ms.openlocfilehash: d9081cef3ed58929fa976470b1c567c6accd0f60029f64f28ee7a90d16600d2d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132014"
---
# <a name="__timerinstruction-class"></a>\_\_Classe TimerInstruction

La classe di sistema astratta **\_ \_ TimerInstruction** specifica le istruzioni sulla modalità di generazione degli eventi [timer](receiving-a-timed-or-repeating-event.md) per i consumer.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

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

La **\_ \_ classe TimerInstruction** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **\_ \_ classe TimerInstruction** ha queste proprietà.

<dl> <dt>

**SkipIfPassed**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrive se verrà generato e ricevuto un evento di notifica quando un consumer diventa disponibile.

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

Stringa univoca assegnata dall'utente che identifica questo particolare evento timer. Per evitare conflitti di denominazione con altri identificatori timer, è possibile usare la forma stringa di un GUID di tipo DCE (Distributed Computer Environment). Questa proprietà fa parte [**\_ \_ dell'istanza di TimerEvent**](--timerevent.md) che rappresenta l'evento.

</dd> </dl>

## <a name="remarks"></a>Commenti

La **\_ \_ classe TimerInstruction** è derivata da [**\_ \_ EventGenerator**](--eventgenerator.md).

Le **\_ \_ sottoclassi TimerInstruction** sono [**\_ \_ AbsoluteTimerInstruction**](--absolutetimerinstruction.md), usate dai consumer per la registrazione per un evento timer assoluto, e [**\_ \_ IntervalTimerInstruction**](--intervaltimerinstruction.md), usate per la registrazione per un evento timer intervallo.

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

 

