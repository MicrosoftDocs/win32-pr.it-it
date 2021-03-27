---
description: Arresta un servizio denominato.
ms.assetid: AC22C91E-BBC6-4a2e-8D39-F9D7C0AC0947
title: Metodo Shell. ServiceStop (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.ServiceStop
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 31388078fe1c0e15c2e54efc86f0ff76bcfb7ed2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232104"
---
# <a name="shellservicestop-method"></a>Shell. ServiceStop, metodo

Arresta un servizio denominato.

## <a name="syntax"></a>Sintassi


```JScript
retVal = Shell.ServiceStop(
  sServiceName,
  vPersistent
)
```


```VB

Shell.ServiceStop( _
  ByVal sServiceName As BSTR, _
  ByVal vPersistent As Variant _
) As Variant
```





## <a name="parameters"></a>Parametri

<dl> <dt>

*sServiceName* \[ in\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

**Stringa** che contiene il nome del servizio.

</dd> <dt>

*vPersistent* \[ in\]
</dt> <dd>

Tipo: **Variant**

Impostare su **true** per fare in modo che il servizio venga avviato da Gestione controllo servizi quando viene chiamato il metodo [**ServiceStart**](./shell-servicestart.md) . Per lasciare invariata la configurazione del servizio, impostare *vPersistent* su **false**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

### <a name="jscript"></a>JScript

Tipo: **Variant \** _

Restituisce _ *true** se ha esito positivo; in caso contrario, **false**.

### <a name="vb"></a>VB

Tipo: **Variant \** _

Restituisce _ *true** se ha esito positivo; in caso contrario, **false**.

## <a name="remarks"></a>Commenti

Il metodo restituisce **false** se il servizio è già stato arrestato. Prima di chiamare questo metodo, è possibile chiamare [**Shell. IsServiceRunning**](./shell-isservicerunning.md) per verificare lo stato del servizio.

Questo metodo non è attualmente disponibile in Microsoft Visual Basic.

## <a name="examples"></a>Esempio

Gli esempi seguenti illustrano l'uso di **ServiceStop** per arrestare il servizio Messenger. L'utilizzo viene visualizzato per JScript e VBScript.

JScript


```JScript
<script language="JScript">
    function fnServiceStopJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var bReturn;
        
        bReturn = objShell.ServiceStop("Messenger", true);
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnServiceStopVB()
        dim objShell
        dim bReturn

        set objShell = CreateObject("shell.application")

        bReturn = objShell.ServiceStop("Messenger", true)

        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, \[ solo app desktop Windows XP\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 5,0 o successiva)</dt> </dl> |



 

 
