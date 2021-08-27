---
title: Personalizzazione del recapito multimediale
description: Personalizzazione del recapito multimediale
ms.assetid: ffd62602-8bfc-4ca7-91fd-c610faa330cd
keywords:
- Windows playlist di metafile multimediali, personalizzazione della distribuzione di file multimediali
- playlist, personalizzazione della distribuzione di file multimediali
- playlist di metafile, personalizzazione della distribuzione di file multimediali
- Windows playlist di metafile multimediali, personalizzazione della distribuzione di contenuti multimediali
- playlist, personalizzazione della distribuzione di contenuti multimediali
- playlist di metafile, personalizzazione della distribuzione di contenuti multimediali
- personalizzazione della distribuzione di contenuti multimediali
- personalizzazione del recapito multimediale
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9483f4fc7a068c6f6456a5d170b4be73a9ba31ef85294f9a6939181dff00c826
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996011"
---
# <a name="personalizing-media-delivery"></a>Personalizzazione del recapito multimediale

A differenza della comunicazione unidirezionale che trasmette contenuto identico a un pubblico di massa, Windows Media Technologies offre gli strumenti per usare i dati demografici per individualizzare le trasmissioni. Con Internet, la comunicazione bidirezionale su larga scala è immediatamente disponibile. Questo interscambio dinamico di informazioni consente ai provider di contenuti di conoscere i destinatari e rispondere con presentazioni personalizzate.

L'esempio seguente, che usa una società fittizia, illustra come è possibile personalizzare la distribuzione di contenuti in streaming. In questa discussione si presuppone che si abbia familiarità con Active Server pagine (file ASP o ASP) e con la definizione delle variabili.

News Network è un'organizzazione fittizia di notizie trasmesse che ha ampliato le proprie operazioni per includere un sito Web. La funzionalità principale del sito è una sezione in cui gli utenti possono creare newscast personalizzati. Invece di visualizzare un newscast tradizionale destinato a un pubblico di massa, un utente visualizza un programma di notizie completo che contiene solo argomenti di interesse personale. La sequenza seguente descrive un'esperienza utente tipica.

1.  Un nuovo utente passa al sito e fa clic su **Create Your Personal Newscast (Crea il tuo newscast personale).**
2.  Verrà aperto un modulo delle preferenze. In questo modulo l'utente risponde alle domande relative alle preferenze personali, ad esempio le notizie preferite, le notizie meno preferite, gli hobbies e il metodo consueto per ricevere notizie giornaliere.
3.  L'utente invia queste informazioni e pochi secondi dopo visualizza un newscast personale completo di 15 minuti contenente il contenuto del programma, le transizioni e gli spot pubblicitari. La selezione di ogni elemento multimediale, inclusi gli spot pubblicitari, si basa sul profilo utente e viene eseguita automaticamente con i componenti di Windows Media Technologies e gli strumenti Internet pronti all'uso.

Nell'elenco seguente viene descritto come interagiscono i vari strumenti per creare un newscast personalizzato.

1.  Il modulo delle preferenze che l'utente compila è Active Server pagina web (ASP) (Choices.asp). I dati ottenuti dal form delle preferenze vengono analizzati da due componenti server. Un componente usa le informazioni per eseguire query su un database Microsoft SQL Server di notizie. L'altro componente è un server di annunci che usa un set complesso di regole basate su requisiti contrattuali e dati demografici per pianificare annunci appropriati per l'utente in quel momento.
2.  I due database restituiscono parti diverse di una playlist. Il database delle notizie restituisce un set di voci della storia appropriate e il server di annunci restituisce un set di voci commerciali appropriate.
3.  Una seconda pagina ASP (PlayShow.asp) riceve le voci dal database delle notizie e dal server di annunci e le combina con le voci standard di apertura, chiusura e transizione. Tutte le voci vengono quindi disposte in base al modello fornito da PlayShow.asp e la pagina ASP restituisce una playlist all'utente.
4.  Il controllo Windows Media Player sul computer dell'utente riproduce la playlist dall'inizio alla fine e visualizza un newscast personalizzato.

L'esempio seguente è una parte di un file di playlist che un utente potrebbe ricevere. Sono stati aggiunti banner pubblicitari, collegamenti MOREINFO e ABSTRACTS.


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

[**Uso di playlist di metafile**](using-metafile-playlists.md)
</dt> <dt>

[**Windows Informazioni di riferimento per gli elementi metafile multimediali**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Guida ai metafile multimediali**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




