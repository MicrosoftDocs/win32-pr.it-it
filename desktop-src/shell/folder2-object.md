---
description: Estende l'oggetto Folder per supportare le cartelle offline.
title: Oggetto Cartella2 (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder2
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 5b52b141-ced3-4d38-8584-7dfcfe12ab56
ms.openlocfilehash: 8db899fc52cc3511d1af82013fc6c4c87544f1cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979674"
---
# <a name="folder2-object"></a>Oggetto Cartella2

Estende l'oggetto [**Folder**](folder.md) per supportare le cartelle offline.

## <a name="members"></a>Membri

L'oggetto **Cartella2** dispone di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'oggetto **Cartella2** dispone di questi metodi.



| Metodo                                                                 | Descrizione                                                                          |
|:-----------------------------------------------------------------------|:-------------------------------------------------------------------------------------|
| [**DismissedWebViewBarricade**](folder2-dismissedwebviewbarricade.md) | Chiamato in risposta alla barricata della visualizzazione Web che viene rilasciata dall'utente.<br/> |
| [**Sincronizzare**](folder2-synchronize.md)                             | Sincronizza tutti i file offline nella cartella.<br/>                             |



 

### <a name="properties"></a>Proprietà

L'oggetto **Cartella2** dispone di queste proprietà.



| Proprietà                                                                            | Tipo di accesso          | Descrizione                                                               |
|:------------------------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------|
| [**HaveToShowWebViewBarricade**](folder2-havetoshowwebviewbarricade.md)<br/> | Sola lettura<br/> | Non è attualmente supportato.<br/>                                       |
| [**OfflineStatus**](folder2-offlinestatus.md)<br/>                           | Sola lettura<br/> | Contiene lo stato offline della cartella.<br/>                     |
| [**Auto**](folder2-self.md)<br/>                                             | Sola lettura<br/> | Contiene l'oggetto [**FolderItem**](folderitem.md) della cartella.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, \[ solo app desktop Windows XP\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 5,0 o successiva)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Cartella**](folder.md)
</dt> </dl>

 

 




