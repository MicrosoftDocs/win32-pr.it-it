---
description: Aggiunge un nuovo canale all'elenco di canali nel menu Preferiti Windows Internet Explorer canale e alla barra Dei canali sul desktop.
title: Metodo ShellUIHelper.AddChannel (Exdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellUIHelper.AddChannel
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: b62e6e82-429a-4d41-96d4-cba639b611f5
ms.openlocfilehash: 6be928a7cae9d9349bb39fc3a27a49a16495a8609c8e1cb448de888ac190619b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118047514"
---
# <a name="shelluihelperaddchannel-method"></a>Metodo ShellUIHelper.AddChannel

Aggiunge un nuovo canale all'elenco di canali nel **menu** Preferiti Windows Internet Explorer e alla barra **Dei** canali sul desktop.

> [!Note]  
> Questo metodo non è più supportato in Windows Vista. In tale sistema operativo restituisce E \_ NOTIMPL.

 

## <a name="syntax"></a>Sintassi


```JScript
iRetVal = ShellUIHelper.AddChannel(
  sURL
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*sURL* \[ Pollici\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Valore **String** che specifica l'URL del file CDF.

> [!Note]  
> I collegamenti nel file CDF devono usare protocolli HTTP, HTTPS o FTP. Se il file CDF contiene qualsiasi altro protocollo, l'aggiunta del canale ha esito negativo e non viene visualizzata alcuna finestra di dialogo.

 

</dd> </dl>

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato l'utilizzo corretto di questo metodo JScript incorporato in HTML e Visual Basic.

JScript:


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
    function fnShellUIHelperAddChannelJ()
    {
        ShellUIHelper.AddChannel("https://www.microsoft.com/windows/cdf/g_stock.cdf");
    }
</script>

</head>
<body onload=fnShellUIHelperAddChannelJ()>
</body>
</html>
```



Visual Basic:


```VB
Private Sub fnShellUIHelperAddChannelVB()
    Dim objShellUIHelper As ShellUIHelper
    
    Set objShellUIHelper = New ShellUIHelper
        objShellUIHelper.AddChannel ("https://www.microsoft.com/windows/cdf/g_stock.cdf")
    Set objShellUIHelper = Nothing
End Sub
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, Windows solo app desktop XP \[\]<br/>                                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                           |
| Intestazione<br/>                   | <dl> <dt>Exdisp.h</dt> </dl>                            |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 4.71 o successiva)</dt> </dl> |



 

 
