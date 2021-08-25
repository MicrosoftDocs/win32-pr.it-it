---
description: Ripristina tutte le finestre desktop allo stesso stato in cui si trovavano prima dell'ultimo comando MinimizeAll.
ms.assetid: dcedfa18-6dde-4fb8-9679-4d6ff80249e4
title: Metodo Shell.UndoMinimizeALL (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.UndoMinimizeALL
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 5e2342bda1059e2bcb00893afb182e415840a4e650392fc3e1d3df4756cb2d03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941571"
---
# <a name="shellundominimizeall-method"></a>Metodo Shell.UndoMinimizeALL

Ripristina tutte le finestre desktop allo stesso stato in cui si trovavano prima dell'ultimo [**comando MinimizeAll.**](shell-minimizeall.md) Questo metodo ha lo stesso effetto di fare clic con il pulsante destro del mouse  sulla barra delle applicazioni e scegliere Annulla Riduci a icona tutto **Windows** nei sistemi precedenti o un secondo clic sull'icona Mostra desktop nell'area Avvio veloce della barra delle applicazioni in Windows 2000 o Windows XP.

## <a name="syntax"></a>Sintassi


```JScript
iRetVal = Shell.UndoMinimizeALL()
```


```VB

Shell.UndoMinimizeALL() As Integer
```





## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="examples"></a>Esempio

L'esempio seguente **mostra UndoMinimizeALL** in uso. Viene visualizzato l'utilizzo corretto JScript, VBScript e Visual Basic.

JScript:


```JScript
<script language="JScript">
    function fnShellUndoMinimizeALLJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.UndoMinimizeALL();
    }
</script>
```



Vbscript:


```VB
<script language="VBScript">
    function fnShellUndoMinimizeALLVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.UndoMinimizeALL

        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnShellUndoMinimizeAllVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.UndoMinimizeALL

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



 

 




