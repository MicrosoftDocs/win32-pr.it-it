---
title: Informazioni sulle tabelle Atom
description: In questa sezione vengono illustrate le tabelle atom.
ms.assetid: 12114a3e-99a4-480f-9d1a-57c1942b7382
keywords:
- atomi
- Tabelle atom
- nomi atom
- Dynamic Data Exchange (DDE), atoms
- DDE (Dynamic Data Exchange),atoms
- tabelle atom globali
- tabelle atom locali
- atomi integer
- atomi di stringa
ms.topic: article
ms.date: 08/25/2020
ms.openlocfilehash: 92a8304e1e96c7385ddb11ba6391258acbe62a26
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549606"
---
# <a name="about-atom-tables"></a>Informazioni sulle tabelle Atom

Una *tabella atom è* una tabella definita dal sistema che archivia stringhe e identificatori corrispondenti. Un'applicazione inserisce una stringa in una tabella atom e riceve un intero a 16 bit, denominato *atom*, che può essere usato per accedere alla stringa. Una stringa inserita in una tabella atom è denominata nome *atom*.

Il sistema fornisce una serie di tabelle atom. Ogni tabella atom ha uno scopo diverso. Ad esempio, le Dynamic Data Exchange (DDE) usano la tabella [atom](#global-atom-table) globale per condividere stringhe nome-elemento e nome argomento con altre applicazioni. Anziché passare stringhe effettive, un'applicazione DDE passa atomi globali all'applicazione partner. Il partner usa gli atom per ottenere le stringhe dalla tabella atom.

Le applicazioni possono usare tabelle atom locali per archiviare le proprie associazioni nome-elemento.

Il sistema usa tabelle atom che non sono direttamente accessibili alle applicazioni. Tuttavia, l'applicazione usa questi atomi quando chiama un'ampia gamma di funzioni. Ad esempio, i formati degli Appunti registrati vengono archiviati in una tabella atom interna usata dal sistema. Un'applicazione aggiunge atom a questa tabella atom usando la [**funzione RegisterClipboardFormat.**](/windows/desktop/api/Winuser/nf-winuser-registerclipboardformata) Inoltre, le classi registrate vengono archiviate in una tabella atom interna usata dal sistema. Un'applicazione aggiunge atom a questa tabella atom usando la [**funzione RegisterClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa) o [**RegisterClassEx.**](/windows/desktop/api/winuser/nf-winuser-registerclassexa)

In questa sezione vengono descritti gli argomenti seguenti.

-   [Tabella Atom globale](#global-atom-table)
-   [Tabella Atom utente](#user-atom-table)
-   [Tabelle atom locali](#local-atom-tables)
-   [Tipi Atom](#atom-types)
    -   [Atomi di stringhe](#string-atoms)
    -   [Atomi interi](#integer-atoms)
-   [Numero di creazione e utilizzo di Atom](#atom-creation-and-usage-count)
-   [Query con tabella Atom](#atom-table-queries)
-   [Formati di stringa Atom](#atom-string-formats)

## <a name="global-atom-table"></a>Tabella Atom globale

La tabella atom globale è disponibile per tutte le applicazioni. Quando un'applicazione inserisce una stringa nella tabella atom globale, il sistema genera un atom univoco in tutto il sistema. Qualsiasi applicazione con l'atom può ottenere la stringa identificata tramite query sulla tabella atom globale.

Un'applicazione che definisce un formato dati DDE privato per la condivisione dei dati con altre applicazioni deve inserire il nome del formato nella tabella atom globale. Questa tecnica impedisce conflitti con i nomi dei formati definiti dal sistema o da altre applicazioni e rende disponibili per le altre applicazioni gli identificatori (atomi) per i messaggi o i formati.

## <a name="user-atom-table"></a>Tabella Atom utente

Oltre alla tabella atom globale, la tabella atom dell'utente è un'altra tabella atom di sistema condivisa anche tra tutti i processi. La tabella atom dell'utente viene usata per un numero ridotto di scenari interni a win32k. ad esempio nomi di moduli windows, stringhe note in win32k, formati OLE e così via. Anche se le applicazioni non interagiscono direttamente con la tabella atom dell'utente, chiamano diverse API, ad esempio [RegisterClass,](/windows/win32/api/winuser/nf-winuser-registerclassexa) [RegisterWindowMessage](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea)e [RegisterClipboardFormat,](/windows/win32/api/winuser/nf-winuser-registerclipboardformata)che aggiungono voci alla tabella atom dell'utente. Le voci aggiunte da `RegisterClass` possono essere eliminate da `UnregisterClass` . Tuttavia, le voci aggiunte da `RegisterWindowMessage` e non vengono eliminate fino al termine della `RegisterClipboardFormat` sessione. Se la tabella atom dell'utente non ha più spazio e la stringa passata non è già presente nella tabella, la chiamata avrà esito negativo. 

### <a name="atom-table-size"></a>Dimensioni tabella Atom
 
Molte API critiche, tra cui [CreateWindow,](/windows/win32/api/winuser/nf-winuser-createwindowa)si basano su atomi utente. Di conseguenza, l'esaurimento dello spazio nella tabella atom dell'utente comporta gravi problemi. Ad esempio, l'avvio di tutte le applicazioni potrebbe non riuscire. Ecco alcuni consigli per garantire che l'applicazione usa in modo efficiente le tabelle atom e mantengono l'affidabilità e le prestazioni dell'applicazione e del sistema:  

1. È consigliabile limitare l'utilizzo della tabella atom dell'utente da parte dell'app. L'archiviazione di stringhe univoche tramite API come , o occupa spazio nella tabella atom dell'utente, usata a livello globale da altre app per registrare le classi di finestre `RegisterClass` `RegisterWindowMessage` usando le `RegisterClipboardFormat` stringhe. Se possibile, è consigliabile usare [AddAtom](/windows/desktop/api/Winbase/nf-winbase-addatomw)DeleteAtom per archiviare le stringhe in una tabella atom locale o / [](/windows/desktop/api/Winbase/nf-winbase-deleteatom) [GlobalAddAtom](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) / [GlobalDeleteAtom](/windows/desktop/api/Winbase/nf-winbase-globaldeleteatom) se gli atom sono necessari tra processi incrociati.

1. Se l'applicazione causa problemi di tabella atom utente, è possibile analizzare la causa radice connettendo il debugger del kernel ed interrompendo il processo nelle chiamate a `UserAddAtomEx` ( `bae1 win32kbase!UserAddAtomEx /p <eprocess> "kc10;g"` ). Cercare nel `user32!` callstack per vedere quale API viene chiamata. La metodologia è simile al rilevamento dei problemi delle tabelle atom globali descritto in [Identificazione delle perdite di tabelle Atom globali](/archive/blogs/ntdebugging/identifying-global-atom-table-leaks). Un altro modo per eseguire il dump del contenuto della tabella atom utente è chiamando [GetClipboardFormatName](/windows/win32/api/winuser/nf-winuser-getclipboardformatnamea) sull'intervallo di possibili atomi da 0xC000 a 0xFFFF. Se il numero totale di atomi aumenta costantemente mentre l'applicazione è in esecuzione o non torna alla baseline quando l'app viene chiusa, si verifica un problema.

## <a name="local-atom-tables"></a>Tabelle atom locali

Un'applicazione può usare una tabella atom locale per gestire in modo efficiente un numero elevato di stringhe usate solo all'interno dell'applicazione. Queste stringhe e gli atomi associati sono disponibili solo per l'applicazione che ha creato la tabella.

Un'applicazione che richiede la stessa stringa in un numero di strutture può ridurre l'utilizzo della memoria usando una tabella atom locale. Anziché copiare la stringa in ogni struttura, l'applicazione può inserire la stringa nella tabella atom e includere l'atomo risultante nelle strutture. In questo modo, una stringa viene visualizzata una sola volta in memoria, ma può essere usata più volte nell'applicazione.

Le applicazioni possono anche usare tabelle atom locali per risparmiare tempo durante la ricerca di una determinata stringa. Per eseguire una ricerca, un'applicazione deve inserire solo la stringa di ricerca nella tabella atom e confrontare l'atomo risultante con gli atomi nelle strutture pertinenti. Il confronto di atomi è in genere più veloce rispetto al confronto di stringhe.

Le tabelle Atom vengono implementate come tabelle hash. Per impostazione predefinita, una tabella atom locale usa 37 bucket per la tabella hash. Tuttavia, è possibile modificare il numero di bucket usati chiamando la [**funzione InitAtomTable.**](/windows/desktop/api/Winbase/nf-winbase-initatomtable) Se l'applicazione chiama **InitAtomTable**, tuttavia, deve eseguire questa operazione prima di chiamare qualsiasi altra funzione di gestione atom.

## <a name="atom-types"></a>Tipi Atom

Le applicazioni possono creare due tipi di atomi: atomi di stringa e atomi di interi. I valori degli atomi integer e degli atomi di stringa non si sovrappongono, quindi entrambi i tipi di atomi possono essere usati nello stesso blocco di codice.

Diverse funzioni accettano stringhe o atom come parametri. Quando si passa un atom a queste funzioni, un'applicazione può usare la macro [**MAKEINTATOM**](/windows/desktop/api/Winbase/nf-winbase-makeintatom) per convertire l'atom in un formato che può essere usato dalla funzione.

Le sezioni seguenti descrivono i tipi atom.

-   [Atomi di stringa](#string-atoms)
-   [Atomi integer](#integer-atoms)

### <a name="string-atoms"></a>Atomi di stringa

Quando le applicazioni passano stringhe con terminazione Null alle funzioni [**GlobalAddAtom,**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) [**AddAtom**](/windows/desktop/api/Winbase/nf-winbase-addatomw), [**GlobalFindAtom**](/windows/desktop/api/Winbase/nf-winbase-globalfindatoma)e [**FindAtom,**](/windows/desktop/api/Winbase/nf-winbase-findatoma) ricevono *atomi* di stringa (interi a 16 bit) in cambio. Gli atomi di stringa hanno le proprietà seguenti:

-   I valori degli atomi di stringa sono nell'intervallo 0xC000 (MAXINTATOM) fino 0xFFFF.
-   La distinzione tra maiuscole e minuscole non è significativa nelle ricerche di un nome atom in una tabella atom. Inoltre, l'intera stringa deve corrispondere in un'operazione di ricerca. non viene eseguita alcuna corrispondenza di sottostringhe.
-   Le dimensioni della stringa associata a un atom di stringa non possono essere superiori a 255 byte. Questa limitazione si applica a tutte le funzioni atom.
-   Un *conteggio dei* riferimenti è associato a ogni nome atom. Il conteggio viene incrementato ogni volta che il nome atom viene aggiunto alla tabella e decrementato ogni volta che il nome atom viene eliminato. In questo modo si impedisce a utenti diversi dello stesso atom di stringa di eliminare i reciproci nomi di atom. Quando il conteggio dei riferimenti per un nome atom è uguale a zero, il sistema rimuove l'atom e il nome atom dalla tabella.

### <a name="integer-atoms"></a>Atomi integer

Gli atomi interi differiscono dagli atomi di stringa nei modi seguenti:

-   I valori degli atomi interi sono nell'intervallo compreso tra 0x0001 e 0xBFFF (**MAXINTATOM**– 1).
-   La rappresentazione di stringa di un atom integer \# *è dddd*, dove i valori rappresentati da *dddd* sono cifre decimali. Gli zeri iniziali vengono ignorati.
-   Non è presente alcun numero di riferimenti o sovraccarico di archiviazione associato a un atom integer.

## <a name="atom-creation-and-usage-count"></a>Numero di creazione e utilizzo di Atom

Un'applicazione crea un atom locale chiamando la [**funzione AddAtom.**](/windows/desktop/api/Winbase/nf-winbase-addatomw) crea un atom globale chiamando la [**funzione GlobalAddAtom.**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) Entrambe le funzioni richiedono un puntatore a una stringa. Il sistema cerca la stringa nella tabella atom appropriata e restituisce l'atom corrispondente all'applicazione. Nel caso di un atom di stringa, se la stringa si trova già nella tabella atom, il sistema incrementa il conteggio dei riferimenti per la stringa durante questo processo.

Le chiamate ripetute per aggiungere lo stesso nome atom restituiscono lo stesso atomo. Se il nome atom non esiste nella tabella quando viene chiamato [**AddAtom,**](/windows/desktop/api/Winbase/nf-winbase-addatomw) il nome atom viene aggiunto alla tabella e viene restituito un nuovo atom. Se si tratta di un atomo di stringhe, anche il conteggio dei riferimenti viene impostato su uno.

Un'applicazione deve chiamare [**la funzione DeleteAtom**](/windows/desktop/api/Winbase/nf-winbase-deleteatom) quando non deve più usare un atom locale. deve chiamare la [**funzione GlobalDeleteAtom**](/windows/desktop/api/Winbase/nf-winbase-globaldeleteatom) quando non richiede più un atom globale. Nel caso di un atomo di stringhe, una di queste funzioni riduce di uno il conteggio dei riferimenti dell'atomo corrispondente. Quando il conteggio dei riferimenti raggiunge lo zero, il sistema elimina il nome atom dalla tabella.

Il nome atom di un atom di stringa rimane nella tabella atom globale purché il conteggio dei riferimenti sia maggiore di zero, anche dopo la fine dell'applicazione che lo ha inserito nella tabella. Una tabella atom locale viene distrutta quando l'applicazione associata termina, indipendentemente dal conteggio dei riferimenti degli atomi nella tabella.

## <a name="atom-table-queries"></a>Atom-Table query

Un'applicazione può determinare se una determinata stringa si trova già in una tabella atom usando la [**funzione FindAtom**](/windows/desktop/api/Winbase/nf-winbase-findatoma) o [**GlobalFindAtom.**](/windows/desktop/api/Winbase/nf-winbase-globalfindatoma) Queste funzioni ricercano in una tabella atom la stringa specificata e, se la stringa è presente, restituiscono l'atom corrispondente.

Un'applicazione può usare la [**funzione GetAtomName**](/windows/desktop/api/Winbase/nf-winbase-getatomnamea) o [**GlobalGetAtomName**](/windows/desktop/api/Winbase/nf-winbase-globalgetatomnamea) per recuperare una stringa con nome atom da una tabella atom, purché l'applicazione abbia l'atom corrispondente alla stringa cercata. Entrambe le funzioni copiano la stringa del nome atom dell'atom specificato in un buffer e restituiscono la lunghezza della stringa copiata. **GetAtomName** recupera una stringa di nome atom da una tabella atom locale e **GlobalGetAtomName** recupera una stringa di nome atom dalla tabella atom globale.

## <a name="atom-string-formats"></a>Formati di stringa Atom

Le [**funzioni AddAtom**](/windows/desktop/api/Winbase/nf-winbase-addatomw), [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma), [**FindAtom**](/windows/desktop/api/Winbase/nf-winbase-findatoma)e [**GlobalFindAtom**](/windows/desktop/api/Winbase/nf-winbase-globalfindatoma) accettano un puntatore a una stringa con terminazione Null. Un'applicazione può specificare questo puntatore in uno dei modi seguenti.



|     Formato stringa               |    Descrizione                                                                                                |
|--------------------|----------------------------------------------------------------------------------------------------|
| \#*Dv*           | Intero specificato come stringa decimale. Usato per creare o trovare un atom di numeri interi.                  |
| *string atom name* | Nome atom di stringa. Usato per aggiungere un nome atom di stringa a una tabella atom e ricevere un atom in cambio. |



 

 

 
