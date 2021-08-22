---
title: Uso delle playlist auto per organizzare il contenuto nella raccolta
description: Uso delle playlist auto per organizzare il contenuto nella raccolta
ms.assetid: 118d4357-044f-4986-af51-0c344470e891
keywords:
- Windows Media Player store online, playlist auto
- online store, playlist auto
- type 1 online stores,auto playlists
- type 2 online stores,auto playlists
- Windows Media Player online, organizzazione del contenuto della raccolta
- negozi online, organizzazione del contenuto della raccolta
- tipo 1 negozi online, organizzazione del contenuto della raccolta
- store online di tipo 2, organizzazione del contenuto della raccolta
- Windows Media Player online, organizzazione del contenuto della raccolta
- negozi online, organizzazione del contenuto della raccolta
- tipo 1 negozi online, organizzazione del contenuto della raccolta
- store online di tipo 2, organizzazione del contenuto della raccolta
- libreria, organizzazione del contenuto
- organizzazione del contenuto della raccolta
- playlist auto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0e32d0f95093d9550c71643330267d59a57f56db7e0d666274a492ac29b2c58
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119507171"
---
# <a name="using-auto-playlists-to-organize-content-in-the-library"></a>Uso delle playlist auto per organizzare il contenuto nella raccolta

È possibile usare le playlist auto per organizzare il contenuto Premium fornito. Ad esempio, è possibile usare Windows Media Player per creare una playlist automatica che contenga solo il contenuto fornito con una classificazione utente di almeno quattro stelle. È quindi possibile aggiungere la playlist automatica alla libreria in Windows Media Player in modo che sia visualizzata nel nodo Purchased Musica nel nodo del server di distribuzione del contenuto.

A questo scopo, seguire questa procedura:

1.  Creare la playlist automatica.
2.  Usando Windows Explorer, passare alla playlist automatica e recuperare il file con estensione wpl.
3.  Usando il Windows Media Player a oggetti, aggiungere la playlist automatica alla libreria.
4.  Impostare **l'attributo WM/ContentDistributor** per la playlist sul nome della chiave del distributore di contenuti.
5.  Impostare **l'attributo SyncOnly** per la playlist su true.

L'JScript di esempio seguente mostra una funzione che aggiunge una playlist automatica denominata "Favorite Hits" al nodo Proseware nella libreria:


```C++
function AddWPL()
{
    var pl = Player.mediaCollection.add("c:\\media\\Favorite Hits.wpl");
    pl.setItemInfo("WM/ContentDistributor", "Proseware");
    pl.setItemInfo("SyncOnly", true);
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sull'integrazione delle librerie](download-manager-overview.md)
</dt> <dt>

[**Informazioni comuni ai negozi online di tipo 1 e di tipo 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**MediaCollection.add**](mediacollection-add.md)
</dt> <dt>

[**Playlist.setItemInfo**](playlist-setiteminfo.md)
</dt> <dt>

[**Playlist statiche e auto**](static-and-auto-playlists.md)
</dt> <dt>

[**Attributo SyncOnly**](synconly-attribute.md)
</dt> <dt>

[**Attributo WM/ContentDistributor**](wm-contentdistributor-attribute.md)
</dt> <dt>

[**Uso della libreria**](working-with-the-library.md)
</dt> </dl>

 

 




