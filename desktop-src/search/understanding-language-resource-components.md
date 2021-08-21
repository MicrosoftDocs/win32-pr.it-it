---
description: Le risorse della lingua sono costituite da word breaker e stemmer che estendono le funzionalità di compilazione e query degli indici a nuove lingue e impostazioni locali.
ms.assetid: 7963805e-e279-42cf-ba95-f81a7de8e68e
title: Informazioni sui componenti delle risorse del linguaggio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8feb10d14edbf4aba59b912ae1945d5e87ec32ef684f0b1f5530f1770ba70053
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118462383"
---
# <a name="understanding-language-resource-components"></a>Informazioni sui componenti delle risorse del linguaggio

Le risorse della lingua sono costituite da word breaker e stemmer che estendono le funzionalità di compilazione e query degli indici a nuove lingue e impostazioni locali. I word breaker vengono usati sia durante la creazione dell'indice che durante l'esecuzione di query. Gli stemmer vengono utilizzati solo per l'esecuzione di query. Windows La ricerca usa le DLL delle risorse della lingua per l'associazione alle [**implementazioni IWordBreaker**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordbreaker) e [**ISte common**](/windows/desktop/api/Indexsrv/nn-indexsrv-istemmer) per impostazioni locali specifiche della lingua.

Questo argomento è organizzato come segue:

-   [Informazioni sulle risorse del linguaggio](#about-language-resources)
-   [Word Breaking](#word-breaking)
-   [Derivanti](#stemming)
-   [Normalization](#normalization)
-   [Parole non pronunciate](#noise-words)
-   [Argomenti correlati](#related-topics)

## <a name="about-language-resources"></a>Informazioni sulle risorse del linguaggio

Windows La ricerca usa un filtro (un'implementazione [**dell'interfaccia IFilter)**](/windows/win32/api/filter/nn-filter-ifilter) e [**ILoadFilter**](/windows/desktop/api/filtereg/nn-filtereg-iloadfilter) per accedere a un documento nel formato nativo. Il [**componente IFilter**](/windows/win32/api/filter/nn-filter-ifilter) estrae contenuto di testo, proprietà e formattazione dal documento. Il [**filtro IFilter**](/windows/win32/api/filter/nn-filter-ifilter) identifica le impostazioni locali del documento da filtrare. Il componente di indicizzazione richiama il word breaker appropriato per le impostazioni locali. Se non è disponibile, il componente di indicizzazione richiama il word breaker neutro. Il word breaker riceve, da [**un filtro IFilter,**](/windows/win32/api/filter/nn-filter-ifilter)un flusso di input di caratteri Unicode che il word breaker analizza per produrre singole parole e frasi. Il word breaker normalizza anche i formati di data e ora. L'indicizzatore normalizza le parole prodotte dal word breaker convertendo le parole in lettere maiuscole. L'indicizzatore salva le parole maiuscole nell'indice full-text, ad eccezione delle parole non pronunciate identificate per le impostazioni locali.

La tabella seguente elenca le azioni e i risultati corrispondenti per la frase "Figura 1 illustra il ruolo delle risorse linguistiche per Windows ricerca durante il processo di creazione dell'indice".



| Azione                  | Testo risultante                                                                                                               |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------|
| Testo originale           | La figura 1 illustra il ruolo delle risorse del linguaggio per Windows ricerca durante il processo di creazione dell'indice.                    |
| Filtro               | La figura 1 illustra il ruolo delle risorse del linguaggio per Windows ricerca durante il processo di creazione dell'indice.                    |
| Word breaking           | Figura 1, illustra, ruolo, di, linguaggio, risorse, per, Windows, ricerca, durante, l'indice, creazione, processo, EOS |
| Normalization           | FIGURA, 1, ILLUSTRA, THE, ROLE, OF, LANGUAGE, RESOURCES, WINDOWS, SEARCH, DURING, THE, INDEX, CREATION, PROCESS           |
| Rimozione di parole non rumorose      | FIGURA, ILLUSTRA, RUOLO, LINGUAGGIO, RISORSE, WINDOWS, RICERCA, DURANTE, INDICE, CREAZIONE, PROCESSO                            |
| Salvare nell'indice full-text | FIGURA, ILLUSTRA, RUOLO, LINGUAGGIO, RISORSE, WINDOWS, RICERCA, DURANTE, INDICE, CREAZIONE, PROCESSO                            |



 

Word breaker e stemmer vengono utilizzati per espandere le [query FREETEXT](-search-sql-freetext.md) in fase di query. Le impostazioni locali della query sono le impostazioni locali predefinite, a meno che non venga passato un identificatore del codice lingua (LCID) come parametro di query. Il componente di query richiama il word breaker appropriato sui termini di query elencati nella [clausola WHERE](-search-sql-where.md) della query. Ad esempio, se la clausola WHERE della query contiene "FREETEXT (apples, oranges, and pears)," il word breaker riceve il testo "apples, oranges, and pears". Se la clausola WHERE della query usa il predicato [full-text CONTAINS,](-search-sql-contains.md) l'output di testo del word breaker viene normalizzato. In caso contrario, il componente di query passa ogni parola identificata dal word breaker al stemmer appropriato per la lingua e le impostazioni locali. Lo stemmer genera un elenco di forme alternative, o inflessete, per tale parola. Il componente di query normalizza l'elenco espanso di termini di query e rimuove le parole non erre.

Nella tabella seguente sono elencate le azioni e i risultati corrispondenti per la query "apples, oranges, and pears".



| Azione                       | Testo risultante                                            |
|------------------------------|-----------------------------------------------------------|
| Testo originale                | apples, oranges, and pears                                |
| Word breaking                | apples, oranges, and, pears, EOS                          |
| Stemming                     | apple, apples, orange, orangey, oranges, and, pear, pears |
| Normalization                | APPLE, APPLES, ORANGEY, ORANGEY, ORANGES E, PEAR, PEARS |
| Rimozione di parole non rumorose           | APPLE, APPLES, ORANGE, ORANGEY, ORANGES, PEAR, PEARS      |
| Elenco esteso di termini di query | APPLE, APPLES, ORANGE, ORANGEY, ORANGES, PEAR, PEARS      |



 

I termini di query espansi aumentano la probabilità che la query trovi documenti che corrispondono alla finalità della query originale. Il testo generato dal word breaker o stemmer in fase di query non viene archiviato su disco.

## <a name="word-breaking"></a>Word breaking

Il word breaking è la separazione del testo in singoli token di testo o parole. Molte lingue, in particolare quelle con alfabeti romani, hanno una matrice di separatori di parole (ad esempio spazi vuoti) e punteggiatura usati per distinguere parole, frasi e frasi. I word breaker devono basarsi sull'euristica della lingua accurata per fornire risultati affidabili e accurati. La suddivisione delle parole è più complessa per i sistemi di scrittura di caratteri o di alfabeti basati su script, in cui il significato dei singoli caratteri è determinato dal contesto. Per altre informazioni sulle considerazioni linguistiche che possono influire sull'implementazione del word breaker, vedere [Considerazioni sul formato linguistico e Unicode.](linguistic-and-unicode-considerations.md)

## <a name="stemming"></a>Stemming

Windows La ricerca applica gli stemmer esclusivamente in fase di query per generare formati di parola aggiuntivi per i termini in [FREETEXT](-search-sql-freetext.md) e nelle query di proprietà. Gli stemmer eseguono l'analisi morfica e applicano regole grammaticali per generare un elenco di forme alternative o flesse per le parole. Le forme alternative hanno spesso lo stesso gambo o lo stesso formato di base. Generando i formati inflected per una parola, il servizio di indicizzazione restituisce risultati di query statisticamente più rilevanti per una query. Ad esempio, una query full-text per "meet" corrisponde a documenti che contengono "corsi, corsi, corsie, corsie", acquaio, swam, swum" o "meet, meets, meets", meeting, met" e combinazioni di questi termini.

Alcuni linguaggi richiedono che i termini inflected siano generati sia in fase di indice che in fase di query per flesszioni standard e varianti. In questo caso, lo stemming si verifica nel componente word breaker, con uno stemmer minimo nello stemmer effettivo. Ad esempio, il word breaker giapponese esegue lo stemming sia durante la creazione dell'indice che durante l'esecuzione di query per consentire a una query di trovare forme gonfiate diverse dei termini di ricerca.

## <a name="normalization"></a>Normalization

I documenti di tutte le lingue vengono archiviati in un singolo indice. Anche se le parole e le regole linguistiche differiscono notevolmente, esistono alcune considerazioni, ad esempio numeri, date e ore, che vengono gestite in modo coerente in tutti i word breaker. Per altre informazioni sulle considerazioni sulla normalizzazione che possono influire sull'implementazione del word breaker, vedere [Normalizzazione dei moduli di surface.](surface-form-normalization.md)

## <a name="noise-words"></a>Parole non pronunciate

Le parole non significative, note anche come parole non significative, sono parole che non sono indicatori significativi per il contenuto. Il servizio di indicizzazione rimuove le parole non erre dai termini di query e dal contenuto incluso nell'indice full-text. Un *offset è* l'occorrenza di una parola in un documento o in un elenco di termini di query. L'offset delle parole non pronunciate in un documento o in una query viene registrato come vuoto. La rimozione di parole non necessarie migliora le prestazioni delle query evitando l'aumento non necessario dell'indice. Migliora anche la pertinenza dei risultati delle query. È possibile configurare la Windows per l'uso di elenchi di parole non erre per lingue specifiche. Questi elenchi vengono usati quando viene richiamato un word breaker per tale lingua. Ad esempio, "il" nella lingua inglese si verifica così spesso che ha poco valore come chiave univoca. "The" è presente nell'elenco di parole non erre, non viene scritto nell'indice di contenuto e, se viene eseguita una query, non restituisce alcun risultato.

Le parole non complesse fungono da segnaposto nelle query di frase. Un documento che contiene il testo "wag the dog" viene archiviato nell'indice con "wag" in corrispondenza dell'occorrenza 1 e "dog" all'occorrenza 3. La query di frase "wag dog" non corrisponde, ma la query di frase "wag a dog" lo fa, perché le informazioni sull'occorrenza corrispondono. La frase "wag purple dog" non corrisponde perché "viola" non è presente nell'indice in corrispondenza dell'occorrenza 2. Tuttavia, una query per "wag the dog" restituisce documenti che contengono "wag purple dog" perché non è possibile determinare in modo efficiente se il documento contiene una parola non non rumore tra "wag" e "dog".

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Estensione delle risorse del linguaggio](extending-language-resources-in-windows-search.md)
</dt> <dt>

[Implementazione di word breaker e stemmer](implementing-a-word-breaker-and-stemmer.md)
</dt> <dt>

[Considerazioni linguistiche e Unicode](linguistic-and-unicode-considerations.md)
</dt> <dt>

[Risoluzione dei problemi relativi alle risorse del linguaggio e alle procedure consigliate](troubleshooting-language-resources.md)
</dt> </dl>

 

 
