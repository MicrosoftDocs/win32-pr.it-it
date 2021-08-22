---
description: Questo argomento descrive i passaggi necessari per connettere un servizio Web tra l'archivio dati e Windows Ricerca federata e come inviare query e restituire i risultati della ricerca in RSS o Atom.
ms.assetid: 4c8de310-49e6-4d90-a920-0c715351c86a
title: Connessione del servizio Web in Windows federata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4980b2d62f766806cf89856b8ef9e5231284be0dfea3258d2e5d5155e7a46598
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119456721"
---
# <a name="connecting-your-web-service-in-windows-federated-search"></a>Connessione del servizio Web in Windows federata

Questo argomento descrive i passaggi necessari per connettere un servizio Web tra l'archivio dati e Windows Ricerca federata e come inviare query e restituire i risultati della ricerca in RSS o Atom.

Questo argomento è organizzato come segue:

-   [Connessione Servizio Web](#connect-your-web-service)
-   [Registrare un archivio dati remoto esistente](#register-an-existing-remote-data-store)
-   [Risorse aggiuntive](#additional-resources)
-   [Argomenti correlati](#related-topics)

## <a name="connect-your-web-service"></a>Connessione Servizio Web

**Per connettere il servizio Web dell'archivio dati alla ricerca federata, seguire questa procedura:**

1.  Creare un file con estensione osdx.
2.  Fornire il file OSDX agli utenti in modo che possano aggiungere il servizio su richiesta aprendo il file OSDX.
3.  Generare un connettore di ricerca e distribuirlo attivamente nell'organizzazione.

## <a name="register-an-existing-remote-data-store"></a>Registrare un archivio dati remoto esistente

Un utente registra un nuovo archivio dati remoto Windows ricerca federata aprendo un file OpenSearch description (con estensione osdx). Quando l'utente esegue questa operazione, si verificano gli eventi seguenti:

1.  Viene creato un file con estensione searchconnector-ms (connettore di ricerca) nella cartella ricerche Windows (%userprofile%/Searches).
2.  Viene creato un collegamento al file .searchconnector-ms nella cartella Collegamenti (%userprofile%/Links).
3.  Viene visualizzato un collegamento nel riquadro  Preferiti Windows Explorer, che consente all'utente di passare al nuovo archivio dati ed eseguire query sul servizio Web.

> [!Note]  
> Un archivio dati che [](https://github.com/dewitt/opensearch) dispone già di un servizio Web OpenSearch compatibile con Windows Federated Search può essere aggiunto Windows Explorer quando un utente apre un file OSDX.

 

## <a name="additional-resources"></a>Risorse aggiuntive

Per altre informazioni sull'implementazione della federazione della ricerca negli archivi dati remoti usando tecnologie OpenSearch in Windows 7 e versioni successive, vedere "Risorse aggiuntive" in Ricerca federata [in Windows](/previous-versions//dd742958(v=vs.85)).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Ricerca federata in Windows](-search-federated-search-overview.md)
</dt> <dt>

[Attività iniziali con ricerca federata in Windows](getting-started-with-federated-search-in-windows.md)
</dt> <dt>

[Abilitazione dell'archivio dati Windows ricerca federata](-search-federated-search-data-store.md)
</dt> <dt>

[Creazione di un OpenSearch file di descrizione Windows ricerca federata](-search-federated-search-osdx-file.md)
</dt> <dt>

[Procedure consigliate per la ricerca Windows federata](-search-fedsearch-best.md)
</dt> <dt>

[Distribuzione di connettori di ricerca Windows ricerca federata](-search-federated-search-deploying.md)
</dt> </dl>

 

 
