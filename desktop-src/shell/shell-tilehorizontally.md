---
description: Riquadri orizzontalmente tutte le finestre sul desktop. Questo metodo ha lo stesso effetto che si fa clic con il pulsante destro del mouse sulla barra delle applicazioni e si seleziona finestre affiancate orizzontalmente
ms.assetid: b0e06766-1bd4-4744-81f3-139b018aa72c
title: Metodo Shell. TileHorizontally (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.TileHorizontally
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: e295d0a7847afc0cb405f3ab9141e54ae424e9e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232100"
---
# <a name="shelltilehorizontally-method"></a>Shell. TileHorizontally, metodo

Riquadri orizzontalmente tutte le finestre sul desktop. Questo metodo ha lo stesso effetto che si fa clic con il pulsante destro del mouse sulla barra delle applicazioni e si seleziona **finestre affiancate orizzontalmente**

## <a name="syntax"></a>Sintassi


```JScript
iRetVal = Shell.TileHorizontally()
```


```VB

Shell.TileHorizontally() As Integer
```





## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato **TileHorizontally** in uso. L'utilizzo corretto viene visualizzato per JScript, VBScript e Visual Basic.

JScript


```JScript
<script language="JScript">
    function fnShellTileHorizontallyJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.TileHorizontally();
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnShellTileHorizontallyVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.TileHorizontally

        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnShellTileHorizontallyVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.TileHorizontally

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



 

 




