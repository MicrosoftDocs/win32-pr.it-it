---
title: Metodo WebViewFolderContents. SelectItem (shldisp. h)
description: Imposta lo stato di selezione di un elemento nella visualizzazione.
ms.assetid: c0e163ee-1951-476c-807a-781e26766d99
keywords:
- Funzionalità dell'ambiente Windows legacy del metodo SelectItem
- Funzionalità dell'ambiente Windows legacy del metodo SelectItem, oggetto WebViewFolderContents
- Funzionalità dell'ambiente Windows legacy dell'oggetto WebViewFolderContents, metodo SelectItem
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
ms.openlocfilehash: e491fb27db2d6e1e9b449be4aa2924684021539a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301033"
---
# <a name="webviewfoldercontentsselectitem-method"></a>WebViewFolderContents. SelectItem, metodo

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

*vite* \[ in\]
</dt> <dd>

Tipo: **Variant \** _

Oggetto [_ *FolderItem* *](../shell/folderitem.md) per il quale verrà impostato lo stato di selezione.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Tipo: **Integer**

Set di flag che indicano il nuovo stato di selezione. Può corrispondere a uno o più dei valori seguenti.

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

Inserire l'elemento in modalità di modifica.

</dd> <dt>



 (4)


</dt> <dd>

Deseleziona tutto tranne l'elemento specificato.

</dd> <dt>



 (8)


</dt> <dd>

Verificare che l'elemento sia visualizzato nella visualizzazione.

</dd> <dt>



 (16)


</dt> <dd>

Assegnare all'elemento lo stato attivo.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato l'utilizzo corretto di questo metodo per JScript incorporato in HTML.


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
| Client minimo supportato<br/> | Windows 2000 Professional, \[ solo app desktop Windows XP\]<br/>                                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                           |
| Intestazione<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 4,71 o successiva)</dt> </dl> |



 

