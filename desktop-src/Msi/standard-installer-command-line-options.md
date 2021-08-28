---
description: il programma eseguibile che interpreta i pacchetti e installa i prodotti è Msiexec.exe. Nota Msiexec imposta anche un livello di errore al ritorno che corrisponde ai codici di errore di sistema. La tabella seguente identifica le opzioni della riga di comando standard per questo programma. Per le opzioni della riga di comando non viene fatto distinzione tra maiuscole e minuscole. Windows Programma di installazione 2.0: le opzioni della riga di comando identificate in questo argomento sono disponibili a partire da Windows Installer 3.0. Le Windows di installazione Command-Line sono disponibili con Windows Installer&\# 160;3.0 e versioni precedenti.
ms.assetid: b1707c88-1cca-45ab-bb23-6002bfd5204e title: Standard Installer Command-Line Options ms.topic: article ms.date: 05/31/2018
---

# <a name="standard-installer-command-line-options"></a>Opzioni di installazione Command-Line standard

Il programma eseguibile che interpreta i pacchetti e installa i prodotti è Msiexec.exe.

> [!Note]  
> Msiexec imposta anche un livello di errore al ritorno che corrisponde ai [codici di errore di sistema](../debug/system-error-codes.md).

 

La tabella seguente identifica le opzioni della riga di comando standard per questo programma. Per le opzioni della riga di comando non viene fatto distinzione tra maiuscole e minuscole.

**Windows Installer 2.0:** Le opzioni della riga di comando identificate in questo argomento sono disponibili a partire da Windows Installer 3.0. Le Windows della [riga di comando](command-line-options.md) del programma di installazione di Windows 3.0 e versioni precedenti.



<table>
<colgroup>
<col  />
<col  />
<col  />
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
<td><strong>/help</strong></td>
<td> </td>
<td>Guida e opzione di riferimento rapido. Visualizza l'utilizzo corretto del comando di installazione, incluso un elenco di tutte le opzioni e il comportamento. La descrizione dell'utilizzo può essere visualizzata nell'interfaccia utente. L'uso non corretto di un'opzione richiama questa opzione della Guida.<br/> Esempio: <strong>msiexec /help</strong><br/>
<blockquote>
[!Note]<br />
L'equivalente Windows <a href="command-line-options.md">della riga di comando del programma di installazione</a> è <strong>/?</strong>.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><strong>/quiet</strong></td>
<td> </td>
<td>Opzione di visualizzazione non interattiva. Il programma di installazione esegue un'installazione senza visualizzare un'interfaccia utente. All'utente non vengono visualizzati prompt, messaggi o finestre di dialogo. L'utente non può annullare l'installazione. Usare le opzioni della riga di comando standard <strong>/norestart</strong> o <strong>/forcerestart</strong> per controllare i riavvii. Se non viene specificata alcuna opzione di riavvio, il programma di installazione riavvia il computer ogni volta che è necessario senza visualizzare alcuna richiesta o avviso all'utente.<br/> Esempi: <br/> <strong>msiexec /package Application.msi /quiet</strong><br/> <strong>Msiexec /uninstall Application.msi /quiet</strong><br/> <strong>Msiexec /update msipatch.msp /quiet</strong><br/> <strong>Msiexec /uninstall msipatch.msp /package Application.msi /quiet</strong><br/>
<blockquote>
[!Note]<br />
L'opzione Windows <a href="command-line-options.md">della riga di comando del</a> programma di installazione equivalente è <strong>/qn</strong>.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><strong>/passive</strong></td>
<td> </td>
<td>Opzione di visualizzazione passiva. Il programma di installazione visualizza all'utente un indicatore di stato che indica che è in corso un'installazione, ma non vengono visualizzati prompt o messaggi di errore. L'utente non può annullare l'installazione. Usare le opzioni della riga di comando standard <strong>/norestart</strong> o <strong>/forcerestart</strong> per controllare i riavvii. Se non viene specificata alcuna opzione di riavvio, il programma di installazione riavvia il computer ogni volta che è necessario senza visualizzare alcuna richiesta o avviso all'utente. <br/> Esempio: <strong>msiexec /package Application.msi /passive</strong> <br/>
<blockquote>
[!Note]<br />
L'Windows riga <a href="command-line-options.md">di</a> comando del programma di installazione equivalente è <strong>/qb!-</strong> con <a href="rebootprompt.md"><strong>REBOOTPROMPT</strong></a>=S impostato nella riga di comando.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><strong>/norestart</strong></td>
<td> </td>
<td>Opzione Non riavviare mai. Il programma di installazione non riavvia mai il computer dopo l'installazione.<br/> Esempio: msiexec /package Application.msi <strong>/norestart</strong><br/>
<blockquote>
[!Note]<br />
L'equivalente Windows riga di comando del programma di installazione ha <a href="reboot.md"><strong>REBOOT</strong></a>=ReallySuppress impostato nella riga di comando.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><strong>/forcerestart</strong></td>
<td> </td>
<td>Opzione di riavvio sempre. Il programma di installazione riavvia sempre il computer dopo ogni installazione.<br/> Esempio: msiexec /package Application.msi <strong>/forcerestart</strong><br/>
<blockquote>
[!Note]<br />
L'equivalente Windows riga di comando del programma di installazione <a href="reboot.md"><strong>ha REBOOT</strong></a>=Force impostato nella riga di comando.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><strong>/promptrestart</strong></td>
<td> </td>
<td>Chiedi conferma prima del riavvio dell'opzione. Visualizza un messaggio che indica che è necessario un riavvio per completare l'installazione e chiede all'utente se riavviare il sistema ora. Questa opzione non può essere usata insieme <strong>all'opzione /quiet.</strong><br/>
<blockquote>
[!Note]<br />
La riga di Windows installer equivalente ha <a href="rebootprompt.md"><strong>REBOOTPROMPT</strong></a>  =  &quot; &quot; impostato nella riga di comando.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><strong>/uninstall</strong></td>
<td><em>&lt;Package.msi| Codice Prodotto></em></td>
<td>Opzione di disinstallazione del prodotto. Disinstalla un prodotto.<br/>
<blockquote>
[!Note]<br />
L'opzione Windows <a href="command-line-options.md">riga di comando del</a> programma di installazione equivalente è <strong>/x</strong>.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><strong>/uninstall</strong></td>
<td><em>/package &lt;Package.msi | ProductCode> /uninstall <Update1.msp | PatchGUID1> [; Aggiornamento 2.msp | PatchGUID2]</em></td>
<td>Opzione di disinstallazione dell'aggiornamento. Disinstalla una patch di aggiornamento.<br/>
<blockquote>
[!Note]<br />
L'Windows della riga <a href="command-line-options.md">di</a> comando del programma di installazione equivalente è <strong>/I</strong> con <a href="msipatchremove.md"><strong>MSIPATCHREMOVE</strong></a>=Update1.msp | PatchGUID1[; Aggiornamento 2.msp | PatchGUID2] impostato nella riga di comando.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><strong>/log</strong></td>
<td><em><logfile></em></td>
<td>Opzione di log. Scrive le informazioni di registrazione in un file di log nel percorso esistente specificato. Il percorso del file di log deve esistere già. Il programma di installazione non crea la struttura di directory per il file di log.<br/> Nel log vengono immesse le informazioni seguenti:<br/>
<ul>
<li>Messaggi di stato</li>
<li>Avvisi non irreversibile</li>
<li>Tutti i messaggi di errore</li>
<li>Avvio delle azioni</li>
<li>Record specifici dell'azione</li>
<li>Richieste utente</li>
<li>Parametri iniziali dell'interfaccia utente</li>
<li>Informazioni di uscita in memoria insufficiente o irreversibile</li>
<li>Messaggi di spazio su disco insufficiente</li>
<li>Proprietà del terminale</li>
</ul>
<blockquote>
[!Note]<br />
L'opzione Windows <a href="command-line-options.md">riga di comando del</a> programma di installazione equivalente è <strong>/L*.</strong>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
Per altre informazioni su tutti i metodi disponibili per l'impostazione della modalità di registrazione, vedere <a href="normal-logging.md">Registrazione</a> normale nella Windows registrazione del programma <a href="windows-installer-logging.md">di</a> installazione.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><strong>/package</strong></td>
<td><em>&lt;Package.msi| Codice Prodotto></em></td>
<td>Installare l'opzione del prodotto. Installa o configura un prodotto.<br/>
<blockquote>
[!Note]<br />
L'opzione Windows <a href="command-line-options.md">riga di comando del</a> programma di installazione equivalente è <strong>/I</strong>.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><strong>/update</strong></td>
<td><em><Update1.msp>[; Update2.msp]</em></td>
<td>Opzione Installa patch. Installa una o più patch. <br/>
<blockquote>
[!Note]<br />
La riga di Windows installer equivalente <a href="patch.md"><strong>ha PATCH</strong></a> = [msipatch.msp]<; PatchGuid2> impostata nella riga di comando.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

 

 
