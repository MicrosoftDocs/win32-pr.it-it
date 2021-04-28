---
description: 'Metodo IShellDispatch.NameSpace: crea e restituisce un oggetto Folder per la cartella specificata.'
ms.assetid: CEA73705-1C27-4138-86C4-1715016E2ED8
title: Metodo IShellDispatch.NameSpace (Shldisp.h)
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
ms.openlocfilehash: d1db0a3969350b4be4bc32e027bf2000036e099f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108100519"
---
# <a name="ishelldispatchnamespace-method"></a>Metodo IShellDispatch.NameSpace

Crea e restituisce un [**oggetto Folder**](folder.md) per la cartella specificata.

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

*vDir* \[ Pollici\]
</dt> <dd>

Tipo: **Variante**

Cartella per la quale creare [**l'oggetto**](folder.md) Folder. Può essere una stringa che specifica il percorso della cartella o uno dei [**valori ShellSpecialFolderConstants.**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) Si noti che i nomi delle costanti presenti in **ShellSpecialFolderConstants** sono disponibili in Visual Basic, ma non in VBScript o JScript. In questi casi, i valori numerici devono essere usati al loro posto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

### <a name="jscript"></a>JScript

Tipo: **[ **Cartella**](folder.md)\*\***

Riferimento all'oggetto [**Folder**](folder.md) per la cartella specificata. Se la cartella non viene creata correttamente, questo valore restituisce **null.**

### <a name="vb"></a>VB

Tipo: **[ **Cartella**](folder.md)\*\***

Riferimento all'oggetto [**Folder**](folder.md) per la cartella specificata. Se la cartella non viene creata correttamente, questo valore restituisce **null.**

## <a name="remarks"></a>Commenti

Questo metodo viene implementato e accessibile tramite il [**metodo Shell.NameSpace.**](shell-namespace.md)

## <a name="examples"></a>Esempio

Gli esempi seguenti illustrano l'uso [**di NameSpace**](shell-namespace.md) in JScript, VBScript e Visual Basic.

Jscript:


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



Vbscript:


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
| Client minimo supportato<br/> | Solo app desktop windows 2000 Professional e Windows XP \[\]<br/>                                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                           |
| Intestazione<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 4.71 o successiva)</dt> </dl> |



 

 




