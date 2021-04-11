---
title: Gestione di elementi multimediali
description: Gestione di elementi multimediali
ms.assetid: fba1df60-d603-4e37-a021-8fa618144149
keywords:
- Windows Media Player, libreria
- Modello a oggetti di Windows Media Player, libreria
- modello a oggetti, libreria
- Windows Media Player Mobile, libreria per il modello a oggetti
- Controllo ActiveX di Windows Media Player, libreria per il modello a oggetti
- Controllo ActiveX Windows Media Player Mobile, libreria per il modello a oggetti
- Controllo ActiveX, libreria per il modello a oggetti
- Windows Media Player Library, gestione di elementi multimediali
- libreria, gestione di elementi multimediali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03b8003de49de9b7e4e51aabeffa222fb649ddef
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104116925"
---
# <a name="managing-media-items"></a>Gestione di elementi multimediali

Un oggetto **multimediale** rappresenta un elemento multimediale. Dispone di proprietà e metodi che è possibile utilizzare per recuperare le informazioni e visualizzarle all'utente o per eseguire azioni diverse in base al valore recuperato.

Gran parte del lavoro con gli oggetti **multimediali** riguarda i metadati relativi al contenuto dell'elemento multimediale, denominato attributi. Nell'argomento [attributi elemento multimediale](media-item-attributes.md) viene descritto come leggere e modificare i valori di attributo. Oltre a questo argomento, vedere le [linee guida sull'utilizzo dei metadati di Windows Media](/previous-versions/ms867702(v=msdn.10)) nel sito Web Microsoft per ulteriori informazioni sugli attributi e sul relativo utilizzo.

L'oggetto **multimediale** dispone di proprietà e metodi che recuperano direttamente alcuni attributi, ad esempio il nome o la durata dell'elemento. Per gli elementi video, è possibile recuperare l'altezza e la larghezza dell'immagine ed è possibile recuperare le informazioni sul marcatore in base al nome o all'indice di un marcatore. È anche possibile determinare se un particolare elemento multimediale è incluso in una determinata playlist.

## <a name="retrieving-a-media-object"></a>Recupero di un oggetto multimediale

È possibile accedere rapidamente all'elemento multimediale corrente usando il *lettore*. proprietà **currentMedia** .

In questo argomento, l'oggetto **Player** è stato definito nel modo seguente:


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



Nell'esempio C# seguente viene recuperato un oggetto **multimediale** che rappresenta l'elemento corrente.


```C++
IWMPMedia media;
media = Player.currentMedia;

```



È possibile creare un nuovo elemento multimediale da un file multimediale digitale usando il *lettore*. metodo **newMedia** . Il metodo passa il percorso URL a un file multimediale digitale e restituisce un riferimento al nuovo oggetto **multimediale** . Il metodo non aggiunge direttamente il nuovo oggetto alla libreria. Tuttavia, è possibile passare l'oggetto alla *playlist*. metodo **appendItem** o *playlist*. metodo **InsertItem** .

Nell'esempio C# seguente viene creato un oggetto **multimediale** basato su uno degli esempi di supporti digitali installati con Windows Media Player SDK.


```C++
IWMPMedia media;
media = Player.newMedia("C:\\WMSDK\\WMPSDK10\\samples\\media\\laure.wma");

```



> [!Note]  
> È necessario includere due barre rovesciate ( \) caratteri (o usare il carattere @ in C#) in una stringa per rappresentare un carattere barra rovesciata effettivo. Questo perché C# usa un singolo carattere barra rovesciata per definire una sequenza di escape.

 

È possibile creare un nuovo elemento multimediale da un file multimediale digitale e aggiungerlo alla libreria in un unico passaggio usando *mediacollection*. **aggiungere** il metodo. Come il *lettore*. metodo **newMedia** , il metodo **Add** accetta un percorso di un file multimediale digitale.

Nell'esempio C# seguente viene creato un oggetto **multimediale** basato su uno dei file di esempio SDK e tale oggetto viene aggiunto alla libreria.


```C++
IWMPMedia media;
media = Player.mediaCollection.add("C:\\WMSDK\\WMPSDK10\\samples\\media\\laure.wma");

```



È possibile recuperare un oggetto **multimediale** che rappresenta un elemento multimediale in una playlist usando la *playlist*. metodo **Item** . Nell'esempio C# seguente viene recuperato il sesto elemento multimediale dalla playlist corrente.


```C++
IWMPMedia media;
media = Player.currentPlaylist.get_Item(5);

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Controls. currentItem**](controls-currentitem.md)
</dt> <dt>

[**Gestione delle playlist**](managing-playlists.md)
</dt> <dt>

[**Oggetto multimediale**](media-object.md)
</dt> <dt>

[**Mediacollection. Add**](mediacollection-add.md)
</dt> <dt>

[**Player. currentMedia**](player-currentmedia.md)
</dt> <dt>

[**Player. newMedia**](player-newmedia.md)
</dt> <dt>

[**Playlist. Item**](playlist-item.md)
</dt> <dt>

[**Utilizzo della libreria**](working-with-the-library.md)
</dt> </dl>

 

 




