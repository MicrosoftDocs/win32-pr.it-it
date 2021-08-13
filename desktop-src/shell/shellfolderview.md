---
description: Rappresenta gli oggetti in una vista e fornisce proprietà e metodi utilizzati per ottenere informazioni sul contenuto della vista.
ms.assetid: 3b866266-fee0-42f7-a1e0-9adb6cc2e23f
title: Oggetto ShellFolderView (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: a95d57edb7992c9511e34480190580d34ad42da23c64c4297f5e4ebb75a95e73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118452128"
---
# <a name="shellfolderview-object"></a>Oggetto ShellFolderView

Rappresenta gli oggetti in una vista e fornisce proprietà e metodi utilizzati per ottenere informazioni sul contenuto della vista.

## <a name="members"></a>Membri

**L'oggetto ShellFolderView** ha questi tipi di membri:

-   [Eventi](#events)
-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="events"></a>Eventi

**L'oggetto ShellFolderView** include questi eventi.



| Event                                                        | Descrizione                                                                              |
|:-------------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| [**SelectionChanged**](shellfolderview-selectionchanged.md) | Si verifica quando lo stato di selezione di uno o più elementi nella visualizzazione viene modificato.<br/> |



 

### <a name="methods"></a>Metodi

**L'oggetto ShellFolderView** dispone di questi metodi.



| Metodo                                                 | Descrizione                                                                                                        |
|:-------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------|
| [**PopupItemMenu**](shellfolderview-popupitemmenu.md) | Crea un menu di scelta rapida per l'elemento specificato e restituisce la stringa di comando selezionata.<br/>                 |
| [**SelectedItems**](shellfolderview-selecteditems.md) | Ottiene un [**oggetto FolderItems**](folderitems.md) che rappresenta tutti gli elementi selezionati nella visualizzazione.<br/> |
| [**SelectItem**](shellfolderview-selectitem.md)       | Imposta lo stato di selezione di un elemento nella visualizzazione.<br/>                                                        |



 

### <a name="properties"></a>Proprietà

**L'oggetto ShellFolderView** ha queste proprietà.



| Proprietà                                                      | Tipo di accesso          | Descrizione                                                                                                  |
|:--------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------------------------------------|
| [**Applicazione**](shellfolderview-application.md)<br/> | Sola lettura<br/> | Contiene l'oggetto Application dell'oggetto.<br/>                                                         |
| [**FocusedItem**](shellfolderview-focuseditem.md)<br/> | Sola lettura<br/> | Ottiene un [**oggetto FolderItem**](folderitem.md) che rappresenta l'elemento con lo stato attivo per l'input.<br/> |
| [**Cartella**](shellfolderview-folder.md)<br/>           | Sola lettura<br/> | Ottiene un [**oggetto Folder**](folder.md) che rappresenta la visualizzazione.<br/>                                  |
| [**Padre**](shellfolderview-parent.md)<br/>           | Sola lettura<br/> | Non implementato.<br/>                                                                                  |
| [**Script**](shellfolderview-script.md)<br/>           | Sola lettura<br/> | Deprecato.<br/>                                                                                       |
| [**ViewOptions**](shellfolderview-viewoptions.md)<br/> | Sola lettura<br/> | Ottiene un set di flag che indicano le opzioni correnti della visualizzazione.<br/>                                |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, Windows solo app desktop XP \[\]<br/>                                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                           |
| Intestazione<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 4.71 o successiva)</dt> </dl> |
| IID<br/>                      | CLSID \_ ShellFolderView<br/>                                                                              |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Flag ShellFolderViewOptions**](/windows/desktop/api/Shldisp/ne-shldisp-shellfolderviewoptions)
</dt> </dl>

 

 




