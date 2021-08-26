---
title: Playlist.attributeName
description: La proprietà attributeName recupera il nome di un attributo in corrispondenza di un indice specificato.
ms.assetid: 3ff68e78-5fa1-4ca6-aa59-4752dbaee52a
keywords:
- Playlist.attributeName Windows Media Player
topic_type:
- apiref
api_name:
- Playlist.attributeName
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 695e0ee00aca0fe7743a028e0e7830e1839c0b2f89b42a94e9ce1dbe29ef35ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120003211"
---
# <a name="playlistattributename"></a>Playlist.attributeName

La **proprietà attributeName** recupera il nome di un attributo in corrispondenza di un indice specificato.

## <a name="syntax"></a>Sintassi

*lettore*. *currentPlaylist*. **attributeName**( *index* )

## <a name="parameters"></a>Parametri

*index*

**Numero** (**long**) contenente l'indice.

## <a name="possible-values"></a>Valori possibili

Questa proprietà è una stringa di sola **lettura.**

## <a name="remarks"></a>Commenti

Il numero di attributi viene recuperato dalla **proprietà attributeCount.** Dato un indice, **attributeName** restituisce un **valore String** che può essere usato insieme a **setItemInfo** o **getItemInfo** per specificare o recuperare un valore per l'attributo.

Per recuperare il valore di questa proprietà, è necessario l'accesso in lettura alla libreria. Per altre informazioni, vedere [Accesso alla libreria](library-access.md).

Per informazioni sugli attributi supportati da Windows Media Player, vedere le informazioni di Windows Media Player [sugli attributi](attribute-reference.md).

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

[**Playlist.attributeCount**](playlist-attributecount.md)
</dt> <dt>

[**Playlist.getItemInfo**](playlist-getiteminfo.md)
</dt> <dt>

[**Playlist.setItemInfo**](playlist-setiteminfo.md)
</dt> <dt>

[**Impostazioni.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Impostazioni.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





