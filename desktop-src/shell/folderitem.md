---
description: Rappresenta un elemento in una cartella della shell. Questo oggetto contiene proprietà e metodi che consentono di recuperare informazioni sull'elemento.
title: Oggetto FolderItem (shldisp. h)
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
ms.openlocfilehash: a1c66c594a60682ad359ffbcdcd0bf045601051d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484028"
---
# <a name="folderitem-object"></a>Oggetto FolderItem

Rappresenta un elemento in una cartella della shell. Questo oggetto contiene proprietà e metodi che consentono di recuperare informazioni sull'elemento.

## <a name="members"></a>Membri

L'oggetto **FolderItem** dispone di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'oggetto **FolderItem** dispone di questi metodi.



| Metodo                                      | Descrizione                                                                                                                                                 |
|:--------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**InvokeVerb**](folderitem-invokeverb.md) | Esegue un verbo sull'elemento.<br/>                                                                                                                     |
| [**Verbi**](folderitem-verbs.md)           | Recupera l'oggetto [**folderitemverbs**](folderitemverbs.md) dell'elemento. Questo oggetto è la raccolta di verbi che possono essere eseguiti sull'elemento.<br/> |



 

### <a name="properties"></a>Proprietà

L'oggetto **FolderItem** dispone di queste proprietà.



| Proprietà                                                   | Tipo di accesso           | Descrizione                                                                                                                                                                                                        |
|:-----------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Applicazione**](folderitem-application.md)<br/>   | Sola lettura<br/>  | Contiene l'oggetto [**applicazione**](folderitem-application.md) dell'elemento della cartella.<br/>                                                                                                                   |
| [**GetFolder**](folderitem-getfolder.md)<br/>       | Sola lettura<br/>  | Contiene l'oggetto [**cartella**](folder.md) dell'elemento, se l'elemento è una cartella.<br/>                                                                                                                           |
| [**GetLink**](folderitem-getlink.md)<br/>           | Sola lettura<br/>  | Contiene l'oggetto [**ShellLinkObject**](shelllinkobject-object.md) dell'elemento, se l'elemento è un tasto di scelta rapida.<br/>                                                                                                |
| [**IsBrowsable**](folderitem-isbrowsable.md)<br/>   | Sola lettura<br/>  | Indica se l'elemento può essere ospitato all'interno di un browser o di un frame di Esplora risorse.<br/>                                                                                                                         |
| [**FileSystem**](folderitem-isfilesystem.md)<br/> | Sola lettura<br/>  | Indica se l'elemento fa parte dell'file system.<br/>                                                                                                                                                       |
| [**IsFolder**](folderitem-isfolder.md)<br/>         | Sola lettura<br/>  | Indica se l'elemento è una cartella.<br/>                                                                                                                                                                      |
| [**IsLink**](folderitem-islink.md)<br/>             | Sola lettura<br/>  | Indica se l'elemento è un tasto di scelta rapida.<br/>                                                                                                                                                               |
| [**ModifyDate**](folderitem-modifydate.md)<br/>     | Lettura/Scrittura<br/> | Imposta o ottiene la data e l'ora dell'Ultima modifica apportata a un file. [**ModifyDate**](folderitem-modifydate.md) può essere utilizzato per recuperare la data e l'ora dell'Ultima modifica di una cartella, ma non può essere impostata.<br/> |
| [**Nome**](folderitem-name.md)<br/>                 | Lettura/Scrittura<br/> | Imposta o ottiene il nome dell'elemento.<br/>                                                                                                                                                                           |
| [**Padre**](folderitem-parent.md)<br/>             | Sola lettura<br/>  | Ottiene un oggetto che rappresenta l'elemento padre dell'elemento.<br/>                                                                                                                                                  |
| [**Percorso**](folderitem-path.md)<br/>                 | Sola lettura<br/>  | Contiene il nome e il percorso completo dell'elemento.<br/>                                                                                                                                                                 |
| [**Dimensione**](folderitem-size.md)<br/>                 | Sola lettura<br/>  | Contiene la dimensione dell'elemento.<br/>                                                                                                                                                                               |
| [**Tipo**](folderitem-type.md)<br/>                 | Sola lettura<br/>  | Contiene una rappresentazione di stringa del tipo dell'elemento.<br/>                                                                                                                                                    |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, \[ solo app desktop Windows XP\]<br/>                                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                           |
| Intestazione<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 4,71 o successiva)</dt> </dl> |



 

 




