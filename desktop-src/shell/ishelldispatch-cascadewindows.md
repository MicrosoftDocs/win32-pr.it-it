---
description: Si sovrappone a tutte le finestre sul desktop. Questo metodo ha lo stesso effetto di fare clic con il pulsante destro del mouse sulla barra delle applicazioni e selezionare Cascade Windows.
ms.assetid: 6A957D70-D6A3-4485-8DF3-7FD2C6DEFF78
title: Metodo IShellDispatch. CascadeWindows (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.CascadeWindows
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 4252e4df579bc73e9f082630f9f98b83e3b57f47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130099"
---
# <a name="ishelldispatchcascadewindows-method"></a>IShellDispatch. CascadeWindows, metodo

Si sovrappone a tutte le finestre sul desktop. Questo metodo ha lo stesso effetto di fare clic con il pulsante destro del mouse sulla barra delle applicazioni e selezionare **Cascade Windows**.

## <a name="syntax"></a>Sintassi


```JScript
IShellDispatch.CascadeWindows()
```


```VB

IShellDispatch.CascadeWindows()
```





## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

### <a name="jscript"></a>JScript

Questo metodo non restituisce valori.

### <a name="vb"></a>VB

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo viene implementato e accessibile tramite il metodo [**Shell. CascadeWindows**](shell-cascadewindows.md) .

## <a name="examples"></a>Esempio

Negli esempi seguenti viene illustrato l'utilizzo di **CascadeWindows** in JScript, VBScript e Visual Basic.

JScript


```JScript
<script language="JScript">
    function fnShellCascadeWindowsJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.CascadeWindows();
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnShellCascadeWindowsVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.CascadeWindows
        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnShellCascadeWindowsVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.CascadeWindows
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



 

 




