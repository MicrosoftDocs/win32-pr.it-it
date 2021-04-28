---
description: "Metodo IShellDispatch.BrowseForFolder: crea una finestra di dialogo che consente all'utente di selezionare una cartella e quindi restituisce l'oggetto Folder della cartella selezionata."
ms.assetid: 578C51C1-F59B-4604-A09B-62BA61225ABB
title: Metodo IShellDispatch.BrowseForFolder (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.BrowseForFolder
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: ee6202c7029e2c27684e15d96dd6c38680cb0678
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086689"
---
# <a name="ishelldispatchbrowseforfolder-method"></a>Metodo IShellDispatch.BrowseForFolder

Crea una finestra di dialogo che consente all'utente di selezionare una cartella e quindi restituisce l'oggetto [**Folder della cartella**](folder.md) selezionata.

## <a name="syntax"></a>Sintassi


```JScript
retVal = IShellDispatch.BrowseForFolder(
  Hwnd,
  sTitle,
  iOptions,
  [ vRootFolder ]
)
```


```VB

IShellDispatch.BrowseForFolder( _
  ByVal Hwnd As Integer, _
  ByVal sTitle As BSTR, _
  ByVal iOptions As Integer, _
  [ ByVal vRootFolder As Variant ] _
) As FOLDER
```





## <a name="parameters"></a>Parametri

<dl> <dt>

*Hwnd* \[ Pollici\]
</dt> <dd>

Tipo: **Integer**

Handle per la finestra padre della finestra di dialogo. Il valore può essere zero.

</dd> <dt>

*sTitle* \[ Pollici\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Valore **String** che rappresenta il titolo visualizzato nella finestra **di dialogo** Sfoglia.

</dd> <dt>

*iOptions* \[ Pollici\]
</dt> <dd>

Tipo: **Integer**

Valore **integer** che contiene le opzioni per il metodo. Può essere zero o una combinazione dei valori elencati nel **membro ulFlags** della [**struttura BROWSEINFO.**](/windows/desktop/api/shlobj_core/ns-shlobj_core-browseinfoa)

</dd> <dt>

*vRootFolder* \[ in, facoltativo\]
</dt> <dd>

Tipo: **Variante**

Cartella radice da utilizzare nella finestra di dialogo. L'utente non può spostarsi più in alto nell'albero rispetto a questa cartella. Se questo valore non viene specificato, la cartella radice usata nella finestra di dialogo è il desktop. Questo valore può essere una stringa che specifica il percorso della cartella o uno dei [**valori shellSpecialFolderConstants.**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) Si noti che i nomi delle costanti presenti in **ShellSpecialFolderConstants** sono disponibili in Visual Basic, ma non in VBScript o JScript. In questi casi, i valori numerici devono essere usati al loro posto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

### <a name="jscript"></a>JScript

Tipo: **\* \* FOLDER**

Riferimento all'oggetto Folder [**della cartella**](folder.md) selezionata.

### <a name="vb"></a>VB

Tipo: **\* \* FOLDER**

Riferimento all'oggetto Folder [**della cartella**](folder.md) selezionata.

## <a name="remarks"></a>Commenti

Questo metodo viene implementato e accessibile tramite il [**metodo Shell.BrowseForFolder.**](shell-browseforfolder.md)

## <a name="examples"></a>Esempio

Gli esempi seguenti usano **BrowseForFolder** per visualizzare una finestra di esplorazione denominata "Example" radice nella cartella Windows. L'utilizzo è illustrato per JScript, VBScript e Visual Basic.

Jscript:


```JScript
<script language="JScript">
    function fnShellBrowseForFolderJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var ssfWINDOWS = 36;
        var objFolder;
        
        objFolder = objshell.BrowseForFolder(0, "Example", 0, ssfWINDOWS);
        if (objFolder != null)
        {
            // Add code here.
        }
    }
</script>
```



Vbscript:


```VB
<script language="VBScript">
    function fnShellBrowseForFolderVB()
        dim objShell
        dim ssfWINDOWS
        dim objFolder
        
        ssfWINDOWS = 36
        set objShell = CreateObject("shell.application")
            set objFolder = objshell.BrowseForFolder(0, "Example", 0, ssfWINDOWS)
                if (not objFolder is nothing) then
                    'Add code here.
                end if
            set objFolder = nothing
        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnShellBrowseForFolderVB()
    Dim objShell   As Shell
    Dim ssfWINDOWS As Long
    Dim objFolder  As Folder
    
    ssfWINDOWS = 36
    Set objShell = New Shell
        Set objFolder = objshell.BrowseForFolder(0, "Example", 0, ssfWINDOWS)
            If (Not objFolder Is Nothing) Then
                'Add code here
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



 

 
