---
description: Consente di visualizzare la finestra di dialogo Proprietà data e ora . Questo metodo ha lo stesso effetto di fare clic con il pulsante destro del mouse sull'orologio nell'area di stato della barra delle applicazioni e scegliere Regola data/ora.
ms.assetid: 01694607-3fc2-4d0d-ba48-5bdbb40da000
title: Metodo Shell.SetTime (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.SetTime
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: cff10e89cfdc8ba038be2b619264c02b1c7b168d4ecb35cd625683f648121be6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118452842"
---
# <a name="shellsettime-method"></a>Metodo Shell.SetTime

Consente di visualizzare **la finestra di dialogo Proprietà data** e ora . Questo metodo ha lo stesso effetto di fare clic con il pulsante destro del mouse sull'orologio nell'area di stato della barra delle applicazioni e scegliere **Regola data/ora**.

## <a name="syntax"></a>Sintassi


```JScript
iRetVal = Shell.SetTime()
```


```VB

Shell.SetTime() As Integer
```





## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="examples"></a>Esempio

L'esempio seguente illustra **SetTime** in uso. Viene visualizzato un utilizzo appropriato per JScript, VBScript e Visual Basic.

JScript:


```JScript
<script language="JScript">
    function fnShellSetTimeJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.SetTime();
    }
</script>
```



Vbscript:


```VB
<script language="VBScript">
    function fnShellSetTimeVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.SetTime
 
        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnShellSetTimeVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.SetTime
 
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



 

 




