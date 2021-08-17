---
title: Configurazione della registrazione degli errori dell'API del server HTTP
description: La registrazione degli errori dell'API del server HTTP è controllata da tre valori del Registro di sistema in una chiave \\ parametri HTTP.
ms.assetid: a7712159-939e-42e3-a8d8-73148c2f4f6e
keywords:
- API server HTTP, configurazione dei log degli errori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a10479a1b2bd1ebf559213b6cd4b738f6c0b9ea63c142edcce3c10f64f877dda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950890"
---
# <a name="configuring-http-server-api-error-logging"></a>Configurazione della registrazione degli errori dell'API del server HTTP

La registrazione degli errori dell'API server HTTP è controllata da tre valori del Registro di sistema in una **chiave parametri HTTP** che si \\  trova in:

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            HTTP
               Parameters
```

> [!Note]  
> Il percorso e la forma dei valori di configurazione possono cambiare nelle versioni future del Windows operativo.

 

Un utente deve disporre dei privilegi di amministratore/sistema locale per modificare i valori del Registro di sistema e visualizzare o modificare i file di log e la cartella che li contiene.

Le informazioni di configurazione nei valori del Registro di sistema vengono lette all'avvio del driver API del server HTTP. Di conseguenza, se le impostazioni vengono modificate, il driver deve essere arrestato e riavviato per leggere i nuovi valori. Questa operazione può essere eseguita usando i comandi della console seguenti:

**net stop http**

**net start http**

I file di log vengono denominati usando la convenzione seguente:

**httperr +** *SequenceNumber* **+ .log**

Ad esempio: "httperr4.log".

I file di log vengono ciclici quando raggiungono le dimensioni massime specificate dal valore del Registro di sistema **ErrorLogFileTruncateSize** e il valore non può essere inferiore a un megabyte (MB).

Se la configurazione della registrazione degli errori non è valida o si verifica qualsiasi tipo di errore durante la scrittura nei file di log, l'API server HTTP usa la registrazione eventi per notificare agli amministratori che la registrazione degli errori non è stata eseguita.

I valori di configurazione del Registro di sistema sono descritti nella tabella seguente.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valore del Registro di sistema</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="EnableErrorLogging"></span><span id="enableerrorlogging"></span><span id="ENABLEERRORLOGGING"></span>EnableErrorLogging<br/></td>
<td>Valore <strong>DWORD che</strong> può essere impostato su <strong>TRUE per</strong> abilitare la registrazione degli errori o <strong>FALSE</strong> per disabilitarla. Il valore predefinito è <strong>TRUE.</strong><br/></td>
</tr>
<tr class="even">
<td><span id="ErrorLogFileTruncateSize"></span><span id="errorlogfiletruncatesize"></span><span id="ERRORLOGFILETRUNCATESIZE"></span>ErrorLogFileTruncateSize<br/></td>
<td>Valore <strong>DWORD che</strong> specifica le dimensioni massime in byte di un file di log degli errori. Il valore predefinito è 1 MB (0x100000).<br/>
<blockquote>
[!Note]<br />
Il valore specificato non può essere minore del valore predefinito.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ErrorLoggingDir"></span><span id="errorloggingdir"></span><span id="ERRORLOGGINGDIR"></span>ErrorLoggingDir<br/></td>
<td>Valore <strong>String che</strong> specifica la cartella in cui l'API del server HTTP inserisce i file di registrazione. <br/> L'API server HTTP crea una sottocartella denominata HTTPERR nella cartella specificata in cui vengono inseriti &quot; &quot; i file di log. Questa sottocartella e i file di log ricevono le stesse impostazioni di autorizzazione, ovvero gli account amministratore e di sistema locale hanno accesso completo, mentre altri utenti non hanno accesso.<br/> Se non viene specificata una cartella nel Registro di sistema, la cartella predefinita è la seguente:<br/> &quot;%SystemRoot%\System32\LogFiles&quot;<br/>
<blockquote>
[!Note]<br />
Il valore della stringa ErrorLoggingDir deve essere un percorso completo, ma può contenere &quot; %SystemRoot% &quot; .
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

 

 





