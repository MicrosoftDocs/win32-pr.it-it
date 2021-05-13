---
description: Rappresenta un oggetto nella shell.
title: Oggetto IShellDispatch (Shldisp.h)
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
ms.openlocfilehash: 02fbead4b2d40a91ec6dab70f536d1ea3241ee84
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840892"
---
# <a name="ishelldispatch-object"></a>Oggetto IShellDispatch

Rappresenta un oggetto nella shell. Vengono forniti metodi per controllare la shell ed eseguire comandi all'interno della shell. Sono disponibili anche metodi per ottenere altri oggetti correlati alla shell.

> [!Note]  
> **IShellDispatch viene** implementato e accessibile tramite [**l'oggetto Shell.**](shell.md)

 

## <a name="members"></a>Membri

**L'oggetto IShellDispatch** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

**L'oggetto IShellDispatch** dispone di questi metodi.



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
<td style="text-align: left;">Crea una finestra di dialogo che consente all'utente di selezionare una cartella e quindi restituisce l'oggetto <a href="folder.md"><strong>Folder della</strong></a> cartella selezionata.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="ishelldispatch-cascadewindows.md"><strong>CascadeWindows</strong></a></td>
<td style="text-align: left;">Sovrapporre tutte le finestre sul desktop. Questo metodo ha lo stesso effetto del clic con il pulsante destro del mouse sulla barra delle applicazioni e della <strong>selezione di Sovrapponi finestre.</strong><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="ishelldispatch-controlpanelitem.md"><strong>ControlPanelItem</strong></a></td>
<td style="text-align: left;">Esegue l'applicazione Pannello di controllo specificata. Se l'applicazione è già aperta, attiverà l'istanza in esecuzione. <br/>
<blockquote>
<p>[!Note]<br />
A data di Windows Vista, la maggior Pannello di controllo applicazioni sono elementi della shell e non possono essere aperte con questa funzione. Per aprire tali Pannello di controllo applicazioni, passare il nome canonico a control.exe. Ad esempio:</p>
<pre class="syntax" data-space="preserve"><code>control.exe /name Microsoft.Personalization</code></pre>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="ishelldispatch-ejectpc.md"><strong>EjectPC</strong></a></td>
<td style="text-align: left;">Espulse il computer dall'alloggiamento di espansione. Questo è lo stesso che si fa clic sul menu <strong>Start</strong> e si <strong>seleziona Espulsa PC</strong>, se il computer supporta questo comando.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="ishelldispatch-explore.md"><strong>Esplorare</strong></a></td>
<td style="text-align: left;">Apre una cartella specificata in una finestra Esplora risorse dati.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="ishelldispatch-filerun.md"><strong>FileRun</strong></a></td>
<td style="text-align: left;">Visualizza la <strong>finestra di</strong> dialogo Esegui per l'utente.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="ishelldispatch-findcomputer.md"><strong>FindComputer</strong></a></td>
<td style="text-align: left;">Visualizza la <strong>finestra di dialogo Risultati ricerca:</strong> Computer. La finestra di dialogo mostra il risultato della ricerca di un computer specificato.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="ishelldispatch-findfiles.md"><strong>FindFiles</strong></a></td>
<td style="text-align: left;">Visualizza la <strong>finestra di dialogo Trova:</strong> Tutti i file. Questo è lo stesso che si fa clic sul menu <strong>Start</strong> e quindi si seleziona <strong>Cerca</strong>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="ishelldispatch-help.md"><strong>Guida</strong></a></td>
<td style="text-align: left;">Visualizza la finestra Guida e supporto tecnico di Windows. Questo metodo ha lo stesso effetto di fare clic sul menu <strong>Start</strong> e selezionare <strong>Guida e supporto tecnico</strong>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="ishelldispatch-minimizeall.md"><strong>MinimizeAll</strong></a></td>
<td style="text-align: left;">Riduce a icona tutte le finestre sul desktop. Questo metodo ha lo stesso effetto di fare clic con il pulsante destro del mouse sulla barra delle applicazioni e scegliere Riduci a icona Tutte le <strong>finestre</strong> nei sistemi meno recenti o facendo clic sull'icona <strong>Mostra desktop</strong> sulla barra delle applicazioni.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="ishelldispatch-namespace.md"><strong>Namespace</strong></a></td>
<td style="text-align: left;">Crea e restituisce un <a href="folder.md"><strong>oggetto Folder</strong></a> per la cartella specificata.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="ishelldispatch-open.md"><strong>Apri</strong></a></td>
<td style="text-align: left;">Apre la cartella specificata.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="ishelldispatch-refreshmenu.md"><strong>RefreshMenu</strong></a></td>
<td style="text-align: left;">Aggiorna il contenuto del menu <strong>Start.</strong> Utilizzato solo con sistemi che precedono Windows XP.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="ishelldispatch-settime.md"><strong>Settime</strong></a></td>
<td style="text-align: left;">Consente di visualizzare <strong>la finestra di dialogo Data e</strong> ora . Questo metodo ha lo stesso effetto di fare clic con il pulsante destro del mouse sull'orologio nell'area di stato della barra delle applicazioni e <strong>scegliere Regola data/ora.</strong><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="ishelldispatch-shutdownwindows.md"><strong>ShutdownWindows</strong></a></td>
<td style="text-align: left;">Consente di visualizzare <strong>la finestra di dialogo Arresta</strong> Windows . Si tratta di un'operazione identica a quando si fa clic sul menu <strong>Start</strong> e si <strong>sceglie Arresta</strong>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="ishelldispatch-suspend.md"><strong>Sospendi</strong></a></td>
<td style="text-align: left;"></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="ishelldispatch-tilehorizontally.md"><strong>TileHorizontally</strong></a></td>
<td style="text-align: left;">Affianca orizzontalmente tutte le finestre sul desktop. Questo metodo ha lo stesso effetto di fare clic con il pulsante destro del mouse sulla barra delle applicazioni e <strong>scegliere Mostra finestre in pila.</strong><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="ishelldispatch-tilevertically.md"><strong>TileVertically</strong></a></td>
<td style="text-align: left;">Affianca verticalmente tutte le finestre sul desktop. Questo metodo ha lo stesso effetto del clic con il pulsante destro del mouse sulla barra delle applicazioni e della selezione <strong>di Mostra finestre affiancate.</strong><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="ishelldispatch-trayproperties.md"><strong>Proprietà della barra delle applicazioni</strong></a></td>
<td style="text-align: left;">Visualizza la finestra <strong>di dialogo Proprietà barra delle</strong> applicazioni e menu Start . Questo metodo ha lo stesso effetto di fare clic con il pulsante destro del mouse sulla barra delle applicazioni e <strong>scegliere Proprietà.</strong><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="ishelldispatch-undominimizeall.md"><strong>UndoMinimizeALL</strong></a></td>
<td style="text-align: left;">Ripristina tutte le finestre del desktop nello stato in cui si trovavano prima dell'ultimo <a href="shell-minimizeall.md"><strong>comando MinimizeAll.</strong></a> Questo metodo ha lo stesso effetto di fare clic con il pulsante destro del mouse sulla barra delle applicazioni e scegliere Annulla Riduci a icona tutte le finestre <strong>(nei</strong> sistemi precedenti) o un secondo clic sull'icona Mostra <strong>desktop</strong> nella barra delle applicazioni.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="ishelldispatch-windows.md"><strong>Windows</strong></a></td>
<td style="text-align: left;">Crea e restituisce un <a href="shellwindows.md"><strong>oggetto ShellWindows.</strong></a> Questo oggetto rappresenta una raccolta di tutte le finestre aperte che appartengono alla shell.<br/></td>
</tr>
</tbody>
</table>



 

### <a name="properties"></a>Proprietà

**L'oggetto IShellDispatch** ha queste proprietà.



| Proprietà                                                     | Tipo di accesso          | Descrizione                                                                      |
|:-------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------------|
| [**Applicazione**](ishelldispatch-application.md)<br/> | Sola lettura<br/> | Contiene un oggetto che rappresenta un'applicazione.<br/>                    |
| [**Padre**](ishelldispatch-parent.md)<br/>           | Sola lettura<br/> | Recupera un oggetto che rappresenta l'elemento padre dell'oggetto corrente.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop di Windows 2000 Professional e Windows XP \[\]<br/>                                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                           |
| Intestazione<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 4.71 o successiva)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Idispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[**Oggetto Shell**](shell.md)
</dt> </dl>

 

 
