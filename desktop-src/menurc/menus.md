---
title: Menu (menu e altre risorse)
description: In questa sezione vengono illustrati i menu.
ms.assetid: vs|winui|~\winui\windowsuserinterface\resources\menus.htm
keywords:
- risorse, menu
- menu, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c376aa1d2f55fa482ca7a2f98f57ae15236bf26b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104400056"
---
# <a name="menus-menus-and-other-resources"></a>Menu (menu e altre risorse)

Questa sezione descrive i menu e spiega come usarli.

### <a name="in-this-section"></a>Contenuto della sezione



| Nome                                 | Descrizione                                                  |
|--------------------------------------|--------------------------------------------------------------|
| [Informazioni sui menu](about-menus.md)       | Vengono illustrati i menu.<br/>                                  |
| [Uso di menu](using-menus.md)       | Fornisce esempi di codice di attività correlate ai menu.<br/> |
| [Riferimento a menu](menu-reference.md) | Contiene il riferimento all'API.<br/>                       |



 

### <a name="menu-functions"></a>Funzioni di menu



| Nome                                                             | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua)                                 | Aggiunge un nuovo elemento alla fine della barra dei menu, del menu a discesa, del sottomenu o del menu di scelta rapida specificato. È possibile utilizzare questa funzione per specificare il contenuto, l'aspetto e il comportamento della voce di menu. <br/>                                                                                                                                                                                                  |
| [**CheckMenuItem**](/windows/desktop/api/Winuser/nf-winuser-checkmenuitem)                           | Imposta lo stato dell'attributo di segno di spunta della voce di menu specificato su selezionato o deselezionato.<br/>                                                                                                                                                                                                                                                                                                      |
| [**CheckMenuRadioItem**](/windows/desktop/api/Winuser/nf-winuser-checkmenuradioitem)                 | Controlla una voce di menu specificata e la imposta come voce di radio. Allo stesso tempo, la funzione Cancella tutte le altre voci di menu nel gruppo associato e cancella il flag del tipo di elemento radio per tali elementi.<br/>                                                                                                                                                                                                    |
| [**CreateMenu**](/windows/desktop/api/Winuser/nf-winuser-createmenu)                                 | Crea un menu. Il menu è inizialmente vuoto, ma può essere riempito con le voci di menu usando le funzioni [**InsertMenuItem**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema), [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua)e [**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua) . <br/>                                                                                                                                                                        |
| [**CreatePopupMenu**](/windows/desktop/api/Winuser/nf-winuser-createpopupmenu)                       | Consente di creare un menu a discesa, un sottomenu o un menu di scelta rapida. Il menu è inizialmente vuoto. È possibile inserire o accodare voci di menu tramite la funzione [**InsertMenuItem**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema) . È anche possibile usare la funzione [**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua) per inserire voci di menu e la funzione [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua) per aggiungere voci di menu.<br/>                                                  |
| [**DeleteMenu**](/windows/desktop/api/Winuser/nf-winuser-deletemenu)                                 | Elimina un elemento dal menu specificato. Se la voce di menu apre un menu o un sottomenu, questa funzione Elimina l'handle dal menu o dal sottomenu e libera la memoria usata dal menu o dal sottomenu. <br/>                                                                                                                                                                                                     |
| [**DestroyMenu**](/windows/desktop/api/Winuser/nf-winuser-destroymenu)                               | Elimina il menu specificato e libera la memoria occupata dal menu. <br/>                                                                                                                                                                                                                                                                                                                          |
| [**DrawMenuBar**](/windows/desktop/api/Winuser/nf-winuser-drawmenubar)                               | Riestrae la barra dei menu della finestra specificata. Se la barra dei menu viene modificata dopo che il sistema ha creato la finestra, questa funzione deve essere chiamata per creare la barra dei menu modificata. <br/>                                                                                                                                                                                                                         |
| [**EnableMenuItem**](/windows/desktop/api/Winuser/nf-winuser-enablemenuitem)                         | Abilita, Disabilita o Disabilita la voce di menu specificata. <br/>                                                                                                                                                                                                                                                                                                                                              |
| [**EndMenu**](/windows/desktop/api/Winuser/nf-winuser-endmenu)                                       | Termina il menu attivo del thread chiamante.<br/>                                                                                                                                                                                                                                                                                                                                                             |
| [**GetMenu**](/windows/desktop/api/Winuser/nf-winuser-getmenu)                                       | Recupera un handle per il menu assegnato alla finestra specificata. <br/>                                                                                                                                                                                                                                                                                                                                  |
| [**GetMenuBarInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenubarinfo)                         | Recupera le informazioni sulla barra dei menu specificata.<br/>                                                                                                                                                                                                                                                                                                                                                |
| [**GetMenuCheckMarkDimensions**](/windows/desktop/api/Winuser/nf-winuser-getmenucheckmarkdimensions) | Recupera le dimensioni dell'oggetto bitmap di segno di spunta predefinito. Il sistema Visualizza questa bitmap accanto alle voci di menu selezionate. Prima di chiamare la funzione [**SetMenuItemBitmaps**](/windows/desktop/api/Winuser/nf-winuser-setmenuitembitmaps) per sostituire la bitmap del segno di spunta predefinita per una voce di menu, un'applicazione deve determinare la dimensione bitmap corretta chiamando [**GetMenuCheckMarkDimensions**](/windows/desktop/api/Winuser/nf-winuser-getmenucheckmarkdimensions). <br/> |
| [**GetMenuDefaultItem**](/windows/desktop/api/Winuser/nf-winuser-getmenudefaultitem)                 | Determina la voce di menu predefinita nel menu specificato.<br/>                                                                                                                                                                                                                                                                                                                                            |
| [**GetMenuInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuinfo)                               | Recupera le informazioni su un menu specificato.<br/>                                                                                                                                                                                                                                                                                                                                                      |
| [**GetMenuItemCount**](/windows/desktop/api/Winuser/nf-winuser-getmenuitemcount)                     | Recupera il numero di elementi nel menu specificato. <br/>                                                                                                                                                                                                                                                                                                                                              |
| [**GetMenuItemID**](/windows/desktop/api/Winuser/nf-winuser-getmenuitemid)                           | Recupera l'identificatore della voce di menu di una voce di menu presente in corrispondenza della posizione specificata in un menu. <br/>                                                                                                                                                                                                                                                                                                    |
| [**GetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa)                       | Recupera le informazioni su una voce di menu.<br/>                                                                                                                                                                                                                                                                                                                                                           |
| [**GetMenuItemRect**](/windows/desktop/api/Winuser/nf-winuser-getmenuitemrect)                       | Recupera il rettangolo di delimitazione per la voce di menu specificata.<br/>                                                                                                                                                                                                                                                                                                                                      |
| [**GetMenuState**](/windows/desktop/api/Winuser/nf-winuser-getmenustate)                             | Recupera i flag di menu associati alla voce di menu specificata. Se la voce di menu apre un sottomenu, questa funzione restituisce anche il numero di elementi nel sottomenu. <br/>                                                                                                                                                                                                                                |
| [**GetMenuString**](/windows/desktop/api/Winuser/nf-winuser-getmenustringa)                           | Copia la stringa di testo della voce di menu specificata nel buffer specificato. <br/>                                                                                                                                                                                                                                                                                                                      |
| [**Getsottomenù**](/windows/desktop/api/Winuser/nf-winuser-getsubmenu)                                 | Recupera un handle per il menu a discesa o il sottomenu attivato dalla voce di menu specificata. <br/>                                                                                                                                                                                                                                                                                                         |
| [**GetSystemMenu**](/windows/desktop/api/Winuser/nf-winuser-getsystemmenu)                           | Consente all'applicazione di accedere al menu finestra (anche noto come menu di sistema o menu di controllo) per la copia e la modifica. <br/>                                                                                                                                                                                                                                                                  |
| [**HiliteMenuItem**](/windows/desktop/api/Winuser/nf-winuser-hilitemenuitem)                         | Evidenzia o rimuove l'evidenziazione da un elemento in una barra dei menu. <br/>                                                                                                                                                                                                                                                                                                                                |
| [**InsertMenuItem**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema)                         | Inserisce una nuova voce di menu in corrispondenza della posizione specificata in un menu.<br/>                                                                                                                                                                                                                                                                                                                                       |
| [**Menu di scelta rapida**](/windows/desktop/api/Winuser/nf-winuser-ismenu)                                         | Determina se un handle è un handle di menu. <br/>                                                                                                                                                                                                                                                                                                                                                     |
| [**LoadMenu**](/windows/desktop/api/Winuser/nf-winuser-loadmenua)                                     | Carica la risorsa di menu specificata dal file eseguibile (exe) associato a un'istanza dell'applicazione. <br/>                                                                                                                                                                                                                                                                                        |
| [**LoadMenuIndirect**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta)                     | Carica il modello di menu specificato in memoria. <br/>                                                                                                                                                                                                                                                                                                                                                      |
| [**MenuItemFromPoint**](/windows/desktop/api/Winuser/nf-winuser-menuitemfrompoint)                   | Determina quale voce di menu, se presente, si trova nella posizione specificata.<br/>                                                                                                                                                                                                                                                                                                                                  |
| [**ModifyMenu**](/windows/desktop/api/Winuser/nf-winuser-modifymenua)                                 | Modifica una voce di menu esistente. Questa funzione viene usata per specificare il contenuto, l'aspetto e il comportamento della voce di menu. <br/>                                                                                                                                                                                                                                                                           |
| [**RemoveMenu**](/windows/desktop/api/Winuser/nf-winuser-removemenu)                                 | Elimina una voce di menu o disconnette un sottomenu dal menu specificato. Se la voce di menu apre un menu a discesa o un sottomenu, [**RemoveMenu**](/windows/desktop/api/Winuser/nf-winuser-removemenu) non elimina il menu o il relativo handle, consentendo il riutilizzo del menu. Prima di chiamare questa funzione, la funzione [**getsottomenù**](/windows/desktop/api/Winuser/nf-winuser-getsubmenu) deve recuperare un handle per il menu a discesa o il sottomenu. <br/>                         |
| [**SetMenu**](/windows/desktop/api/Winuser/nf-winuser-setmenu)                                       | Assegna un nuovo menu alla finestra specificata. <br/>                                                                                                                                                                                                                                                                                                                                                       |
| [**SetMenuDefaultItem**](/windows/desktop/api/Winuser/nf-winuser-setmenudefaultitem)                 | Imposta la voce di menu predefinita per il menu specificato.<br/>                                                                                                                                                                                                                                                                                                                                                 |
| [**SetMenuInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuinfo)                               | Imposta le informazioni per un menu specificato.<br/>                                                                                                                                                                                                                                                                                                                                                             |
| [**SetMenuItemBitmaps**](/windows/desktop/api/Winuser/nf-winuser-setmenuitembitmaps)                 | Associa la bitmap specificata a una voce di menu. Se la voce di menu è selezionata o deselezionata, il sistema Visualizza la bitmap appropriata accanto alla voce di menu. <br/>                                                                                                                                                                                                                                   |
| [**SetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa)                       | Modifica le informazioni relative a una voce di menu.<br/>                                                                                                                                                                                                                                                                                                                                                             |
| [**TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu)                         | Visualizza un menu di scelta rapida nella posizione specificata e tiene traccia della selezione degli elementi nel menu. Il menu di scelta rapida può essere visualizzato in qualsiasi punto dello schermo.<br/>                                                                                                                                                                                                                                             |
| [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex)                     | Visualizza un menu di scelta rapida nella posizione specificata e tiene traccia della selezione degli elementi dal menu di scelta rapida. Il menu di scelta rapida può essere visualizzato in qualsiasi punto dello schermo.<br/>                                                                                                                                                                                                                                    |



 

La funzione seguente è obsoleta.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Nome</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-insertmenua"><strong>InsertMenu</strong></a></td>
<td>Inserisce una nuova voce di menu in un menu, spostandolo gli altri elementi verso il basso nel menu.
<blockquote>
[!Note]<br />
La funzione <a href="/windows/desktop/api/Winuser/nf-winuser-insertmenua"><strong>InsertMenu</strong></a> è stata sostituita dalla funzione <a href="/windows/desktop/api/Winuser/nf-winuser-insertmenuitema"><strong>InsertMenuItem</strong></a> . È comunque possibile usare <strong>InsertMenu</strong>, se non sono necessarie le funzionalità estese di <strong>InsertMenuItem</strong>.
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

### <a name="menu-notifications"></a>Notifiche di menu



| Nome                                                  | Descrizione                                                                                                                                                                          |
|-------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_comando WM**](wm-command.md)                     | Inviato quando l'utente seleziona un elemento di comando da un menu, quando un controllo Invia un messaggio di notifica alla relativa finestra padre o quando viene convertita una sequenza di tasti di scelta rapida. <br/> |
| [**ContextMenu di WM \_**](wm-contextmenu.md)             | Informa una finestra che l'utente ha fatto clic con il *pulsante destro del* mouse sulla finestra.<br/>                                                                            |
| [**\_ENTERMENULOOP WM**](wm-entermenuloop.md)         | Informa la routine della finestra principale di un'applicazione che è stato immesso un ciclo modale di menu. <br/>                                                                                  |
| [**\_EXITMENULOOP WM**](wm-exitmenuloop.md)           | Informa la routine della finestra principale di un'applicazione che un ciclo modale del menu è stato terminato. <br/>                                                                                   |
| [**\_GETTITLEBARINFOEX WM**](wm-gettitlebarinfoex.md) | Inviato per richiedere informazioni estese sulla barra del titolo. Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .<br/>                                  |
| [**MENUCOMMAND di WM \_**](wm-menucommand.md)             | Inviato quando l'utente effettua una selezione da un menu. <br/>                                                                                                                        |
| [**\_MENUDRAG WM**](wm-menudrag.md)                   | Inviato al proprietario di un menu di trascinamento della selezione quando l'utente trascina una voce di menu. <br/>                                                                                               |
| [**\_MENUGETOBJECT WM**](wm-menugetobject.md)         | Inviato al proprietario di un menu a trascinamento quando il cursore del mouse entra in una voce di menu o viene spostato dal centro dell'elemento alla parte superiore o inferiore dell'elemento. <br/>                |
| [**\_MENURBUTTONUP WM**](wm-menurbuttonup.md)         | Inviato quando l'utente rilascia il pulsante destro del mouse mentre il cursore si trova in una voce di menu. <br/>                                                                                   |
| [**\_NEXTMENU WM**](wm-nextmenu.md)                   | Inviato a un'applicazione quando viene usato il tasto freccia destra o sinistra per passare dalla barra dei menu al menu di sistema e viceversa. <br/>                                                      |
| [**\_UNINITMENUPOPUP WM**](wm-uninitmenupopup.md)     | Inviato quando un menu a discesa o un sottomenu viene eliminato definitivamente. <br/>                                                                                                                |



 

### <a name="menu-structures"></a>Strutture di menu



| Nome                                                       | Descrizione                                                                                                                                                     |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MDINEXTMENU**](/windows/win32/api/winuser/ns-winuser-mdinextmenu)                         | Contiene informazioni sul menu da attivare. <br/>                                                                                                |
| [**MENUBARINFO**](/windows/win32/api/winuser/ns-winuser-menubarinfo)                         | Contiene informazioni sulla barra dei menu.<br/>                                                                                                                       |
| [**\_intestazione del modello menuex \_**](menuex-template-header.md) | Definisce l'intestazione per un modello di menu esteso. Questa definizione di struttura è solo per la spiegazione; non è presente in alcun file di intestazione standard. <br/> |
| [**\_elemento del modello menuex \_**](menuex-template-item.md)     | Definisce una voce di menu in un modello di menu esteso. Questa definizione di struttura è solo per la spiegazione; non è presente in alcun file di intestazione standard.<br/>  |
| [**MENUGETOBJECTINFO**](/windows/win32/api/winuser/ns-winuser-menugetobjectinfo)             | Contiene informazioni sul menu su cui si trova il cursore del mouse.<br/>                                                                                     |
| [**MENUINFO**](/windows/win32/api/winuser/ns-winuser-menuinfo)                               | Contiene informazioni relative a un menu.<br/>                                                                                                                   |
| [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa)                       | Contiene informazioni su una voce di menu. <br/>                                                                                                             |
| [**MENUITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplate)               | Definisce una voce di menu in un modello di menu. <br/>                                                                                                             |
| [**MENUITEMTEMPLATEHEADER**](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplateheader)   | Definisce l'intestazione per un modello di menu. Un modello di menu completo è costituito da un'intestazione e da uno o più elenchi di voci di menu. <br/>                              |
| [**TPMPARAMS**](/windows/win32/api/winuser/ns-winuser-tpmparams)                             | Contiene parametri estesi per la funzione [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) .<br/>                                                          |



 

 

