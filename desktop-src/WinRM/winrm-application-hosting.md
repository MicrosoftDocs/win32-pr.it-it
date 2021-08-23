---
title: Infrastruttura per la gestione dei servizi ospitati
description: Windows Gestione remota 2.0 (WinRM) introduce un framework di hosting. Per usare il framework, vengono scritti plug-in WinRM che espongono i dati di gestione di un'applicazione all'interno dell'infrastruttura winrm.
ms.assetid: 924dcc70-9a29-45a6-99a2-5681235e4574
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa41f7952867a121b8a4bd4847cb90ca42dafac346398954afbd5e4dc8bdf43e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119795271"
---
# <a name="infrastructure-for-managing-hosted-services"></a>Infrastruttura per la gestione dei servizi ospitati

Windows Gestione remota 2.0 (WinRM) introduce un framework di hosting. Per usare il framework, vengono scritti plug-in WinRM che espongono i dati di gestione di un'applicazione all'interno dell'infrastruttura winrm. Sono supportati due modelli di hosting. Uno è Internet Information Services (IIS) e l'altro è basato sul servizio WinRMâ€". Il modello basato su WinRM usa HTTP.sys e non dipende da IIS.

Le sezioni seguenti descrivono i modelli di hosting:

-   [Modello di hosting dell'estensione IIS WinRM](#winrm-iis-extension-hosting-model)
    -   [Bilanciamento del carico nel modello di hosting dell'estensione IIS di Gestione remota Windows](#load-balancing-in-the-winrm-iis-extension-hosting-model)
    -   [Reindirizzamento HTTP nel modello di hosting dell'estensione IIS winrm](#http-redirection-in-the-winrm-iis-extension-hosting-model)
-   [Modello di hosting del servizio WinRM](#winrm-service-hosting-model)

## <a name="winrm-iis-extension-hosting-model"></a>Modello di hosting dell'estensione IIS WinRM

Il modulo di estensione IIS di Gestione remota Windows è un componente facoltativo che viene installato usando il **Server Manager**. Il modulo di estensione IIS WinRM viene usato per creare endpoint abilitati per WinRM dal servizio IIS. Questo modulo può essere abilitato a livello di sito Web o di directory virtuale. Funziona intercettando e reindirizzando le richieste in ingresso al sito Web o alla directory virtuale associata. Le richieste vengono reindirizzate a un modulo WinRM che analizza il contenuto e quindi determina quale plug-in WinRM è configurato per gestire ogni richiesta. Per altre informazioni, vedere [Configurazione del plug-in host IIS.](iis-host-plug-in-configuration.md)

Il modello di hosting dell'estensione IIS WinRM è progettato per gestire un volume elevato di richieste. Se il modello basato su IIS viene usato come framework di hosting, sono disponibili le funzionalità seguenti:

-   Moduli di autenticazione IIS standard.
-   Processo del pool di applicazioni IIS per l'hosting di tutti i plug-in.
-   Gestione delle quote per la limitazione degli utenti del sistema. Per altre informazioni, vedere [Gestione delle quote per le shell remote.](quotas.md)
-   Modello di plug-in della shell. Vedere [API della shell client WinRM.](client-shell-api.md)
-   Modello di autorizzazione flessibile. Vedere [API del plug-in WinRM.](winrm-plugin-api.md)

### <a name="load-balancing-in-the-winrm-iis-extension-hosting-model"></a>Bilanciamento del carico nel modello di hosting dell'estensione IIS di Gestione remota Windows

La maggior parte dei servizi di bilanciamento del carico supporta un modello di per stickiness basato su cookie. L'LB inserisce un cookie nella risposta alla prima richiesta del client. Per tutte le richieste successive, il cookie viene trasmesso nella richiesta e l'LB usa il cookie per instradare la richiesta al server appropriato.

Negli ambienti in cui WinRM 2.0 è ospitato dietro un LB, l'LB deve essere configurato per aggiungere il prefisso MS-WSMAN al nome del cookie. Inoltre, il servizio di gestione delle applicazioni deve essere configurato per consentire che la durata del cookie sia infinita, perché il client WinRM deve controllare per quanto tempo il cookie è valido.

Di seguito è riportato un esempio di nome di cookie:

``` syntax
MS-WSMAN=2046820362.20480.0000; path=/
```

### <a name="http-redirection-in-the-winrm-iis-extension-hosting-model"></a>Reindirizzamento HTTP nel modello di hosting dell'estensione IIS winrm

WinRM 2.0 può gestire il reindirizzamento HTTP. È consigliabile che tutti i reindirizzamenti usino Secure Sockets Layer (SSL) e che tutte le applicazioni convalidino l'URI reindirizzato prima di creare una nuova sessione.

## <a name="winrm-service-hosting-model"></a>Modello di hosting del servizio WinRM

Il modello basato sul servizio Gestione remota Windows viene eseguito su HTTP.sys. Il servizio Gestione remota Windows è un servizio di rete che gestisce le richieste provenienti dai client WinRM. Il servizio determina se la richiesta viene instradata a un plug-in eseguito nel servizio principale o tramite un host in cui viene eseguito il plug-in di terze parti. Questo modello è destinato agli scenari in cui il carico sul nodo gestito è basso. Inoltre, questo modello è destinato agli scenari in cui l'hosting IIS non è un'opzione. Per altre informazioni, vedere [Configurazione del plug-in del servizio WinRM.](wsman-service-plug-in-configuration.md)

 

 




