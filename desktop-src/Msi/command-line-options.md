---
description: Opzioni della riga di comando per msiexec.exe per Windows Installer 3.0 e versioni precedenti. Fornisce una tabella che mostra opzioni, parametri e descrizioni. Esempi che illustrano come installare prodotti e altre attività.
ms.assetid: a70d8cc8-af47-4472-aabc-97481d97080d
title: Opzioni della riga di comando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 287b5711468217105846a13496a23794235bbcfdfcbd0e79278aaba17e7c0341
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118380315"
---
# <a name="command-line-options"></a>Opzioni della riga di comando

Il programma eseguibile che interpreta i pacchetti e installa i prodotti è Msiexec.exe. Si noti che Msiexec imposta anche un livello di errore al ritorno che corrisponde ai codici [di errore di sistema](/windows/desktop/Debug/system-error-codes). Le opzioni della riga di comando non fa distinzione tra maiuscole e minuscole.

Le opzioni della riga di comando nella tabella seguente sono disponibili con Windows Installer 3.0 e versioni precedenti. Il [programma di Command-Line standard è](standard-installer-command-line-options.md) disponibile anche a partire da Windows Installer 3.0.



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
<td><strong>/i</strong></td>
<td><em>Pacchetto| Productcode</em></td>
<td>Installa o configura un prodotto.<br/></td>
</tr>
<tr class="even">
<td><strong>/f</strong></td>
<td>[p|o|e|d|c|a|u|m|s|v] <em>Pacchetto</em> | <em>Codice Prodotto</em></td>
<td>Ripristina un prodotto. Questa opzione ignora tutti i valori delle proprietà immessi nella riga di comando. L'elenco di argomenti predefinito per questa opzione è 'omus'. Questa opzione condivide lo stesso elenco di argomenti della <a href="reinstallmode.md"><strong>proprietà REINSTALLMODE.</strong></a><br/> p : reinstalla solo se il file non è presente.<br/> o - Reinstalla se il file è mancante o se è installata una versione precedente.<br/> e : reinstalla se il file è mancante o se è installata una versione uguale o precedente.<br/> d : reinstalla se il file non è presente o se è installata una versione diversa.<br/> c : reinstalla se il file non è presente o il checksum archiviato non corrisponde al valore calcolato. Ripristina solo i file con <strong>msidbFileAttributesChecksum</strong> nella colonna Attributi della <a href="file-table.md">tabella File.</a><br/> a : forza la reinstallazione di tutti i file.<br/> u : riscrive tutte le voci del Registro di sistema specifiche dell'utente necessarie.<br/> m : riscrive tutte le voci del Registro di sistema specifiche del computer necessarie.<br/> s : sovrascrive tutti i collegamenti esistenti.<br/> v: viene eseguito dall'origine e memorizza nuovamente nella cache il pacchetto locale. Non usare <strong>l'opzione v</strong> reinstall per la prima installazione di un'applicazione o di una funzionalità.<br/></td>
</tr>
<tr class="odd">
<td><strong>/a</strong></td>
<td><em>Pacchetto</em></td>
<td><a href="administrative-installation.md">Opzione di installazione</a> amministrativa. Installa un prodotto in rete.<br/></td>
</tr>
<tr class="even">
<td><strong>/x</strong></td>
<td><em>Pacchetto| Productcode</em></td>
<td>Disinstalla un prodotto.</td>
</tr>
<tr class="odd">
<td><strong>/j</strong></td>
<td>[u|m] <em>Packageor</em><br/> [u|m] <em>Package</em><strong>/t</strong><em>Transform List</em><br/> <em>or</em><br/> [u|m] <em>Pacchetto</em><strong>/g</strong><em>LanguageID</em><br/></td>
<td>Annuncia un prodotto. Questa opzione ignora tutti i valori delle proprietà immessi nella riga di comando.<br/> u : annuncia all'utente corrente.<br/> m : annuncia a tutti gli utenti del computer.<br/> g : identificatore della lingua.<br/> t : applica la trasformazione al pacchetto annunciato.<br/></td>
</tr>
<tr class="even">
<td><strong>/L</strong></td>
<td>[i|w|e|a|r|u|c|m|o|p|v|x|+|!| *] <em>File di log</em></td>
<td>Scrive le informazioni di registrazione in un file di log nel percorso esistente specificato. Il percorso del file di log deve esistere già. Il programma di installazione non crea la struttura di directory per il file di log. I flag indicano le informazioni da registrare. Se non viene specificato alcun flag, il valore predefinito è "i sistema".<br/> i : messaggi di stato.<br/> w : avvisi non irreversibile.<br/> e : tutti i messaggi di errore.<br/> a : avvio delle azioni.<br/> r: record specifici dell'azione.<br/> u : richieste dell'utente.<br/> c : parametri iniziali dell'interfaccia utente.<br/> m : informazioni di uscita di memoria insufficiente o irreversibile.<br/> o - Messaggi di spazio su disco insufficiente.<br/> p : proprietà del terminale.<br/> v : output dettagliato.<br/> x: informazioni di debug aggiuntive. <strong>Windows Installer 2.0:</strong> Non supportato. L'opzione x è disponibile con Windows Installer versione 3.0.3790.2180 e successive.<br/> <br/> + - Accoda a un file esistente.<br/> ! - Scarica ogni riga nel log.<br/> &quot;*&quot; - Carattere jolly, registrare tutte le informazioni ad eccezione delle opzioni v e x. Per includere le opzioni v e x, specificare &quot; /l* vx &quot; .<br/>
<blockquote>
[!Note]<br />
Per altre informazioni su tutti i metodi disponibili per l'impostazione della modalità di registrazione, vedere <a href="normal-logging.md">Registrazione</a> normale nella Windows <a href="windows-installer-logging.md">registrazione del</a> programma di installazione
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><strong>/m</strong></td>
<td><em>Filename</em>
<blockquote>
[!Note]<br />
La lunghezza del <em>nome file</em> non deve essere superiore a otto caratteri.
</blockquote>
<br/></td>
<td>Genera un file con estensione mif di stato SMS. Deve essere usato con le opzioni di installazione (-i), rimozione (-x), installazione amministrativa (-a) o reinstallazione (-f). Il ISMIF32.DLL viene installato come parte di SMS e deve essere nel percorso .<br/> I campi del file mif di stato vengono compilati con le informazioni seguenti:<br/> Produttore - <a href="author-summary.md"> <strong>Autore</strong></a><br/> Prodotto - <a href="revision-number-summary.md"> <strong>Numero revisione</strong></a><br/> Versione - <a href="subject-summary.md"> <strong>Oggetto</strong></a><br/> Impostazioni locali - <a href="template-summary.md"> <strong>Modello</strong></a><br/> Numero di serie: non impostato<br/> Installazione: impostata ISMIF32.DLL su &quot; DateTime&quot;<br/> InstallStatus - &quot; Operazione riuscita o non &quot; &quot; riuscita&quot;<br/> Descrizione: messaggi di errore nell'ordine seguente: 1) Messaggi di errore generati dal programma di installazione. 2) Risorsa da Msi.dll se non è stato possibile avviare l'installazione o uscire dall'utente. 3) File di messaggi di errore di sistema. 4) Messaggio formattato: errore &quot; del programma di installazione %i , dove &quot; %i è l'errore restituito da Msi.dll.<br/></td>
</tr>
<tr class="even">
<td><strong>/p</strong></td>
<td><em>PatchPackage[;p atchPackage2</em> ]</td>
<td>Applica una patch. Per applicare una patch a un'immagine amministrativa installata, è necessario combinare le opzioni seguenti:<br/> /p <em> <PatchPackage> [;p atchPackage2 ] </em> /a<em><Package></em><br/></td>
</tr>
<tr class="odd">
<td><strong>/q</strong></td>
<td>n|b|r|f</td>
<td>Imposta il <a href="user-interface-levels.md">livello dell'interfaccia utente</a>.<br/> q , qn - Nessuna interfaccia utente<br/> qb - Interfaccia <a href="b-gly.md"><em>utente di base.</em></a> Usare qb! per nascondere il <strong>pulsante</strong> Annulla.<br/> qr : <a href="r-gly.md"><em>interfaccia utente ridotta</em></a> senza finestra di dialogo modale visualizzata al termine dell'installazione.<br/> qf: <a href="f-gly.md"><em>interfaccia utente</em></a> completa ed eventuali finestre di dialogo modali <a href="fatalerror-dialog.md">FatalError,</a> <a href="userexit-dialog.md">UserExit</a>o <a href="exit-dialog.md">Exit</a> scritte nella parte finale.<br/> qn+ - Nessuna interfaccia utente ad eccezione di una finestra di dialogo modale visualizzata alla fine.<br/> qb+ - <a href="b-gly.md"><em>Interfaccia utente di</em></a> base con una finestra di dialogo modale visualizzata alla fine. La casella modale non viene visualizzata se l'utente annulla l'installazione. Usare qb+! o qb!+ per nascondere il <strong>pulsante</strong> Annulla.<br/> qb- - Interfaccia <a href="b-gly.md"><em>utente di base</em></a> senza finestre di dialogo modali. Si noti che /qb+- non è un livello di interfaccia utente supportato. Usare qb-! o qb!- per nascondere il <strong>pulsante</strong> Annulla.<br/> Si noti che l'oggetto ! L'opzione è disponibile con Windows Installer 2.0 e funziona solo con l'interfaccia utente di base. Non è valida con l'interfaccia utente completa.<br/></td>
</tr>
<tr class="even">
<td><strong>/?</strong> o <strong>/h</strong></td>
<td> </td>
<td>Visualizza le informazioni sul copyright per Windows programma di installazione.<br/></td>
</tr>
<tr class="odd">
<td><strong>/y</strong></td>
<td><em>Modulo</em></td>
<td>Chiama la funzione di sistema <strong>DllRegisterServer per</strong> registrare automaticamente i moduli passati nella riga di comando. Specificare il percorso completo della DLL. Ad esempio, per MY_FILE.DLL nella cartella corrente è possibile usare:<br/> <strong>msiexec /y .\MY_FILE.DLL</strong><br/> Questa opzione viene utilizzata solo per le informazioni del Registro di sistema che non possono essere aggiunte utilizzando le tabelle del Registro di sistema del file .msi file.<br/></td>
</tr>
<tr class="even">
<td><strong>/z</strong></td>
<td><em>Modulo</em></td>
<td>Chiama la funzione di sistema <strong>DllUnRegisterServer per</strong> annullare la registrazione dei moduli passati nella riga di comando. Specificare il percorso completo della DLL. Ad esempio, per MY_FILE.DLL nella cartella corrente è possibile usare: <br/> <strong>msiexec /z .\MY_FILE.DLL</strong><br/> Questa opzione viene utilizzata solo per le informazioni del Registro di sistema che non possono essere rimosse utilizzando le tabelle del Registro di sistema del file .msi file.<br/></td>
</tr>
<tr class="odd">
<td><strong>/c</strong></td>

<td>Annuncia una nuova istanza del prodotto. Deve essere usato in combinazione con /t. Disponibile a partire dalla versione Windows Installer fornita con Windows Server 2003 e Windows XP con Service Pack 1 (SP1).<br/></td>
</tr>
<tr class="even">
<td><strong>/n</strong></td>
<td><em>ProductCode</em></td>
<td>Specifica una particolare istanza del prodotto. Consente di identificare un'istanza installata utilizzando il supporto di più istanze tramite trasformazioni di modifica del codice prodotto. Disponibile a partire dalla Windows Installer fornita con Windows Server 2003 e Windows XP con SP1. <br/></td>
</tr>
</tbody>
</table>



 

Le opzioni /i, /x, /f \[ p e d c a u m s \| v \| , \| \| \| \| \| \| \| \] /j u m , \[ \| \] /a, /p, /y e /z non devono essere usate insieme. L'unica eccezione a questa regola è che l'applicazione di patch a un'installazione [amministrativa](administrative-installation.md) richiede l'uso di /p e /a. Le opzioni /t, /c e /g devono essere usate solo con /j. Le opzioni /l e /q possono essere usate con /i, /x, /f \[ p o e d c a u m s \| v \| , \| \| \| \| \| \| \| \] /j u m , \[ \| \] /a e /p. L'opzione /n può essere usata con /i, /f, /x e /p.

Per installare un prodotto da A: \\Example.msi, installare il prodotto come segue:

**msiexec /i A: \\Example.msi**

Solo [le proprietà pubbliche](public-properties.md) possono essere modificate tramite la riga di comando. Tutti i nomi di proprietà nella riga di comando vengono interpretati in maiuscolo, ma il valore mantiene la distinzione tra maiuscole e minuscole. Se si immette **MyProperty** dalla riga di comando, il programma di installazione esegue l'override del valore di MYPROPERTY e non del valore **di MyProperty** nella tabella Property. Per altre informazioni, vedere [Informazioni sulle proprietà.](about-properties.md)

Per installare un prodotto con PROPERTY impostato su VALUE, usare la sintassi seguente nella riga di comando. È possibile inserire la proprietà in qualsiasi punto tranne che tra un'opzione e il relativo argomento.

Sintassi corretta:

**msiexec /i A: \\Example.msi PROPERTY=VALUE**

Sintassi non corretta:

**msiexec /i PROPERTY=VALUE A: \\Example.msi**

I valori delle proprietà che sono stringhe letterali devono essere racchiusi tra virgolette. Includere eventuali spazi vuoti nella stringa tra i contrassegni.

**msiexec /i A: \\Example.msi PROPERTY="Spazio vuoto incorporato"**

Per cancellare una proprietà pubblica tramite la riga di comando, impostarne il valore su una stringa vuota.

**msiexec /i A: \\Example.msi PROPERTY=""**

Per le sezioni di testo separate da virgolette letterali, racchiudere la sezione tra una seconda coppia di virgolette.

**msiexec /i A: \\Example.msi PROPERTY="Embedded ""Quotes"" White Space"**

L'esempio seguente illustra una riga di comando complessa.

**msiexec /i testdb.msi INSTALLLEVEL=3 /l \* msi.log COMPANYNAME="Acme ""Widgets" e ""Gizmos."""**

Nell'esempio seguente vengono illustrate le opzioni relative agli annunci. Si noti che le opzioni non supportano la distinzione tra maiuscole e minuscole.

**msiexec /JM msisample.msi /T transform.mst /logfile.txt**

L'esempio seguente illustra come installare una nuova istanza di un prodotto da annunciare. Questo prodotto è stato creato per supportare trasformazioni a più istanze.

**msiexec /JM msisample.msi /T :instance1.mst;customization.mst /c /logfile.txt**

Nell'esempio seguente viene illustrato come applicare patch a un'istanza di un prodotto installato utilizzando trasformazioni a più istanze.

**msiexec /p msipatch.msp;msipatch2.msp /n {00000001-0002-0000-0000-624474736554} /qb**

Quando si applicano patch a un prodotto specifico, le opzioni /i e /p non possono essere specificate insieme in una riga di comando. In questo caso, è possibile applicare patch a un prodotto come indicato di seguito.

**msiexec /i A: \\Example.msi PATCH=msipatch.msp;msipatch2.msp /qb**

La [**proprietà PATCH**](patch.md) non può essere impostata in una riga di comando quando si usa l'opzione /p. Se la **proprietà PATCH** viene impostata quando si usa l'opzione /p , il valore della **proprietà PATCH** viene ignorato e sovrascritto.

 

