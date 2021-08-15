---
description: Recupera un oggetto FolderItems che rappresenta la raccolta di elementi nella cartella.
ms.assetid: ef2965ec-c8ab-4108-8e5e-b4fd5370521a
title: Metodo Folder.Items (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.Items
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: e698c74cd8cc04265ef75e01062f8aa05171f660f5cf5eb7253d04d3397ed984
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119093135"
---
# <a name="folderitems-method"></a>Metodo Folder.Items

Recupera un [**oggetto FolderItems**](folderitems.md) che rappresenta la raccolta di elementi nella cartella.

## <a name="syntax"></a>Sintassi


```JScript
retVal = Folder.Items()
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **[ **FolderItems**](folderitems.md)\*\***

Riferimento all'oggetto [**FolderItems.**](folderitems.md)

## <a name="remarks"></a>Commenti

> [!Note]  
> Non tutti i metodi vengono implementati per tutte le cartelle. Ad esempio, il [**metodo ParseName**](folder-parsename.md) non viene implementato per la cartella Pannello di controllo (CSIDL \_ CONTROLS). Se si tenta di chiamare un metodo non implementato, viene generato un errore 0x800A01BD (decimale 445).

 

## <a name="examples"></a>Esempio

Nell'esempio seguente **viene utilizzato Items** per determinare il numero di elementi nella cartella C: \\ Windows. Viene visualizzato un utilizzo appropriato per JScript, VBScript e Visual Basic.

JScript:


```JScript
<script language="JScript">
    function fnFolderObjectItemsJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder = new Object;
        
        objFolder = objShell.NameSpace("C:\\WINDOWS");
        if (objFolder != null)
        {
            var objFolderItems = new Object;
            
            objFolderItems = objFolder.Items();
            if (objFolderItems != null)
            {
                document.write (objFolderItems.Count);
            }
        }
    }
</script>
```



Vbscript:


```VB
<script language="VBScript">
    function fnFolderObjectItemsVB()
        dim objShell
        dim objFolder
        
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace("C:\WINDOWS")

        if (not objFolder is nothing) then
            dim objFolderItems

            set objFolderItems = objFolder.Items

            if (not objFolderItems Is Nothing) then
                document.write objFolderItems.Count
            end if

            set objFolderItem = nothing
        end if

        set objFolder = nothing
        set objShell = nothing
    end function
</script>
```



Visual Basic:


```VB
Private Sub btnFolderObjectItems_Click()
    Dim objShell  As Shell
    Dim objFolder As Folder

    Set objShell = New Shell
    Set objFolder = objShell.NameSpace("C:\WINDOWS")

    If (Not objFolder Is Nothing) Then
        Dim objFolderItems As FolderItems

        Set objFolderItems = objFolder.Items()

        If (Not objFolderItems Is Nothing) Then
            Dim vCount As Variant

            vCount = objFolderItems.Count
        End If

        Set objFolderItems = Nothing
    End If

    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, Windows solo app desktop XP \[\]<br/>                                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                           |
| Intestazione<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 4.71 o successiva)</dt> </dl> |



 

 




