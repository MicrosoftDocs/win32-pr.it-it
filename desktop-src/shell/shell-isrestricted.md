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
ms.openlocfilehash: 40e6c23f14b3c09a6cfe4885cc7b7bf877e3e4bfbf538645cf96b99ea451776f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968550"
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

Valore **String** che contiene il nome del gruppo. Questo valore è il nome di una sottochiave del Registro di sistema in cui verificare la restrizione.

</dd> <dt>

*sRestriction* \[ Pollici\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Valore **String** che contiene la restrizione il cui valore deve essere recuperato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

### <a name="jscript"></a>JScript

Tipo: **\* Integer**

Valore della restrizione. Se la restrizione specificata non viene trovata, il valore restituito è 0.

### <a name="vb"></a>VB

Tipo: **\* Integer**

Valore della restrizione. Se la restrizione specificata non viene trovata, il valore restituito è 0.

## <a name="remarks"></a>Commenti

**IsRestricted** cerca innanzitutto un nome di sottochiave che corrisponde *a sGroup* nella chiave seguente.

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

Negli esempi seguenti viene illustrato l'uso di **IsRestricted** per recuperare il valore dei dati della restrizione **undockwithoutlogon** dalla **sottochiave System.** L'utilizzo viene visualizzato per JScript e VBScript.

JScript:


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
| Client minimo supportato<br/> | Windows 2000 Professional, Windows solo app desktop XP \[\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 5.0 o successiva)</dt> </dl> |



 

 
