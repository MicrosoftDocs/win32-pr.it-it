---
title: Evento Player.CurrentPlaylistChange
description: L'evento CurrentPlaylistChange si verifica quando viene modificato un elemento all'interno della playlist corrente. | Evento Player.CurrentPlaylistChange
ms.assetid: 5270373e-e401-40c6-bf8c-ef0557610372
keywords:
- Evento CurrentPlaylistChange Windows Media Player
- Classe di evento CurrentPlaylistChange Windows Media Player , Player
- Classe Player Windows Media Player, evento CurrentPlaylistChange
topic_type:
- apiref
api_name:
- Player.CurrentPlaylistChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 672ff739e60efe73e1d30670dec5bc956f9fdd56506464b036add6f52cc6fc34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118338147"
---
# <a name="playercurrentplaylistchange-event"></a>Evento Player.CurrentPlaylistChange

**L'evento CurrentPlaylistChange** si verifica quando viene modificato un elemento all'interno della playlist corrente.

## <a name="syntax"></a>Sintassi


```JScript
Player.CurrentPlaylistChange(
  change
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*change* 
</dt> <dd>

**Numero** (**long**) che indica il tipo di modifica apportata alla playlist. Vedere *player*. **Evento PlaylistChange** per una tabella di valori possibili.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Questo evento non si verifica quando una playlist diversa diventa la playlist corrente. Si verifica solo quando si verifica una modifica all'interno della playlist corrente, ad esempio un elemento multimediale aggiunto alla playlist.

Il valore dei parametri dell'evento viene specificato da Windows Media Player e può essere accessibile o passato a un metodo in un file JScript importato usando il nome del parametro specificato. Questo nome di parametro deve essere digitato esattamente come illustrato, inclusa l'maiuscola.

## <a name="examples"></a>Esempio

Nell'JScript seguente viene aggiornato il testo in un elemento DIV HTML, denominato PlItems, per visualizzare i nomi degli elementi multimediali nella playlist corrente. **L'oggetto Player** è stato creato con ID = "Player".


```JScript
<!-- Create an event handler for current playlist change. -->
<SCRIPT FOR = "Player" EVENT = "currentPlaylistChange(change)">
   switch (change){
      // Only update for move, delete, insert, and append events.
      case 3, 4, 5, 6:

         // Clear the contents of the DIV.
         PlItems.innerHTML = "";

         // Loop through the playlist and display each item name.
         for (var i = 0; i < Player.currentPlaylist.count; i++){
            PlItems.innerHTML += Player.currentPlaylist.item(i).name;
            PlItems.innerHTML += "<br>";
         }
         break;
      
      default:
   } 
</SCRIPT>

```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Player**](player-object.md)
</dt> <dt>

[**Player.currentPlaylist**](player-currentplaylist.md)
</dt> <dt>

[**Player.PlaylistChange**](player-player-playlistchange.md)
</dt> </dl>

 

 





