---
description: Aggiunge un elemento a Microsoft Active Desktop.
title: Metodo ShellUIHelper. AddDesktopComponent (Exdisp. h)
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
ms.openlocfilehash: d5234a0b43ea25c8ac931dc14ec90f7a6696ddfb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980591"
---
# <a name="shelluihelperadddesktopcomponent-method"></a>ShellUIHelper. AddDesktopComponent, metodo

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

*surl* \[ in\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Valore **stringa** che specifica l'URL del nuovo elemento preferito.

</dd> <dt>

*sPrevista* \[ in\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Valore **stringa** che specifica il tipo di elemento da aggiungere. Può corrispondere a uno dei valori seguenti.

<dt>



 immagine


</dt> <dd>

Il componente è un'immagine.

</dd> <dt>



 sito Web


</dt> <dd>

Il componente è un sito Web.

</dd> </dl> </dd> <dt>

A *sinistra* \[ in, facoltativo\]
</dt> <dd>

Tipo: **Variant**

Posizione del bordo sinistro del componente, in coordinate dello schermo.

</dd> <dt>

In *alto* \[ in, facoltativo\]
</dt> <dd>

Tipo: **Variant**

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

JScript


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
| Client minimo supportato<br/> | Windows 2000 Professional, \[ solo app desktop Windows XP\]<br/>                                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                           |
| Intestazione<br/>                   | <dl> <dt>Exdisp. h</dt> </dl>                            |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 4,71 o successiva)</dt> </dl> |



 

 
