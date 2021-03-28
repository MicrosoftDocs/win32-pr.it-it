---
description: Invia gli eventi dell'oggetto ShellFolderView specificato al gestore eventi ShellFolderViewOC corrispondente.
ms.assetid: 44a2a0a5-aa87-43ae-b4ea-0d301fcb8464
title: Metodo ShellFolderViewOC. SetFolderView (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderViewOC.SetFolderView
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 7d331fadbd8abae62ee896caec772d84d079f88d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980423"
---
# <a name="shellfolderviewocsetfolderview-method"></a>ShellFolderViewOC. SetFolderView, metodo

Invia gli eventi dell'oggetto [**ShellFolderView**](shellfolderview.md) specificato al gestore eventi [**ShellFolderViewOC**](shellfolderviewoc-object.md) corrispondente.

## <a name="syntax"></a>Sintassi


```JScript
iRetVal = ShellFolderViewOC.SetFolderView(
  oShellFolderView
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*oShellFolderView* \[ in\]
</dt> <dd>

Tipo: **[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) \** _

Oggetto [_ *ShellFolderView* *](shellfolderview.md) . Gli eventi [**EnumDone**](shellfolderviewoc-enumdone.md) e [**SelectionChanged**](shellfolderview-selectionchanged.md) verranno trasmessi al gestore eventi [**ShellFolderViewOC**](shellfolderviewoc-object.md) corrispondente.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, \[ solo app desktop Windows XP\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 5,0 o successiva)</dt> </dl> |



 

 
