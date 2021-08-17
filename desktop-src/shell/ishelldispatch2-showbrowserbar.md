---
description: 'Metodo IShellDispatch2.ShowBrowserBar: visualizza una barra del browser.'
ms.assetid: 5776370c-3bbf-449b-a8fe-2dbc7d89dd25
title: Metodo IShellDispatch2.ShowBrowserBar (Shldisp.h)
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
ms.openlocfilehash: 0b1380a44d2985b75e77dced43878c85e38d6a21b877fe06d9cdc7c10a8a2002
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120090331"
---
# <a name="ishelldispatch2showbrowserbar-method"></a>Metodo IShellDispatch2.ShowBrowserBar

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

*sCLSID* \[ Pollici\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Stringa **contenente** il formato stringa del CLSID della barra del browser da visualizzare. L'oggetto deve essere registrato come oggetto barra di Explorer con una categoria di componenti \_ CATID InfoBand. Per altre informazioni, vedere [Creazione di barre di Esplorazione personalizzate, bande degli strumenti e fasce da tavolo.](band-objects.md)

</dd> <dt>

*vShow* \[ Pollici\]
</dt> <dd>

Tipo: **Variante**

Impostare su **true per** visualizzare la barra del browser o **su false** per nasconderla.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

### <a name="jscript"></a>JScript

Tipo: **\* Variante**

Restituisce **true se** l'operazione ha esito positivo. in caso contrario, **false**.

### <a name="vb"></a>VB

Tipo: **\* Variante**

Restituisce **true se** l'operazione ha esito positivo. in caso contrario, **false**.

## <a name="remarks"></a>Commenti

Questo metodo viene implementato e accessibile tramite il [**metodo Shell.ShowBrowserBar.**](./shell-showbrowserbar.md)

È possibile visualizzare una delle barre di Explorer standard impostando il *parametro sCLSID* sul CLSID di tale barra di Explorer. Le barre di Explorer standard e le relative stringhe CLSID sono le seguenti:



| Barra di Explorer | Stringa CLSID                           |
|--------------|----------------------------------------|
| Preferiti    | {EFA24E61-B078-11d0-89E4-00C04FC9E26E} |
| Cartelle      | {EFA24E64-B078-11d0-89E4-00C04FC9E26E} |
| Cronologia      | {EFA24E62-B078-11d0-89E4-00C04FC9E26E} |
| Cerca       | {30D02401-6A81-11d0-8274-00C04FD5AE38} |



 

Questo metodo non è attualmente disponibile in Microsoft Visual Basic.

## <a name="examples"></a>Esempio

Gli esempi seguenti illustrano l'uso **di ShowBrowserBar** per visualizzare la **barra del** browser Preferiti. L'utilizzo viene visualizzato per JScript e VBScript.

JScript:


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
| Client minimo supportato<br/> | Windows 2000 Professional, Windows solo app desktop XP \[\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 5.0 o successiva)</dt> </dl> |



 

 
