---
description: Visualizza l'interfaccia utente predefinita per la creazione di un elemento preferito. L'interfaccia utente viene inizializzata sui parametri specificati.
title: Metodo ShellUIHelper.AddFavorite (Exdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellUIHelper.AddFavorite
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: b30e776e-642c-4599-b83f-ef15bc0b23d2
ms.openlocfilehash: 2ce6fa0a71bb2ab995e510f06b4403c78bebcc60
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842452"
---
# <a name="shelluihelperaddfavorite-method"></a>Metodo ShellUIHelper.AddFavorite

Visualizza l'interfaccia utente predefinita per la creazione di un elemento preferito. L'interfaccia utente viene inizializzata sui parametri specificati.

## <a name="syntax"></a>Sintassi


```JScript
iRetVal = ShellUIHelper.AddFavorite(
  sURL,
  [ vTitle ]
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*sURL* \[ Pollici\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Valore **String** che specifica l'URL dell'elemento da aggiungere alla **cartella** Preferiti.

</dd> <dt>

*vTitle* \[ in, facoltativo\]
</dt> <dd>

Tipo: **\* Variante**

Valore **Variant** che specifica il nome dell'elemento.

</dd> </dl>

## <a name="examples"></a>Esempio

L'esempio seguente illustra l'utilizzo corretto di questo metodo per JScript incorporato in HTML e Visual Basic.

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
    function fnShellUIHelperAddFavoriteJ()
    {
        ShellUIHelper.AddFavorite("https://www.msn.com", "MSN Home Page");
    }
</script>

</head>
<body onload=fnShellUIHelperAddFavoriteJ()>
</body>
</html>
```



Visual Basic:


```VB
Private Sub fnShellUIHelperAddFavoriteVB()
    Dim objShellUIHelper As ShellUIHelper
    
    Set objShellUIHelper = New ShellUIHelper
        objShellUIHelper.AddFavorite "https://www.msn.com", "MSN Home Page"
    Set objShellUIHelper = Nothing
End Sub
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop di Windows 2000 Professional e Windows XP \[\]<br/>                                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                           |
| Intestazione<br/>                   | <dl> <dt>Exdisp.h</dt> </dl>                            |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 4.71 o successiva)</dt> </dl> |



 

 
