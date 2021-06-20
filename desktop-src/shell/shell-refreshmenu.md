---
description: Informazioni sul metodo Shell.RefreshMenu, che aggiorna il contenuto del menu Start. Usato solo con i sistemi precedenti a Windows XP.
ms.assetid: 1269c66d-61df-432d-9220-5ac975e3ad58
title: Metodo Shell.RefreshMenu (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.RefreshMenu
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 90020cd128f5cbc585bd7bc9ab33a8a81c745f8e
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404534"
---
# <a name="shellrefreshmenu-method"></a>Metodo Shell.RefreshMenu

Aggiorna il contenuto del menu **Start.** Usato solo con i sistemi precedenti a Windows XP.

## <a name="syntax"></a>Sintassi


```JScript
iRetVal = Shell.RefreshMenu()
```


```VB

Shell.RefreshMenu() As Integer
```





## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="remarks"></a>Commenti

La funzionalità fornita **da RefreshMenu** viene gestita automaticamente in Windows XP o versioni successive. Non chiamare questo metodo in tale sistema operativo.

## <a name="examples"></a>Esempio

L'esempio seguente mostra **RefreshMenu** in uso. Viene illustrato l'utilizzo corretto per JScript, VBScript e Visual Basic.

Jscript:


```JScript
<script language="JScript">
    function fnShellRefreshMenuJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.RefreshMenu();
    }
</script>
```



Vbscript:


```VB
<script language="VBScript">
    function fnShellRefreshMenuVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.RefreshMenu

        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnShellRefreshMenuVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.RefreshMenu

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop di Windows 2000 Professional e Windows XP \[\]<br/>                                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                           |
| Intestazione<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 4.71 o successiva)</dt> </dl> |



 

 




