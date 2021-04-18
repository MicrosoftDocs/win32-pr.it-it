---
title: Oggetto WebViewFolderContents (Shldisp.h)
description: Implementato dalla Shell per l'utilizzo all'interno di una visualizzazione WebView.
ms.assetid: c9c46e21-2721-43c9-a6f4-38fafbda3798
keywords:
- Funzionalità dell'ambiente Windows legacy dell'oggetto WebViewFolderContents
- Funzionalità dell'ambiente Windows legacy dell'oggetto WebViewFolderContents, descritte
topic_type:
- apiref
api_name:
- WebViewFolderContents
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9ea2020e2d9baaffbc026692faafc702db14781
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301032"
---
# <a name="webviewfoldercontents-object"></a>Oggetto WebViewFolderContents

Implementato dalla Shell per l'utilizzo all'interno di una *visualizzazione WebView*. **WebViewFolderContents** si inizializza automaticamente nella cartella corrente di WebView. Viene creata una visualizzazione di cartelle della shell che Visualizza il contenuto della cartella in uno dei cinque formati seguenti: icona piccola, icona grande, elenco, dettagli o anteprima. Non è valido all'esterno di una WebView.

I metodi e le proprietà esposte da **WebViewFolderContents** sono identici a quelli dell'oggetto [**ShellFolderView**](/windows/desktop/shell/shellfolderview) .

## <a name="members"></a>Membri

L'oggetto **WebViewFolderContents** dispone di questi tipi di membri:

-   [Eventi](#events)
-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="events"></a>Eventi

L'oggetto **WebViewFolderContents** presenta questi eventi.



| Event                                                              | Descrizione                                                                              |
|:-------------------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| [**SelectionChanged**](webviewfoldercontents-selectionchanged.md) | Si verifica quando viene modificato lo stato di selezione di un elemento o di elementi nella visualizzazione.<br/> |



 

### <a name="methods"></a>Metodi

L'oggetto **WebViewFolderContents** dispone di questi metodi.



| Metodo                                                       | Descrizione                                                                                                          |
|:-------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [**PopupItemMenu**](webviewfoldercontents-popupitemmenu.md) | Crea un menu di scelta rapida per l'elemento specificato e restituisce la stringa di comando selezionata.<br/>                   |
| [**SelectedItems**](webviewfoldercontents-selecteditems.md) | Ottiene un oggetto [**FolderItems**](../shell/folderitems.md) che rappresenta tutti gli elementi selezionati nella visualizzazione.<br/> |
| [**SelectItem**](webviewfoldercontents-selectitem.md)       | Imposta lo stato di selezione di un elemento nella visualizzazione.<br/>                                                          |



 

### <a name="properties"></a>Proprietà

L'oggetto **WebViewFolderContents** dispone di queste proprietà.



| Proprietà                                                            | Tipo di accesso          | Descrizione                                                                                                                              |
|:--------------------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [**Applicazione**](webviewfoldercontents-application.md)<br/> | Sola lettura<br/> | Non implementato.<br/>                                                                                                              |
| [**FocusedItem**](webviewfoldercontents-focuseditem.md)<br/> | Sola lettura<br/> | Ottiene un oggetto [**FolderItem**](../shell/folderitem.md) che rappresenta l'elemento con lo stato attivo per l'input.<br/>                           |
| [**Cartella**](webviewfoldercontents-folder.md)<br/>           | Sola lettura<br/> | Ottiene un oggetto [**cartella**](../shell/folder.md) che rappresenta la visualizzazione.<br/>                                                            |
| [**Padre**](webviewfoldercontents-parent.md)<br/>           | Sola lettura<br/> | Non implementato.<br/>                                                                                                              |
| [**Script**](webviewfoldercontents-script.md)<br/>           | Sola lettura<br/> | Ottiene l'oggetto di scripting per la visualizzazione.<br/>                                                                                       |
| [**ViewOptions**](webviewfoldercontents-viewoptions.md)<br/> | Sola lettura<br/> | Ottiene un set di flag [**ShellFolderViewOptions**](/windows/desktop/api/shldisp/ne-shldisp-shellfolderviewoptions) che indicano le opzioni correnti della visualizzazione.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, \[ solo app desktop Windows XP\]<br/>                                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                           |
| Intestazione<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 4,71 o successiva)</dt> </dl> |



 

