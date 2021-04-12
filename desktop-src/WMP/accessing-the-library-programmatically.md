---
title: Accesso alla libreria a livello di codice
description: Accesso alla libreria a livello di codice
ms.assetid: f48fbb49-5b79-4a78-af72-8509c460a149
keywords:
- Windows Media Player, libreria
- Modello a oggetti di Windows Media Player, libreria
- modello a oggetti, libreria
- Controllo ActiveX di Windows Media Player, libreria per il modello a oggetti
- Controllo ActiveX, libreria per il modello a oggetti
- Controllo ActiveX Windows Media Player Mobile, libreria per il modello a oggetti
- Windows Media Player Mobile, libreria per il modello a oggetti
- Windows Media Player Library, accesso a livello di codice
- libreria, accesso
- accesso a Windows Media Player Library a livello di codice
- Libreria di Media Player Windows, aggiunta di elementi multimediali
- libreria, aggiunta di elementi multimediali
- Libreria Media Player di Windows, recupero di elementi multimediali
- raccolta, recupero di elementi multimediali
- Libreria Media Player di Windows, rimozione di elementi multimediali
- libreria, rimozione di elementi multimediali
- Aggiunta di elementi multimediali a Windows Media Player Library
- recupero di elementi multimediali dalla libreria Media Player di Windows
- rimozione di elementi multimediali dalla libreria Media Player di Windows
- recupero di metadati
- Libreria Media Player di Windows, recupero di metadati da elementi multimediali
- raccolta, recupero di metadati da elementi multimediali
- metadati, recupero
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d40e03e91b2a67a24cb49b0ac1810ceb7b9544c9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396391"
---
# <a name="accessing-the-library-programmatically"></a>Accesso alla libreria a livello di codice

Nel codice la libreria è rappresentata dall'oggetto **mediacollection** (o dall'interfaccia **IWMPMediaCollection** ). Gli elementi multimediali sono rappresentati come oggetti **multimediali** o dall'interfaccia **IWMPMedia** . Gli elementi della playlist sono rappresentati come oggetti **playlist** (o dall'interfaccia **IWMPPlaylist** ). Per semplicità, in questa sezione si faranno semplicemente riferimento ai nomi degli oggetti, quando possibile.

Utilizzando l'oggetto **mediacollection** , è possibile utilizzare gli elementi multimediali e le playlist. La libreria espone anche l'oggetto **PlaylistCollection** (o l'interfaccia **IWMPPlaylistCollection** ), che fornisce alcune funzionalità specifiche per l'uso delle playlist. Nella maggior parte dei casi, l'oggetto **mediacollection** fornirà le funzionalità necessarie, anche quando si lavora con le playlist. Per ulteriori informazioni sull'utilizzo di elementi multimediali, vedere [gestione di elementi multimediali](managing-media-items.md). Per altre informazioni sull'uso delle playlist, vedere [gestione delle playlist](managing-playlists.md).

## <a name="adding-media-items-to-the-library"></a>Aggiunta di elementi multimediali alla libreria

L'aggiunta di contenuti multimediali digitali alla libreria è semplice. È sufficiente chiamare il metodo [mediacollection. Add](mediacollection-add.md) , specificando il percorso del file multimediale come argomento.

## <a name="retrieving-media-items-from-the-library"></a>Recupero di elementi multimediali dalla libreria

Quando si recuperano elementi multimediali dalla libreria, ciò che viene effettivamente recuperato è una playlist. Anche se si prevede di recuperare un solo elemento multimediale, si otterrà un oggetto **playlist** contenente un singolo elemento, che verrà associato all'indice zero. Se ad esempio si desidera recuperare un oggetto **multimediale** che rappresenta il brano denominato "Jeanne", è possibile utilizzare il codice JScript seguente:


```C++
// Retrieve media named Jeanne from the library.
var playlist = player.mediaCollection.getByName("Jeanne");

```



Il codice precedente recupera una playlist contenente tutti gli elementi multimediali il cui nome è "Jeanne". Per questo esempio, si supponga che sia presente un solo brano con tale nome nella libreria. si noti che la libreria supporta più canzoni con lo stesso nome. Ciò significa che è possibile prevedere che il numero di elementi nella playlist recuperata sia uguale a uno e che l'elemento multimediale venga rappresentato dall'indice zero. Il codice di esempio seguente continua l'esempio precedente per illustrare come recuperare l'elemento multimediale dalla playlist usando il metodo [playlist. Item](playlist-item.md) .


```C++
// Retrieve the individual media item from the playlist.
var media = playlist.item(0);

```



Per ulteriori informazioni sul recupero di elementi multimediali dalle playlist, vedere [playlist e elementi multimediali](playlists-and-media-items.md) nella [Guida al controllo del lettore](player-control-guide.md).

## <a name="retrieving-metadata-from-a-media-item"></a>Recupero di metadati da un elemento multimediale

Dopo aver recuperato un oggetto **multimediale** , è possibile leggere i valori di attributo associati al contenuto. Nel caso più semplice, si potrebbe semplicemente voler conoscere un solo valore, ad esempio il nome dell'artista che ha eseguito una traccia musicale. Nell'esempio JScript seguente viene illustrato come utilizzare il metodo [Media. GetItemInfo](media-getiteminfo.md) per recuperare il nome dell'artista dal supporto recuperato nell'esempio precedente:


```C++
// Retrieve the artist name string.
var author = media.getItemInfo("Artist");

```



Un elemento multimediale può avere molti attributi diversi e l'utilizzo dei metadati non è sempre semplice come il semplice caso illustrato nell'esempio precedente. Alcuni attributi, ad esempio, possono contenere più valori o avere valori in più di una lingua. Per ulteriori informazioni sull'utilizzo dei metadati, vedere [attributi elemento multimediale](media-item-attributes.md). Per ulteriori informazioni sui diversi attributi, sui relativi significati e sul supporto dei tipi di file, vedere il [riferimento all'attributo](attribute-reference.md).

## <a name="removing-media-items-from-the-library"></a>Rimozione di elementi multimediali dalla libreria

Anche la rimozione di contenuti multimediali digitali dalla libreria è semplice. È sufficiente chiamare **mediacollection. Remove**, fornendo l'oggetto **multimediale** che rappresenta l'elemento come primo argomento e il valore **true** come secondo. Nell'esempio di codice JScript seguente viene rimosso dalla libreria il file denominato Jeanne (recuperato nell'esempio precedente):


```C++
// Remove Jeanne from the library.
playst.mediaCollection.remove(media, true);

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni sulla libreria**](about-the-library.md)
</dt> <dt>

[**Informazioni sugli oggetti Mediacollection e media**](about-the-mediacollection-and-media-objects.md)
</dt> <dt>

[**Informazioni sugli oggetti playlist, PlaylistCollection e PlaylistArray**](about-the-playlist--playlistcollection--and-playlistarray-objects.md)
</dt> <dt>

[**Utilizzo della libreria**](working-with-the-library.md)
</dt> </dl>

 

 




