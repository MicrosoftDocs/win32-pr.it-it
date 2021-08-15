---
title: Metodo Playlist.setItemInfo
description: Il metodo setItemInfo specifica il valore di un attributo playlist.
ms.assetid: ffecb43f-343d-4a4f-9356-0e3cfa85ce77
keywords:
- Metodo setItemInfo Windows Media Player
- Metodo setItemInfo Windows Media Player , classe Playlist
- Classe Playlist Windows Media Player, metodo setItemInfo
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
ms.openlocfilehash: 47208d1fad03a57e26d1f5591adf658c7553a9087254b49c7aecfd904bd4d95f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118335748"
---
# <a name="playlistsetiteminfo-method"></a>Metodo Playlist.setItemInfo

Il **metodo setItemInfo** specifica il valore di un attributo playlist.

## <a name="syntax"></a>Sintassi


```JScript
Playlist.setItemInfo(
  name,
  value
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*name* \[ Pollici\]
</dt> <dd>

**Stringa** contenente il nome dell'attributo da impostare. Per informazioni sugli attributi supportati da Windows Media Player, vedere le informazioni di riferimento Windows Media Player [attributi.](attribute-reference.md)

</dd> <dt>

*value* \[ Pollici\]
</dt> <dd>

**Stringa** contenente il nuovo valore per l'attributo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Un uso speciale del **metodo setItemInfo è** quello di ordinare gli elementi nella playlist usando l'attributo SortAttribute. Nell'esempio JScript seguente una playlist viene ordinata in base ai valori dell'attributo UserLastPlayedTime. La playlist della variabile è un riferimento a un **oggetto Playlist.**


```JScript
playlist.setItemInfo("SortAttribute", "UserLastPlayedTime")
```



Per usare questo metodo, è necessario l'accesso completo alla libreria. Per altre informazioni, vedere [Accesso alla libreria.](library-access.md)

**Windows Media Player 10 Mobile:** Questo metodo non è supportato.

## <a name="examples"></a>Esempio

Vedere la [proprietà attributeCount](playlist-attributecount.md) per il codice di esempio che usa questa proprietà.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Playlist**](playlist-object.md)
</dt> <dt>

[**Playlist.getItemInfo**](playlist-getiteminfo.md)
</dt> <dt>

[**Impostazioni.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Impostazioni.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





