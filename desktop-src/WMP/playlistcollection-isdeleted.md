---
title: Metodo PlaylistCollection.isDeleted
description: Il metodo isDeleted recupera un valore che indica se la playlist specificata si trova nella cartella degli elementi eliminati.
ms.assetid: 5023927a-5d1a-4b61-8122-476947d537c4
keywords:
- Metodo isDeleted Windows Media Player
- Metodo isDeleted Windows Media Player , classe PlaylistCollection
- Metodo della classe PlaylistCollection Windows Media Player , isDeleted
topic_type:
- apiref
api_name:
- PlaylistCollection.isDeleted
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a59f6ad587740911d55ae2837607c651e3f3be875bfb24f8bfa765ba415e9bc0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119862201"
---
# <a name="playlistcollectionisdeleted-method"></a>Metodo PlaylistCollection.isDeleted

Il **metodo isDeleted** recupera un valore che indica se la playlist specificata si trova nella cartella degli elementi eliminati.

## <a name="syntax"></a>Sintassi


```JScript
bRetVal = PlaylistCollection.isDeleted(
  playlist
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*playlist* \[ Pollici\]
</dt> <dd>

Oggetto **Playlist** da cercare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un valore **booleano**.

**Windows Media Player 10 Mobile:** questo metodo restituisce sempre **false.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0, Windows Media Player versione 7.1 o Windows Media Player per Windows XP. Questo metodo non è supportato per Windows Media Player serie 9 o successive.<br/> |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl>                                                                                                              |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto PlaylistCollection**](playlistcollection-object.md)
</dt> </dl>

 

 





