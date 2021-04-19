---
description: Ogni log della chiave EventLog contiene sottochiavi denominate origini eventi. L'origine evento è il nome del software che registra l'evento.
ms.assetid: bc7fdc74-be41-4d17-997c-27171ef73f0f
title: Origini eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab2b408b76cdbc6e93e44099fea2842f9655a963
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310816"
---
# <a name="event-sources"></a>Origini eventi

Ogni log della [chiave EventLog](eventlog-key.md) contiene sottochiavi denominate *origini eventi*. L'origine evento è il nome del software che registra l'evento. Spesso è il nome dell'applicazione o il nome di un sottocomponente dell'applicazione, se l'applicazione è di grandi dimensioni. È possibile aggiungere al registro di sistema un massimo di 16.384 origini evento. Il registro di **sicurezza** è solo per uso del sistema. I driver di dispositivo devono aggiungere i nomi al registro di **sistema** . Le applicazioni e i servizi devono aggiungere i nomi al registro **applicazioni** o creare un log personalizzato.

La struttura delle origini evento è la seguente:

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

Non è possibile usare un nome di origine già usato come nome di log. Inoltre, i nomi di origine non possono essere gerarchici; ovvero non possono contenere il carattere barra rovesciata (" \\ ").

Ogni origine evento contiene informazioni, ad esempio un [file di messaggio](message-files.md), specifiche del software che registrerà gli eventi, come illustrato nella tabella seguente.



<table>
<thead>
<tr class="header">
<th>Valore del registro di sistema</th>
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
<td>Percorso del file di messaggio di categoria. Un file di messaggio di categoria contiene stringhe dipendenti dalla lingua che descrivono le categorie. Questo valore può essere di tipo <strong>REG_SZ</strong> o <strong>REG_EXPAND_SZ</strong>.</td>
</tr>
<tr class="odd">
<td><strong>EventMessageFile</strong></td>
<td>Percorso di uno o più file di messaggio di evento; utilizzare un punto e virgola per delimitare più file. Un file di messaggio di evento contiene stringhe dipendenti dalla lingua che descrivono gli eventi. Questo valore può essere di tipo <strong>REG_SZ</strong> o <strong>REG_EXPAND_SZ</strong>.</td>
</tr>
<tr class="even">
<td><strong>ParameterMessageFile</strong></td>
<td>Percorso del file dei messaggi di parametro. Un file di messaggi di parametro contiene stringhe indipendenti dalla lingua da inserire nelle stringhe di descrizione dell'evento. Questo valore può essere di tipo <strong>REG_SZ</strong> o <strong>REG_EXPAND_SZ</strong>.</td>
</tr>
<tr class="odd">
<td><strong>TypesSupported</strong></td>
<td>Maschera di maschera dei tipi supportati. Questo valore è di tipo <strong>REG_DWORD</strong>. Può essere uno o più dei valori seguenti: <dl> <strong>EVENTLOG_AUDIT_FAILURE</strong> (0x0010)<br />
<strong>EVENTLOG_AUDIT_SUCCESS</strong> (0x0008)<br />
<strong>EVENTLOG_ERROR_TYPE</strong> (0x0001)<br />
<strong>EVENTLOG_INFORMATION_TYPE</strong> (0x0004)<br />
<strong>EVENTLOG_WARNING_TYPE</strong> (0x0002)<br />
</dl></td>
</tr>
</tbody>
</table>



 

Quando un'applicazione usa la funzione [**RegisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea) o [**OpenEventLog**](/windows/desktop/api/Winbase/nf-winbase-openeventloga) per ottenere un handle per un log eventi, il servizio di registrazione eventi cerca l'origine eventi specificata nel registro di sistema. Ad esempio, il registro **applicazioni** potrebbe contenere origini eventi per Microsoft SQL Server e Microsoft Excel. Se un'applicazione utilizza [**RegisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea) o **OpenEventLog** con il nome di origine dell'applicazione, SQL o Excel, il servizio di registrazione eventi restituisce un handle al registro **applicazioni** .

Un'applicazione può usare il registro **applicazioni** senza aggiungere una nuova origine evento al registro di sistema. Se l'applicazione chiama [**RegisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea) e passa un nome di origine che non è possibile trovare nel registro di sistema, per impostazione predefinita il servizio di registrazione eventi usa il registro **applicazioni** . Tuttavia, poiché non sono presenti file di messaggi, il Visualizzatore eventi non è in grado di eseguire il mapping di qualsiasi identificatore di evento o categoria di eventi a una stringa di descrizione e verrà visualizzato un errore. Per questo motivo, è necessario aggiungere un'origine evento univoca al registro di sistema per l'applicazione e specificare un file di messaggio.

 

 



