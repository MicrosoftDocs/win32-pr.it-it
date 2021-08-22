---
title: Tipi di visualizzazione testo
description: Tipi di visualizzazione testo
ms.assetid: 6aa3fc89-e5f5-420f-82e0-c605676078cb
keywords:
- Windows Media Player Interfaccia per dispositivi mobili, testo
- testo nelle interfaccia, tipi di visualizzazione
- interfaccia, testo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01826f35db0d3877a3ecd34c351315872760b1b9b0713a36955bb3161ed6ba8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134604"
---
# <a name="text-display-types"></a>Tipi di visualizzazione testo

Non è necessario includere testo visualizzato nell'interfaccia, ma esistono molti casi in cui è consigliabile. Ad esempio, è possibile includere un trackbar Seek per consentire all'utente di spostarsi in qualsiasi posizione nell'elemento multimediale, ma è anche possibile includere una visualizzazione testo che mostra il numero di secondi trascorsi dall'inizio della riproduzione dell'elemento multimediale corrente.

**Caselle di visualizzazione**

Di seguito sono riportati diversi attributi che un elemento di testo può visualizzare:

-   Ora
-   Playlist
-   Track\#
-   \#Tracce
-   Titolo
-   Autore
-   Copyright
-   Nome file
-   FilenameExt
-   Bitrate
-   Frequenza
-   Stato
-   VolPercent

Per altre informazioni sui tipi di visualizzazione del testo, vedere la [sezione Text](text.md) di Riferimenti all'interfaccia.

**Scrolling Marquee**

Oltre a usare i singoli elementi di testo, è possibile combinare uno o più attributi in una cornice di testo scorrente. Ciò è utile se si desidera visualizzare un raggruppamento di informazioni di testo correlate in una piccola area. Ad esempio, è possibile visualizzare le informazioni relative a titolo, autore e copyright in una cornice.

Per altre informazioni sulla creazione di una cornice di testo, vedere la [sezione Marquee](marquee.md) di Riferimento all'interfaccia.

**Visualizzazione dello stato**

Un altro tipo di visualizzazione del testo è la visualizzazione dello stato. In questo modo è possibile visualizzare automaticamente le informazioni sullo stato corrente di Windows Media Player Mobile. Ad esempio, la visualizzazione dello stato informerà l'utente quando un elemento multimediale viene memorizzato nel buffer in modo che sia evidente che il lettore funziona.

Nella visualizzazione dello stato vengono visualizzati i messaggi seguenti:

-   responseBuffering
-   Connecting
-   Paused
-   Playing
-   Ready
-   Arrestato

> [!Note]  
> Quando viene riprodotto un elemento multimediale, la visualizzazione dello stato ruota tra sottotitolo, artista, album, genere e velocità in bit corrente.

 

Per informazioni sulla creazione di una visualizzazione dello stato tramite l'elemento Status, vedere la [sezione Status](status.md) in Riferimenti all'interfaccia; È tuttavia preferibile usare l'attributo status nell'elemento Text anziché l'elemento Status.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Windows Media Player Funzionalità per dispositivi mobili**](windows-media-player-mobile-functionality.md)
</dt> </dl>

 

 




