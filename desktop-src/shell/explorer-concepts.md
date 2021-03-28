---
description: Lo spazio dei nomi della shell organizza il file system e altri oggetti gestiti dalla shell in una singola gerarchia strutturata ad albero. Concettualmente, si tratta di una versione più ampia e più completa del file system.
title: Concetti di Esplora comuni
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 78136c36-bd3c-4114-8b69-fef4e307566d
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: d5ea7d154ef0455576d91f99eb53dccd93c25339
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104568737"
---
# <a name="common-explorer-concepts"></a>Concetti di Esplora comuni

Lo *spazio dei nomi* della shell organizza il file System e altri oggetti gestiti dalla shell in una singola gerarchia strutturata ad albero. Concettualmente, si tratta di una versione più ampia e più completa del file system.

-   [Introduzione](#introduction)
-   [Identificazione di oggetti spazio dei nomi](#identifying-namespace-objects)
    -   [ID elemento](#item-ids)
    -   [Elenchi di ID elemento](#item-id-lists)
    -   [PIDL](#pidls)
    -   [Allocazione di PIDL](#allocating-pidls)

## <a name="introduction"></a>Introduzione

Una delle responsabilità principali della shell è la gestione e l'accesso all'ampia gamma di oggetti che costituiscono il sistema. I più numerosi e familiari di questi oggetti sono le cartelle e i file che risiedono in unità disco del computer. Tuttavia, la shell gestisce anche un certo numero di oggetti non file System o *virtuali* . Di seguito sono riportati alcuni esempi:

-   Stampanti di rete
-   Altri computer in rete
-   Applicazioni del pannello di controllo
-   Cestino

Alcuni oggetti virtuali non implicano alcuna archiviazione fisica. L'oggetto Printer, ad esempio, contiene una raccolta di collegamenti alle stampanti di rete. Altri oggetti virtuali, ad esempio il Cestino, possono contenere dati archiviati in un'unità disco, ma devono essere gestiti in modo diverso rispetto ai file normali. È ad esempio possibile utilizzare un oggetto virtuale per rappresentare i dati archiviati in un database. In termini di spazio dei nomi, i vari elementi nel database possono essere visualizzati in Esplora risorse come oggetti separati, anche se sono tutti archiviati in un singolo file su disco.

È possibile che gli oggetti virtuali si trovino anche sui computer remoti. Ad esempio, per facilitare il roaming, i file di documento di un utente possono essere archiviati in un server. Per concedere agli utenti l'accesso ai file da più PC desktop, la cartella documenti sul PC desktop attualmente in uso punterà al server, non al disco rigido del PC desktop. Il percorso includerà un'unità di rete mappata o un nome di percorso UNC.

Analogamente al file system, lo spazio dei nomi include due tipi di base di oggetto: cartelle e file. Gli oggetti folder sono i *nodi* dell'albero. si tratta di contenitori per oggetti file e altre cartelle. Gli oggetti file sono le *foglie* dell'albero. si tratta di normali file su disco o oggetti virtuali, ad esempio collegamenti alla stampante. Le cartelle che non fanno parte del file system sono talvolta denominate *cartelle virtuali*.

Come file system cartelle, la raccolta di cartelle virtuali varia in genere da sistema a sistema. Sono disponibili tre classi di cartelle virtuali:

-   Cartelle virtuali standard, ad esempio il Cestino, presenti in tutti i sistemi.
-   Cartelle virtuali facoltative con nomi e funzionalità standard, ma che potrebbero non essere presenti in tutti i sistemi.
-   Cartelle non standard installate dall'utente.

A differenza di file system cartelle, gli utenti non possono creare nuove cartelle virtuali. Possono installare solo quelli creati da sviluppatori non Microsoft. Il numero di cartelle virtuali è quindi in genere molto inferiore al numero di cartelle file system. Per informazioni su come implementare le cartelle virtuali, vedere [estensioni dello spazio dei nomi](nse-works.md).

È possibile visualizzare una rappresentazione visiva del modo in cui lo spazio dei nomi è strutturato nella barra di Explorer di Esplora risorse. Ad esempio, lo screenshot seguente di Esplora risorse Mostra uno spazio dei nomi relativamente semplice.

![screenshot che mostra una visualizzazione dello spazio dei nomi della shell](images/prog1.png)

La radice finale della gerarchia dello spazio dei nomi è il desktop. Immediatamente sotto la radice sono presenti diverse cartelle virtuali, ad esempio Computer locale e il Cestino.

I file System delle varie unità disco possono essere considerati come subset della gerarchia dello spazio dei nomi più grande. Le radici di questi file System sono le sottocartelle della cartella Computer locale. Computer locale include anche le radici delle unità di rete mappate. Gli altri nodi dell'albero, ad esempio documenti, sono cartelle virtuali.

## <a name="identifying-namespace-objects"></a>Identificazione di oggetti spazio dei nomi

Prima di poter utilizzare un oggetto spazio dei nomi, è necessario innanzitutto disporre di un modo per identificarlo. Un oggetto nel file system potrebbe avere un nome, ad esempio MyFile.htm. Poiché potrebbero essere presenti altri file con lo stesso nome in un'altra posizione del sistema, l'identificazione univoca di un file o di una cartella richiede un percorso completo, ad esempio "C: \\ docs \\MyFile.htm". Questo percorso è fondamentalmente un elenco ordinato di tutte le cartelle in un percorso dalla radice file system, C: \\ , che termina con il file.

Nel contesto dello spazio dei nomi, i percorsi sono comunque molto utili per identificare gli oggetti che si trovano nella parte file system dello spazio dei nomi. Tuttavia, non possono essere utilizzati per gli oggetti virtuali. La shell fornisce invece un mezzo di identificazione alternativo che può essere usato con qualsiasi oggetto spazio dei nomi.

### <a name="item-ids"></a>ID elemento

All'interno di una cartella, ogni oggetto dispone di un *ID elemento*, che è l'equivalente funzionale del nome di un file o di una cartella. L'ID dell'elemento è in realtà una struttura [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) :


```
typedef struct _SHITEMID { 
    USHORT cb; 
    BYTE   abID[1]; 
} SHITEMID, * LPSHITEMID;
```



Il membro **permanente** è l'identificatore dell'oggetto. La lunghezza di **subatter** non è definita e il relativo valore è determinato dalla cartella che contiene l'oggetto. Poiché non esiste una definizione standard per il **modo in** cui i valori di tipo subentrano assegnati dalle cartelle, sono significativi solo per l'oggetto cartella associato. Le applicazioni devono semplicemente gestirle come token che identifica un oggetto in una cartella specifica. Poiché la lunghezza di **attention** varia, il membro **CB** include le dimensioni della struttura [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) in byte.

Poiché gli ID elemento non sono utili a scopo di visualizzazione, la cartella che contiene l'oggetto normalmente assegna un nome visualizzato. Si tratta del nome utilizzato da Esplora risorse quando viene visualizzato il contenuto di una cartella. Per ulteriori informazioni su come vengono gestiti i nomi visualizzati, vedere [recupero di informazioni da una cartella](folder-info.md).

### <a name="item-id-lists"></a>Elenchi di ID elemento

L'ID dell'elemento viene raramente usato da solo. In genere, fa parte di un elenco di ID elemento, che svolge la stessa funzione di un percorso di file system. Tuttavia, invece della stringa di caratteri utilizzata per i percorsi, un elenco di ID elemento è una struttura [**ItemId**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) . Questa struttura è una sequenza ordinata di uno o più ID elemento, terminati da un **valore null** a 2 byte. Ogni ID elemento nell'elenco ID elemento corrisponde a un oggetto spazio dei nomi. Il rispettivo ordine definisce un percorso nello spazio dei nomi, molto simile a un percorso file system.

Nella figura seguente è illustrata una rappresentazione schematica della struttura [**ItemId**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) che corrisponde a C: \\ docs \\MyFile.htm. Il nome visualizzato di ogni ID elemento viene visualizzato sopra. Le larghezze variabili dei membri **rimanenti** sono arbitrarie; viene illustrato il fatto che le dimensioni di questo membro possono variare.

![illustrazione schematica di un PIDL](images/shell2.png)

### <a name="pidls"></a>PIDL

Per l'API shell, gli oggetti dello spazio dei nomi vengono in genere identificati da un puntatore alla relativa struttura [**ItemId**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) o da un puntatore a un elenco di identificatori di elemento (PIDL). Per praticità, il termine PIDL si riferisce in genere a questa documentazione alla struttura stessa anziché al puntatore.

Il PIDL illustrato nella figura precedente viene definito PIDL *completo* o *assoluto*. Un PIDL completo inizia dal desktop e contiene gli ID elemento di tutte le cartelle intermedie nel percorso. Termina con l'ID elemento dell'oggetto seguito da un **valore null** a due byte di terminazione. Un PIDL completo è simile a un percorso completo e identifica in modo univoco l'oggetto nello spazio dei nomi della shell.

I PIDL completi vengono usati raramente. Molti metodi e funzioni prevedono un *PIDL relativo*. La radice di un PIDL relativo è una cartella, non il desktop. Come per i percorsi relativi, la serie di ID elemento che compongono la struttura definiscono un percorso nello spazio dei nomi tra due oggetti. Anche se non identificano in modo univoco l'oggetto, sono in genere inferiori a un PIDL completo e sono sufficienti per molti scopi.

I PIDL relativi più comunemente utilizzati, *PIDL a livello singolo*, sono relativi alla cartella padre dell'oggetto. Contengono solo l'ID elemento dell'oggetto e un **valore null** di terminazione. I PIDL a più livelli vengono usati anche per molti scopi. Contengono due o più ID elemento e in genere definiscono un percorso da una cartella padre a un oggetto tramite una serie di una o più sottocartelle. Si noti che un PIDL a un solo livello può essere ancora un PIDL completo. In particolare, gli oggetti desktop sono elementi figlio del desktop, quindi i PIDL completi contengono un solo ID elemento.

Come illustrato in [ottenere l'ID di una cartella](folder-id.md), l'API shell offre diversi modi per recuperare il PIDL di un oggetto. Una volta creato, in genere è sufficiente usarlo per identificare l'oggetto quando si chiamano altre funzioni e metodi dell'API shell. In questo contesto, il contenuto interno di PIDL è opaco e irrilevante. Ai fini di questa discussione, si può pensare a PIDL come token che rappresentano oggetti specifici dello spazio dei nomi e concentrarsi su come usarli per le attività comuni.

### <a name="allocating-pidls"></a>Allocazione di PIDL

Sebbene PIDL abbia una certa somiglianza con i percorsi, l'uso di tali percorsi richiede un approccio leggermente diverso. La differenza principale è la modalità di allocazione e deallocazione della memoria.

Analogamente alla stringa utilizzata per un percorso, è necessario allocare memoria per un PIDL. Se un'applicazione crea un PIDL, deve allocare memoria sufficiente per la struttura [**ItemId**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) . Per la maggior parte dei casi illustrati in questo articolo, la shell crea il PIDL e gestisce l'allocazione della memoria. Indipendentemente da ciò che ha allocato il PIDL, l'applicazione è in genere responsabile della deallocazione di PIDL quando non è più necessaria.

Usare la funzione [**CoTaskMemAlloc**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc) per allocare PIDL e la funzione [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) per deallocarla.

 

 
