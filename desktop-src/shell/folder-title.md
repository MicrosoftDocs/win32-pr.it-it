---
description: Contiene il titolo della cartella.
ms.assetid: 95c064ff-4504-4e9c-80ac-47beca443ad4
title: Proprietà Folder. title (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.Title
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 8fc66d231d49d724749ae79b248b4dca9d917acc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979682"
---
# <a name="foldertitle-property"></a>Proprietà Folder. title

Contiene il titolo della cartella.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
strTitle = Folder.Title
```



## <a name="property-value"></a>Valore proprietà

Stringa che contiene il titolo dell'oggetto.

## <a name="remarks"></a>Commenti

> [!Note]  
> Non tutti i metodi sono implementati per tutte le cartelle. Il metodo [**ParseName**](folder-parsename.md) , ad esempio, non è implementato per la cartella del pannello di controllo ( \_ controlli CSIDL). Se si tenta di chiamare un metodo non implementato, viene generato un errore 0x800A01BD (decimale 445).

 

## <a name="examples"></a>Esempio

Nell'esempio seguente viene usato **title** per recuperare il titolo della cartella che contiene i gruppi di programmi dell'utente (in genere "programmi"). L'utilizzo corretto viene visualizzato per JScript, VBScript e Visual Basic.

JScript


```JScript
<script language="JScript">
    function fnFolderTitleJ()
    {
        var objShell    = new ActiveXObject("shell.application");
        var objFolder;
        var ssfPROGRAMS = 2;
        
        objFolder = objShell.NameSpace(ssfPROGRAMS);
        if (objFolder != null)
        {
            alert(objFolder.Title);
        }
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnFolderTitleVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder
            dim ssfPROGRAMS
            
            ssfPROGRAMS = 2
            set objFolder = objShell.NameSpace(ssfPROGRAMS)
            if (not objFolder is nothing) then
                alert(objFolder.Title)
            end if
            set objFolder = nothing
        end if
        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnFolderTitleVB()
    Dim objShell    As Shell
    Dim objFolder   As Folder
    Dim ssfPROGRAMS As Long
            
    ssfPROGRAMS = 2
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfPROGRAMS)
    If (Not objFolder Is Nothing) Then
        Debug.Print objFolder.Title
    End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, \[ solo app desktop Windows XP\]<br/>                                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                           |
| Intestazione<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 4,71 o successiva)</dt> </dl> |



 

 




