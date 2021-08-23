---
title: Proprietà WebViewFolderContents.ViewOptions (Shldisp.h)
description: Ottiene un set di flag ShellFolderViewOptions che indicano le opzioni correnti della visualizzazione.
ms.assetid: 96edb144-e532-4ab5-99ae-d945e211d744
keywords:
- Proprietà ViewOptions Funzionalità dell'Windows legacy
- Proprietà ViewOptions Legacy Windows Environment Features , oggetto WebViewFolderContents
- Oggetto WebViewFolderContents Legacy Windows Environment Features , proprietà ViewOptions
topic_type:
- apiref
api_name:
- WebViewFolderContents.ViewOptions
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95c897c75eab32962a18981c605c8465630aaf7b0c6b7d3e3f9a4fbe8e3d75d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119607741"
---
# <a name="webviewfoldercontentsviewoptions-property"></a>WebViewFolderContents.ViewOptions - proprietà

Ottiene un set di [**flag ShellFolderViewOptions**](/windows/desktop/api/shldisp/ne-shldisp-shellfolderviewoptions) che indicano le opzioni correnti della visualizzazione.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
objViewOptions = WebViewFolderContents.ViewOptions
```



## <a name="property-value"></a>Valore proprietà

Variabile di tipo [IDispatch che riceve](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) l'oggetto delle opzioni di visualizzazione.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato l'utilizzo corretto di questa proprietà JScript incorporato in HTML.


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsViewOptionsJ()
    {
        var nViewOptions;

        nViewOptions = FileList.ViewOptions;
        if (nViewOptions != "")
        {
            alert(nViewOptions);
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
| Client minimo supportato<br/> | Windows 2000 Professional, Windows solo app desktop XP \[\]<br/>                                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                           |
| Intestazione<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 4.71 o successiva)</dt> </dl> |



 

