---
description: È possibile estendere Windows Search per indicizzare il contenuto e le proprietà dei nuovi formati di file e gli archivi dati usando le interfacce dei componenti aggiuntivi.
ms.assetid: 69edf316-77a8-4cc5-9af8-fb89f440c9ea
title: Estensione dell'indice (Windows Search)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a74638dd5366732716335af938c00098cc3991c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306188"
---
# <a name="extending-the-index-windows-search"></a>Estensione dell'indice (Windows Search)

È possibile estendere Windows Search per indicizzare il contenuto e le proprietà dei nuovi formati di file e gli archivi dati usando le [interfacce dei componenti](./-search-data-addins-interfaces-entry-page.md)aggiuntivi. Per creare componenti aggiuntivi di Windows Search, gli sviluppatori di terze parti devono implementare prima di tutto un archivio dati della shell, quindi sviluppare un gestore di protocollo in modo che Windows Search possa accedere ai dati per l'indicizzazione. Se si dispone di un formato di file personalizzato, è necessario sviluppare un gestore di filtro per indicizzare il contenuto del file e un gestore di proprietà per ogni tipo di file per indicizzare le proprietà.

Windows Search supporta attualmente l'indicizzazione di più di 200 tipi di elementi (ad esempio, i formati di file con estensione txt, HTML e XML) e può funzionare con più tipi di archivi dati (ad esempio NTFS file system e Microsoft Outlook). Windows Search usa la tecnologia di filtro e gestore di protocollo simile a SharePoint Server. Di conseguenza, se si dispone già di implementazioni per il formato di file, è possibile aggiornare le implementazioni da inizializzare con un flusso usando [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) in modo che il filtro funzioni con la ricerca di Windows.

> [!Note]  
> I gestori di filtri, i gestori di proprietà e i gestori di protocollo devono essere scritti in codice nativo. Ciò è dovuto a potenziali problemi di controllo delle versioni di Common Language Runtime (CLR) con il processo di esecuzione di più componenti aggiuntivi.

 

Questa sezione sull'estensione dell'indice con componenti aggiuntivi contiene gli argomenti seguenti:

-   [Sviluppo di gestori di filtri](-search-ifilter-conceptual.md)
-   [Sviluppo di gestori di proprietà per Windows Search](-search-3x-wds-extidx-propertyhandlers.md)
-   [Sviluppo di gestori di protocollo](-search-3x-wds-phaddins.md)

## <a name="additional-resources"></a>Risorse aggiuntive

Per esempi di codice correlati, vedere [esempi di codice di Windows Search](-search-samples-ovw.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida allo sviluppo di Windows Search](-search-developers-guide-entry-page.md)
</dt> <dt>

[Gestione dell'indice](-search-3x-wds-mngidx-overview.md)
</dt> <dt>

[Esecuzione di query sull'indice a livello di codice](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[Estensione delle risorse della lingua](extending-language-resources-in-windows-search.md)
</dt> </dl>

 

 
