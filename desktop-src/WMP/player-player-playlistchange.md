---
title: Evento Player. PlaylistChange
description: L'evento PlaylistChange si verifica quando viene modificata una playlist. | Evento Player. PlaylistChange
ms.assetid: 09ab0560-e18d-4ee8-a649-2b2468b40c31
keywords:
- Media Player di Windows Event PlaylistChange
- Windows Event PlaylistChange Media Player, classe Player
- Classe Player Windows Media Player, evento PlaylistChange
topic_type:
- apiref
api_name:
- Player.PlaylistChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83d371818e8166b536543246eeecf0090509e62b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326460"
---
# <a name="playerplaylistchange-event"></a>Evento Player. PlaylistChange

L'evento **PlaylistChange** si verifica quando viene modificata una playlist.

## <a name="syntax"></a>Sintassi


```JScript
Player.PlaylistChange(
  Playlist,
  change
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Playlist* 
</dt> <dd>

Oggetto **playlist** che è stato modificato.

</dd> <dt>

*change* 
</dt> <dd>

**Numero** (**Long**) che indica il tipo di modifica apportata alla playlist. Contiene uno dei valori seguenti.



| Number | Nome          |
|--------|---------------|
| 0      | Sconosciuto       |
| 1      | Cancella         |
| 2      | InfoChange    |
| 3      | Sposta          |
| 4      | Delete        |
| 5      | Insert        |
| 6      | Accoda        |
| 7      | Non supportato |
| 8      | NameChange    |
| 9      | Non supportate |
| 10     | Ordina          |



 

È possibile derivare la costante di enumerazione di tipo C anteponendo il valore Name con "wmplc". La costante per lo stato di spostamento, ad esempio, è **wmplcMove**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Il valore dei parametri evento viene specificato da Windows Media Player ed è possibile accedervi o passarli a un metodo in un file JScript importato usando il nome del parametro specificato. Questo nome di parametro deve essere digitato esattamente come illustrato, incluse le maiuscole.

**Windows Media Player 10 Mobile:** Questo evento non è supportato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Player**](player-object.md)
</dt> </dl>

 

 





