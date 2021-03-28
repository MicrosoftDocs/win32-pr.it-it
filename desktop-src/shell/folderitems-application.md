---
description: Contiene l'oggetto applicazione della raccolta di elementi cartella.
ms.assetid: 2cd4243e-a5a6-4de4-b310-f74558ac0fbe
title: Proprietà FolderItems. Application (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItems.Application
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 7f073b81106923f889ca5209c0aa492f4c4bbd60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127839"
---
# <a name="folderitemsapplication-property"></a>Proprietà FolderItems. Application

Contiene l'oggetto **applicazione** della raccolta di elementi cartella.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
objApplication = FolderItems.Application
```



## <a name="property-value"></a>Valore proprietà

Riferimento all'oggetto applicazione.

## <a name="remarks"></a>Commenti

La proprietà dell' **applicazione** restituisce l'oggetto di automazione supportato dall'applicazione che contiene il controllo WebBrowser, se tale oggetto è accessibile. In caso contrario, questa proprietà restituisce l'oggetto di automazione del controllo WebBrowser.

Utilizzare questa proprietà con i comandi **set** e **CreateObject** oppure con il comando **GetObject** per creare e modificare un'istanza dell'applicazione Windows Internet Explorer.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, \[ solo app desktop Windows XP\]<br/>                                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                           |
| Intestazione<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 4,71 o successiva)</dt> </dl> |



 

 




