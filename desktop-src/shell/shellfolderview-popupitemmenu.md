---
description: Crea un menu di scelta rapida per l'elemento specificato e restituisce la stringa di comando selezionata.
title: Metodo ShellFolderView. PopupItemMenu (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView.PopupItemMenu
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 1610d91e-87c3-4ba5-9147-1595eddb2c3a
ms.openlocfilehash: 513f654442361da840cb02089810c814275c5867
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233196"
---
# <a name="shellfolderviewpopupitemmenu-method"></a>ShellFolderView. PopupItemMenu, metodo

Crea un menu di scelta rapida per l'elemento specificato e restituisce la stringa di comando selezionata.

## <a name="syntax"></a>Sintassi


```JScript
retVal = ShellFolderView.PopupItemMenu(
  vItem,
  [ vx ],
  [ vy ]
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*vite* \[ in\]
</dt> <dd>

Tipo: **Variant**

Oggetto [**FolderItem**](folderitem.md) per il quale verrà creato il menu di scelta rapida.

</dd> <dt>

*VX* \[ in, facoltativo\]
</dt> <dd>

Tipo: **Variant**

Posizione orizzontale del menu, in coordinate dello schermo.

</dd> <dt>

stato del  \[ in, facoltativo\]
</dt> <dd>

Tipo: **Variant**

Posizione verticale del menu, in coordinate dello schermo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr) \** _

_ *Stringa** che riceve la stringa di comando.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, \[ solo app desktop Windows XP\]<br/>                                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                           |
| Intestazione<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 4,71 o successiva)</dt> </dl> |



 

 
