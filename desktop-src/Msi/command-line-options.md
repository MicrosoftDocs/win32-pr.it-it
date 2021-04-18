---
description: Opzioni della riga di comando per msiexec.exe per Windows Installer 3,0 e versioni precedenti. Fornisce una tabella che Mostra opzioni, parametri e descrizioni. Esempi che illustrano come installare i prodotti e altre attività.
ms.assetid: a70d8cc8-af47-4472-aabc-97481d97080d
title: Opzioni della riga di comando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46fe56026c21e4120963c86b4de08decc85b2a58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315480"
---
# <a name="command-line-options"></a>Opzioni della riga di comando

Il programma eseguibile che interpreta i pacchetti e installa i prodotti è Msiexec.exe. Si noti che Msiexec imposta anche un livello di errore in return corrispondente ai [codici di errore di sistema](/windows/desktop/Debug/system-error-codes). Le opzioni della riga di comando non fanno distinzione tra maiuscole e minuscole.

Le opzioni della riga di comando nella tabella seguente sono disponibili con Windows Installer 3,0 e versioni precedenti. Le [Opzioni di Command-Line del programma di installazione standard](standard-installer-command-line-options.md) sono disponibili anche a partire da Windows Installer 3,0.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Opzione</th>
<th>Parametri</th>
<th>Significato</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>/I</strong></td>
<td><em>Pacchetto | ProductCode</em></td>
<td>Installa o configura un prodotto.<br/></td>
</tr>
<tr class="even">
<td><strong>/f</strong></td>
<td>[p | o | e | d | c | a | u | m | s | v] <em>Pacchetto</em> | di <em>ProductCode</em></td>
<td>Ripristina un prodotto. Questa opzione Ignora tutti i valori di proprietà immessi nella riga di comando. L'elenco di argomenti predefinito per questa opzione è' omus '. Questa opzione condivide lo stesso elenco di argomenti della proprietà <a href="reinstallmode.md"><strong>REINSTALLMODE</strong></a> .<br/> p-Reinstalla solo se il file è mancante.<br/> o-reinstalla se il file è mancante o se è installata una versione precedente.<br/> e-reinstalla se il file è mancante o se è installata una versione uguale o precedente.<br/> d: Reinstalla se il file è mancante o se è installata una versione diversa.<br/> c: Reinstalla se il file è mancante o il checksum archiviato non corrisponde al valore calcolato. Ripristina solo i file con <strong>msidbFileAttributesChecksum</strong> nella colonna attributi della tabella <a href="file-table.md">file</a> .<br/> a: forza la reinstallazione di tutti i file.<br/> u-riscrive tutte le voci del registro di sistema obbligatorie specifiche dell'utente.<br/> m: riscrive tutte le voci del registro di sistema richieste specifiche del computer.<br/> s-sovrascrive tutti i collegamenti esistenti.<br/> v-viene eseguito dall'origine e memorizza nuovamente nella cache il pacchetto locale. Non usare l'opzione di reinstallazione <strong>v</strong> per la prima installazione di un'applicazione o di una funzionalità.<br/></td>
</tr>
<tr class="odd">
<td><strong>/a</strong></td>
<td><em>Pacchetto</em></td>
<td>Opzione di <a href="administrative-installation.md">installazione amministrativa</a> . Installa un prodotto nella rete.<br/></td>
</tr>
<tr class="even">
<td><strong>/x</strong></td>
<td><em>Pacchetto | ProductCode</em></td>
<td>Disinstalla un prodotto.</td>
</tr>
<tr class="odd">
<td><strong>/j</strong></td>
<td>[u | m] <em>Pacchetto</em> di<br/> [u | m] <em>Elenco di trasformazioni</em> <em>pacchetto</em><strong>/t</strong><br/> <em>or</em><br/> [u | m] <em>Pacchetto</em><strong>/g</strong><em>LanguageID</em><br/></td>
<td>Annuncia un prodotto. Questa opzione Ignora tutti i valori di proprietà immessi nella riga di comando.<br/> u-annuncia l'utente corrente.<br/> m: annuncia a tutti gli utenti del computer.<br/> Identificatore della lingua g.<br/> t-applica la trasformazione al pacchetto annunciato.<br/></td>
</tr>
<tr class="even">
<td><strong>/L</strong></td>
<td>[i | w | e | a | r | u | c | m | o | p | v | x | + |! | *] <em>Logfile</em></td>
<td>Scrive le informazioni di registrazione in un file di log nel percorso esistente specificato. Il percorso del percorso del file di log deve essere già esistente. Il programma di installazione non crea la struttura di directory per il file di log. Flag indica le informazioni da registrare. Se non viene specificato alcun flag, il valore predefinito è "iwearmo".<br/> i-messaggi di stato.<br/> w-avvisi non irreversibili.<br/> e-tutti i messaggi di errore.<br/> a: avvio delle azioni.<br/> r-record specifici dell'azione.<br/> richieste u-user.<br/> c-parametri iniziali dell'interfaccia utente.<br/> m-memoria insufficiente o informazioni di uscita irreversibili.<br/> messaggi o-out-of-disk-space.<br/> p-proprietà del terminale.<br/> output v-verbose.<br/> x: informazioni aggiuntive sul debug. <strong>Windows Installer 2,0:</strong> Non supportato. L'opzione x è disponibile con Windows Installer versione 3.0.3790.2180 e successive.<br/> <br/> + - Accoda a file esistente.<br/> ! -Scarica ogni riga nel log.<br/> &quot;*&quot; -Wildcard, registra tutte le informazioni eccetto le opzioni v e x. Per includere le opzioni v e x, specificare &quot; /l* VX &quot; .<br/>
<blockquote>
[!Note]<br />
Per ulteriori informazioni su tutti i metodi disponibili per l'impostazione della modalità di registrazione, vedere <a href="normal-logging.md">registrazione normale</a> nella sezione <a href="windows-installer-logging.md">registrazione Windows Installer</a>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><strong>/m</strong></td>
<td><em>filename</em>
<blockquote>
[!Note]<br />
La lunghezza del <em>nome file</em> non può superare gli otto caratteri.
</blockquote>
<br/></td>
<td>Genera un file MIF di stato SMS. Deve essere utilizzato con le opzioni installa (-i), Rimuovi (-x), installazione amministrativa (-a) o reinstalla (-f). Il ISMIF32.DLL viene installato come parte di SMS e deve trovarsi nel percorso.<br/> I campi del file MIF di stato sono compilati con le seguenti informazioni:<br/> Produttore- <a href="author-summary.md"> <strong>autore</strong></a><br/> Prodotto- <a href="revision-number-summary.md"> <strong>numero revisione</strong></a><br/> Versione- <a href="subject-summary.md"> <strong>oggetto</strong></a><br/> Impostazioni locali- <a href="template-summary.md"> <strong>modello</strong></a><br/> Numero di serie-non impostato<br/> Installazione-impostata da ISMIF32.DLL a &quot; DateTime&quot;<br/> InstallStatus- &quot; operazione riuscita &quot; o &quot; non riuscita&quot;<br/> Descrizione-messaggi di errore nell'ordine seguente: 1) messaggi di errore generati dal programma di installazione. 2) risorsa da Msi.dll se l'installazione non è stata avviata o se l'utente non è stata chiusa. 3) file del messaggio di errore di sistema. 4) messaggio formattato: &quot; errore del programma di installazione% i &quot; , dove% i è un errore restituito da Msi.dll.<br/></td>
</tr>
<tr class="even">
<td><strong>/p</strong></td>
<td><em>PacchettoPatch [;P atchpackage2</em> ]</td>
<td>Applica una patch. Per applicare una patch a un'immagine amministrativa installata, è necessario combinare le opzioni seguenti:<br/> /p <em> <PatchPackage> [;p atchpackage2] </em> /a<em><Package></em><br/></td>
</tr>
<tr class="odd">
<td><strong>/q</strong></td>
<td>n | b | r | f</td>
<td>Imposta il <a href="user-interface-levels.md">livello dell'interfaccia utente</a>.<br/> d, qn-Nessuna interfaccia utente<br/> qb- <a href="b-gly.md"><em>interfaccia utente di base</em></a>. Usare QB! per nascondere il pulsante <strong>Annulla</strong> .<br/> <a href="r-gly.md"><em>interfaccia utente ridotta</em></a> a QR senza finestra di dialogo modale visualizzata alla fine dell'installazione.<br/> QF- <a href="f-gly.md"><em>interfaccia utente completa</em></a> e tutte le finestre di dialogo <a href="fatalerror-dialog.md">FatalError</a>, <a href="userexit-dialog.md">UserExit</a>o <a href="exit-dialog.md">Exit</a> modale create alla fine.<br/> Qn +-nessuna interfaccia utente ad eccezione di una finestra di dialogo modale visualizzata alla fine.<br/> qb +- <a href="b-gly.md"><em>interfaccia utente di base</em></a> con una finestra di dialogo modale visualizzata alla fine. La casella modale non viene visualizzata se l'utente annulla l'installazione. Usare QB +! o qb! + per nascondere il pulsante <strong>Annulla</strong> .<br/> QB: <a href="b-gly.md"><em>interfaccia utente di base</em></a> senza finestre di dialogo modali. Si noti che/QB +-non è un livello di interfaccia utente supportato. Usare QB-! o qb!-per nascondere il pulsante <strong>Annulla</strong> .<br/> Si noti che il! l'opzione è disponibile con Windows Installer 2,0 e funziona solo con l'interfaccia utente di base. Non è valido con l'interfaccia utente completa.<br/></td>
</tr>
<tr class="even">
<td><strong>/?</strong> o <strong>/h</strong></td>
<td> </td>
<td>Visualizza le informazioni sul copyright per Windows Installer.<br/></td>
</tr>
<tr class="odd">
<td><strong>/y</strong></td>
<td><em>modulo</em></td>
<td>Chiama la funzione di sistema <strong>DllRegisterServer</strong> per registrare autonomamente i moduli passati nella riga di comando. Specificare il percorso completo della DLL. Ad esempio, per MY_FILE.DLL nella cartella corrente, è possibile usare:<br/> <strong>.\MY_FILE.DLLmsiexec/y </strong><br/> Questa opzione viene utilizzata solo per le informazioni del registro di sistema che non possono essere aggiunte utilizzando le tabelle del registro di sistema del file con estensione msi.<br/></td>
</tr>
<tr class="even">
<td><strong>/z</strong></td>
<td><em>modulo</em></td>
<td>Chiama la funzione di sistema <strong>DllUnregisterServer</strong> per annullare la registrazione dei moduli passati nella riga di comando. Specificare il percorso completo della DLL. Ad esempio, per MY_FILE.DLL nella cartella corrente, è possibile usare: <br/> <strong>.\MY_FILE.DLLmsiexec/z </strong><br/> Questa opzione viene utilizzata solo per le informazioni del registro di sistema che non possono essere rimosse utilizzando le tabelle del registro di sistema del file con estensione msi.<br/></td>
</tr>
<tr class="odd">
<td><strong>/c</strong></td>

<td>Annuncia una nuova istanza del prodotto. Deve essere usato insieme a/t. Disponibile a partire dalla versione Windows Installer fornita con Windows Server 2003 e Windows XP con Service Pack 1 (SP1).<br/></td>
</tr>
<tr class="even">
<td><strong>/n</strong></td>
<td><em>ProductCode</em></td>
<td>Specifica un'istanza specifica del prodotto. Utilizzato per identificare un'istanza di installata utilizzando il supporto di più istanze tramite le trasformazioni del codice del prodotto. Disponibile a partire dalla versione Windows Installer fornita con Windows Server 2003 e Windows XP con SP1. <br/></td>
</tr>
</tbody>
</table>



 

Le opzioni/i,/x,/f \[ p \| o \| e \| d \| c \| a \| u \| m \| s \| v \] ,/j \[ u \| m \] ,/a,/p,/y e/z non devono essere utilizzate insieme. L'unica eccezione a questa regola è che l'applicazione di patch a un' [installazione amministrativa](administrative-installation.md) richiede l'utilizzo di/p e/a. Le opzioni/t,/c e/g devono essere usate solo con/j. È possibile usare le opzioni/l e/q con/i,/x,/f \[ p \| o \| e \| d \| c \| a \| u \| m \| s \| v \] ,/j \[ u \| m \] ,/a e/p. L'opzione/n può essere usata con/i,/f,/x e/p.

Per installare un prodotto da un: \\Example.msi, installare il prodotto come indicato di seguito:

**msiexec/i A: \\Example.msi**

È possibile modificare solo le [proprietà pubbliche](public-properties.md) utilizzando la riga di comando. Tutti i nomi di proprietà nella riga di comando vengono interpretati come caratteri maiuscoli, ma il valore mantiene la distinzione tra maiuscole e minuscole. Se si immette la **Proprietà** sulla riga di comando, il programma di installazione esegue l'override del valore di SetProperty e non del valore di **SetProperty** nella tabella delle proprietà. Per ulteriori informazioni, vedere [informazioni sulle proprietà](about-properties.md).

Per installare un prodotto con la proprietà impostata su VALUE, utilizzare la sintassi seguente nella riga di comando. È possibile inserire la proprietà in un punto qualsiasi, tranne che tra un'opzione e il relativo argomento.

Sintassi corretta:

**msiexec/i A: \\Example.msi Property = Value**

Sintassi non corretta:

**msiexec/i PROPERTY = valore A: \\Example.msi**

I valori delle proprietà che sono stringhe letterali devono essere racchiusi tra virgolette. Includere gli spazi vuoti nella stringa tra i contrassegni.

**msiexec/i A: \\Example.msi Property = "spazi vuoti incorporati"**

Per cancellare una proprietà pubblica tramite la riga di comando, impostarne il valore su una stringa vuota.

**msiexec/i A: \\Example.msi Property = ""**

Per le sezioni di testo separate da virgolette letterali, racchiudere la sezione con una seconda coppia di virgolette.

**msiexec/i A: \\Example.msi Property = "embedded" "virgolette" "spazio vuoto"**

Nell'esempio seguente viene illustrata una riga di comando complessa.

**msiexec/i testdb.msi INSTALLLEVEL = 3/l \* MSI. log CompanyName = "Acme" "widgets" "e" "Gizmos." "**

Nell'esempio seguente vengono illustrate le opzioni dell'annuncio. Si noti che le opzioni non fanno distinzione tra maiuscole e minuscole.

**msiexec/JM msisample.msi/T Transform. MST/LIME logfile.txt**

Nell'esempio seguente viene illustrato come installare una nuova istanza di un prodotto da annunciare. Questo prodotto viene creato per supportare le trasformazioni di più istanze.

**msiexec/JM msisample.msi/T: Instance1. MST; Customization. MST/c/LIME logfile.txt**

Nell'esempio seguente viene illustrato come applicare una patch a un'istanza di un prodotto installato utilizzando trasformazioni di più istanze.

**msiexec/p msipatch. msp; msipatch2. msp/n {00000001-0002-0000-0000-624474736554} /qb**

Quando si applicano patch a un prodotto specifico, le opzioni/i e/p non possono essere specificate insieme in una riga di comando. In questo caso, è possibile applicare le patch a un prodotto come indicato di seguito.

**msiexec/i A: \\Example.msi patch = msipatch. msp; msipatch2. msp/QB**

Non è possibile impostare la proprietà [**patch**](patch.md) in una riga di comando quando viene usata l'opzione/p. Se la proprietà **patch** è impostata quando si usa l'opzione/p, il valore della proprietà **patch** viene ignorato e sovrascritto.

 

