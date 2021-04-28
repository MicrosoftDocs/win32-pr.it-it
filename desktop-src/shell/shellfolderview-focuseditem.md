---
description: "Proprietà ShellFolderView.FocusedItem: ottiene un oggetto FolderItem che rappresenta l'elemento con lo stato attivo per l'input."
ms.assetid: ca88801d-c8fa-4c1c-9294-f52eada40ff6
title: Proprietà ShellFolderView.FocusedItem (Shldisp.h)
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
ms.openlocfilehash: 4f661f555f1492a3323fa3749a8dffd6f00f411d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104009"
---
# <a name="shellfolderviewfocuseditem-property"></a>ShellFolderView.FocusedItem - proprietà

Ottiene un [**oggetto FolderItem**](folderitem.md) che rappresenta l'elemento con lo stato attivo per l'input.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
objFocusedItem = ShellFolderView.FocusedItem
```



## <a name="property-value"></a>Valore proprietà

Variabile di tipo [**IDispatch che**](/windows/win32/api/oaidl/nn-oaidl-idispatch) riceve l'oggetto elemento con lo stato attivo.

## <a name="remarks"></a>Commenti

**FocusedItem** può essere chiamato solo nel sistema locale. Non funzionerà quando viene eseguito in una pagina Web tramite HTTP o UNC.

## <a name="examples"></a>Esempio

L'esempio seguente illustra l'uso corretto di questo metodo in JScript incorporato in HTML.


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
| Client minimo supportato<br/> | Windows 2000 Professional, solo app desktop di Windows XP \[\]<br/>                                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                           |
| Intestazione<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 4.71 o successiva)</dt> </dl> |



 

 
