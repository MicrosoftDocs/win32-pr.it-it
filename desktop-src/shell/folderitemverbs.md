---
description: Rappresenta la raccolta di verbi per un elemento in una cartella della shell. Questo oggetto contiene proprietà e metodi che consentono di recuperare informazioni sulla raccolta.
title: Oggetto FolderItemVerbs (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItemVerbs
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 31badb4b-b89e-4294-9dd7-bda716e163b2
ms.openlocfilehash: 651f439ea34a55203da852f2907a27ba87bdd275
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881586"
---
# <a name="folderitemverbs-object"></a>Oggetto FolderItemVerbs

Rappresenta la raccolta di verbi per un elemento in una cartella della shell. Questo oggetto contiene proprietà e metodi che consentono di recuperare informazioni sulla raccolta.

## <a name="members"></a>Membri

L'oggetto **folderitemverbs** dispone di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'oggetto **folderitemverbs** dispone di questi metodi.



| Metodo                                        | Descrizione                                                                                                      |
|:----------------------------------------------|:-----------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](folderitemverbs--newenum.md) | Crea e restituisce un nuovo oggetto **folderitemverbs** che è una copia di questo oggetto folderitemverbs.<br/>   |
| [**Elemento**](folderitemverbs-item.md)          | Recupera l'oggetto [**FolderItemVerb**](folderitemverb.md) per un elemento specificato nella raccolta.<br/> |



 

### <a name="properties"></a>Proprietà

L'oggetto **folderitemverbs** dispone di queste proprietà.



| Proprietà                                                      | Tipo di accesso          | Descrizione                                                |
|:--------------------------------------------------------------|:---------------------|:-----------------------------------------------------------|
| [**Applicazione**](folderitemverbs-application.md)<br/> | Sola lettura<br/> | Non implementato.<br/>                                |
| [**Conteggio**](folderitemverbs-count.md)<br/>             | Sola lettura<br/> | Contiene il numero di elementi nella raccolta.<br/> |
| [**Padre**](folderitemverbs-parent.md)<br/>           | Sola lettura<br/> | Non implementato.<br/>                                |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, \[ solo app desktop Windows XP\]<br/>                                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                           |
| Intestazione<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 4,71 o successiva)</dt> </dl> |



 

 




