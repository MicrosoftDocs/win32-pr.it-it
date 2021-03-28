---
description: Recupera l'impostazione di restrizione di un gruppo dal registro di sistema.
ms.assetid: 04275c5f-c3ed-4962-882f-2cce0258a9f4
title: Metodo IShellDispatch2. Unrestricted (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.IsRestricted
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: f666a9ed3407d12eb9cf2c28ae062a9886d7a2cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978066"
---
# <a name="ishelldispatch2isrestricted-method"></a>Metodo IShellDispatch2. Unrestricted

Recupera l'impostazione di restrizione di un gruppo dal registro di sistema.

## <a name="syntax"></a>Sintassi


```JScript
iRetVal = IShellDispatch2.IsRestricted(
  sGroup,
  sRestriction
)
```


```VB

IShellDispatch2.IsRestricted( _
  ByVal sGroup As BSTR, _
  ByVal sRestriction As BSTR _
) As Integer
```





## <a name="parameters"></a>Parametri

<dl> <dt>

*sGroup* \[ in\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

**Stringa** che contiene il nome del gruppo. Questo valore è il nome di una sottochiave del registro di sistema in cui verificare la restrizione.

</dd> <dt>

*sRestriction* \[ in\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

**Stringa** che contiene la restrizione di cui è necessario recuperare il valore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

### <a name="jscript"></a>JScript

Tipo: **integer \** _

Valore della restrizione. Se la restrizione specificata non viene trovata, il valore restituito è 0.

### <a name="vb"></a>VB

Tipo: _*integer \**_

Valore della restrizione. Se la restrizione specificata non viene trovata, il valore restituito è 0.

## <a name="remarks"></a>Commenti

Questo metodo viene implementato e accessibile tramite il metodo [_ *Shell. Unrestricted* *](./shell-isrestricted.md) .

Con la prima **limitazione** viene eseguita la ricerca di un nome di sottochiave che corrisponde a *sGroup* nella chiave seguente.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Policies
```

Le restrizioni vengono dichiarate come valori delle sottochiavi dei singoli criteri. Se la restrizione denominata in *sRestriction* si trova nella sottochiave denominata in *sGroup*, con **restrizioni** viene restituito il valore corrente della restrizione. Se la restrizione non viene trovata **nel \_ \_ computer locale HKEY**, viene controllata la stessa sottochiave in **HKEY \_ Current \_ User**.

Questo metodo non è attualmente disponibile in Microsoft Visual Basic.

## <a name="examples"></a>Esempio

Negli esempi seguenti viene illustrato l'utilizzo di con **restrizioni** per recuperare il valore dei dati della restrizione **undockwithoutlogon** dalla sottochiave di **sistema** . L'utilizzo viene visualizzato per JScript e VBScript.

JScript


```JScript
<script language="JScript">
    function fnIsRestricedJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var lReturn;
        
        lReturn = objShell.IsRestricted("system", "undockwithoutlogon");
        document.write(lReturn);
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnIsRestricedVB()
        dim objShell
        dim lReturn

        set objShell = CreateObject("shell.application")

        lReturn = objShell.IsRestricted("system", "undockwithoutlogon")
        document.write(lReturn)

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



 

 
