---
description: Estende l'oggetto Folder per supportare le cartelle offline.
title: Oggetto Folder2 (Shldisp.h)
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
ms.openlocfilehash: c2c630ef36f6e4b2b58f3902c3d5728a31ad1f0d
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842062"
---
# <a name="folder2-object"></a>Oggetto Folder2

Estende [**l'oggetto Folder**](folder.md) per supportare le cartelle offline.

## <a name="members"></a>Membri

**L'oggetto Folder2** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

**L'oggetto Folder2** dispone di questi metodi.



| Metodo                                                                 | Descrizione                                                                          |
|:-----------------------------------------------------------------------|:-------------------------------------------------------------------------------------|
| [**DismissedWebViewBarricade**](folder2-dismissedwebviewbarricade.md) | Chiamato in risposta alla barra di visualizzazione Web ignorata dall'utente.<br/> |
| [**Sincronizzare**](folder2-synchronize.md)                             | Sincronizza tutti i file offline nella cartella.<br/>                             |



 

### <a name="properties"></a>Proprietà

**L'oggetto Folder2** ha queste proprietà.



| Proprietà                                                                            | Tipo di accesso          | Descrizione                                                               |
|:------------------------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------|
| [**HaveToShowWebViewBarricade**](folder2-havetoshowwebviewbarricade.md)<br/> | Sola lettura<br/> | Non è attualmente supportato.<br/>                                       |
| [**OfflineStatus**](folder2-offlinestatus.md)<br/>                           | Sola lettura<br/> | Contiene lo stato offline della cartella.<br/>                     |
| [**stesso**](folder2-self.md)<br/>                                             | Sola lettura<br/> | Contiene l'oggetto [**FolderItem della**](folderitem.md) cartella.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, solo app desktop di Windows XP \[\]<br/>                                        |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2003 \[\]<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 5.0 o successiva)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Cartella**](folder.md)
</dt> </dl>

 

 




