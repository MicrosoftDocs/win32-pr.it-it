---
description: "Metodo Shell.IsRestricted: recupera l'impostazione di restrizione di un gruppo dal Registro di sistema."
ms.assetid: C4B3B5C0-7445-483a-885F-5283BD4D4B39
title: Metodo Shell.IsRestricted (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.IsRestricted
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 3e428c914cf95d282fd721071009efc70fcb3a4d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104259"
---
# <a name="shellisrestricted-method"></a>Metodo Shell.IsRestricted

Recupera l'impostazione di restrizione di un gruppo dal Registro di sistema.

## <a name="syntax"></a>Sintassi


```JScript
iRetVal = Shell.IsRestricted(
  sGroup,
  sRestriction
)
```


```VB

Shell.IsRestricted( _
  ByVal sGroup As BSTR, _
  ByVal sRestriction As BSTR _
) As Integer
```





## <a name="parameters"></a>Parametri

<dl> <dt>

*sGroup* \[ Pollici\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Valore **String** contenente il nome del gruppo. Questo valore è il nome di una sottochiave del Registro di sistema in cui verificare la restrizione.

</dd> <dt>

*sRestriction* \[ Pollici\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Valore **String** contenente la restrizione di cui recuperare il valore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

### <a name="jscript"></a>JScript

Tipo: **\* Integer**

Valore della restrizione. Se la restrizione specificata non viene trovata, il valore restituito è 0.

### <a name="vb"></a>VB

Tipo: **\* Integer**

Valore della restrizione. Se la restrizione specificata non viene trovata, il valore restituito è 0.

## <a name="remarks"></a>Commenti

**IsRestricted** cerca prima di tutto un nome di sottochiave che corrisponda *a sGroup* nella chiave seguente.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Policies
```

Le restrizioni vengono dichiarate come valori delle singole sottochiavi dei criteri. Se la restrizione denominata in *sRestriction* viene trovata nella sottochiave denominata in *sGroup*, **IsRestricted** restituisce il valore corrente della restrizione. Se la restrizione non viene trovata in **HKEY \_ LOCAL \_ MACHINE**, la stessa sottochiave viene controllata in **HKEY \_ CURRENT \_ USER**.

Questo metodo non è attualmente disponibile in Microsoft Visual Basic.

## <a name="examples"></a>Esempio

Negli esempi seguenti viene illustrato l'uso di **IsRestricted** per recuperare il valore dei dati della restrizione **undockwithoutlogon** dalla **sottochiave System.** L'utilizzo è illustrato per JScript e VBScript.

Jscript:


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



Vbscript:


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
| Client minimo supportato<br/> | Solo app desktop windows 2000 Professional e Windows XP \[\]<br/>                                        |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2003 \[\]<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 5.0 o successiva)</dt> </dl> |



 

 
