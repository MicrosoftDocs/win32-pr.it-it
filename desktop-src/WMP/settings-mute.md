---
title: Impostazioni. mute
description: La proprietà mute specifica e recupera un valore che indica se l'audio è disattivato.
ms.assetid: d6d4b46d-5631-4af7-bd99-21674f067121
keywords:
- Settings. mute Media Player Windows
topic_type:
- apiref
api_name:
- Settings.mute
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7061439e9e091b2ad1cf6be49873d7e3895132b0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327379"
---
# <a name="settingsmute"></a>Impostazioni. mute

La proprietà **mute** specifica e recupera un valore che indica se l'audio è disattivato.

## <a name="syntax"></a>Sintassi

Player. Settings. mute

## <a name="possible-values"></a>Valori possibili

Questa proprietà è un **valore booleano** di lettura/scrittura.



| Valore | Descrizione                  |
|-------|------------------------------|
| true  | Audio disattivato.              |
| false | Valore predefinito. Audio non è disattivato. |



 

## <a name="examples"></a>Esempio

Nell'esempio seguente viene creato un elemento CHECKBOX HTML che consente all'utente di disattivare e disattivare l'audio. L'oggetto **Player** è stato creato con ID = "Player".


```
<!-- Create an HTML CHECKBOX control. -->
<INPUT  TYPE = "CHECKBOX"  ID = MUTE  
             onClick = "
                        /* Use the CHECKBOX state to set 
                           the mute property. */
                        Player.settings.mute = MUTE.checked;
">
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Settings**](settings-object.md)
</dt> </dl>

 

 





