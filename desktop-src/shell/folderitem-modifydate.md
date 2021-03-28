---
description: Per un file, imposta o ottiene la data e l'ora dell'Ultima modifica apportata. Per una cartella, recupera la data e l'ora dell'Ultima modifica apportata a una cartella, ma non la imposta.
ms.assetid: bb60c800-863b-469b-b937-9816b8b338bf
title: Proprietà FolderItem. ModifyDate (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItem.ModifyDate
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: b9ea5fa6b611a0311840507fb2068d08801a5bfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127850"
---
# <a name="folderitemmodifydate-property"></a>Proprietà FolderItem. ModifyDate

Per un file, imposta o ottiene la data e l'ora dell'Ultima modifica apportata. Per una cartella, recupera la data e l'ora dell'Ultima modifica apportata a una cartella, ma non la imposta.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```JScript
iModifyDate = FolderItem.ModifyDate
FolderItem.ModifyDate = iModifyDate
```



## <a name="property-value"></a>Valore proprietà

**Data** che specifica o riceve la data e l'ora dell'Ultima modifica apportata all'elemento.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene usato **ModifyDate** per recuperare la data dell'Ultima modifica del blocco note e quindi reimpostarla su un tempo molto lungo. L'utilizzo corretto viene visualizzato per JScript, VBScript e Visual Basic.

JScript


```JScript
<script language="JScript">
    function fnModifyDateGetSetJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder2;
        var ssfWINDOWS = 36;
        
        objFolder2 = objShell.NameSpace(ssfWINDOWS);
        if (objFolder2 != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder2.ParseName("NOTEPAD.EXE");
            if (objFolderItem != null)
            {
                var szReturn;
                
                szReturn = objFolderItem.ModifyDate;
                objFolderItem.ModifyDate = "01/01/1900 6:05:00 PM";
            }
        }
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnModifyDateGetSetVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder2
            dim ssfWINDOWS
                
            ssfWINDOWS = 36
            set objFolder2 = objShell.NameSpace(ssfWINDOWS)
            if (not objFolder2 is nothing) then
                dim objFolderItem
                        
                set objFolderItem = objFolder2.ParseName("NOTEPAD.EXE")
                if (not objFolderItem is nothing) then
                    dim szReturn
                                
                    szReturn = objFolderItem.ModifyDate
                    objFolderItem.ModifyDate = "01/01/1900 6:05:00 PM"
                end if
                set objFolderItem = nothing
            end if
            set objFolder2 = nothing
        end if
        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnModifyDateGetSetVB()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2
    Dim ssfWINDOWS As Long
    
    ssfWINDOWS = 36
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace(ssfWINDOWS)
        If (Not objFolder2 Is Nothing) Then
            Dim objFolderItem As FolderItem
            
            Set objFolderItem = objFolder2.ParseName("NOTEPAD.EXE")
                If (Not objFolderItem Is Nothing) Then
                    Dim szReturn As String
                    
                    szReturn = objFolderItem.ModifyDate
                    objFolderItem.ModifyDate = "01/01/1900 6:05:00 PM"
                Else
                    'FolderItem object returned nothing.
                End If
            Set objFolderItem = Nothing
        Else
            'Folder object returned nothing.
        End If
    Set objFolder2 = Nothing
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



 

 




