---
description: In questo argomento viene illustrato come un utente registra un nuovo archivio dati remoto con ricerca federata aprendo un file di descrizione OpenSearch (con estensione osdx), come distribuire un file con estensione osdx e come tenere traccia dell'utilizzo del servizio OpenSearch.
ms.assetid: 9db0f970-4e17-492b-ab75-a8b0f8011d0a
title: Distribuire i connettori di ricerca nella ricerca federata di Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a870169cd6cca3537327a8631a15d61da78eb6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484437"
---
# <a name="deploying-search-connectors-in-windows-federated-search"></a>Distribuzione di connettori di ricerca nella ricerca federata di Windows

In questo argomento viene illustrato come un utente registra un nuovo archivio dati remoto con ricerca federata aprendo un file di descrizione OpenSearch (con estensione osdx), come distribuire un file con estensione osdx e come tenere traccia dell'utilizzo del servizio [OpenSearch](https://github.com/dewitt/opensearch) .

Questo argomento è organizzato nel modo seguente:

-   [File. searchconnector-ms (connettore di ricerca)](#the-searchconnector-ms-search-connector-file)
-   [Metodi di distribuzione](#deployment-methods)
    -   [Distribuzione pull](#pull-deployment)
    -   [Distribuzione push](#push-deployment)
-   [Rilevamento dell'utilizzo](#tracking-usage)
-   [Risorse aggiuntive](#additional-resources)
-   [Argomenti correlati](#related-topics)

## <a name="the-searchconnector-ms-search-connector-file"></a>File. searchconnector-ms (connettore di ricerca)

È sufficiente aprire il file con estensione osdx che descrive come connettersi al servizio Web e come eseguire il mapping di eventuali elementi personalizzati nel codice XML RSS o Atom per la registrazione del nuovo archivio dati remoto con la ricerca federata. Un archivio dati che dispone già di un servizio Web [OpenSearch](https://github.com/dewitt/opensearch) compatibile con la ricerca federata può essere aggiunto a Esplora risorse quando un utente apre un file con estensione osdx.

Dopo aver assegnato il file. osdx all'utente e l'utente apre il file con estensione osdx, si verificano gli eventi seguenti.

1.  Viene creato un file con estensione searchconnector-ms nella cartella **ricerche di Windows** (% USERPROFILE%/Searches).
2.  Viene creato un collegamento al file. searchconnector-ms nella cartella **Links** (% USERPROFILE%/Links).
3.  Viene visualizzato un collegamento nel riquadro **Preferiti** di esplorazione di Esplora risorse, che consente all'utente di spostarsi nel nuovo archivio dati ed eseguire query sul servizio Web.

## <a name="deployment-methods"></a>Metodi di distribuzione

Esistono due modi per distribuire i connettori di ricerca, la distribuzione pull e la distribuzione push.

### <a name="pull-deployment"></a>Distribuzione pull

Distribuzione pull descrive qualsiasi tipo di distribuzione in cui l'utente finale intraprende l'iniziativa di installare i connettori di ricerca. I metodi comuni di distribuzione pull sono:

-   Il file con estensione osdx viene collegato in un messaggio di posta elettronica.
-   Pubblicazione del file in una pagina Web.
-   Fornire un collegamento dinamico nel sito Intranet. ad esempio, uno che genera file con estensione osdx personalizzati in base alle scelte utente o all'ambito corrente all'interno del sito.

Per il download del file quando l'utente fa clic sul collegamento nel browser, il server Web che ospita il servizio Web deve essere configurato in modo da recapitare il file con estensione osdx. Pertanto, è necessario configurare i tipi MIME nel server Web per trattare i file. osdx come `"application/opensearchdescription+xml"` . Facoltativamente, è possibile usare l'icona fornita da Microsoft per identificare il collegamento al connettore di ricerca.

### <a name="push-deployment"></a>Distribuzione push

Distribuzione push descrive tutti i tipi di distribuzione che non dipendono dall'iniziativa utente per installare i connettori di ricerca. I metodi comuni di distribuzione push sono i seguenti:

-   Preferenze Criteri di gruppo (GPP)
-   Script di accesso
-   Profili mobili
-   Creazione delle immagini

## <a name="tracking-usage"></a>Rilevamento dell'utilizzo

Per tenere traccia dell'utilizzo del servizio [OpenSearch](https://github.com/dewitt/opensearch) da parte degli utenti che eseguono ricerche da Esplora risorse, filtrare i file di log del server Web per la stringa dell'agente utente: `Windows-Search+(Windows+NT+6.1)` .

## <a name="additional-resources"></a>Risorse aggiuntive

Per ulteriori informazioni sull'implementazione della Federazione di ricerca negli archivi dati remoti tramite le tecnologie OpenSearch in Windows 7 e versioni successive, vedere l'argomento relativo alle risorse aggiuntive in [ricerca federata in Windows](/previous-versions//dd742958(v=vs.85)).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Ricerca federata in Windows](-search-federated-search-overview.md)
</dt> <dt>

[Introduzione con ricerca federata in Windows](getting-started-with-federated-search-in-windows.md)
</dt> <dt>

[Connessione del servizio Web in ricerca federata di Windows](-search-federated-search-web-service.md)
</dt> <dt>

[Abilitazione dell'archivio dati in ricerca federata di Windows](-search-federated-search-data-store.md)
</dt> <dt>

[Creazione di un file di descrizione OpenSearch nella ricerca federata di Windows](-search-federated-search-osdx-file.md)
</dt> <dt>

[Procedure consigliate seguenti in ricerca federata di Windows](-search-fedsearch-best.md)
</dt> </dl>

 

 
