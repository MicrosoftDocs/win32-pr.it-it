---
title: SSL in modalità kernel
description: SSL in modalità kernel
ms.assetid: ada82704-cb7d-4e98-8c87-76c7bfbd098b
keywords:
- SSL in modalità kernel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 737ac7c6c25bac6e7b66d91aa967fc6fa550459b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298821"
---
# <a name="kernel-mode-ssl"></a>SSL in modalità kernel

La modalità kernel SSL è stata introdotta in Windows Server 2003 con Service Pack 1 (SP1) con supporto limitato. Per i computer in cui è in esecuzione Windows Server 2003 con SP1, è necessario impostare una chiave del registro di sistema per abilitare il kernel SSL. Per i computer che eseguono Windows Server 2008 e Windows Vista, è disponibile il supporto completo della modalità kernel per SSL.

Nelle sezioni seguenti viene descritto il supporto SSL in modalità kernel:

-   Modalità kernel SSL in Windows Server 2003 con SP1
-   SSL in modalità kernel in Windows Server 2008 e Windows Vista

## <a name="kernel-modes-ssl-in-windows-server-2003-with-sp1"></a>Modalità kernel SSL in Windows Server 2003 con SP1

In Windows Server 2003 con SP1, l'API server HTTP fornisce la possibilità di eseguire la protezione SSL in modalità kernel (l'impostazione predefinita è SSL in modalità utente). La funzionalità modalità kernel migliora le prestazioni SSL spostando le operazioni di crittografia e decrittografia nel kernel, riducendo così il numero di transizioni tra la modalità kernel e la modalità utente.

Le funzionalità seguenti non sono supportate quando SSL viene eseguito in modalità kernel:

-   Certificati client
-   Crittografie RC2
-   Protocollo PCT 1,0
-   Le modifiche alla configurazione del certificato server richiedono il riavvio del servizio HTTP
-   Supporto per la crittografia e l'offload bulk

## <a name="configuring-kernel-mode-ssl"></a>Configurazione di SSL in modalità kernel

Il protocollo SSL in modalità kernel è controllato dal valore del registro di sistema **EnableKernelSSL** e viene abilitato impostando il valore su 1. L'abilitazione di SSL in modalità kernel Disabilita SSL in modalità utente e richiede il riavvio del servizio HTTP per renderlo effettivo. La chiave del registro di sistema **EnableKernelSSL** si trova in:

**HKEY \_ \_** \\  \\  \\  \\  \\ **Parametri** http dei servizi \\  CurrentControlSet del sistema del computer locale EnableKernelSSL

## <a name="kernel-mode-ssl-in-windows-server-2008-and-windows-vista"></a>SSL in modalità kernel in Windows Server 2008 e Windows Vista

Per i computer che eseguono Windows Server 2008 e Windows Vista, l'API server HTTP offre funzionalità SSL avanzate.

Sono supportate le seguenti nuove funzionalità:

-   Supporto completo del certificato client in modalità kernel SSL
-   SSL in modalità kernel per tutte le transazioni SSL HTTP
-   Supporto per la crittografia e l'offload bulk
-   Protocollo PCT 1,0
-   Crittografie RC2
-   Miglioramento delle prestazioni in modalità utente SSL

## <a name="configuration"></a>Configurazione

La modalità kernel SSL può essere configurata tramite due valori del registro di sistema nella chiave Parameters HTTP disponibile in:

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            HTTP
               Parameters
                  EnableSslCloseNotify
                  DisableSslCertChainCacheOnlyUrlRetrieval
```

Un utente deve disporre dei privilegi di amministratore/sistema locale per modificare i valori del registro di sistema e visualizzare o modificare i file di log e la cartella che li contiene.

Le informazioni di configurazione nei valori del registro di sistema vengono lette all'avvio del driver dell'API del server HTTP. Di conseguenza, se le impostazioni vengono modificate, il driver deve essere arrestato e riavviato per leggere i nuovi valori. Questa operazione può essere eseguita usando i comandi seguenti della console:

**NET stop http**

**NET start http**

Nella tabella seguente sono elencati i valori di configurazione del registro di sistema.



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
<td>EnableKernelSSL</td>
<td><strong>Windows Server 2008 e Windows Vista:</strong> Questo valore del registro di sistema è obsoleto.<br/></td>
</tr>
<tr class="even">
<td>EnableSslCloseNotify</td>
<td>Valore <strong>DWORD</strong> impostato su <strong>true</strong> per abilitare la notifica di chiusura o <strong>false</strong> per disabilitare il requisito di chiusura della notifica. Close-Notify è disabilitato per impostazione predefinita.<br/> Quando Close-Notify è abilitato, è necessario che l'applicazione client invii un messaggio di notifica di chiusura prima di chiudere le connessioni TCP. L'API server HTTP invia anche una notifica di chiusura prima di chiudere la connessione.<br/> Quando Close-Notify è abilitato e il client invia un messaggio di notifica di chiusura, l'API server HTTP riutilizzerà la sessione SSL nelle future connessioni al client. Se il client non invia una notifica di chiusura, l'API del server HTTP non riutilizzerà la stessa sessione SSL per le connessioni future. Pertanto, un handshake SSL completo viene attivato sulla nuova connessione, riducendo così le prestazioni. <br/>
<blockquote>
[!Note]<br />
L'abilitazione di Close-Notify contribuisce a ridurre gli attacchi di troncamento contro le richieste e le risposte HTTPS.
</blockquote>
<br/> <br/> Quando Close-Notify è disabilitato, l'API server HTTP riutilizza la sessione SSL per le connessioni future.<br/></td>
</tr>
<tr class="odd">
<td>DisableSslCertChainCacheOnlyUrlRetrieval</td>
<td>Valore <strong>DWORD</strong> impostato su <strong>true</strong> per consentire all'API del server http di recuperare i certificati intermedi da Internet o dall'archivio locale oppure <strong>false</strong> per recuperare i certificati intermedi solo dall'archivio locale. Il valore predefinito del registro di sistema è <strong>false</strong>.<br/> Per impostazione predefinita, l'API server HTTP compila una catena di certificati client recuperando i certificati intermedi dall'archivio Autorità di certificazione intermedio nell'account del computer locale. L'impostazione di questo valore su <strong>true</strong> consente all'API del server http di recuperare i certificati intermedi non solo dall'archivio locale, ma anche dall'autorità di certificazione intermedia su Internet.<br/></td>
</tr>
</tbody>
</table>



 

 

 





