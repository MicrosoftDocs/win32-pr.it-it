---
title: Uso delle playlist automatiche per organizzare il contenuto nella libreria
description: Uso delle playlist automatiche per organizzare il contenuto nella libreria
ms.assetid: 118d4357-044f-4986-af51-0c344470e891
keywords:
- Windows Media Player Online Stores, playlist automatiche
- archivi online, playlist automatiche
- digitare 1 archivi online, playlist automatiche
- digitare 2 archivi online, playlist automatiche
- Windows Media Player Online Store, organizzazione del contenuto della libreria
- negozi online, organizzazione del contenuto della libreria
- digitare 1 negozi online, organizzare il contenuto della libreria
- digitare 2 archivi online, organizzare il contenuto della libreria
- Windows Media Player Online Stores, organizzazione contenuto libreria
- negozi online, organizzazione del contenuto della libreria
- digitare 1 negozi online, organizzazione del contenuto della libreria
- digitare 2 negozi online, organizzazione del contenuto della libreria
- libreria, organizzazione del contenuto
- organizzazione del contenuto della libreria
- playlist automatiche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa53a4b9f56a8aa6425f137ef4a8c43bd8ed1454
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515865"
---
# <a name="using-auto-playlists-to-organize-content-in-the-library"></a>Uso delle playlist automatiche per organizzare il contenuto nella libreria

È possibile usare playlist automatiche per organizzare il contenuto Premium fornito. Ad esempio, è possibile usare Windows Media Player per creare una playlist automatica che contiene solo il contenuto fornito con una classificazione utente di almeno quattro stelle. È quindi possibile aggiungere la playlist automatica alla libreria in Windows Media Player in modo che venga visualizzata nel nodo musica acquistato nel nodo del server di distribuzione del contenuto.

A questo scopo, seguire questa procedura:

1.  Creare la playlist automatica.
2.  Utilizzando Esplora risorse, passare alla playlist automatica e recuperare il file con estensione WPL.
3.  Usando il modello a oggetti di Windows Media Player, aggiungere la playlist automatica alla libreria.
4.  Impostare l'attributo **WM/contentdistributor** per la playlist sul nome della chiave del server di distribuzione del contenuto.
5.  Impostare l'attributo **SyncOnly** per la playlist su true.

Il codice di esempio JScript seguente mostra una funzione che aggiunge una playlist automatica denominata "hit preferiti" al nodo Proseware nella libreria:


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

[Informazioni sull'integrazione della libreria](download-manager-overview.md)
</dt> <dt>

[**Informazioni comuni ai negozi online di tipo 1 e di tipo 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**Mediacollection. Add**](mediacollection-add.md)
</dt> <dt>

[**Playlist. setItemInfo**](playlist-setiteminfo.md)
</dt> <dt>

[**Playlist statiche e automatiche**](static-and-auto-playlists.md)
</dt> <dt>

[**Attributo SyncOnly**](synconly-attribute.md)
</dt> <dt>

[**Attributo WM/ContentDistributor**](wm-contentdistributor-attribute.md)
</dt> <dt>

[**Utilizzo della libreria**](working-with-the-library.md)
</dt> </dl>

 

 




