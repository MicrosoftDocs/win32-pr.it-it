---
title: Metodo PlaylistArray.item
description: Il metodo item recupera la playlist in corrispondenza dell'indice specificato.
ms.assetid: cc851695-f9a2-4594-8bd3-3555c18bfa10
keywords:
- Metodo item Windows Media Player
- Metodo item Windows Media Player , classe PlaylistArray
- Metodo della classe PlaylistArray Windows Media Player , item
topic_type:
- apiref
api_name:
- PlaylistArray.item
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a45bb38250285563d9e4b7abcc1a4bfd1f7a0bea35b41b7e4cd801f8eff1d00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118335428"
---
# <a name="playlistarrayitem-method"></a>Metodo PlaylistArray.item

Il **metodo item** recupera la playlist in corrispondenza dell'indice specificato.

## <a name="syntax"></a>Sintassi


```JScript
retVal = PlaylistArray.item(
  index
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*index* \[ Pollici\]
</dt> <dd>

**Numero** (**long**) contenente l'indice della playlist da recuperare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un **oggetto Playlist.**

## <a name="remarks"></a>Commenti

Per usare questo metodo, è necessario l'accesso in lettura alla libreria. Per altre informazioni, vedere [Accesso alla libreria](library-access.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto PlaylistArray**](playlistarray-object.md)
</dt> <dt>

[**Impostazioni.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Impostazioni.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





