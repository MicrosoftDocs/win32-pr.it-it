---
description: Ogni log nella chiave eventlog contiene sottochiavi denominate origini eventi. L'origine evento è il nome del software che registra l'evento.
ms.assetid: bc7fdc74-be41-4d17-997c-27171ef73f0f
title: Origini eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75c82c3328709a16ee7788025624a904ae7e25a21ddc83cecc9c41b27c283ab7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119914791"
---
# <a name="event-sources"></a>Origini eventi

Ogni log nella chiave [eventlog contiene](eventlog-key.md) sottochiavi denominate *origini eventi*. L'origine evento è il nome del software che registra l'evento. È spesso il nome dell'applicazione o il nome di un sottocomponente dell'applicazione se l'applicazione è di grandi dimensioni. È possibile aggiungere un massimo di 16.384 origini eventi al Registro di sistema. Il **registro di** sicurezza è solo per uso di sistema. I driver di dispositivo devono aggiungere i nomi al **registro di** sistema. Le applicazioni e i servizi devono aggiungere i nomi **al** registro applicazioni o creare un log personalizzato.

La struttura delle origini eventi è la seguente:

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
            EventLog
               Application
                  AppName
               Security
               System
                  DriverName
               CustomLog
                  AppName
```

Non è possibile usare un nome di origine già usato come nome di log. Inoltre, i nomi di origine non possono essere gerarchici. ciò significa che non possono contenere il carattere barra rovesciata (" \\ ").

Ogni origine evento contiene informazioni ( ad esempio un [file](message-files.md)di messaggio ) specifiche del software che registrare gli eventi, come illustrato nella tabella seguente.



<table>
<thead>
<tr class="header">
<th>Valore del Registro di sistema</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>CategoryCount</strong></td>
<td>Numero di categorie di eventi supportate. Questo valore è di tipo <strong>REG_DWORD</strong>.</td>
</tr>
<tr class="even">
<td><strong>CategoryMessageFile</strong></td>
<td>Percorso del file di messaggi di categoria. Un file di messaggi di categoria contiene stringhe dipendenti dalla lingua che descrivono le categorie. Questo valore può essere di tipo <strong>REG_SZ</strong> o <strong>REG_EXPAND_SZ</strong>.</td>
</tr>
<tr class="odd">
<td><strong>EventMessageFile</strong></td>
<td>Percorso di uno o più file di messaggi di evento. usare un punto e virgola per delimitare più file. Un file di messaggi di evento contiene stringhe dipendenti dalla lingua che descrivono gli eventi. Questo valore può essere di tipo <strong>REG_SZ</strong> o <strong>REG_EXPAND_SZ</strong>.</td>
</tr>
<tr class="even">
<td><strong>ParameterMessageFile</strong></td>
<td>Percorso del file di messaggi di parametro. Un file di messaggi di parametro contiene stringhe indipendenti dalla lingua che devono essere inserite nelle stringhe di descrizione dell'evento. Questo valore può essere di tipo <strong>REG_SZ</strong> o <strong>REG_EXPAND_SZ</strong>.</td>
</tr>
<tr class="odd">
<td><strong>Tipi supportati</strong></td>
<td>Maschera di bit dei tipi supportati. Questo valore è di tipo <strong>REG_DWORD</strong>. Può essere uno o più dei valori seguenti: <dl> <strong>EVENTLOG_AUDIT_FAILURE</strong> (0x0010)<br />
<strong>EVENTLOG_AUDIT_SUCCESS</strong> (0x0008)<br />
<strong>EVENTLOG_ERROR_TYPE</strong> (0x0001)<br />
<strong>EVENTLOG_INFORMATION_TYPE</strong> (0x0004)<br />
<strong>EVENTLOG_WARNING_TYPE</strong> (0x0002)<br />
</dl></td>
</tr>
</tbody>
</table>



 

Quando un'applicazione usa la [**funzione RegisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea) o [**OpenEventLog**](/windows/desktop/api/Winbase/nf-winbase-openeventloga) per ottenere un handle per un log eventi, il servizio di registrazione eventi cerca l'origine evento specificata nel Registro di sistema. Ad esempio, **il** registro applicazioni potrebbe contenere origini evento per Microsoft SQL Server e Microsoft Excel. Se un'applicazione usa [**RegisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea) o **OpenEventLog** con il nome di origine Application, SQL o Excel, il servizio di registrazione eventi restituisce un handle al **registro** applicazioni.

Un'applicazione può usare il **registro** applicazioni senza aggiungere una nuova origine evento al Registro di sistema. Se l'applicazione chiama [**RegisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea) e passa un nome di origine che non è possibile trovare nel Registro di sistema, il servizio di registrazione eventi usa il **registro** applicazioni per impostazione predefinita. Tuttavia, poiché non sono presenti file di messaggio, il Visualizzatore eventi non è in grado di eseguire il mapping di identificatori di evento o categorie di eventi a una stringa di descrizione e verrà visualizzato un errore. Per questo motivo, è necessario aggiungere un'origine evento univoca al Registro di sistema per l'applicazione e specificare un file di messaggio.

 

 



