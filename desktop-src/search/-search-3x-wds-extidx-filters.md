---
description: Microsoft Windows Search USA i filtri per estrarre il contenuto degli elementi da includere in un indice full-text.
ms.assetid: 7b86a1b4-c8a9-400d-a9f1-a3b821c0269d
title: Procedure consigliate per i gestori di filtro in Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 544992e252d9ec0e3a7c402d1c348d3e3bfa9a85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525537"
---
# <a name="best-practices-for-creating-filter-handlers-in-windows-search"></a>Procedure consigliate per la creazione di gestori di filtro in Windows Search

Microsoft Windows Search USA i filtri per estrarre il contenuto degli elementi da includere in un indice full-text. È possibile estendere la ricerca di Windows per indicizzare i tipi di file nuovi o proprietari scrivendo i gestori di filtro per estrarre il contenuto e i gestori delle proprietà per estrarre le proprietà dei file. I filtri sono associati ai tipi di file, come indicato dalle estensioni dei nomi di file, dai tipi MIME o dagli identificatori di classe (CLSID). Mentre un filtro può gestire più tipi di file, ogni tipo funziona con un solo filtro.

In questo argomento sono incluse le sezioni seguenti:

-   [Codice nativo](#native-code)
-   [Procedure di sicurezza del codice per Windows Search](#secure-code-practices-for-windows-search)
-   [Risorse aggiuntive](#additional-resources)
-   [Argomenti correlati](#related-topics)

## <a name="native-code"></a>Codice nativo

In Windows 7 e versioni successive, i filtri scritti nel codice gestito vengono bloccati in modo esplicito. I filtri devono essere scritti in codice nativo a causa di potenziali problemi di controllo delle versioni di CLR con il processo di esecuzione di più componenti aggiuntivi.

## <a name="secure-code-practices-for-windows-search"></a>Procedure di sicurezza del codice per Windows Search

Di seguito sono riportate le procedure per la scrittura di applicazioni sicure per l'utilizzo con Windows Search.

**Per le applicazioni di query:**

-   Quando si scrivono i client di ricerca, è necessario scegliere l'API che viene eseguita in un contesto di sicurezza che consente all'utente il privilegio minimo. Ad esempio, le pagine ASP possono usare l'oggetto query IXSSO, che viene eseguito come processo utente.

**Per IFilters e risorse della lingua:**

-   Se è in corso l'installazione di un nuovo gestore di filtro per un tipo di file in sostituzione di una registrazione filtro esistente, il programma di installazione deve salvare la registrazione corrente e ripristinarla se il nuovo gestore di filtro viene disinstallato. Non esiste alcun meccanismo per concatenare i filtri. Di conseguenza, il nuovo gestore di filtro è responsabile della replica di tutte le funzionalità necessarie del filtro precedente.
-   Gli IFilter, i Word breaker e gli stemmer per la ricerca di Windows vengono eseguiti nel contesto di sicurezza locale. Devono essere scritti per gestire i buffer e per eseguire lo stack in modo corretto. Tutte le copie di stringhe devono avere controlli espliciti per evitare sovraccarichi del buffer. Verificare sempre la dimensione allocata del buffer e verificare le dimensioni dei dati rispetto alle dimensioni del buffer. I sovraccarichi del buffer sono una tecnica comune per sfruttare il codice che non impone restrizioni per le dimensioni del buffer.
-   I componenti [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter), Word breaker e stemmer non devono mai chiamare la funzione [ExitProcess Function](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) o un'API simile che termina un processo e tutti i relativi thread.
-   Non allocare o liberare risorse nel punto di ingresso DllMain. Questo può causare errori durante i test di stress con risorse insufficienti.
-   Codificare tutti gli oggetti in modo che siano thread-safe. Windows Search chiama una qualsiasi istanza di un Word breaker o uno stemmer in un thread alla volta, ma può chiamare più istanze contemporaneamente tra più thread.
-   Evitare di creare file temporanei o scrivere nel registro di sistema.
-   Se si usa il compilatore Microsoft Visual C++, assicurarsi di compilare l'applicazione con l'opzione **/GS** . L'opzione **/GS** viene usata per rilevare i sovraccarichi del buffer. L'opzione/GS inserisce i controlli di sicurezza nel codice compilato. Per ulteriori informazioni, vedere [DllGetClassObject Function](https://msdn.microsoft.com/library/8dbf701c(vs.71).aspx)  / **GS** (buffer Security Check) nella sezione Visual C++ opzioni del compilatore di Platform SDK.

## <a name="additional-resources"></a>Risorse aggiuntive

-   Nell'esempio [IFilterSample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample) viene illustrato come creare una classe di base IFilter per implementare l'interfaccia [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) .
-   Per una panoramica del processo di indicizzazione, vedere [il processo di indicizzazione](-search-indexing-process-overview.md).
-   Per una panoramica dei tipi di file, vedere [tipi di file](../shell/fa-file-types.md).
-   Per eseguire query sugli attributi di associazione file per un tipo di file, vedere [PerceivedTypes, SystemFileAssociations e registrazione dell'applicazione](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sviluppo di gestori di filtri](-search-ifilter-conceptual.md)
</dt> <dt>

[Informazioni sui gestori di filtro in Windows Search](-search-ifilter-about.md)
</dt> <dt>

[Restituzione di proprietà da un gestore di filtro](-search-ifilter-property-filtering.md)
</dt> <dt>

[Gestori di filtri forniti con Windows](-search-ifilter-implementations.md)
</dt> <dt>

[Implementazione di gestori di filtro in Windows Search](-search-ifilter-constructing-filters.md)
</dt> <dt>

[Registrazione di gestori di filtro](-search-ifilter-registering-filters.md)
</dt> <dt>

[Test di gestori filtro](-search-ifilter-testing-filters.md)
</dt> </dl>

 

 
