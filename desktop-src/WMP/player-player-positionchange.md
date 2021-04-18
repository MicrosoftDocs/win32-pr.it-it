---
title: Evento Player. PositionChange
description: L'evento PositionChange si verifica quando la posizione corrente dell'elemento multimediale è stata modificata.
ms.assetid: 0561c58c-da5d-438e-adf8-2472405c6b9e
keywords:
- Media Player di Windows Event PositionChange
- Windows Event PositionChange Media Player, classe Player
- Classe Player Windows Media Player, evento PositionChange
topic_type:
- apiref
api_name:
- Player.PositionChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0ab7f64d6f5c4a081b8a81a14e3fcb353e1478e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327717"
---
# <a name="playerpositionchange-event"></a>Evento Player. PositionChange

L'evento **PositionChange** si verifica quando la posizione corrente dell'elemento multimediale è stata modificata.

## <a name="syntax"></a>Sintassi


```JScript
Player.PositionChange(
  oldPosition,
  newPosition
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*oldPosition* 
</dt> <dd>

Numero (**Double**) che specifica la posizione precedente.

</dd> <dt>

*newPosition* 
</dt> <dd>

**Numero** (**Double**) che specifica la nuova posizione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Questo evento non viene generato periodicamente durante la riproduzione. Si verifica solo quando un elemento modifica attivamente la posizione corrente dell'elemento multimediale in riproduzione, ad esempio l'utente che sposta il handle di ricerca o il codice specificando un valore per i *controlli*. **currentPosition**.

Il valore dei parametri evento viene specificato da Windows Media Player ed è possibile accedervi o passarli a un metodo in un file JScript importato usando il nome del parametro specificato. Questo nome di parametro deve essere digitato esattamente come illustrato, incluse le maiuscole.

**Windows Media Player 10 Mobile:** Questo evento non è supportato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Player**](player-object.md)
</dt> </dl>

 

 





