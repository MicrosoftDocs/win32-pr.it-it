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
ms.openlocfilehash: dbcf0f90a8bca0cf1f648f74d1b58d7037b79fa8bc9d2d13c4fe2c6dc8306eba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996521"
---
# <a name="logfileeventconsumer-class"></a>Classe LogFileEventConsumer

La **classe LogFileEventConsumer** scrive stringhe personalizzate in un file di log di testo quando gli eventi vengono recapitati. Le stringhe sono separate da sequenze di fine riga. Questa classe è uno dei consumer di eventi standard forniti da WMI. Per altre informazioni, vedere [Monitoraggio e risposta agli eventi con consumer standard.](monitoring-and-responding-to-events-with-standard-consumers.md)

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

La **classe LogFileEventConsumer** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe LogFileEventConsumer** ha queste proprietà.

<dl> <dt>

**CreatorSID**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

ID di sicurezza (SID) che identifica in modo univoco l'utente che crea un filtro. WMI archivia il SID dell'utente che crea un'istanza di [**\_ \_ EventConsumer**](--eventconsumer.md) o il SID amministratore, a seconda del sistema operativo. Per altre informazioni, vedere [Associazione di un filtro eventi con](binding-an-event-filter-with-a-logical-consumer.md) un consumer logico e Monitoraggio e Risposta agli eventi con consumer [standard.](monitoring-and-responding-to-events-with-standard-consumers.md)

Questa proprietà viene ereditata da [**\_ \_ EventConsumer.**](--eventconsumer.md)

</dd> <dt>

**Filename**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome di un file che include il percorso a cui vengono aggiunte le voci di log. Se il file non esiste, **LogFileEventConsumer** tenta di crearlo. Il consumer ha esito negativo quando il percorso non esiste o quando l'utente che crea il consumer non dispone delle autorizzazioni di scrittura per il file o il percorso.

</dd> <dt>

**IsUnicode**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se **TRUE,** il file di log è un file di testo Unicode. Se **FALSE,** il file di log è un file di testo di codice multibyte. Se il file esiste, questa proprietà viene ignorata e viene usata l'impostazione del file corrente. Ad esempio, se **IsUnicode** è **FALSE,** ma il file esistente è un file Unicode, viene usato Unicode. Se **IsUnicode** è **TRUE,** ma il file è codice multibyte, viene usato il codice multibyte.

</dd> <dt>

**MachineName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome del computer a cui Windows Management Instrumentation (WMI).

Questa proprietà viene ereditata da [**\_ \_ EventConsumer.**](--eventconsumer.md)

</dd> <dt>

**Maximumfilesize**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Dimensioni massime di un file di log in byte. Se il file primario supera le dimensioni massime, il contenuto viene spostato in un file diverso e il file primario viene svuotato. Il valore 0 (zero) indica che non esiste alcun limite di dimensioni. Il valore predefinito è 65.535 byte. Le dimensioni del file vengono controllate prima di un'operazione di scrittura. Pertanto, è possibile avere un file di dimensioni leggermente superiori al limite di dimensioni specificato. L'operazione di scrittura successiva lo intercetta e avvia un nuovo file.

L'elenco seguente identifica la struttura di denominazione per il file di backup:

-   Se il nome file originale è 8.3, l'estensione viene sostituita da una stringa nel formato "001", "002" e così via con il numero più piccolo maggiore di tutti i numeri usati e scelti in precedenza. Se si usa "999", il numero scelto è il più piccolo non usato.
-   Se il nome file originale non è 8.3, al nome del file viene aggiunta una stringa nel formato "001", "002" e così via.

Per altre informazioni sull'uso **dei valori uint64** negli script, vedere [Scripting in WMI.](/windows/desktop/WmiSdk/creating-a-wmi-script)

</dd> <dt>

**MaximumQueueSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Coda massima per un consumer specifico, in byte.

Questa proprietà viene ereditata da [**\_ \_ EventConsumer.**](--eventconsumer.md)

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **key**](key-qualifier.md)
</dt> </dl>

Nome univoco per questo consumer.

</dd> <dt>

**Text**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Modello di [stringa standard](using-standard-string-templates.md) per il testo di una voce di log.

</dd> </dl>

## <a name="remarks"></a>Commenti

> [!Note]  
> **LogFileEventConsumer** non protegge il file di log. Pertanto, quando si configura **LogFileEventConsumer**, è importante specificare una directory protetta al livello richiesto.

 

La **classe LogFileEventConsumer** è derivata dalla [**\_ \_ classe astratta EventConsumer.**](--eventconsumer.md)

## <a name="examples"></a>Esempio

Per un esempio dell'uso **di LogFileEventConsumer** per creare un consumer, vedere Scrittura in un file di [log in base a un evento](writing-to-a-log-file-based-on-an-event.md).

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

[Scrittura in un file di log in base a un evento](writing-to-a-log-file-based-on-an-event.md)
</dt> <dt>

[Creazione di un consumer logico](creating-a-logical-consumer.md)
</dt> <dt>

[Ricezione di eventi in qualsiasi momento](receiving-events-at-all-times.md)
</dt> <dt>

[**\_\_EventConsumer**](--eventconsumer.md)
</dt> </dl>

 

