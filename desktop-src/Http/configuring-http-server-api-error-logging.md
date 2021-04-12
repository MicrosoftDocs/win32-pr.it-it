---
title: Configurazione della registrazione degli errori dell'API del server HTTP
description: La registrazione degli errori dell'API del server HTTP è controllata da tre valori del registro di sistema in una \\ chiave di parametri http.
ms.assetid: a7712159-939e-42e3-a8d8-73148c2f4f6e
keywords:
- API server HTTP, configurazione dei log degli errori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 698f6b5ae81b1933ea745789e0fae33dfc7ebce6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395931"
---
# <a name="configuring-http-server-api-error-logging"></a>Configurazione della registrazione degli errori dell'API del server HTTP

La registrazione degli errori dell'API del server http è controllata da tre valori del registro di sistema in una chiave di \\ **parametri** http disponibile in:

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            HTTP
               Parameters
```

> [!Note]  
> Il percorso e il formato dei valori di configurazione possono cambiare nelle versioni future del sistema operativo Windows.

 

Un utente deve disporre dei privilegi di amministratore/sistema locale per modificare i valori del registro di sistema e visualizzare o modificare i file di log e la cartella che li contiene.

Le informazioni di configurazione nei valori del registro di sistema vengono lette all'avvio del driver dell'API del server HTTP. Di conseguenza, se le impostazioni vengono modificate, il driver deve essere arrestato e riavviato per leggere i nuovi valori. Questa operazione può essere eseguita usando i comandi seguenti della console:

**NET stop http**

**NET start http**

I file di log vengono denominati usando la convenzione seguente:

**HTTPERR +** *SequenceNumber* **+. log**

Ad esempio: "httperr4. log".

I file di log vengono ciclati quando raggiungono la dimensione massima specificata dal valore del registro di sistema **ErrorLogFileTruncateSize** e il valore non può essere minore di un megabyte (MB).

Se la configurazione della registrazione degli errori non è valida o si verifica un qualsiasi tipo di errore durante la scrittura nei file di log, l'API del server HTTP usa la registrazione degli eventi per notificare agli amministratori che la registrazione degli errori non è stata eseguita.

Nella tabella seguente sono descritti i valori di configurazione del registro di sistema.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valore del registro di sistema</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="EnableErrorLogging"></span><span id="enableerrorlogging"></span><span id="ENABLEERRORLOGGING"></span>EnableErrorLogging<br/></td>
<td><strong>Valore DWORD</strong> che può essere impostato su <strong>true</strong> per abilitare la registrazione degli errori oppure <strong>false</strong> per disabilitarlo. Il valore predefinito è <strong>true</strong>.<br/></td>
</tr>
<tr class="even">
<td><span id="ErrorLogFileTruncateSize"></span><span id="errorlogfiletruncatesize"></span><span id="ERRORLOGFILETRUNCATESIZE"></span>ErrorLogFileTruncateSize<br/></td>
<td><strong>Valore DWORD</strong> che specifica la dimensione massima in byte del file di log degli errori. Il valore predefinito è 1 MB (0x100000).<br/>
<blockquote>
[!Note]<br />
Il valore specificato non può essere minore del valore predefinito.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ErrorLoggingDir"></span><span id="errorloggingdir"></span><span id="ERRORLOGGINGDIR"></span>ErrorLoggingDir<br/></td>
<td><strong>Stringa</strong> che specifica la cartella in cui l'API del server http inserisce i file di registrazione. <br/> L'API server HTTP crea una sottocartella denominata &quot; HTTPERR nella &quot; cartella specificata in cui vengono inseriti i file di log. Questa sottocartella e i file di log ricevono le stesse impostazioni di autorizzazione, il che significa che gli account amministratore e di sistema locale hanno accesso completo, mentre altri utenti non hanno accesso.<br/> Se una cartella non è specificata nel registro di sistema, la cartella predefinita è la seguente:<br/> &quot;%SystemRoot%\System32\LogFiles&quot;<br/>
<blockquote>
[!Note]<br />
Il valore della stringa ErrorLoggingDir deve essere un percorso completo, ma può contenere &quot; % systemroot% &quot; .
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

 

 





