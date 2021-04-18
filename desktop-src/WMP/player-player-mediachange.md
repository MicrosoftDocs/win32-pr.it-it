---
title: Evento Player. MediaChange
description: L'evento MediaChange si verifica quando viene modificato un elemento multimediale. | Evento Player. MediaChange
ms.assetid: c4bdd2ae-c51f-4577-b762-bc84aaf52f76
keywords:
- Media Player di Windows Event MediaChange
- Windows Event MediaChange Media Player, classe Player
- Classe Player Windows Media Player, evento MediaChange
topic_type:
- apiref
api_name:
- Player.MediaChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99a63e087356b5d39ae8d751236b8128330c4f3c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331857"
---
# <a name="playermediachange-event"></a>Evento Player. MediaChange

L'evento **MediaChange** si verifica quando viene modificato un elemento multimediale.

## <a name="syntax"></a>Sintassi


```JScript
Player.MediaChange(
  Item
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Item* 
</dt> <dd>

Oggetto **multimediale** che rappresenta l'elemento modificato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Il valore dei parametri evento viene specificato da Windows Media Player ed è possibile accedervi o passarli a un metodo in un file JScript importato usando il nome del parametro specificato. Questo nome di parametro deve essere digitato esattamente come illustrato, incluse le maiuscole.

**Windows Media Player 10 Mobile:** Questo evento non è supportato.

## <a name="examples"></a>Esempio

Nell'esempio JScript seguente viene usato un elemento DIV HTML, denominato MEDIANAME, per visualizzare il nome dell'elemento multimediale corrente. Il codice aggiorna il testo nel DIV con ogni occorrenza dell'evento **mediaChange** . L'oggetto **Player** è stato creato con ID = "Player".


```JScript
<!-- Create an event handler for media change. -->
<SCRIPT FOR = "Player" EVENT = "mediaChange(Item)">
   // Test whether a valid currentMedia object exists.
   if (Player.currentMedia){
      // Display the name of the current media item.
      MediaName.innerHTML = Player.currentMedia.name;
   }
</SCRIPT>

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

 

 





