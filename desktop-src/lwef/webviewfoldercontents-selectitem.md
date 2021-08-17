---
title: Metodo WebViewFolderContents.SelectItem (Shldisp.h)
description: 'Metodo WebViewFolderContents.SelectItem: imposta lo stato di selezione di un elemento nella visualizzazione.'
ms.assetid: c0e163ee-1951-476c-807a-781e26766d99
keywords:
- Metodo SelectItem Funzionalità dell'Windows legacy
- Metodo SelectItem Legacy Windows Environment Features , oggetto WebViewFolderContents
- Oggetto WebViewFolderContents Legacy Windows Environment Features , metodo SelectItem
topic_type:
- apiref
api_name:
- WebViewFolderContents.SelectItem
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d144801e62962f4071b6c8e60147326908a9b4f7787e0d4ac549be9c51fa3c97
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119960621"
---
# <a name="webviewfoldercontentsselectitem-method"></a>Metodo WebViewFolderContents.SelectItem

Imposta lo stato di selezione di un elemento nella visualizzazione.

## <a name="syntax"></a>Sintassi


```JScript
WebViewFolderContents.SelectItem(
  vItem,
  dwFlags
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*vItem* \[ Pollici\]
</dt> <dd>

Tipo: **\* Variante**

Oggetto [**FolderItem**](../shell/folderitem.md) per il quale verrà impostato lo stato di selezione.

</dd> <dt>

*dwFlags* \[ Pollici\]
</dt> <dd>

Tipo: **Integer**

Set di flag che indicano il nuovo stato di selezione. Può trattarsi di uno o più dei valori seguenti.

<dt>



  (0)


</dt> <dd>

Deselezionare l'elemento.

</dd> <dt>



 (1)


</dt> <dd>

Selezionare l'elemento.

</dd> <dt>



 (3)


</dt> <dd>

Mettere l'elemento in modalità di modifica.

</dd> <dt>



 (4)


</dt> <dd>

Deselezionare tutti gli elementi, ad esempio l'elemento specificato.

</dd> <dt>



 (8)


</dt> <dd>

Assicurarsi che l'elemento sia visualizzato nella visualizzazione.

</dd> <dt>



 (16)


</dt> <dd>

Assegnare lo stato attivo all'elemento.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="examples"></a>Esempio

L'esempio seguente illustra l'uso corretto di questo metodo per JScript incorporato in HTML.


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsSelectItemJ()
    {
        var objFolderItem;

        objFolderItem = FileList.FocusedItem;
        if (objFolderItem != null)
        {
            FileList.SelectItem(objFolderItem, 1);
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



 

