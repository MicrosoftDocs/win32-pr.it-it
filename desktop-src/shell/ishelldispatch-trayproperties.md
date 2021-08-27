---
description: 'Metodo IShellDispatch.TrayProperties: visualizza la finestra di dialogo Proprietà barra delle applicazioni e menu Start. Questo metodo ha lo stesso effetto di fare clic con il pulsante destro del mouse sulla barra delle applicazioni e scegliere Proprietà.'
ms.assetid: 8E0AC08E-1132-4312-9B75-E7686B91AB02
title: Metodo IShellDispatch.TrayProperties (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.TrayProperties
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 1c7ec210b7b3eb178f328e880041e45dd1e9a9279b3644e5b83fc9d5d78ef77c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111521"
---
# <a name="ishelldispatchtrayproperties-method"></a>Metodo IShellDispatch.TrayProperties

Consente di visualizzare la **finestra di dialogo Proprietà barra delle** applicazioni e menu Start . Questo metodo ha lo stesso effetto di fare clic con il pulsante destro del mouse sulla barra delle applicazioni e scegliere **Proprietà**.

## <a name="syntax"></a>Sintassi


```JScript
IShellDispatch.TrayProperties()
```


```VB

IShellDispatch.TrayProperties()
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

## <a name="examples"></a>Esempio

Gli esempi seguenti illustrano l'uso di **TrayProperties** in JScript, VBScript e Visual Basic.

JScript:


```JScript
<script language="JScript">
    function fnShellTrayPropertiesJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.TrayProperties();
    }
</script>
```



Vbscript:


```VB
<script language="VBScript">
    function fnShellTrayPropertiesVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.TrayProperties

        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnShellTrayPropertiesVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.TrayProperties

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



 

 




