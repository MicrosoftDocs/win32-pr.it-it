---
description: Visualizza una barra del browser.
ms.assetid: 5776370c-3bbf-449b-a8fe-2dbc7d89dd25
title: Metodo IShellDispatch2. ShowBrowserBar (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.ShowBrowserBar
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: e1df729401dd12b8221ba98a3b81ea65569113e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978015"
---
# <a name="ishelldispatch2showbrowserbar-method"></a>IShellDispatch2. ShowBrowserBar, metodo

Visualizza una barra del browser.

## <a name="syntax"></a>Sintassi


```JScript
retVal = IShellDispatch2.ShowBrowserBar(
  sCLSID,
  vShow
)
```


```VB

IShellDispatch2.ShowBrowserBar( _
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

Questo metodo viene implementato e accessibile tramite il metodo [**Shell. ShowBrowserBar**](./shell-showbrowserbar.md) .

È possibile visualizzare una delle barre di Explorer standard impostando il parametro *sCLSID* sul CLSID della barra di Explorer. Le barre di Explorer standard e le relative stringhe CLSID sono le seguenti:



| Barra di Explorer | Stringa CLSID                           |
|--------------|----------------------------------------|
| Preferiti    | {EFA24E61-B078-11d0-89E4-00C04FC9E26E} |
| Cartelle      | {EFA24E64-B078-11d0-89E4-00C04FC9E26E} |
| Cronologia      | {EFA24E62-B078-11d0-89E4-00C04FC9E26E} |
| Cerca       | {30D02401-6A81-11d0-8274-00C04FD5AE38} |



 

Questo metodo non è attualmente disponibile in Microsoft Visual Basic.

## <a name="examples"></a>Esempio

Negli esempi seguenti viene illustrato l'utilizzo di **ShowBrowserBar** per visualizzare la barra del browser **Preferiti** . L'utilizzo viene visualizzato per JScript e VBScript.

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



 

 
