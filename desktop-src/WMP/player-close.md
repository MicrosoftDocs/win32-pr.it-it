---
title: Metodo Player.close
description: Il metodo close rilascia Windows Media Player risorse.
ms.assetid: 15bd5a05-dbfa-4bea-90c2-afd9f69631e0
keywords:
- Metodo close Windows Media Player
- Metodo close Windows Media Player , classe Player
- Classe Player Windows Media Player , metodo close
topic_type:
- apiref
api_name:
- Player.close
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a29e68aed11b095dff80c8c91c88410f98b9a236bbcadcbff75da0fc0de392fa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119467881"
---
# <a name="playerclose-method"></a>Metodo Player.close

Il **metodo close** rilascia Windows Media Player risorse.

## <a name="syntax"></a>Sintassi


```JScript
Player.close()
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo chiude il file multimediale digitale corrente, non Windows Media Player stesso.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene creato un elemento BUTTON HTML che, quando selezionato, interrompe la riproduzione Windows Media Player e rilascia le risorse in uso. **L'oggetto Player** è stato creato con ID = "Player".


```JScript
<INPUT  TYPE = "BUTTON"  ID = "CLOSEIT"  VALUE = "Close it"  onClick = "

        /* Close the Player object. */
        Player.close();
">

```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Player**](player-object.md)
</dt> </dl>

 

 





