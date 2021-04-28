---
description: 'Metodo Shell.ShowBrowserBar: visualizza una barra del browser.'
ms.assetid: 203636D2-54D3-4163-B9AC-39213D6F4203
title: Metodo Shell.ShowBrowserBar (Shldisp.h)
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
ms.openlocfilehash: d19cd5b98ce39470860cc481ab05e4bb41adc9a4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083725"
---
# <a name="shellshowbrowserbar-method"></a>Metodo Shell.ShowBrowserBar

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

*sCLSID* \[ Pollici\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Valore **String** contenente il formato stringa del CLSID della barra del browser da visualizzare. L'oggetto deve essere registrato come oggetto barra di Explorer con una categoria di \_ componenti CATID InfoBand. Per altre informazioni, vedere [Creating Custom Explorer Bars, Tool Bands, and Desk Bands](band-objects.md).

</dd> <dt>

*vShow* \[ Pollici\]
</dt> <dd>

Tipo: **Variante**

Impostare su **true per** visualizzare la barra del browser o **su false** per nasconderla.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

### <a name="jscript"></a>JScript

Tipo: **\* Variant**

Restituisce **true se** ha esito positivo; in caso contrario, **false.**

### <a name="vb"></a>VB

Tipo: **\* Variant**

Restituisce **true se** ha esito positivo; in caso contrario, **false.**

## <a name="remarks"></a>Commenti

È possibile visualizzare una delle barre di Explorer standard impostando il *parametro sCLSID* sul CLSID di tale barra di Explorer. Le barre di Explorer standard e le relative stringhe CLSID sono le seguenti:



| Barra di Explorer | Stringa CLSID                           |
|--------------|----------------------------------------|
| Preferiti    | {EFA24E61-B078-11d0-89E4-00C04FC9E26E} |
| Cartelle      | {EFA24E64-B078-11d0-89E4-00C04FC9E26E} |
| Cronologia      | {EFA24E62-B078-11d0-89E4-00C04FC9E26E} |
| Cerca       | {30D02401-6A81-11d0-8274-00C04FD5AE38} |



 

Questo metodo non è attualmente disponibile in Microsoft Visual Basic.

## <a name="examples"></a>Esempio

Gli esempi seguenti illustrano l'uso di **Shell.ShowBrowserBar** per visualizzare la **barra del** browser Preferiti. L'utilizzo è illustrato per JScript e VBScript.

Jscript:


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



Vbscript:


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
| Client minimo supportato<br/> | Solo app desktop windows 2000 Professional e Windows XP \[\]<br/>                                        |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2003 \[\]<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 5.0 o successiva)</dt> </dl> |



 

 
