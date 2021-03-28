---
description: Rappresenta gli oggetti nella shell. Vengono forniti metodi per controllare la shell e per eseguire comandi all'interno della shell. Sono inoltre disponibili metodi per ottenere altri oggetti correlati alla Shell.
title: 'Oggetto di shell (Shldisp.h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 75fc151e-5b9e-476b-b4e5-b848917357a8
ms.openlocfilehash: 3e891278d98ca2eb51fca11054cba01947e03c09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884389"
---
# <a name="shell-object"></a>Oggetto Shell

Rappresenta gli oggetti nella shell. Vengono forniti metodi per controllare la shell e per eseguire comandi all'interno della shell. Sono inoltre disponibili metodi per ottenere altri oggetti correlati alla Shell.

## <a name="members"></a>Membri

L'oggetto **Shell** dispone di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

Questi metodi sono disponibili nell'oggetto **Shell** .



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Metodo</th>
<th style="text-align: left;">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-addtorecent"><strong>AddToRecent</strong></a></td>
<td style="text-align: left;">Aggiunge un file all'elenco degli ultimi elementi usati (MRU).<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-browseforfolder.md"><strong>BrowseForFolder</strong></a></td>
<td style="text-align: left;">Crea una finestra di dialogo che consente all'utente di selezionare una cartella e quindi restituisce l'oggetto <a href="folder.md"><strong>cartella</strong></a> della cartella selezionata.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-canstartstopservice"><strong>CanStartStopService</strong></a></td>
<td style="text-align: left;">Determina se l'utente corrente può avviare e arrestare il servizio denominato.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-cascadewindows.md"><strong>CascadeWindows</strong></a></td>
<td style="text-align: left;">Si sovrappone a tutte le finestre sul desktop. Questo metodo ha lo stesso effetto di fare clic con il pulsante destro del mouse sulla barra delle applicazioni e selezionare <strong>Cascade Windows</strong>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-controlpanelitem.md"><strong>ControlPanelItem</strong></a></td>
<td style="text-align: left;">Esegue l'applicazione del pannello di controllo (*. cpl) specificata. Se l'applicazione è già aperta, attiverà l'istanza in esecuzione. <br/>
<blockquote>
<p>[!Note]<br />
A partire da Windows Vista, la maggior parte delle applicazioni del pannello di controllo sono elementi della shell e non possono essere aperti con questa funzione. Per aprire le applicazioni del pannello di controllo, passare il nome canonico a control.exe. Ad esempio:</p>
<pre class="syntax" data-space="preserve"><code>control.exe /name Microsoft.Personalization</code></pre>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-ejectpc.md"><strong>EjectPC</strong></a></td>
<td style="text-align: left;">Espelle il computer dalla relativa stazione di ancoraggio. Questa operazione equivale a fare clic sul menu <strong>Start</strong> e selezionare <strong>eject PC (Rimuovi PC</strong>) se il computer supporta questo comando.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-explore.md"><strong>Esplora</strong></a></td>
<td style="text-align: left;">Apre una cartella specificata in una finestra di Esplora risorse.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-explorerpolicy.md"><strong>ExplorerPolicy</strong></a></td>
<td style="text-align: left;">Ottiene il valore per i criteri di Internet Explorer specificati.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-filerun.md"><strong>FileRun</strong></a></td>
<td style="text-align: left;">Consente di visualizzare la finestra di dialogo <strong>Esegui</strong> all'utente. Questo metodo ha lo stesso effetto di quando si fa clic sul menu <strong>Start</strong> e si seleziona <strong>Esegui</strong>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-findcomputer.md"><strong>FindComputer</strong></a></td>
<td style="text-align: left;">Consente di visualizzare la finestra di dialogo <strong>Risultati ricerca: computer</strong> . Nella finestra di dialogo viene visualizzato il risultato della ricerca di un computer specifico.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-findfiles.md"><strong>FindFiles</strong></a></td>
<td style="text-align: left;">Consente di visualizzare la finestra di dialogo <strong>trova: tutti i file</strong> . Questa operazione equivale a fare clic sul menu <strong>Start</strong> e quindi selezionare <strong>Cerca</strong> (o l'equivalente in sistemi precedenti a Windows XP).<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-findprinter"><strong>FindPrinter</strong></a></td>
<td style="text-align: left;">Consente di visualizzare la finestra di dialogo <strong>Trova stampante</strong> .<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-getsetting"><strong>GetSetting</strong></a></td>
<td style="text-align: left;">Recupera un'impostazione della shell globale.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-getsysteminformation"><strong>GetSystemInformation</strong></a></td>
<td style="text-align: left;">Recupera le informazioni di sistema.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-help.md"><strong>Help</strong></a></td>
<td style="text-align: left;">Visualizza la guida e il supporto tecnico di Windows. Questo metodo ha lo stesso effetto di quando si fa clic sul menu <strong>Start</strong> e si seleziona <strong>Guida e supporto</strong>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-isrestricted"><strong>IsRestricted</strong></a></td>
<td style="text-align: left;">Recupera l'impostazione di restrizione di un gruppo dal registro di sistema.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-isservicerunning"><strong>IsServiceRunning</strong></a></td>
<td style="text-align: left;">Restituisce un valore che indica se un particolare servizio è in esecuzione.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-minimizeall.md"><strong>MinimizeAll</strong></a></td>
<td style="text-align: left;">Riduce al minimo tutte le finestre sul desktop. Questo metodo ha lo stesso effetto di fare clic con il pulsante destro del mouse sulla barra delle applicazioni e selezionare <strong>Riduci a icona tutte le finestre</strong> nei sistemi meno recenti oppure fare clic sull'icona <strong>Mostra desktop</strong> nell'area avvio veloce della barra delle applicazioni in Windows 2000 o Windows XP.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-namespace.md"><strong>NameSpace</strong></a></td>
<td style="text-align: left;">Crea e restituisce un oggetto <a href="folder.md"><strong>Folder</strong></a> per la cartella specificata.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-open.md"><strong>Aprire</strong></a></td>
<td style="text-align: left;">Apre la cartella specificata.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-refreshmenu.md"><strong>RefreshMenu</strong></a></td>
<td style="text-align: left;">Aggiorna il contenuto del menu <strong>Start</strong> . Utilizzato solo con i sistemi precedenti a Windows XP.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-searchcommand.md"><strong>SearchCommand</strong></a></td>
<td style="text-align: left;">Consente di visualizzare il riquadro di ricerca delle app.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-servicestart"><strong>ServiceStart</strong></a></td>
<td style="text-align: left;">Avvia un servizio denominato.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-servicestop"><strong>ServiceStop</strong></a></td>
<td style="text-align: left;">Arresta un servizio denominato.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-settime.md"><strong>SetTime</strong></a></td>
<td style="text-align: left;">Consente di visualizzare la finestra di dialogo <strong>Proprietà data e ora</strong> . Questo metodo ha lo stesso effetto di fare clic con il pulsante destro del mouse sull'orologio nell'area stato della barra delle applicazioni e scegliere <strong>regola Data/ora</strong>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-shellexecute"><strong>ShellExecute</strong></a></td>
<td style="text-align: left;">Esegue un'operazione specificata su un file specificato.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-showbrowserbar"><strong>ShowBrowserBar</strong></a></td>
<td style="text-align: left;">Visualizza una barra del browser.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-shutdownwindows.md"><strong>ShutdownWindows</strong></a></td>
<td style="text-align: left;">Consente di visualizzare la finestra di dialogo <strong>arresta Windows</strong> . Equivale a fare clic sul menu <strong>Start</strong> e selezionare <strong>Arresta</strong>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-suspend.md"><strong>Sospendere</strong></a></td>
<td style="text-align: left;"></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-tilehorizontally.md"><strong>TileHorizontally</strong></a></td>
<td style="text-align: left;">Riquadri orizzontalmente tutte le finestre sul desktop. Questo metodo ha lo stesso effetto che si fa clic con il pulsante destro del mouse sulla barra delle applicazioni e si seleziona <strong>finestre affiancate orizzontalmente</strong><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-tilevertically.md"><strong>TileVertically</strong></a></td>
<td style="text-align: left;">Riquadri verticalmente tutte le finestre sul desktop. Questo metodo ha lo stesso effetto che si fa clic con il pulsante destro del mouse sulla barra delle applicazioni e si seleziona <strong>finestre affiancate verticalmente</strong><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-toggledesktop.md"><strong>ToggleDesktop</strong></a></td>
<td style="text-align: left;">Consente di visualizzare o nascondere il desktop.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-trayproperties.md"><strong>TrayProperties</strong></a></td>
<td style="text-align: left;">Consente di visualizzare la <strong>barra delle applicazioni e la finestra di dialogo Proprietà menu Start</strong> . Questo metodo ha lo stesso effetto di fare clic con il pulsante destro del mouse sulla barra delle applicazioni e scegliere <strong>Proprietà</strong>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-undominimizeall.md"><strong>UndoMinimizeALL</strong></a></td>
<td style="text-align: left;">Ripristina tutte le finestre desktop nello stesso stato in cui si trovavano prima dell'ultimo comando <a href="shell-minimizeall.md"><strong>MinimizeAll</strong></a> . Questo metodo ha lo stesso effetto di fare clic con il pulsante destro del mouse sulla barra delle applicazioni e selezionare <strong>Annulla Riduci</strong> a icona tutte le finestre nei sistemi meno recenti o un secondo clic sull'icona <strong>Mostra desktop</strong> nell'area avvio veloce della barra delle applicazioni in Windows 2000 o Windows XP.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-windows.md"><strong>Windows</strong></a></td>
<td style="text-align: left;">Crea e restituisce un oggetto <a href="shellwindows.md"><strong>ShellWindows</strong></a> . Questo oggetto rappresenta una raccolta di tutte le finestre aperte che appartengono alla Shell.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-windowssecurity.md"><strong>WindowsSecurity</strong></a></td>
<td style="text-align: left;">Consente di visualizzare la finestra di dialogo <strong>sicurezza di Windows</strong> .<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-windowswitcher.md"><strong>Aperto WindowSwitcher</strong></a></td>
<td style="text-align: left;">Consente di visualizzare le finestre aperte in uno stack 3D che è possibile scorrere.<br/></td>
</tr>
</tbody>
</table>



 

### <a name="properties"></a>Proprietà

L'oggetto **Shell** dispone di queste proprietà.



| Proprietà                                            | Tipo di accesso          | Descrizione                                                                 |
|:----------------------------------------------------|:---------------------|:----------------------------------------------------------------------------|
| [**Applicazione**](shell-application.md)<br/> | Sola lettura<br/> | Contiene l'oggetto applicazione dell'oggetto.<br/>                        |
| [**Padre**](shell-parent.md)<br/>           | Sola lettura<br/> | Ottiene un oggetto che rappresenta l'elemento padre dell'oggetto corrente.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, \[ solo app desktop Windows XP\]<br/>                                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                           |
| Intestazione<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 4,71 o successiva)</dt> </dl> |



 

 
