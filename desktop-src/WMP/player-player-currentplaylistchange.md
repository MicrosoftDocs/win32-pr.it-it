---
title: Evento Player. CurrentPlaylistChange
description: L'evento CurrentPlaylistChange si verifica quando viene apportata una modifica all'interno della playlist corrente. | Evento Player. CurrentPlaylistChange
ms.assetid: 5270373e-e401-40c6-bf8c-ef0557610372
keywords:
- Media Player di Windows Event CurrentPlaylistChange
- Windows Event CurrentPlaylistChange Media Player, classe Player
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
ms.openlocfilehash: 4722db224285587198e3ddb021022ec5d8f2cea6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326225"
---
# <a name="playercurrentplaylistchange-event"></a>Evento Player. CurrentPlaylistChange

L'evento **CurrentPlaylistChange** si verifica quando viene apportata una modifica all'interno della playlist corrente.

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

**Numero** (**Long**) che indica il tipo di modifica apportata alla playlist. Vedere il *lettore*. Evento **PlaylistChange** per una tabella di valori possibili.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Questo evento non si verifica quando una playlist diversa diventa la playlist corrente. Si verifica solo quando si verifica una modifica all'interno della playlist corrente, ad esempio un elemento multimediale aggiunto alla playlist.

Il valore dei parametri evento viene specificato da Windows Media Player ed è possibile accedervi o passarli a un metodo in un file JScript importato usando il nome del parametro specificato. Questo nome di parametro deve essere digitato esattamente come illustrato, incluse le maiuscole.

## <a name="examples"></a>Esempio

Nell'esempio JScript seguente viene aggiornato il testo in un elemento DIV HTML, denominato PlItems, per visualizzare i nomi degli elementi multimediali nella playlist corrente. L'oggetto **Player** è stato creato con ID = "Player".


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
| Versione<br/> | Windows Media Player versione 7,0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Player**](player-object.md)
</dt> <dt>

[**Player. currentPlaylist**](player-currentplaylist.md)
</dt> <dt>

[**Player. PlaylistChange**](player-player-playlistchange.md)
</dt> </dl>

 

 





