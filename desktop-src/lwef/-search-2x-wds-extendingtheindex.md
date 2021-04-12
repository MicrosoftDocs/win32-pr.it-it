---
title: Estensione dell'indice (funzionalità legacy dell'ambiente Windows)
description: L'utilizzo di e lo sviluppo per le versioni 2. x di Microsoft Windows Desktop Search (WDS) è fortemente sconsigliato a favore di Windows Search.
ms.assetid: vs|search|~\search\wds2x\extending_index_ovr.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ad766d6fa1c00649f7cbdc3118039ed50f13491
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104118874"
---
# <a name="extending-the-index-legacy-windows-environment-features"></a>Estensione dell'indice (funzionalità legacy dell'ambiente Windows)

> [!NOTE]
> Windows Desktop Search 2. x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003. Nelle versioni successive usare invece [Windows Search](../search/-search-3x-wds-overview.md) .

L'utilizzo di e lo sviluppo per le versioni 2. x di Microsoft Windows Desktop Search (WDS) è fortemente sconsigliato a favore di [Windows Search](../search/-search-3x-wds-overview.md).

WDS può essere esteso per indicizzare il contenuto dei nuovi tipi di file e degli archivi dati. Attualmente, WDS 2. x contiene filtri per più di 200 tipi di elementi (inclusi elementi di testo non crittografato, ad esempio HTML, XML e file di codice sorgente) e utilizza lo stesso [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)e la stessa tecnologia del gestore di protocollo di SharePoint Services. Se si dispone già di implementazioni di filtro installate per i nuovi tipi di file, WDS può utilizzare le interfacce di filtro esistenti per indicizzare questi dati.

I componenti aggiuntivi di WDS 2. x consentono all'indice di attraversare e analizzare i nuovi dati e le strutture di dati per aggiungere informazioni al catalogo ricercabile. Questi componenti aggiuntivi possono anche estendere la shell di Windows per associare icone e gestori di menu di scelta rapida con i nuovi tipi di file e gli archivi dati. Per includere nuovi tipi di file nel catalogo WDS, un componente aggiuntivo deve implementare l'interfaccia [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter). Per includere nuovi archivi dati, un componente aggiuntivo deve essere un gestore di protocollo. Se il nuovo archivio dati include file incorporati o nuovi tipi di file, sarà anche necessario scrivere un filtro appropriato.

> [!Note]
>
> I filtri e i gestori di protocollo devono essere scritti in codice nativo a causa di potenziali problemi di controllo delle versioni di CLR con il processo in cui vengono eseguiti tutti i componenti aggiuntivi.

 

## <a name="adding-file-types-to-the-index"></a>Aggiunta di tipi di file all'indice

I componenti aggiuntivi possono estendere WDS per indicizzare i tipi di file nuovi o proprietari e associare ogni nuovo tipo di file a un'icona o a un menu di scelta rapida specifico per il file. A tale scopo, è possibile creare e registrare un componente aggiuntivo che:

1.  Implementa un'interfaccia [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)per ogni tipo di file, in modo che WDS possa accedere e indicizzare il testo e i metadati del tipo di file.
2.  Implementa le interfacce **IExtractIcon** e **IContextMenu** per aggiungere icone e menu di scelta rapida per una maggiore integrazione e usabilità.

Per informazioni sull'implementazione di filtri, vedere [sviluppo di componenti aggiuntivi IFilter](-search-2x-wds-ifilteraddins.md).

## <a name="adding-data-stores-to-the-index"></a>Aggiunta di archivi dati all'indice

I componenti aggiuntivi possono estendere WDS per indicizzare nuovi archivi dati e associare i file a un'icona specifica del file o a un menu di scelta rapida. A tale scopo, è possibile creare e registrare un gestore di protocollo che:

1.  Implementa le interfacce **ISearchProtocol** e **IUrlAccessor** per elaborare e associare singoli elementi nell'origine del contenuto. WDS usa gli URL per identificare in modo univoco gli elementi, sia che si trovino nel file system, all'interno di un archivio simile a un database o sul Web.
2.  Implementa l'interfaccia **IPersistFolder** e le parti dell'interfaccia **IShellFolder** per aggiungere icone e menu di scelta rapida per una maggiore integrazione e usabilità.

Per informazioni sull'implementazione dei gestori di protocollo, vedere [sviluppo di gestori di protocollo](-search-2x-wds-phaddins.md).

## <a name="add-in-installer-guidelines"></a>Linee guida del programma di installazione del componente aggiuntivo

L'installazione di un componente aggiuntivo deve attenersi alle linee guida seguenti:

-   Il programma di installazione deve usare il programma di installazione EXE o MSI.
-   È necessario fornire le note sulla versione.
-   È necessario creare una voce di installazione **applicazioni** per ogni componente aggiuntivo installato.
-   Il programma di installazione deve assumere tutte le impostazioni del registro di sistema per il tipo di file o l'archivio specifico che il componente aggiuntivo corrente riconosce.
-   Se un componente aggiuntivo precedente viene sovrascritto, il programma di installazione deve inviare una notifica all'utente.
-   Se un componente aggiuntivo più recente ha sovrascritto il componente aggiuntivo precedente, dovrebbe essere possibile ripristinare la funzionalità del componente aggiuntivo precedente e renderlo di nuovo il componente aggiuntivo predefinito per il tipo di file o l'archivio.

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

[**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)
</dt> </dl>

 

 
