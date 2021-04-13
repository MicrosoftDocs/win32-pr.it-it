---
title: Costanti percorso libreria
description: Costanti percorso libreria
ms.assetid: 88ff9b91-6b21-4f7d-ae13-e8456a3e0f75
keywords:
- Windows Media Player Online Store, costanti del percorso della libreria
- archivi online, costanti del percorso della libreria
- digitare 1 archivi online, costanti del percorso della libreria
- Windows Media Player Online Stores, località
- negozi online, località
- digitare 1 negozi online, località
- Windows Media Player Library, costanti location
- Library, costanti location
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38cbb297831acce9724988309880390cdcbe1894
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "104398759"
---
# <a name="library-location-constants"></a>Costanti percorso libreria

> [!Note]  
> In questa sezione viene descritta la funzionalità progettata per l'utilizzo da parte degli archivi online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.

 

Le costanti del percorso della libreria sono variabili di stringa globali definite in contentpartner. h. Vengono usati da determinati metodi delle interfacce [IWMPContentPartner](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner) e [IWMPContentPartnerCallback](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartnercallback) e da determinati metodi dell'oggetto [esterno](external-object-for-type-1-online-stores.md) . Queste costanti vengono utilizzate per indicare i tipi seguenti.

-   Tipo di percorso della libreria: questo è il tipo di visualizzazione della libreria visualizzata da Windows Media Player. Ad esempio, il lettore potrebbe visualizzare una visualizzazione di un album specifico (g \_ szCPAlbumID) o la visualizzazione di tutti i generi (g \_ szAllCPGenreIDs).
-   Tipo di elemento selezionato: è il tipo di elemento selezionato nella visualizzazione libreria. Ad esempio, l'utente potrebbe selezionare uno specifico album (g \_ szCPAlbumID) nella visualizzazione di tutti gli album.
-   Tipo di elenco: tipo di elenco richiesto dal plug-in del partner di contenuti. Ad esempio, Windows Media Player potrebbe chiedere al plug-in di fornire un elenco di elementi associati a una particolare playlist (g \_ szCPListID).
-   Tipo di elemento elenco: tipo di singolo elemento di elenco richiesto dal plug-in del partner di contenuti. Ad esempio, Windows Media Player potrebbe chiedere al plug-in di fornire l'elenco di tracce (g \_ szCPTrackID) in una particolare playlist.

La tabella seguente contiene il nome e il valore di ogni costante e una breve descrizione del tipo o del percorso della libreria. Nel codice C o C++ compilato con il file di intestazione contentpartner. h, è possibile usare il nome o il valore di una costante. È preferibile usare il nome perché il compilatore rileverà errori di ortografia. Nello script (ad esempio, quando si chiamano i metodi dell'oggetto [esterno](external-object-for-type-1-online-stores.md) ), non è possibile usare il nome di una costante. è necessario utilizzare il valore.



| Nome                              | Valore                        | Località o tipo                                                                                                                                                   |
|-----------------------------------|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| g \_ szUnknownLocation              | UnknownLocation              | Un set di tracce che non è né un album né una playlist. Windows Media Player usa anche questa costante nel raro caso in cui non sia in grado di determinare un percorso valido. |
| g \_ szRootLocation                 | RootLocation                 | Nodo principale nel controllo di visualizzazione ad albero della libreria                                                                                                                      |
| g \_ szFlyoutMenu                   | FlyoutMenu                   | Menu a comparsa del negozio online corrente                                                                                                                             |
| g \_ szOnlineStore                  | OnlineStore                  | Tutti i negozi online                                                                                                                                                  |
| g \_ szCPListID                     | CPListID                     | Elenco singolo                                                                                                                                                 |
| g \_ szAllCPListIDs                 | AllCPListIDs                 | Tutti gli elenchi                                                                                                                                                          |
| g \_ szCPTrackID                    | CPTrackID                    | Una singola traccia                                                                                                                                                |
| g \_ szAllCPTrackIDs                | AllCPTrackIDs                | Tutte le tracce                                                                                                                                                         |
| g \_ szCPArtistID                   | CPArtistID                   | Un singolo artista                                                                                                                                               |
| g \_ szAllCPArtistIDs               | AllCPArtistIDs               | Tutti gli artisti                                                                                                                                                        |
| g \_ szCPAlbumID                    | CPAlbumID                    | Un singolo album                                                                                                                                                |
| g \_ szAllCPAlbumIDs                | AllCPAlbumIDs                | Tutti gli album                                                                                                                                                         |
| g \_ szCPGenreID                    | CPGenreID                    | Un singolo genere                                                                                                                                                |
| g \_ szAllCPGenreIDs                | AllCPGenreIDs                | Tutti i generi                                                                                                                                                         |
| g \_ szCPAlbumSubGenreID            | CPAlbumSubGenreID            | Un singolo sottogenere                                                                                                                                             |
| g \_ szAllCPAlbumSubGenreIDs        | AllCPAlbumSubGenreIDs        | Tutti i sottogeneri                                                                                                                                                      |
| g \_ szReleaseDateYear              | ReleaseDateYear              | Anno singolo in cui è stato rilasciato il contenuto del catalogo                                                                                                               |
| g \_ szAllReleaseDateYears          | AllReleaseDateYears          | Tutti gli anni in cui è stato rilasciato il contenuto del catalogo                                                                                                                        |
| g \_ szCPRadioID                    | CPRadioID                    | Un singolo flusso di radio                                                                                                                                         |
| g \_ szAllCPRadioIDs                | AllCPRadioIDs                | Tutti i flussi radio                                                                                                                                                  |
| g \_ szAuthor                       | Autore                       | Singolo autore                                                                                                                                               |
| g \_ szAllAuthors                   | AllAuthors                   | Tutti gli autori                                                                                                                                                        |
| g \_ szWMParentalRating             | WMParentalRating             | Classificazione di singoli elementi padre                                                                                                                                      |
| g \_ szAllWMParentalRatings         | AllWMParentalRatings         | Tutte le classificazioni parentali                                                                                                                                               |
| g \_ szUserEffectiveRatingStars     | UserEffectiveRatingStars     | Classificazione utente individuale, misurata come numero di stelle                                                                                                           |
| g \_ szAllUserEffectiveRatingStarss | AllUserEffectiveRatingStarss | Tutte le classificazioni utente                                                                                                                                                   |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**External. addToBasket**](external-addtobasket.md)
</dt> <dt>

[**External. Buy**](external-buy.md)
</dt> <dt>

[**External. changeView**](external-changeview.md)
</dt> <dt>

[**External. changeViewOnlineList**](external-changeviewonlinelist.md)
</dt> <dt>

[**External. download**](external-download.md)
</dt> <dt>

[**External. libraryLocationType**](external-librarylocationtype.md)
</dt> <dt>

[**External. Play**](external-play.md)
</dt> <dt>

[**IWMPContentPartner:: GetCommands**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcommands)
</dt> <dt>

[**IWMPContentPartner::GetListContents**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getlistcontents)
</dt> <dt>

[**IWMPContentPartner:: GetTemplate**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate)
</dt> <dt>

[**IWMPContentPartner:: InvokeCommand**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-invokecommand)
</dt> <dt>

[**IWMPContentPartnerCallback::ChangeView**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-changeview)
</dt> </dl>

 

 




