---
title: Metodo WebViewFolderContents. PopupItemMenu (shldisp. h)
description: Crea un menu di scelta rapida per l'elemento specificato e restituisce la stringa di comando selezionata.
ms.assetid: 3c07500c-2fe9-4976-a1a8-b128e75f9325
keywords:
- Funzionalità dell'ambiente Windows legacy del metodo PopupItemMenu
- Funzionalità dell'ambiente Windows legacy del metodo PopupItemMenu, oggetto WebViewFolderContents
- Funzionalità dell'ambiente Windows legacy dell'oggetto WebViewFolderContents, metodo PopupItemMenu
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
ms.openlocfilehash: 41753814f103998185acc798a37447f22356d2aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740127"
---
# <a name="webviewfoldercontentspopupitemmenu-method"></a>WebViewFolderContents. PopupItemMenu, metodo

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

*vite* \[ in\]
</dt> <dd>

Tipo: **Variant**

Oggetto [**FolderItem**](../shell/folderitem.md) per il quale verrà creato il menu di scelta rapida.

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

Tipo: **[BSTR](/previous-versions/windows/desktop/automat/bstr) \** _

Quando termina, questo metodo contiene la stringa di comando.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato l'uso corretto di _ *PopupItemMenu** per JScript incorporato in HTML.


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
| Client minimo supportato<br/> | Windows 2000 Professional, \[ solo app desktop Windows XP\]<br/>                                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                           |
| Intestazione<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 4,71 o successiva)</dt> </dl> |



 

