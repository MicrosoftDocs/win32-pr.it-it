---
description: Rappresenta gli oggetti nella shell. Vengono forniti metodi per controllare la shell ed eseguire comandi all'interno della shell. Sono disponibili anche metodi per ottenere altri oggetti correlati alla shell.
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
ms.openlocfilehash: fe2fbaa1bad61ac9c22d36919e49cf493a26a778a8e97d69d1b200c0c62205e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117857720"
---
# <a name="shell-object"></a>Oggetto shell

Rappresenta gli oggetti nella shell. Vengono forniti metodi per controllare la shell ed eseguire comandi all'interno della shell. Sono disponibili anche metodi per ottenere altri oggetti correlati alla shell.

## <a name="members"></a>Membri

**L'oggetto Shell** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

**L'oggetto Shell** dispone di questi metodi.



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
<td style="text-align: left;">Aggiunge un file all'elenco degli elementi usati più di recente.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-browseforfolder.md"><strong>BrowseForFolder</strong></a></td>
<td style="text-align: left;">Crea una finestra di dialogo che consente all'utente di selezionare una cartella e quindi restituisce l'oggetto <a href="folder.md"><strong>Cartella della</strong></a> cartella selezionata.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-canstartstopservice"><strong>CanStartStopService</strong></a></td>
<td style="text-align: left;">Determina se l'utente corrente può avviare e arrestare il servizio denominato.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-cascadewindows.md"><strong>CascadeWindows</strong></a></td>
<td style="text-align: left;">Sovrapporre tutte le finestre sul desktop. Questo metodo ha lo stesso effetto di fare clic con il pulsante destro del mouse sulla barra delle applicazioni e <strong>scegliere Propaga</strong>Windows .<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-controlpanelitem.md"><strong>ControlPanelItem</strong></a></td>
<td style="text-align: left;">Esegue l'Pannello di controllo (*.cpl) specificata. Se l'applicazione è già aperta, attiverà l'istanza in esecuzione. <br/>
<blockquote>
<p>[!Note]<br />
A Windows Vista, la maggior parte Pannello di controllo applicazioni sono elementi della shell e non possono essere aperti con questa funzione. Per aprire tali Pannello di controllo applicazioni, passare il nome canonico a control.exe. Esempio:</p>
<pre class="syntax" data-space="preserve"><code>control.exe /name Microsoft.Personalization</code></pre>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-ejectpc.md"><strong>EjectPC</strong></a></td>
<td style="text-align: left;">Espulsa il computer dalla relativa stazione di ancoraggio. Questa operazione è identica a quando si fa clic sul menu <strong>Start</strong> e si <strong>seleziona Eject PC (Espila PC),</strong>se il computer supporta questo comando.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-explore.md"><strong>Esplorare</strong></a></td>
<td style="text-align: left;">Apre una cartella specificata in una finestra Windows Explorer.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-explorerpolicy.md"><strong>ExplorerPolicy</strong></a></td>
<td style="text-align: left;">Ottiene il valore per un criterio di Internet Explorer specificato.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-filerun.md"><strong>Esecuzione file</strong></a></td>
<td style="text-align: left;">Visualizza la <strong>finestra di</strong> dialogo Esegui all'utente. Questo metodo ha lo stesso effetto di fare clic sul menu <strong>Start</strong> e scegliere <strong>Esegui.</strong><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-findcomputer.md"><strong>FindComputer</strong></a></td>
<td style="text-align: left;">Visualizza la <strong>finestra di dialogo Risultati ricerca:</strong> Computer . Nella finestra di dialogo viene visualizzato il risultato della ricerca di un computer specificato.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-findfiles.md"><strong>FindFiles</strong></a></td>
<td style="text-align: left;">Consente di visualizzare <strong>la finestra di dialogo Trova:</strong> Tutti i file . Equivale a fare clic sul menu <strong>Start</strong> e quindi selezionare Cerca <strong>(o</strong> l'equivalente in sistemi precedenti a Windows XP.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-findprinter"><strong>FindPrinter</strong></a></td>
<td style="text-align: left;">Consente di visualizzare <strong>la finestra di dialogo</strong> Trova stampante .<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-getsetting"><strong>GetSetting</strong></a></td>
<td style="text-align: left;">Recupera un'impostazione globale della shell.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-getsysteminformation"><strong>GetSystemInformation</strong></a></td>
<td style="text-align: left;">Recupera le informazioni di sistema.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-help.md"><strong>Help</strong></a></td>
<td style="text-align: left;">Visualizza il Windows Guida e supporto tecnico. Questo metodo ha lo stesso effetto del menu <strong>Start</strong> e della selezione di <strong>Guida e supporto tecnico.</strong><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-isrestricted"><strong>IsRestricted</strong></a></td>
<td style="text-align: left;">Recupera l'impostazione di restrizione di un gruppo dal Registro di sistema.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-isservicerunning"><strong>Esecuzione di IsServiceRunning</strong></a></td>
<td style="text-align: left;">Restituisce un valore che indica se un determinato servizio è in esecuzione.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-minimizeall.md"><strong>MinimizeAll</strong></a></td>
<td style="text-align: left;">Riduce a icona tutte le finestre sul desktop. Questo metodo ha lo stesso effetto di fare clic con il pulsante destro <strong></strong> del mouse sulla barra delle applicazioni e scegliere Riduci a icona tutto <strong>Windows</strong> nei sistemi meno recenti o facendo clic sull'icona Mostra desktop nell'area Avvio veloce della barra delle applicazioni in Windows 2000 o Windows XP.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-namespace.md"><strong>Namespace</strong></a></td>
<td style="text-align: left;">Crea e restituisce un <a href="folder.md"><strong>oggetto Folder</strong></a> per la cartella specificata.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-open.md"><strong>Aperto</strong></a></td>
<td style="text-align: left;">Apre la cartella specificata.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-refreshmenu.md"><strong>RefreshMenu</strong></a></td>
<td style="text-align: left;">Aggiorna il contenuto del menu <strong>Start.</strong> Utilizzato solo con sistemi che precedono Windows XP.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-searchcommand.md"><strong>SearchCommand</strong></a></td>
<td style="text-align: left;">Visualizza il riquadro Ricerca app.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-servicestart"><strong>Avvio del servizio</strong></a></td>
<td style="text-align: left;">Avvia un servizio denominato.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-servicestop"><strong>ServiceStop</strong></a></td>
<td style="text-align: left;">Arresta un servizio denominato.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-settime.md"><strong>Settime</strong></a></td>
<td style="text-align: left;">Consente di visualizzare <strong>la finestra di dialogo Proprietà data</strong> e ora . Questo metodo ha lo stesso effetto di fare clic con il pulsante destro del mouse sull'orologio nell'area di stato della barra delle applicazioni e <strong>scegliere Regola data/ora.</strong><br/></td>
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
<td style="text-align: left;">Consente di <strong>visualizzare la finestra Windows</strong> arresta il sistema. Si tratta di un'operazione identica a quando si fa clic sul menu <strong>Start</strong> e si <strong>sceglie Arresta</strong>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-suspend.md"><strong>Sospendi</strong></a></td>
<td style="text-align: left;"></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-tilehorizontally.md"><strong>TileHorizontally</strong></a></td>
<td style="text-align: left;">Affianca orizzontalmente tutte le finestre sul desktop. Questo metodo ha lo stesso effetto di fare clic con il pulsante destro del mouse sulla barra delle applicazioni e scegliere <strong>Windows orizzontalmente.</strong><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-tilevertically.md"><strong>TileVertically</strong></a></td>
<td style="text-align: left;">Affianca verticalmente tutte le finestre sul desktop. Questo metodo ha lo stesso effetto di fare clic con il pulsante destro del mouse sulla barra delle applicazioni e <strong>scegliere Windows verticalmente.</strong><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-toggledesktop.md"><strong>ToggleDesktop</strong></a></td>
<td style="text-align: left;">Visualizza o nasconde il desktop.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-trayproperties.md"><strong>Proprietà della barra delle applicazioni</strong></a></td>
<td style="text-align: left;">Visualizza la finestra <strong>di dialogo Proprietà barra delle</strong> applicazioni e menu Start . Questo metodo ha lo stesso effetto di fare clic con il pulsante destro del mouse sulla barra delle applicazioni e <strong>scegliere Proprietà.</strong><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-undominimizeall.md"><strong>UndoMinimizeALL</strong></a></td>
<td style="text-align: left;">Ripristina tutte le finestre desktop allo stesso stato in cui si trovavano prima dell'ultimo <a href="shell-minimizeall.md"><strong>comando MinimizeAll.</strong></a> Questo metodo ha lo stesso effetto di fare clic con il pulsante destro del mouse <strong></strong> sulla barra delle applicazioni e scegliere Annulla Riduci a icona tutto <strong>Windows</strong> nei sistemi precedenti o un secondo clic sull'icona Mostra desktop nell'area Avvio veloce della barra delle applicazioni in Windows 2000 o Windows XP.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-windows.md"><strong>Windows</strong></a></td>
<td style="text-align: left;">Crea e restituisce un <a href="shellwindows.md"><strong>oggetto ShellWindows.</strong></a> Questo oggetto rappresenta una raccolta di tutte le finestre aperte che appartengono alla shell.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-windowssecurity.md"><strong>WindowsSicurezza</strong></a></td>
<td style="text-align: left;">Consente di visualizzare <strong>Sicurezza di Windows</strong> finestra di dialogo.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-windowswitcher.md"><strong>WindowSwitcher</strong></a></td>
<td style="text-align: left;">Visualizza le finestre aperte in uno stack 3D che è possibile scorrere.<br/></td>
</tr>
</tbody>
</table>



 

### <a name="properties"></a>Proprietà

**L'oggetto Shell** ha queste proprietà.



| Proprietà                                            | Tipo di accesso          | Descrizione                                                                 |
|:----------------------------------------------------|:---------------------|:----------------------------------------------------------------------------|
| [**Applicazione**](shell-application.md)<br/> | Sola lettura<br/> | Contiene l'oggetto Application dell'oggetto.<br/>                        |
| [**Padre**](shell-parent.md)<br/>           | Sola lettura<br/> | Ottiene un oggetto che rappresenta l'elemento padre dell'oggetto corrente.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, Windows solo app \[ desktop XP\]<br/>                                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                           |
| Intestazione<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 4.71 o successiva)</dt> </dl> |



 

 
