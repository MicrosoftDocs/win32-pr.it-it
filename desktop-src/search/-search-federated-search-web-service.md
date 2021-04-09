---
description: In questo argomento vengono descritti i passaggi necessari per connettere un servizio Web tra l'archivio dati e la ricerca federata di Windows e come inviare query e restituire i risultati della ricerca in formato RSS o Atom.
ms.assetid: 4c8de310-49e6-4d90-a920-0c715351c86a
title: Connessione del servizio Web in ricerca federata di Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45632d1d3c7b820ab1f39db0896c9f2927b24ccb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128578"
---
# <a name="connecting-your-web-service-in-windows-federated-search"></a>Connessione del servizio Web in ricerca federata di Windows

In questo argomento vengono descritti i passaggi necessari per connettere un servizio Web tra l'archivio dati e la ricerca federata di Windows e come inviare query e restituire i risultati della ricerca in formato RSS o Atom.

Questo argomento è organizzato nel modo seguente:

-   [Connettere il servizio Web](#connect-your-web-service)
-   [Registrare un archivio dati remoto esistente](#register-an-existing-remote-data-store)
-   [Risorse aggiuntive](#additional-resources)
-   [Argomenti correlati](#related-topics)

## <a name="connect-your-web-service"></a>Connettere il servizio Web

**Per connettere il servizio Web dell'archivio dati alla ricerca federata, seguire questa procedura:**

1.  Creare un file con estensione osdx.
2.  Fornire il file. osdx agli utenti in modo che possano aggiungere il servizio su richiesta aprendo il file. osdx.
3.  Generare un connettore di ricerca e distribuirlo attivamente nell'azienda.

## <a name="register-an-existing-remote-data-store"></a>Registrare un archivio dati remoto esistente

Un utente registra un nuovo archivio dati remoto con ricerca federata di Windows aprendo un file di descrizione OpenSearch (con estensione osdx). Quando l'utente esegue questa operazione, si verificano gli eventi seguenti:

1.  Un file. searchconnector-ms (connettore di ricerca) viene creato nella cartella ricerche di Windows (% USERPROFILE%/Searches).
2.  Viene creato un collegamento al file. searchconnector-ms nella cartella Links (% USERPROFILE%/Links).
3.  Viene visualizzato un collegamento nel riquadro **Preferiti** di esplorazione di Esplora risorse, che consente all'utente di spostarsi nel nuovo archivio dati ed eseguire query sul servizio Web.

> [!Note]  
> Un archivio dati che dispone già di un servizio Web [OpenSearch](https://github.com/dewitt/opensearch) compatibile con la ricerca federata di Windows può essere aggiunto a Esplora risorse quando un utente apre un file con estensione osdx.

 

## <a name="additional-resources"></a>Risorse aggiuntive

Per ulteriori informazioni sull'implementazione della Federazione di ricerca negli archivi dati remoti tramite le tecnologie OpenSearch in Windows 7 e versioni successive, vedere l'argomento relativo alle risorse aggiuntive in [ricerca federata in Windows](/previous-versions//dd742958(v=vs.85)).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Ricerca federata in Windows](-search-federated-search-overview.md)
</dt> <dt>

[Introduzione con ricerca federata in Windows](getting-started-with-federated-search-in-windows.md)
</dt> <dt>

[Abilitazione dell'archivio dati in ricerca federata di Windows](-search-federated-search-data-store.md)
</dt> <dt>

[Creazione di un file di descrizione OpenSearch nella ricerca federata di Windows](-search-federated-search-osdx-file.md)
</dt> <dt>

[Procedure consigliate seguenti in ricerca federata di Windows](-search-fedsearch-best.md)
</dt> <dt>

[Distribuzione di connettori di ricerca nella ricerca federata di Windows](-search-federated-search-deploying.md)
</dt> </dl>

 

 
