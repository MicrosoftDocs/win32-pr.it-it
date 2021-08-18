---
title: Metodo Playlist.insertItem
description: Il metodo insertItem inserisce un elemento multimediale nella playlist nella posizione specificata.
ms.assetid: c186abc4-0a15-49d2-bbc4-5660e8cc0a4b
keywords:
- Metodo insertItem Windows Media Player
- Metodo insertItem Windows Media Player , classe Playlist
- Classe Playlist Windows Media Player , metodo insertItem
topic_type:
- apiref
api_name:
- Playlist.insertItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a71d9ceb39b29c1627ea7596166c39b3dc2f6c76faf45e5ffb54bea14154ac2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995701"
---
# <a name="playlistinsertitem-method"></a>Metodo Playlist.insertItem

Il **metodo insertItem** inserisce un elemento multimediale nella playlist nella posizione specificata.

## <a name="syntax"></a>Sintassi


```JScript
Playlist.insertItem(
  index,
  item
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*index* \[ Pollici\]
</dt> <dd>

**Numero** (**long**) contenente l'indice in corrispondenza del quale aggiungere l'elemento.

</dd> <dt>

*item* \[ Pollici\]
</dt> <dd>

**Oggetto** multimediale da inserire.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

I numeri di indice di tutti gli elementi dopo l'elemento inserito saranno aumentati di uno.

Per usare questo metodo, è necessario l'accesso completo alla libreria. Per altre informazioni, vedere [Accesso alla libreria.](library-access.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Playlist**](playlist-object.md)
</dt> <dt>

[**Playlist.item**](playlist-item.md)
</dt> <dt>

[**Playlist.removeItem**](playlist-removeitem.md)
</dt> <dt>

[**Impostazioni.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Impostazioni.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





