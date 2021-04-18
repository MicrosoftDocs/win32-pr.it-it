---
description: Le proprietà vengono estratte da elementi utilizzando gestori di proprietà registrati o utilizzando filtri registrati per tipi di file specifici. Un gestore di filtro (un'implementazione dell'interfaccia IFilter) può interpretare il contenuto di un tipo di file in diversi modi.
ms.assetid: 6701d151-c36f-43e5-929b-9831c5ce5823
title: Restituzione di proprietà da un gestore di filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4df0bfc811176e9b0672dbcbe4ef4f04f3c3a6f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306168"
---
# <a name="returning-properties-from-a-filter-handler"></a>Restituzione di proprietà da un gestore di filtro

Le proprietà vengono estratte da elementi utilizzando gestori di proprietà registrati o utilizzando filtri registrati per tipi di file specifici. Un gestore di filtro (un'implementazione dell'interfaccia [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) ) può interpretare il contenuto di un tipo di file in diversi modi.

Questo argomento è organizzato nel modo seguente:

- [Filtro proprietà](#returning-properties-from-a-filter-handler)
  - [Limitazioni relative alle dimensioni delle proprietà](#property-size-limitations)
- [Risorse aggiuntive](#additional-resources)
- [Argomenti correlati](#related-topics)

## <a name="property-filtering"></a>Filtro proprietà

Nella tabella seguente sono elencate le procedure consigliate per il filtro delle proprietà.

| Metodo                                                | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IFilter:: init**](/windows/win32/api/filter/nf-filter-ifilter-init)      | Restituisce l'enumerazione dei [**\_ flag IFILTER**](/windows/win32/api/filter/ne-filter-ifilter_flags) . Se il membro delle *\_ \_ \_ proprietà OLE dei flag IFILTER* di questa enumerazione è impostato su uno, Windows Search usa le interfacce delle interfacce [IPropertySetStorage](/windows/win32/api/propidl/nn-propidl-ipropertysetstorage) e [IPropertyStorage](/windows/win32/api/propidlbase/nn-propidlbase-ipropertystorage) per enumerare e accedere alle proprietà del tipo di valore esterno. |
| [**IFilter:: GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) | Restituisce informazioni da un documento in "blocchi" con il tipo di blocco (testo o valore), il nome e le impostazioni locali. Un blocco contiene una proprietà del documento.                                                                                                                                                                                                                                                                                                      |
| [**IFilter:: GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext)   | Ottiene una proprietà di tipo testo da un blocco.                                                                                                                                                                                                                                                                                                                                                                                                         |
| [**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) | Ottiene una proprietà di tipo valore da un blocco.                                                                                                                                                                                                                                                                                                                                                                                                        |

Nella figura seguente viene illustrato un documento di esempio. La proprietà del tipo di valore esterno, `DocTitle` ottenuta usando i metodi delle interfacce [IPropertySetStorage](/windows/win32/api/propidl/nn-propidl-ipropertysetstorage) e [IPropertyStorage](/windows/win32/api/propidlbase/nn-propidlbase-ipropertystorage) , e la proprietà del tipo di valore interno `Book` (ottenuta come risultato di un'implementazione personalizzata di [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) ) descrivono l'intero documento. Proprietà del tipo di testo `Contents` e `Chapter` descrivono il contenuto del documento. Quando si elabora questo documento, il gestore di filtro (un'implementazione dell'interfaccia **IFilter** ) identifica ed estrae queste proprietà.

![diagramma che Mostra gli elementi di un documento tipico](images/ifilterpropertyextraction.png)

### <a name="property-size-limitations"></a>Limitazioni relative alle dimensioni delle proprietà

Esistono due potenziali limitazioni alla dimensione delle proprietà:

- Dimensioni massime dei dati accettati da Windows Search per ogni file.
- Dimensione massima per ogni proprietà definita nel file di descrizione della proprietà.

Attualmente, Windows Search non utilizza la dimensione della proprietà definita durante il calcolo della quantità di dati accettata da un elemento. Al contrario, il limite usato da Windows Search è il prodotto delle dimensioni del file e `MaxGrowFactor` (file size N \* MaxGrowFactor) letto dal registro di sistema. Il valore predefinito `MaxGrowFactor` è quattro.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Gathering Manager
            MaxGrowFactor
```

Di conseguenza, se il tipo di file tende a essere ridotto in dimensioni totali ma con proprietà più grandi, è possibile che Windows Search non accetti tutti i dati di proprietà che si desidera creare. Tuttavia, è possibile aumentare il `MaxGrowFactor` in base alle esigenze.

## <a name="additional-resources"></a>Risorse aggiuntive

- Nell'esempio di codice [IFilterSample](-search-sample-ifiltersample.md) , disponibile in [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), viene illustrato come creare una classe di base IFilter per implementare l'interfaccia [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) .
- Per una panoramica del processo di indicizzazione, vedere [il processo di indicizzazione](-search-indexing-process-overview.md).
- Per una panoramica dei tipi di file, vedere [tipi di file](../shell/fa-file-types.md).
- Per eseguire query sugli attributi di associazione file per un tipo di file, vedere [PerceivedTypes, SystemFileAssociations e registrazione dell'applicazione](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).
- Per una panoramica delle proprietà e dei gestori di proprietà e un elenco di proprietà di sistema che è possibile usare per i formati di file, vedere [sviluppo di gestori di proprietà per la ricerca di Windows](-search-3x-wds-extidx-propertyhandlers.md).

## <a name="related-topics"></a>Argomenti correlati

[Sviluppo di gestori di filtri](-search-ifilter-conceptual.md)

[Informazioni sui gestori di filtro in Windows Search](-search-ifilter-about.md)

[Procedure consigliate per la creazione di gestori di filtro in Windows Search](-search-3x-wds-extidx-filters.md)

[Gestori di filtri forniti con Windows](-search-ifilter-implementations.md)

[Implementazione di gestori di filtro in Windows Search](-search-ifilter-constructing-filters.md)

[Registrazione di gestori di filtro](-search-ifilter-registering-filters.md)

[Test di gestori filtro](-search-ifilter-testing-filters.md)
