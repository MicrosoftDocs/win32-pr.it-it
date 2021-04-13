---
title: Informazioni sulle tabelle Atom
description: In questa sezione vengono descritte le tabelle Atom.
ms.assetid: 12114a3e-99a4-480f-9d1a-57c1942b7382
keywords:
- atomi
- tabelle Atom
- nomi Atom
- Dynamic Data Exchange (DDE), atomi
- DDE (Dynamic Data Exchange), atomi
- tabelle atom globali
- tabelle Atom locali
- atomi Integer
- atomi di stringa
ms.topic: article
ms.date: 08/25/2020
ms.openlocfilehash: 27f7cdb4bb2dc2fd97b4dba6909022b297df1a1d
ms.sourcegitcommit: e985e0532f0f895ae418e8c2658dac819cdae3b1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2020
ms.locfileid: "104399807"
---
# <a name="about-atom-tables"></a>Informazioni sulle tabelle Atom

Una *tabella Atom* è una tabella definita dal sistema che archivia stringhe e identificatori corrispondenti. Un'applicazione inserisce una stringa in una tabella Atom e riceve un intero a 16 bit, denominato *Atom*, che può essere usato per accedere alla stringa. Una stringa che è stata inserita in una tabella Atom è detta *nome Atom*.

Il sistema fornisce un numero di tabelle Atom. Ogni tabella Atom svolge uno scopo diverso. Ad esempio, le applicazioni Dynamic Data Exchange (DDE) utilizzano la [tabella Atom globale](#global-atom-table) per condividere le stringhe nome-elemento e nome argomento con altre applicazioni. Anziché passare stringhe effettive, un'applicazione DDE passa gli atomi globali alla relativa applicazione partner. Il partner utilizza gli atomi per ottenere le stringhe dalla tabella Atom.

Le applicazioni possono utilizzare le tabelle Atom locali per archiviare le proprie associazioni di nomi di elemento.

Il sistema utilizza tabelle Atom non direttamente accessibili per le applicazioni. Tuttavia, l'applicazione utilizza questi atomi quando si chiamano diverse funzioni. Ad esempio, i formati degli Appunti registrati vengono archiviati in una tabella Atom interna utilizzata dal sistema. Un'applicazione aggiunge atomi a questa tabella Atom usando la funzione [**RegisterClipboardFormat**](/windows/desktop/api/Winuser/nf-winuser-registerclipboardformata) . Inoltre, le classi registrate vengono archiviate in una tabella Atom interna utilizzata dal sistema. Un'applicazione aggiunge atomi a questa tabella Atom usando la funzione [**registerClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa) o [**RegisterClassEx**](/windows/desktop/api/winuser/nf-winuser-registerclassexa) .

In questa sezione vengono descritti gli argomenti seguenti.

-   [Tabella Atom globale](#global-atom-table)
-   [Tabella Atom utente](#user-atom-table)
-   [Tabelle Atom locali](#local-atom-tables)
-   [Tipi Atom](#atom-types)
    -   [Atomi di stringa](#string-atoms)
    -   [Atomi Integer](#integer-atoms)
-   [Conteggio utilizzo e creazione Atom](#atom-creation-and-usage-count)
-   [Query di tabella Atom](#atom-table-queries)
-   [Formati di stringa Atom](#atom-string-formats)

## <a name="global-atom-table"></a>Tabella Atom globale

La tabella Atom globale è disponibile per tutte le applicazioni. Quando un'applicazione inserisce una stringa nella tabella Atom globale, il sistema genera un Atom univoco nel sistema. Qualsiasi applicazione che dispone di Atom può ottenere la stringa che identifica eseguendo una query sulla tabella Atom globale.

Un'applicazione che definisce un formato dati DDE privato per la condivisione di dati con altre applicazioni deve inserire il nome del formato nella tabella Atom globale. Questa tecnica impedisce i conflitti con i nomi dei formati definiti dal sistema o da altre applicazioni e rende disponibili gli identificatori (atomi) per i messaggi o i formati per le altre applicazioni.

## <a name="user-atom-table"></a>Tabella Atom utente

Oltre alla tabella Atom globale, la tabella Atom dell'utente è un'altra tabella Atom di sistema condivisa anche in tutti i processi. La tabella Atom utente viene utilizzata per un numero ridotto di scenari interni a Win32k; ad esempio, i nomi dei moduli di Windows, le stringhe note in Win32k, i formati OLE e così via. Sebbene le applicazioni non interagiscano direttamente con la tabella Atom dell'utente, chiamano diverse API, ad esempio [registerClass](/windows/win32/api/winuser/nf-winuser-registerclassexa), [RegisterWindowMessage](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea)e [RegisterClipboardFormat](/windows/win32/api/winuser/nf-winuser-registerclipboardformata), che aggiungono voci alla tabella Atom dell'utente. Le voci aggiunte da `RegisterClass` possono essere eliminate da `UnregisterClass` . Tuttavia, le voci aggiunte da `RegisterWindowMessage` e non `RegisterClipboardFormat` vengono eliminate fino alla fine della sessione. Se la tabella Atom dell'utente non ha più spazio e la stringa passata non è già presente nella tabella, la chiamata avrà esito negativo. 

### <a name="atom-table-size"></a>Dimensioni tabella Atom
 
Molte API critiche, tra cui [CreateWindow](/windows/win32/api/winuser/nf-winuser-createwindowa), si basano sugli atomi utente. Pertanto, l'esaurimento dello spazio nella tabella Atom dell'utente provocherà gravi problemi; ad esempio, l'avvio di tutte le applicazioni potrebbe non riuscire. Di seguito sono riportate alcune indicazioni per garantire che l'applicazione utilizzi le tabelle Atom in modo efficiente e preservare l'affidabilità e le prestazioni dell'applicazione e del sistema:  

1. È necessario limitare l'utilizzo dell'app della tabella Atom dell'utente. L'archiviazione di stringhe univoche tramite API come `RegisterClass` , `RegisterWindowMessage` o `RegisterClipboardFormat` occupa spazio nella tabella Atom dell'utente, che viene usata a livello globale da altre app per registrare le classi di finestra usando le stringhe. Se possibile, è consigliabile usare [AddAtom](/windows/desktop/api/Winbase/nf-winbase-addatomw) / [DeleteAtom](/windows/desktop/api/Winbase/nf-winbase-deleteatom) per archiviare le stringhe in una tabella atom locale o [GlobalAddAtom](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) / [GlobalDeleteAtom](/windows/desktop/api/Winbase/nf-winbase-globaldeleteatom) se gli atomi sono necessari tra processi.

1. Se si verificano problemi relativi all'applicazione che causa problemi della tabella Atom dell'utente, è possibile esaminare la causa radice connettendo il debugger del kernel e suddividendo il processo nelle chiamate a `UserAddAtomEx` ( `bae1 win32kbase!UserAddAtomEx /p <eprocess> "kc10;g"` ). Cercare `user32!` su stack per vedere quale API viene chiamata. La metodologia è simile al rilevamento dei problemi della tabella Atom globale illustrato nell' [identificazione delle perdite di tabella atom globali](/archive/blogs/ntdebugging/identifying-global-atom-table-leaks). Un altro modo per eseguire il dump del contenuto della tabella Atom utente consiste nel chiamare [GetClipboardFormatName](/windows/win32/api/winuser/nf-winuser-getclipboardformatnamea) sull'intervallo di atomi possibili da 0XC000 a 0xFFFF. Se il numero totale di Atom aumenta costantemente mentre l'applicazione è in esecuzione o non torna alla baseline quando l'app viene chiusa, si verifica un problema.

## <a name="local-atom-tables"></a>Tabelle Atom locali

Un'applicazione può utilizzare una tabella atom locale per gestire in modo efficiente un numero elevato di stringhe utilizzate solo all'interno dell'applicazione. Queste stringhe e gli atomi associati sono disponibili solo per l'applicazione che ha creato la tabella.

Un'applicazione che richiede la stessa stringa in una serie di strutture può ridurre l'utilizzo della memoria utilizzando una tabella atom locale. Anziché copiare la stringa in ogni struttura, l'applicazione può inserire la stringa nella tabella Atom e includere il Atom risultante nelle strutture. In questo modo, una stringa viene visualizzata solo una volta in memoria, ma può essere utilizzata più volte nell'applicazione.

Le applicazioni possono inoltre utilizzare tabelle Atom locali per risparmiare tempo durante la ricerca di una determinata stringa. Per eseguire una ricerca, un'applicazione deve inserire solo la stringa di ricerca nella tabella Atom e confrontare il valore Atom risultante con gli atomi nelle strutture pertinenti. Il confronto di atomi è in genere più veloce rispetto a quello delle stringhe.

Le tabelle Atom vengono implementate come tabelle hash. Per impostazione predefinita, una tabella atom locale usa bucket 37 per la relativa tabella hash. Tuttavia, è possibile modificare il numero di bucket usati chiamando la funzione [**InitAtomTable**](/windows/desktop/api/Winbase/nf-winbase-initatomtable) . Se l'applicazione chiama **InitAtomTable**, tuttavia, questa operazione deve essere eseguita prima di chiamare qualsiasi altra funzione di gestione Atom.

## <a name="atom-types"></a>Tipi Atom

Le applicazioni possono creare due tipi di atomi, ovvero atomi di stringa e atomi di tipo Integer. I valori di atomi Integer e atomi di stringa non si sovrappongono, quindi è possibile usare entrambi i tipi di atomi nello stesso blocco di codice.

Diverse funzioni accettano stringhe o atomi come parametri. Quando si passa un Atom a queste funzioni, un'applicazione può utilizzare la macro [**MAKEINTATOM**](/windows/desktop/api/Winbase/nf-winbase-makeintatom) per convertire il valore Atom in un form che può essere utilizzato dalla funzione.

Nelle sezioni seguenti vengono descritti i tipi Atom.

-   [Atomi di stringa](#string-atoms)
-   [Atomi Integer](#integer-atoms)

### <a name="string-atoms"></a>Atomi di stringa

Quando le applicazioni passano stringhe con terminazione null alle funzioni [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma), [**AddAtom**](/windows/desktop/api/Winbase/nf-winbase-addatomw), [**GlobalFindAtom**](/windows/desktop/api/Winbase/nf-winbase-globalfindatoma)e [**FindAtom**](/windows/desktop/api/Winbase/nf-winbase-findatoma) , ricevono *atomi di stringa* (interi a 16 bit) in return. Gli atomi di stringa hanno le proprietà seguenti:

-   I valori degli atomi di stringa sono compresi tra 0xC000 (MAXINTATOM) e 0xFFFF.
-   Il caso non è significativo nelle ricerche di un nome Atom in una tabella Atom. Inoltre, l'intera stringa deve corrispondere in un'operazione di ricerca; non viene eseguita alcuna corrispondenza della sottostringa.
-   La stringa associata a un Atom di stringa non può avere una dimensione superiore a 255 byte. Questa limitazione si applica a tutte le funzioni Atom.
-   Un *conteggio dei riferimenti* è associato a ogni nome Atom. Il conteggio viene incrementato ogni volta che il nome Atom viene aggiunto alla tabella e decrementato ogni volta che il nome Atom viene eliminato. In questo modo si impedisce a utenti diversi della stessa stringa Atom di eliminare definitivamente i nomi Atom. Quando il conteggio dei riferimenti per un nome Atom è uguale a zero, il sistema rimuove il nome Atom e il nome Atom dalla tabella.

### <a name="integer-atoms"></a>Atomi Integer

Gli atomi Integer differiscono dagli atomi di stringa nei modi seguenti:

-   I valori degli atomi integer sono compresi nell'intervallo compreso tra 0x0001 e 0xBFFF (**MAXINTATOM**-1).
-   La rappresentazione di stringa di un Atom Integer è \# *dddd*, dove i valori rappresentati da *dddd* sono cifre decimali. Gli zeri iniziali vengono ignorati.
-   Nessun conteggio dei riferimenti o overhead di archiviazione associato a un Atom di tipo Integer.

## <a name="atom-creation-and-usage-count"></a>Conteggio utilizzo e creazione Atom

Un'applicazione crea un Atom locale chiamando la funzione [**AddAtom**](/windows/desktop/api/Winbase/nf-winbase-addatomw) . viene creato un Atom globale chiamando la funzione [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) . Entrambe le funzioni richiedono un puntatore a una stringa. Il sistema esegue la ricerca della stringa nella tabella Atom appropriata e restituisce l'Atom corrispondente all'applicazione. Nel caso di un Atom di stringa, se la stringa si trova già nella tabella Atom, il sistema incrementa il conteggio dei riferimenti per la stringa durante questo processo.

Le chiamate ripetute per aggiungere lo stesso nome Atom restituiscono lo stesso Atom. Se il nome Atom non esiste nella tabella quando viene chiamato [**AddAtom**](/windows/desktop/api/Winbase/nf-winbase-addatomw) , il nome Atom viene aggiunto alla tabella e viene restituito un nuovo Atom. Se si tratta di una stringa Atom, il conteggio dei riferimenti viene impostato su uno.

Quando non è più necessario usare un Atom locale, un'applicazione deve chiamare la funzione [**DeleteAtom**](/windows/desktop/api/Winbase/nf-winbase-deleteatom) . deve chiamare la funzione [**GlobalDeleteAtom**](/windows/desktop/api/Winbase/nf-winbase-globaldeleteatom) quando non è più necessario un Atom globale. Nel caso di una stringa Atom, una di queste funzioni riduce il conteggio dei riferimenti del Atom corrispondente di uno. Quando il conteggio dei riferimenti raggiunge zero, il sistema elimina il nome Atom dalla tabella.

Il nome Atom di un Atom di stringa rimane nella tabella Atom globale purché il conteggio dei riferimenti sia maggiore di zero, anche dopo che l'applicazione che lo ha inserito nella tabella viene terminata. Una tabella atom locale viene distrutta quando l'applicazione associata viene terminata, indipendentemente dal conteggio dei riferimenti degli atomi nella tabella.

## <a name="atom-table-queries"></a>Query di Atom-Table

Un'applicazione può determinare se una determinata stringa si trova già in una tabella Atom usando la funzione [**FindAtom**](/windows/desktop/api/Winbase/nf-winbase-findatoma) o [**GlobalFindAtom**](/windows/desktop/api/Winbase/nf-winbase-globalfindatoma) . Queste funzioni ricercano una tabella Atom per la stringa specificata e, se la stringa è presente, restituiscono il valore Atom corrispondente.

Un'applicazione può utilizzare la funzione [**GetAtomName**](/windows/desktop/api/Winbase/nf-winbase-getatomnamea) o [**GlobalGetAtomName**](/windows/desktop/api/Winbase/nf-winbase-globalgetatomnamea) per recuperare una stringa del nome Atom da una tabella Atom, purché l'applicazione disponga del valore Atom corrispondente alla stringa cercata. Entrambe le funzioni copiano la stringa del nome Atom del Atom specificato in un buffer e restituiscono la lunghezza della stringa copiata. **GetAtomName** recupera una stringa del nome Atom da una tabella atom locale e **GlobalGetAtomName** recupera una stringa del nome Atom dalla tabella Atom globale.

## <a name="atom-string-formats"></a>Formati di stringa Atom

Le funzioni [**AddAtom**](/windows/desktop/api/Winbase/nf-winbase-addatomw), [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma), [**FindAtom**](/windows/desktop/api/Winbase/nf-winbase-findatoma)e [**GlobalFindAtom**](/windows/desktop/api/Winbase/nf-winbase-globalfindatoma) accettano un puntatore a una stringa con terminazione null. Un'applicazione può specificare questo puntatore in uno dei modi seguenti.



|                    |                                                                                                    |
|--------------------|----------------------------------------------------------------------------------------------------|
| \#*dddd*           | Intero specificato come stringa decimale. Utilizzato per creare o trovare un Atom di tipo Integer.                  |
| *nome Atom stringa* | Nome Atom della stringa. Utilizzato per aggiungere un nome Atom di stringa a una tabella Atom e ricevere un Atom in return. |



 

 

 
