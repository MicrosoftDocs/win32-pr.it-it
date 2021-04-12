---
title: Infrastruttura per la gestione dei servizi ospitati
description: Gestione remota Windows 2,0 (WinRM) introduce un Framework di hosting. Per utilizzare il Framework, vengono scritti i plug-in WinRM che espongono i dati di gestione di un'applicazione all'interno dell'infrastruttura WinRM.
ms.assetid: 924dcc70-9a29-45a6-99a2-5681235e4574
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8439aca1f36d2d0c2cebb6ed3111aeaa2e4fcee
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332372"
---
# <a name="infrastructure-for-managing-hosted-services"></a>Infrastruttura per la gestione dei servizi ospitati

Gestione remota Windows 2,0 (WinRM) introduce un Framework di hosting. Per utilizzare il Framework, vengono scritti i plug-in WinRM che espongono i dati di gestione di un'applicazione all'interno dell'infrastruttura WinRM. Sono supportati due modelli di hosting. Uno è Internet Information Services (IIS) "based" e l'altro è WinRMâ "based service". Il modello basato su WinRM USA HTTP.sys e non dipende da IIS.

Le sezioni seguenti descrivono i modelli di hosting:

-   [Modello di hosting dell'estensione IIS WinRM](#winrm-iis-extension-hosting-model)
    -   [Bilanciamento del carico nel modello di hosting dell'estensione IIS di gestione remota Windows](#load-balancing-in-the-winrm-iis-extension-hosting-model)
    -   [Reindirizzamento HTTP nel modello di hosting dell'estensione IIS WinRM](#http-redirection-in-the-winrm-iis-extension-hosting-model)
-   [Modello di hosting del servizio WinRM](#winrm-service-hosting-model)

## <a name="winrm-iis-extension-hosting-model"></a>Modello di hosting dell'estensione IIS WinRM

Il modulo di estensione IIS WinRM è un componente facoltativo installato utilizzando il **Server Manager**. Il modulo di estensione IIS WinRM viene usato per creare endpoint abilitati per WinRMâ "dall'interno del servizio IIS. Questo modulo può essere abilitato a livello di sito Web o di directory virtuale. Funziona intercettando e reindirizzando le richieste in ingresso al sito Web o alla directory virtuale associata. Le richieste vengono reindirizzate a un modulo WinRM che analizza il contenuto e quindi determina il plug-in WinRM configurato per gestire ogni richiesta. Per ulteriori informazioni, vedere [configurazione del plug-in host IIS](iis-host-plug-in-configuration.md).

Il modello di hosting dell'estensione IIS WinRM è progettato per gestire un volume elevato di richieste. Se il modello basato su IIS viene utilizzato come Framework di hosting, sono disponibili le seguenti funzionalità:

-   Moduli di autenticazione IIS standard.
-   Processo del pool di applicazioni IIS per l'hosting di tutti i plug-in.
-   Gestione delle quote per la limitazione degli utenti pesanti del sistema. Per altre informazioni, vedere [gestione delle quote per shell remote](quotas.md).
-   Un modello di plug-in della shell. Vedere [API della shell client WinRM](client-shell-api.md).
-   Un modello di autorizzazione flessibile. Vedere [API del plug](winrm-plugin-api.md)-in WinRM.

### <a name="load-balancing-in-the-winrm-iis-extension-hosting-model"></a>Bilanciamento del carico nel modello di hosting dell'estensione IIS di gestione remota Windows

La maggior parte dei servizi di bilanciamento del carico (LBs) supporta un modello di appiccicosità basato su cookie. Il LB inserisce un cookie nella risposta alla prima richiesta dal client. Per tutte le richieste successive, il cookie viene trasmesso nella richiesta e il LB usa il cookie per indirizzare la richiesta al server appropriato.

Negli ambienti in cui WinRM 2,0 è ospitato dietro un LB, il LB deve essere configurato in modo da precedere MS-WSMAN al nome del cookie. Inoltre, la funzionalità LB deve essere configurata in modo da consentire che la durata del cookie sia infinita, perché il client WinRM deve controllare per quanto tempo il cookie è valido.

Di seguito è riportato un esempio di un nome di cookie:

``` syntax
MS-WSMAN=2046820362.20480.0000; path=/
```

### <a name="http-redirection-in-the-winrm-iis-extension-hosting-model"></a>Reindirizzamento HTTP nel modello di hosting dell'estensione IIS WinRM

WinRM 2,0 è in grado di gestire il reindirizzamento HTTP. È consigliabile che tutti i reindirizzamenti usino Secure Sockets Layer (SSL) e che tutte le applicazioni convalidano l'URI reindirizzato prima di creare una nuova sessione.

## <a name="winrm-service-hosting-model"></a>Modello di hosting del servizio WinRM

Il modello basato su servizi WinRM viene eseguito sopra HTTP.sys. Il servizio gestione remota Windows è un servizio di rete che gestisce le richieste provenienti dai client WinRM. Il servizio determina se la richiesta viene instradata a un plug-in che viene eseguito nel servizio principale o viene instradato attraverso un host in cui viene eseguito il plug-in di terze parti. Questo modello è destinato a scenari in cui il carico sul nodo gestito è basso. Inoltre, questo modello è destinato a scenari in cui l'hosting di IIS non è un'opzione. Per ulteriori informazioni, vedere [configurazione del plug-in del servizio WinRM](wsman-service-plug-in-configuration.md).

 

 




