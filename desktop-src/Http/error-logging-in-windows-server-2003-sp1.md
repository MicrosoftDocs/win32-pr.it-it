---
title: Registrazione degli errori in Windows Server 2003 SP1
description: Registrazione degli errori in Windows Server 2003 SP1
ms.assetid: 8c7fcc66-5446-4e25-8e6d-1a9260c55e36
keywords:
- Registrazione degli errori in Windows Server 2003 con Service Pack 1 (SP1)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b82c816dab39877f700973de3c0c7798034d124
ms.sourcegitcommit: 7bdca1558c21be976be950a213c5a072c449f111
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/14/2019
ms.locfileid: "103719339"
---
# <a name="error-logging-in-windows-server-2003-sp1"></a>Registrazione degli errori in Windows Server 2003 SP1

## <a name="addition-of-w3c-style-headers"></a>Aggiunta di intestazioni di stile W3C

A partire da Windows Server 2003 con Service Pack 1 (SP1), il log degli errori dell'API del server HTTP include intestazioni di stile W3C che consentono di analizzare i file di log tramite parser di log standard. Il modello riportato di seguito elenca tutti i campi che possono essere registrati nel file di log degli errori http.

``` syntax
#Software: <Name of the HTTP Server>
#Version: 1.0 <Log format version>
#Date: <Log file creation date and time>
#Fields: <date time s-computername c-ip c-port s-ip s-port cs-version
         cs-method cs-uri cs(User-Agent) cs(Cookie) cs(referrer) 
         cs-host sc-status sc-bytes cs-bytes time-taken s-siteid  
         s- reason s-queuename <header names of fields logged>

```

## <a name="logging-additional-fields"></a>Registrazione di campi aggiuntivi

Il log degli errori HTTP è stato esteso per includere nove più campi per registrare i dati sugli errori che si verificano. I nuovi campi di errore sono elencati di seguito:

-   Nome computer server \[ S-computername\]
-   CS agente utente \[ ( \_ agente utente)\]
-   Cookie \[ cs (cookie)\]
-   \[CS Referrer (referrer)\]
-   Nome host \[ cs-host\]
-   Byte ricevuti dal server \[ sc-bytes\]
-   Byte ricevuti ed elaborati dal server \[ CS-bytes\]
-   Tempo impiegato per elaborare la richiesta in \[ tempo\]
-   Queue-Name (riservato per IIS) \[ S-QueueName\]

## <a name="selecting-fileds-to-log-in-the-http-error-log-file"></a>Selezione dei file di log per l'accesso al file di log degli errori HTTP

È stata aggiunta la chiave del registro di sistema **ErrorLoggingFields** per controllare i campi registrati nel log degli errori http. I valori del registro di sistema si trovano in una \\ chiave di parametri http disponibile in:

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
      Services
         HTTP
            Parameters
```

Il valore del registro di sistema **ErrorLoggingFields** è un valore DWORD che contiene i valori di bit per ognuno dei campi che possono essere registrati. Per abilitare la registrazione di un campo specifico, impostare il valore di bit corrispondente su 1 e riavviare il servizio HTTP. Per disabilitare la registrazione, impostare il valore di bit su 0. Per configurare più campi, utilizzare un operatore OR bit per bit dei singoli valori. Ad esempio, per attivare il cookie e i campi di registrazione del referrer, il valore deve essere 0x00020000 \| 0x00040000 = 0x00060000. Se la chiave del registro di sistema **ErrorLoggingFields** è assente, vengono registrati i campi predefiniti. Il valore di **ErrorLoggingFields** per la registrazione dei campi predefiniti è 0x7c884c7. Per abilitare la registrazione per tutti i campi indicati nella tabella seguente, impostare il valore su 0x7dff4e7.

I campi di registrazione degli errori sono elencati nella tabella seguente:



| Campo log            | Registrato per impostazione predefinita | Valore bit  |
|----------------------|-------------------|------------|
| Data                 | Sì               | 0x00000001 |
| Tempo                 | Sì               | 0x00000002 |
| Nome computer server | No                | 0x00000020 |
| Indirizzo IP client    | Sì               | 0x00000004 |
| Porta client          | Sì               | 0x00400000 |
| Indirizzo IP del server    | Sì               | 0x00000040 |
| Porta server          | Sì               | 0x00008000 |
| Versione protocollo     | Sì               | 0x00080000 |
| Metodo               | Sì               | 0x00000080 |
| URI                  | Sì               | 0x00800000 |
| Agente utente           | No                | 0x00010000 |
| Cookie               | No                | 0x00020000 |
| Referrer             | No                | 0x00040000 |
| Host                 | No                | 0x00100000 |
| Stato protocollo      | Sì               | 0x00000400 |
| SC-Bytes             | No                | 0x00001000 |
| CS-Bytes             | No                | 0x00002000 |
| Tempo impiegato           | No                | 0x00004000 |
| SiteId               | Sì               | 0x01000000 |
| Frase motivo        | Sì               | 0x02000000 |
| Nome coda           | No                | 0x04000000 |
| ID flusso            | No                | 0x???????? |



 

## <a name="time-and-date-rollover"></a>Rollover di data e ora

Per impostazione predefinita, viene creato un nuovo file di log degli errori HTTP (denominato rollover dei file) quando il file di log corrente raggiunge una dimensione specificata. A partire da Windows Server 2003 con SP1, è possibile creare nuovi file di log degli errori in base alla data e all'ora. Il rollover di data e ora è controllato da due nuovi valori del registro di sistema: **ErrorLoggingRolloverType** e **ErrorLoggingLocaltimeRollover**. Per abilitare il rollover di data e ora, questi valori del registro di sistema devono essere aggiunti al registro di sistema. Il servizio HTTP deve essere riavviato quando queste chiavi vengono aggiunte al registro di sistema. Le chiavi del registro di sistema per il rollover dei file di log vengono create nella chiave seguente:

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            HTTP
               Parameters
```

La chiave del registro di sistema **ErrorLoggingRolloverType** indica il tipo di rollover desiderato e per impostazione predefinita è impostato sul rollover basato sulle dimensioni. Il rollover può anche essere impostato in modo da essere eseguito su base giornaliera, settimanale, mensile o oraria. Quando il rollover dei file è basato sul tempo, un valore **ErrorLoggingLocaltimeRollover** pari a 0 indica che il tempo di rollover è espresso in GMT e il valore 1 indica che il tempo di rollover è espresso nell'ora locale. La chiave **ErrorLoggingRolloverType** può assumere un valore compreso tra 0 e 4, come elencato nella tabella seguente.



| Valore tipo di rollover | Descrizione                                                                                                                             |
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| 0                   | Rollover basato sulle dimensioni. Viene eseguito il rollover dei file di log quando il file raggiunge le dimensioni definite nella chiave del registro di sistema **ErrorLogFileTruncateSize** . |
| 1                   | Il rollover dei file di log viene eseguito ogni giorno.                                                                                                         |
| 2                   | Il rollover dei file di log viene eseguito settimanalmente.                                                                                                        |
| 3                   | Il rollover dei file di log viene eseguito mensilmente.                                                                                                       |
| 4                   | Il rollover dei file di log viene eseguito ogni ora.                                                                                                        |



 

Le convenzioni di denominazione per i file in cui sono archiviati i log degli errori sono diverse per le dimensioni, la data e il rollover basato sull'ora. Nella tabella seguente sono elencate le convenzioni di denominazione per i file di log http.



| Tipo Tollover | Nome file di log  | Descrizione                                                                                                                         |
|---------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------|
| Dimensione          | HTTPERRn. LOG   | Il file di log viene riciclato quando raggiunge una dimensione specifica. n è il numero di file e viene incrementato quando viene eseguito il rollover del file di log. |
| Ogni giorno         | htYYMMDD. log   | Il file di log viene riciclato quotidianamente.                                                                                                     |
| Settimanale        | htYYMMww. log   | Il file di log viene riciclato settimanalmente, dove WW è la settimana del mese.                                                                 |
| Ogni mese       | htYYMM. log     | Il file di log viene riciclato ogni mese.                                                                                               |
| Ogni ora        | htYYMMDDhh. log | Il file di log viene riciclato ogni ora, dove HH è l'ora del giorno espressa in notazione di 0-24 ore.                                   |



 

 

 




