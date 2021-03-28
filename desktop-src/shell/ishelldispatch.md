---
description: Rappresenta un oggetto nella shell.
title: Oggetto IShellDispatch (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 9B429C03-7F80-45db-B8CD-58D19FAD2E61
ms.openlocfilehash: 20c6cc9f0b3a2e2fde8f56311564d63bc1cc9c0e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978074"
---
# <a name="ishelldispatch-object"></a>Oggetto IShellDispatch

Rappresenta un oggetto nella shell. Vengono forniti metodi per controllare la shell e per eseguire comandi all'interno della shell. Sono inoltre disponibili metodi per ottenere altri oggetti correlati alla Shell.

> [!Note]  
> **IShellDispatch** viene implementato e accessibile tramite l'oggetto [**Shell**](shell.md) .

 

## <a name="members"></a>Membri

L'oggetto **IShellDispatch** dispone di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'oggetto **IShellDispatch** dispone di questi metodi.



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
<td style="text-align: left;"><a href="ishelldispatch-browseforfolder.md"><strong>BrowseForFolder</strong></a></td>
<td style="text-align: left;">Crea una finestra di dialogo che consente all'utente di selezionare una cartella e quindi restituisce l'oggetto <a href="folder.md"><strong>cartella</strong></a> della cartella selezionata.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="ishelldispatch-cascadewindows.md"><strong>CascadeWindows</strong></a></td>
<td style="text-align: left;">Si sovrappone a tutte le finestre sul desktop. Questo metodo ha lo stesso effetto di fare clic con il pulsante destro del mouse sulla barra delle applicazioni e selezionare <strong>Cascade Windows</strong>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="ishelldispatch-controlpanelitem.md"><strong>ControlPanelItem</strong></a></td>
<td style="text-align: left;">Esegue l'applicazione del pannello di controllo specificata. Se l'applicazione è già aperta, attiverà l'istanza in esecuzione. <br/>
<blockquote>
<p>[!Note]<br />
A partire da Windows Vista, la maggior parte delle applicazioni del pannello di controllo sono elementi della shell e non possono essere aperti con questa funzione. Per aprire le applicazioni del pannello di controllo, passare il nome canonico a control.exe. Ad esempio:</p>
<pre class="syntax" data-space="preserve"><code>control.exe /name Microsoft.Personalization</code></pre>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="ishelldispatch-ejectpc.md"><strong>EjectPC</strong></a></td>
<td style="text-align: left;">Espelle il computer dalla relativa stazione di ancoraggio. Questa operazione equivale a fare clic sul menu <strong>Start</strong> e selezionare <strong>eject PC (Rimuovi PC</strong>) se il computer supporta questo comando.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="ishelldispatch-explore.md"><strong>Esplora</strong></a></td>
<td style="text-align: left;">Apre una cartella specificata in una finestra di Esplora risorse.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="ishelldispatch-filerun.md"><strong>FileRun</strong></a></td>
<td style="text-align: left;">Consente di visualizzare la finestra di dialogo <strong>Esegui</strong> all'utente.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="ishelldispatch-findcomputer.md"><strong>FindComputer</strong></a></td>
<td style="text-align: left;">Consente di visualizzare la finestra di dialogo <strong>Risultati ricerca: computer</strong> . Nella finestra di dialogo viene visualizzato il risultato della ricerca di un computer specifico.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="ishelldispatch-findfiles.md"><strong>FindFiles</strong></a></td>
<td style="text-align: left;">Consente di visualizzare la finestra di dialogo <strong>trova: tutti i file</strong> . Questo equivale a fare clic sul menu <strong>Start</strong> e quindi scegliere <strong>Cerca</strong>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="ishelldispatch-help.md"><strong>Help</strong></a></td>
<td style="text-align: left;">Visualizza la finestra Guida e supporto tecnico di Windows. Questo metodo ha lo stesso effetto di quando si fa clic sul menu <strong>Start</strong> e si seleziona <strong>Guida e supporto</strong>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="ishelldispatch-minimizeall.md"><strong>MinimizeAll</strong></a></td>
<td style="text-align: left;">Riduce al minimo tutte le finestre sul desktop. Questo metodo ha lo stesso effetto di fare clic con il pulsante destro del mouse sulla barra delle applicazioni e selezionare <strong>Riduci a icona tutte le finestre</strong> nei sistemi meno recenti o facendo clic sull'icona <strong>Mostra desktop</strong> sulla barra delle applicazioni.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="ishelldispatch-namespace.md"><strong>NameSpace</strong></a></td>
<td style="text-align: left;">Crea e restituisce un oggetto <a href="folder.md"><strong>Folder</strong></a> per la cartella specificata.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="ishelldispatch-open.md"><strong>Aprire</strong></a></td>
<td style="text-align: left;">Apre la cartella specificata.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="ishelldispatch-refreshmenu.md"><strong>RefreshMenu</strong></a></td>
<td style="text-align: left;">Aggiorna il contenuto del menu <strong>Start</strong> . Utilizzato solo con i sistemi precedenti a Windows XP.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="ishelldispatch-settime.md"><strong>SetTime</strong></a></td>
<td style="text-align: left;">Consente di visualizzare la finestra di dialogo <strong>data e ora</strong> . Questo metodo ha lo stesso effetto di fare clic con il pulsante destro del mouse sull'orologio nell'area stato della barra delle applicazioni e scegliere <strong>regola Data/ora</strong>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="ishelldispatch-shutdownwindows.md"><strong>ShutdownWindows</strong></a></td>
<td style="text-align: left;">Consente di visualizzare la finestra di dialogo <strong>arresta Windows</strong> . Equivale a fare clic sul menu <strong>Start</strong> e selezionare <strong>Arresta</strong>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="ishelldispatch-suspend.md"><strong>Sospendere</strong></a></td>
<td style="text-align: left;"></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="ishelldispatch-tilehorizontally.md"><strong>TileHorizontally</strong></a></td>
<td style="text-align: left;">Riquadri orizzontalmente tutte le finestre sul desktop. Questo metodo ha lo stesso effetto di fare clic con il pulsante destro del mouse sulla barra delle applicazioni e selezionare <strong>Mostra Windows in pila</strong>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="ishelldispatch-tilevertically.md"><strong>TileVertically</strong></a></td>
<td style="text-align: left;">Riquadri verticalmente tutte le finestre sul desktop. Questo metodo ha lo stesso effetto che si fa clic con il pulsante destro del mouse sulla barra delle applicazioni e si seleziona <strong>Mostra finestre affiancate</strong>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="ishelldispatch-trayproperties.md"><strong>TrayProperties</strong></a></td>
<td style="text-align: left;">Consente di visualizzare la <strong>barra delle applicazioni e la finestra di dialogo Proprietà menu Start</strong> . Questo metodo ha lo stesso effetto di fare clic con il pulsante destro del mouse sulla barra delle applicazioni e scegliere <strong>Proprietà</strong>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="ishelldispatch-undominimizeall.md"><strong>UndoMinimizeALL</strong></a></td>
<td style="text-align: left;">Ripristina tutte le finestre desktop nello stato in cui si trovavano prima dell'ultimo comando <a href="shell-minimizeall.md"><strong>MinimizeAll</strong></a> . Questo metodo ha lo stesso effetto di fare clic con il pulsante destro del mouse sulla barra delle applicazioni e selezionare <strong>Annulla Riduci a icona tutte le finestre</strong> (nei sistemi meno recenti) o un secondo clic sull'icona <strong>Mostra desktop</strong> sulla barra delle applicazioni.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="ishelldispatch-windows.md"><strong>Windows</strong></a></td>
<td style="text-align: left;">Crea e restituisce un oggetto <a href="shellwindows.md"><strong>ShellWindows</strong></a> . Questo oggetto rappresenta una raccolta di tutte le finestre aperte che appartengono alla Shell.<br/></td>
</tr>
</tbody>
</table>



 

### <a name="properties"></a>Proprietà

L'oggetto **IShellDispatch** dispone di queste proprietà.



| Proprietà                                                     | Tipo di accesso          | Descrizione                                                                      |
|:-------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------------|
| [**Applicazione**](ishelldispatch-application.md)<br/> | Sola lettura<br/> | Contiene un oggetto che rappresenta un'applicazione.<br/>                    |
| [**Padre**](ishelldispatch-parent.md)<br/>           | Sola lettura<br/> | Recupera un oggetto che rappresenta l'elemento padre dell'oggetto corrente.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, \[ solo app desktop Windows XP\]<br/>                                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                           |
| Intestazione<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 4,71 o successiva)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[**Oggetto Shell**](shell.md)
</dt> </dl>

 

 
