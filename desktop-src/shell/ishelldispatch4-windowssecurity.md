---
description: 'Metodo IShellDispatch4.WindowsSecurity: visualizza la Sicurezza di Windows finestra di dialogo.'
title: Metodo IShellDispatch4.WindowsSecurity (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch4.WindowsSecurity
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 665c4644-7749-446e-8212-3ecc9901a035
ms.openlocfilehash: 2d7e8cfbd1e7a2a2392b78487c6a58b62de6df6a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116809"
---
# <a name="ishelldispatch4windowssecurity-method"></a>Metodo IShellDispatch4.WindowsSecurity

Consente di visualizzare **Sicurezza di Windows** finestra di dialogo.

## <a name="syntax"></a>Sintassi


```JScript
IShellDispatch4.WindowsSecurity()
```


```VB

IShellDispatch4.WindowsSecurity()
```





## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

### <a name="jscript"></a>JScript

Questo metodo non restituisce valori.

### <a name="vb"></a>VB

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo visualizza la finestra di dialogo visualizzata dopo aver premuto CTRL+ALT+CANC o usando l'opzione di sicurezza nel menu **Start.**

> [!Note]  
> Questo metodo può essere usato solo quando è connesso da una sessione del terminale a Microsoft Terminal Server.

 

## <a name="examples"></a>Esempio

Gli esempi seguenti illustrano l'uso di **WindowsSecurity** per JScript, VBScript e Visual Basic.

Jscript:


```JScript
<script language="JScript">
     function fnIShellDispatch4WindowsSecurityJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.WindowsSecurity();
    }
</script>
```



Vbscript:


```VB
<script language="VBScript">
     function fnIShellDispatch4WindowsSecurityVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
            objshell.WindowsSecurity
        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnIShellDispatch4WindowsSecurityVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
        objshell.WindowsSecurity
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop di Windows XP \[\]<br/>                                                                   |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2003 \[\]<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 6.0 o successiva)</dt> </dl> |



 

 




