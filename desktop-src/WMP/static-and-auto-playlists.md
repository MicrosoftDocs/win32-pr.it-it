---
title: Playlist statiche e auto
description: Playlist statiche e auto
ms.assetid: 708c236e-8f3c-4188-aefb-eda7da598944
keywords:
- Windows Media Player,playlist
- Windows Media Player a oggetti, playlist
- modello a oggetti, playlist
- Windows Media Player Dispositivi mobili, playlist
- Windows Media Player ActiveX, playlist
- Windows Media Player Controllo ActiveX per dispositivi mobili, playlist
- ActiveX, playlist
- playlist, static
- playlist di metafile, static
- Windows Playlist metafile multimediali,static
- playlist statiche
- playlist auto
- playlist, auto
- playlist di metafile, auto
- Windows playlist metafile multimediali,auto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 645b3bd9ca9ddeebcce9fd6cbb905caa54717e87876be6e449ebd4d3ab64a11a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118568783"
---
# <a name="static-and-auto-playlists"></a>Playlist statiche e auto

Esistono due tipi di playlist:

-   Playlist statiche, che includono elementi multimediali specifici
-   Playlist automatica, che ricercano la libreria ogni volta che vengono aperte e possono contenere elementi multimediali diversi in momenti diversi. Una playlist automatica è il risultato di una query di database.

Per importare una playlist statica da un metafile, chiamare prima *Player*. **newPlaylist** per creare un oggetto **Playlist** in base ai dati nel metafile e quindi passare tale oggetto *a PlaylistCollection*. **importPlaylist** per aggiungere la playlist alla libreria.

Per importare una playlist automatica da un metafile, usare *MediaCollection*. **aggiungere**. Per altre informazioni, vedere [Playlist e l'oggetto MediaCollection](playlists-and-the-mediacollection-object.md).

Per importare una playlist statica da un metafile di playlist automatica, usare *Player*. **newPlaylist** e *PlaylistCollection*. **importPlaylist come** descritto in precedenza. La playlist automatica verrà eseguita una sola volta e verrà creata una playlist statica in base al risultato dell'esecuzione.

L'uso di una playlist automatica per eseguire query sulla libreria dell'utente non è supportato per le pagine Web a cui gli utenti accedono tramite Internet.

Il codice di esempio C# seguente illustra l'importazione di un metafile di playlist automatica come playlist statica. Per eseguire questo esempio, creare una playlist automatica usando l'interfaccia utente della libreria e quindi includere il percorso corretto del metafile della playlist automatica in questo codice.


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

 

 




