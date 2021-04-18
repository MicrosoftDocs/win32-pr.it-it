---
title: Playlist. insertItem, metodo
description: Il metodo insertItem inserisce un elemento multimediale nella playlist nella posizione specificata.
ms.assetid: c186abc4-0a15-49d2-bbc4-5660e8cc0a4b
keywords:
- metodo insertItem Media Player Windows
- metodo insertItem Media Player Windows, classe playlist
- Classe playlist Windows Media Player, metodo insertItem
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
ms.openlocfilehash: a456b7a359d59958ce7693cc48c16eabba435621
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324722"
---
# <a name="playlistinsertitem-method"></a>Playlist. insertItem, metodo

Il metodo **InsertItem** inserisce un elemento multimediale nella playlist nella posizione specificata.

## <a name="syntax"></a>Sintassi


```JScript
Playlist.insertItem(
  index,
  item
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Indice* \[ di in\]
</dt> <dd>

**Numero** (**Long**) che contiene l'indice in corrispondenza del quale aggiungere l'elemento.

</dd> <dt>

*elemento* \[ di in\]
</dt> <dd>

Oggetto **multimediale** da inserire.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Per tutti gli elementi dopo l'elemento inserito i numeri di indice aumenteranno di uno.

Per usare questo metodo, è necessario l'accesso completo alla libreria. Per altre informazioni, vedere [accesso alla libreria](library-access.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto playlist**](playlist-object.md)
</dt> <dt>

[**Playlist. Item**](playlist-item.md)
</dt> <dt>

[**Playlist. removeItem**](playlist-removeitem.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





