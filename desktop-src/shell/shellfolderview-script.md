---
description: Contiene l'oggetto di scripting per la visualizzazione.
ms.assetid: 63a4e42f-3d24-493f-8801-fc09a7477401
title: Proprietà ShellFolderView. script (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView.Script
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 86926f2013dd78c2c6685163ae78f890c337a251
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233195"
---
# <a name="shellfolderviewscript-property"></a>Proprietà ShellFolderView. script

\[Questa proprietà non è supportata in Windows XP o versioni successive.\]

Contiene l'oggetto di scripting per la visualizzazione.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
objScript = ShellFolderView.Script
```



## <a name="property-value"></a>Valore proprietà

Variabile di tipo [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) che riceve l'oggetto di scripting.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, \[ solo app desktop Windows XP\]<br/>                                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                           |
| Intestazione<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 4,71 o successiva)</dt> </dl> |



 

 
