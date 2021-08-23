---
title: Metodo MediaCollection.getAll
description: Il metodo getAll recupera una playlist contenente tutti gli elementi multimediali nella libreria.
ms.assetid: c22532ee-5714-4762-966f-7dc6543384f4
keywords:
- Metodo getAll Windows Media Player
- Metodo getAll Windows Media Player , classe MediaCollection
- Classe MediaCollection Windows Media Player metodo , getAll
topic_type:
- apiref
api_name:
- MediaCollection.getAll
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1d3bba961f9400470c16e3d773a5765d389ce05bc23c2e948f0b94c7ad22229
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135065"
---
# <a name="mediacollectiongetall-method"></a>Metodo MediaCollection.getAll

Il **metodo getAll** recupera una playlist contenente tutti gli elementi multimediali nella libreria.

## <a name="syntax"></a>Sintassi


```JScript
retVal = MediaCollection.getAll()
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un **oggetto Playlist.**

## <a name="remarks"></a>Commenti

Per usare questo metodo, è necessario l'accesso in lettura alla libreria. Per altre informazioni, vedere [Accesso alla libreria](library-access.md).

## <a name="examples"></a>Esempio

Nell'JScript seguente viene utilizzato *MediaCollection*. **getAll per** riprodurre elementi multimediali in modo casuale dalla raccolta di supporti. **L'oggetto** Player è stato creato con ID = "Player".


```JScript
// Store the count of all media items in the media collection.
var count = Player.mediaCollection.getAll().count;

// Generate a random number using the media count.
var rand = Math.random() * count;

// Round down the random number to the nearest integer.
rand = Math.floor(rand);

// Make the random media item the current media item.
Player.currentMedia = Player.mediaCollection.getAll().item(rand);

// Play the media item.
// Player.controls.play();

```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto MediaCollection**](mediacollection-object.md)
</dt> <dt>

[**Oggetto Playlist**](playlist-object.md)
</dt> <dt>

[**Impostazioni.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Impostazioni.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





