---
description: Ottiene un oggetto FolderItem che rappresenta l'elemento con lo stato attivo per l'input.
ms.assetid: ca88801d-c8fa-4c1c-9294-f52eada40ff6
title: Proprietà ShellFolderView. FocusedItem (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView.FocusedItem
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 26f0f24cddd3b9299ec70b41160579659c71b5bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233201"
---
# <a name="shellfolderviewfocuseditem-property"></a>Proprietà ShellFolderView. FocusedItem

Ottiene un oggetto [**FolderItem**](folderitem.md) che rappresenta l'elemento con lo stato attivo per l'input.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
objFocusedItem = ShellFolderView.FocusedItem
```



## <a name="property-value"></a>Valore proprietà

Variabile di tipo [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) che riceve l'oggetto elemento con lo stato attivo.

## <a name="remarks"></a>Commenti

**FocusedItem** può essere chiamato solo sul sistema locale. Non funzionerà se eseguita in una pagina Web su HTTP o UNC.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato l'utilizzo corretto di questo metodo in JScript incorporato in HTML.


```JScript
<html>
<head>
<title></title>

<script language="JavaScript">
    function fnShellFolderViewFocusedItemJ()
    {
        var objFolderItem;
        
        objFolderItem = WebOC.Document.FocusedItem;
        if (objFolderItem != null)
        {
            alert("Got FolderItem object.");
        }
    }
    
    function fnLoad()
    {
        var webOC;
        
        webOC = document.all("WebOC");
        webOC.Navigate("C:\\");
    }
</script>

</head>
<body onload="fnLoad()">
<object id="WebOC"
        classid="clsid:8856F961-340A-11D0-A96B-00C04FD705A2"
        width=400
        height=400>
</object>
<br><br>
<INPUT id=FocusedItem 
       type=button 
       value=FocusedItem 
       name=FocusedItem 
       onclick="fnShellFolderViewFocusedItemJ()">
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



 

 
