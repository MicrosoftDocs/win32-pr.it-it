---
description: Crea e restituisce un oggetto Folder per la cartella specificata.
ms.assetid: CEA73705-1C27-4138-86C4-1715016E2ED8
title: Metodo IShellDispatch. NameSpace (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.NameSpace
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 069752a5e81949889dce5539e3f23960a12c9736
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527343"
---
# <a name="ishelldispatchnamespace-method"></a>IShellDispatch. NameSpace, metodo

Crea e restituisce un oggetto [**Folder**](folder.md) per la cartella specificata.

## <a name="syntax"></a>Sintassi


```JScript
retVal = IShellDispatch.NameSpace(
  vDir
)
```


```VB

IShellDispatch.NameSpace( _
  ByVal vDir As Variant _
) As Folder
```





## <a name="parameters"></a>Parametri

<dl> <dt>

*vdir* \[ in\]
</dt> <dd>

Tipo: **Variant**

Cartella per cui creare l'oggetto [**cartella**](folder.md) . Può trattarsi di una stringa che specifica il percorso della cartella o uno dei valori [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) . Si noti che i nomi delle costanti presenti in **ShellSpecialFolderConstants** sono disponibili in Visual Basic, ma non in VBScript o JScript. In questi casi, i valori numerici devono essere usati al suo posto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

### <a name="jscript"></a>JScript

Tipo: **[ **cartella**](folder.md)\*\***

Riferimento all'oggetto [**Folder**](folder.md) per la cartella specificata. Se la cartella non viene creata correttamente, questo valore restituisce **null**.

### <a name="vb"></a>VB

Tipo: **[ **cartella**](folder.md)\*\***

Riferimento all'oggetto [**Folder**](folder.md) per la cartella specificata. Se la cartella non viene creata correttamente, questo valore restituisce **null**.

## <a name="remarks"></a>Commenti

Questo metodo viene implementato e accessibile tramite il metodo [**Shell. Namespace**](shell-namespace.md) .

## <a name="examples"></a>Esempio

Negli esempi seguenti viene illustrato l'utilizzo dello [**spazio dei nomi**](shell-namespace.md) in JScript, VBScript e Visual Basic.

JScript


```JScript
<script language="JScript">
    function fnShellNameSpaceJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder;
        var ssfWINDOWS = 36
        
        objFolder = objShell.NameSpace(ssfWINDOWS);
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
    function fnShellNameSpaceVB()
        dim objShell
        dim objFolder
        
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace("C:\")

        if (not objFolder is nothing) then
            alert(objFolder.Title)
        end if

        set objFolder = nothing
        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnShellNameSpaceVB()
    Dim objShell  As Shell
    Dim objFolder As Folder

    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfPERSONAL)

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



 

 




