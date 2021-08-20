---
description: Sovrapporre tutte le finestre sul desktop. Questo metodo ha lo stesso effetto di fare clic con il pulsante destro del mouse sulla barra delle applicazioni e scegliere Sovrapponi finestre.
ms.assetid: 6A957D70-D6A3-4485-8DF3-7FD2C6DEFF78
title: Metodo IShellDispatch.CascadeWindows (Shldisp.h)
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
ms.openlocfilehash: 7e14514c31f81327d9d0c0217479d2ce746c61ed58c9f71e1b2fa6f19f4e31ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032279"
---
# <a name="ishelldispatchcascadewindows-method"></a>Metodo IShellDispatch.CascadeWindows

Sovrapporre tutte le finestre sul desktop. Questo metodo ha lo stesso effetto di fare clic con il pulsante destro del mouse sulla barra delle applicazioni e scegliere **Sovrapponi finestre**.

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

Questo metodo viene implementato e accessibile tramite il [**metodo Shell.CascadeWindows.**](shell-cascadewindows.md)

## <a name="examples"></a>Esempio

Gli esempi seguenti illustrano l'uso di **CascadeWindows** in JScript, VBScript e Visual Basic.

JScript:


```JScript
<script language="JScript">
    function fnShellCascadeWindowsJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.CascadeWindows();
    }
</script>
```



Vbscript:


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
| Client minimo supportato<br/> | Windows 2000 Professional, Windows solo app desktop XP \[\]<br/>                                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                           |
| Intestazione<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 4.71 o successiva)</dt> </dl> |



 

 




