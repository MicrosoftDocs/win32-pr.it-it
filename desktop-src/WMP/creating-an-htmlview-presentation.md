---
title: Creazione di una presentazione HTMLView
description: Creazione di una presentazione HTMLView
ms.assetid: 70203160-2dd9-4096-be6a-c704db757f7f
keywords:
- Playlist Windows Media Metafile, presentazioni HTMLView
- playlist, presentazioni HTMLView
- playlist di metafile, presentazioni HTMLView
- Playlist Windows Media Metafile, creazione di presentazioni HTMLView
- playlist, creazione di presentazioni HTMLView
- playlist di metafile, creazione di presentazioni HTMLView
- creazione di presentazioni HTMLView
- Windows Media Player, creazione di presentazioni HTMLView
- Windows Media Player, presentazioni HTMLView
- HTMLView, creazione di presentazioni
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1094ce787e55fbeb98e628389b5fd51ab94ab415
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396294"
---
# <a name="creating-an-htmlview-presentation"></a>Creazione di una presentazione HTMLView

Per creare una presentazione HTMLView di base, sono necessari almeno tre elementi:

-   **Contenuto multimediale digitale.** Si tratta di uno o più file audio o video riprodotti da Windows Media Player.
-   **Una pagina Web.** Si tratta del contenuto basato sul Web che viene visualizzato nella funzionalità **Now Play** dell'interfaccia utente del lettore.
-   **Metafile di Windows Media.** Si tratta della playlist di metafile che indica a Windows Media Player di combinare il contenuto multimediale digitale con la pagina Web.

Un file con estensione asx è un file di testo che fornisce informazioni su un flusso di file e la relativa presentazione. In base alla sintassi Extensible Markup Language (XML), i file con estensione ASX possono contenere diversi elementi, ciascuno identificato da un tag con attributi associati. L'elemento **param** fornisce un modo per associare un parametro personalizzato a una voce specifica in una playlist di metafile o all'intero metafile. Uno dei nomi di parametro predefiniti disponibili per l'utilizzo è "HTMLView". Si tratta del parametro che determina la visualizzazione della pagina Web specificata dal valore URL in Windows Media Player.

Il codice di esempio seguente mostra un file con estensione asx che combina un singolo file multimediale digitale con una singola pagina Web:


```XML
<ASX version="3.0">
<PARAM name="HTMLView" value="https://www.proseware.com/htmlview.htm"/>

<ENTRY>
   <REF href="rtsp://www.proseware.com/content1.wma"/>
</ENTRY>

</ASX>

```



Quando in Windows Media Player viene aperto il file con estensione asx nell'esempio precedente, l'audio viene riprodotto dal file denominato Content1. WMA e viene visualizzata la pagina Web denominata htmlview.htm nella funzionalità **ora di riproduzione** del lettore in modalità completa. L'utente può sospendere, cercare e arrestare il contenuto audio usando i controlli Media Player di Windows.

È possibile modificare facilmente la pagina Web visualizzata per ogni parte del contenuto associando un elemento **param** a ogni voce, come illustrato nell'esempio di codice seguente:


```XML
<ASX version="3.0">

<ENTRY>
   <PARAM name="HTMLView" value="https://www.proseware.com/htmlview1.htm"/>
   <REF href="rtsp://www.proseware.com/content1.wma"/>
</ENTRY>

<ENTRY>
   <PARAM name="HTMLView" value="https://www.proseware.com/htmlview2.htm"/>
   <REF href="rtsp://www.proseware.com/content2.wma"/>
</ENTRY>

</ASX>

```



Nell'esempio precedente, Windows Media Player Visualizza prima di tutto la pagina Web htmlview1.htm durante la riproduzione del file audio digitale Content1. WMA. Quando il giocatore apre la voce successiva nella playlist, Content2. WMA, la pagina Web visualizzata in **Now Playing** changes to htmlview2.htm. In questo modo, è possibile specificare la pagina Web visualizzata dall'utente per ogni contenuto multimediale digitale.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Visualizzazione di pagine Web in Windows Media Player**](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[**PARAM (elemento)**](param-element.md)
</dt> </dl>

 

 




