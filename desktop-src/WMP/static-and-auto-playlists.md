---
title: Playlist statiche e automatiche
description: Playlist statiche e automatiche
ms.assetid: 708c236e-8f3c-4188-aefb-eda7da598944
keywords:
- Media Player di Windows, playlist
- Modello a oggetti di Windows Media Player, playlist
- modello a oggetti, playlist
- Windows Media Player Mobile, playlist
- Controllo ActiveX di Windows Media Player, playlist
- Controllo ActiveX Windows Media Player Mobile, playlist
- Controllo ActiveX, playlist
- playlist, statiche
- playlist di metafile, statiche
- Playlist Windows Media Metafile, statiche
- playlist statiche
- playlist automatiche
- playlist, auto
- playlist di metafile, auto
- Playlist Windows Media Metafile, auto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 083ee2029eec2cfee7510766790f4ca7eb6468e5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395474"
---
# <a name="static-and-auto-playlists"></a>Playlist statiche e automatiche

Sono disponibili due tipi di playlist:

-   Playlist statiche, che includono elementi multimediali specifici
-   Playlist automatiche, che eseguono ricerche nella libreria ogni volta che vengono aperte e possono contenere elementi multimediali diversi in momenti diversi. Una playlist automatica è il risultato di una query di database.

Per importare una playlist statica da un metafile, chiamare prima il *lettore*. **nuova playlist** per creare un oggetto **playlist** basato sui dati nel metafile, quindi passare l'oggetto a *PlaylistCollection*. **importPlaylist** aggiungere la playlist alla libreria.

Per importare una playlist automatica da un metafile, usare *mediacollection*. **Aggiungi**. Per ulteriori informazioni, vedere [playlist e l'oggetto mediacollection](playlists-and-the-mediacollection-object.md).

Per importare una playlist statica da un metafile di playlist automatico, usare *Player*. **nuova playlist** e *PlaylistCollection*. **importPlaylist** come descritto in precedenza. La playlist automatica verrà eseguita una volta e una playlist statica verrà creata in base al risultato di tale esecuzione.

L'uso di una playlist automatica per eseguire query sulla libreria dell'utente non è supportato per le pagine Web a cui gli utenti accedono tramite Internet.

Il codice di esempio C# seguente illustra l'importazione di un metafile di playlist automatico come playlist statica. Per eseguire questo esempio, creare una playlist automatica usando l'interfaccia utente della libreria e quindi includere il percorso corretto per il metafile della playlist automatica in questo codice.


```C++
private void addStaticPlaylist()
{
    IWMPPlaylist pList;

    pList = Player.newPlaylist("NewImportedList", "\\\\myServer\\myPath\\artistcollection.wpl");
    if (pList.count == 0)
        MessageBox.Show("The specified playlist is empty.");
    else
        Player.playlistCollection.importPlaylist(pList);
}

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Gestione delle playlist**](managing-playlists.md)
</dt> </dl>

 

 




