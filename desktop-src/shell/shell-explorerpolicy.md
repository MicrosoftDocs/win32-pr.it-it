---
description: 'Metodo Shell.ExplorerPolicy: ottiene il valore per un criterio Windows Internet Explorer specificato.'
ms.assetid: 47E17F6A-ED43-44cd-AF77-A6E49865E1B5
title: Metodo Shell.ExplorerPolicy (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.ExplorerPolicy
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 78a0e601e8093358ef05f259586726e840982d1a97d428b8453f26ecb878a4c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117857933"
---
# <a name="shellexplorerpolicy-method"></a>Metodo Shell.ExplorerPolicy

Ottiene il valore per un criterio di Windows Internet Explorer specificati.

## <a name="syntax"></a>Sintassi


```JScript
retVal = Shell.ExplorerPolicy(
  bstrPolicyName
)
```


```VB

Shell.ExplorerPolicy( _
  ByVal bstrPolicyName As BSTR _
) As Variant
```





## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrPolicyName* \[ Pollici\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Valore **String** che specifica il nome dei criteri.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

### <a name="jscript"></a>JScript

Tipo: **\* Variante**

Valore associato al nome del criterio specificato.

### <a name="vb"></a>VB

Tipo: **\* Variante**

Valore associato al nome del criterio specificato.

## <a name="remarks"></a>Commenti

Gli amministratori di rete possono controllare e gestire l'ambiente di elaborazione degli utenti impostando criteri.

Il nome del valore specificato deve essere all'interno **della sottochiave HKEY \_ CURRENT \_ USER** \\ **Software** \\ **Windows** \\  \\ **CurrentVersion** \\ **Policies** \\ **Explorer.** Se il nome del valore non esiste, il metodo restituisce **Null.**

## <a name="examples"></a>Esempio

Gli esempi seguenti illustrano l'uso corretto di **ExplorerPolicy** per JScript, VBScript e Visual Basic.

JScript:


```JScript
<script language="JScript">
    function fnIShellDispatch4ExplorerPolicyJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var vReturn;
        
        vReturn = objShell.ExplorerPolicy("ValueName");
        alert(vReturn);
    }
</script>
```



Vbscript:


```VB
<script language="VBScript">
     function fnIShellDispatch4ExplorerPolicyVB()
        dim objShell
        dim vReturn
        
        set objShell = CreateObject("shell.application")
            vReturn = objShell.ExplorerPolicy("ValueName")
            alert(vReturn)
        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnIShellDispatch4ExplorerPolicyVB()
    Dim objShell As Shell
    Dim vReturn  As Variant
    
    Set objShell = New Shell
        vReturn = objShell.ExplorerPolicy("ValueName")
        Debug.Print vReturn
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                                                   |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 6.0 o successiva)</dt> </dl> |



 

 
