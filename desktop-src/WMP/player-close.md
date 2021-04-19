---
title: Player. Close (metodo)
description: Il metodo Close rilascia le risorse di Windows Media Player.
ms.assetid: 15bd5a05-dbfa-4bea-90c2-afd9f69631e0
keywords:
- Chiudi metodo Windows Media Player
- Metodo Close Media Player Windows, classe Player
- Classe Player Windows Media Player, metodo Close
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
ms.openlocfilehash: debc2667c42da92b3a2639e0f14c767d2b5b0651
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329714"
---
# <a name="playerclose-method"></a>Player. Close (metodo)

Il metodo **Close** rilascia le risorse di Windows Media Player.

## <a name="syntax"></a>Sintassi


```JScript
Player.close()
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo chiude il file multimediale digitale corrente, non Windows Media Player.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene creato un elemento BUTTON HTML che, quando selezionato, interrompe la riproduzione in Windows Media Player e rilascia le risorse in uso. L'oggetto **Player** è stato creato con ID = "Player".


```JScript
<INPUT  TYPE = "BUTTON"  ID = "CLOSEIT"  VALUE = "Close it"  onClick = "

        /* Close the Player object. */
        Player.close();
">

```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Player**](player-object.md)
</dt> </dl>

 

 





