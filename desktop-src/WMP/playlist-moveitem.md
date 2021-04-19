---
title: Playlist. moveItem, metodo
description: Il metodo moveItem modifica la posizione di un elemento nella playlist.
ms.assetid: 82a8de86-4419-48a7-89f8-f7b9084b51d4
keywords:
- Metodo moveItem Windows Media Player
- Metodo moveItem Media Player Windows, classe playlist
- Classe playlist Windows Media Player, metodo moveItem
topic_type:
- apiref
api_name:
- Playlist.moveItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06e2e48b2987af4becd8c07357ff2eecf137f31d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332521"
---
# <a name="playlistmoveitem-method"></a>Playlist. moveItem, metodo

Il metodo **moveItem** modifica la posizione di un elemento nella playlist.

## <a name="syntax"></a>Sintassi


```JScript
Playlist.moveItem(
  oldIndex,
  newIndex
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*OldIndex* \[ in\]
</dt> <dd>

**Numero** (**Long**) che contiene l'indice precedente.

</dd> <dt>

*newIndex* \[ in\]
</dt> <dd>

**Numero** (**Long**) che contiene il nuovo indice.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Le playlist archiviate nella libreria possono essere modificate all'esterno del controllo. Assicurarsi di monitorare e gestire tutti gli eventi appropriati correlati alla playlist, in modo che l'ordine degli elementi nella playlist non venga modificato in modo imprevisto.

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

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





