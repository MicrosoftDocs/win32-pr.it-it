---
description: Le risorse della lingua sono costituite da Word breaker e stemmer che estendono le funzionalità di compilazione e query degli indici a nuove lingue e impostazioni locali.
ms.assetid: 7963805e-e279-42cf-ba95-f81a7de8e68e
title: Informazioni sui componenti delle risorse della lingua
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e03c9294eaf6e50de024b866372093a0359fc79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525441"
---
# <a name="understanding-language-resource-components"></a>Informazioni sui componenti delle risorse della lingua

Le risorse della lingua sono costituite da Word breaker e stemmer che estendono le funzionalità di compilazione e query degli indici a nuove lingue e impostazioni locali. I Word breaker vengono utilizzati durante la creazione e l'esecuzione di query degli indici. Gli stemmer vengono utilizzati solo per le query. Windows Search usa le DLL delle risorse di linguaggio per l'associazione alle implementazioni [**IWordBreaker**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordbreaker) e [**IStemmer**](/windows/desktop/api/Indexsrv/nn-indexsrv-istemmer) per le impostazioni locali di una lingua specifica.

Questo argomento è organizzato nel modo seguente:

-   [Informazioni sulle risorse della lingua](#about-language-resources)
-   [Word-interruzioni](#word-breaking)
-   [Derivanti](#stemming)
-   [Normalization](#normalization)
-   [Parole non significative](#noise-words)
-   [Argomenti correlati](#related-topics)

## <a name="about-language-resources"></a>Informazioni sulle risorse della lingua

Windows Search usa un filtro (un'implementazione dell'interfaccia [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) ) e [**ILoadFilter**](/windows/desktop/api/filtereg/nn-filtereg-iloadfilter) per accedere a un documento nel formato nativo. Il componente [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) estrae il contenuto di testo, le proprietà e la formattazione dal documento. [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) identifica le impostazioni locali del documento che sta filtrando. Il componente di indicizzazione richiama il Word breaker appropriato per le impostazioni locali. Se non è disponibile alcun, il componente di indicizzazione richiama il Word breaker neutro. Il Word breaker riceve, da un [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter), un flusso di input di caratteri Unicode che il Word breaker analizza per produrre singole parole e frasi. Il Word breaker normalizza anche i formati di data e ora. L'indicizzatore normalizza le parole prodotte dal Word breaker convertendo le parole in lettere maiuscole. L'indicizzatore Salva le parole maiuscole nell'indice full-text, ad eccezione delle parole non significative identificate per le impostazioni locali.

Nella tabella seguente sono elencate le azioni e i risultati corrispondenti per la frase "nella figura 1 viene illustrato il ruolo delle risorse di lingua per la ricerca di Windows durante il processo di creazione dell'indice".



| Azione                  | Testo risultante                                                                                                               |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------|
| Testo originale           | Nella figura 1 viene illustrato il ruolo delle risorse di lingua per la ricerca di Windows durante il processo di creazione dell'indice.                    |
| Filtro               | Nella figura 1 viene illustrato il ruolo delle risorse di lingua per la ricerca di Windows durante il processo di creazione dell'indice.                    |
| Word-interruzioni           | Figura 1, illustra,,, Role, of, language, Resources, for, Windows, Search, while,, index, Creation, process, EOS |
| Normalization           | FIGURA 1, ILLUSTRA,,, ROLE, OF, LANGUAGE, RESOURCES, WINDOWS, SEARCH, WHILE,,, INDEX, CREATION, PROCESS           |
| Rimozione di parole non significative      | FIGURA, ILLUSTRA, ROLE, LANGUAGE, RESOURCES, WINDOWS, SEARCH, WHILE, INDEX, CREATION, PROCESS                            |
| Salva nell'indice full-text | FIGURA, ILLUSTRA, ROLE, LANGUAGE, RESOURCES, WINDOWS, SEARCH, WHILE, INDEX, CREATION, PROCESS                            |



 

I Word breaker e gli stemmer vengono usati per espandere query [FREETEXT](-search-sql-freetext.md) in fase di query. Le impostazioni locali della query sono le impostazioni locali predefinite, a meno che non venga passato un identificatore di codice della lingua (LCID) come parametro di query. Il componente query richiama il Word breaker appropriato nei termini di query elencati nella clausola [where](-search-sql-where.md) della query. Se, ad esempio, la clausola WHERE della query contiene "FREETEXT (mele, arance e pera)", il Word breaker riceve il testo "mele, arance e pere". Se nella clausola WHERE della query viene utilizzato il predicato full-text [Contains](-search-sql-contains.md) , l'output di testo del Word breaker viene normalizzato. In caso contrario, il componente della query passa ogni parola identificata dal Word breaker allo stemmer appropriato per la lingua e le impostazioni locali. Lo stemmer genera un elenco di forme alternative o flesse per la parola. Il componente query normalizza l'elenco espanso dei termini della query e rimuove le parole non significative.

La tabella seguente elenca le azioni e i risultati corrispondenti per la query "mele, arance e pere".



| Azione                       | Testo risultante                                            |
|------------------------------|-----------------------------------------------------------|
| Testo originale                | mele, arance e pera                                |
| Word-interruzioni                | mele, arance e, pere, EOS                          |
| Stemming                     | Apple, mele, arancione, arancione, arancione e, pera, pera |
| Normalization                | APPLE, MELE, ARANCIONE, ARANCIONE, ARANCIONE E, PERA, PERA |
| Rimozione di parole non significative           | APPLE, MELE, ARANCIO, ARANCIO, ARANCIA, PERA, PERA      |
| Elenco espanso dei termini della query | APPLE, MELE, ARANCIO, ARANCIO, ARANCIA, PERA, PERA      |



 

I termini della query espansa aumentano la probabilità che la query trovi documenti che corrispondono allo scopo della query originale. Il testo generato dal Word breaker o dallo stemmer in fase di query non è archiviato su disco.

## <a name="word-breaking"></a>Word breaking

La parola suddivisione è la separazione del testo in singoli token di testo o parole. Molti linguaggi, soprattutto quelli con alfabeti romani, hanno una matrice di separatori di parola, ad esempio spazi vuoti, e punteggiatura usati per distinguere parole, frasi e frasi. I Word breaker devono basarsi su euristiche accurate del linguaggio per fornire risultati affidabili e accurati. L'elaborazione delle parole è più complessa per i sistemi basati su caratteri di scrittura o alfabeti basati su script, in cui il significato dei singoli caratteri è determinato dal contesto. Per ulteriori informazioni sulle considerazioni linguistiche che possono influire sull'implementazione del Word breaker, vedere [considerazioni linguistiche e Unicode](linguistic-and-unicode-considerations.md).

## <a name="stemming"></a>Stemming

Windows Search applica gli stemmer esclusivamente in fase di query per generare forme di Word aggiuntive per i termini nelle query [FREETEXT](-search-sql-freetext.md) e Property. Gli stemmer eseguono l'analisi morfologica e applicano regole grammaticali per generare un elenco di forme alternative, o flesse, per le parole. I formati alternativi hanno spesso lo stesso stem o form di base. Generando i moduli declinati per una parola, il servizio di indicizzazione restituisce i risultati della query statisticamente più rilevanti per una query. Una query full-text per "swim meet", ad esempio, corrisponde a documenti che contengono "swim, Swim, swims, swims", nuoto, nuotato, nuotato "o" Meet, Meet, Meets, Meets ", meeting, met" e combinazioni di questi termini.

Per alcuni linguaggi è necessario che i termini flesso vengano generati sia in fase di indicizzazione sia in fase di query per le flessioni standard e Variant. In questo caso, lo stemming si verifica nel componente word breaker, con un lavoro con stemming minimo nello stemmer effettivo. Ad esempio, il Word breaker giapponese esegue lo stemming durante la creazione dell'indice e l'esecuzione di query per consentire a una query di trovare forme flesse diverse dei termini di ricerca.

## <a name="normalization"></a>Normalization

I documenti di tutte le lingue vengono archiviati in un unico indice. Sebbene le parole e le regole linguistiche differiscano notevolmente, esistono alcune considerazioni, ad esempio numeri, date e ore, che vengono gestite in modo coerente in tutti i Word breaker. Per ulteriori informazioni sulle considerazioni di normalizzazione che possono influire sull'implementazione del Word breaker, vedere [normalizzazione dei form di Surface](surface-form-normalization.md).

## <a name="noise-words"></a>Parole non significative

Parole non significative, note anche come parole non significative, sono parole che non sono indicatori significativi per il contenuto. Il servizio di indicizzazione rimuove le parole non significative dai termini di query e dal contenuto incluso nell'indice full-text. Un *offset* è l'occorrenza di una parola in un documento o in un elenco di termini di query. L'offset delle parole non significative in un documento o in una query viene registrato come vuoto. La rimozione di parole non significative consente di migliorare le prestazioni delle query, evitando una crescita Migliora inoltre la pertinenza dei risultati della query. È possibile configurare la ricerca di Windows in modo da usare elenchi di parole non significative per lingue specifiche. Questi elenchi vengono utilizzati quando viene richiamato un Word breaker per tale lingua. Ad esempio, "The" nella lingua inglese si verifica spesso con un valore minimo come chiave univoca. "L'oggetto" è nell'elenco di parole non significative, non viene scritto nell'indice di contenuto e, se sottoposto a query, non restituisce alcun risultato.

Le parole non significative fungono da segnaposto nelle query di frasi. Un documento che contiene il testo "Wag the Dog" viene archiviato nell'indice con "Wag" nell'occorrenza 1 e "Dog" nell'occorrenza 3. La query di frase "Wag Dog" non corrisponde, ma la frase "WAG a Dog", perché le informazioni sull'occorrenza corrispondono. La frase "Wag Purple Dog" non corrisponde perché "Purple" non è stato trovato nell'indice nell'occorrenza 2. Tuttavia, una query per "Wag the Dog" restituisce documenti che contengono "Wag Purple Dog" perché non esiste alcun modo per determinare in modo efficiente se il documento ha una parola non significativa tra "Wag" e "Dog".

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Estensione delle risorse della lingua](extending-language-resources-in-windows-search.md)
</dt> <dt>

[Implementazione di un Word breaker e uno stemmer](implementing-a-word-breaker-and-stemmer.md)
</dt> <dt>

[Considerazioni linguistiche e Unicode](linguistic-and-unicode-considerations.md)
</dt> <dt>

[Risoluzione dei problemi relativi a risorse di linguaggio e procedure consigliate](troubleshooting-language-resources.md)
</dt> </dl>

 

 
