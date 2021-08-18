---
description: Informazioni sulle procedure consigliate per la creazione di gestori di filtri in Windows ricerca. La ricerca usa i filtri per estrarre gli elementi da includere in un indice full-text.
ms.assetid: 7b86a1b4-c8a9-400d-a9f1-a3b821c0269d
title: Procedure consigliate per i gestori di filtri nella Windows ricerca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8320cf0f85bf86f7d61df09437271af67d0e4096fc3a917d037914854c9bad3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118463700"
---
# <a name="best-practices-for-creating-filter-handlers-in-windows-search"></a>Procedure consigliate per la creazione di gestori di filtri in Windows ricerca

Microsoft Windows Ricerca di Microsoft usa filtri per estrarre il contenuto degli elementi da includere in un indice full-text. È possibile estendere Windows ricerca per indicizzare tipi di file nuovi o proprietari scrivendo gestori di filtri per estrarre il contenuto e gestori di proprietà per estrarre le proprietà dei file. I filtri sono associati ai tipi di file, come denotato da estensioni di file, tipi MIME o identificatori di classe (CLSID). Mentre un filtro può gestire più tipi di file, ogni tipo funziona con un solo filtro.

In questo argomento sono incluse le sezioni seguenti:

-   [Codice nativo](#native-code)
-   [Procedure di sicurezza del codice per Windows ricerca](#secure-code-practices-for-windows-search)
-   [Risorse aggiuntive](#additional-resources)
-   [Argomenti correlati](#related-topics)

## <a name="native-code"></a>Codice nativo

In Windows 7 e versioni successive i filtri scritti in codice gestito vengono bloccati in modo esplicito. I filtri DEVONO essere scritti in codice nativo a causa di potenziali problemi di controllo delle versioni di CLR con il processo in cui vengono eseguiti più componenti aggiuntivi.

## <a name="secure-code-practices-for-windows-search"></a>Procedure di sicurezza del codice per Windows ricerca

Di seguito sono riportate le procedure per la scrittura di applicazioni sicure da usare con Windows ricerca.

**Per le applicazioni di query:**

-   Quando si scrivono client di ricerca, è consigliabile scegliere l'API che viene eseguita in un contesto di sicurezza che consenta all'utente il privilegio minimo. Ad esempio, le pagine ASP possono usare l'oggetto query IXSSO, che viene eseguito come processo utente.

**Per IFilter e risorse della lingua:**

-   Se viene installato un nuovo gestore di filtri per un tipo di file in sostituzione di una registrazione di filtro esistente, il programma di installazione deve salvare la registrazione corrente e ripristinarla se il nuovo gestore di filtri viene disinstallato. Non esiste alcun meccanismo per concatenare i filtri. Di conseguenza, il nuovo gestore di filtri è responsabile della replica di tutte le funzionalità necessarie del filtro precedente.
-   I Filtri IFilter, word breaker e stemmer per Windows ricerca vengono eseguiti nel contesto di sicurezza locale. Devono essere scritti per gestire i buffer e lo stack correttamente. Tutte le copie di stringhe devono avere controlli espliciti per proteggersi dai sovraccarichi del buffer. È sempre necessario verificare le dimensioni allocate del buffer e verificare le dimensioni dei dati rispetto alle dimensioni del buffer. I sovraccarichi del buffer sono una tecnica comune per sfruttare il codice che non applica restrizioni relative alle dimensioni del buffer.
-   [**I componenti IFilter,**](/windows/win32/api/filter/nn-filter-ifilter)word breaker e stemmer non devono mai chiamare la funzione [ExitProcess](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) o un'API simile che termina un processo e tutti i relativi thread.
-   Non allocare o liberare risorse nel punto di ingresso DllMain. Ciò può causare errori durante i test di stress con risorse basse.
-   Codificare tutti gli oggetti in modo che siano thread-safe. Windows La ricerca chiama qualsiasi istanza di un word breaker o stemmer in un thread alla volta, ma può chiamare più istanze contemporaneamente tra più thread.
-   Evitare di creare file temporanei o scrivere nel Registro di sistema.
-   Se si usa il compilatore Microsoft Visual C++, assicurarsi di compilare l'applicazione usando **l'opzione /GS.** **L'opzione /GS** viene usata per rilevare i sovraccarichi del buffer. L'opzione /GS inserisce i controlli di sicurezza nel codice compilato. Per altre informazioni, vedere [DllGetClassObject Function](https://msdn.microsoft.com/library/8dbf701c(vs.71).aspx)  / **GS** (Buffer Security Check) nella sezione Visual C++ Compiler Options (Opzioni del compilatore di Visual C++) di Platform SDK.

## <a name="additional-resources"></a>Risorse aggiuntive

-   [L'esempio IFilterSample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample) illustra come creare una classe di base IFilter per l'implementazione [**dell'interfaccia IFilter.**](/windows/win32/api/filter/nn-filter-ifilter)
-   Per una panoramica del processo di indicizzazione, vedere [Processo di indicizzazione.](-search-indexing-process-overview.md)
-   Per una panoramica dei tipi di file, vedere [Tipi di file.](../shell/fa-file-types.md)
-   Per eseguire query su attributi di associazione di file per un tipo di file, vedere [PerceivedTypes, SystemFileAssociations e Registrazione dell'applicazione.](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85))

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sviluppo di gestori di filtri](-search-ifilter-conceptual.md)
</dt> <dt>

[Informazioni sui gestori di filtri Windows ricerca](-search-ifilter-about.md)
</dt> <dt>

[Restituzione di proprietà da un gestore di filtri](-search-ifilter-property-filtering.md)
</dt> <dt>

[Gestori di filtri forniti con Windows](-search-ifilter-implementations.md)
</dt> <dt>

[Implementazione di gestori di filtri in Windows ricerca](-search-ifilter-constructing-filters.md)
</dt> <dt>

[Registrazione di gestori di filtri](-search-ifilter-registering-filters.md)
</dt> <dt>

[Test dei gestori di filtri](-search-ifilter-testing-filters.md)
</dt> </dl>

 

 
