---
title: Media.sourceURL
description: La proprietà sourceURL recupera l'URL dell'elemento multimediale.
ms.assetid: 98ff6ed4-ad3d-44f8-893d-f016e5217ce5
keywords:
- Media.sourceURL Windows Media Player
topic_type:
- apiref
api_name:
- Media.sourceURL
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e2f99aeb64a73bcf36e2cbd472aedfa8f509a5073e70792e7b47343a1b37d60
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119415951"
---
# <a name="mediasourceurl"></a>Media.sourceURL

La **proprietà sourceURL** recupera l'URL dell'elemento multimediale.

## <a name="syntax"></a>Sintassi

*lettore*. *currentMedia*.sourceURL

## <a name="possible-values"></a>Valori possibili

Questa proprietà è una stringa di sola **lettura.**

## <a name="examples"></a>Esempio

Nell'esempio JScript seguente viene utilizzato *Media*. **sourceURL per** recuperare l'URL del primo elemento multimediale nella playlist di esempio. L'URL dell'elemento multimediale viene quindi assegnato alla proprietà **URL dell'oggetto lettore.** **L'oggetto** Player è stato creato con ID = "Player".


```JScript
// Store the sample playlist object in a variable. 
var pl = Player.playlistCollection.getByName("Sample Playlist").item(0);

// Store the first media item from the sample playlist.
var media = pl.item(0);

// Change the URL property of the player to the URL of the media item.
Player.URL = media.sourceURL;

// Play the media item.
Player.controls.play();

```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto multimediale**](media-object.md)
</dt> </dl>

 

 





