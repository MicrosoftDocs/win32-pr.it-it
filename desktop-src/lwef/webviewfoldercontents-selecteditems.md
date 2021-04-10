---
title: Metodo WebViewFolderContents.SelectedItems (Shldisp.h)
description: Ottiene un oggetto FolderItems che rappresenta tutti gli elementi selezionati nella visualizzazione.
ms.assetid: 683acac4-f157-4a75-a3f8-c693887c1ea5
keywords:
- Funzionalità dell'ambiente Windows legacy del Metodo SelectedItems
- Funzionalità dell'ambiente Windows legacy del Metodo SelectedItems, oggetto WebViewFolderContents
- Funzionalità dell'ambiente Windows legacy dell'oggetto WebViewFolderContents, Metodo SelectedItems
topic_type:
- apiref
api_name:
- WebViewFolderContents.SelectedItems
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cee4b7f34cdcabec637671af79775fc1fa546790
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048673"
---
# <a name="webviewfoldercontentsselecteditems-method"></a>WebViewFolderContents. SelectedItems (metodo)

Ottiene un oggetto [**FolderItems**](../shell/folderitems.md) che rappresenta tutti gli elementi selezionati nella visualizzazione.

## <a name="syntax"></a>Sintassi


```JScript
retVal = WebViewFolderContents.SelectedItems()
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **[ **FolderItems**](../shell/folderitems.md)\*\***

Riferimento all'oggetto [**FolderItems**](../shell/folderitems.md) .

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato l'utilizzo corretto di questo metodo per JScript incorporato in HTML.


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsSelectedItemsJ()
    {
        var objFolderItems;

        objFolderItems = FileList.SelectedItems();
        if (objFolderItems != null)
        {
            alert(objFolderItems.Count);
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



 

