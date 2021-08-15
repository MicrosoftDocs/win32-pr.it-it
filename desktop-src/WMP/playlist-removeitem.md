---
title: Metodo Playlist.removeItem
description: Il metodo removeItem rimuove l'elemento specificato dalla playlist.
ms.assetid: 294ba4fb-967b-4a03-b0c5-6e9c15db3bff
keywords:
- Metodo removeItem Windows Media Player
- Metodo removeItem Windows Media Player , classe Playlist
- Metodo removeItem della Windows Media Player playlist
topic_type:
- apiref
api_name:
- Playlist.removeItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8a55fb45fa7ea8d172d76321d7c907fbedfd3f868448f1ad63e220ff8e69f9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118336592"
---
# <a name="playlistremoveitem-method"></a>Metodo Playlist.removeItem

Il **metodo removeItem** rimuove l'elemento specificato dalla playlist.

## <a name="syntax"></a>Sintassi


```JScript
Playlist.removeItem(
  item
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*elemento* \[ Pollici\]
</dt> <dd>

**Oggetto** multimediale da rimuovere.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Se l'elemento rimosso è la traccia attualmente in riproduzione (*Player*.**currentMedia**), la riproduzione si arresta e l'elemento successivo nella playlist diventa quello corrente. Se non è presente alcun elemento successivo, viene usato l'elemento precedente o se non sono presenti altri elementi, *player*. **currentMedia** è impostato su **NULL.**

Per usare questo metodo, è necessario l'accesso completo alla libreria. Per altre informazioni, vedere [Accesso alla libreria](library-access.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Player.currentMedia**](player-currentmedia.md)
</dt> <dt>

[**Oggetto Playlist**](playlist-object.md)
</dt> <dt>

[**Playlist.insertItem**](playlist-insertitem.md)
</dt> <dt>

[**Playlist.item**](playlist-item.md)
</dt> <dt>

[**Impostazioni.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Impostazioni.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





