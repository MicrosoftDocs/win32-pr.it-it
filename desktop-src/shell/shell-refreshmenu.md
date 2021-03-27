---
description: Aggiorna il contenuto del menu Start. Utilizzato solo con i sistemi precedenti a Windows XP.
ms.assetid: 1269c66d-61df-432d-9220-5ac975e3ad58
title: Metodo Shell. RefreshMenu (shldisp. h)
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
ms.openlocfilehash: a5812312c846026f4e0c7d2a4f6a5f857a572a23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979767"
---
# <a name="shellrefreshmenu-method"></a>Shell. RefreshMenu, metodo

Aggiorna il contenuto del menu **Start** . Utilizzato solo con i sistemi precedenti a Windows XP.

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

La funzionalità fornita da **RefreshMenu** viene gestita automaticamente in Windows XP o versioni successive. Non chiamare questo metodo in quel sistema operativo.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato **RefreshMenu** in uso. L'utilizzo corretto viene visualizzato per JScript, VBScript e Visual Basic.

JScript


```JScript
<script language="JScript">
    function fnShellRefreshMenuJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.RefreshMenu();
    }
</script>
```



VBScript


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
| Client minimo supportato<br/> | Windows 2000 Professional, \[ solo app desktop Windows XP\]<br/>                                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                           |
| Intestazione<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 4,71 o successiva)</dt> </dl> |



 

 




