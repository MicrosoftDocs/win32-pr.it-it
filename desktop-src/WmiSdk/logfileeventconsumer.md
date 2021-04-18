---
description: La classe LogFileEventConsumer scrive stringhe personalizzate in un file di log di testo quando gli eventi vengono recapitati.
ms.assetid: 8934b60e-3763-4b85-89fd-58fe6136dff6
ms.tgt_platform: multiple
title: Classe LogFileEventConsumer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LogFileEventConsumer
- LogFileEventConsumer.CreatorSID
- LogFileEventConsumer.MachineName
- LogFileEventConsumer.MaximumQueueSize
- LogFileEventConsumer.Filename
- LogFileEventConsumer.IsUnicode
- LogFileEventConsumer.MaximumFileSize
- LogFileEventConsumer.Name
- LogFileEventConsumer.Text
api_type:
- DllExport
api_location:
- Wbemcons.dll
ms.openlocfilehash: 462989b740aaf6a6bd78968c951b7c676038cea5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310342"
---
# <a name="logfileeventconsumer-class"></a>Classe LogFileEventConsumer

La classe **LogFileEventConsumer** scrive stringhe personalizzate in un file di log di testo quando gli eventi vengono recapitati. Le stringhe sono separate dalle sequenze di fine riga. Questa classe è uno dei consumer di eventi standard forniti da WMI. Per altre informazioni, vedere [monitoraggio e risposta agli eventi con consumer standard](monitoring-and-responding-to-events-with-standard-consumers.md).

## <a name="syntax"></a>Sintassi

``` syntax
[AMENDMENT]
class LogFileEventConsumer : __EventConsumer
{
  uint8   CreatorSID[];
  string  MachineName;
  uint32  MaximumQueueSize;
  string  Filename;
  boolean IsUnicode;
  uint64  MaximumFileSize = 65535;
  string  Name;
  string  Text;
};
```

## <a name="members"></a>Members

La classe **LogFileEventConsumer** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **LogFileEventConsumer** dispone di queste proprietà.

<dl> <dt>

**CreatorSID**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **Uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

ID di sicurezza (SID) che identifica in modo univoco l'utente che crea un filtro. WMI archivia il SID dell'utente che crea un'istanza di [**\_ \_ EventConsumer**](--eventconsumer.md) o il SID Administrator, a seconda del sistema operativo. Per ulteriori informazioni, vedere [associazione di un filtro eventi a un consumer logico](binding-an-event-filter-with-a-logical-consumer.md) e [monitoraggio e risposta agli eventi con](monitoring-and-responding-to-events-with-standard-consumers.md)consumer standard.

Questa proprietà viene ereditata da [**\_ \_ EventConsumer**](--eventconsumer.md).

</dd> <dt>

**Filename**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome di un file che include il percorso a cui vengono accodate le voci di log. Se il file non esiste, **LogFileEventConsumer** tenta di crearlo. Il consumer ha esito negativo quando il percorso non esiste o quando l'utente che crea il consumer non dispone delle autorizzazioni di scrittura per il file o il percorso.

</dd> <dt>

**Unicode**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se **true**, il file di log è un file di testo Unicode. Se **false**, il file di log è un file di testo di codice multibyte. Se il file esiste, questa proprietà viene ignorata e viene utilizzata l'impostazione del file corrente. Se, ad esempio, il valore **di Unicode è** **false**, ma il file esistente è un file Unicode, viene utilizzato Unicode. Se la codifica è **true**, ma il file è di tipo multibyte **, viene utilizzato** il codice multibyte.

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

**MaximumFileSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Dimensioni massime di un file di log in byte. Se il file primario supera la dimensione massima, il contenuto viene spostato in un altro file e il file primario viene svuotato. Il valore 0 (zero) indica che non è previsto alcun limite per le dimensioni. Il valore predefinito è 65.535 byte. Le dimensioni del file vengono verificate prima di un'operazione di scrittura. Pertanto, è possibile avere un file leggermente più grande del limite di dimensioni specificato. L'operazione di scrittura successiva la intercetta e avvia un nuovo file.

L'elenco seguente identifica la struttura di denominazione per il file di backup:

-   Se il nome file originale è 8,3, l'estensione viene sostituita da una stringa nel formato "001", "002" e così via con il numero più piccolo maggiore di tutti i numeri scelti e usati in precedenza. Se si usa "999", il numero scelto è il numero inutilizzato più piccolo.
-   Se il nome file originale non è 8,3, viene aggiunta una stringa nel formato "001", "002" e così via al nome del file.

Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

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

Nome univoco del consumer.

</dd> <dt>

**Text**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

[Modello](using-standard-string-templates.md) di stringa standard per il testo di una voce di log.

</dd> </dl>

## <a name="remarks"></a>Commenti

> [!Note]  
> Il **LogFileEventConsumer** non protegge il file di log. Pertanto, quando si configura **LogFileEventConsumer**, è importante specificare una directory protetta per il livello richiesto.

 

La classe **LogFileEventConsumer** è derivata dalla classe astratta [**\_ \_ EventConsumer**](--eventconsumer.md) .

## <a name="examples"></a>Esempio

Per un esempio dell'uso di **LogFileEventConsumer** per creare un consumer, vedere [scrittura in un file di log in base a un evento](writing-to-a-log-file-based-on-an-event.md).

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

[Scrittura in un file di log in base a un evento](writing-to-a-log-file-based-on-an-event.md)
</dt> <dt>

[Creazione di un consumer logico](creating-a-logical-consumer.md)
</dt> <dt>

[Ricezione di eventi in qualsiasi momento](receiving-events-at-all-times.md)
</dt> <dt>

[**\_\_EventConsumer**](--eventconsumer.md)
</dt> </dl>

 

