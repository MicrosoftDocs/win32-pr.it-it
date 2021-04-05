---
description: In questa sezione vengono fornite le informazioni concettuali necessarie per l'implementazione, l'estensione e il test dei gestori del protocollo.
ms.assetid: c76d5c82-d62b-4dd4-9743-9572be61e2be
title: Sviluppo di gestori di protocollo per Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e56c237dd4876ae05bcd7b983c4da2708f299a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750426"
---
# <a name="developing-protocol-handlers-for-windows-search"></a>Sviluppo di gestori di protocollo per Windows Search

In questa sezione vengono fornite le informazioni concettuali necessarie per l'implementazione, l'estensione e il test dei gestori del protocollo.

-   [Informazioni sui gestori di protocollo](-search-3x-wds-extidx-prot-implementing.md)
-   [Notifica dell'indice delle modifiche](-search-3x-wds-notifyingofchanges.md)
-   [Aggiunta di icone e menu di scelta rapida](-search-3x-wds-ph-ui-extensions.md)
-   [Esempio di codice: estensioni della Shell per i gestori di protocollo](-search-3x-wds-ph-ui-samplecode.md)
-   [Installazione e registrazione di gestori di protocollo](-search-3x-wds-ph-install-registration.md)
-   [Creazione di un connettore di ricerca per un gestore di protocollo](-search-3x-wds-ph-search-connector.md)
-   [Debug di gestori di protocollo](-search-ws-protocolhandlertesting.md)

## <a name="additional-resources"></a>Risorse aggiuntive

Per informazioni concettuali sull'indicizzazione, vedere gli argomenti seguenti:

-   Per una panoramica del processo di indicizzazione, vedere [il processo di indicizzazione](-search-indexing-process-overview.md).
-   Per estendere la ricerca di Windows in modo da indicizzare il contenuto e le proprietà dei nuovi formati di file e degli archivi dati, vedere [estensione dell'indice](-search-3x-wds-extidx-overview.md).
-   Per panoramiche su Catalog Manager e Catalog Search Manager (CSM), vedere [using the Catalog Manager](-search-3x-wds-mngidx-catalog-manager.md) and [using the Crawl scope Manager](-search-3x-wds-extidx-csm.md).

Per informazioni concettuali sui tipi di file e sui gestori, vedere gli argomenti seguenti:

-   Per estendere la shell con i gestori di tipi di file, vedere [creazione di gestori di estensioni della shell](../shell/handlers.md).
-   Per informazioni concettuali sui gestori di filtri, vedere [sviluppo di gestori di filtri](-search-ifilter-conceptual.md).
-   Per informazioni sulla creazione di gestori, vedere [Introduzione alle associazioni di file](../shell/fa-intro.md), [registrazione delle estensioni della shell](../shell/reg-shell-exts.md), creazione di gestori di estensioni della [Shell](../shell/handlers.md), [menu di scelta rapida](/previous-versions/windows/desktop/legacy/cc144169(v=vs.85))e [gestori di anteprime](../shell/preview-handlers.md).

Per informazioni di base sulle tecnologie correlate e sull'implementazione di un archivio dati, vedere gli argomenti seguenti:

-   I gestori del protocollo di ricerca di Windows utilizzano specifiche di progettazione simili a quelle di SharePoint Server e spesso possono essere utilizzati in modo interscambiabile. Per ulteriori informazioni, vedere il [centro per sviluppatori di SharePoint Server](https://developer.microsoft.com/office/docs).
-   In Windows 7 e versioni successive, il server di ricerca di SharePoint 2008 e MOSS 2007 SP2 supportano anche la ricerca federata. Per ulteriori informazioni sulla distribuzione di ricerca federata e server di ricerca 2008 con Office SharePoint Server 2007, vedere la pagina relativa al [ \[ server di ricerca federativo 2008 \] ](/previous-versions/office/bb931109(v=office.14)).
-   Per creare un archivio dati della shell, vedere [Implementing the Basic Folder Object Interfaces](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).

Per esempi di codice, vedere le pagine seguenti del portale:

-   Per gli esempi di codice di ricerca, vedere [esempi di Windows Search SDK](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8).
-   Per esempi di codice della shell, vedere [esempi di Shell SDK](/previous-versions/windows/desktop/legacy/dd940376(v=vs.85)).

 

 
