---
description: Informazioni su come sviluppare gestori di filtri in Windows Search. La ricerca usa i filtri per estrarre gli elementi da includere in un indice full-text.
ms.assetid: 7b24986b-972d-4674-846b-f856b908edf4
title: Sviluppo di gestori di filtri per Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa86c0a1e41ababf6f00db72a26784beb93e1879
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/10/2021
ms.locfileid: "111988860"
---
# <a name="developing-filter-handlers-for-windows-search"></a>Sviluppo di gestori di filtri per Windows Search

Microsoft Windows Search i filtri per estrarre il contenuto degli elementi da includere in un indice full-text. È possibile estendere Windows Search indicizzare tipi di file nuovi o proprietari scrivendo filtri per estrarre il contenuto e gestori di proprietà per estrarre le proprietà dei file.

Questa sezione fornisce il framework concettuale necessario per l'implementazione di un gestore di filtri (un'implementazione [**dell'interfaccia IFilter).**](/windows/win32/api/filter/nn-filter-ifilter)

- [Informazioni sui gestori di filtri in Windows Search](-search-ifilter-about.md)
- [Procedure consigliate per la creazione di gestori di filtri in Windows Search](-search-3x-wds-extidx-filters.md)
- [Restituzione di proprietà da un gestore di filtri](-search-ifilter-property-filtering.md)
- [Gestori di filtri forniti con Windows](-search-ifilter-implementations.md)
- [Implementazione di gestori di filtri in Windows Search](-search-ifilter-constructing-filters.md)
- [Registrazione di gestori di filtri](-search-ifilter-registering-filters.md)
- [Test dei gestori di filtri](-search-ifilter-testing-filters.md)

## <a name="additional-resources"></a>Risorse aggiuntive

- L'esempio di codice [IFilterSample,](-search-sample-ifiltersample.md) disponibile in [GitHub,](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample)illustra come creare una classe di base IFilter per l'implementazione [**dell'interfaccia IFilter.**](/windows/win32/api/filter/nn-filter-ifilter)
- Per una panoramica del processo di indicizzazione, vedere [Processo di indicizzazione.](-search-indexing-process-overview.md)
- Per una panoramica dei tipi di file, vedere [Tipi di file.](../shell/fa-file-types.md)
- Per eseguire query su attributi di associazione di file per un tipo di file, vedere [PerceivedTypes, SystemFileAssociations e Registrazione dell'applicazione.](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85))
