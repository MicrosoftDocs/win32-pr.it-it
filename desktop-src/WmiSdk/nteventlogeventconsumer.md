---
description: La classe NTEventLogEventConsumer registra un messaggio specifico nel registro eventi del sistema operativo quando vi viene recapitato un evento.
ms.assetid: cf986812-f09a-4f32-ba76-db76a23e2e4c
ms.tgt_platform: multiple
title: Classe NTEventLogEventConsumer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NTEventLogEventConsumer
- NTEventLogEventConsumer.CreatorSID
- NTEventLogEventConsumer.MachineName
- NTEventLogEventConsumer.MaximumQueueSize
- NTEventLogEventConsumer.Category
- NTEventLogEventConsumer.NameOfRawDataProperty
- NTEventLogEventConsumer.EventID
- NTEventLogEventConsumer.EventType
- NTEventLogEventConsumer.InsertionStringTemplates
- NTEventLogEventConsumer.Name
- NTEventLogEventConsumer.NumberOfInsertionStrings
- NTEventLogEventConsumer.NameOfUserSidProperty
- NTEventLogEventConsumer.SourceName
- NTEventLogEventConsumer.UNCServerName
api_type:
- DllExport
api_location:
- Wbemcons.dll
ms.openlocfilehash: dfa2a1dcf15b65808af758820604df6aa62d7bc59d4e1c69e8d4d6e06b1d93a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118555171"
---
# <a name="nteventlogeventconsumer-class"></a>Classe NTEventLogEventConsumer

La **classe NTEventLogEventConsumer** registra un messaggio specifico nel registro eventi del sistema operativo quando vi viene recapitato un evento. Questa classe è uno dei consumer di eventi standard forniti da WMI. Per altre informazioni, vedere [Monitoraggio e risposta agli eventi con consumer standard.](monitoring-and-responding-to-events-with-standard-consumers.md)

## <a name="syntax"></a>Sintassi

``` syntax
[AMENDMENT]
class NTEventLogEventConsumer : __EventConsumer
{
  uint8  CreatorSID[];
  string MachineName;
  uint32 MaximumQueueSize;
  uint16 Category;
  string NameOfRawDataProperty;
  uint32 EventID;
  uint32 EventType = 1;
  string InsertionStringTemplates[] = {""};
  string Name;
  uint32 NumberOfInsertionStrings = 0;
  string NameOfUserSidProperty;
  string SourceName;
  string UNCServerName;
};
```

## <a name="members"></a>Members

La **classe NTEventLogEventConsumer** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe NTEventLogEventConsumer** ha queste proprietà.

<dl> <dt>

**Categoria**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Categoria di eventi. Si tratta di informazioni specifiche dell'origine e possono avere qualsiasi valore.

</dd> <dt>

**CreatorSID**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Identificatore di sicurezza (SID) che identifica in modo univoco l'utente che crea un filtro. WMI archivia il SID dell'utente che crea un'istanza di [**\_ \_ EventConsumer**](--eventconsumer.md) o del SID amministratore, a seconda del sistema operativo. Per altre informazioni, vedere [Associazione di un filtro eventi a](binding-an-event-filter-with-a-logical-consumer.md) un consumer logico e Monitoraggio e Risposta agli eventi con consumer [standard](monitoring-and-responding-to-events-with-standard-consumers.md).

Questa proprietà viene ereditata da [**\_ \_ EventConsumer**](--eventconsumer.md).

</dd> <dt>

**EventID**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Messaggio di evento nella DLL del messaggio. Questa proprietà non può essere **NULL.**

</dd> <dt>

**EventType**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Tipo di evento. Questo parametro può avere uno dei valori elencati nell'elenco seguente, definiti in Winnt.h.

<dt>

<span id="EVENTLOG_SUCCESS"></span><span id="eventlog_success"></span>

<span id="EVENTLOG_SUCCESS"></span><span id="eventlog_success"></span>**EVENTLOG \_ SUCCESS** (0 (0x0))


</dt> <dd>

Evento successful

</dd> <dt>

<span id="EVENTLOG_ERROR_TPYE"></span><span id="eventlog_error_tpye"></span>

<span id="EVENTLOG_ERROR_TPYE"></span><span id="eventlog_error_tpye"></span>**EVENTLOG \_ ERRORE \_ TPYE** (1 (0x1))


</dt> <dd>

Evento di errore

</dd> <dt>

<span id="EVENTLOG_WARNING_TYPE"></span><span id="eventlog_warning_type"></span>

<span id="EVENTLOG_WARNING_TYPE"></span><span id="eventlog_warning_type"></span>**EVENTLOG \_ TIPO \_ DI AVVISO** (2 (0x2))


</dt> <dd>

Evento di avviso

</dd> <dt>

<span id="EVENTLOG_INFORMATION_TYPE"></span><span id="eventlog_information_type"></span>

<span id="EVENTLOG_INFORMATION_TYPE"></span><span id="eventlog_information_type"></span>**EVENTLOG \_ TIPO \_ DI INFORMAZIONI** (4 (0x4))


</dt> <dd>

Evento di informazioni

</dd> <dt>

<span id="EVENTLOG_AUDIT_SUCCESS"></span><span id="eventlog_audit_success"></span>

<span id="EVENTLOG_AUDIT_SUCCESS"></span><span id="eventlog_audit_success"></span>**EVENTLOG \_ AUDIT \_ SUCCESS** (8 (0x8))


</dt> <dd>

Tipo di controllo operazione riuscita

</dd> <dt>

<span id="EVENTLOG_AUDIT_FAILURE"></span><span id="eventlog_audit_failure"></span>

<span id="EVENTLOG_AUDIT_FAILURE"></span><span id="eventlog_audit_failure"></span>**EVENTLOG \_ AUDIT \_ FAILURE** (16 (0x10))


</dt> <dd>

Tipo di controllo degli errori

</dd> </dl>

</dd> <dt>

**Oggetti InsertionStringTemplates**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Matrice di modelli di stringa standard utilizzati come stringa di inserimento per un record del log eventi.

</dd> <dt>

**MachineName**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome del computer a cui Windows Management Instrumentation (WMI).

Questa proprietà viene ereditata da [**\_ \_ EventConsumer**](--eventconsumer.md).

</dd> <dt>

**MaximumQueueSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Coda massima per un consumer specifico, in byte.

Questa proprietà viene ereditata da [**\_ \_ EventConsumer**](--eventconsumer.md).

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](key-qualifier.md)
</dt> </dl>

Nome univoco di un consumer.

</dd> <dt>

**NameOfRawDataProperty**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome della proprietà dell'evento che contiene i dati da passare al parametro *lpRawData* della funzione [**ReportEvent.**](/windows/desktop/api/winbase/nf-winbase-reporteventa)

</dd> <dt>

**NameOfUserSidProperty**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome della proprietà dell'evento che contiene un ID di sicurezza (SID) da passare al parametro *lpUserSid* della funzione [**ReportEvent.**](/windows/desktop/api/winbase/nf-winbase-reporteventa) La proprietà deve essere una matrice di byte (**uint8**) o una stringa. Se è una matrice di byte, si presuppone che sia un SID. Se è una stringa, si tratta di un SID di stringa convertito in un SID.

</dd> <dt>

**NumberOfInsertionStrings**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero di elementi nella matrice **InsertionStringTemplates.**

</dd> <dt>

**SourceName**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome dell'origine in cui si trova un messaggio. Si presuppone che il cliente abbia registrato una DLL con i messaggi necessari.

> [!Note]  
> Il valore di questo parametro non deve includere i due punti (:) Carattere.

 

</dd> <dt>

**UNCServerName**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome del computer in cui registrare un evento oppure **NULL** se l'evento deve essere registrato in un server locale.

Per impostazione predefinita, gli utenti autenticati non possono registrare gli eventi nel registro applicazioni in un computer remoto. Di conseguenza, l'uso di questa proprietà per specificare un computer remoto non funzionerà. Per informazioni su come modificare la sicurezza del registro eventi, vedere questo [articolo della Knowledge Base.](https://support.microsoft.com/kb/323076)

</dd> </dl>

## <a name="remarks"></a>Commenti

La **classe NTEventLogEventConsumer** deriva dalla [**\_ \_ classe astratta EventConsumer.**](--eventconsumer.md)

## <a name="examples"></a>Esempio

Per un esempio dell'uso **di NTEventLogEventConsumer** per creare un consumer, vedere Registrazione nel registro eventi [NT in base a un evento](logging-to-nt-event-log-based-on-an-event.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | Sottoscrizione \\ radice<br/>                                                           |
| MOF<br/>                      | <dl> <dt>Wbemcons.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemcons.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Classi consumer standard](standard-consumer-classes.md)
</dt> <dt>

[Creazione di un consumer logico](creating-a-logical-consumer.md)
</dt> <dt>

[Ricezione di eventi in qualsiasi momento](receiving-events-at-all-times.md)
</dt> <dt>

[**\_\_EventConsumer**](--eventconsumer.md)
</dt> </dl>

 

