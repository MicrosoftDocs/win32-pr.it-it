---
title: Cdrom. playlist
description: La proprietà playlist recupera un oggetto playlist che rappresenta le tracce del CD attualmente presenti nell'unità CD o le voci del titolo a livello di radice per DVD.
ms.assetid: 71c76b6c-1344-4d45-b86b-7e49be44dba8
keywords:
- Windows Media Player cdrom. playlist
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
ms.openlocfilehash: bcdb50daa169c6f6eb0690de376abd4433ffe130
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301604"
---
# <a name="cdromplaylist"></a>Cdrom. playlist

La proprietà **playlist** recupera un oggetto **playlist** che rappresenta le tracce del CD attualmente presenti nell'unità CD o le voci del titolo a livello di radice per DVD.

``` syntax
player.cdromCollection.item(
        index
        ).playlist
      
```

## <a name="possible-values"></a>Valori possibili

Questa proprietà è un oggetto **playlist** di sola lettura.

## <a name="remarks"></a>Commenti

In genere, i DVD sono organizzati in titoli. Ogni titolo contiene uno o più capitoli. Ogni DVD viene creato in modo diverso, quindi la modalità di utilizzo dei titoli e dei capitoli spetta all'autore del contenuto.

Per il DVD, questo metodo recupera una playlist che contiene come primo elemento un oggetto **multimediale** che rappresenta il supporto DVD. La riproduzione dell'elemento comporta la riproduzione del DVD dall'inizio se è la prima riproduzione dopo l'inserimento di un nuovo DVD o la ripresa della riproduzione se il DVD è uguale all'ultimo DVD visualizzato. Impostando questo elemento come quello corrente durante la riproduzione, il DVD viene riprodotto dall'inizio.

Gli elementi aggiuntivi (oggetti **multimediali** ) nella playlist sono titoli di DVD rappresentati da Playlist nidificate. Quando si specificano i *controlli*. **CurrentItem** è uguale a uno di questi elementi nidificati della playlist, Windows Media Player imposta automaticamente la playlist nidificata come *Player*. **currentPlaylist** dopo l'inizio della riproduzione del capitolo. È quindi possibile usare le proprietà, i metodi e gli eventi dell'oggetto **currentPlaylist** per lavorare con i capitoli DVD, che sono anche elementi della playlist.

Per recuperare il valore di questa proprietà, è necessario l'accesso in lettura alla libreria. Per altre informazioni, vedere [accesso alla libreria](library-access.md).

**Windows Media Player 10 Mobile:** Questa proprietà non è supportata.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene usato *CDROM*. **playlist** per inserire un elemento di testo HTML, denominato testo, con i titoli del CD audio attualmente presenti nella prima unità CD. Usare *cdromcollection*. **conteggio** per determinare il numero di unità CD disponibili. L'oggetto **Player** è stato creato con ID = "Player".


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
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                               |
| Versione<br/>                  | Windows Media Player versione 7,0 o successiva.<br/>                              |
| DLL<br/>                      | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto cdrom**](cdrom-object.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





