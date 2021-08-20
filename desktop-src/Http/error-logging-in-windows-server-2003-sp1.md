---
title: Registrazione degli errori in Windows Server 2003 SP1
description: Registrazione degli errori in Windows Server 2003 SP1
ms.assetid: 8c7fcc66-5446-4e25-8e6d-1a9260c55e36
keywords:
- Registrazione degli errori in Windows Server 2003 con Service Pack 1 (SP1)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a71d5a84dfba8ecb9a78ed38d3ad112f0820e6b578bce77e189e5047a25f458b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014809"
---
# <a name="error-logging-in-windows-server-2003-sp1"></a>Registrazione degli errori in Windows Server 2003 SP1

## <a name="addition-of-w3c-style-headers"></a>Aggiunta di intestazioni di stile W3C

A partire da Windows Server 2003 con Service Pack 1 (SP1), il log degli errori dell'API server HTTP include intestazioni di stile W3C che consentono l'analisi dei file di log tramite parser di log standard. Il modello illustrato di seguito elenca tutti i campi che possono essere registrati nel file di log degli errori HTTP.

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

Il log degli errori HTTP è stato esteso per includere altri nove campi per registrare i dati sugli errori che si verificano. I nuovi campi di errore sono elencati di seguito:

-   Nome computer server \[ S-COMPUTERNAME\]
-   Agente utente \[ CS (USER \_ AGENT)\]
-   Cookie \[ CS(COOKIE)\]
-   referrer \[ CS(referrer)\]
-   Nome host \[ CS-HOST\]
-   Byte ricevuti dal server \[ SC-BYTES\]
-   Byte ricevuti ed elaborati dal server \[ CS-BYTES\]
-   Tempo impiegato per elaborare la richiesta \[ TIME-TAKEN\]
-   Queue-Name (riservato per IIS) \[ S-QUEUENAME\]

## <a name="selecting-fileds-to-log-in-the-http-error-log-file"></a>Selezione dei file da registrare nel file di log degli errori HTTP

La chiave del Registro di sistema **ErrorLoggingFields** è stata aggiunta per controllare i campi registrati nel log degli errori HTTP. Questi valori del Registro di sistema si trovano in una chiave dei parametri HTTP \\ disponibile in:

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
      Services
         HTTP
            Parameters
```

Il valore del Registro di sistema **ErrorLoggingFields** è un valore DWORD che contiene valori di bit per ognuno dei campi che possono essere registrati. Per abilitare la registrazione di un campo specifico, impostare il valore di bit corrispondente su 1 e riavviare il servizio HTTP. Per disabilitare la registrazione, impostare il valore in bit su 0. Per configurare più campi, usare un'operazione OR bit per bit dei singoli valori. Ad esempio, per attivare i campi di registrazione Cookie e Referrer, il valore deve essere 0x00020000 \| 0x00040000 = 0x00060000. Se la chiave del Registro di sistema **ErrorLoggingFields** è assente, vengono registrati i campi predefiniti. Il **valore ErrorLoggingFields** per registrare i campi predefiniti è 0x7c884c7. Per abilitare la registrazione per tutti i campi illustrati nella tabella seguente, impostare il valore su 0x7dff4e7.

I campi di registrazione degli errori sono elencati nella tabella seguente:



| Campo Log            | Registrato per impostazione predefinita | Valore bit  |
|----------------------|-------------------|------------|
| Data                 | Sì               | 0x00000001 |
| Ora                 | Sì               | 0x00000002 |
| Nome computer server | No                | 0x00000020 |
| Indirizzo IP client    | Sì               | 0x00000004 |
| Porta client          | Sì               | 0x00400000 |
| Indirizzo IP del server    | Sì               | 0x00000040 |
| Porta server          | Sì               | 0x00008000 |
| Versione del protocollo     | Sì               | 0x00080000 |
| Metodo               | Sì               | 0x00000080 |
| URI                  | Sì               | 0x00800000 |
| Agente utente           | No                | 0x00010000 |
| Cookie               | No                | 0x00020000 |
| Referrer             | No                | 0x00040000 |
| Host                 | No                | 0x00100000 |
| Stato del protocollo      | Sì               | 0x00000400 |
| SC-Bytes             | No                | 0x00001000 |
| CS-Bytes             | No                | 0x00002000 |
| Tempo impiegato           | No                | 0x00004000 |
| Siteid               | Sì               | 0x01000000 |
| Frase del motivo        | Sì               | 0x02000000 |
| Nome coda           | No                | 0x04000000 |
| ID flusso            | No                | 0x???????? |



 

## <a name="time-and-date-rollover"></a>Rollover di data e ora

Per impostazione predefinita, viene creato un nuovo file di log degli errori HTTP (operazione di rollover del file) quando il file di log corrente raggiunge una dimensione specificata. A partire da Windows Server 2003 con SP1, è possibile creare nuovi file di log degli errori in base alla data e all'ora. Il rollover di data e ora è controllato da due nuovi valori del Registro di sistema: **ErrorLoggingRolloverType** e **ErrorLoggingLocaltimeRollover.** Per abilitare il rollover di data e ora, questi valori del Registro di sistema devono essere aggiunti al Registro di sistema. Il servizio Http deve essere riavviato quando queste chiavi vengono aggiunte al Registro di sistema. Le chiavi del Registro di sistema di rollover del file di log vengono create nella chiave seguente:

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            HTTP
               Parameters
```

La chiave del Registro di sistema **ErrorLoggingRolloverType** indica il tipo di rollover desiderato ed è impostata per impostazione predefinita sul rollover basato sulle dimensioni. È anche possibile impostare il rollover su base giornaliera, settimanale, mensile o oraria. Quando il rollover dei file è basato sull'ora, un valore **ErrorLoggingLocaltimeRollover** pari a 0 indica che l'ora di rollover è espressa in GMT e il valore 1 indica che l'ora di rollover è espressa nell'ora locale. La **chiave ErrorLoggingRolloverType** può assumere un valore compreso tra 0 e 4, come indicato nella tabella seguente.



| Valore del tipo di rollover | Descrizione                                                                                                                             |
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| 0                   | Rollover basato sulle dimensioni. Il roll over dei file di log viene eseguito quando il file raggiunge le dimensioni definite nella chiave del Registro di sistema **ErrorLogFileTruncateSize.** |
| 1                   | Il rollover dei file di log viene eseguito ogni giorno.                                                                                                         |
| 2                   | Il rollover dei file di log viene eseguito settimanalmente.                                                                                                        |
| 3                   | Il rollover dei file di log viene eseguito ogni mese.                                                                                                       |
| 4                   | Il rollover del file di log viene eseguito ogni ora.                                                                                                        |



 

Le convenzioni di denominazione per i file in cui sono archiviati i log degli errori sono diverse per il rollover basato su dimensioni, data e ora. Nella tabella seguente sono elencate le convenzioni di denominazione per i file di log HTTP.



| Tipo di tollover | Nome file di log  | Descrizione                                                                                                                         |
|---------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------|
| Dimensione          | HTTPERRn.LOG   | Il file di log viene riciclato quando raggiunge dimensioni specifiche. n è il numero di file e viene incrementato quando viene eseguito il roll over del file di log. |
| Ogni giorno         | htYYMMDD.log   | Il file di log viene riciclato ogni giorno.                                                                                                     |
| Settimanale        | htYYMMww.log   | Il file di log viene riciclato settimanalmente, dove ww è la settimana del mese.                                                                 |
| Mensile       | htYYMM.log     | Il file di log viene riciclato ogni mese.                                                                                               |
| Ogni ora        | htYYMMDDhh.log | Il file di log viene riciclato ogni ora, dove hh è l'ora del giorno espressa in notazione da 0 a 24 ore.                                   |



 

 

 




