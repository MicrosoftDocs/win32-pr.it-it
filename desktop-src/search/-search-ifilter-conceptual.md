---
description: Microsoft Windows Search USA i filtri per estrarre il contenuto degli elementi da includere in un indice full-text.
ms.assetid: 7b24986b-972d-4674-846b-f856b908edf4
title: Sviluppo di gestori di filtri per la ricerca di Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bab8f45892549dc3f392824c31c78884b209d283
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049387"
---
# <a name="developing-filter-handlers-for-windows-search"></a>Sviluppo di gestori di filtri per la ricerca di Windows

Microsoft Windows Search USA i filtri per estrarre il contenuto degli elementi da includere in un indice full-text. È possibile estendere la ricerca di Windows per indicizzare i tipi di file nuovi o proprietari scrivendo i filtri per estrarre il contenuto e i gestori delle proprietà per estrarre le proprietà dei file.

In questa sezione viene fornito il framework concettuale necessario per l'implementazione di un gestore di filtri, ovvero un'implementazione dell'interfaccia [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) .

- [Informazioni sui gestori di filtro in Windows Search](-search-ifilter-about.md)
- [Procedure consigliate per la creazione di gestori di filtro in Windows Search](-search-3x-wds-extidx-filters.md)
- [Restituzione di proprietà da un gestore di filtro](-search-ifilter-property-filtering.md)
- [Gestori di filtri forniti con Windows](-search-ifilter-implementations.md)
- [Implementazione di gestori di filtro in Windows Search](-search-ifilter-constructing-filters.md)
- [Registrazione di gestori di filtro](-search-ifilter-registering-filters.md)
- [Test di gestori filtro](-search-ifilter-testing-filters.md)

## <a name="additional-resources"></a>Risorse aggiuntive

- Nell'esempio di codice [IFilterSample](-search-sample-ifiltersample.md) , disponibile in [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), viene illustrato come creare una classe di base IFilter per implementare l'interfaccia [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) .
- Per una panoramica del processo di indicizzazione, vedere [il processo di indicizzazione](-search-indexing-process-overview.md).
- Per una panoramica dei tipi di file, vedere [tipi di file](../shell/fa-file-types.md).
- Per eseguire query sugli attributi di associazione file per un tipo di file, vedere [PerceivedTypes, SystemFileAssociations e registrazione dell'applicazione](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).
