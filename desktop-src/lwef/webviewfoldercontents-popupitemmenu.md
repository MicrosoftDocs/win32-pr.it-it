---
title: Metodo WebViewFolderContents.PopupItemMenu (Shldisp.h)
description: "Metodo WebViewFolderContents.PopupItemMenu: crea un menu di scelta rapida per l'elemento specificato e restituisce la stringa di comando selezionata."
ms.assetid: 3c07500c-2fe9-4976-a1a8-b128e75f9325
keywords:
- Metodo PopupItemMenu Funzionalità Windows'ambiente legacy
- Metodo PopupItemMenu Legacy Windows Environment Features , oggetto WebViewFolderContents
- Oggetto WebViewFolderContents Legacy Windows Environment Features , metodo PopupItemMenu
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
ms.openlocfilehash: 274237b2a17aa3e891f0c65f139cc7b251c1ff8a78b1f0ad387fb2931c8e3107
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035969"
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

Tipo: **Variant**

Posizione verticale del menu, in coordinate dello schermo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[BSTR](/previous-versions/windows/desktop/automat/bstr)\***

Quando questo metodo viene restituito, contiene la stringa di comando.

## <a name="examples"></a>Esempio

L'esempio seguente illustra l'uso corretto di **PopupItemMenu** per JScript incorporato in HTML.


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
| Client minimo supportato<br/> | Windows 2000 Professional, Windows solo app \[ desktop XP\]<br/>                                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                           |
| Intestazione<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 4.71 o successiva)</dt> </dl> |



 

