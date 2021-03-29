---
description: 'Consente di visualizzare la finestra di dialogo Risultati ricerca: computer. Nella finestra di dialogo viene visualizzato il risultato della ricerca di un computer specifico.'
ms.assetid: 9B687A8A-BB29-49a0-8AE3-11A75FAF3257
title: Metodo IShellDispatch. FindComputer (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.FindComputer
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 3ad928b6860a85126a714a08f3bc3df9d4aff67c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978111"
---
# <a name="ishelldispatchfindcomputer-method"></a>IShellDispatch. FindComputer, metodo

Consente di visualizzare la finestra di dialogo **Risultati ricerca: computer** . Nella finestra di dialogo viene visualizzato il risultato della ricerca di un computer specifico.

## <a name="syntax"></a>Sintassi


```JScript
IShellDispatch.FindComputer()
```


```VB

IShellDispatch.FindComputer()
```





## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

### <a name="jscript"></a>JScript

Questo metodo non restituisce valori.

### <a name="vb"></a>VB

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo viene implementato e accessibile tramite il metodo [**Shell. FindComputer**](shell-findcomputer.md) .

## <a name="examples"></a>Esempio

Negli esempi seguenti viene illustrato l'utilizzo di **FindComputer** in JScript, VBScript e Visual Basic.

JScript


```JScript
<script language="JScript">
    function fnShellFindComputerJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.FindComputer();
    }
</script>
```



VBScript


```VB
 <script language="VBScript">
    function fnShellFindComputerVB()
        dim objShell
        dim ssfWINDOWS
        ssfWINDOWS = 36

        set objShell = CreateObject("shell.application")
        objshell.FindComputer

        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnShellFindComputerVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objshell.FindComputer

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



 

 




