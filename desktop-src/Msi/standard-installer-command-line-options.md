---
Descrizione: il programma eseguibile che interpreta i pacchetti e installa i prodotti è Msiexec.exe. Nota Msiexec imposta anche un livello di errore in return corrispondente ai codici di errore di sistema. Nella tabella seguente vengono identificate le opzioni della riga di comando standard per il programma. Le opzioni della riga di comando non fanno distinzione tra maiuscole e minuscole. Windows Installer 2,0: le opzioni della riga di comando identificate in questo argomento sono disponibili a partire da Windows Installer 3,0. Le opzioni Windows Installer Command-Line sono disponibili con Windows Installer&\# 160; 3.0 e versioni precedenti.
ms. AssetID: b1707c88-1cca-45AB-BB23-6002bfd5204e title: programma di installazione standard Command-Line opzioni ms. Topic: articolo ms. Date: 05/31/2018
---

# <a name="standard-installer-command-line-options"></a>Opzioni di Command-Line del programma di installazione standard

Il programma eseguibile che interpreta i pacchetti e installa i prodotti è Msiexec.exe.

> [!Note]  
> Msiexec imposta anche un livello di errore al ritorno che corrisponde ai [codici di errore di sistema](../debug/system-error-codes.md).

 

Nella tabella seguente vengono identificate le opzioni della riga di comando standard per il programma. Le opzioni della riga di comando non fanno distinzione tra maiuscole e minuscole.

**Windows Installer 2,0:** Le opzioni della riga di comando identificate in questo argomento sono disponibili a partire da Windows Installer 3,0. Le [Opzioni della riga di comando](command-line-options.md) Windows Installer sono disponibili con Windows Installer 3,0 e versioni precedenti.



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
<td><strong>/Help</strong></td>
<td> </td>
<td>Guida e opzioni di riferimento rapido. Visualizza l'utilizzo corretto del comando di installazione, incluso un elenco di tutte le opzioni e il comportamento. La descrizione dell'utilizzo può essere visualizzata nell'interfaccia utente. L'uso errato di qualsiasi opzione richiama questa opzione della guida.<br/> Esempio: <strong>msiexec/Help</strong><br/>
<blockquote>
[!Note]<br />
L'opzione della <a href="command-line-options.md">riga di comando</a> Windows Installer equivalente è <strong>/?</strong>.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><strong>/quiet</strong></td>
<td> </td>
<td>Opzione di visualizzazione non interattiva. Il programma di installazione esegue un'installazione senza visualizzare un'interfaccia utente. Non vengono visualizzati messaggi di richiesta, messaggi o finestre di dialogo per l'utente. L'utente non può annullare l'installazione. Usare le opzioni della riga di comando standard <strong>/norestart</strong> o <strong>/forcerestart</strong> per controllare i riavvii. Se non vengono specificate opzioni di riavvio, il programma di installazione riavvia il computer ogni volta che è necessario senza visualizzare alcun messaggio di richiesta o avviso per l'utente.<br/> Esempi: <br/> <strong>msiexec/package Application.msi/quiet</strong><br/> <strong>Msiexec/Uninstall Application.msi/quiet</strong><br/> <strong>Msiexec/Update msipatch. msp/quiet</strong><br/> <strong>Msiexec/Uninstall msipatch. msp/Package Application.msi/quiet</strong><br/>
<blockquote>
[!Note]<br />
L'opzione della <a href="command-line-options.md">riga di comando</a> equivalente Windows Installer è <strong>/qn</strong>.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><strong>/passive</strong></td>
<td> </td>
<td>Opzione di visualizzazione passiva. Il programma di installazione visualizza all'utente un indicatore di stato che indica che è in corso un'installazione, ma non vengono visualizzati messaggi di richiesta o messaggi di errore. L'utente non può annullare l'installazione. Usare le opzioni della riga di comando standard <strong>/norestart</strong> o <strong>/forcerestart</strong> per controllare i riavvii. Se non viene specificata alcuna opzione di riavvio, il programma di installazione riavvia il computer ogni volta che è necessario senza visualizzare alcun messaggio di richiesta o avviso per l'utente. <br/> Esempio: <strong>msiexec/package Application.msi/passive</strong> <br/>
<blockquote>
[!Note]<br />
L'opzione della <a href="command-line-options.md">riga di comando</a> Windows Installer equivalente è <strong>/qb!-</strong> con <a href="rebootprompt.md"><strong>REBOOTPROMPT</strong></a>= S impostata nella riga di comando.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><strong>/norestart</strong></td>
<td> </td>
<td>Non riavviare mai l'opzione. Il programma di installazione non riavvia mai il computer dopo l'installazione.<br/> Esempio: msiexec/package Application.msi <strong>/norestart</strong><br/>
<blockquote>
[!Note]<br />
La riga di comando Windows Installer equivalente è impostata su <a href="reboot.md"><strong>reboot</strong></a>= ReallySuppress nella riga di comando.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><strong>/forcerestart</strong></td>
<td> </td>
<td>Sempre l'opzione di riavvio. Il programma di installazione riavvia sempre il computer dopo ogni installazione.<br/> Esempio: msiexec/package Application.msi <strong>/forcerestart</strong><br/>
<blockquote>
[!Note]<br />
La riga di comando di Windows Installer equivalente ha <a href="reboot.md"><strong>reboot</strong></a>= Force impostato nella riga di comando.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><strong>/promptrestart</strong></td>
<td> </td>
<td>Richiedi conferma prima di riavviare l'opzione. Visualizza un messaggio che indica che è necessario riavviare il computer per completare l'installazione e chiede all'utente se riavviare il sistema adesso. Questa opzione non può essere usata in combinazione con l'opzione <strong>/quiet</strong> .<br/>
<blockquote>
[!Note]<br />
La riga di comando equivalente Windows Installer dispone di <a href="rebootprompt.md"><strong>REBOOTPROMPT</strong></a>  =  &quot; &quot; impostato nella riga di comando.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><strong>/Uninstall</strong></td>
<td><em><Package.msi|ProductCode></em></td>
<td>Disinstalla il prodotto. Disinstalla un prodotto.<br/>
<blockquote>
[!Note]<br />
L'opzione della <a href="command-line-options.md">riga di comando</a> Windows Installer equivalente è <strong>/x</strong>.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><strong>/Uninstall</strong></td>
<td><em>/Package <Package.msi | ProductCode> /Uninstall <Update1.msp | PatchGUID1> [; Update2. msp | PatchGUID2]</em></td>
<td>Opzione Disinstalla aggiornamento. Disinstalla una patch di aggiornamento.<br/>
<blockquote>
[!Note]<br />
L'opzione della <a href="command-line-options.md">riga di comando</a> Windows Installer equivalente è <strong>/i</strong> con <a href="msipatchremove.md"><strong>MSIPATCHREMOVE</strong></a>= Update1. msp | PatchGUID1[; Update2. msp | PatchGUID2] impostato nella riga di comando.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><strong>/log</strong></td>
<td><em><logfile></em></td>
<td>Opzione log. Scrive le informazioni di registrazione in un file di log nel percorso esistente specificato. Il percorso del percorso del file di log deve essere già esistente. Il programma di installazione non crea la struttura di directory per il file di log.<br/> Le seguenti informazioni vengono immesse nel log:<br/>
<ul>
<li>Messaggi di stato</li>
<li>Avvisi non irreversibili</li>
<li>Tutti i messaggi di errore</li>
<li>Avvio delle azioni</li>
<li>Record specifici dell'azione</li>
<li>Richieste utente</li>
<li>Parametri iniziali dell'interfaccia utente</li>
<li>Informazioni sulla memoria insufficiente o sull'uscita fatale</li>
<li>Messaggi spazio su disco esaurito</li>
<li>Proprietà Terminal</li>
</ul>
<blockquote>
[!Note]<br />
L'opzione della <a href="command-line-options.md">riga di comando</a> Windows Installer equivalente è <strong>/l *</strong>.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
Per ulteriori informazioni su tutti i metodi disponibili per l'impostazione della modalità di registrazione, vedere <a href="normal-logging.md">registrazione normale</a> nella sezione <a href="windows-installer-logging.md">registrazione Windows Installer</a> .
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><strong>/Package</strong></td>
<td><em><Package.msi|ProductCode></em></td>
<td>Installare l'opzione del prodotto. Installa o configura un prodotto.<br/>
<blockquote>
[!Note]<br />
L'opzione della <a href="command-line-options.md">riga di comando</a> Windows Installer equivalente è <strong>/i</strong>.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><strong>/Update</strong></td>
<td><em><Update1.msp>[; Update2. msp]</em></td>
<td>Opzione Installa patch. Installa una o più patch. <br/>
<blockquote>
[!Note]<br />
La riga di comando equivalente Windows Installer presenta <a href="patch.md"><strong>patch</strong></a> = [msipatch. msp] <; PatchGuid2> impostato nella riga di comando.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

 

 
