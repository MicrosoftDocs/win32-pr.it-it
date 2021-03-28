---
description: Riquadri verticalmente tutte le finestre sul desktop. Questo metodo ha lo stesso effetto che si fa clic con il pulsante destro del mouse sulla barra delle applicazioni e si seleziona Mostra finestre affiancate.
ms.assetid: 63CB7E20-48E6-4cfe-B0BA-0D28A7B151BD
title: Metodo IShellDispatch. TileVertically (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.TileVertically
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 42f98ae99814495029c67d41b05e86182c6b8b34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978079"
---
# <a name="ishelldispatchtilevertically-method"></a>IShellDispatch. TileVertically, metodo

Riquadri verticalmente tutte le finestre sul desktop. Questo metodo ha lo stesso effetto che si fa clic con il pulsante destro del mouse sulla barra delle applicazioni e si seleziona **Mostra finestre affiancate**.

## <a name="syntax"></a>Sintassi


```JScript
IShellDispatch.TileVertically()
```


```VB

IShellDispatch.TileVertically()
```





## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

### <a name="jscript"></a>JScript

Questo metodo non restituisce valori.

### <a name="vb"></a>VB

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo viene implementato e accessibile tramite il metodo [**Shell. TileVertically**](shell-tilevertically.md) .

## <a name="examples"></a>Esempio

Negli esempi seguenti viene illustrato l'utilizzo di **TileVertically** in JScript, VBScript e Visual Basic.

JScript


```JScript
<script language="JScript">
    function fnShellTileVerticallyJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.TileVertically();
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnShellTileVerticallyVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.TileVertically

        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnShellTileVerticallyVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.TileVertically

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



 

 




