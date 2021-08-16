---
description: In questo argomento vengono elencati gli elementi di programmazione principali utilizzati con i menu di scelta rapida e i gestori dei menu di scelta rapida. I gestori dei menu di scelta rapida, noti anche come gestori di menu di scelta rapida o gestori di verbi, sono un tipo di gestore del tipo di file.
ms.assetid: efd96a52-6455-40bc-9c21-65f89728e771
title: Informazioni di riferimento sul menu di scelta rapida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25f80b62b88750200456da76c22017b3f18fbba584272dc028809771c807ad85
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120090771"
---
# <a name="shortcut-menu-reference"></a>Informazioni di riferimento sul menu di scelta rapida

In questo argomento vengono elencati gli elementi di programmazione principali utilizzati con i menu di scelta rapida e i gestori dei menu di scelta rapida. I gestori dei menu di scelta rapida, noti anche come gestori di menu di scelta rapida o gestori di verbi, sono un tipo di gestore del tipo di file.

## <a name="about-shortcut-menu-implemetation"></a>Informazioni sull'implessimento del menu di scelta rapida

È consigliabile implementare un menu di scelta rapida usando uno dei metodi verbi statici. Esaminare le istruzioni seguenti:

-   Per usare un metodo verbo statico per implementare un menu di scelta rapida, vedere la sezione "Personalizzazione di un menu di scelta rapida tramite verbi statici" di Creazione di gestori [del menu di scelta rapida.](context-menu-handlers.md)
-   Per ottenere il comportamento dinamico per i verbi statici in Windows 7 e versioni successive, vedere "Recupero del comportamento dinamico per i verbi statici" in Creazione di gestori del [menu di scelta rapida.](context-menu-handlers.md)
-   Per informazioni dettagliate sull'implementazione di verbi statici e sui verbi dinamici da evitare, vedere Scelta di un verbo statico o dinamico [per il menu di scelta rapida.](shortcut-choose-method.md)
-   Se è necessario estendere il menu di scelta rapida per un tipo di file registrando un verbo dinamico per il tipo di file, seguire le istruzioni fornite in [Personalizzazione](shortcut-menu-using-dynamic-verbs.md)di un menu di scelta rapida utilizzando verbi dinamici .

### <a name="interfaces"></a>Interfacce



| Argomento                                        | Contenuto                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu)         | Espone metodi che creano o uniscono un menu di scelta rapida associato a un oggetto shell.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**IContextMenu2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu2)       | Espone metodi che creano o uniscono un menu di scelta rapida associato a un oggetto shell. Estende [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) aggiungendo un metodo che consente agli oggetti client di gestire i messaggi associati alle voci di menu disegnate dal proprietario.<br/>                                                                                                                                                                                                                                                    |
| [**IContextMenu3**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu3)       | Espone metodi che creano o uniscono un menu di scelta rapida associato a un oggetto shell. Consente agli oggetti client di gestire i messaggi associati alle voci di menu disegnate dal proprietario ed estende [**IContextMenu2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu2) accettando un valore restituito dalla gestione dei messaggi.<br/>                                                                                                                                                                                                                         |
| [**IContextMenuCB**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenucb)     | Espone un metodo che abilita il callback di un menu di scelta rapida. Ad esempio, per aggiungere un'icona di schermatura a un **menuItem che** richiede l'elevazione dei privilegi.<br/>                                                                                                                                                                                                                                                                                                                                                                     |
| [**IContextMenuSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenusite) | Implementato dalla visualizzazione cartella predefinita creata usando [**SHCreateShellFolderView.**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderview) Un'implementazione di [**IContextMenuSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenusite) supporta [**IContextMenu::QueryContextMenu,**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand)e [**TrackPopupMenu**](/windows/win32/api/winuser/nf-winuser-trackpopupmenu) e qualsiasi inoltro di messaggi necessario per tale funzione. **IContextMenuSite in** genere aggiorna anche la barra di stato.<br/> |



 

### <a name="functions"></a>Funzioni



| Argomento                                                            | Contenuto                                                                                                                                |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2)        | Crea un menu di scelta rapida per un gruppo selezionato di oggetti cartella file.<br/>                                                          |
| [**LPFNDFMCALLBACK**](/windows/win32/api/shlobj_core/nc-shlobj_core-lpfndfmcallback)                       | Definisce il prototipo per la funzione di callback che riceve messaggi dall'implementazione del menu di scelta rapida predefinito della shell.<br/> |
| [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu) | Crea un oggetto che rappresenta l'implementazione predefinita del menu di scelta rapida della shell.<br/>                                           |



 

### <a name="structures"></a>Strutture



| Argomento                                                  | Contenuto                                                                                                                                                                                                   |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CMINVOKECOMMANDINFO**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo)     | Contiene le informazioni necessarie a [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) per richiamare un comando di menu di scelta rapida.<br/>                                                             |
| [**CMINVOKECOMMANDINFOEX**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) | Contiene informazioni estese su un comando di menu di scelta rapida. Questa struttura è una versione estesa di [**CMINVOKECOMMANDINFO**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo) che consente l'uso di valori Unicode.<br/> |
| [**DEFCONTEXTMENU**](/windows/desktop/api/shlobj_core/ns-shlobj_core-defcontextmenu)               | Contiene informazioni sul menu di scelta rapida [**usate da SHCreateDefaultContextMenu.**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu)<br/>                                                                                     |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Menu di scelta rapida e gestori del menu di scelta rapida](context-menu.md)
</dt> <dt>

[Scelta di un verbo statico o dinamico per il menu di scelta rapida](shortcut-choose-method.md)
</dt> <dt>

[Verbi e associazioni di file](fa-verbs.md)
</dt> <dt>

[Procedure consigliate per i gestori del menu di scelta rapida e più verbi di selezione](verbs-best-practices.md)
</dt> <dt>

[Creazione di gestori del menu di scelta rapida](context-menu-handlers.md)
</dt> <dt>

[Personalizzazione di un menu di scelta rapida tramite verbi dinamici](shortcut-menu-using-dynamic-verbs.md)
</dt> </dl>

 

 
