---
description: Ottiene o imposta lo stato di visualizzazione iniziale (ridimensionato, ridotto a icona o ingrandito) del comando del collegamento.
ms.assetid: 139c6924-f554-4fde-9ed0-bc117bafbb16
title: Proprietà ShellLinkObject. ShowCommand (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellLinkObject.ShowCommand
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 9bacdf98a24d749b5128bc286f06e99299aef437
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104995165"
---
# <a name="shelllinkobjectshowcommand-property"></a>Proprietà ShellLinkObject. ShowCommand

Ottiene o imposta lo stato di visualizzazione iniziale (ridimensionato, ridotto a icona o ingrandito) del comando del collegamento.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```JScript
iShowCommand = ShellLinkObject.ShowCommand
ShellLinkObject.ShowCommand(intShowCommand) = iShowCommand
```



## <a name="property-value"></a>Valore proprietà

stato di visualizzazione del collegamento. I valori possibili sono i seguenti:

<dt>



 (1)


</dt> <dd>

Attiva e visualizza una finestra. Se la finestra è ridotta a icona o ingrandita, il sistema ripristina le dimensioni e la posizione originali.

</dd> <dt>



 (2)


</dt> <dd>

Attiva la finestra e la Visualizza come finestra ridotta a icona.

</dd> <dt>



 (3)


</dt> <dd>

Attiva la finestra e la Visualizza come finestra ingrandita.

</dd> </dl>

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato l'utilizzo corretto di questa proprietà in JScript, VBScript e Visual Basic.

JScript


```JScript
<script language="JScript">
    function fnShellShellLinkObjectShowCommandJ()
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
                    var nShow;
                    
                    // Get the ShowCommand for the ShellLinkObject.
                    nShow = objShellLink.ShowCommand;
                    alert(nShow);
                    
                    // Set the ShowCommand for the ShellLinkObject.
                    objShellLink.ShowCommand = 1
                }
            }
        }
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnShellLinkObjectShowCommandVB()
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
                                dim nShow
                                
                                'Get the ShowCommand for the ShellLinkObject.
                                nShow = objShellLink.ShowCommand
                                alert(nShow)
                                
                                'Set the ShowCommand for the ShellLinkObject.
                                objShellLink.ShowCommand = 1
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
Private Sub fnShellLinkObjectShowCommandVB()
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
                            Dim nShow As Integer
                            
                            'Get the ShowCommand for the ShellLinkObject.
                            nShow = objShellLink.ShowCommand
                            Debug.Print nShow
                            
                            'Set the ShowCommand for the ShellLinkObject.
                            objShellLink.ShowCommand = 1
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
| Client minimo supportato<br/> | Windows 2000 Professional con \[ solo app desktop SP3\]<br/>                                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 5,0 o successiva)</dt> </dl> |



 

 




