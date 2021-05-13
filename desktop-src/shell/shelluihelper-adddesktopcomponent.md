---
description: Aggiunge un elemento a Microsoft Active Desktop.
title: Metodo ShellUIHelper.AddDesktopComponent (Exdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellUIHelper.AddDesktopComponent
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 41634a89-15b9-41c8-ba3f-4bf19b786f6f
ms.openlocfilehash: 2edaa79bd62dcee40e4f197700d2128cb0b2070d
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842462"
---
# <a name="shelluihelperadddesktopcomponent-method"></a>Metodo ShellUIHelper.AddDesktopComponent

Aggiunge un elemento a Microsoft Active Desktop.

## <a name="syntax"></a>Sintassi


```JScript
iRetVal = ShellUIHelper.AddDesktopComponent(
  sURL,
  sType,
  [ Left ],
  [ Top ],
  [ Width ],
  [ Height ]
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*sURL* \[ Pollici\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Valore **String** che specifica l'URL del nuovo elemento preferito.

</dd> <dt>

*sType* \[ Pollici\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Valore **String** che specifica il tipo di elemento aggiunto. Può essere uno dei valori seguenti.

<dt>



 (immagine)


</dt> <dd>

Il componente è un'immagine.

</dd> <dt>



 (sito Web)


</dt> <dd>

Il componente è un sito Web.

</dd> </dl> </dd> <dt>

*A sinistra* \[ in, facoltativo\]
</dt> <dd>

Tipo: **Variante**

Posizione del bordo sinistro del componente, in coordinate dello schermo.

</dd> <dt>

*In alto* \[ in, facoltativo\]
</dt> <dd>

Tipo: **Variante**

Posizione del bordo superiore del componente, in coordinate dello schermo.

</dd> <dt>

*Larghezza* \[ in, facoltativo\]
</dt> <dd>

Tipo: **Variant**

Larghezza del componente, in unità dello schermo.

</dd> <dt>

*Altezza* \[ in, facoltativo\]
</dt> <dd>

Tipo: **Variant**

Altezza del componente, in unità dello schermo.

</dd> </dl>

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato l'utilizzo corretto di questo metodo per JScript incorporato in HTML e Visual Basic.

Jscript:


```JScript
<html>
<head>
<title></title>

<object id="ShellUIHelper"
        classid="CLSID:64AB4BB7-111E-11d1-8F79-00C04FC2FBE1"
        width=0
        height=0
        VIEWASTEXT>
</object>

<script language="JavaScript">
    function fnShellUIHelperAddDesktopComponentJ()
    {
        ShellUIHelper.AddDesktopComponent("https://www.microsoft.com/", "website");
    }
</script>

</head>
<body onload=fnShellUIHelperAddDesktopComponentJ()>
</body>
</html>
```



Visual Basic:


```VB
Private Sub fnShellUIHelperAddDesktopComponentVB()
    Dim objShellUIHelper As ShellUIHelper
    
    Set objShellUIHelper = New ShellUIHelper
        objShellUIHelper.AddDesktopComponent "https://www.microsoft.com/", "website"
    Set objShellUIHelper = Nothing
End Sub
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, solo app desktop di Windows XP \[\]<br/>                                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                           |
| Intestazione<br/>                   | <dl> <dt>Exdisp.h</dt> </dl>                            |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 4.71 o successiva)</dt> </dl> |



 

 
