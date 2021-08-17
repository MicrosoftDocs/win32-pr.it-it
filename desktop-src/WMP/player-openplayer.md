---
title: Metodo Player.openPlayer
description: Il metodo openPlayer apre Windows Media Player usando l'URL specificato. | Metodo Player.openPlayer
ms.assetid: 9ddd63c9-f4a0-490a-8543-51ad0fa74a26
keywords:
- Metodo openPlayer Windows Media Player
- Metodo openPlayer Windows Media Player , classe Player
- Classe Player Windows Media Player , metodo openPlayer
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
ms.openlocfilehash: 42245ec29f7d7caeac17f116d1f592f74f10ba95716d5d16734ecd21bbcbb60d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117747569"
---
# <a name="playeropenplayer-method"></a>Metodo Player.openPlayer

Il **metodo openPlayer** apre Windows Media Player usando l'URL specificato.

## <a name="syntax"></a>Sintassi


```JScript
Player.openPlayer(
  URL
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*URL* \[ Pollici\]
</dt> <dd>

**Stringa** che rappresenta l'URL dell'elemento multimediale da riprodurre.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo avvia Windows Media Player con l'URL specificato impostato come elemento multimediale corrente. Se il lettore è stato chiuso in precedenza in modalità interfaccia, si aprirà usando l'ultima interfaccia scelta dall'utente. In caso contrario, il lettore viene aperto in modalità completa.

Se questo metodo viene chiamato da un Windows Media PlayerActiveX incorporato in modalità remota, il relativo comportamento è identico a quello di *PlayerApplication.* **Metodo switchToPlayerApplication.**

**Windows Media Player 10 Mobile:** Questo metodo non è supportato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player serie 9 o successiva.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Player**](player-object.md)
</dt> <dt>

[**PlayerApplication.switchToPlayerApplication**](playerapplication-switchtoplayerapplication.md)
</dt> </dl>

 

 





