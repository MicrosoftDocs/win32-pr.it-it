---
description: Visualizza una barra del browser.
ms.assetid: 203636D2-54D3-4163-B9AC-39213D6F4203
title: Metodo Shell. ShowBrowserBar (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.ShowBrowserBar
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: d112399e62825714b4c060aeddcb8618ff73d478
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979759"
---
# <a name="shellshowbrowserbar-method"></a>Shell. ShowBrowserBar, metodo

Visualizza una barra del browser.

## <a name="syntax"></a>Sintassi


```JScript
retVal = Shell.ShowBrowserBar(
  sCLSID,
  vShow
)
```


```VB

Shell.ShowBrowserBar( _
  ByVal sCLSID As BSTR, _
  ByVal vShow As Variant _
) As Variant
```





## <a name="parameters"></a>Parametri

<dl> <dt>

*sCLSID* \[ in\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

**Stringa** che contiene il formato stringa del CLSID della barra del browser da visualizzare. L'oggetto deve essere registrato come oggetto della barra di Explorer con una \_ categoria di componenti INFOBAND CATID. Per ulteriori informazioni, vedere [creazione di barre di esplorazione personalizzate, bande di strumenti e bande della scrivania](band-objects.md).

</dd> <dt>

*vShow* \[ in\]
</dt> <dd>

Tipo: **Variant**

Impostare su **true** per visualizzare la barra del browser o **false** per nasconderla.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

### <a name="jscript"></a>JScript

Tipo: **Variant \** _

Restituisce _ *true** se ha esito positivo; in caso contrario, **false**.

### <a name="vb"></a>VB

Tipo: **Variant \** _

Restituisce _ *true** se ha esito positivo; in caso contrario, **false**.

## <a name="remarks"></a>Commenti

È possibile visualizzare una delle barre di Explorer standard impostando il parametro *sCLSID* sul CLSID della barra di Explorer. Le barre di Explorer standard e le relative stringhe CLSID sono le seguenti:



| Barra di Explorer | Stringa CLSID                           |
|--------------|----------------------------------------|
| Preferiti    | {EFA24E61-B078-11d0-89E4-00C04FC9E26E} |
| Cartelle      | {EFA24E64-B078-11d0-89E4-00C04FC9E26E} |
| Cronologia      | {EFA24E62-B078-11d0-89E4-00C04FC9E26E} |
| Cerca       | {30D02401-6A81-11d0-8274-00C04FD5AE38} |



 

Questo metodo non è attualmente disponibile in Microsoft Visual Basic.

## <a name="examples"></a>Esempio

Negli esempi seguenti viene illustrato l'utilizzo di **Shell. ShowBrowserBar** per visualizzare la barra del browser **Preferiti** . L'utilizzo viene visualizzato per JScript e VBScript.

JScript


```JScript
<script language="JavaScript">
    function fnShowBrowserBarJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var bReturn;
        
        bReturn = objShell.ShowBrowserBar("{EFA24E61-B078-11d0-89E4-00C04FC9E26E}", true);
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnShowBrowserBarVB()
        dim objShell
        dim bReturn

        set objShell = CreateObject("shell.application")

        bReturn = objShell.ShowBrowserBar("{EFA24E61-B078-11d0-89E4-00C04FC9E26E}", true)

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



 

 
