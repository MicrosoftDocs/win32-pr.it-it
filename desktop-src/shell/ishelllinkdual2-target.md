---
description: Contiene la destinazione dell'oggetto collegamento.
ms.assetid: 26da562b-a1d6-4150-9d9a-05b11e3972d9
title: Proprietà IShellLinkDual2.Target (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellLinkDual2.Target
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 3319e84abc32887d7cf7a9126ea9ae0f57b9607f937256b8377030fdd9dd75cc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119884321"
---
# <a name="ishelllinkdual2target-property"></a>Proprietà IShellLinkDual2.Target

Contiene la destinazione dell'oggetto collegamento.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
Target = IShellLinkDual2.Target
```



## <a name="property-value"></a>Valore proprietà

Espressione dell'oggetto che restituisce l'oggetto [**FolderItem della**](folderitem.md) destinazione.

## <a name="examples"></a>Esempio

L'esempio seguente usa **Target** per recuperare la destinazione di un collegamento Internet Explorer. Viene visualizzato l'utilizzo corretto JScript, VBScript e Visual Basic.

JScript:


```JScript
<script language="JScript">
    function fnIShellLinkDual2TargetJ()
    {
        var objShell    = new ActiveXObject("shell.application");
        var objFolder;
        var ssfPROGRAMS = 2;
        
        objFolder = objShell.NameSpace(ssfPROGRAMS);
        if (objFolder != null)
        {
            var objFolderItem;
                
            objFolderItem = objFolder.ParseName("Internet Explorer.lnk");
            if (objFolderItem != null)
            {
                var objShellLink;
                        
                objShellLink = objFolderItem.GetLink;
                if (objShellLink != null)
                {
                    var objTargetItem;
                            
                    objTargetItem = objShellLink.Target;
                    if (objTargetItem != null)
                    {
                        // Add code here.
                    }
                }
            }
        }
    }
</script>
```



Vbscript:


```VB
<script language="VBScript">
    function fnIShellLinkDual2TargetVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder
            dim ssfPROGRAMS
            
            ssfPROGRAMS = 2
            set objFolder = objShell.NameSpace(ssfPROGRAMS)
            if (not objFolder is nothing) then
                dim objFolderItem
                        
                set objFolderItem = objFolder.ParseName("Internet Explorer.lnk")
                if (not objFolderItem is nothing) then
                    dim objShellLink
                    
                    set objShellLink = objFolderItem.GetLink
                        if (not objShellLink is nothing) then
                            dim objTargetItem
                            
                            set objTargetItem = objShellLink.Target
                                if (not objTargetItem is nothing) then
                                    'Add code here.
                                end if
                            set objTargetItem = nothing
                        end if
                    set objShellLink = nothing
                end if
                set objFolderItem = nothing
            end if
            set objFolder = nothing
        end if
        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnIShellLinkDual2TargetVB()
    Dim objShell   As Shell
    Dim objFolder  As Folder
    Dim ssfPROGRAMS
            
    ssfPROGRAMS = 2
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfPROGRAMS)
    If (Not objFolder Is Nothing) Then
        Dim objFolderItem As FolderItem
                
        Set objFolderItem = objFolder.ParseName("Internet Explorer.lnk")
        If (Not objFolderItem Is Nothing) Then
            Dim objShellLink As ShellLinkObject
            
            Set objShellLink = objFolderItem.GetLink
                If (Not objShellLink Is Nothing) Then
                    Dim objTargetItem As FolderItem
                    
                    Set objTargetItem = objShellLink.Target
                        If (Not objTargetItem Is Nothing) Then
                            'Add code here
                        End If
                    Set objTargetItem = Nothing
                End If
            Set objShellLink = Nothing
        End If
        Set objFolderItem = Nothing
    End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, Windows solo app desktop XP \[\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 5.0 o successiva)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IShellLinkDual2**](ishelllinkdual2-object.md)
</dt> <dt>

[**ShellLinkObject**](shelllinkobject-object.md)
</dt> </dl>

 

 




