---
description: Le proprietà vengono estratte dagli elementi usando gestori di proprietà registrati o filtri registrati per tipi di file specifici. Un gestore di filtri (un'implementazione dell'interfaccia IFilter) può interpretare il contenuto di un tipo di file in diversi modi.
ms.assetid: 6701d151-c36f-43e5-929b-9831c5ce5823
title: Restituzione di proprietà da un gestore di filtri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b1842710af65e22f5a730891ea6e7f32053b92212f8c3ad4c5f0f68f23578d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119594856"
---
# <a name="returning-properties-from-a-filter-handler"></a>Restituzione di proprietà da un gestore di filtri

Le proprietà vengono estratte dagli elementi usando gestori di proprietà registrati o filtri registrati per tipi di file specifici. Un gestore di filtri (un'implementazione [**dell'interfaccia IFilter)**](/windows/win32/api/filter/nn-filter-ifilter) può interpretare il contenuto di un tipo di file in diversi modi.

Questo argomento è organizzato come segue:

- [Filtro delle proprietà](#returning-properties-from-a-filter-handler)
  - [Limitazioni delle dimensioni delle proprietà](#property-size-limitations)
- [Risorse aggiuntive](#additional-resources)
- [Argomenti correlati](#related-topics)

## <a name="property-filtering"></a>Filtro delle proprietà

Nella tabella seguente sono elencate le procedure consigliate per il filtro delle proprietà.

| Metodo                                                | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IFilter::Init**](/windows/win32/api/filter/nf-filter-ifilter-init)      | Restituisce [**l'enumerazione IFILTER \_ FLAGS.**](/windows/win32/api/filter/ne-filter-ifilter_flags) Se il membro *\_ OLE \_ \_ PROPERTIES* di IFILTER FLAGS di questa enumerazione è impostato su uno, Windows Search usa le interfacce [IPropertySetStorage](/windows/win32/api/propidl/nn-propidl-ipropertysetstorage) e [IPropertyStorage](/windows/win32/api/propidlbase/nn-propidlbase-ipropertystorage) per enumerare e accedere alle proprietà esterne del tipo di valore. |
| [**IFilter::GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) | Restituisce informazioni da un documento in "blocchi" con tipo di blocco (testo o valore), nome e impostazioni locali. Un blocco contiene una proprietà del documento.                                                                                                                                                                                                                                                                                                      |
| [**IFilter::GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext)   | Ottiene una proprietà di tipo testo da un blocco.                                                                                                                                                                                                                                                                                                                                                                                                         |
| [**IFilter::GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) | Ottiene una proprietà di tipo valore da un blocco.                                                                                                                                                                                                                                                                                                                                                                                                        |

La figura seguente mostra un documento di esempio. La proprietà esterna di tipo valore (ottenuta usando i metodi delle interfacce `DocTitle` [IPropertySetStorage](/windows/win32/api/propidl/nn-propidl-ipropertysetstorage) e [IPropertyStorage)](/windows/win32/api/propidlbase/nn-propidlbase-ipropertystorage) e la proprietà interna del tipo di valore (ottenuta come risultato di un'implementazione `Book` [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) personalizzata) descrivono il documento nel suo complesso. Proprietà di tipo testo `Contents` e `Chapter` descrizione del contenuto del documento. Durante l'elaborazione di questo documento, il gestore di filtri (un'implementazione **dell'interfaccia IFilter)** identifica ed estrae queste proprietà.

![Diagramma che mostra gli elementi di un documento tipico](images/ifilterpropertyextraction.png)

### <a name="property-size-limitations"></a>Limitazioni delle dimensioni delle proprietà

Esistono due potenziali limitazioni alle dimensioni delle proprietà:

- Dimensione massima dei dati accettati Windows ricerca per ogni file.
- Dimensioni massime per proprietà definite nel file di descrizione della proprietà.

Attualmente, Windows ricerca non usa le dimensioni della proprietà definite durante il calcolo della quantità di dati accettati da un elemento. Al contrario, il limite Windows ricerca è il prodotto delle dimensioni del file e `MaxGrowFactor` (dimensioni del file N \* MaxGrowFactor) lette dal Registro di sistema. Il valore `MaxGrowFactor` predefinito è quattro.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Gathering Manager
            MaxGrowFactor
```

Di conseguenza, se il tipo di file tende a essere di dimensioni totali ridotte ma ha proprietà più grandi, Windows Ricerca potrebbe non accettare tutti i dati delle proprietà da generare. Tuttavia, è possibile aumentare in `MaxGrowFactor` base alle proprie esigenze.

## <a name="additional-resources"></a>Risorse aggiuntive

- L'esempio di codice [IFilterSample,](-search-sample-ifiltersample.md) disponibile in [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), illustra come creare una classe di base IFilter per l'implementazione [**dell'interfaccia IFilter.**](/windows/win32/api/filter/nn-filter-ifilter)
- Per una panoramica del processo di indicizzazione, vedere [Processo di indicizzazione.](-search-indexing-process-overview.md)
- Per una panoramica dei tipi di file, vedere [Tipi di file.](../shell/fa-file-types.md)
- Per eseguire query su attributi di associazione di file per un tipo di file, vedere [PerceivedTypes, SystemFileAssociations e Registrazione dell'applicazione.](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85))
- Per una panoramica delle proprietà e dei gestori delle proprietà e per un elenco delle proprietà di sistema che è possibile usare per i formati di file, vedere Sviluppo di gestori di proprietà per Windows [ricerca.](-search-3x-wds-extidx-propertyhandlers.md)

## <a name="related-topics"></a>Argomenti correlati

[Sviluppo di gestori di filtri](-search-ifilter-conceptual.md)

[Informazioni sui gestori di filtri Windows ricerca](-search-ifilter-about.md)

[Procedure consigliate per la creazione di gestori di filtri in Windows ricerca](-search-3x-wds-extidx-filters.md)

[Gestori di filtri forniti con Windows](-search-ifilter-implementations.md)

[Implementazione di gestori di filtri in Windows ricerca](-search-ifilter-constructing-filters.md)

[Registrazione di gestori di filtri](-search-ifilter-registering-filters.md)

[Test dei gestori di filtri](-search-ifilter-testing-filters.md)
