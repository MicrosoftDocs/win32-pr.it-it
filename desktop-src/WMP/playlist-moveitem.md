---
title: Metodo Playlist.moveItem
description: Il metodo moveItem modifica la posizione di un elemento nella playlist.
ms.assetid: 82a8de86-4419-48a7-89f8-f7b9084b51d4
keywords:
- Metodo moveItem Windows Media Player
- Metodo moveItem Windows Media Player , classe Playlist
- Classe playlist Windows Media Player metodo , moveItem
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
ms.openlocfilehash: a725ae53e38d1903d31dc47a3362f90c29fb064e3a785b816de0d0b695998aee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117746853"
---
# <a name="playlistmoveitem-method"></a>Metodo Playlist.moveItem

Il **metodo moveItem** modifica la posizione di un elemento nella playlist.

## <a name="syntax"></a>Sintassi


```JScript
Playlist.moveItem(
  oldIndex,
  newIndex
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*oldIndex* \[ Pollici\]
</dt> <dd>

**Numero** (**long**) contenente l'indice precedente.

</dd> <dt>

*newIndex* \[ Pollici\]
</dt> <dd>

**Numero** (**long**) contenente il nuovo indice.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Le playlist archiviate nella libreria possono cambiare all'esterno del controllo. Assicurarsi di monitorare e gestire tutti gli eventi appropriati correlati alle playlist in modo che l'ordine degli elementi nella playlist non cambi in modo imprevisto.

Per usare questo metodo, è necessario l'accesso completo alla libreria. Per altre informazioni, vedere [Accesso alla libreria](library-access.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Playlist**](playlist-object.md)
</dt> <dt>

[**Impostazioni.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Impostazioni.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





