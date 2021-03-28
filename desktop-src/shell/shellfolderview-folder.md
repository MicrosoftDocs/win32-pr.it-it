---
description: Ottiene un oggetto cartella che rappresenta la visualizzazione.
ms.assetid: 8f3e7827-f2a0-4ce9-b3e9-e6316ec58863
title: Proprietà ShellFolderView. Folder (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView.Folder
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 40590064048ba5410dc9341791aec443f16d68e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233199"
---
# <a name="shellfolderviewfolder-property"></a>Proprietà ShellFolderView. Folder

Ottiene un oggetto [**cartella**](folder.md) che rappresenta la visualizzazione.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
Folder = ShellFolderView.Folder
```



## <a name="property-value"></a>Valore proprietà

Oggetto che riceve l'oggetto [**cartella**](folder.md) .

## <a name="remarks"></a>Commenti

La **cartella** può essere chiamata solo sul sistema locale. Non funzionerà se eseguita in una pagina Web su HTTP o UNC.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato l'utilizzo corretto di questa proprietà per JScript incorporato in HTML.


```JScript
<html>
<head>
<title></title>

<script language="JavaScript">
    function fnShellFolderViewFolderJ()
    {
        var objFolder;
        
        objFolder = WebOC.Document.Folder;
        if (objFolder != null)
        {
            alert("Got Folder object");
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
        height=400 VIEWASTEXT>
</object>
<br><br>
<INPUT id=Folder 
       type=button 
       value=Folder 
       name=Folder 
       onclick="fnShellFolderViewFolderJ()">
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



 

 




