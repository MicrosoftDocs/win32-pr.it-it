---
description: La classe SMTPEventConsumer Invia un messaggio di posta elettronica utilizzando Simple Mail Transfer Protocol (SMTP) ogni volta che viene recapitato un evento.
ms.assetid: 42178360-9e22-4cd1-9b72-5f6b0d7e6c9c
ms.tgt_platform: multiple
title: Classe SMTPEventConsumer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SMTPEventConsumer
- SMTPEventConsumer.CreatorSID
- SMTPEventConsumer.MachineName
- SMTPEventConsumer.MaximumQueueSize
- SMTPEventConsumer.BccLine
- SMTPEventConsumer.CcLine
- SMTPEventConsumer.FromLine
- SMTPEventConsumer.HeaderFields
- SMTPEventConsumer.Message
- SMTPEventConsumer.Name
- SMTPEventConsumer.ReplyToLine
- SMTPEventConsumer.SMTPServer
- SMTPEventConsumer.Subject
- SMTPEventConsumer.ToLine
api_type:
- DllExport
api_location:
- Smtpcons.dll
ms.openlocfilehash: 76c7fad3b5cb4bbf6c3c0c03689607ba64fbcc67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233810"
---
# <a name="smtpeventconsumer-class"></a>Classe SMTPEventConsumer

La classe **SMTPEventConsumer** Invia un messaggio di posta elettronica utilizzando Simple Mail Transfer Protocol (SMTP) ogni volta che viene recapitato un evento. Un server SMTP deve esistere sulla rete. La classe SMTPEventConsumer non supporta gli allegati. La codifica del messaggio di posta elettronica deve essere US-ASCII.

Questa classe è uno dei consumer di eventi standard forniti da WMI. Per un esempio dell'uso di **SMTPEventConsumer** per creare un consumer, vedere [invio di messaggi di posta elettronica in base a un evento](sending-e-mail-based-on-an-event.md). Per altre informazioni, vedere [monitoraggio e risposta agli eventi con consumer standard](monitoring-and-responding-to-events-with-standard-consumers.md).

La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate. Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[AMENDMENT]
class SMTPEventConsumer : __EventConsumer
{
  uint8  CreatorSID[];
  string MachineName;
  uint32 MaximumQueueSize;
  string BccLine;
  string CcLine;
  string FromLine;
  string HeaderFields[];
  string Message;
  string Name;
  string ReplyToLine;
  string SMTPServer;
  string Subject;
  string ToLine;
};
```

## <a name="members"></a>Members

La classe **SMTPEventConsumer** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **SMTPEventConsumer** dispone di queste proprietà.

<dl> <dt>

**BccLine**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Elenco di indirizzi, separati da virgola o punto e virgola, nel formato di un modello di stringa standard a cui il messaggio viene inviato come copia nascosta. Per ulteriori informazioni, vedere la sezione Osservazioni di questo argomento.

</dd> <dt>

**CcLine**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Elenco di indirizzi, separati da una virgola o un punto e virgola, nel formato di un modello di stringa standard a cui il messaggio viene inviato come copia carbone. Per ulteriori informazioni, vedere la sezione Osservazioni di questo argomento.

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

**FromLine**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Dalla riga di un messaggio di posta elettronica nel formato di un modello di stringa standard. Se è **null**, una riga da viene costruita nel formato "WinMgmt@*machineName*".

</dd> <dt>

**HeaderFields**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Matrice di campi di intestazione che vengono inseriti in un messaggio di posta elettronica senza interpretazione.

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

**Messaggio**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Modello di stringa standard che contiene il corpo di un messaggio di posta elettronica.

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](key-qualifier.md)
</dt> </dl>

Identificatore univoco del consumer di eventi.

</dd> <dt>

**ReplyToLine**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Risposta alla riga di un messaggio di posta elettronica nel formato di un modello di stringa standard. Se è **null**, non viene utilizzata alcuna riga di risposta.

</dd> <dt>

**SMTPServer**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome del server SMTP tramite il quale viene inviato un messaggio di posta elettronica. I nomi consentiti sono un indirizzo IP o un nome DNS o NetBIOS. Questa proprietà non può essere **null**.

</dd> <dt>

**Oggetto**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Modello di stringa standard che contiene l'oggetto di un messaggio di posta elettronica.

</dd> <dt>

**ToLine**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Elenco di indirizzi, separati da virgola o punto e virgola, nel formato di un modello di stringa standard che identifica la posizione in cui deve essere inviato il messaggio. Per ulteriori informazioni, vedere la sezione Osservazioni di questo argomento.

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe SMTPEventConsumer è derivata dalla classe astratta [**\_ \_ EventConsumer**](--eventconsumer.md) .

Alcune delle proprietà **ToLine**, **CcLine** o **BccLine** possono essere **null**, ma non tutte possono essere **null**.

La ricezione di un codice di errore restituito dal servizio SMTP viene considerata un errore.

## <a name="examples"></a>Esempio

Per un esempio dell'uso di **SMTPEventConsumer** per creare un consumer, vedere [invio di messaggi di posta elettronica in base a un evento](sending-e-mail-based-on-an-event.md). Per altre informazioni, vedere [monitoraggio e risposta agli eventi con consumer standard](monitoring-and-responding-to-events-with-standard-consumers.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\Sottoscrizione radice<br/>                                                           |
| MOF<br/>                      | <dl> <dt>Smtpcons. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Smtpcons.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_\_EventConsumer**](--eventconsumer.md)
</dt> <dt>

[Classi consumer standard](standard-consumer-classes.md)
</dt> <dt>

[Invio di messaggi di posta elettronica in base a un evento](sending-e-mail-based-on-an-event.md)
</dt> <dt>

[Creazione di un consumer logico](creating-a-logical-consumer.md)
</dt> <dt>

[Ricezione di eventi in qualsiasi momento](receiving-events-at-all-times.md)
</dt> </dl>

 

 




