---
description: I gestori di filtro, che sono implementazioni dell'interfaccia IFilter, analizzano i documenti per il testo e le proprietà.
ms.assetid: 2ee9ea19-ae03-4f14-8f06-f8aa670e204e
title: Informazioni sui gestori di filtro in Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e49cc1d3e479ae03645665618c60a33bdcfe19ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525519"
---
# <a name="understanding-filter-handlers-in-windows-search"></a>Informazioni sui gestori di filtro in Windows Search

I gestori di filtro, che sono implementazioni dell'interfaccia [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) , analizzano i documenti per il testo e le proprietà. I gestori di filtro estraggono i blocchi di testo da questi elementi, filtrando la formattazione incorporata e mantenendo le informazioni sulla posizione del testo. Estraggono anche i blocchi di valori, che sono proprietà del documento. **IFilter** è la base per la creazione di applicazioni di livello superiore, ad esempio indicizzatori di documenti e visualizzatori indipendenti dall'applicazione.

Questo argomento è organizzato nel modo seguente:

- [Informazioni sull'interfaccia IFilter](#about-the-ifilter-interface)
  - [Processo di isolamento](#isolation-process)
  - [Dll IFilter](#ifilter-dlls)
  - [Struttura IFilter](#ifilter-structure)
  - [Codice nativo](#native-code)
- [Ricerca dell'identificatore di classe IFilter](#finding-the-ifilter-class-identifier)
  - [IFilter:: GetChunk e identificatori di codice delle impostazioni locali](#ifiltergetchunk-and-locale-code-identifiers)
- [Risorse aggiuntive](#additional-resources)
- [Argomenti correlati](#related-topics)

## <a name="about-the-ifilter-interface"></a>Informazioni sull'interfaccia IFilter

Microsoft Windows Search USA i filtri per estrarre il contenuto degli elementi da includere in un indice full-text. È possibile estendere la ricerca di Windows per indicizzare i tipi di file nuovi o proprietari scrivendo i filtri per estrarre il contenuto e i gestori delle proprietà per estrarre le proprietà dei file.

L'interfaccia [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) è progettata per soddisfare le esigenze specifiche dei motori di ricerca full-text. I motori di ricerca full-text come Windows Search chiamano i metodi **IFilter** per estrarre le informazioni relative a testo e proprietà e aggiungerle a un indice. Windows Search interrompe i risultati del metodo [**IFilter:: GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext) restituito in parole, li normalizza e li salva in un indice. Se disponibile, il motore di ricerca usa l'identificatore del codice lingua (LCID) di un blocco di testo per eseguire la normalizzazione e la normalizzazione delle parole specifiche della lingua.

Windows Search usa tre funzioni, descritte nella tabella seguente, per accedere ai gestori di filtri registrati (implementazioni dell'interfaccia [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) ). Queste funzioni sono particolarmente utili quando si caricano e si associano al gestore di filtro di un oggetto incorporato.

| Funzione               | Descrizione                                                                                                                                                                                               |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| LoadIFilter            | Ottiene un puntatore all' [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) più adatto per il tipo di contenuto specificato.                                                                                            |
| BindIFilterFromStorage | Ottiene un puntatore al [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) che è più adatto per il contenuto contenuto in un oggetto di [interfaccia IStorage](/windows/win32/api/objidl/nn-objidl-istorage) . |
| BindIFilterFromStream  | Ottiene un puntatore al [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) che è più adatto per un identificatore di classe specificato (CLSID) recuperato da una variabile di flusso.                                                 |

L'interfaccia [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) ha cinque metodi, descritti nella tabella seguente.

| Metodo                                                    | Descrizione                                                                                                        |
|-----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [**IFilter:: init**](/windows/win32/api/filter/nf-filter-ifilter-init)          | Inizializza una sessione di filtro.                                                                                   |
| [**IFilter:: GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk)     | Posiziona [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) all'inizio del primo o del blocco successivo e restituisce un descrittore. |
| [**IFilter:: GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext)       | Recupera il testo dal blocco corrente.                                                                             |
| [**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue)     | Recupera i valori dal blocco corrente.                                                                           |
| [**IFilter:: BindRegion**](/windows/win32/api/filter/nf-filter-ifilter-bindregion) | Recupera un'interfaccia che rappresenta la parte specificata dell'oggetto. Riservato per utilizzi futuri.                      |

### <a name="isolation-process"></a>Processo di isolamento

Windows Search esegue IFilters nel contesto di sicurezza del sistema locale con diritti limitati. In questo processo di isolamento host [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) viene rimosso un numero di diritti:

- Codice con restrizioni
- Tutti
- Locale
- Interattività
- Utenti autenticati
- Utenti predefiniti
- ID di sicurezza (SID) degli utenti

La rimozione di questi diritti indica che l'interfaccia [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) non ha accesso al sistema del disco o alla rete o a qualsiasi interfaccia utente o funzione degli Appunti. Inoltre, il processo di isolamento viene eseguito in un oggetto processo che impedisce la creazione di processi figlio e impone un limite di 100 MB nel working set. il processo di isolamento host dell'interfaccia **IFilter** aumenta la stabilità della piattaforma di indicizzazione, a causa della possibilità di applicare erroneamente filtri di terze parti.

> [!NOTE]  
> È necessario scrivere i gestori di filtro per gestire i buffer e lo stack correttamente. Tutte le copie di stringhe devono avere controlli espliciti per evitare sovraccarichi del buffer. Verificare sempre la dimensione allocata del buffer. È consigliabile testare sempre le dimensioni dei dati rispetto alle dimensioni del buffer.

### <a name="ifilter-dlls"></a>Dll IFilter

[**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) Le DLL implementano l'interfaccia **IFilter** per consentire a un client di estrarre informazioni sul valore di testo e proprietà da un tipo di file, una classe o un tipo percepito. Il processo di filtro di ricerca di Windows **SearchFilterHost.exe** viene associato all' **IFilter** registrato per la classe, il tipo percepito o l'estensione del nome dell'elemento.

### <a name="ifilter-structure"></a>Struttura IFilter

Ogni [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) è un file dll che implementa un server in-process Component Object Model (com) per fornire le funzionalità di filtro specificate. Nella figura seguente viene illustrata la struttura complessiva di una tipica dll **IFilter** . Un esempio più complesso potrebbe implementare più di una classe **IFilter** .

![diagramma della struttura di una dll IFilter tipica](images/ifilter-structure.png)

### <a name="native-code"></a>Codice nativo

I filtri devono essere scritti in codice nativo a causa di potenziali problemi di controllo delle versioni di Common Language Runtime (CLR) con il processo di esecuzione di più componenti aggiuntivi. In Windows 7 e versioni successive, i filtri scritti nel codice gestito vengono bloccati in modo esplicito.

## <a name="finding-the-ifilter-class-identifier"></a>Ricerca dell'identificatore di classe IFilter

La classe della dll [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) è registrata nella chiave del registro di sistema PersistentHandler. Nell'esempio seguente, per i file HTML, viene illustrato come trovare la dll **IFilter** per un documento HTML. Questo esempio segue una logica simile a quella usata dal sistema per trovare l' **IFilter** associato a un elemento.

1. Controllare se l'estensione per il tipo di file che la DLL filtra dispone di un PersistentHandler registrato nella voce del registro di sistema \\ HKEY \_ Local \_ Machine \\ software \\ Classes. Lasciare che la chiave sia `Value1` . Se la voce esiste già, andare al passaggio 4 di questa procedura e usarla `Value1` in tale chiave. I valori sono di tipo REG \_ SZ.

```
    \HKEY_LOCAL_MACHINE
       SOFTWARE
          Classes
             .htm
                PersistentHandler
                   {EEC97550-47A9-11CF-B952-00AA0051FE20}
```

2. In alternativa, se non è presente un PersistentHandler registrato per l'estensione, trovare il CLSID associato al tipo di documento nella voce del registro di sistema \\ HKEY \_ Local \_ Machine \\ software \\ Classes. Lasciare che la chiave sia `Value2` .

```
    \HKEY_LOCAL_MACHINE
       SOFTWARE
          Classes
             htmlfile
                 = Class for WWW HTML files
                CLSID
                   {25336920-03F9-11CF-8FD0-00AA00686F13}
```

3. Determinare se un PersistentHandler è registrato per il CLSID. Utilizzando `Value2` determinato nel passaggio 2, trovare PersistentHandler per le \\ \_ \_ classi software del computer locale HKEY \\ \\ \\ CLSID \\ value2 voce. Lasciare che la chiave sia `Value3` .

```
    \HKEY_LOCAL_MACHINE
       SOFTWARE
          Classes
             htmlfile
                 = Class for WWW HTML files
                PersistentHandler
                   {EEC97550-47A9-11CF-B952-00AA0051FE20}
```

4. Determinare il GUID del gestore persistente [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) . Utilizzando `Value1` e `Value3` , trovare il GUID del gestore permanente **IFilter** per il tipo di documento. Il valore nella voce del registro \\ di sistema HKEY \_ Local \_ Machine \\ software \\ classi \\ CLSID \\ Value1 o 3 \\ PersistentAddinsRegistered \\ 89BCB740-6119-101A-BCB7-00DD010655AF "/> restituisce il GUID PersistentHandler **IFilter** per questo tipo di documento. Lasciare che la chiave sia `Value4` . In questo esempio il GUID dell'interfaccia **IFilter** è 89BCB740-6119-101A-BCB7-00DD010655AF.

```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Classes
             {EEC97550-47A9-11CF-B952-00AA0051FE20}
                 = HTML File Persistent Handler
                    Data type         REG_SZ
                        PersistentAddinsRegistered
                        {89BCB740-6119-101A-BCB7-00DD010655AF}

                    Data type         REG_SZ
                        default = {E0CA5340-4534-11CF-B952-00AA0051FE20}
```

> [!NOTE]  
> In questo esempio la dll [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) per i documenti HTML è nlhtml.dll.

### <a name="ifiltergetchunk-and-locale-code-identifiers"></a>IFilter:: GetChunk e identificatori di codice delle impostazioni locali

Il valore LCID del testo può essere modificato all'interno di un singolo file. Ad esempio, il testo di un manuale di istruzioni potrebbe essere alternativo tra inglese (en-US) e spagnolo (es) oppure il testo potrebbe includere una singola parola in una lingua diversa dalla lingua primaria. In entrambi i casi, l' [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) deve iniziare un nuovo blocco ogni volta che viene modificato l'identificatore LCID. Poiché l'identificatore LCID viene utilizzato per scegliere un Word breaker appropriato, è molto importante identificarlo correttamente. Se **IFilter** non è in grado di determinare le impostazioni locali del testo, deve restituire un identificatore LCID pari a zero con il blocco. Se si restituisce un LCID pari a zero, Windows Search utilizzerà la tecnologia del rilevamento automatico del linguaggio (LAD) per determinare l'ID delle impostazioni locali del blocco. Se la ricerca di Windows non è in grado di trovare una corrispondenza, per impostazione predefinita vengono predefinite le impostazioni locali predefinite del sistema (chiamando la funzione [GetSystemDefaultLocaleName Function](/windows/win32/api/winnls/nf-winnls-getsystemdefaultlocalename) ). Per altre informazioni, vedere [**IFilter:: GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk), [**chunk \_ BREAKTYPE**](/windows/win32/api/filter/ne-filter-chunk_breaktype), [**CHUNKSTATE**](/windows/win32/api/filter/ne-filter-chunkstate)e [**Stat \_ chunk**](/windows/win32/api/filter/ns-filter-stat_chunk).

Se si controlla il formato del file e attualmente non contiene informazioni sulle impostazioni locali, è necessario aggiungere una funzionalità utente per abilitare l'identificazione delle impostazioni locali corretta. L'utilizzo di un Word breaker non corrispondente può comportare una scarsa esperienza di query per l'utente. Per ulteriori informazioni, vedere [**IWordBreaker**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordbreaker).

> [!NOTE]  
> I filtri sono associati ai tipi di file, come indicato dalle estensioni dei nomi di file, dai tipi MIME o dai CLSID. Mentre un filtro può gestire più tipi di file, ogni tipo funziona con un solo filtro.

## <a name="additional-resources"></a>Risorse aggiuntive

- Nell'esempio di codice [IFilterSample](-search-sample-ifiltersample.md) , disponibile in [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample7), viene illustrato come creare una classe di base IFilter per implementare l'interfaccia [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) .
- Per una panoramica del processo di indicizzazione, vedere [il processo di indicizzazione](-search-indexing-process-overview.md).
- Per una panoramica dei tipi di file, vedere [tipi di file](../shell/fa-file-types.md).
- Per eseguire query sugli attributi di associazione file per un tipo di file, vedere [PerceivedTypes, SystemFileAssociations e registrazione dell'applicazione](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).

## <a name="related-topics"></a>Argomenti correlati

[Sviluppo di gestori di filtri](-search-ifilter-conceptual.md)

[Procedure consigliate per la creazione di gestori di filtro in Windows Search](-search-3x-wds-extidx-filters.md)

[Restituzione di proprietà da un gestore di filtro](-search-ifilter-property-filtering.md)

[Gestori di filtri forniti con Windows](-search-ifilter-implementations.md)

[Implementazione di gestori di filtro in Windows Search](-search-ifilter-constructing-filters.md)

[Registrazione di gestori di filtro](-search-ifilter-registering-filters.md)

[Test di gestori filtro](-search-ifilter-testing-filters.md)
