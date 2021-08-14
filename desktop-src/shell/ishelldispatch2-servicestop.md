---
description: 'Metodo IShellDispatch2.ServiceStop: arresta un servizio denominato.'
ms.assetid: f4cd0e2c-4ecc-4e9f-a0b5-d2a8a739f0e2
title: Metodo IShellDispatch2.ServiceStop (Shldisp.h)
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
ms.openlocfilehash: 71bc0502d45e4092decfe1b712ed11f75a02bf50d112436ad1d21f9e02c17e72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118221022"
---
# <a name="ishelldispatch2servicestop-method"></a>Metodo IShellDispatch2.ServiceStop

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

*sServiceName* \[ Pollici\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Valore **String** contenente il nome del servizio.

</dd> <dt>

*vPersistent* \[ Pollici\]
</dt> <dd>

Tipo: **Variante**

Impostare su **true per** fare in modo che il servizio sia avviato da Gestione controllo servizi quando viene [**chiamato ServiceStart.**](ishelldispatch2-servicestart.md) Per lasciare invariata la configurazione del servizio, *impostare vPersistent* su **false.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

### <a name="jscript"></a>JScript

Tipo: **\* Variante**

Restituisce **true se** ha esito positivo; in caso contrario, **false.**

### <a name="vb"></a>VB

Tipo: **\* Variante**

Restituisce **true se** ha esito positivo; in caso contrario, **false.**

## <a name="remarks"></a>Commenti

Questo metodo viene implementato e accessibile tramite il [**metodo Shell.ServiceStop.**](./shell-servicestop.md)

Il metodo restituisce **false** se il servizio è già stato arrestato. Prima di chiamare questo metodo, è possibile chiamare [**Shell.IsServiceRunning**](./shell-isservicerunning.md) per verificare lo stato del servizio.

Questo metodo non è attualmente disponibile in Microsoft Visual Basic.

## <a name="examples"></a>Esempio

Gli esempi seguenti illustrano l'uso **di ServiceStop** per arrestare il servizio Messenger. L'utilizzo viene visualizzato JScript e VBScript.

JScript:


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



Vbscript:


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
| Client minimo supportato<br/> | Windows 2000 Professional, Windows solo app desktop XP \[\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 5.0 o successiva)</dt> </dl> |



 

 
