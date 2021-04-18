---
title: Playlist. removeItem, metodo
description: Il metodo removeItem rimuove l'elemento specificato dalla playlist.
ms.assetid: 294ba4fb-967b-4a03-b0c5-6e9c15db3bff
keywords:
- Metodo removeItem Windows Media Player
- Metodo removeItem Media Player Windows, classe playlist
- Classe playlist Windows Media Player, metodo removeItem
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
ms.openlocfilehash: 2de03333e2373744f9e9197be8ed8582997c557d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327609"
---
# <a name="playlistremoveitem-method"></a>Playlist. removeItem, metodo

Il metodo **RemoveItem** rimuove l'elemento specificato dalla playlist.

## <a name="syntax"></a>Sintassi


```JScript
Playlist.removeItem(
  item
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*elemento* \[ di in\]
</dt> <dd>

Oggetto **multimediale** da rimuovere.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Se l'elemento rimosso è la traccia attualmente in gioco (*Player*.**currentMedia**), la riproduzione viene arrestata e l'elemento successivo nella playlist diventa quello corrente. Se non è presente alcun elemento successivo, viene usato l'elemento precedente o se non sono presenti altri elementi, quindi *Player*. **currentMedia** è impostato su **null**.

Per usare questo metodo, è necessario l'accesso completo alla libreria. Per altre informazioni, vedere [accesso alla libreria](library-access.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Player. currentMedia**](player-currentmedia.md)
</dt> <dt>

[**Oggetto playlist**](playlist-object.md)
</dt> <dt>

[**Playlist. insertItem**](playlist-insertitem.md)
</dt> <dt>

[**Playlist. Item**](playlist-item.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





