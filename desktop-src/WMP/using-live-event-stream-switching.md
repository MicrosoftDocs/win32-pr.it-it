---
title: Uso del cambio di flusso di eventi live
description: Uso del cambio di flusso di eventi live
ms.assetid: fa8af007-2db6-438f-9551-8e748bb79ef4
keywords:
- Windows Playlist di metafile multimediali, cambio di flusso di eventi live
- playlist, cambio di flusso di eventi live
- playlist di metafile, cambio di flusso di eventi live
- Windows playlist di metafile multimediali, cambio di flusso di eventi
- playlist, cambio di flusso di eventi
- playlist di metafile, cambio di flusso di eventi
- Windows playlist di metafile multimediali,inserimento di annunci
- playlist, inserimento di annunci
- playlist di metafile, inserimento di annunci
- Windows Media Player, cambio di flusso di eventi live
- Windows Media Player, cambio di flusso di eventi
- Windows Media Player,inserimento di annunci
- cambio di flusso di eventi live
- cambio di flusso di eventi
- inserimento di annunci
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d8524fe1a83a6b3276c274726fa27fa7fcccb97b88f0384a54e5433d09380501
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134364"
---
# <a name="using-live-event-stream-switching"></a>Uso del cambio di flusso di eventi live

I supporti di streaming possono anche essere controllati dall'interazione di comandi script incorporati in un flusso multimediale con Windows metafile multimediali in una playlist di metafile.

Un evento è un particolare tipo di comando script incorporato in un flusso multimediale o in un file multimediale. Quando il Windows Media Player riceve il comando script, elabora l'evento come definito **dall'elemento EVENT** nella playlist del metafile. Windows Media Player passa dal flusso corrente di cui viene eseguito il rendering ed esegue il rendering del contenuto a cui si fa riferimento nell'elemento EVENT della playlist **del** metafile. **L'elemento EVENT** viene in genere usato nell'ambiente di produzione live.

Un **elemento EVENT** è simile a un elemento **ENTRY,** ma ognuno gestisce la riproduzione di flussi e file multimediali in modo diverso. **L'elemento ENTRY** viene usato per creare playlist. Un flusso o un file multimediale a cui si fa riferimento in un elemento **ENTRY** inizia la riproduzione al termine del flusso o del file multimediale a cui si fa riferimento nell'elemento **ENTRY** precedente. Un flusso a cui si fa riferimento in **un evento** viene riprodotto solo quando viene ricevuto un comando script specifico. Ad esempio, quando Windows Media Player riceve un comando script con la stringa di tipo "EVENT" e la stringa di comando "Adlink", cerca gli elementi seguenti nella playlist.


```XML
<EVENT NAME="Adlink" WHENDONE="RESUME"> 
    <ENTRY HREF=mms://www.proseware.com/adlink.wma />
</EVENT>

```



Windows Media Player quindi passa dal flusso live per riprodurre il flusso o il file multimediale contenuto **nell'evento**, in questo caso Adlink.wma. Il codice `WHENDONE="RESUME"` indica Windows Media Player di riprendere la riproduzione del flusso precedente al termine di Adlink.wma.

> [!Note]  
> La mancata gestione di ogni evento incorporato in un flusso multimediale o in un file multimediale può produrre risultati imprevisti.

 

Se si vuole usare il cambio di flusso di eventi live, è necessario includere un elemento **EVENT** nella playlist per gestire ogni comando di script di evento incorporato nei flussi multimediali o nei file multimediali nella playlist. Prima di creare la playlist, è necessario conoscere i dettagli sui comandi di script incorporati nel contenuto multimediale digitale. Se è presente un comando script di evento che si vuole che Windows Media Player ignori, includere un elemento **EVENT** nella playlist per gestire l'evento, ma fare riferimento a un URL fittizio nel gestore eventi.

## <a name="ad-insertion"></a>Inserimento di annunci

Questa tecnica può essere usata per l'inserimento di annunci. Ad esempio, durante una trasmissione Internet live di un gioco di palla, è possibile inviare un comando all'inizio di ogni interruzione commerciale che indica a ogni client (Windows Media Player) di riprodurre gli spot elencati nella playlist. Quando i client terminano la riproduzione degli spot pubblicitari, la playlist indica a ogni client di eseguire il cut-back alla trasmissione live. Il **rendering del** contenuto multimediale EVENT verrà eseguito solo quando il contenuto multimediale in streaming a cui si accede trasmette script incorporati con il nome **dell'EVENTO** corrispondente.

Le possibilità inerenti al cambio di evento sono più apprezzate rispetto al modo in cui gli annunci raggiungono gli utenti tramite la trasmissione standard over-the-air con il modo **in** cui gli annunci possono raggiungere gli utenti usando Windows Media Technologies. In un momento storico, gli annunci trasmessi potevano essere indirizzati solo approssimativamente ai visualizzatori, usando i dati delle classificazioni come criteri principali. Gli annunci inviati tramite Windows Media Technologies possono essere destinati direttamente all'utente di destinazione, perché gli **EVENT** e le playlist possono essere creati in tempo reale in base all'input dell'utente. Per altre informazioni, vedere [Personalizzazione del recapito multimediale.](personalizing-media-delivery.md)

È anche possibile usare playlist di metafile per visualizzare grafica, audio e testo personalizzati per la pubblicità. È possibile usare **l'elemento BANNER** come elemento figlio di un **evento** per visualizzare un messaggio grafico pubblicitario. **L'elemento BANNER** fornisce il percorso e il file contenente la grafica per il banner pubblicitario. È anche possibile fornire un collegamento a un sito o a un file usando **l'elemento figlio MOREINFO.** L'URL **nell'elemento MOREINFO** può fornire un collegamento a un numero ancora maggiore di annunci sul Web. Nell'esempio seguente viene illustrato l'utilizzo di questi elementi.

Codice di esempio


```XML
<BANNER HREF="SomePath\2.gif">
    <ABSTRACT>Read This Ad and Buy.</ABSTRACT>
    <MOREINFO HREF="https://www.proseware.com" />
</BANNER>

```



L'esempio seguente inserisce l'annuncio Advert.wma nel flusso unicast broadcast BallGame  quando un client riceve un evento di comando script con l'attributo **NAME** impostato su "Time-Out". **CLIENTSKIP è** impostato su NO per impedire che l'annuncio trasmesso venga ignorato. In questo esempio, l'annuncio trasmesso deve essere riprodotto prima di tornare al flusso originale. Al termine dell'annuncio, il client riprende la riproduzione del flusso originale.

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

[**Uso di playlist di metafile**](using-metafile-playlists.md)
</dt> <dt>

[**Windows Informazioni di riferimento per gli elementi metafile multimediali**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Guida ai metafile multimediali**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




