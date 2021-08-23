---
title: Proprietà WebViewFolderContents.Folder (Shldisp.h)
description: 'Proprietà WebViewFolderContents.Folder: ottiene un oggetto Folder che rappresenta la visualizzazione.'
ms.assetid: 1d81c27a-1e48-4c0a-b74d-c63af43a909d
keywords:
- Proprietà Cartella Funzionalità dell'Windows legacy
- Proprietà Folder Legacy Windows Environment Features , oggetto WebViewFolderContents
- Oggetto WebViewFolderContents Legacy Windows Environment Features , Proprietà Folder
topic_type:
- apiref
api_name:
- WebViewFolderContents.Folder
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af475d55351d9278ca954a9ebb896ef03928538b9984a2f87478ed3358a1741e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119607841"
---
# <a name="webviewfoldercontentsfolder-property"></a>Proprietà WebViewFolderContents.Folder

Ottiene un [**oggetto Folder**](../shell/folder.md) che rappresenta la visualizzazione.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
Folder = WebViewFolderContents.Folder
```



## <a name="property-value"></a>Valore proprietà

Oggetto che riceve [**l'oggetto**](../shell/folder.md) Folder.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato l'utilizzo corretto di questa proprietà JScript incorporato in HTML.


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsFolderJ()
    {
        var objFolder;

        objFolder = FileList.Folder;
        if (objFolder != null)
        {
            alert(objFolder.Title);
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



 

