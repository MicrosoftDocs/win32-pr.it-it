---
description: La classe NTEventLogEventConsumer registra un messaggio specifico nel registro eventi del sistema operativo quando viene recapitato un evento.
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
ms.openlocfilehash: e98948688b0fee37316102b2c37039de1c139310
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879966"
---
# <a name="nteventlogeventconsumer-class"></a>Classe NTEventLogEventConsumer

La classe **NTEventLogEventConsumer** registra un messaggio specifico nel registro eventi del sistema operativo quando viene recapitato un evento. Questa classe è uno dei consumer di eventi standard forniti da WMI. Per altre informazioni, vedere [monitoraggio e risposta agli eventi con consumer standard](monitoring-and-responding-to-events-with-standard-consumers.md).

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

La classe **NTEventLogEventConsumer** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **NTEventLogEventConsumer** dispone di queste proprietà.

<dl> <dt>

**Categoria**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Categoria di eventi. Si tratta di informazioni specifiche dell'origine e possono avere qualsiasi valore.

</dd> <dt>

**CreatorSID**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **Uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

ID di sicurezza (SID) che identifica in modo univoco l'utente che crea un filtro. WMI archivia il SID dell'utente che crea un'istanza di [**\_ \_ EventConsumer**](--eventconsumer.md) o il SID Administrator, a seconda del sistema operativo. Per ulteriori informazioni, vedere [associazione di un filtro eventi a un consumer logico](binding-an-event-filter-with-a-logical-consumer.md) e [monitoraggio e risposta agli eventi con](monitoring-and-responding-to-events-with-standard-consumers.md)consumer standard.

Questa proprietà viene ereditata da [**\_ \_ EventConsumer**](--eventconsumer.md).

</dd> <dt>

**EventID**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Messaggio di evento nella DLL del messaggio. Questa proprietà non può essere **null**.

</dd> <dt>

**EventType**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Tipo di evento. Questo parametro può avere uno dei valori elencati nell'elenco seguente, definiti in Winnt. h.

<dt>

<span id="EVENTLOG_SUCCESS"></span><span id="eventlog_success"></span>

<span id="EVENTLOG_SUCCESS"></span><span id="eventlog_success"></span>**Registro eventi \_ Operazione riuscita** (0 (0x0))


</dt> <dd>

Evento riuscito

</dd> <dt>

<span id="EVENTLOG_ERROR_TPYE"></span><span id="eventlog_error_tpye"></span>

<span id="EVENTLOG_ERROR_TPYE"></span><span id="eventlog_error_tpye"></span>**Registro eventi \_ ERRORE \_ Tpye** (1 (0x1))


</dt> <dd>

Evento di errore

</dd> <dt>

<span id="EVENTLOG_WARNING_TYPE"></span><span id="eventlog_warning_type"></span>

<span id="EVENTLOG_WARNING_TYPE"></span><span id="eventlog_warning_type"></span>**Registro eventi \_ \_Tipo di avviso** (2 (0x2))


</dt> <dd>

Evento di avviso

</dd> <dt>

<span id="EVENTLOG_INFORMATION_TYPE"></span><span id="eventlog_information_type"></span>

<span id="EVENTLOG_INFORMATION_TYPE"></span><span id="eventlog_information_type"></span>**Registro eventi \_ \_Tipo di informazioni** (4 (0x4))


</dt> <dd>

Evento informativo

</dd> <dt>

<span id="EVENTLOG_AUDIT_SUCCESS"></span><span id="eventlog_audit_success"></span>

<span id="EVENTLOG_AUDIT_SUCCESS"></span><span id="eventlog_audit_success"></span>**Registro eventi \_ CONTROLLO \_ riuscito** (8 (0x8))


</dt> <dd>

Tipo di controllo con esito positivo

</dd> <dt>

<span id="EVENTLOG_AUDIT_FAILURE"></span><span id="eventlog_audit_failure"></span>

<span id="EVENTLOG_AUDIT_FAILURE"></span><span id="eventlog_audit_failure"></span>**Registro eventi \_ \_Errore di controllo** (16 (0x10))


</dt> <dd>

Tipo di controllo errore

</dd> </dl>

</dd> <dt>

**InsertionStringTemplates**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Matrice di modelli di stringa standard utilizzata come stringa di inserimento per un record del log eventi.

</dd> <dt>

**MachineName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome del computer a cui Strumentazione gestione Windows (WMI) Invia gli eventi.

Questa proprietà viene ereditata da [**\_ \_ EventConsumer**](--eventconsumer.md).

</dd> <dt>

**MaximumQueueSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero massimo di code per un consumer specifico, in byte.

Questa proprietà viene ereditata da [**\_ \_ EventConsumer**](--eventconsumer.md).

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](key-qualifier.md)
</dt> </dl>

Nome univoco di un consumer.

</dd> <dt>

**NameOfRawDataProperty**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome della proprietà dell'evento che contiene i dati da passare al parametro *lpRawData* della funzione [**ReportEvent**](/windows/desktop/api/winbase/nf-winbase-reporteventa) .

</dd> <dt>

**NameOfUserSidProperty**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome della proprietà dell'evento che contiene un ID di sicurezza (SID) da passare al parametro *lpUserSid* della funzione [**ReportEvent**](/windows/desktop/api/winbase/nf-winbase-reporteventa) . La proprietà deve essere una matrice di byte (**Uint8**) o una stringa. Se si tratta di una matrice di byte, si presuppone che sia un SID. Se è una stringa, si tratta di un SID di stringa convertito in un SID.

</dd> <dt>

**NumberOfInsertionStrings**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero di elementi nella matrice **InsertionStringTemplates** .

</dd> <dt>

**SourceName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome dell'origine in cui si trova un messaggio. Si presuppone che il cliente abbia registrato una DLL con i messaggi necessari.

> [!Note]  
> Il valore di questo parametro non deve includere i due punti (:) carattere.

 

</dd> <dt>

**UNCServerName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome del computer in cui registrare un evento o **null** se l'evento deve essere registrato in un server locale.

Per impostazione predefinita, gli utenti autenticati non possono registrare gli eventi nel registro applicazioni in un computer remoto. Di conseguenza, l'utilizzo di questa proprietà per specificare un computer remoto non funzionerà. Per informazioni su come modificare la sicurezza del registro eventi, vedere l' [articolo della Knowledge Knowledge](https://support.microsoft.com/kb/323076).

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **NTEventLogEventConsumer** è derivata dalla classe astratta [**\_ \_ EventConsumer**](--eventconsumer.md) .

## <a name="examples"></a>Esempio

Per un esempio dell'uso di **NTEventLogEventConsumer** per creare un consumer, vedere [registrazione nel registro eventi NT in base a un evento](logging-to-nt-event-log-based-on-an-event.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\Sottoscrizione radice<br/>                                                           |
| MOF<br/>                      | <dl> <dt>Wbemcons. mof</dt> </dl> |
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

 

