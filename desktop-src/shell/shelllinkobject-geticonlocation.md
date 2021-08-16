---
description: Ottiene il percorso dell'icona assegnata al collegamento.
ms.assetid: 3bb7f0f0-7ab9-41e6-b738-274efbcd52ab
title: Metodo ShellLinkObject.GetIconLocation (Shlobj \_ core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellLinkObject.GetIconLocation
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 09ace233291d5eac285ac1115866a54cb9792c85aefbb8faa5a2d1f6c37393e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117857582"
---
# <a name="shelllinkobjectgeticonlocation-method"></a>Metodo ShellLinkObject.GetIconLocation

Ottiene il percorso dell'icona assegnata al collegamento.

## <a name="syntax"></a>Sintassi


```JScript
iRetVal = ShellLinkObject.GetIconLocation(
  sPath
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*sPath* \[ Cambio\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)\***

Quando viene restituito, questo metodo contiene il percorso completo del file che contiene l'icona.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **\* Integer**

Restituisce l'indice dell'icona nel file specificato da *sPath*.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato l'utilizzo corretto di questo metodo per JScript, VBScript e Visual Basic.

JScript:


```JScript
<script language="JScript">
    function fnShellShellLinkObjectGetIconLocationJ()
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
                    var nIcon;
                    
                    nIcon = objShellLink.GetIconLocation(objFolderItem.Path);
                    alert(nIcon);
                }
            }
        }
    }
</script>
```



Vbscript:


```VB
<script language="VBScript">
    function fnShellLinkObjectGetIconLocationVB()
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
                                dim nIcon
                                
                                nIcon = objShellLink.GetIconLocation(objFolderItem.Path)
                                alert(nIcon)
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
Private Sub fnShellLinkObjectGetIconLocationVB()
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
                            Dim nIcon As Integer
                            
                            nIcon = objShellLink.GetIconLocation(objFolderItem.Path)
                            Debug.Print nIcon
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
| Intestazione<br/>                   | <dl> <dt>Shlobj \_ core.h (includere Shldisp.h)</dt> </dl> |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 5.0 o successiva)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ShellLinkObject**](shelllinkobject-object.md)
</dt> <dt>

[**SetIconLocation**](shelllinkobject-seticonlocation.md)
</dt> </dl>

 

 
