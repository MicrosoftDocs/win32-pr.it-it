---
description: In questo argomento vengono elencati gli elementi di programmazione principali utilizzati con i menu di scelta rapida (contesto) e i gestori dei menu di scelta rapida. I gestori dei menu di scelta rapida, noti anche come gestori di menu di scelta rapida o gestori di verbi, sono un tipo di gestore di tipi di file.
ms.assetid: efd96a52-6455-40bc-9c21-65f89728e771
title: Riferimento al menu di scelta rapida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cb1552c8f2f383b08984e9142e464b6831a3c8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225932"
---
# <a name="shortcut-menu-reference"></a>Riferimento al menu di scelta rapida

In questo argomento vengono elencati gli elementi di programmazione principali utilizzati con i menu di scelta rapida (contesto) e i gestori dei menu di scelta rapida. I gestori dei menu di scelta rapida, noti anche come gestori di menu di scelta rapida o gestori di verbi, sono un tipo di gestore di tipi di file.

## <a name="about-shortcut-menu-implemetation"></a>Informazioni sul menu di scelta rapida implementazione

Si consiglia di implementare un menu di scelta rapida utilizzando uno dei metodi del verbo statico. Leggere le istruzioni seguenti:

-   Per usare un metodo verbo statico per implementare un menu di scelta rapida, vedere la sezione "personalizzazione di un menu di scelta rapida con verbi statici" di [creazione di gestori di menu di scelta rapida](context-menu-handlers.md).
-   Per ottenere il comportamento dinamico per i verbi statici in Windows 7 e versioni successive, vedere la sezione relativa all'acquisizione del comportamento dinamico per i verbi statici in [creazione di gestori di menu di scelta rapida](context-menu-handlers.md).
-   Per informazioni dettagliate sull'implementazione del verbo statico e sui verbi dinamici da evitare, vedere [scelta di un verbo statico o dinamico per il menu di scelta rapida](shortcut-choose-method.md).
-   Se è necessario estendere il menu di scelta rapida per un tipo di file registrando un verbo dinamico per il tipo di file, seguire le istruzioni fornite in [personalizzazione di un menu di scelta rapida usando verbi dinamici](shortcut-menu-using-dynamic-verbs.md).

### <a name="interfaces"></a>Interfacce



| Argomento                                        | Contenuto                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu)         | Espone metodi che creano o uniscono un menu di scelta rapida associato a un oggetto Shell.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**IContextMenu2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu2)       | Espone metodi che creano o uniscono un menu di scelta rapida associato a un oggetto Shell. Estende [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) aggiungendo un metodo che consente agli oggetti client di gestire i messaggi associati a voci di menu create dal proprietario.<br/>                                                                                                                                                                                                                                                    |
| [**IContextMenu3**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu3)       | Espone metodi che creano o uniscono un menu di scelta rapida associato a un oggetto Shell. Consente agli oggetti client di gestire i messaggi associati a voci di menu create dal proprietario ed estende [**IContextMenu2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu2) accettando un valore restituito dalla gestione dei messaggi.<br/>                                                                                                                                                                                                                         |
| [**IContextMenuCB**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenucb)     | Espone un metodo che Abilita il callback di un menu di scelta rapida. Ad esempio, per aggiungere un'icona dello scudo a un **MenuItem** che richiede l'elevazione dei privilegi.<br/>                                                                                                                                                                                                                                                                                                                                                                     |
| [**IContextMenuSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenusite) | Implementato dalla visualizzazione cartella predefinita creata utilizzando [**SHCreateShellFolderView**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderview). Un'implementazione di [**IContextMenuSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenusite) supporta [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu), [**IContextMenu:: InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand)e [**TrackPopupMenu**](/windows/win32/api/winuser/nf-winuser-trackpopupmenu) ed eventuali inoltri dei messaggi necessari per tale funzione. **IContextMenuSite** in genere aggiorna anche la barra di stato.<br/> |



 

### <a name="functions"></a>Funzioni



| Argomento                                                            | Contenuto                                                                                                                                |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [**\_Create2 CDefFolderMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2)        | Consente di creare un menu di scelta rapida per un gruppo selezionato di oggetti cartella di file.<br/>                                                          |
| [**LPFNDFMCALLBACK**](/windows/win32/api/shlobj_core/nc-shlobj_core-lpfndfmcallback)                       | Definisce il prototipo per la funzione di callback che riceve i messaggi dall'implementazione del menu di scelta rapida predefinito della shell.<br/> |
| [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu) | Crea un oggetto che rappresenta l'implementazione del menu di scelta rapida predefinito della shell.<br/>                                           |



 

### <a name="structures"></a>Strutture



| Argomento                                                  | Contenuto                                                                                                                                                                                                   |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CMINVOKECOMMANDINFO**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo)     | Contiene le informazioni necessarie per [**IContextMenu:: InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) per richiamare un comando di menu di scelta rapida.<br/>                                                             |
| [**CMINVOKECOMMANDINFOEX**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) | Contiene informazioni estese su un comando di menu di scelta rapida. Questa struttura è una versione estesa di [**CMINVOKECOMMANDINFO**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo) che consente l'utilizzo di valori Unicode.<br/> |
| [**DEFCONTEXTMENU**](/windows/desktop/api/shlobj_core/ns-shlobj_core-defcontextmenu)               | Contiene informazioni sul menu di scelta rapida utilizzate da [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).<br/>                                                                                     |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Menu di scelta rapida (contesto) e gestori di menu di scelta rapida](context-menu.md)
</dt> <dt>

[Scelta di un verbo statico o dinamico per il menu di scelta rapida](shortcut-choose-method.md)
</dt> <dt>

[Verbi e associazioni di file](fa-verbs.md)
</dt> <dt>

[Procedure consigliate per i gestori di menu di scelta rapida e più verbi di selezione](verbs-best-practices.md)
</dt> <dt>

[Creazione di gestori di menu di scelta rapida](context-menu-handlers.md)
</dt> <dt>

[Personalizzazione di un menu di scelta rapida tramite verbi dinamici](shortcut-menu-using-dynamic-verbs.md)
</dt> </dl>

 

 
