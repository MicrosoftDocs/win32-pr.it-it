---
description: 'Metodo IShellDispatch2.ServiceStart: avvia un servizio denominato.'
ms.assetid: 3af57cdc-f449-433d-a9e1-119038045e4c
title: Metodo IShellDispatch2.ServiceStart (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.ServiceStart
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: f48d13e593898b7b4f91fc9246745b183b928ffaa0a799100990a327a3f670ba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120090341"
---
# <a name="ishelldispatch2servicestart-method"></a>Metodo IShellDispatch2.ServiceStart

Avvia un servizio denominato.

## <a name="syntax"></a>Sintassi


```JScript
retVal = IShellDispatch2.ServiceStart(
  sServiceName,
  vPersistent
)
```


```VB

IShellDispatch2.ServiceStart( _
  ByVal sServiceName As BSTR, _
  ByVal vPersistent As Variant _
) As Variant
```





## <a name="parameters"></a>Parametri

<dl> <dt>

*sServiceName* \[ Pollici\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Valore **String** contenente il nome del servizio.

</dd> <dt>

*vPersistent* \[ Pollici\]
</dt> <dd>

Tipo: **Variant**

Impostare su **true per fare** in modo che il servizio sia avviato automaticamente da Gestione controllo servizi durante l'avvio del sistema. Impostare su **false per** lasciare invariata la configurazione del servizio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

### <a name="jscript"></a>JScript

Tipo: **\* Variante**

Restituisce **true se** ha esito positivo; in caso contrario, **false.**

### <a name="vb"></a>VB

Tipo: **\* Variante**

Restituisce **true se** ha esito positivo; in caso contrario, **false.**

## <a name="remarks"></a>Commenti

Questo metodo viene implementato e accessibile tramite il [**metodo Shell.ServiceStart.**](./shell-servicestart.md)

Il metodo restituisce **false** se il servizio è già stato avviato. Prima di chiamare questo metodo, è possibile chiamare [**Shell.IsServiceRunning**](./shell-isservicerunning.md) per verificare lo stato del servizio.

Questo metodo non è attualmente disponibile in Microsoft Visual Basic.

## <a name="examples"></a>Esempio

Gli esempi seguenti illustrano l'uso **di ServiceStart** per avviare il servizio Messenger. L'utilizzo viene visualizzato per JScript e VBScript.

JScript:


```JScript
<script language="JScript">
    function fnServiceStartJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var bReturn;
        
        bReturn = objShell.ServiceStart("Messenger", true);
    }
</script>
```



Vbscript:


```VB
<script language="VBScript">
    function fnServiceStartVB()
        dim objShell
        dim bReturn

        set objShell = CreateObject("shell.application")

        bReturn = objShell.ServiceStart("Messenger", true)

        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, Windows solo app \[ desktop XP\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 5.0 o successiva)</dt> </dl> |



 

 
