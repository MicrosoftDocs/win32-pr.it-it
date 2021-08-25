---
title: Cdrom.playlist
description: La proprietà playlist recupera un oggetto Playlist che rappresenta le tracce sul CD attualmente nell'unità CD o le voci del titolo a livello radice per DVD.
ms.assetid: 71c76b6c-1344-4d45-b86b-7e49be44dba8
keywords:
- Cdrom.playlist Windows Media Player
topic_type:
- apiref
api_name:
- Cdrom.playlist
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b29419b68c50718165e49c0fbe9e75487e9154c19243453981ab352f03e8209a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119864181"
---
# <a name="cdromplaylist"></a>Cdrom.playlist

La **proprietà playlist** recupera un oggetto **Playlist** che rappresenta le tracce sul CD attualmente nell'unità CD o le voci del titolo a livello radice per IL DVD.

``` syntax
player.cdromCollection.item(
        index
        ).playlist
      
```

## <a name="possible-values"></a>Valori possibili

Questa proprietà è un oggetto **Playlist di** sola lettura.

## <a name="remarks"></a>Commenti

In genere, i DVD sono organizzati in titoli. Ogni titolo contiene uno o più capitoli. Ogni DVD viene creato in modo diverso, quindi il modo in cui vengono usati i titoli e i capitoli è all'autore del contenuto.

Per DVD, questo metodo recupera una playlist che contiene come primo elemento un **oggetto Media** che rappresenta il supporto DVD. La riproduzione dell'elemento comporta la riproduzione del DVD dall'inizio se è la prima riproduzione dopo l'inserimento di un nuovo DVD o la ripresa della riproduzione se il DVD è lo stesso dell'ultimo DVD visualizzato. Se si imposta questo elemento come corrente durante la riproduzione, il DVD viene riprodotto dall'inizio.

Gli elementi aggiuntivi **(oggetti** multimediali) nella playlist sono titoli DVD rappresentati da playlist annidate. Quando si specifica *Controls*. **currentItem in** modo che sia uguale a uno di questi elementi di playlist annidati, Windows Media Player automaticamente la playlist nidificata come *Player*. **currentPlaylist dopo** l'inizio della riproduzione del capitolo. È quindi possibile usare le proprietà, i metodi e gli eventi dell'oggetto **currentPlaylist** per usare i capitoli DVD, che sono anche elementi della playlist.

Per recuperare il valore di questa proprietà, è necessario l'accesso in lettura alla libreria. Per altre informazioni, vedere [Accesso alla libreria](library-access.md).

**Windows Media Player 10 Mobile:** Questa proprietà non è supportata.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene *utilizzato Cdrom*. **playlist** per riempire un elemento di testo HTML, denominato myText, con i titoli del CD audio attualmente nella prima unità CD. Usare *CdromCollection*. **count** per determinare il numero di unità CD disponibili. **L'oggetto** Player è stato creato con ID = "Player".


```
// Store the CD playlist object.
var pl = Player.cdromCollection.Item(0).Playlist;

// Iterate through the CD track list.
for(var i = 0; i < pl.count; i++){

   // Print each CD track name.
   myText.value += pl.Item(i).name + "\n"; 
}
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                               |
| Versione<br/>                  | Windows Media Player versione 7.0 o successiva.<br/>                              |
| DLL<br/>                      | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Cdrom**](cdrom-object.md)
</dt> <dt>

[**Impostazioni.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Impostazioni.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





