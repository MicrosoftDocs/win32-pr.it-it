---
description: "Metodo ShellFolderView.PopupItemMenu: crea un menu di scelta rapida per l'elemento specificato e restituisce la stringa di comando selezionata."
title: Metodo ShellFolderView.PopupItemMenu (Shldisp.h)
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
ms.openlocfilehash: 7a2feda23d6e1759e1c0be27805fefbb6b592df7
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840752"
---
# <a name="shellfolderviewpopupitemmenu-method"></a>Metodo ShellFolderView.PopupItemMenu

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

*vItem* \[ Pollici\]
</dt> <dd>

Tipo: **Variante**

Oggetto [**FolderItem**](folderitem.md) per il quale verrà creato il menu di scelta rapida.

</dd> <dt>

*vx* \[ in, facoltativo\]
</dt> <dd>

Tipo: **Variante**

Posizione orizzontale del menu, in coordinate dello schermo.

</dd> <dt>

*vy* \[ in, facoltativo\]
</dt> <dd>

Tipo: **Variante**

Posizione verticale del menu, in coordinate dello schermo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)\***

Stringa **che** riceve la stringa di comando.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop di Windows 2000 Professional e Windows XP \[\]<br/>                                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                           |
| Intestazione<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 4.71 o successiva)</dt> </dl> |



 

 
