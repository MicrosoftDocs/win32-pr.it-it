---
description: Crea una finestra di dialogo che consente all'utente di selezionare una cartella e quindi restituisce l'oggetto cartella della cartella selezionata.
title: Metodo Shell. BrowseForFolder (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.BrowseForFolder
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 4cc44e5a-3578-448b-9b19-1b71e1ae2cb9
ms.openlocfilehash: 7e14dffbfb9ab3e18bd4d8e11ffaf4768ad53131
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050260"
---
# <a name="shellbrowseforfolder-method"></a>Shell. BrowseForFolder, metodo

Crea una finestra di dialogo che consente all'utente di selezionare una cartella e quindi restituisce l'oggetto [**cartella**](folder.md) della cartella selezionata.

## <a name="syntax"></a>Sintassi


```JScript
retVal = Shell.BrowseForFolder(
  Hwnd,
  sTitle,
  iOptions,
  [ vRootFolder ]
)
```


```VB

Shell.BrowseForFolder( _
  ByVal Hwnd As Integer, _
  ByVal sTitle As BSTR, _
  ByVal iOptions As Integer, _
  [ ByVal vRootFolder As Variant ] _
) As FOLDER
```





## <a name="parameters"></a>Parametri

<dl> <dt>

*HWND* \[ in\]
</dt> <dd>

Tipo: **Integer**

Handle per la finestra padre della finestra di dialogo. Il valore può essere zero.

</dd> <dt>

*sTitle* \[ in\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Valore **stringa** che rappresenta il titolo visualizzato nella finestra di dialogo **Sfoglia** .

</dd> <dt>

*iOptions* \[ in\]
</dt> <dd>

Tipo: **Integer**

Valore **intero** che contiene le opzioni per il metodo. Può essere zero o una combinazione dei valori elencati sotto il membro **ulFlags** della struttura [**BROWSEINFO**](/windows/desktop/api/shlobj_core/ns-shlobj_core-browseinfoa) .

</dd> <dt>

*vRootFolder* \[ in, facoltativo\]
</dt> <dd>

Tipo: **Variant**

Cartella radice da utilizzare nella finestra di dialogo. L'utente non può spostarsi più in alto nell'albero rispetto a questa cartella. Se questo valore non viene specificato, la cartella radice utilizzata nella finestra di dialogo è il desktop. Questo valore può essere una stringa che specifica il percorso della cartella o uno dei valori [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) . Si noti che i nomi delle costanti presenti in **ShellSpecialFolderConstants** sono disponibili in Visual Basic, ma non in VBScript o JScript. In questi casi, i valori numerici devono essere usati al suo posto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

### <a name="jscript"></a>JScript

Tipo: **cartella \* \***

Riferimento all'oggetto [**Folder**](folder.md) della cartella selezionata.

### <a name="vb"></a>VB

Tipo: **cartella \* \***

Riferimento all'oggetto [**Folder**](folder.md) della cartella selezionata.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene usato **BrowseForFolder** per visualizzare una finestra di esplorazione denominata "example" con radice nella cartella Windows. L'utilizzo corretto viene visualizzato per JScript, VBScript e Visual Basic.

JScript


```JScript
<script language="JScript">
    function fnShellBrowseForFolderJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var ssfWINDOWS = 36;
        var objFolder;
        
        objFolder = objShell.BrowseForFolder(0, "Example", 0, ssfWINDOWS);
        if (objFolder != null)
        {
            // Add code here.
        }
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnShellBrowseForFolderVB()
        dim objShell
        dim ssfWINDOWS
        dim objFolder
        
        ssfWINDOWS = 36
        set objShell = CreateObject("shell.application")
            set objFolder = objShell.BrowseForFolder(0, "Example", 0, ssfWINDOWS)
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
        Set objFolder = objShell.BrowseForFolder(0, "Example", 0, ssfWINDOWS)
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
| Client minimo supportato<br/> | Windows 2000 Professional, \[ solo app desktop Windows XP\]<br/>                                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                           |
| Intestazione<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 4,71 o successiva)</dt> </dl> |



 

 
