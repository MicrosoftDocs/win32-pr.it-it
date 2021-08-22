---
description: Inoltra gli eventi dell'oggetto ShellFolderView specificato al gestore eventi ShellFolderViewOC corrispondente.
ms.assetid: 44a2a0a5-aa87-43ae-b4ea-0d301fcb8464
title: Metodo ShellFolderViewOC.SetFolderView (Shldisp.h)
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
ms.openlocfilehash: 41a37d1b8f9874bdddd5a9593e0eade8bc0b5b92d30f8ada4ee9c6295af1d632
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968400"
---
# <a name="shellfolderviewocsetfolderview-method"></a>Metodo ShellFolderViewOC.SetFolderView

Inoltra gli eventi dell'oggetto [**ShellFolderView**](shellfolderview.md) specificato al gestore eventi [**ShellFolderViewOC**](shellfolderviewoc-object.md) corrispondente.

## <a name="syntax"></a>Sintassi


```JScript
iRetVal = ShellFolderViewOC.SetFolderView(
  oShellFolderView
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*oShellFolderView* \[ Pollici\]
</dt> <dd>

Tipo: **[ **IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\***

Oggetto [**ShellFolderView.**](shellfolderview.md) Gli [**eventi EnumDone**](shellfolderviewoc-enumdone.md) [**e SelectionChanged**](shellfolderview-selectionchanged.md) verranno inoltrati al gestore eventi [**ShellFolderViewOC**](shellfolderviewoc-object.md) corrispondente.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, Windows solo app desktop XP \[\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 5.0 o successiva)</dt> </dl> |



 

 
