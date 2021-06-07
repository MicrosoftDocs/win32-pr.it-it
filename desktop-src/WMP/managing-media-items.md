---
title: Gestione degli elementi multimediali
description: Gestione degli elementi multimediali
ms.assetid: fba1df60-d603-4e37-a021-8fa618144149
keywords:
- Windows Media Player,library
- Windows Media Player a oggetti, libreria
- modello a oggetti, libreria
- Windows Media Player Mobile, libreria per il modello a oggetti
- Windows Media Player controllo ActiveX, libreria per il modello a oggetti
- Windows Media Player controllo ActiveX mobile, libreria per il modello a oggetti
- Controllo ActiveX, libreria per il modello a oggetti
- Windows Media Player libreria, gestione di elementi multimediali
- libreria, gestione di elementi multimediali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf984c2f884ae828bd6426dd2a3f6da19a78ddea
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386890"
---
# <a name="managing-media-items"></a>Gestione degli elementi multimediali

Un **oggetto Media** rappresenta un elemento multimediale. Include proprietà e metodi che è possibile usare per recuperare informazioni e visualizzarle all'utente o per eseguire azioni diverse in base al valore recuperato.

Gran parte del lavoro con **gli oggetti Multimediali** comporta metadati relativi al contenuto dell'elemento multimediale, denominati attributi. L'argomento [Attributi elemento multimediale](media-item-attributes.md) descrive come leggere e modificare i valori degli attributi. Oltre a questo argomento, vedere le linee guida per l'utilizzo dei metadati di [Windows Media](/previous-versions/ms867702(v=msdn.10)) nel sito Web Microsoft per altre informazioni sugli attributi e sul relativo utilizzo.

**L'oggetto Media** dispone di proprietà e metodi che recuperano direttamente alcuni attributi, ad esempio il nome o la durata dell'elemento. Per gli elementi video, è possibile recuperare l'altezza e la larghezza dell'immagine ed è possibile recuperare le informazioni sul marcatore in base al nome o all'indice di un marcatore. È anche possibile determinare se un particolare elemento multimediale è incluso in una playlist specifica.

## <a name="retrieving-a-media-object"></a>Recupero di un oggetto multimediale

È possibile accedere rapidamente all'elemento multimediale corrente usando *player*. **proprietà currentMedia.**

In questo argomento **l'oggetto Player** è stato definito nel modo seguente:


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



Nell'esempio C# seguente viene recuperato un **oggetto Media** che rappresenta l'elemento corrente.


```C++
IWMPMedia media;
media = Player.currentMedia;

```



È possibile creare un nuovo elemento multimediale da un file multimediale digitale usando il *lettore*. **Metodo newMedia.** Il metodo passa il percorso URL a un file multimediale digitale e restituisce un riferimento al nuovo **oggetto Media.** Il metodo non aggiunge direttamente il nuovo oggetto alla libreria. Tuttavia, è possibile passare l'oggetto alla *playlist*. **Metodo appendItem** o *playlist*. **Metodo insertItem.**

L'esempio C# seguente crea un **oggetto Media** in base a uno degli esempi di supporti digitali installati con Windows Media Player SDK.


```C++
IWMPMedia media;
media = Player.newMedia("C:\\WMSDK\\WMPSDK10\\samples\\media\\laure.wma");

```



> [!Note]  
> È necessario includere due caratteri barra rovesciata ( ) (o usare il carattere @ in C#) in una stringa per rappresentare un carattere barra \\ rovesciata effettiva. Questo perché C# usa un singolo carattere barra rovesciata per definire una sequenza di escape.

 

È possibile creare un nuovo elemento multimediale da un file multimediale digitale e aggiungerlo alla libreria in un unico passaggio usando *MediaCollection*. **Metodo add.** Come il *lettore*. **newMedia,** il **metodo add** accetta un percorso a un file multimediale digitale.

Nell'esempio C# seguente viene creato un **oggetto Media** basato su uno dei file di esempio dell'SDK e tale oggetto viene aggiunto alla libreria.


```C++
IWMPMedia media;
media = Player.mediaCollection.add("C:\\WMSDK\\WMPSDK10\\samples\\media\\laure.wma");

```



È possibile recuperare un **oggetto Media** che rappresenta un elemento multimediale in una playlist usando *playlist*. **metodo item.** Nell'esempio C# seguente viene recuperato il sesto elemento multimediale dalla playlist corrente.


```C++
IWMPMedia media;
media = Player.currentPlaylist.get_Item(5);

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Controls.currentItem**](controls-currentitem.md)
</dt> <dt>

[**Gestione delle playlist**](managing-playlists.md)
</dt> <dt>

[**Oggetto multimediale**](media-object.md)
</dt> <dt>

[**MediaCollection.add**](mediacollection-add.md)
</dt> <dt>

[**Player.currentMedia**](player-currentmedia.md)
</dt> <dt>

[**Player.newMedia**](player-newmedia.md)
</dt> <dt>

[**Playlist.item**](playlist-item.md)
</dt> <dt>

[**Uso della libreria**](working-with-the-library.md)
</dt> </dl>

 

 




