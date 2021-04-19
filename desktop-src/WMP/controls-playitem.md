---
title: Controls. playItem, metodo
description: Il metodo playItem riproduce l'elemento multimediale specificato. | Controls. playItem, metodo
ms.assetid: 410e315d-8d5f-4f45-82a7-4249e656c809
keywords:
- Metodo playItem Windows Media Player
- Metodo playItem Windows Media Player, classe Controls
- Classe Controls Media Player Windows, metodo playItem
topic_type:
- apiref
api_name:
- Controls.playItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9096e378a328f43147a0a94d97034c8e566b611
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331866"
---
# <a name="controlsplayitem-method"></a>Controls. playItem, metodo

Il metodo **playItem** riproduce l'elemento multimediale specificato.

## <a name="syntax"></a>Sintassi


```JScript
Controls.playItem(
  theMediaItem
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*theMediaItem* \[ in\]
</dt> <dd>

Oggetto **multimediale** da riprodurre.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

L'elemento multimediale verrà caricato e riprodotto automaticamente, indipendentemente dal valore delle *Impostazioni*. Proprietà di **avvio automatico** . Per caricare un elemento senza riprodurlo automaticamente, impostare *le impostazioni*. **avvio automatico** a false e assegnazione di un valore al *lettore*. **URL**, dopo il quale è possibile chiamare **Play** per iniziare a riprodurre l'elemento.

Nota

**playItem** funziona solo con gli elementi in *currentPlaylist*. La chiamata di **playItem** con un riferimento a un elemento multimediale salvato non è supportata.

## <a name="examples"></a>Esempio

Nell'esempio JScript seguente viene usato **playItem** per riprodurre un elemento multimediale dalla playlist corrente. L'elemento da riprodurre viene scelto in base alla relativa posizione nella playlist. L'oggetto **Player** è stato creato con ID = "Player".


```JScript
// Declare a variable to hold the position of the media item 
// in the current playlist. An arbitrary value is supplied here.
var index = 3

// Retrieve the media item at the fourth position in the current playlist.
var media = Player.currentPlaylist.item(index);

// Play the media item.
Player.controls.playItem(media);

```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Controls**](controls-object.md)
</dt> <dt>

[**Playlist. Item**](playlist-item.md)
</dt> </dl>

 

 





