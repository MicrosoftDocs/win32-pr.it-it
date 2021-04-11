---
title: Personalizzazione del recapito multimediale
description: Personalizzazione del recapito multimediale
ms.assetid: ffd62602-8bfc-4ca7-91fd-c610faa330cd
keywords:
- Playlist Windows Media Metafile, personalizzazione del recapito multimediale
- playlist, personalizzazione del recapito multimediale
- playlist di metafile, personalizzazione del recapito multimediale
- Playlist Windows Media Metafile, personalizzazione del recapito multimediale
- playlist, personalizzazione del recapito multimediale
- playlist di metafile, personalizzazione del recapito multimediale
- personalizzazione del recapito multimediale
- personalizzazione del recapito multimediale
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ddb01364e2ea36214b94d01517f1d3d3b802ba63
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221018"
---
# <a name="personalizing-media-delivery"></a>Personalizzazione del recapito multimediale

A differenza della comunicazione unidirezionale che trasmette contenuto identico a un pubblico di massa, le tecnologie Windows Media forniscono gli strumenti per usare i dati demografici per individuare le trasmissioni. Con Internet, la comunicazione bidirezionale su larga scala è immediatamente disponibile. Questo interscambio dinamico di informazioni consente ai provider di contenuti di conoscerne i destinatari e rispondere con presentazioni personalizzate.

Nell'esempio seguente, usando una società fittizia, viene illustrato come è possibile personalizzare la distribuzione di contenuti in streaming. In questa discussione si presuppone che l'utente abbia familiarità con Active Server pagine (file ASP o ASP) e definendo le variabili.

News Network è un'organizzazione di notizie di broadcast fittizio che ha ampliato le proprie operazioni per includere un sito Web. La funzionalità principale del sito è una sezione in cui gli utenti possono creare telegiornali personalizzati. Anziché visualizzare un telegiornale tradizionale destinato a un pubblico di massa, un utente visualizza un programma di notizie completo che contiene solo argomenti di interesse personale. La sequenza seguente descrive un'esperienza utente tipica.

1.  Un nuovo utente passa al sito e fa clic su **Crea il telegiornale personale**.
2.  Verrà visualizzato un modulo preferenza. In questo formato, l'utente risponde alle domande relative alle preferenze personali, ad esempio le storie di notizie preferite, le storie di notizie preferite, i passatempi e il metodo usuale per ricevere notizie giornaliere.
3.  L'utente invia queste informazioni e, dopo alcuni secondi, Visualizza un telegiornale completo di 15 minuti che contiene contenuto del programma, transizioni e commerciali. La selezione di ogni elemento multimediale, inclusi gli annunci pubblicitari, si basa sul profilo utente e viene eseguita automaticamente con i componenti di Windows Media Technologies e gli strumenti Internet disponibili.

L'elenco seguente descrive il modo in cui i vari strumenti interagiscono per creare un telegiornale personalizzato.

1.  Il modulo di preferenza che l'utente compila è una pagina di Active Server (ASP) (Choices. asp). I dati ottenuti dal formato preferenza vengono analizzati da due componenti server. Un componente usa le informazioni per eseguire una query su un database Microsoft SQL Server di storie di notizie. L'altro componente è un server ad che usa un set complesso di regole in base ai requisiti contrattuali e ai dati demografici per pianificare gli annunci appropriati per l'utente in quel momento.
2.  I due database restituiscono parti diverse di una playlist. Il database di News Story restituisce un set di voci di storie appropriate e il server di Active Directory restituisce un set di voci commerciali appropriate.
3.  Una seconda pagina ASP (PlayShow. asp) riceve le voci dal database di News Story e da ad server e combina quelle con le voci di visualizzazione standard di apertura, chiusura e transizione. Tutte le voci vengono quindi disposte in base al modello fornito da PlayShow. asp e la pagina ASP restituisce una playlist per l'utente.
4.  Il controllo Windows Media Player incorporato nel computer dell'utente riproduce la playlist dall'inizio alla fine e l'utente visualizza un telegiornale personalizzato.

L'esempio seguente è una parte di un file di playlist che un utente può ricevere. Ad essi sono stati aggiunti banner ad, collegamenti MOREINFO ed ABSTRACT.


```XML
<ASX Version="3">
<TITLE>MyPersonalized NewsCast</TITLE>
<ENTRY ClientSkip="no">
    <!<entity type="mdash"/>- Commercial Element 1 -->
    <REF HREF="mms://proseware.com/Commercial.wma" />
    <BANNER HREF="https://www.proseware.com/images/MoreInfo.gif" >
        <MOREINFO HREF="https://www.proseware.com" target="_blank" />
    <ABSTRACT>Courtesy of Windows Media Technologies
    </ABSTRACT>
    </BANNER>
</ENTRY>
<ENTRY>
    <!<entity type="mdash"/>- Program Element 1 -->
    <TITLE>A Celebrity's Life</TITLE>
    <COPYRIGHT>Copyright 2004</COPYRIGHT>
    <REF HREF="mms://proseware.com/SomePath/TheFile.wma" />
    <ABSTRACT>
     :: A celebrity looks back on her career after 40 years in public life.
    </ABSTRACT>
    <COPYRIGHT>Copyright 2004-- All Rights
         Reserved
    </COPYRIGHT>
</ENTRY>

<ENTRY>
    <!<entity type="mdash"/>Program Element 2 -->
    <TITLE>City council votes to build new bicycle path</TITLE>
    <COPYRIGHT>Copyright 2004</COPYRIGHT>
    <REF HREF="mms://proseware.com/SomePath/MyFile.wma" />
    <ABSTRACT>
        :: Some residents opposed changing the landscape in the public parks to accommodate bicycles.
    </ABSTRACT>
    <COPYRIGHT>Copyright 2004 -- All Rights Reserved
    </COPYRIGHT>
</ENTRY>
</ASX>

```



-   Ogni riferimento a società, organizzazioni, prodotti, persone ed eventi utilizzati negli esempi è puramente casuale e ha il solo scopo di illustrare l'uso del prodotto Microsoft.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Creazione di playlist di metafile**](creating-metafile-playlists.md)
</dt> <dt>

[**Playlist di metafile**](metafile-playlists.md)
</dt> <dt>

[**Uso delle playlist di metafile**](using-metafile-playlists.md)
</dt> <dt>

[**Riferimento agli elementi metafile di Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Guida ai metafile di Windows Media**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




