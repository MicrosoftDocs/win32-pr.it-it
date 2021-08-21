---
title: Evento Player.OpenPlaylistSwitch
description: L'evento OpenPlaylistSwitch si verifica quando inizia la riproduzione di un titolo in un DVD. | Evento Player.OpenPlaylistSwitch
ms.assetid: 97d69716-602f-4522-b743-83f2dbc852a2
keywords:
- Evento OpenPlaylistSwitch Windows Media Player
- Classe di evento OpenPlaylistSwitch Windows Media Player , Player
- Classe Player Windows Media Player, evento OpenPlaylistSwitch
topic_type:
- apiref
api_name:
- Player.OpenPlaylistSwitch
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5610c4e5a4870b1ad5dc5d12d9d8c315dce630578d5af01f8f428b1af47884e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118835148"
---
# <a name="playeropenplaylistswitch-event"></a>Evento Player.OpenPlaylistSwitch

**L'evento OpenPlaylistSwitch** si verifica quando inizia la riproduzione di un titolo in un DVD.

## <a name="syntax"></a>Sintassi


```JScript
Player.OpenPlaylistSwitch(
  pItem
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pItem* 
</dt> <dd>

**Oggetto Playlist** che rappresenta il titolo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Il valore dei parametri dell'evento viene specificato da Windows Media Player e può essere accessibile o passato a un metodo in un file JScript importato usando il nome del parametro specificato. Questo nome di parametro deve essere digitato esattamente come illustrato, inclusa l'maiuscola.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player per Windows XP o versioni successive.<br/>                           |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Player**](player-object.md)
</dt> </dl>

 

 





