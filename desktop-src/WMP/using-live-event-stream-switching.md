---
title: Uso del cambio di flusso di eventi Live
description: Uso del cambio di flusso di eventi Live
ms.assetid: fa8af007-2db6-438f-9551-8e748bb79ef4
keywords:
- Playlist Windows Media Metafile, cambio di flusso di eventi Live
- playlist, cambio di flusso di eventi Live
- playlist di metafile, cambio di flusso di eventi Live
- Playlist Windows Media Metafile, cambio di flusso di eventi
- playlist, cambio di flusso di eventi
- playlist di metafile, cambio di flusso di eventi
- Playlist Windows Media Metafile, inserimento ad
- playlist, inserimento di annunci
- playlist di metafile, inserimento di annunci
- Windows Media Player, cambio di flusso di eventi Live
- Windows Media Player, cambio del flusso di eventi
- Windows Media Player, inserimento di annunci
- cambio di flusso di eventi Live
- cambio di flusso di eventi
- inserimento ad
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: fd5c586e0f1ef2b36913dee822e461daeffbfcbf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221136"
---
# <a name="using-live-event-stream-switching"></a>Uso del cambio di flusso di eventi Live

I flussi multimediali possono anche essere controllati dall'interazione dei comandi di script incorporati in un flusso multimediale con elementi metafile di Windows Media in una playlist di metafile.

Un evento è un particolare tipo di comando di script incorporato in un flusso multimediale o in un file multimediale. Quando il controllo Windows Media Player riceve il comando script, l'evento viene elaborato come definito dall'elemento **Event** nella playlist del metafile. Windows Media Player passa dal flusso corrente in cui viene eseguito il rendering ed esegue il rendering del contenuto a cui si fa riferimento nell'elemento dell' **evento** della playlist del metafile. L'elemento **Event** viene in genere usato nella produzione in tempo reale.

Un elemento **evento** è simile a un elemento **entry** , ma ogni gestisce la riproduzione di flussi e file multimediali in modo diverso. L'elemento **entry** viene usato per creare playlist. Un flusso o un file multimediale a cui si fa riferimento in un elemento **entry** inizia la riproduzione quando il flusso o il file multimediale a cui viene fatto riferimento nella **voce** precedente termina. Un flusso a cui viene fatto riferimento in un **evento** viene riprodotto solo quando viene ricevuto un comando di script specifico. Ad esempio, quando Windows Media Player riceve un comando script con tipo stringa "EVENT" e la stringa di comando "AdLINK", Cerca nella playlist gli elementi seguenti.


```XML
<EVENT NAME="Adlink" WHENDONE="RESUME"> 
    <ENTRY HREF=mms://www.proseware.com/adlink.wma />
</EVENT>

```



Windows Media Player quindi passa dal flusso Live per riprodurre il flusso o il file multimediale contenuto nell' **evento**, in questo caso AdLINK. WMA. Il codice `WHENDONE="RESUME"` indica a Windows Media Player di riprendere la riproduzione del flusso precedente al termine di AdLINK. WMA.

> [!Note]  
> La mancata gestione di ogni evento incorporato in un flusso multimediale o in un file multimediale può produrre risultati imprevisti.

 

Se si vuole usare il cambio di flusso di eventi live, è necessario includere un elemento **Event** nella playlist per gestire ogni comando di script degli eventi incorporato nei flussi multimediali o nei file multimediali della playlist. Prima di creare la playlist, è necessario conoscere i dettagli relativi ai comandi di script incorporati nel contenuto multimediale digitale. Se è presente un comando script di evento che si desidera ignorare con Windows Media Player, includere un elemento **Event** nella playlist per gestire l'evento, ma fare riferimento a un URL fittizio nel gestore eventi.

## <a name="ad-insertion"></a>Inserimento ad

Questa tecnica può essere utilizzata per l'inserimento di annunci. Ad esempio, durante una trasmissione Internet diretta di una partita a palla, è possibile inviare un comando all'inizio di ogni break pubblicitario che indica a ogni client (Windows Media Player) di riprodurre le pubblicità elencate nella propria playlist. Quando i client terminano la riproduzione dei dati commerciali, la playlist indica a ogni client di tornare alla trasmissione live. Il rendering del contenuto multimediale dell' **evento** verrà eseguito solo quando il supporto di streaming a cui si accede trasmette lo scripting incorporato con il nome dell' **evento** corrispondente.

Le possibilità inerenti al cambio di **eventi** sono particolarmente apprezzate, a differenza del modo in cui gli annunci raggiungono i visualizzatori attraverso la trasmissione standard e in modalità wireless con il modo in cui gli annunci possono raggiungere i visualizzatori usando le tecnologie In passato, gli annunci broadcast potevano essere indirizzati solo ai visualizzatori, usando i dati di classificazione come criterio primario. Gli annunci inviati usando le tecnologie Windows Media possono essere indirizzati direttamente all'utente di destinazione perché **gli eventi** e le playlist possono essere creati in tempo reale in base all'input dell'utente. Per altre informazioni, vedere [personalizzazione del recapito multimediale](personalizing-media-delivery.md).

È anche possibile usare le playlist di metafile per visualizzare grafica, audio e testo personalizzati per la pubblicità. È possibile usare l'elemento **banner** come elemento figlio di un **evento** per visualizzare un'immagine di messaggio pubblicitario. L'elemento **banner** fornisce il percorso e il file che contiene la grafica per il banner pubblicitario. È anche possibile fornire un collegamento a un sito o a un file usando l'elemento figlio **moreinfo** . L'URL nell'elemento **moreinfo** può fornire un collegamento a un numero ancora maggiore di annunci sul Web. Nell'esempio seguente viene illustrato l'utilizzo di questi elementi.

Codice di esempio


```XML
<BANNER HREF="SomePath\2.gif">
    <ABSTRACT>Read This Ad and Buy.</ABSTRACT>
    <MOREINFO HREF="https://www.proseware.com" />
</BANNER>

```



L'esempio seguente inserisce il file annuncio. WMA nel flusso di trasmissione unicast broadcast quando un client riceve un **evento** del comando script con l'attributo **Name** impostato su "timeout". **CLIENTSKIP** è impostato su No per impedire che l'annuncio trasmesso venga ignorato. In questo esempio, il flusso di Active Directory deve essere riprodotto prima di tornare al flusso originale. Al termine dell'annuncio, il client riprende la riproduzione del flusso originale.

Codice di esempio


```XML
<ASX VERSION="3.0">
    <ENTRY>
        <REF HREF="mms://proseware.com/BallGame" />
    </ENTRY>
    <EVENT NAME="Time-Out" WHENDONE="RESUME">
        <ENTRY>
            <REF HREF = "mms://proseware.com/Advert.wma" 
                CLIENTSKIP = "NO" />
       </ENTRY>
    </EVENT>
</ASX>

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Playlist di metafile**](metafile-playlists.md)
</dt> <dt>

[**Uso delle playlist di metafile**](using-metafile-playlists.md)
</dt> <dt>

[**Riferimento agli elementi metafile di Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Guida ai metafile di Windows Media**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




