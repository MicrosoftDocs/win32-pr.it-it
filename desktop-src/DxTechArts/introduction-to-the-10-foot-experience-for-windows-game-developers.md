---
title: Introduzione all'esperienza a 10 piedi per gli sviluppatori di giochi Windows
description: Questo articolo illustra l'esperienza di 10 metri ed Esplora l'elenco di elementi da considerare prima di questo nuovo modello di interazione, anche se non si prevede che il gioco venga riprodotto in questo modo.
ms.assetid: 126a0aae-6a7a-8cda-5748-c364e54c304e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4814c76aeefdadbe1fd8bf9dc4c21cd84612671
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2020
ms.locfileid: "104399849"
---
# <a name="introduction-to-the-10-foot-experience-for-windows-game-developers"></a>Introduzione all'esperienza a 10 piedi per gli sviluppatori di giochi Windows

Un numero crescente di persone usa i computer personali in modo completamente nuovo. Quando si pensa all'interazione tipica con un computer basato su Windows, è probabile che si preveda di sedersi a una scrivania con un monitor e di usare il mouse e la tastiera (o forse un dispositivo joystick); Questa operazione è detta esperienza a 2 piedi ed è comunque lo scenario più comune per i giochi di Windows, ma c'è un'altra tendenza che probabilmente inizierà a ricevere altre informazioni: l'esperienza a 10 piedi, che descrive l'uso del computer come dispositivo di intrattenimento con l'output in una TV. Questo articolo illustra l'esperienza di 10 metri ed Esplora l'elenco di elementi da considerare prima di questo nuovo modello di interazione, anche se non si prevede che il gioco venga riprodotto in questo modo. Una parte dei clienti eseguirà il gioco basato su Windows in un computer che esegue Windows Media Center. è preferibile sapere quale sarà l'esperienza prima che i clienti lo provino.

-   [Che cos'è Windows Media Center?](#what-is-windows-media-center)
-   [Esperienza a 10 piedi](#the-10-foot-experience)
    -   [Installazione](#installation)
    -   [Input utente](#user-input)
    -   [Schermo](#display)
-   [Proporzioni e widescreen](#aspect-ratio-and-widescreen)
-   [Area indipendente dal titolo](#title-safe-region)
-   [Suggerimenti per NTSC](#ntsc-suggestions)
    -   [Blocca i valori del componente colore RGB tra 16 e 235](#clamp-the-rgb-color-component-values-between-16-and-235)
    -   [Evitare colori simili che potrebbero apparire identici](#avoid-similar-colors-that-might-appear-identical)
    -   [Evitare differenze acute al contrasto](#avoid-sharp-differences-in-contrast)
-   [Conclusione](#conclusion)

## <a name="what-is-windows-media-center"></a>Che cos'è Windows Media Center?

Windows Media Center può fungere da interfaccia per le funzionalità multimediali del computer host. Il sito Web per questa funzionalità, [Windows Media Center Home](https://windows.microsoft.com/windows/products/windows-media-center/), offre un'introduzione completa e Mostra tutte le informazioni valide disponibili nella versione più recente. Media Center è incluso in Windows XP Media Center Edition, Windows Vista Home Premium, Windows Vista Ultimate e la maggior parte delle edizioni di Windows 7.

In passato, l'unico modo per ottenere Windows Media Center era quello di acquistare un PC di Media Center da un produttore di sistemi di livello 1, ma poiché Windows Media Center è ora incluso in due edizioni di Windows Vista, il Marketplace potenziale è ora molto più grande.

## <a name="the-10-foot-experience"></a>Esperienza a 10 piedi

Windows Media Center è stato progettato in modo da consentire agli utenti di utilizzare Windows per un'esperienza di intrattenimento con spazio di lavoro completo e segue che la maggior parte degli utenti preferisce interagire in modo diverso con Windows Media Center in modo diverso rispetto alle applicazioni per computer tradizionali. Per uno, se il cliente usa il computer nella sala living per l'intrattenimento, è probabile che il video venga visualizzato in un computer diverso da quello di un monitor di computer convenzionale: televisori analoghi, TV digitale ad alta definizione e un numero qualsiasi di schermi LCD sono tutti probabili candidati. Questi tipi di visualizzazione vengono in genere visualizzati da una distanza di circa 10 metri, di conseguenza l'esperienza dell'etichetta a *10 piedi*.

L'esperienza di 10 metri non è confinata agli utenti di Windows Media Center; negli ultimi anni, gli utenti possono connettere la propria workstation o il computer notebook al sistema TV e audio. È sempre più comune per i dispositivi di visualizzazione del consumer esporre le connessioni RGB o DVI, ovvero le porte di output video standard nei computer. Inoltre, le porte S-video sono una caratteristica tipica delle schede video di fascia alta e offrono un modo semplice per eseguire l'output in un dispositivo di visualizzazione alternativo.

Esistono alcune importanti linee guida di progettazione da considerare per una piacevole esperienza a 10 piedi: installazione, input utente e visualizzazione.

### <a name="installation"></a>Installazione

Durante la media dell'esperienza a 2 piedi, l'utente raggiunge la distanza del computer; Se durante l'avvio o il gioco è necessario che l'utente inserisca o Commuti il contenuto multimediale, l'utente può rimanere seduto almeno. L'esperienza media di 10 metri posiziona il computer nell'intera stanza dall'utente e, di conseguenza, qualsiasi elemento che richiede all'utente di interagire fisicamente con il computer impone all'utente di entrare e attraversare la stanza. Per questo motivo, gli sviluppatori devono evitare di forzare l'utente a modificare i supporti; prendere in considerazione la possibilità di eseguire un'installazione completa dell'applicazione sul disco rigido.

### <a name="user-input"></a>Input utente

Un'altra funzionalità di Windows Media Center è il supporto per un controllo remoto standard, che è il dispositivo di input preferito in genere. Sebbene il genere del titolo del gioco decida in gran parte se il controllo remoto è adatto per fornire l'input del gioco, è comunque possibile consentire all'utente di sospendere il gioco e accedere ai menu dei giochi usando il controllo remoto; Tuttavia, assicurarsi di consentire anche all'utente di controllare i menu usando il dispositivo di input del gioco primario. Per ulteriori informazioni sulla progettazione e sullo sviluppo per Windows Media Center e i relativi dispositivi, vedere [Windows Media Center Software Development Kit](/previous-versions/msdn10/bb895967(v=msdn.10)) in MSDN.

Evitare qualsiasi interazione fisica tra l'utente e il computer o le relative periferiche. Richiedere all'utente di modificare i controller di input durante il gioco è indesiderato, perché è probabile che sia vicino solo al dispositivo di input primario.

Microsoft ha creato controller di gamepad comuni per l'uso con Windows e Xbox 360, il controller Xbox 360 per Windows e il controller wireless Xbox 360 per Windows. Assicurandosi che il titolo riproduca correttamente sui controller comuni faciliterà una certa parte della cefalea associata al test del gioco contro potenziali dispositivi di input.

### <a name="display"></a>Visualizza

L'ampia gamma di potenziali dispositivi di visualizzazione offre consigli sulla visualizzazione complessa e ogni tipo di dispositivo presenta Avvertenze particolari. Di seguito sono riportati alcuni dei problemi che riguardano tecnologie di visualizzazione specifiche più avanti in questo documento. Indipendentemente dal dispositivo di output video, è importante che i tipi di carattere e le dimensioni della grafica dell'interfaccia utente siano sufficientemente grandi per una leggibilità comoda a una distanza di 10 metri. Si noti inoltre che i tipi di carattere con aliasing offrono in genere una migliore leggibilità.

È inoltre consigliabile evitare linee orizzontali ed elementi statici dell'interfaccia utente con uno spessore o un dettaglio di singolo pixel. I televisori precedenti potrebbero non visualizzare i dettagli e anche nei dispositivi di visualizzazione più recenti, il contenuto sfarfallerà quando viene eseguito in modalità interlacciata, perché una singola riga di pixel è visibile solo metà del tempo. Come sostituzione per piccoli dettagli, tenere presente che una linea grigia da 2 pixel appare più sottile rispetto a una linea bianca da 2 pixel. Si tratta essenzialmente della sfocatura di una linea bianca da 1 pixel.

## <a name="aspect-ratio-and-widescreen"></a>Proporzioni e widescreen

Proporzioni descrive la percentuale di larghezza e altezza dello schermo. Gli schermi TV standard e monitor computer presentano proporzioni pari a 4:3, vale a dire che per ogni 4 pixel in esecuzione lungo la larghezza del buffer dei frame sono presenti 3 pixel lungo l'altezza (talvolta rappresentata anche come 1,33).

Con l'avvento di HDTV, una proporzione di 16:9, nota anche come wide screen, è diventata lo standard per il futuro della TV e, insieme a Enhanced-Definition TV (EDTV), sono disponibili tre modalità di visualizzazione che è probabile che si verifichino:

<dl> <dt>

<span id="480p_EDTV"></span><span id="480p_edtv"></span><span id="480P_EDTV"></span>480p EDTV
</dt> <dd>

480 righe di analisi presentate gradualmente. Questa modalità può restituire 4:3 (con una risoluzione del buffer del frame di 640 × 480) o 16:9 (720 × 480).

</dd> <dt>

<span id="720p_HDTV"></span><span id="720p_hdtv"></span><span id="720P_HDTV"></span>720p HDTV
</dt> <dd>

720 righe di analisi presentate gradualmente. Questa modalità è sempre 16:9 (1280 × 720).

</dd> <dt>

<span id="1080i_HDTV"></span><span id="1080i_hdtv"></span><span id="1080I_HDTV"></span>1080i HDTV
</dt> <dd>

1080 righe di analisi presentate interlacciate. Questa modalità è sempre 16:9 (1920 × 1080 o 1920 × 540 se si esegue il rendering dei campi interlacci separatamente).

</dd> </dl>

Se il gioco è hardcoded per funzionare in proporzioni di 4:3, un utente che Visualizza il gioco in una schermata 16:9 probabilmente avrà tre opzioni per la visualizzazione dell'immagine, nessuna delle quali è particolarmente soddisfacente:

<dl> <dt>

<span id="Stretch"></span><span id="stretch"></span><span id="STRETCH"></span>Stretch
</dt> <dd>

Il buffer di frame 4:3 viene esteso per coprire perfettamente la risoluzione nativa del 16:9 dello schermo, causando un più ampio rispetto a quello desiderato per gli oggetti della scena. Alcuni televisori offrono modalità di estensione aggiuntive che tentano di mantenere le proporzioni in prossimità del centro dello schermo e di aumentare gradualmente l'estensione ai lati dell'immagine.

</dd> <dt>

<span id="Center"></span><span id="center"></span><span id="CENTER"></span>Center
</dt> <dd>

Il buffer del frame di 4:3 viene visualizzato non distorto al centro dello schermo, con barre dei colori solide che riempiono i pixel rimanenti sui lati.

</dd> <dt>

<span id="Zoom"></span><span id="zoom"></span><span id="ZOOM"></span>Zoom
</dt> <dd>

Il buffer di frame 4:3 viene ritagliato in un'area 16:9, che quindi compila la risoluzione dello schermo nativa senza distorsione; Si noti che i pixel sopra e sotto il rettangolo di ritaglio vengono rimossi completamente, ovvero aree comuni per gli elementi dell'interfaccia utente di un gioco.

</dd> </dl>

Un approccio migliore consiste nell'aggiungere il supporto per la visualizzazione a schermo intero per il gioco. La modifica più importante consiste nell'impostare la trasformazione di proiezione della fotocamera del gioco in modo da usare le proporzioni di 16:9, che evita la distorsione dell'estensione. Anche se si lascia il buffer nascosto a una risoluzione 4:3, il cambio della trasformazione proiezione per l'uso di 16:9 migliora notevolmente la precisione percepita dell'immagine di cui è stato eseguito il rendering. Naturalmente, l'immagine finale viene filtrata per ridimensionare la risoluzione del buffer 4:3 per soddisfare la risoluzione dello schermo nativo 16:9, ma si tratta di un artefatto meno evidente rispetto alla distorsione dell'estensione causata da una mancata corrispondenza delle proporzioni.

Il costo del rendering della scena tramite la fotocamera 16:9 può essere superiore a una fotocamera 4:3 (anche con risoluzioni identiche), perché più oggetti scena saranno visibili nella vista più ampia tronco. È anche necessario conoscere il modo in cui l'area visualizzabile ingrandita può influenzare il gameplay; ad esempio, una videocamera di gioco con un rapporto 16:9 potrebbe rivelare più del mondo del gioco rispetto a una fotocamera 4:3.

Per ottenere risultati ottimali in una visualizzazione 16:9, è necessario eseguire il rendering in un buffer di 16:9, ma questo richiederà ovviamente il riempimento di più pixel. La differenza tra 640 × 480 e 720 × 480 è circa 38.400 pixel, un guadagno del 12,5%. Se è possibile permettersi il costo di riempire questa area di dimensioni maggiori, è consigliabile farlo.

## <a name="title-safe-region"></a>Area Title-Safe

Il buffer del frame immagine potrebbe essere parzialmente nascosto dall'utente, perché alcuni pixel intorno al bordo sono spesso coperti dalla lunetta anteriore dello schermo. Per assicurarsi che gli elementi dell'interfaccia utente critici siano visibili in un'ampia gamma di hardware di visualizzazione, è necessario osservare i requisiti di area indipendente dal titolo per la modalità di visualizzazione di destinazione. Per le modalità non HDTV, l'area indipendente dal titolo è il 85% interno del buffer dei frame e per le modalità HDTV, l'area indipendente dal titolo è il 90% interno. Pertanto, per ottenere la massima compatibilità con l'hardware di visualizzazione corrente e futuro, è necessario tenere tutti gli elementi critici dell'interfaccia utente e gli indicatori di visualizzazione delle intestazioni all'interno del 85% interno del buffer del frame.

## <a name="ntsc-suggestions"></a>Suggerimenti per NTSC

Poiché NTSC è lo standard video più comune nel Stati Uniti per l'hardware di visualizzazione del consumer, è importante conoscere alcune delle linee guida che è necessario seguire per l'immagine di output.

### <a name="clamp-the-rgb-color-component-values-between-16-and-235"></a>Blocca i valori del componente colore RGB tra 16 e 235

I colori non compresi nell'intervallo di 16-235 possono essere inviati a una TV NTSC, ma è probabile che questi valori non compresi nell'intervallo verranno interpretati come dati audio. Questo è spesso detto *Buzz audio* e risulta più evidente se il contenuto è stato presentato su uno sfondo bianco a tinta unita. È possibile implementare facilmente la pressione del colore di output all'interno di una pixel shader.

### <a name="avoid-similar-colors-that-might-appear-identical"></a>Evitare colori simili che potrebbero apparire identici

La gamma di colori NTSC non offre la stessa tavolozza di un monitor del computer tipico, quindi evitare di usare colori simili quando il gioco richiede che il lettore riconosca la differenza.

### <a name="avoid-sharp-differences-in-contrast"></a>Evitare differenze acute al contrasto

Anche se questa linea guida non è sempre praticabile, è possibile mitigare alcuni disturbi relativi al sanguinamento dei colori nelle visualizzazioni NTSC (anche noto come *Chroma Crawl*) selezionando i colori appropriati per gli elementi di primo piano e di sfondo dell'interfaccia utente. il testo bianco su sfondo colorato fornirà probabilmente risultati migliori rispetto ai colori a contrasto.

## <a name="conclusion"></a>Conclusione

In questo articolo è stata illustrata l'esperienza a 10 piedi dal punto di vista di uno sviluppatore di giochi Windows, ma non si tratta di un sondaggio completo; è consigliabile approfondire questi argomenti se si sviluppa un titolo di gioco Windows (anche se non è destinato all'uso con Windows Media Center). Il vero test consiste nel provare il gioco in un'ampia gamma di visualizzazioni video per assicurarsi che il gioco offra un'esperienza piacevole per ognuno di essi. In base alla durata tipica di un gioco basato su Windows e alla crescita prevista per l'uso di Windows Media Center, è quasi garantito che un gioco rilasciato oggi faccia parte dell'esperienza di 10 piedi di un utente, indipendentemente dal fatto che i clienti possano giocare dalla comodità dei divani o che siano costretti a sedersi al banco.

 

 