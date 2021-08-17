---
description: Questo argomento illustra come un utente registra un nuovo archivio dati remoto con la ricerca federata aprendo un file OpenSearch Description (con estensione osdx), come distribuire un file con estensione osdx e come tenere traccia dell'utilizzo del servizio OpenSearch.
ms.assetid: 9db0f970-4e17-492b-ab75-a8b0f8011d0a
title: Distribuire i connettori di ricerca Windows ricerca federata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7515fa905abf3767696457f30a52abdb0a36d78883e9649cb2bf42e77e8b8c2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118463136"
---
# <a name="deploying-search-connectors-in-windows-federated-search"></a>Distribuzione di connettori di ricerca Windows ricerca federata

Questo argomento illustra come un utente registra un nuovo archivio dati remoto con la ricerca federata aprendo un file OpenSearch Description (.osdx), come distribuire un file con estensione osdx e come tenere traccia dell'utilizzo del [servizio OpenSearch.](https://github.com/dewitt/opensearch)

Questo argomento è organizzato come segue:

-   [File con estensione searchconnector-ms (Search Connector)](#the-searchconnector-ms-search-connector-file)
-   [Metodi di distribuzione](#deployment-methods)
    -   [Distribuzione pull](#pull-deployment)
    -   [Distribuzione push](#push-deployment)
-   [Rilevamento dell'utilizzo](#tracking-usage)
-   [Risorse aggiuntive](#additional-resources)
-   [Argomenti correlati](#related-topics)

## <a name="the-searchconnector-ms-search-connector-file"></a>File con estensione searchconnector-ms (Search Connector)

Semplicemente aprendo il file con estensione osdx che descrive come connettersi al servizio Web e come eseguire il mapping di qualsiasi elemento personalizzato nel file RSS o Atom XML, il nuovo archivio dati remoto viene registrato con la ricerca federata. Un archivio dati che [](https://github.com/dewitt/opensearch) dispone già di un servizio Web OpenSearch compatibile con la ricerca federata può essere aggiunto a Windows Explorer quando un utente apre un file OSDX.

Dopo aver assegnato il file OSDX all'utente e aver aperto il file OSDX, si verificano gli eventi seguenti.

1.  Viene creato un file con estensione searchconnector-ms nella cartella Windows **ricerche** (%userprofile%/Searches).
2.  Viene creato un collegamento al file .searchconnector-ms nella **cartella Collegamenti** (%userprofile%/Links).
3.  Viene visualizzato un collegamento nel riquadro  Preferiti Windows Explorer, che consente all'utente di passare al nuovo archivio dati ed eseguire query sul servizio Web.

## <a name="deployment-methods"></a>Metodi di distribuzione

Esistono due modi per distribuire i connettori di ricerca, la distribuzione pull e la distribuzione push.

### <a name="pull-deployment"></a>Distribuzione pull

La distribuzione pull descrive qualsiasi tipo di distribuzione in cui l'utente finale prende l'iniziativa di installare i connettori di ricerca. I metodi comuni di distribuzione pull sono:

-   Allegare il file con estensione osdx in un messaggio di posta elettronica.
-   Pubblicazione del file in una pagina Web.
-   Fornire un collegamento dinamico nel sito Intranet; ad esempio uno che genera file OSDX personalizzati in base alle scelte dell'utente o all'ambito corrente all'interno del sito.

Per scaricare il file quando l'utente fa clic sul collegamento nel browser, il server Web che ospita il servizio Web deve essere configurato per recapitare il file con estensione osdx come file. Di conseguenza, è necessario configurare i tipi MIME nel server Web per considerare i file OSDX come `"application/opensearchdescription+xml"` . Facoltativamente, è possibile usare l'icona fornita da Microsoft per identificare il collegamento del connettore di ricerca.

### <a name="push-deployment"></a>Distribuzione push

La distribuzione push descrive qualsiasi tipo di distribuzione che non dipende dall'iniziativa dell'utente per installare i connettori di ricerca. I metodi comuni di distribuzione push sono:

-   Criteri di gruppo preferenze (GPP)
-   Script di accesso
-   Profili mobili
-   Creazione delle immagini

## <a name="tracking-usage"></a>Rilevamento dell'utilizzo

Per tenere traccia dell'utilizzo [del servizio OpenSearch](https://github.com/dewitt/opensearch) da parte degli utenti che esempe la ricerca da Windows Explorer, filtrare i file di log del server Web per questa stringa agente utente: `Windows-Search+(Windows+NT+6.1)` .

## <a name="additional-resources"></a>Risorse aggiuntive

Per altre informazioni sull'implementazione della federazione della ricerca negli archivi dati remoti usando tecnologie OpenSearch in Windows 7 e versioni successive, vedere "Risorse aggiuntive" in Ricerca federata [in Windows](/previous-versions//dd742958(v=vs.85)).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Ricerca federata in Windows](-search-federated-search-overview.md)
</dt> <dt>

[Attività iniziali con ricerca federata in Windows](getting-started-with-federated-search-in-windows.md)
</dt> <dt>

[Connessione del servizio Web in Windows federata](-search-federated-search-web-service.md)
</dt> <dt>

[Abilitazione dell'archivio dati Windows ricerca federata](-search-federated-search-data-store.md)
</dt> <dt>

[Creazione di un OpenSearch file di descrizione Windows ricerca federata](-search-federated-search-osdx-file.md)
</dt> <dt>

[Procedure consigliate per la ricerca Windows federata](-search-fedsearch-best.md)
</dt> </dl>

 

 
