---
description: Contiene un oggetto che rappresenta un'applicazione.
ms.assetid: 61B85691-399D-41c1-9901-825345A38E5A
title: Proprietà IShellDispatch.Application (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.Application
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 5fbdbd8b2cc847a1b06a316d6f8caebfe1e2e5e4fc79fc4be2ff2ebdb8ee3912
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119443321"
---
# <a name="ishelldispatchapplication-property"></a>Proprietà IShellDispatch.Application

Contiene un oggetto che rappresenta un'applicazione.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
objApplication = IShellDispatch.Application
```


```VB

Property Application As Object
```





## <a name="property-value"></a>Valore proprietà

Variabile di tipo [**IDispatch che**](/windows/win32/api/oaidl/nn-oaidl-idispatch) riceve l'oggetto applicazione.

## <a name="remarks"></a>Commenti

Questa proprietà viene implementata e accessibile tramite la [**proprietà Shell.EjectPC.**](shell-ejectpc.md)

La **proprietà Application** restituisce l'oggetto di automazione supportato dall'applicazione che contiene il controllo WebBrowser, se tale oggetto è accessibile. In caso contrario, questa proprietà restituisce l'oggetto di automazione del controllo WebBrowser.

Usare questa proprietà con i **comandi Set** e **CreateObject** o con il **comando GetObject** per creare e modificare un'istanza dell Windows Internet Explorer app.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, Windows solo app desktop XP \[\]<br/>                                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                           |
| Intestazione<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 4.71 o successiva)</dt> </dl> |



 

 
