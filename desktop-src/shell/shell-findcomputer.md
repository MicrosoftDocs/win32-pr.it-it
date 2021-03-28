---
description: 'Consente di visualizzare la finestra di dialogo Risultati ricerca: computer. Nella finestra di dialogo viene visualizzato il risultato della ricerca di un computer specifico.'
ms.assetid: 0304b955-afde-4de4-824a-9ec9c9530360
title: Metodo Shell. FindComputer (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.FindComputer
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 3824eeb98bfac11e007d1bf7dd9f89153a7b73ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980642"
---
# <a name="shellfindcomputer-method"></a>Shell. FindComputer, metodo

Consente di visualizzare la finestra di dialogo **Risultati ricerca: computer** . Nella finestra di dialogo viene visualizzato il risultato della ricerca di un computer specifico.

## <a name="syntax"></a>Sintassi


```JScript
Shell.FindComputer()
```


```VB

Shell.FindComputer()
```





## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

### <a name="jscript"></a>JScript

Questo metodo non restituisce valori.

### <a name="vb"></a>VB

Questo metodo non restituisce valori.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato **FindComputer** in uso. Il risultato di questo codice è identico a quello che si ottiene facendo clic sul pulsante **Start** , scegliendo **Cerca**, facendo clic sull'opzione **stampanti, computer o persone** , quindi facendo clic **su un computer in rete**. L'utilizzo corretto viene visualizzato per JScript, VBScript e Visual Basic.

JScript


```JScript
<script language="JScript">
    function fnShellFindComputerJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.FindComputer();
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
        objShell.FindComputer

        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnShellFindComputerVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objShell.FindComputer

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



 

 




