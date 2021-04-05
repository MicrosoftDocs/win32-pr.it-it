---
title: Tipi di visualizzazione testo
description: Tipi di visualizzazione testo
ms.assetid: 6aa3fc89-e5f5-420f-82e0-c605676078cb
keywords:
- Windows Media Player Mobile Skins, testo
- testo in interfacce, tipi di visualizzazione
- interfacce, testo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4fa8871d889a271bcbc59ce7b3118bc05be2eb7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709565"
---
# <a name="text-display-types"></a>Tipi di visualizzazione testo

Non è necessario includere le visualizzazioni di testo nell'interfaccia utente, ma è possibile scegliere tra molte istanze. È ad esempio possibile includere un TrackBar Seek per consentire all'utente di spostarsi in qualsiasi posizione dell'elemento multimediale, ma è anche possibile includere una visualizzazione di testo che mostra il numero di secondi trascorsi dall'inizio della riproduzione dell'elemento multimediale corrente.

**Caselle di visualizzazione**

Di seguito sono riportati diversi attributi che possono essere visualizzati in un elemento di testo:

-   Tempo
-   Playlist
-   Track\#
-   \#Tiene traccia
-   Titolo
-   Autore
-   Copyright
-   Nome file
-   FilenameExt
-   Bitrate
-   Frequenza
-   Stato
-   VolPercent

Per ulteriori informazioni sui tipi di visualizzazione del testo, vedere la sezione [testo](text.md) del riferimento all'interfaccia.

**Selezione scorrevole**

Oltre a usare i singoli elementi di testo, è possibile combinare uno o più attributi in uno scorrevole del testo di scorrimento. Questa opzione è utile se si desidera visualizzare un raggruppamento di informazioni di testo correlate in un'area di piccole dimensioni. Ad esempio, è possibile visualizzare le informazioni relative a titolo, autore e copyright in un Marquee.

Per ulteriori informazioni sulla creazione di un testo scorrevole, vedere la sezione [Marquee](marquee.md) del riferimento all'interfaccia.

**Visualizzazione dello stato**

Un altro tipo di visualizzazione del testo è la visualizzazione dello stato. In questo modo è possibile visualizzare automaticamente informazioni sullo stato corrente di Windows Media Player mobile. Ad esempio, la visualizzazione di stato informa l'utente quando un elemento multimediale memorizza nel buffer, in modo che sia evidente che il lettore funziona.

Nella finestra di stato vengono visualizzati i messaggi seguenti:

-   responseBuffering
-   Connecting
-   Paused
-   Playing
-   Ready
-   Arrestato

> [!Note]  
> Quando un elemento multimediale viene riprodotto, la visualizzazione dello stato viene ruotata attraverso il sottotitolo, l'artista, l'album, il genere e la velocità in bit corrente.

 

Per informazioni sulla creazione di una visualizzazione dello stato tramite l'elemento status, vedere la sezione relativa [allo stato](status.md) del riferimento all'interfaccia. Tuttavia, è preferibile usare l'attributo status nell'elemento Text anziché l'elemento status.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Funzionalità Windows Media Player Mobile**](windows-media-player-mobile-functionality.md)
</dt> </dl>

 

 




