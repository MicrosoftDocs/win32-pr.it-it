---
title: Costanti di percorso della libreria
description: Costanti di percorso della libreria
ms.assetid: 88ff9b91-6b21-4f7d-ae13-e8456a3e0f75
keywords:
- Windows Media Player negozi online, costanti di posizione della libreria
- negozi online, costanti di posizione della libreria
- tipo 1 negozi online, costanti di posizione della libreria
- Windows Media Player negozi online, località
- negozi online, località
- tipo 1 negozi online, località
- Windows Media Player libreria, costanti di posizione
- library,costanti location
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45a677f405ff36030647618a83bd0b8b952dae254a756cebc48e4c3210e5fcde
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135364"
---
# <a name="library-location-constants"></a>Costanti di percorso della libreria

> [!Note]  
> Questa sezione descrive le funzionalità progettate per l'uso da parte dei negozi online. L'uso di questa funzionalità all'esterno del contesto di un negozio online non è supportato.

 

Le costanti di percorso della libreria sono variabili stringa globali definite in contentpartner.h. Vengono usati da determinati metodi delle [interfacce IWMPContentPartner](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner) e [IWMPContentPartnerCallback](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartnercallback) e da determinati metodi dell'oggetto External. [](external-object-for-type-1-online-stores.md) Queste costanti vengono usate per indicare i tipi seguenti.

-   Tipo di percorso della libreria: tipo di visualizzazione della libreria visualizzata da Windows Media Player. Ad esempio, il lettore potrebbe visualizzare una visualizzazione di un determinato album (g szCPAlbumID) o la visualizzazione di tutti i generi \_ (g \_ szAllCPGenreIDs).
-   Tipo di elemento selezionato: tipo di elemento selezionato nella visualizzazione libreria. Ad esempio, l'utente potrebbe selezionare un album specifico (g \_ szCPAlbumID) nella visualizzazione di tutti gli album.
-   Tipo di elenco: tipo di elenco richiesto dal plug-in partner di contenuti. Ad esempio, Windows Media Player chiedere al plug-in di fornire un elenco di elementi associati a una playlist specifica (g \_ szCPListID).
-   Tipo di elemento elenco: tipo di singolo elemento dell'elenco richiesto dal plug-in partner per il contenuto. Ad esempio, Windows Media Player potrebbe chiedere al plug-in di fornire l'elenco di tracce (g \_ szCPTrackID) in una playlist specifica.

La tabella seguente fornisce il nome e il valore di ogni costante e una breve descrizione del percorso o del tipo della libreria. Nel codice C o C++ compilato con il file di intestazione contentpartner.h è possibile usare il nome o il valore di una costante. L'uso del nome è preferibile perché il compilatore rileverà errori di ortografia. Nello script, ad esempio quando si chiamano i metodi [dell'oggetto External,](external-object-for-type-1-online-stores.md) non è possibile usare il nome di una costante. è necessario usare il valore .



| Nome                              | Valore                        | Località o tipo                                                                                                                                                   |
|-----------------------------------|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| g \_ szUnknownLocation              | UnknownLocation              | Set di tracce che non è né un album né una playlist. Windows Media Player usa anche questa costante nel raro caso in cui non sia in grado di determinare una posizione valida. |
| g \_ szRootLocation                 | RootLocation                 | Nodo superiore nel controllo visualizzazione albero della libreria                                                                                                                      |
| g \_ szFlyoutMenu                   | Riquadro a comparsaMenu                   | Menu a comparsa del negozio online corrente                                                                                                                             |
| g \_ szOnlineStore                  | OnlineStore                  | Tutti i negozi online                                                                                                                                                  |
| g \_ szCPListID                     | CPListID                     | Un singolo elenco                                                                                                                                                 |
| g \_ szAllCPListIDs                 | AllCPListIDs                 | Tutti gli elenchi                                                                                                                                                          |
| g \_ szCPTrackID                    | CPTrackID                    | Una traccia singola                                                                                                                                                |
| g \_ szAllCPTrackIDs                | AllCPTrackIDs                | Tutte le tracce                                                                                                                                                         |
| g \_ szCPArtistID                   | CPArtistID                   | Un singolo artista                                                                                                                                               |
| g \_ szAllCPArtistIDs               | AllCPArtistIDs               | Tutti gli artisti                                                                                                                                                        |
| g \_ szCPAlbumID                    | CPAlbumID                    | Un singolo album                                                                                                                                                |
| g \_ szAllCPAlbumIDs                | AllCPAlbumIDs                | Tutti gli album                                                                                                                                                         |
| g \_ szCPGenreID                    | CPGenreID                    | Un genere singolo                                                                                                                                                |
| g \_ szAllCPGenreIDs                | AllCPGenreIDs                | Tutti i generi                                                                                                                                                         |
| g \_ szCPAlbumSubGenreID            | CPAlbumSubGenreID            | Un singolo sottogenere                                                                                                                                             |
| g \_ szAllCPAlbumSubGenreIDs        | AllCPAlbumSubGenreIDs        | Tutti i sottogeneri                                                                                                                                                      |
| g \_ szReleaseDateYear              | ReleaseDateYear              | Anno in cui è stato rilasciato il contenuto del catalogo                                                                                                               |
| g \_ szAllReleaseDateYears          | AllReleaseDateYears          | Tutti gli anni in cui il contenuto del catalogo è stato rilasciato                                                                                                                        |
| g \_ szCPRadioID                    | CPRadioID                    | Un singolo flusso radio                                                                                                                                         |
| g \_ szAllCPRadioIDs                | AllCPRadioIDs                | Tutti i flussi radio                                                                                                                                                  |
| g \_ szAuthor                       | Autore                       | Un singolo autore                                                                                                                                               |
| g \_ szAllAuthors                   | AllAuthors                   | Tutti gli autori                                                                                                                                                        |
| g \_ szWMParentalRating             | WMParentalRating             | Una classificazione individuale dei genitori                                                                                                                                      |
| g \_ szAllWMParentalRatings         | AllWMParentalRatings         | Tutte le classificazioni dei genitori                                                                                                                                               |
| g \_ szUserEffectiveRatingStars     | UserEffectiveRatingStars     | Valutazione di un singolo utente, misurata come numero di stelle                                                                                                           |
| g \_ szAllUserEffectiveRatingStarss | AllUserEffectiveRatingStarss | Tutte le classificazioni utente                                                                                                                                                   |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**External.addToBasket**](external-addtobasket.md)
</dt> <dt>

[**External.buy**](external-buy.md)
</dt> <dt>

[**External.changeView**](external-changeview.md)
</dt> <dt>

[**External.changeViewOnlineList**](external-changeviewonlinelist.md)
</dt> <dt>

[**External.download**](external-download.md)
</dt> <dt>

[**External.libraryLocationType**](external-librarylocationtype.md)
</dt> <dt>

[**External.play**](external-play.md)
</dt> <dt>

[**IWMPContentPartner::GetCommands**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcommands)
</dt> <dt>

[**IWMPContentPartner::GetListContents**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getlistcontents)
</dt> <dt>

[**IWMPContentPartner::GetTemplate**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate)
</dt> <dt>

[**IWMPContentPartner::InvokeCommand**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-invokecommand)
</dt> <dt>

[**IWMPContentPartnerCallback::ChangeView**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-changeview)
</dt> </dl>

 

 




