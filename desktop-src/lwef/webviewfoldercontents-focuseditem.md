---
title: Proprietà WebViewFolderContents. FocusedItem (shldisp. h)
description: Ottiene un oggetto FolderItem che rappresenta l'elemento con lo stato attivo per l'input.
ms.assetid: 84cf92ac-dadb-4741-8383-a8ae1d35d4e0
keywords:
- Funzionalità dell'ambiente Windows legacy della proprietà FocusedItem
- Proprietà FocusedItem ambiente Windows legacy funzionalità, oggetto WebViewFolderContents
- Funzionalità dell'ambiente Windows legacy dell'oggetto WebViewFolderContents, proprietà FocusedItem
topic_type:
- apiref
api_name:
- WebViewFolderContents.FocusedItem
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 050e7c2a4c280a949ec3684e2b05610830315a37
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400266"
---
# <a name="webviewfoldercontentsfocuseditem-property"></a>Proprietà WebViewFolderContents. FocusedItem

Ottiene un oggetto [**FolderItem**](../shell/folderitem.md) che rappresenta l'elemento con lo stato attivo per l'input.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
objFocusedItem = WebViewFolderContents.FocusedItem
```



## <a name="property-value"></a>Valore proprietà

Variabile di tipo [IDispatch](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) che riceve l'oggetto elemento con lo stato attivo.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato l'utilizzo corretto di questa proprietà in JScript incorporato in HTML.


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsFocusedItemJ()
    {
        var objFolderItem;

        objFolderItem = FileList.FocusedItem;
        if (objFolderItem != null)
        {
            alert(objFolderItem.Name);
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



 

