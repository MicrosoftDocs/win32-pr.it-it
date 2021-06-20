---
title: Estensione dell'indice (funzionalità legacy dell'ambiente Windows)
description: Informazioni su come estendere l'indice in Windows Desktop Search 2.x. Per le versioni di Windows successive a Windows XP e Windows Server 2003, usare Windows Search.
ms.assetid: vs|search|~\search\wds2x\extending_index_ovr.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63408cfe1efeb8da4d6a4540cc57b99ea56ae935
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407354"
---
# <a name="extending-the-index-legacy-windows-environment-features"></a>Estensione dell'indice (funzionalità legacy dell'ambiente Windows)

> [!NOTE]
> Windows Desktop Search 2.x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003. Nelle versioni successive usare [invece Windows Search.](../search/-search-3x-wds-overview.md)

L'uso di e lo sviluppo per le versioni 2.x di Microsoft Windows Desktop Search (WDS) è fortemente sconsigliato a favore [di Windows Search](../search/-search-3x-wds-overview.md).

WDS può essere esteso per indicizzare il contenuto di nuovi tipi di file e archivi dati. Attualmente, WDS 2.x contiene filtri per oltre 200 tipi di elementi (inclusi elementi di testo non crittografato come HTML, XML e file di codice sorgente) e usa la stessa tecnologia [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)e gestore di protocollo di SharePoint Services. Se sono già state installate implementazioni di filtro per i nuovi tipi di file, WDS può usare le interfacce di filtro esistenti per indicizzare questi dati.

I componenti aggiuntivi WDS 2.x consentono all'indice di attraversare e analizzare nuovi dati e strutture di dati per ottenere informazioni da aggiungere al catalogo ricercabile. Questi componenti aggiuntivi possono anche estendere la shell di Windows per associare icone e gestori di menu di scelta rapida ai nuovi tipi di file e archivi dati. Per includere nuovi tipi di file nel catalogo di Servizi di distribuzione Windows, un componente aggiuntivo deve implementare [**l'interfaccia IFilter.**](/windows/desktop/api/filter/nn-filter-ifilter) Per includere nuovi archivi dati, un componente aggiuntivo deve essere un gestore di protocollo. Se il nuovo archivio dati include file incorporati o nuovi tipi di file, sarà anche necessario scrivere un filtro appropriato.

> [!Note]
>
> I filtri e i gestori di protocollo devono essere scritti in codice nativo a causa di potenziali problemi di controllo delle versioni clr con il processo in cui vengono eseguiti tutti i componenti aggiuntivi.

 

## <a name="adding-file-types-to-the-index"></a>Aggiunta di tipi di file all'indice

I componenti aggiuntivi possono estendere Servizi di distribuzione Windows per indicizzare tipi di file nuovi o proprietari e per associare ogni nuovo tipo di file a un'icona specifica del file o a un menu di scelta rapida. A tale scopo, è possibile compilare e registrare un componente aggiuntivo che:

1.  Implementa [**un'interfaccia IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)per ogni tipo di file in modo che WDS possa accedere e indicizzare il testo e i metadati del tipo di file.
2.  Implementa le **interfacce IExtractIcon** e **IContextMenu** per aggiungere icone e menu di scelta rapida per una maggiore integrazione e usabilità.

Per informazioni sull'implementazione dei filtri, vedere Sviluppo di [componenti aggiuntivi IFilter.](-search-2x-wds-ifilteraddins.md)

## <a name="adding-data-stores-to-the-index"></a>Aggiunta di archivi dati all'indice

I componenti aggiuntivi possono estendere Servizi di distribuzione Windows per indicizzare nuovi archivi dati e associare file a un'icona o a un menu di scelta rapida specifico del file. A tale scopo, è possibile compilare e registrare un gestore di protocollo che:

1.  Implementa le **interfacce ISearchProtocol** e **IUrlAccessor** per elaborare e associare singoli elementi nell'origine contenuto. WDS usa gli URL per identificare in modo univoco gli elementi, se si trova nel file system, all'interno di un archivio simile a un database o sul Web.
2.  Implementa **l'interfaccia IPersistFolder** e parti **dell'interfaccia IShellFolder** per aggiungere icone e menu di scelta rapida per una maggiore integrazione e usabilità.

Per una discussione sull'implementazione di gestori di protocollo, vedere [Sviluppo di gestori di protocollo.](-search-2x-wds-phaddins.md)

## <a name="add-in-installer-guidelines"></a>Linee guida per il programma di installazione dei componenti aggiuntivi

L'installazione di un componente aggiuntivo deve seguire le linee guida seguenti:

-   Il programma di installazione deve usare il programma di installazione EXE o MSI.
-   È necessario fornire le note sulla versione.
-   È **necessario creare una voce Installazione** applicazioni per ogni componente aggiuntivo installato.
-   Il programma di installazione deve assumere tutte le impostazioni del Registro di sistema per il particolare tipo di file o archivio che il componente aggiuntivo corrente è in conoscenza.
-   Se viene sovrascritto un componente aggiuntivo precedente, il programma di installazione deve inviare una notifica all'utente.
-   Se un componente aggiuntivo più recente ha sovrascritto il componente aggiuntivo precedente, dovrebbe essere possibile ripristinare la funzionalità del componente aggiuntivo precedente e renderlo nuovamente il componente aggiuntivo predefinito per quel tipo di file o archivio.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Riferimento**
</dt> <dt>

[Sviluppo di componenti aggiuntivi IFilter](-search-2x-wds-ifilteraddins.md)
</dt> <dt>

[Sviluppo di gestori di protocollo](-search-2x-wds-phaddins.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**Ifilter**](/windows/desktop/api/filter/nn-filter-ifilter)
</dt> </dl>

 

 
