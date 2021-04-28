---
title: Metodo WebViewFolderContents.PopupItemMenu (Shldisp.h)
description: "Metodo WebViewFolderContents.PopupItemMenu: crea un menu di scelta rapida per l'elemento specificato e restituisce la stringa di comando selezionata."
ms.assetid: 3c07500c-2fe9-4976-a1a8-b128e75f9325
keywords:
- Metodo PopupItemMenu Funzionalità legacy dell'ambiente Windows
- Metodo PopupItemMenu Funzionalità legacy dell'ambiente Windows, oggetto WebViewFolderContents
- Oggetto WebViewFolderContents Funzionalità legacy dell'ambiente Windows, metodo PopupItemMenu
topic_type:
- apiref
api_name:
- WebViewFolderContents.PopupItemMenu
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c879e10097b334f0c2d4f98b1b76289d20ee4a93
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102639"
---
# <a name="webviewfoldercontentspopupitemmenu-method"></a>Metodo WebViewFolderContents.PopupItemMenu

Crea un menu di scelta rapida per l'elemento specificato e restituisce la stringa di comando selezionata.

## <a name="syntax"></a>Sintassi


```JScript
retVal = WebViewFolderContents.PopupItemMenu(
  vItem,
  [ vx ],
  [ vy ]
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*vItem* \[ Pollici\]
</dt> <dd>

Tipo: **Variant**

Oggetto [**FolderItem**](../shell/folderitem.md) per il quale verrà creato il menu di scelta rapida.

</dd> <dt>

*vx* \[ in, facoltativo\]
</dt> <dd>

Tipo: **Variant**

Posizione orizzontale del menu, in coordinate dello schermo.

</dd> <dt>

*vy* \[ in, facoltativo\]
</dt> <dd>

Tipo: **Variante**

Posizione verticale del menu, in coordinate dello schermo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[BSTR](/previous-versions/windows/desktop/automat/bstr)\***

Quando questo metodo viene restituito, contiene la stringa di comando.

## <a name="examples"></a>Esempio

L'esempio seguente illustra l'uso corretto **di PopupItemMenu** per JScript incorporato in HTML.


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsPopupItemMenuJ()
    {
        var objFolderItem;

        objFolderItem = FileList.FocusedItem;
        if (objFolderItem != null)
        {
            var szCommand;

            szCommand = FileList.PopupItemMenu(objFolderItem);
        }
    }
</script>

</head>
<body>

...

<object id=FileList classid="clsid:1820FED0-473E-11D0-A96C-00C04FD705A2" tabIndex=1>
</body>
</html>
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, solo app desktop di Windows XP \[\]<br/>                                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                           |
| Intestazione<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 4.71 o successiva)</dt> </dl> |



 

