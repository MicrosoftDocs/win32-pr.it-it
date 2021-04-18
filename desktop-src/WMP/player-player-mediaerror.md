---
title: Evento Player. errore MediaError
description: L'evento errore MediaError si verifica quando l'oggetto multimediale presenta una condizione di errore.
ms.assetid: b2e0176a-cc52-4f59-8894-440f426a1b6e
keywords:
- Media Player di Windows Event errore MediaError
- Windows Event errore MediaError Media Player, classe Player
- Classe Player Windows Media Player, evento errore MediaError
topic_type:
- apiref
api_name:
- Player.MediaError
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec8c22825f4aa720efa85275ce520eb81f082fd9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329918"
---
# <a name="playermediaerror-event"></a>Evento Player. errore MediaError

L'evento **errore MediaError** si verifica quando l'oggetto **multimediale** presenta una condizione di errore.

## <a name="syntax"></a>Sintassi


```JScript
Player.MediaError(
  pMediaObject
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pMediaObject* 
</dt> <dd>

Oggetto **multimediale** con una condizione di errore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Il valore dei parametri evento viene specificato da Windows Media Player ed è possibile accedervi o passarli a un metodo in un file JScript importato usando il nome del parametro specificato. Questo nome di parametro deve essere digitato esattamente come illustrato, incluse le maiuscole.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player per Windows XP o versione successiva.<br/>                           |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Player**](player-object.md)
</dt> </dl>

 

 





