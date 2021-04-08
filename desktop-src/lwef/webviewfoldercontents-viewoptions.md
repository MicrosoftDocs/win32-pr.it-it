---
title: Proprietà WebViewFolderContents. ViewOptions (shldisp. h)
description: Ottiene un set di flag ShellFolderViewOptions che indicano le opzioni correnti della visualizzazione.
ms.assetid: 96edb144-e532-4ab5-99ae-d945e211d744
keywords:
- Funzionalità dell'ambiente Windows legacy della proprietà ViewOptions
- Proprietà ViewOptions ambiente Windows legacy funzionalità, oggetto WebViewFolderContents
- Funzionalità dell'ambiente Windows legacy dell'oggetto WebViewFolderContents, proprietà ViewOptions
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
ms.openlocfilehash: 737ec5cb22fdc5c0002006898b837b557b5f6089
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047950"
---
# <a name="webviewfoldercontentsviewoptions-property"></a>Proprietà WebViewFolderContents. ViewOptions

Ottiene un set di flag [**ShellFolderViewOptions**](/windows/desktop/api/shldisp/ne-shldisp-shellfolderviewoptions) che indicano le opzioni correnti della visualizzazione.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
objViewOptions = WebViewFolderContents.ViewOptions
```



## <a name="property-value"></a>Valore proprietà

Variabile di tipo [IDispatch](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) che riceve l'oggetto opzioni di visualizzazione.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato l'utilizzo corretto di questa proprietà in JScript incorporato in HTML.


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
| Client minimo supportato<br/> | Windows 2000 Professional, \[ solo app desktop Windows XP\]<br/>                                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                           |
| Intestazione<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 4,71 o successiva)</dt> </dl> |



 

