---
title: Accesso alla libreria a livello di codice
description: Accesso alla libreria a livello di codice
ms.assetid: f48fbb49-5b79-4a78-af72-8509c460a149
keywords:
- Windows Media Player,library
- Windows Media Player a oggetti, libreria
- modello a oggetti, libreria
- Windows Media Player ActiveX, libreria per il modello a oggetti
- ActiveX, libreria per il modello a oggetti
- Windows Media Player Controllo ActiveX per dispositivi mobili, libreria per il modello a oggetti
- Windows Media Player Mobile, libreria per il modello a oggetti
- Windows Media Player libreria, accesso a livello di codice
- libreria, accesso
- accesso alla Windows Media Player a livello di codice
- Windows Media Player libreria, aggiunta di elementi multimediali
- libreria,aggiunta di elementi multimediali
- Windows Media Player libreria, recupero di elementi multimediali
- libreria, recupero di elementi multimediali
- Windows Media Player libreria, rimozione di elementi multimediali
- libreria, rimozione di elementi multimediali
- aggiunta di elementi multimediali Windows Media Player libreria
- recupero di elementi multimediali dalla libreria Windows Media Player dati
- rimozione di elementi multimediali da Windows Media Player libreria
- recupero di metadati
- Windows Media Player libreria, recupero di metadati da elementi multimediali
- libreria, recupero di metadati da elementi multimediali
- metadati, recupero
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b575d1ed265d5c8e65beab9cc8e937b3639d8547867dacf473b2db21fe99198
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119619431"
---
# <a name="accessing-the-library-programmatically"></a>Accesso alla libreria a livello di codice

Nel codice la libreria è rappresentata **dall'oggetto MediaCollection** (o dall'interfaccia **IWMPMediaCollection).** Gli elementi multimediali sono rappresentati **come oggetti** multimediali (o dall'interfaccia **IWMPMedia).** Gli elementi della playlist sono rappresentati come **oggetti Playlist** (o dall'interfaccia **IWMPPlaylist).** Per semplicità, questa sezione farà semplicemente riferimento ai nomi degli oggetti, quando possibile.

Usando **l'oggetto MediaCollection** è possibile usare elementi multimediali e playlist. La libreria espone anche l'oggetto **PlaylistCollection** (o **l'interfaccia IWMPPlaylistCollection),** che fornisce alcune funzionalità specifiche per l'uso delle playlist. Nella maggior parte dei casi, **l'oggetto MediaCollection** fornirà le funzionalità necessarie, anche quando si lavora con le playlist. Per altre informazioni sull'uso degli elementi multimediali, vedere [Gestione di elementi multimediali](managing-media-items.md). Per altre informazioni sull'uso delle playlist, vedere [Gestione delle playlist.](managing-playlists.md)

## <a name="adding-media-items-to-the-library"></a>Aggiunta di elementi multimediali alla libreria

L'aggiunta di contenuto multimediale digitale alla libreria è semplice. È sufficiente chiamare [il metodo MediaCollection.add,](mediacollection-add.md) specificando il percorso del file multimediale come argomento.

## <a name="retrieving-media-items-from-the-library"></a>Recupero di elementi multimediali dalla libreria

Quando si recuperano elementi multimediali dalla libreria, si recupera realmente una playlist. Anche se si prevede di recuperare un solo elemento multimediale, si otterrà un oggetto **Playlist** contenente un singolo elemento, che verrà associato all'indice zero. Ad esempio, se si vuole recuperare un oggetto **Media** che rappresenta il brano denominato "Giovanna", è possibile usare il codice JScript seguente:


```C++
// Retrieve media named Jeanne from the library.
var playlist = player.mediaCollection.getByName("Jeanne");

```



Il codice precedente recupera una playlist contenente tutti gli elementi multimediali con il nome "Giovanna" come titolo. Per questo esempio, si supponga di sapere che nella libreria è presente un solo brano in base al nome (si noti che la libreria supporta più brani con lo stesso nome). Ciò significa che è possibile prevedere che il numero di elementi nella playlist recuperata sia uguale a uno e che l'elemento multimediale sia rappresentato dall'indice zero. Il codice di esempio seguente continua l'esempio precedente per illustrare come recuperare l'elemento multimediale dalla playlist usando il [metodo Playlist.item.](playlist-item.md)


```C++
// Retrieve the individual media item from the playlist.
var media = playlist.item(0);

```



Per altre informazioni sul recupero di elementi multimediali dalle playlist, vedere [Playlist ed elementi multimediali](playlists-and-media-items.md) nella Guida al controllo [player.](player-control-guide.md)

## <a name="retrieving-metadata-from-a-media-item"></a>Recupero di metadati da un elemento multimediale

Dopo aver recuperato un **oggetto Media,** è possibile leggere i valori degli attributi associati al contenuto. Nel caso più semplice, si potrebbe semplicemente voler conoscere un singolo valore, ad esempio il nome dell'artista che ha eseguito una traccia musicale. L'JScript seguente illustra come usare il metodo [Media.getItemInfo](media-getiteminfo.md) per recuperare il nome dell'artista dai supporti recuperati nell'esempio precedente:


```C++
// Retrieve the artist name string.
var author = media.getItemInfo("Artist");

```



Un elemento multimediale può avere molti attributi diversi e l'uso dei metadati non è sempre semplice come il semplice caso illustrato nell'esempio precedente. Ad esempio, alcuni attributi possono contenere più valori o avere valori in più lingue. Per altre informazioni sull'uso dei metadati, vedere [Attributi degli elementi multimediali](media-item-attributes.md). Per altre informazioni sui vari attributi, sui relativi significati e sul supporto dei tipi di file, vedere Informazioni [di riferimento sugli attributi](attribute-reference.md).

## <a name="removing-media-items-from-the-library"></a>Rimozione di elementi multimediali dalla libreria

Anche la rimozione del contenuto multimediale digitale dalla libreria è semplice. È sufficiente **chiamare MediaCollection.remove**, fornendo l'oggetto **Media** che rappresenta l'elemento come primo argomento e il valore **true** come secondo. L'JScript seguente rimuove il file denominato Giovanna (recuperato nell'esempio precedente) dalla libreria:


```C++
// Remove Jeanne from the library.
playst.mediaCollection.remove(media, true);

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni sulla libreria**](about-the-library.md)
</dt> <dt>

[**Informazioni sugli oggetti MediaCollection e Media Objects**](about-the-mediacollection-and-media-objects.md)
</dt> <dt>

[**Informazioni sugli oggetti Playlist, PlaylistCollection e PlaylistArray**](about-the-playlist--playlistcollection--and-playlistarray-objects.md)
</dt> <dt>

[**Uso della libreria**](working-with-the-library.md)
</dt> </dl>

 

 




