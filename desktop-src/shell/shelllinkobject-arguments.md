---
description: Contiene gli argomenti di un collegamento.
ms.assetid: 938db958-4b59-4dd6-ac56-f21db05ec989
title: Proprietà ShellLinkObject.Arguments (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellLinkObject.Arguments
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 3124e76ec8ba46f3e8915ac24c080c3e28caad620f7de1d100eaa7bb2316d851
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117857592"
---
# <a name="shelllinkobjectarguments-property"></a>ShellLinkObject.Arguments - proprietà

Contiene gli argomenti di un collegamento.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```JScript
strArguments = ShellLinkObject.Arguments
ShellLinkObject.Arguments(sArguments) = strArguments
```



## <a name="property-value"></a>Valore proprietà

argomenti del collegamento.

## <a name="examples"></a>Esempio

Nell'esempio seguente vengono utilizzati **argomenti** per recuperare gli argomenti per un collegamento Internet Explorer trovati nel menu Start dell'utente. Viene visualizzato un utilizzo appropriato per JScript, VBScript e Visual Basic.

JScript:


```JScript
<script language="JScript">
    function fnShellShellLinkObjectArgumentJ()
    {
        var objShell = new ActiveXObject("shell.application");
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
                    var szArguments;
                    
                    // Get the arguments for the ShellLinkObject
                    szArguments = objShellLink.Arguments;
                    alert(szArguments);
                    
                    // Set the arguments for the ShellLinkObject
                    objShellLink.Arguments = "/s"
                }
            }
        }
    }
</script>
```



Vbscript:


```VB
<script language="VBScript">
    function fnShellLinkObjectArgumentVB()
        dim objShell
        dim objFolder
        dim ssfPROGRAMS
        
        ssfPROGRAMS = 2
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace(ssfPROGRAMS)

        if (not objFolder is nothing) then
            dim objFolderItem
            
            set objFolderItem = objFolder.ParseName("Internet Explorer.lnk")

            if (not objFolderItem is nothing) then
                dim objShellLink
                
                set objShellLink = objFolderItem.GetLink

                if (not objShellLink is nothing) then
                    dim szArguments
                    
                    'Get the arguments for the ShellLinkObject
                    szArguments = objShellLink.Arguments
                    alert(szArguments)
                    
                    'Set the arguments for the ShellLinkObject
                    objShellLink.Arguments = "/s"
                end if

                set objShellLink = nothing
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
Private Sub fnShellLinkObjectArgumentsVB()
    Dim objShell  As Shell
    Dim objFolder As Folder
    
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfPROGRAMS)
        If (Not objFolder Is Nothing) Then
            Dim objFolderItem As FolderItem
            
            Set objFolderItem = objFolder.ParseName("Internet Explorer.lnk")

            If (Not objFolderItem Is Nothing) Then
                Dim objShellLink As ShellLinkObject
                
                Set objShellLink = objFolderItem.GetLink

                If (Not objShellLink Is Nothing) Then
                    Dim szArguments As String
                    
                    'Get the arguments for the ShellLinkObject
                    szArguments = objShellLink.Arguments
                    Debug.Print szArguments
                    
                    'Set the arguments for the ShellLinkObject
                    objShellLink.Arguments = "/s"
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
| Client minimo supportato<br/> | Windows 2000 Professional solo con le app desktop SP3 \[\]<br/>                                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 5.0 o successiva)</dt> </dl> |



 

 




