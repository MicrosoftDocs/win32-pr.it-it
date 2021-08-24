---
description: Rappresenta un elemento in una cartella Shell. Questo oggetto contiene proprietà e metodi che consentono di recuperare informazioni sull'elemento.
title: Oggetto FolderItem (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItem
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 38c0e049-2f9f-43bc-8bf2-1b7becf16e66
ms.openlocfilehash: f6744441c051d65bd24f2db888f9bc8d71e66cedcf50c097094beee8ae5a96a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119715371"
---
# <a name="folderitem-object"></a>Oggetto FolderItem

Rappresenta un elemento in una cartella Shell. Questo oggetto contiene proprietà e metodi che consentono di recuperare informazioni sull'elemento.

## <a name="members"></a>Membri

**L'oggetto FolderItem** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

**L'oggetto FolderItem** dispone di questi metodi.



| Metodo                                      | Descrizione                                                                                                                                                 |
|:--------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**InvokeVerb**](folderitem-invokeverb.md) | Esegue un verbo sull'elemento.<br/>                                                                                                                     |
| [**Verbi**](folderitem-verbs.md)           | Recupera l'oggetto [**FolderItemVerbs**](folderitemverbs.md) dell'elemento. Questo oggetto è la raccolta di verbi che possono essere eseguiti sull'elemento.<br/> |



 

### <a name="properties"></a>Proprietà

**L'oggetto FolderItem** ha queste proprietà.



| Proprietà                                                   | Tipo di accesso           | Descrizione                                                                                                                                                                                                        |
|:-----------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Applicazione**](folderitem-application.md)<br/>   | Sola lettura<br/>  | Contiene [**l'oggetto Application**](folderitem-application.md) dell'elemento cartella.<br/>                                                                                                                   |
| [**GetFolder**](folderitem-getfolder.md)<br/>       | Sola lettura<br/>  | Contiene l'oggetto [**Folder dell'elemento,**](folder.md) se l'elemento è una cartella.<br/>                                                                                                                           |
| [**GetLink**](folderitem-getlink.md)<br/>           | Sola lettura<br/>  | Contiene l'oggetto [**ShellLinkObject**](shelllinkobject-object.md) dell'elemento, se l'elemento è un collegamento.<br/>                                                                                                |
| [**IsBrowsable**](folderitem-isbrowsable.md)<br/>   | Sola lettura<br/>  | Indica se l'elemento può essere ospitato all'interno di un browser o Windows Explorer.<br/>                                                                                                                         |
| [**IsFileSystem**](folderitem-isfilesystem.md)<br/> | Sola lettura<br/>  | Indica se l'elemento fa parte del file system.<br/>                                                                                                                                                       |
| [**IsFolder**](folderitem-isfolder.md)<br/>         | Sola lettura<br/>  | Indica se l'elemento è una cartella.<br/>                                                                                                                                                                      |
| [**IsLink**](folderitem-islink.md)<br/>             | Sola lettura<br/>  | Indica se l'elemento è un collegamento.<br/>                                                                                                                                                               |
| [**ModifyDate**](folderitem-modifydate.md)<br/>     | Lettura/Scrittura<br/> | Imposta o ottiene la data e l'ora dell'ultima modifica di un file. [**ModifyDate**](folderitem-modifydate.md) può essere usato per recuperare la data e l'ora dell'ultima modifica di una cartella, ma non può impostarla.<br/> |
| [**Nome**](folderitem-name.md)<br/>                 | Lettura/Scrittura<br/> | Imposta o ottiene il nome dell'elemento.<br/>                                                                                                                                                                           |
| [**Padre**](folderitem-parent.md)<br/>             | Sola lettura<br/>  | Ottiene un oggetto che rappresenta l'elemento padre dell'elemento.<br/>                                                                                                                                                  |
| [**Percorso**](folderitem-path.md)<br/>                 | Sola lettura<br/>  | Contiene il percorso completo e il nome dell'elemento.<br/>                                                                                                                                                                 |
| [**Dimensione**](folderitem-size.md)<br/>                 | Sola lettura<br/>  | Contiene le dimensioni dell'elemento.<br/>                                                                                                                                                                               |
| [**Tipo**](folderitem-type.md)<br/>                 | Sola lettura<br/>  | Contiene una rappresentazione di stringa del tipo dell'elemento.<br/>                                                                                                                                                    |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, Windows solo app desktop XP \[\]<br/>                                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                           |
| Intestazione<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 4.71 o successiva)</dt> </dl> |



 

 




