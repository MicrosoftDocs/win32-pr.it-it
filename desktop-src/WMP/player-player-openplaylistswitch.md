---
title: Evento Player. OpenPlaylistSwitch
description: L'evento OpenPlaylistSwitch si verifica quando viene avviata la riproduzione di un titolo su un DVD. | Evento Player. OpenPlaylistSwitch
ms.assetid: 97d69716-602f-4522-b743-83f2dbc852a2
keywords:
- Media Player di Windows Event OpenPlaylistSwitch
- Windows Event OpenPlaylistSwitch Media Player, classe Player
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
ms.openlocfilehash: 6d35d4568356365cc9276c13ea33f866e937da1a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326465"
---
# <a name="playeropenplaylistswitch-event"></a>Evento Player. OpenPlaylistSwitch

L'evento **OpenPlaylistSwitch** si verifica quando viene avviata la riproduzione di un titolo su un DVD.

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

Oggetto **playlist** che rappresenta il titolo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Il valore dei parametri evento viene specificato da Windows Media Player ed è possibile accedervi o passarli a un metodo in un file JScript importato usando il nome del parametro specificato. Questo nome di parametro deve essere digitato esattamente come illustrato, incluse le maiuscole.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player per Windows XP o versione successiva.<br/>                           |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Player**](player-object.md)
</dt> </dl>

 

 





