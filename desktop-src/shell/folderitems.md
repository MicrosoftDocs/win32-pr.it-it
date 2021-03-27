---
description: Rappresenta la raccolta di elementi in una cartella della shell. Questo oggetto contiene proprietà e metodi che consentono di recuperare informazioni sulla raccolta.
title: Oggetto FolderItems (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItems
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: b99201b3-95e8-4ddd-b338-dee8d107d0a0
ms.openlocfilehash: 6f9a6fa978c64c788cbd224cf3a39454c644a57e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749154"
---
# <a name="folderitems-object"></a>Oggetto FolderItems

Rappresenta la raccolta di elementi in una cartella della shell. Questo oggetto contiene proprietà e metodi che consentono di recuperare informazioni sulla raccolta.

## <a name="members"></a>Membri

L'oggetto **FolderItems** dispone di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'oggetto **FolderItems** dispone di questi metodi.



| Metodo                                    | Descrizione                                                                                              |
|:------------------------------------------|:---------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](folderitems--newenum.md) | Non implementato.<br/>                                                                              |
| [**Elemento**](folderitems-item.md)          | Recupera l'oggetto [**FolderItem**](folderitem.md) per un elemento specificato nella raccolta.<br/> |



 

### <a name="properties"></a>Proprietà

L'oggetto **FolderItems** dispone di queste proprietà.



| Proprietà                                                  | Tipo di accesso          | Descrizione                                                                                                   |
|:----------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------|
| [**Applicazione**](folderitems-application.md)<br/> | Sola lettura<br/> | Contiene l'oggetto [**applicazione**](folderitems-application.md) della raccolta di elementi cartella.<br/> |
| [**Conteggio**](folderitems-count.md)<br/>             | Sola lettura<br/> | Contiene il numero di elementi nella raccolta.<br/>                                                    |
| [**Padre**](folderitems-parent.md)<br/>           | Sola lettura<br/> | Non implementato.<br/>                                                                                   |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, \[ solo app desktop Windows XP\]<br/>                                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                           |
| Intestazione<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 4,71 o successiva)</dt> </dl> |



 

 




