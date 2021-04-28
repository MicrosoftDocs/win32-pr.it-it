---
description: 'Metodo IShellDispatch2.IsServiceRunning: restituisce un valore che indica se un determinato servizio è in esecuzione.'
ms.assetid: 91f3fba1-7aa5-423a-bc37-49db230c79db
title: Metodo IShellDispatch2.IsServiceRunning (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.IsServiceRunning
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: e8ad792f1669a8ebcfa411c58b34da214ccf69a7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117089"
---
# <a name="ishelldispatch2isservicerunning-method"></a>Metodo IShellDispatch2.IsServiceRunning

Restituisce un valore che indica se un determinato servizio è in esecuzione.

## <a name="syntax"></a>Sintassi


```JScript
retVal = IShellDispatch2.IsServiceRunning(
  sServiceName
)
```


```VB

IShellDispatch2.IsServiceRunning( _
  ByVal sServiceName As BSTR _
) As Variant
```





## <a name="parameters"></a>Parametri

<dl> <dt>

*sServiceName* \[ Pollici\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Valore **String** contenente il nome del servizio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

### <a name="jscript"></a>JScript

Tipo: **\* Variante**

Restituisce **true** se il servizio specificato da *sServiceName è* in esecuzione; in caso contrario, **false**.

### <a name="vb"></a>VB

Tipo: **\* Variante**

Restituisce **true** se il servizio specificato da *sServiceName è* in esecuzione; in caso contrario, **false**.

## <a name="remarks"></a>Commenti

Questo metodo viene implementato e accessibile tramite il [**metodo Shell.IsServiceRunning.**](./shell-isservicerunning.md)

Questo metodo non è attualmente disponibile in Microsoft Visual Basic.

## <a name="examples"></a>Esempio

Gli esempi seguenti illustrano l'uso di **IsServiceRunning** per determinare se il servizio Temi è in esecuzione per un'applicazione. L'utilizzo è illustrato per JScript e VBScript.

Jscript:


```JScript
<script language="JScript">
    function fnIsServiceRunningJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var bReturn;
    
        bReturn = objShell.IsServiceRunning("Themes");
    }
</script>
```



Vbscript:


```VB
<script language="VBScript">
    function fnIsServiceRunningVB()
        dim objShell
        dim bReturn
    
        set objShell = CreateObject("shell.application")
    
        bReturn = objShell.IsServiceRunning("Themes")
    
        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop windows 2000 Professional e Windows XP \[\]<br/>                                        |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2003 \[\]<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 5.0 o successiva)</dt> </dl> |



 

 
