---
description: Informazioni sul metodo IShellDispatch.RefreshMenu, che aggiorna il contenuto del menu Start. Usato solo con i sistemi che precedono Windows XP.
ms.assetid: D36FA5A0-AF03-4627-86E0-869BF1440958
title: Metodo IShellDispatch.RefreshMenu (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.RefreshMenu
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: ac5bb37f5880011fcabcfcc0e923196857694012a547b0391326a9fe5d8424f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118969060"
---
# <a name="ishelldispatchrefreshmenu-method"></a>Metodo IShellDispatch.RefreshMenu

Aggiorna il contenuto del menu **Start.** Usato solo con i sistemi che precedono Windows XP.

## <a name="syntax"></a>Sintassi


```JScript
IShellDispatch.RefreshMenu()
```


```VB

IShellDispatch.RefreshMenu()
```





## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

### <a name="jscript"></a>JScript

Questo metodo non restituisce valori.

### <a name="vb"></a>VB

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo viene implementato e accessibile tramite il [**metodo Shell.TrayProperties.**](shell-trayproperties.md)

La funzionalità fornita **da RefreshMenu** viene gestita automaticamente in Windows XP o versioni successive. Non chiamare questo metodo in Windows XP o versioni successive.

## <a name="examples"></a>Esempio

Gli esempi seguenti illustrano l'uso di **RefreshMenu** in JScript, VBScript e Visual Basic.

JScript:


```JScript
<script language="JScript">
    function fnShellRefreshMenuJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.RefreshMenu();
    }
</script>
```



Vbscript:


```VB
<script language="VBScript">
    function fnShellRefreshMenuVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.RefreshMenu

        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnShellRefreshMenuVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.RefreshMenu

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, Windows solo app \[ desktop XP\]<br/>                                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                           |
| Intestazione<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 4.71 o successiva)</dt> </dl> |



 

 




