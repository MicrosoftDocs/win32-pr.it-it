---
description: Contiene l'oggetto Applicazione dell'elemento cartella.
ms.assetid: cd8d6dea-1d16-4d62-b56b-c915192f730b
title: Proprietà FolderItem.Application (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItem.Application
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 684edfbcd830cd0e2f6b70162d045c1f8035dc7e4477ace1c39220bc076215cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117860238"
---
# <a name="folderitemapplication-property"></a>FolderItem.Application - proprietà

Contiene **l'oggetto Applicazione** dell'elemento cartella.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
objApplication = FolderItem.Application
```



## <a name="property-value"></a>Valore proprietà

Variabile di tipo [**IDispatch che**](/windows/win32/api/oaidl/nn-oaidl-idispatch) riceve l'oggetto Application. 

## <a name="remarks"></a>Commenti

La **proprietà Application** restituisce l'oggetto di automazione supportato dall'applicazione che contiene il controllo WebBrowser, se tale oggetto è accessibile. In caso contrario, questa proprietà restituisce l'oggetto di automazione del controllo WebBrowser.

Usare questa proprietà con i **comandi Set** e **CreateObject** o con il **comando GetObject** per creare e modificare un'istanza dell Windows Internet Explorer appliata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, Windows solo app desktop XP \[\]<br/>                                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                           |
| Intestazione<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 4.71 o successiva)</dt> </dl> |



 

 
