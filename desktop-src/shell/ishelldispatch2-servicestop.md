---
description: Arresta un servizio denominato.
ms.assetid: f4cd0e2c-4ecc-4e9f-a0b5-d2a8a739f0e2
title: Metodo IShellDispatch2. ServiceStop (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.ServiceStop
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 6a4a76c1f53309c14875eeaf6f3f4c0839a511bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978018"
---
# <a name="ishelldispatch2servicestop-method"></a>IShellDispatch2. ServiceStop, metodo

Arresta un servizio denominato.

## <a name="syntax"></a>Sintassi


```JScript
retVal = IShellDispatch2.ServiceStop(
  sServiceName,
  vPersistent
)
```


```VB

IShellDispatch2.ServiceStop( _
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

Impostare su **true** per fare in modo che il servizio venga avviato da Gestione controllo servizi quando viene chiamato il metodo [**ServiceStart**](ishelldispatch2-servicestart.md) . Per lasciare invariata la configurazione del servizio, impostare *vPersistent* su **false**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

### <a name="jscript"></a>JScript

Tipo: **Variant \** _

Restituisce _ *true** se ha esito positivo; in caso contrario, **false**.

### <a name="vb"></a>VB

Tipo: **Variant \** _

Restituisce _ *true** se ha esito positivo; in caso contrario, **false**.

## <a name="remarks"></a>Commenti

Questo metodo viene implementato e accessibile tramite il metodo [**Shell. ServiceStop**](./shell-servicestop.md) .

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



 

 
