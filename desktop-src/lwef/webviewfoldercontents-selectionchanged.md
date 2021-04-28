---
title: Evento WebViewFolderContents.SelectionChanged (Shldisp.h)
description: 'Evento WebViewFolderContents.SelectionChanged: si verifica quando viene modificato lo stato di selezione di uno o più elementi nella visualizzazione.'
ms.assetid: 46dfceec-aa81-4950-81e5-526a6e621271
keywords:
- Funzionalità legacy dell'ambiente Windows per l'evento SelectionChanged
topic_type:
- apiref
api_name:
- SelectionChanged
api_location:
- Shell32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea6176cb2a1703d48cd2ddec8069c65d7efc978f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102659"
---
# <a name="webviewfoldercontentsselectionchanged-event"></a>Evento WebViewFolderContents.SelectionChanged

Si verifica quando lo stato di selezione di uno o più elementi nella visualizzazione viene modificato.

## <a name="syntax"></a>Sintassi


```JScript
function EventHandler()
{
    // Code to handle the event.
}

// Set the event property to the handler.
WebViewFolderContents.SelectionChanged = EventHandler;
```



## <a name="parameters"></a>Parametri

Questo gestore eventi non ha parametri.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato l'utilizzo corretto di questo evento per JScript incorporato in HTML.


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsSelectionChangedJ()
    {
        alert("SelectionChanged event was called");
    }
</script>

<script language="JavaScript" for="FileList" event="SelectionChanged">
    fnWebViewFolderContentsSelectionChangedJ();
</script>

</head>
<body>

...

<object id=FileList classid="clsid:1820FED0-473E-11D0-A96C-00C04FD705A2" tabIndex=1>
</body>
</html>
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, solo app desktop di Windows XP \[\]<br/>                                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                           |
| Intestazione<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 4.71 o successiva)</dt> </dl> |



 

 





