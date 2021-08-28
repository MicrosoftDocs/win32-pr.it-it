---
title: SSL in modalità kernel
description: SSL in modalità kernel
ms.assetid: ada82704-cb7d-4e98-8c87-76c7bfbd098b
keywords:
- SSL in modalità kernel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdfbc66e72f4e3e79c53207cbe9f4b77d3887b36
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475497"
---
# <a name="kernel-mode-ssl"></a>SSL in modalità kernel

Ssl in modalità kernel è stato introdotto in Windows Server 2003 con Service Pack 1 (SP1) con supporto limitato. Per i computer che eseguono Windows Server 2003 con SP1, è necessario impostare una chiave del Registro di sistema per abilitare SSL del kernel. Per i computer che eseguono Windows Server 2008 e Windows Vista, viene fornito il supporto completo della modalità kernel per SSL.

Le sezioni seguenti descrivono il supporto SSL in modalità kernel:

-   Modalità kernel SSL in Windows Server 2003 con SP1
-   SSL in modalità kernel in Windows Server 2008 e Windows Vista

## <a name="kernel-modes-ssl-in-windows-server-2003-with-sp1"></a>Modalità kernel SSL in Windows Server 2003 con SP1

In Windows Server 2003 con SP1, l'API server HTTP offre la possibilità di eseguire la sicurezza SSL in modalità kernel (ssl in modalità utente è l'impostazione predefinita). La funzionalità modalità kernel migliora le prestazioni SSL spostando le operazioni di crittografia e decrittografia nel kernel, riducendo così il numero di transizioni tra la modalità kernel e la modalità utente.

Le funzionalità seguenti non sono supportate quando SSL viene eseguito in modalità kernel:

-   Certificati client
-   Crittografia RC2
-   Protocollo PCT 1.0
-   Le modifiche alla configurazione del certificato server richiedono un riavvio del servizio HTTP
-   Supporto per la crittografia in blocco e l'offload

## <a name="configuring-kernel-mode-ssl"></a>Configurazione di SSL in modalità kernel

Ssl in modalità kernel è controllato dal **valore del Registro di sistema EnableKernelSSL** e viene abilitato impostando il valore su 1. L'abilitazione di SSL in modalità kernel disabilita SSL in modalità utente e richiede il riavvio del servizio HTTP. La chiave del Registro di sistema **EnableKernelSSL** si trova in:

**HKEY \_ Local \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **Parametri HTTP** \\  \\ **EnableKernelSSL**

## <a name="kernel-mode-ssl-in-windows-server-2008-and-windows-vista"></a>SSL in modalità kernel in Windows Server 2008 e Windows Vista

Per i computer che eseguono Windows Server 2008 e Windows Vista, l'API server HTTP offre funzionalità SSL avanzate.

Sono supportate le nuove funzionalità seguenti:

-   Supporto completo del certificato client in modalità kernel SSL
-   SSL in modalità kernel per tutte le transazioni SSL HTTP
-   Supporto per la crittografia in blocco e l'offload
-   Protocollo PCT 1.0
-   Crittografia RC2
-   Aumento delle prestazioni rispetto a SSL in modalità utente

## <a name="configuration"></a>Configurazione

Ssl in modalità kernel è configurabile tramite due valori del Registro di sistema nella chiave Parametri HTTP disponibile in:

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

Un utente deve disporre dei privilegi di amministratore/sistema locale per modificare i valori del Registro di sistema e visualizzare o modificare i file di log e la cartella che li contiene.

Le informazioni di configurazione nei valori del Registro di sistema vengono lette all'avvio del driver API del server HTTP. Di conseguenza, se le impostazioni vengono modificate, il driver deve essere arrestato e riavviato per leggere i nuovi valori. Questa operazione può essere eseguita usando i comandi della console seguenti:

**net stop http**

**net start http**

Nella tabella seguente sono elencati i valori di configurazione del Registro di sistema.




| Valore del Registro di sistema | Descrizione | 
|----------------|-------------|
| EnableKernelSSL | <strong>Windows Server 2008 e Windows Vista:</strong> Questo valore del Registro di sistema è obsoleto.<br /> | 
| EnableSslCloseNotify | Valore <strong>DWORD impostato</strong> su <strong>TRUE</strong> per abilitare la notifica di chiusura o <strong>FALSE</strong> per disabilitare il requisito close-notify. La notifica di chiusura è disabilitata per impostazione predefinita.<br /> Quando la notifica di chiusura è abilitata, l'applicazione client deve inviare un messaggio di notifica di chiusura prima di chiudere le connessioni TCP. L'API del server HTTP invia anche una notifica di chiusura prima di chiudere la connessione.<br /> Quando la notifica di chiusura è abilitata e il client invia un messaggio di notifica di chiusura, l'API server HTTP riutilizzerà la sessione SSL nelle connessioni future al client. Se il client non invia una notifica di chiusura, l'API del server HTTP non riuserà la stessa sessione SSL nelle connessioni future. Di conseguenza, viene attivato un handshake SSL completo sulla nuova connessione, riducendo così le prestazioni. <br /><blockquote>[!Note]<br />L'abilitazione della notifica di chiusura consente di attenuare gli attacchi di troncamento alle richieste e alle risposte HTTPS.</blockquote><br /><br /> Quando la notifica di chiusura è disabilitata, l'API del server HTTP riutilizza la sessione SSL per le connessioni future.<br /> | 
| DisableSslCertChainCacheOnlyUrlRetrieval | Valore <strong>DWORD</strong> impostato su <strong>TRUE per</strong> consentire all'API del server HTTP di recuperare certificati intermedi da Internet o dall'archivio locale oppure <strong>FALSE</strong> per recuperare i certificati intermedi solo dall'archivio locale. Il valore predefinito del Registro di sistema è <strong>FALSE.</strong><br /> Per impostazione predefinita, l'API server HTTP compila una catena di certificati client recuperando i certificati intermedi dall'archivio autorità di certificazione intermedia nell'account del computer locale. L'impostazione di questo valore su <strong>TRUE</strong> consente all'API del server HTTP di recuperare i certificati intermedi non solo dall'archivio locale, ma anche dall'autorità di certificazione intermedia su Internet.<br /> | 




 

 

 





