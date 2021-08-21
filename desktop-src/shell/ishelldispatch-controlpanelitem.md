---
description: Esegue l'applicazione Pannello di controllo specificata.
title: Metodo IShellDispatch.ControlPanelItem (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.ControlPanelItem
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 9A9B6B3F-FBBC-4e76-8018-8858B6392276
ms.openlocfilehash: 89ea8431df7e8cac09a041bd9a16c805633cd3ec82a2cc506cb30fcf0f0cd39b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032259"
---
# <a name="ishelldispatchcontrolpanelitem-method"></a>Metodo IShellDispatch.ControlPanelItem

Esegue l'applicazione Pannello di controllo specificata. Se l'applicazione è già aperta, attiverà l'istanza in esecuzione.

> [!Note]  
> A Windows Vista, la maggior parte Pannello di controllo applicazioni sono elementi della shell e non possono essere aperti con questa funzione. Per aprire tali Pannello di controllo applicazioni, passare il nome canonico a control.exe. Ad esempio:
>
> ``` syntax
> control.exe /name Microsoft.Personalization
> ```

 

## <a name="syntax"></a>Sintassi


```JScript
IShellDispatch.ControlPanelItem(
  bstrDir
)
```


```VB

IShellDispatch.ControlPanelItem( _
  ByVal bstrDir As BSTR _
)
```





## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrDir* \[ Pollici\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Nome Pannello di controllo file dell'applicazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

### <a name="jscript"></a>JScript

Questo metodo non restituisce valori.

### <a name="vb"></a>VB

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo viene implementato e accessibile tramite il [**metodo Shell.ControlPanelItem.**](shell-controlpanelitem.md)

## <a name="examples"></a>Esempio

Gli esempi seguenti usano [**ControlPanelItem**](shell-controlpanelitem.md) per eseguire l'Pannello di controllo **dell'Proprietà dello schermo** elemento. L'utilizzo viene visualizzato JScript, VBScript e Visual Basic.

JScript:


```JScript
<script language="JScript">
    function fnShellControlPanelItemJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.Shell_ControlPanelItem("desk.cpl");
    }
</script>
```



Vbscript:


```VB
<script language="VBScript">
    function fnShellControlPanelItemVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.Shell_ControlPanelItem("desk.cpl")
       
        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnShellControlPanelItemVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.Shell_ControlPanelItem ("desk.cpl")
    
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



 

 
