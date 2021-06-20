---
description: Informazioni sullo spazio dei nomi Shell e sui relativi oggetti origine dati. Questo spazio dei nomi offre opzioni di estendibilità nell'interfaccia utente della shell di Windows.
ms.assetid: 539c4455-e1c7-45a0-b3c3-781f2b7a1617
title: Introduzione allo spazio dei nomi della shell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e1be0187094ffe7cf7b56b724c5990fe18321fa
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404294"
---
# <a name="introduction-to-the-shell-namespace"></a>Introduzione allo spazio dei nomi della shell

Lo spazio *dei nomi* Shell organizza i file system e altri oggetti gestiti da Shell in un'unica gerarchia strutturata ad albero. Concettualmente, si tratta di una versione più ampia e più inclusiva del file system.

-   [Introduzione](#introduction)
-   [Identificazione degli oggetti dello spazio dei nomi](#identifying-namespace-objects)
    -   [ID elemento](#item-ids)
    -   [Elenchi di ID elemento](#item-id-lists)
    -   [PIDL](#pidls)
    -   [Allocazione di PID](#allocating-pidls)

## <a name="introduction"></a>Introduzione

Una delle principali responsabilità di Shell è la gestione e l'accesso all'ampia gamma di oggetti che costituiscono il sistema. I più numerosi e familiari di questi oggetti sono le cartelle e i file che si trovano nelle unità disco del computer. Tuttavia, Shell gestisce anche un certo numero  di oggetti virtuali o di sistema non file. Di seguito sono riportati alcuni esempi:

-   Stampanti di rete
-   Altri computer in rete
-   Pannello di controllo applicazioni
-   Oggetto Cestino

Alcuni oggetti virtuali non implicano affatto l'archiviazione fisica. L'oggetto stampante, ad esempio, contiene una raccolta di collegamenti alle stampanti di rete. Altri oggetti virtuali, ad esempio Cestino, possono contenere dati archiviati in un'unità disco, ma che devono essere gestiti in modo diverso rispetto ai normali file. Ad esempio, un oggetto virtuale può essere usato per rappresentare i dati archiviati in un database. In termini di spazio dei nomi, i vari elementi nel database possono essere visualizzati nel Esplora risorse come oggetti separati, anche se sono tutti archiviati in un singolo file su disco.

Gli oggetti virtuali possono anche trovarsi in computer remoti. Ad esempio, per facilitare il roaming, i file di documento di un utente potrebbero essere archiviati in un server. Per concedere agli utenti l'accesso ai propri file da più PC desktop, la cartella Documenti nel PC desktop attualmente in uso farà riferimento al server, non al disco rigido del PC desktop. Il percorso includerà un'unità di rete mappata o un nome di percorso UNC.

Come il file system, lo spazio dei nomi include due tipi di oggetto di base: cartelle e file. Gli oggetti cartella sono *i nodi* dell'albero. sono contenitori per oggetti file e altre cartelle. Gli oggetti file sono *le foglia* dell'albero. si tratta di normali file su disco o di oggetti virtuali, ad esempio collegamenti alla stampante. Le cartelle che non fanno parte del file system vengono talvolta definite *cartelle virtuali*.

Come file system cartelle virtuali, la raccolta di cartelle virtuali varia in genere da sistema a sistema. Esistono tre classi di cartelle virtuali:

-   Cartelle virtuali standard, ad esempio Cestino, che si trovano in tutti i sistemi.
-   Cartelle virtuali facoltative con nomi e funzionalità standard, ma che potrebbero non essere presenti in tutti i sistemi.
-   Cartelle non standard installate dall'utente.

A file system cartelle virtuali, gli utenti non possono creare nuove cartelle virtuali. Possono installare solo quelli creati da sviluppatori non Microsoft. Il numero di cartelle virtuali è quindi in genere molto inferiore al numero di cartelle file system virtuali. Per informazioni su come implementare le cartelle virtuali, vedere Estensioni dello spazio [dei nomi](nse-works.md).

È possibile visualizzare una rappresentazione visiva della struttura dello spazio dei nomi nella barra di Explorer del Esplora risorse. Ad esempio, la schermata seguente di Esplora risorse uno spazio dei nomi relativamente semplice.

![visualizzazione dello spazio dei nomi della shell](images/prog1.png)

La radice finale della gerarchia dello spazio dei nomi è il desktop. Immediatamente sotto la radice sono presenti diverse cartelle virtuali, ad esempio Computer locale e Cestino.

I file system delle varie unità disco possono essere visti come subset della gerarchia dello spazio dei nomi più grande. Le radici di questi file system sono sottocartelle della Computer locale cartella. Computer locale include anche le radici di qualsiasi unità di rete mappata. Altri nodi nell'albero, ad esempio Documenti, sono cartelle virtuali.

## <a name="identifying-namespace-objects"></a>Identificazione degli oggetti dello spazio dei nomi

Prima di poter usare un oggetto spazio dei nomi, è necessario avere un modo per identificarlo. Un oggetto nel file system può avere un nome, ad esempio MyFile.htm. Poiché potrebbero essere presenti altri file con tale nome altrove nel sistema, l'identificazione univoca di un file o di una cartella richiede un percorso completo, ad esempio "C: \\ \\ MyDocsMyFile.htm". Questo percorso è fondamentalmente un elenco ordinato di tutte le cartelle in un percorso file system radice, C: \\ , che termina con il file.

Nel contesto dello spazio dei nomi, i percorsi sono ancora molto utili per identificare gli oggetti file system parte dello spazio dei nomi. Tuttavia, non possono essere usati per gli oggetti virtuali. La shell fornisce invece un mezzo alternativo di identificazione che può essere usato con qualsiasi oggetto spazio dei nomi.

### <a name="item-ids"></a>ID elemento

All'interno di una cartella, ogni oggetto ha un *ID elemento*, che è l'equivalente funzionale di un nome di file o cartella. L'ID elemento è in realtà [**una struttura SHITEMID:**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid)


```
typedef struct _SHITEMID { 
    USHORT cb; 
    BYTE   abID[1]; 
} SHITEMID, * LPSHITEMID; 
```



Il **membro abID** è l'identificatore dell'oggetto. La lunghezza di **abID** non è definita e il relativo valore è determinato dalla cartella che contiene l'oggetto . Poiché non esiste una definizione standard per il modo in cui **i valori abID** vengono assegnati dalle cartelle, sono significativi solo per l'oggetto cartella associato. Le applicazioni devono semplicemente considerarle come un token che identifica un oggetto in una cartella specifica. Poiché la lunghezza di **abID** varia, il membro **cb** contiene le dimensioni della [**struttura SHITEMID,**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) in byte.

Poiché gli ID elemento non sono utili a scopo di visualizzazione, la cartella che contiene l'oggetto assegna in genere un nome visualizzato. Questo è il nome usato da Esplora risorse quando visualizza il contenuto di una cartella. Per altre informazioni sulla gestione dei nomi visualizzati, vedere [Recupero di informazioni da una cartella](folder-info.md).

### <a name="item-id-lists"></a>Elenchi di ID elemento

L'ID elemento viene usato raramente da solo. In genere, fa parte di un elenco di ID elemento, che svolge lo stesso scopo di un file system percorso. Tuttavia, anziché la stringa di caratteri usata per i percorsi, un elenco di ID elemento è una [**struttura ITEMIDLIST.**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) Questa struttura è una sequenza ordinata di uno o più ID elemento, terminati da un valore **NULL** a due byte. Ogni ID elemento nell'elenco di ID elemento corrisponde a un oggetto spazio dei nomi. L'ordine definisce un percorso nello spazio dei nomi, in modo simile a un file system percorso.

La figura seguente mostra una rappresentazione schematica della [**struttura ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) che corrisponde a C: \\ MyDocs \\MyFile.htm. Il nome visualizzato di ogni ID elemento viene visualizzato sopra di esso. Le larghezze variabili dei **membri abID** sono arbitrarie. illustrano il fatto che le dimensioni di questo membro possono variare.

![illustrazione schematica di un pidl](images/shell2.png)

### <a name="pidls"></a>PIDL

Per l'API Shell, gli oggetti dello spazio dei nomi sono in genere identificati da un puntatore alla struttura [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) o da un puntatore a un elenco di identificatori di elemento (PIDL). Per praticità, il termine PIDL in genere farà riferimento in questa documentazione alla struttura stessa anziché al puntatore a essa.

Il FILE PIDL illustrato nella figura precedente viene definito PIDL completo *o* assoluto. Un FILE PIDL completo inizia dal desktop e contiene gli ID elemento di tutte le cartelle intermedie nel percorso. Termina con l'ID elemento dell'oggetto seguito da un valore NULL a due byte di **terminazione.** Un FILE PIDL completo è simile a un percorso completo e identifica in modo univoco l'oggetto nello spazio dei nomi Shell.

Gli PID completi vengono usati raramente. Molte funzioni e metodi prevedono un *FILE PIDL relativo.* La radice di un FILE PIDL relativo è una cartella, non il desktop. Come per i percorsi relativi, la serie di ID elemento che costituiscono la struttura definisce un percorso nello spazio dei nomi tra due oggetti. Anche se non identificano in modo univoco l'oggetto, sono in genere più piccoli di un PIDL completo e sufficienti per molti scopi.

Gli PID relativi più comunemente usati, *gli PID* a livello singolo, sono relativi alla cartella padre dell'oggetto. Contengono solo l'ID elemento dell'oggetto e un valore **NULL di terminazione.** Gli PID a più livelli vengono usati anche per molti scopi. Contengono due o più ID elemento e in genere definiscono un percorso da una cartella padre a un oggetto tramite una serie di una o più sottocartelle. Si noti che un FILE PIDL a livello singolo può comunque essere un FILE PIDL completo. In particolare, gli oggetti desktop sono elementi figlio del desktop, quindi i relativi PID completi contengono un solo ID elemento.

Come illustrato in [Recupero dell'ID di una](folder-id.md)cartella, l'API shell offre diversi modi per recuperare il PIDL di un oggetto. Una volta creato, in genere è sufficiente usarlo per identificare l'oggetto quando si chiamano altre funzioni e metodi dell'API shell. In questo contesto, il contenuto interno di un PIDL è opaco e irrilevante. Ai fini di questa discussione, è possibile pensare agli PID come a token che rappresentano oggetti dello spazio dei nomi specifici e concentrarsi su come usarli per attività comuni.

### <a name="allocating-pidls"></a>Allocazione di PID

Anche se gli PID hanno una certa somiglianza con i percorsi, l'uso di questi elementi richiede un approccio leggermente diverso. La differenza principale consiste nel modo in cui allocare e deallocare la memoria.

Analogamente alla stringa usata per un percorso, la memoria deve essere allocata per un PIDL. Se un'applicazione crea un file PIDL, deve allocare memoria sufficiente per la [**struttura ITEMIDLIST.**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) Per la maggior parte dei casi descritti in questo argomento, la shell crea il file PIDL e gestisce l'allocazione della memoria. Indipendentemente dall'allocazione del file PIDL, l'applicazione è in genere responsabile della deallocazione del file PIDL quando non è più necessario.

Usare la [**funzione CoTaskMemAlloc**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc) per allocare il file PIDL e la [**funzione CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) per deallocarlo.

 

 
