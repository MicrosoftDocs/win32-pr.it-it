---
description: Indica se l'elemento può essere ospitato all'interno di un browser o Windows Explorer.
ms.assetid: 472e0906-9561-4390-a503-c5e490245ea0
title: Proprietà FolderItem.IsBrowsable (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItem.IsBrowsable
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 9c417b3a225ba7d9f39329fe274d99ee09c3a98353a9822d1047ea426610411c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119093087"
---
# <a name="folderitemisbrowsable-property"></a>FolderItem.IsBrowsable - proprietà

Indica se l'elemento può essere ospitato all'interno di un browser o Windows Explorer.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
bIsBrowsable = FolderItem.IsBrowsable
```



## <a name="property-value"></a>Valore proprietà

Valore **booleano** che riceve **true se** l'elemento può essere visualizzato o false **in** caso contrario.

## <a name="examples"></a>Esempio

L'esempio seguente **usa IsBrowsable** per determinare lo stato esplorabile della Windows cartella. Viene visualizzato l'utilizzo corretto JScript, VBScript e Visual Basic.

JScript:


```JScript
<script language="JScript">
    function fnIsBrowsableJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder2;
        var ssfWINDOWS = 36;
        
        objFolder2 = objShell.NameSpace(ssfWINDOWS);
        if (objFolder2 != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder2.Self;
            if (objFolderItem != null)
            {
                var bReturn;
                
                bReturn = objFolderItem.IsBrowsable;
            }
        }
    }
</script>
```



Vbscript:


```VB
<script language="VBScript">
    function fnIsBrowsableVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder2
            dim ssfWINDOWS
                
            ssfWINDOWS = 36
            set objFolder2 = objShell.NameSpace(ssfWINDOWS)
            if (not objFolder2 is nothing) then
                dim objFolderItem
                        
                set objFolderItem = objFolder2.Self
                if (not objFolderItem is nothing) then
                    dim bReturn
                                
                    bReturn = objFolderItem.IsBrowsable
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
Private Sub fnIsBrowsableVB()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2
    Dim ssfWINDOWS As Long
    
    ssfWINDOWS = 36
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace(ssfWINDOWS)
        If (Not objFolder2 Is Nothing) Then
            Dim objFolderItem As FolderItem
            
            Set objFolderItem = objFolder2.Self
                If (Not objFolderItem Is Nothing) Then
                    Dim bReturn As Boolean
                    
                    bReturn = objFolderItem.IsBrowsable
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
| Client minimo supportato<br/> | Windows 2000 Professional, Windows solo app \[ desktop XP\]<br/>                                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                           |
| Intestazione<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 4.71 o successiva)</dt> </dl> |



 

 




