---
title: Player. openPlayer, metodo
description: Il metodo openPlayer apre Windows Media Player usando l'URL specificato. | Player. openPlayer, metodo
ms.assetid: 9ddd63c9-f4a0-490a-8543-51ad0fa74a26
keywords:
- Metodo openPlayer Windows Media Player
- Metodo openPlayer Windows Media Player, classe Player
- Classe Player Windows Media Player, metodo openPlayer
topic_type:
- apiref
api_name:
- Player.openPlayer
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3378df48f961f1aa5e3fccec72e79b7f1c26ff08
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327067"
---
# <a name="playeropenplayer-method"></a>Player. openPlayer, metodo

Il metodo **openPlayer** apre Windows Media Player usando l'URL specificato.

## <a name="syntax"></a>Sintassi


```JScript
Player.openPlayer(
  URL
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*URL* \[ di in\]
</dt> <dd>

**Stringa** che rappresenta l'URL dell'elemento multimediale da riprodurre.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo avvia Media Player Windows con l'URL specificato impostato come elemento multimediale corrente. Se il lettore è stato chiuso in precedenza in modalità Skin, verrà aperto utilizzando l'ultima interfaccia selezionata dall'utente. In caso contrario, il lettore verrà aperto in modalità completa.

Se questo metodo viene chiamato da un controllo Windows Media PlayerActiveX incorporato in modalità remota, il comportamento è identico a quello di *PlayerApplication*. metodo **switchToPlayerApplication** .

**Windows Media Player 10 Mobile:** Questo metodo non è supportato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player 9 serie o versione successiva.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Player**](player-object.md)
</dt> <dt>

[**PlayerApplication.switchToPlayerApplication**](playerapplication-switchtoplayerapplication.md)
</dt> </dl>

 

 





