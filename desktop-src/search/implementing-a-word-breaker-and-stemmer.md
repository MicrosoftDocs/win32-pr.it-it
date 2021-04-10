---
description: Microsoft fornisce Word breaker e stemmer per diversi linguaggi. In questo argomento viene descritto come implementare e utilizzare Word breaker e stemmer personalizzati per le lingue e le impostazioni locali oltre a quelle fornite da Microsoft.
ms.assetid: 47768691-7071-440e-bfbf-975713880c00
title: Implementazione di un Word breaker e uno stemmer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bd4f4e3210e7f4e17bb035115fd694656cc6e6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049382"
---
# <a name="implementing-a-word-breaker-and-stemmer"></a>Implementazione di un Word breaker e uno stemmer

Microsoft fornisce Word breaker e stemmer per diversi linguaggi. In questo argomento viene descritto come implementare e utilizzare Word breaker e stemmer personalizzati per le lingue e le impostazioni locali oltre a quelle fornite da Microsoft.

> [!Note]
> Al 2018 luglio è stata apportata una modifica alla sicurezza di Windows Server 2019 che impedisce il caricamento delle dll senza una firma Microsoft da SearchIndexer.exe. Di conseguenza, Windows Server 2019 non supporta più Word breaker personalizzati non Microsoft firmati. 

Questo argomento è organizzato nel modo seguente:

-   [Registrazione di una DLL di risorse della lingua](#registering-a-language-resource-dll)
-   [Registrazione di una lingua](#registering-a-language-resource-dll)
-   [Implementazione di un Word Becher](#implementing-a-word-beaker)
    -   [WordSink e PhraseSink](#wordsink-and-phrasesink)
    -   [Interruzioni](#breaks)
    -   [Scalabilità, Performancy e sicurezza](#scalability-performancy-and-security)
-   [Implementazione di uno stemmer](#implementing-a-stemmer)
    -   [Scalabilità, Performancy e sicurezza](#scalability-performancy-and-security)
-   [Argomenti correlati](#related-topics)

## <a name="registering-a-language-resource-dll"></a>Registrazione di una DLL di risorse della lingua

Ogni DLL di risorse della lingua deve implementare ed esportare i punti di ingresso seguenti. La DLL può essere registrata in qualsiasi cartella.

-   DllMain è il punto di ingresso standard della DLL.
-   DllRegisterServer registra la DLL nel registro di sistema, ad esempio `regsvr32.exe %SystemRoot%\MyFolder\wordbreaker.dll`
-   DllCanUnloadNow consente ai client di chiamare questo punto di ingresso tramite Component Object Model (COM) per determinare se è possibile scaricare la DLL di risorse della lingua.
-   DllUnRegisterServer rimuove la DLL dal registro di sistema.

## <a name="registering-a-language"></a>Registrazione di una lingua

Il registro di sistema contiene voci specifiche della lingua per la lingua da indicizzare e queste voci controllano le parti dei processi di indicizzazione e query specifiche della lingua. Queste voci del registro di sistema si trovano nella seguente chiave del registro di sistema.

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         ContentIndex
            Control
               Language
                  
```

## <a name="implementing-a-word-beaker"></a>Implementazione di un Word Becher

I Word breaker implementano [**IWordBreaker**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordbreaker). Il metodo [**IWordBreaker:: BreakText**](/windows/desktop/api/Indexsrv/nf-indexsrv-iwordbreaker-breaktext) esegue tutte le operazioni di elaborazione e analisi del testo. Per implementare un componente word breaker, è necessario disporre di euristica per la lingua. Sono incluse informazioni sulla sintassi e la morfologia. Potrebbe essere necessario anche un elenco di parole da escludere o includere. Si compila il file di parole non significative per le impostazioni locali della lingua dall'elenco di parole escluse. Per ulteriori informazioni sulle considerazioni linguistiche e sul modo in cui queste considerazioni influiscono sulle implementazioni del Word breaker, vedere [considerazioni linguistiche e Unicode](linguistic-and-unicode-considerations.md).

Lo scopo principale di [**IWordBreaker:: BreakText**](/windows/desktop/api/Indexsrv/nf-indexsrv-iwordbreaker-breaktext) è elaborare continuamente il testo dall' [**\_ origine del testo**](/windows/win32/api/indexsrv/ns-indexsrv-text_source) fino a quando non viene elaborato tutto il testo o finché il Word breaker non rileva un errore. In questo ciclo di elaborazione dati, **IWordBreaker:: BreakText** chiama i metodi di analisi e di utilità che eseguono attività specifiche per tale processo. Il Word breaker tedesco, ad esempio, può gestire parole composte, mentre il Word breaker francese può elaborare [segni diacritici](surface-form-normalization.md) o [clitici](surface-form-normalization.md). Le funzioni specifiche eseguite dal Word breaker e la strategia utilizzata per l'esecuzione di queste attività dipendono interamente dai requisiti per tale lingua.

Quando si interrompe il testo, i Word breaker identificano i moduli "alternativi" per le parole che possono avere più rappresentazioni. Nessuna relazione semantica è implicita tra le parole generate. Infatti, la parola originale non può essere inclusa nell'elenco delle alternative. I formati alternativi vengono salvati nella stessa posizione nell'indice della parola originale per indicare che sono identici.

Quando un documento viene incluso nell'indice, a ogni parola viene assegnato un valore integer che rappresenta l'offset o la distanza della parola dall'inizio di un documento. La distanza relativa tra le parole in una query viene confrontata con gli offset archiviati nell'indice full-text. La query "Where is the Kyle ' s Document" corrisponde a qualsiasi documento con "Where" at offset n, "is" at n + 1, "Kyle ' s" at n + 2 e "Document" at n + 3. "Dov'è il documento di Kyle archiviato nella data-base?" è rappresentato come:



|       |     |                        |          |       |     |     |                               |
|-------|-----|------------------------|----------|-------|-----|-----|-------------------------------|
| Where | is  | Kyle Kyle<br/> | documento | campo | in ingresso  | il | data base database<br/> |



 

In questo esempio il Word breaker archivia moduli alternativi per "Kyle" ("Kyle") e "database" ("data base") nell'indice. Il Word breaker genera e archivia parole alternative durante il processo di creazione dell'indice nelle condizioni seguenti:

-   Se una parola alternativa viene probabilmente visualizzata come una singola parola in una query
-   Se uno stemmer non è in grado di derivare la parola originale dall'alternativa

La generazione di moduli Word alternativi aumenta il numero di modi in cui le query rappresentano e corrispondono a una frase, come illustrato nelle varianti seguenti:

1.  Dove è il documento Kyle archiviato nel database
2.  Dove si trova il documento di Kyle archiviato nel database
3.  Dove è il documento Kyle archiviato nel database
4.  Dove si trova il documento di Kyle archiviato nel database

### <a name="wordsink-and-phrasesink"></a>WordSink e PhraseSink

I Word breaker utilizzano gli oggetti [**IWordSink**](iwordsink.md) e [**IPhraseSink**](/windows/win32/api/indexsrv/nn-indexsrv-iphrasesink) per raccogliere e archiviare tutte le parole e le frasi estratte dal testo. Un Word breaker archivia le parole in un modulo il più vicino possibile al modulo Word originale nel documento. **IPhraseSink** archivia le frasi in fase di query. Le frasi migliorano la pertinenza dei risultati delle query perché le sequenze più lunghe di parole sono più rare e forniscono una maggiore distinzione rispetto a frasi più piccole. Quando l'indicizzatore posiziona una frase in **IPhraseSink** in fase di query, crea un'istanza del Word breaker per suddividere la frase in parole. L'indicizzatore valuta quindi la frase controllando se le parole nella frase si trovano adiacenti l'una all'altra nell'indice. Se, ad esempio, si verifica "ABCD" nell'indice nelle posizioni *x*, *x*+ 1, *x*+ 2 e *x*+ 3, la frase corrispondente si verificherà se in una query viene inviata una sottostringa adiacente di "abcd". Questa strategia è efficace per i Word breaker basati su caratteri che dividono le frasi e le parole lunghe durante la creazione dell'indice e generano frasi durante la fase di esecuzione della query.

### <a name="breaks"></a>Interruzioni

Le interruzioni sono gli spazi tra le parole. Gli spazi vuoti, la punteggiatura, la formattazione o solo la natura del linguaggio stesso possono causare interruzioni. Sono disponibili quattro tipi diversi di interruzioni utilizzate dall'indicizzatore: end of Word (EOW), end of frase (EOS), end of Paragraph (EOP) e End of Chapter (EDC). L'EOW Break è l'opzione predefinita. Dopo ogni token, ogni Break indica una distanza semantica diversa tra le parole su entrambi i lati. Le parole separate da EOW hanno il collegamento semantico più stretto, seguito da EOS, EOP e EDC. Più chiamate a [**IWordSink::P utbreak**](iwordsink-putbreak.md) sono cumulative e sono analoghe all'inserimento di parole o frasi null.

### <a name="scalability-performancy-and-security"></a>Scalabilità, Performancy e sicurezza

Il modo in cui il Word breaker risponde alle chiamate simultanee è in gran parte determinato dalla scelta del modello di Threading. L'indicizzatore è un'applicazione a thread singolo. Per il funzionamento dei word breaker in un ambiente a thread singolo, è necessario scrivere i Word breaker usando un modello di threading "libero" o "both". I Word breaker non devono registrarsi a COM utilizzando il modello di threading "Apartment".

È consigliabile che i Word breaker evitino gli Stati globali e memorizzino i dati nell'istanza per il Word breaker. L'unico contenuto che deve essere archiviato nell'implementazione del Word breaker riguarda i parametri *fQuery* e *ulMaxTokenSize*. I Word breaker non devono essere più di due volte più lenti rispetto al benchmark stabilito dal Word breaker per la lingua inglese. Le prestazioni del Word breaker dovrebbero inoltre migliorare con una maggiore capacità di hardware.

I Word breaker per l'indicizzatore vengono eseguiti nel contesto di sicurezza del sistema locale. Devono essere scritti per gestire i buffer e per eseguire lo stack in modo corretto. Tutte le copie di stringhe devono avere controlli espliciti per evitare sovraccarichi del buffer. Verificare sempre la dimensione allocata del buffer e verificare le dimensioni dei dati rispetto alle dimensioni del buffer. I Word breaker non possono presupporre che il testo passato al metodo [**IWordBreaker:: BreakText**](/windows/desktop/api/Indexsrv/nf-indexsrv-iwordbreaker-breaktext) sia ben formato. Per ulteriori informazioni sulla risoluzione dei problemi relativi ai Word breaker, vedere [risoluzione dei problemi relativi a risorse e procedure consigliate](troubleshooting-language-resources.md).

## <a name="implementing-a-stemmer"></a>Implementazione di uno stemmer

Gli stemmer implementano l'interfaccia [**IStemmer**](/windows/desktop/api/Indexsrv/nn-indexsrv-istemmer) . Il metodo [**IStemmer:: GenerateWordForms**](/windows/desktop/api/Indexsrv/nf-indexsrv-istemmer-generatewordforms) genera un elenco di forme di Word flesse per una determinata parola di input. Per implementare un componente dello stemmer, è necessario avere l'euristica del linguaggio per la lingua. Sono incluse informazioni sulla morfologia. Potrebbe essere necessario anche un elenco di parole da escludere o includere. Per ulteriori informazioni sulle considerazioni linguistiche e sul modo in cui queste considerazioni influiscono sulle implementazioni dello stemmer, vedere [considerazioni relative a lingue e Unicode](linguistic-and-unicode-considerations.md).

È consigliabile che gli stemmer non generino il genitivo, o il caso possessivo, per le parole. Ad esempio, "David" non viene generato come forma alternativa per "David". Il Word breaker genera "David" e "David" durante l'analisi di "David".

Lo stemmer usa l'oggetto [IWordFormSink](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) per raccogliere l'elenco di parole alternative. [**IWordFormSink::P utword**](iwordformsink-putword.md) genera la parola finale dallo stemmer. In tutti i casi, la parola finale corrisponde alla parola di input di [**IStemmer:: GenerateWordForms**](/windows/desktop/api/Indexsrv/nf-indexsrv-istemmer-generatewordforms). Ad esempio, data la parola "swim", lo stemmer genera le seguenti forme di Word: "nuoto", "nuotatore", "nuota", "nuotata" e "nuotata" tramite chiamate a [**IWordFormSink::P utaltword**](iwordformsink-putphrase.md). Lo stemmer genera "swim" tramite **IWordFormSink::P utword**.

### <a name="scalability-performancy-and-security"></a>Scalabilità, Performancy e sicurezza

Gli stemmer, come i Word breaker, devono usare un modello di threading "libero" e registrarsi con COM con il modello di threading impostato su "Free" o "both". Windows Search chiama istanze separate dello stemmer da diversi thread contemporaneamente. Gli stemmer devono quindi avere dati di istanza minimi.

L'accuratezza dello stemmer ha un impatto significativo sulla rilevanza delle query. Se lo stemmer deriva il testo in modo errato, le query possono restituire risultati imprevedibili e non accurati. Gli stemmer devono gestire centinaia di query al secondo senza influire negativamente sulle prestazioni di esecuzione delle query. Le prestazioni dello stemmer dovrebbero migliorare con una maggiore capacità hardware. Per informazioni sulla risoluzione dei problemi relativi agli stemmer, vedere [risoluzione dei problemi relativi a risorse di linguaggio e procedure consigliate](troubleshooting-language-resources.md).

Gli stemmer per la ricerca di Windows vengono eseguiti nel contesto di sicurezza locale. Devono essere scritti per gestire i buffer e per eseguire lo stack in modo corretto. Tutte le copie di stringhe devono avere controlli espliciti per evitare sovraccarichi del buffer. Verificare sempre la dimensione allocata del buffer e verificare le dimensioni dei dati rispetto alle dimensioni del buffer.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Estensione delle risorse della lingua](extending-language-resources-in-windows-search.md)
</dt> <dt>

[Informazioni sui componenti delle risorse della lingua](understanding-language-resource-components.md)
</dt> <dt>

[Considerazioni linguistiche e Unicode](linguistic-and-unicode-considerations.md)
</dt> <dt>

[Risoluzione dei problemi relativi a risorse di linguaggio e procedure consigliate](troubleshooting-language-resources.md)
</dt> </dl>

 

 
