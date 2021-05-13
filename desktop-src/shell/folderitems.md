---
description: Rappresenta la raccolta di elementi in una cartella Shell. Questo oggetto contiene proprietà e metodi che consentono di recuperare informazioni sulla raccolta.
title: Oggetto FolderItems (Shldisp.h)
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
ms.openlocfilehash: 2b6e9506d6c2354018a41ae7a15ca6e8e1900857
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840652"
---
# <a name="folderitems-object"></a>Oggetto FolderItems

Rappresenta la raccolta di elementi in una cartella Shell. Questo oggetto contiene proprietà e metodi che consentono di recuperare informazioni sulla raccolta.

## <a name="members"></a>Membri

**L'oggetto FolderItems** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

**L'oggetto FolderItems** dispone di questi metodi.



| Metodo                                    | Descrizione                                                                                              |
|:------------------------------------------|:---------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](folderitems--newenum.md) | Non implementato.<br/>                                                                              |
| [**Elemento**](folderitems-item.md)          | Recupera [**l'oggetto FolderItem**](folderitem.md) per un elemento specificato nella raccolta.<br/> |



 

### <a name="properties"></a>Proprietà

**L'oggetto FolderItems** ha queste proprietà.



| Proprietà                                                  | Tipo di accesso          | Descrizione                                                                                                   |
|:----------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------|
| [**Applicazione**](folderitems-application.md)<br/> | Sola lettura<br/> | Contiene [**l'oggetto Application**](folderitems-application.md) della raccolta di elementi cartella.<br/> |
| [**Conteggio**](folderitems-count.md)<br/>             | Sola lettura<br/> | Contiene il numero di elementi nella raccolta.<br/>                                                    |
| [**Padre**](folderitems-parent.md)<br/>           | Sola lettura<br/> | Non implementato.<br/>                                                                                   |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop di Windows 2000 Professional e Windows XP \[\]<br/>                                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                           |
| Intestazione<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 4.71 o successiva)</dt> </dl> |



 

 




