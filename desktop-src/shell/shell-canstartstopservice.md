---
description: "Metodo Shell.CanStartStopService: determina se l'utente corrente può avviare e arrestare il servizio denominato."
ms.assetid: 1428F529-61F6-4113-A553-2C0D617FD859
title: Metodo Shell.CanStartStopService (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.CanStartStopService
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: a8f4d70d4f4c8a1b8c2745739e2434be0cfde936facd9dbb43cb04c6b7de5c52
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117858044"
---
# <a name="shellcanstartstopservice-method"></a>Metodo Shell.CanStartStopService

Determina se l'utente corrente può avviare e arrestare il servizio denominato.

## <a name="syntax"></a>Sintassi


```JScript
retVal = Shell.CanStartStopService(
  sServiceName
)
```


```VB

Shell.CanStartStopService( _
  ByVal sServiceName As String _
) As Variant
```





## <a name="parameters"></a>Parametri

<dl> <dt>

*sServiceName* \[ Pollici\]
</dt> <dd>

Tipo: **Stringa**

Valore **String** contenente il nome del servizio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

### <a name="jscript"></a>JScript

Tipo: **\* Variante**

Restituisce **true se** l'utente può avviare e arrestare il servizio. in caso contrario, **false**.

### <a name="vb"></a>VB

Tipo: **\* Variante**

Restituisce **true se** l'utente può avviare e arrestare il servizio. in caso contrario, **false**.

## <a name="remarks"></a>Commenti

Questo metodo non è attualmente disponibile in Microsoft Visual Basic.

## <a name="examples"></a>Esempio

Gli esempi seguenti illustrano l'utilizzo di **CanStartStopService** per JScript e VBScript.

JScript:


```JScript
<script language="JScript">
    function fnCanStartStopServiceJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var bReturn;

        bReturn = objShell.CanStartStopService("service name");
    }
</script>
```



Vbscript:


```VB
<script language="VBScript">
    function fnCanStartStopServiceVB()
        dim objShell
        dim bReturn

        set objShell = CreateObject("shell.application")

        bReturn = objShell.CanStartStopService("service name")

        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, Windows solo app \[ desktop XP\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 5.0 o successiva)</dt> </dl> |



 

 




