---
description: 'Metodo ShellFolderView.SelectItem: imposta lo stato di selezione di un elemento nella visualizzazione.'
title: Metodo ShellFolderView.SelectItem (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView.SelectItem
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 91c39d4c-56c3-4c2b-93e8-9f782ca0aa93
ms.openlocfilehash: c8cbff0da4da55d9621bfeb01f26c5ed62fe230a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116749"
---
# <a name="shellfolderviewselectitem-method"></a>Metodo ShellFolderView.SelectItem

Imposta lo stato di selezione di un elemento nella visualizzazione.

## <a name="syntax"></a>Sintassi


```JScript
ShellFolderView.SelectItem(
  vItem,
  dwFlags
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*vItem* \[ Pollici\]
</dt> <dd>

Tipo: **\* Variante**

Oggetto [**FolderItem**](folderitem.md) per il quale verrà impostato lo stato di selezione.

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

## <a name="remarks"></a>Commenti

[**FocusedItem**](shellfolderview-focuseditem.md) può essere chiamato solo nel sistema locale. Non funzionerà quando viene eseguito in una pagina Web tramite HTTP o UNC.

## <a name="examples"></a>Esempio

L'esempio seguente illustra l'uso corretto di questo metodo in JScript incorporato in HTML.


```JScript
<html>
<head>
<title></title>

<script language="JavaScript">
    function fnShellFolderViewSelectItemJ()
    {
        var objFolder;
        
        objFolder = WebOC.Document.Folder;
        if (objFolder != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder.Self;
            if (objFolderItem != null)
            {
                WebOC.Document.SelectItem(objFolderItem, 16);
                alert("item selected");
            }
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
<INPUT id=SelectItem 
       type=button 
       value=SelectItem 
       name=SelectItem 
       onclick="fnShellFolderViewSelectItemJ()">
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



 

 




