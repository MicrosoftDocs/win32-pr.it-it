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
ms.openlocfilehash: 322b912ad7332b0862309b0ecc1510adb3aa1a10
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475297"
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




| Metodo | Descrizione | 
|--------|-------------|
| <a href="ishelldispatch-browseforfolder.md"><strong>BrowseForFolder</strong></a> | Crea una finestra di dialogo che consente all'utente di selezionare una cartella e quindi restituisce l'oggetto <a href="folder.md"><strong>Cartella della</strong></a> cartella selezionata.<br /> | 
| <a href="ishelldispatch-cascadewindows.md"><strong>CascadeWindows</strong></a> | Sovrapporre tutte le finestre sul desktop. Questo metodo ha lo stesso effetto del clic con il pulsante destro del mouse sulla barra delle applicazioni e della <strong>selezione di Sovrapponi finestre.</strong><br /> | 
| <a href="ishelldispatch-controlpanelitem.md"><strong>ControlPanelItem</strong></a> | Esegue l'applicazione Pannello di controllo specificata. Se l'applicazione è già aperta, attiverà l'istanza in esecuzione. <br /><blockquote><p>[!Note]<br />A Windows Vista, la maggior parte Pannello di controllo applicazioni sono elementi della shell e non possono essere aperte con questa funzione. Per aprire tali Pannello di controllo applicazioni, passare il nome canonico a control.exe. Ad esempio:</p><pre class="syntax" data-space="preserve"><code>control.exe /name Microsoft.Personalization</code></pre></blockquote><br /> | 
| <a href="ishelldispatch-ejectpc.md"><strong>EjectPC</strong></a> | Espulsa il computer dalla relativa stazione di ancoraggio. Questa operazione è identica a quando si fa clic sul menu <strong>Start</strong> e si <strong>seleziona Eject PC (Espila PC),</strong>se il computer supporta questo comando.<br /> | 
| <a href="ishelldispatch-explore.md"><strong>Esplorare</strong></a> | Apre una cartella specificata in una finestra Windows Explorer.<br /> | 
| <a href="ishelldispatch-filerun.md"><strong>Esecuzione file</strong></a> | Visualizza la <strong>finestra di</strong> dialogo Esegui all'utente.<br /> | 
| <a href="ishelldispatch-findcomputer.md"><strong>FindComputer</strong></a> | Visualizza la <strong>finestra di dialogo Risultati ricerca:</strong> Computer . Nella finestra di dialogo viene visualizzato il risultato della ricerca di un computer specificato.<br /> | 
| <a href="ishelldispatch-findfiles.md"><strong>FindFiles</strong></a> | Consente di visualizzare <strong>la finestra di dialogo Trova:</strong> Tutti i file . Questa operazione è identica a quando si fa clic sul menu <strong>Start</strong> e quindi si seleziona <strong>Cerca</strong>.<br /> | 
| <a href="ishelldispatch-help.md"><strong>Help</strong></a> | Consente di visualizzare Windows guida e supporto tecnico. Questo metodo ha lo stesso effetto del menu <strong>Start</strong> e della selezione di <strong>Guida e supporto tecnico.</strong><br /> | 
| <a href="ishelldispatch-minimizeall.md"><strong>MinimizeAll</strong></a> | Riduce a icona tutte le finestre sul desktop. Questo metodo ha lo stesso effetto di fare clic con il pulsante destro del mouse sulla barra delle applicazioni e scegliere Riduci a icona <strong>Windows</strong> nei sistemi precedenti o facendo clic sull'icona <strong>Mostra desktop</strong> sulla barra delle applicazioni.<br /> | 
| <a href="ishelldispatch-namespace.md"><strong>Namespace</strong></a> | Crea e restituisce un <a href="folder.md"><strong>oggetto Folder</strong></a> per la cartella specificata.<br /> | 
| <a href="ishelldispatch-open.md"><strong>Aperto</strong></a> | Apre la cartella specificata.<br /> | 
| <a href="ishelldispatch-refreshmenu.md"><strong>RefreshMenu</strong></a> | Aggiorna il contenuto del menu <strong>Start.</strong> Utilizzato solo con sistemi che precedono Windows XP.<br /> | 
| <a href="ishelldispatch-settime.md"><strong>Settime</strong></a> | Consente di visualizzare <strong>la finestra di dialogo Data e</strong> ora . Questo metodo ha lo stesso effetto di fare clic con il pulsante destro del mouse sull'orologio nell'area di stato della barra delle applicazioni e scegliere <strong>Regola data/ora.</strong><br /> | 
| <a href="ishelldispatch-shutdownwindows.md"><strong>ShutdownWindows</strong></a> | Consente di <strong>visualizzare la finestra Windows</strong> Arresta il sistema. Si tratta di un'operazione identica a quando si fa clic sul menu <strong>Start</strong> e si <strong>sceglie Arresta</strong>.<br /> | 
| <a href="ishelldispatch-suspend.md"><strong>Sospendi</strong></a> | Td | 
| <a href="ishelldispatch-tilehorizontally.md"><strong>TileHorizontally</strong></a> | Affianca orizzontalmente tutte le finestre sul desktop. Questo metodo ha lo stesso effetto del clic con il pulsante destro del mouse sulla barra delle applicazioni e della <strong>selezione di Mostra finestre in pila.</strong><br /> | 
| <a href="ishelldispatch-tilevertically.md"><strong>TileVertically</strong></a> | Affianca verticalmente tutte le finestre sul desktop. Questo metodo ha lo stesso effetto del clic con il pulsante destro del mouse sulla barra delle applicazioni e della selezione <strong>di Mostra finestre affiancate.</strong><br /> | 
| <a href="ishelldispatch-trayproperties.md"><strong>Proprietà della barra delle applicazioni</strong></a> | Visualizza la finestra <strong>di dialogo Proprietà barra delle</strong> applicazioni e menu Start . Questo metodo ha lo stesso effetto di fare clic con il pulsante destro del mouse sulla barra delle applicazioni e <strong>scegliere Proprietà.</strong><br /> | 
| <a href="ishelldispatch-undominimizeall.md"><strong>UndoMinimizeALL</strong></a> | Ripristina tutte le finestre desktop allo stato precedente all'ultimo <a href="shell-minimizeall.md"><strong>comando MinimizeAll.</strong></a> Questo metodo ha lo stesso effetto di fare clic con il pulsante destro del mouse sulla barra delle applicazioni e scegliere Annulla Riduci a icona tutto <strong>Windows</strong> (nei sistemi precedenti) o un secondo clic sull'icona <strong>Mostra desktop</strong> nella barra delle applicazioni.<br /> | 
| <a href="ishelldispatch-windows.md"><strong>Windows</strong></a> | Crea e restituisce un <a href="shellwindows.md"><strong>oggetto ShellWindows.</strong></a> Questo oggetto rappresenta una raccolta di tutte le finestre aperte che appartengono alla shell.<br /> | 




 

### <a name="properties"></a>Proprietà

**L'oggetto IShellDispatch** ha queste proprietà.



| Proprietà                                                     | Tipo di accesso          | Descrizione                                                                      |
|:-------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------------|
| [**Applicazione**](ishelldispatch-application.md)<br/> | Sola lettura<br/> | Contiene un oggetto che rappresenta un'applicazione.<br/>                    |
| [**Padre**](ishelldispatch-parent.md)<br/>           | Sola lettura<br/> | Recupera un oggetto che rappresenta l'elemento padre dell'oggetto corrente.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, Windows solo app desktop XP \[\]<br/>                                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                           |
| Intestazione<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 4.71 o successiva)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Idispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[**Oggetto shell**](shell.md)
</dt> </dl>

 

 
