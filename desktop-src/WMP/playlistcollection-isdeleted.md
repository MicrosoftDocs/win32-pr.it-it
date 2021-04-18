---
title: PlaylistCollection. Metodo eliminato
description: Il metodo IsValid recupera un valore che indica se la playlist specificata si trova nella cartella Deleted Items.
ms.assetid: 5023927a-5d1a-4b61-8122-476947d537c4
keywords:
- Metodo eliminato Media Player Windows
- Metodo di eliminazione di Windows Media Player, Classe PlaylistCollection
- Classe PlaylistCollection Windows Media Player, metodo eliminato
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
ms.openlocfilehash: 3fed3e7e8ff41f23d0f9f741ea99f3382d20532e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329429"
---
# <a name="playlistcollectionisdeleted-method"></a>PlaylistCollection. Metodo eliminato

Il **Metodo IsValid** recupera un valore che indica se la playlist specificata si trova nella cartella Deleted Items.

## <a name="syntax"></a>Sintassi


```JScript
bRetVal = PlaylistCollection.isDeleted(
  playlist
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*playlist* \[ in\]
</dt> <dd>

Oggetto **playlist** da cercare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un **valore booleano**.

**Windows Media Player 10 Mobile**: questo metodo restituisce sempre **false**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0, Windows Media Player versione 7,1 o Windows Media Player per Windows XP. Questo metodo non è supportato per Windows Media Player 9 Series o versioni successive.<br/> |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl>                                                                                                              |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PlaylistCollection (oggetto)**](playlistcollection-object.md)
</dt> </dl>

 

 





