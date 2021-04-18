---
title: Playlist. setItemInfo, metodo
description: Il metodo setItemInfo specifica il valore di un attributo della playlist.
ms.assetid: ffecb43f-343d-4a4f-9356-0e3cfa85ce77
keywords:
- Metodo setItemInfo Windows Media Player
- Metodo setItemInfo Media Player Windows, classe playlist
- Classe playlist Windows Media Player, metodo setItemInfo
topic_type:
- apiref
api_name:
- Playlist.setItemInfo
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ff42e56e549100044db0881bb38ade5f2f1711a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333839"
---
# <a name="playlistsetiteminfo-method"></a>Playlist. setItemInfo, metodo

Il metodo **setItemInfo** specifica il valore di un attributo della playlist.

## <a name="syntax"></a>Sintassi


```JScript
Playlist.setItemInfo(
  name,
  value
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*nome* \[ in\]
</dt> <dd>

**Stringa** contenente il nome dell'attributo da impostare. Per informazioni sugli attributi supportati da Windows Media Player, vedere la Guida di [riferimento](attribute-reference.md)agli attributi di Windows Media Player.

</dd> <dt>

*valore* \[ di in\]
</dt> <dd>

**Stringa** contenente il nuovo valore per l'attributo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Un uso speciale del metodo **setItemInfo** consiste nell'ordinare gli elementi nella playlist usando l'attributo SortAttribute. Nell'esempio JScript seguente viene ordinata una playlist in base ai valori dell'attributo UserLastPlayedTime. La variabile playlist è un riferimento a un oggetto **playlist** .


```JScript
playlist.setItemInfo("SortAttribute", "UserLastPlayedTime")
```



Per usare questo metodo, è necessario l'accesso completo alla libreria. Per altre informazioni, vedere [accesso alla libreria](library-access.md).

**Windows Media Player 10 Mobile:** Questo metodo non è supportato.

## <a name="examples"></a>Esempio

Per il codice di esempio che usa questa proprietà, vedere la proprietà [attributeCount](playlist-attributecount.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto playlist**](playlist-object.md)
</dt> <dt>

[**Playlist. getItemInfo**](playlist-getiteminfo.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





