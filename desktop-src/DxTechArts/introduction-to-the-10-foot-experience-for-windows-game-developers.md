---
title: Introduzione all'esperienza di 10 metri per gli sviluppatori di Windows game
description: Questo articolo presenta l'esperienza di 10 metri ed esplora l'elenco di aspetti da considerare per primi su questo nuovo modello di interazione, anche se non si prevede che il gioco sia riprodotto in questo modo.
ms.assetid: 126a0aae-6a7a-8cda-5748-c364e54c304e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 049cbbe839509681f8f8629144511853d2984bbabafbf989611d1ed1db32e686
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963621"
---
# <a name="introduction-to-the-10-foot-experience-for-windows-game-developers"></a>Introduzione all'esperienza di 10 metri per gli sviluppatori di Windows game

Un numero crescente di persone usa i propri personal computer in un modo completamente nuovo. Quando si pensa all'interazione tipica con un computer basato su Windows, probabilmente si prevede di sedersi a una scrivania con un monitor e di usare un mouse e una tastiera (o forse un dispositivo joystick); questa esperienza è nota come esperienza di 2 metri ed è ancora lo scenario più comune per i giochi Windows, ma esiste un'altra tendenza che probabilmente si inizierà a ascoltare di più: l'esperienza di 10 piedi, che descrive l'uso del computer come dispositivo di intrattenimento con output in un TV. Questo articolo presenta l'esperienza di 10 metri ed esplora l'elenco di aspetti da considerare per primi su questo nuovo modello di interazione, anche se non si prevede che il gioco sia riprodotto in questo modo. Una parte dei clienti eseguirà il gioco basato su Windows in un computer che esegue Windows Media Center. È meglio sapere quale sarà l'esperienza prima che i clienti la provino.

-   [Che cos'Windows Media Center?](#what-is-windows-media-center)
-   [L'esperienza di 10 piedi](#the-10-foot-experience)
    -   [Installazione](#installation)
    -   [Input utente](#user-input)
    -   [Schermo](#display)
-   [Proporzioni e widescreen](#aspect-ratio-and-widescreen)
-   [Area Cassaforte titolo](#title-safe-region)
-   [Suggerimenti NTSC](#ntsc-suggestions)
    -   [Clampare i valori del componente colore RGB tra 16 e 235](#clamp-the-rgb-color-component-values-between-16-and-235)
    -   [Evitare colori simili che potrebbero apparire identici](#avoid-similar-colors-that-might-appear-identical)
    -   [Evitare differenze nette al contrasto](#avoid-sharp-differences-in-contrast)
-   [Conclusione](#conclusion)

## <a name="what-is-windows-media-center"></a>Che cos'Windows Media Center?

Windows Media Center può fungere da interfaccia per le funzionalità multimediali del computer host. Il sito Web per questa funzionalità, [Windows Media Center Home,](https://windows.microsoft.com/windows/products/windows-media-center/)offre un'introduzione completa e illustra tutti gli elementi disponibili nella versione più recente. Media Center è incluso in Windows XP Media Center Edition, Windows Vista Home Premium, Windows Vista Ultimate e nella maggior parte delle edizioni di Windows 7.

In passato, l'unico modo per ottenere Windows Media Center era acquistare un PC Media Center da un produttore di sistema di livello 1, ma poiché Windows Media Center è ora incluso in due edizioni di Windows Vista, il marketplace potenziale è ora molto più grande.

## <a name="the-10-foot-experience"></a>L'esperienza di 10 piedi

Windows Media Center è stato progettato in base all'idea che gli utenti potrebbero usare Windows per un'esperienza di intrattenimento in un ambiente di intrattenimento con un ambiente di intrattenimento molto ricco e ne consegue che la maggior parte degli utenti preferisce interagire in modo diverso con Windows Media Center in modo diverso rispetto alle applicazioni computer tradizionali. Per uno, se il cliente usa il computer nel living room per l'intrattenimento, è probabile che il video sia visualizzato su un monitor diverso da un computer convenzionale: TV analogiche, TV digitali ad alta definizione e qualsiasi numero di schermi LCD sono tutti candidati probabili. Questi tipi di display vengono in genere visualizzati da una distanza di circa 10 piedi, quindi l'etichetta *10 piede esperienza*.

L'esperienza di 10 piedi non è limitata agli utenti di Windows Media Center; negli ultimi anni è diventato comune per gli utenti connettere la workstation o il computer notebook al sistema TV e audio. È sempre più comune per i dispositivi di visualizzazione consumer esporre le connessioni RGB o DVI, le porte di output video standard nei computer. Inoltre, le porte S-Video sono una caratteristica tipica delle schede video di fascia alta e offrono un modo semplice per eseguire l'output in un dispositivo di visualizzazione alternativo.

Esistono alcune importanti linee guida di progettazione che devono essere considerate per una piacevole esperienza di 10 piedi: installazione, input dell'utente e visualizzazione.

### <a name="installation"></a>Installazione

Durante l'esperienza media di 2 metri, l'utente si trova a una distanza minima dal computer; se durante l'avvio o il gioco, l'utente deve inserire o cambiare supporto, l'utente può almeno rimanere seduti. L'esperienza media di 10 piedi posiziona il computer dall'altra parte della stanza dall'utente e quindi tutto ciò che richiede all'utente di interagire fisicamente con il computer forza l'utente a alzarsi e attraversare la stanza. Per questo motivo, gli sviluppatori devono evitare di forzare l'utente a modificare i supporti. è consigliabile consentire un'installazione completa dell'applicazione nel disco rigido.

### <a name="user-input"></a>Input utente

Un'altra funzionalità Windows Media Center è il supporto per un controllo remoto standard, che è il dispositivo di input preferito in genere. Anche se il genere del titolo del gioco decide in gran parte se il controllo remoto è adatto per fornire l'input del gioco, è comunque possibile consentire all'utente di sospendere il gioco e accedere ai menu nel gioco usando il controllo remoto. Tuttavia, assicurarsi di consentire anche all'utente di controllare i menu usando il dispositivo di input del gioco primario. Per altre informazioni sulla progettazione e lo sviluppo per Windows Media Center e i relativi dispositivi, vedere [Windows Software Development Kit](/previous-versions/msdn10/bb895967(v=msdn.10)) di Media Center su MSDN.

Evitare qualsiasi interazione fisica tra l'utente e il computer o le relative periferiche. È indesiderabile richiedere all'utente di modificare i controller di input durante il gioco, poiché è probabile che sia vicino solo al dispositivo di input primario.

Microsoft ha creato controller di gamepad comuni da usare con Windows e Xbox 360, ovvero controller Xbox 360 per Windows e controller wireless Xbox 360 per Windows. Assicurarsi che il titolo giochi bene sui controller comuni faciliterà alcune difficoltà associate al test del gioco su potenziali dispositivi di input.

### <a name="display"></a>Visualizza

L'ampia gamma di potenziali dispositivi di visualizzazione consiglia la visualizzazione complessa e ogni tipo di dispositivo presenta particolari avvertenze. Alcuni dei problemi relativi a tecnologie di visualizzazione specifiche vengono introdotti più avanti in questo documento. Indipendentemente dal dispositivo di output video, è importante che i tipi di carattere e la grafica dell'interfaccia utente siano sufficientemente grandi per una leggibilità comoda a una distanza di 10 piedi. Si noti anche che i tipi di carattere antialias in genere offrono una migliore leggibilità.

È inoltre consigliabile evitare linee orizzontali ed elementi statici dell'interfaccia utente con spessore o dettaglio a pixel singolo. I programmi televisivi meno recenti potrebbero non visualizzare dettagli dettagliati e, anche nei dispositivi di visualizzazione più recenti, il contenuto sfarfallierà durante l'esecuzione in modalità interlacciata, poiché una singola riga di pixel è visibile solo la metà del tempo. In sostituzione di piccoli dettagli, si noti che una linea grigia di 2 pixel appare più sottile rispetto a una linea bianca di 2 pixel. Si tratta essenzialmente della sfocatura di una linea bianca di 1 pixel.

## <a name="aspect-ratio-and-widescreen"></a>Proporzioni e widescreen

Proporzioni descrive la proporzione di larghezza e altezza dello schermo. I monitor TV standard e del computer hanno proporzioni di 4:3, vale a dire che per ogni 4 pixel in esecuzione lungo la larghezza del buffer dei fotogrammi, sono presenti 3 pixel lungo l'altezza (talvolta rappresentati anche come 1,33).

Con l'avvento di HDTV, un rapporto di aspetto di 16:9, noto anche come schermo wide, è diventato lo standard per il futuro della TV e insieme alla TV a definizione avanzata (EDTV), è probabile che si verifichino tre modalità di visualizzazione:

<dl> <dt>

<span id="480p_EDTV"></span><span id="480p_edtv"></span><span id="480P_EDTV"></span>480p EDTV
</dt> <dd>

480 righe di analisi presentate in modo progressivo. Questa modalità può 4:3 (con risoluzione del buffer dei frame di 640×480) o 16:9 (720×480).

</dd> <dt>

<span id="720p_HDTV"></span><span id="720p_hdtv"></span><span id="720P_HDTV"></span>HDTV da 720p
</dt> <dd>

720 righe di analisi presentate in modo progressivo. Questa modalità è sempre 16:9 (1280×720).

</dd> <dt>

<span id="1080i_HDTV"></span><span id="1080i_hdtv"></span><span id="1080I_HDTV"></span>1080i HDTV
</dt> <dd>

1080 righe di analisi presentate interlacciate. Questa modalità è sempre 16:9 (1920×1080 o 1920×540 se si esegue il rendering dei campi interlacciati separatamente).

</dd> </dl>

Se il gioco è hard-coded per funzionare in proporzioni 4:3, un utente che visualizza il gioco su uno schermo 16:9 probabilmente ha tre opzioni per la visualizzazione dell'immagine, nessuna delle quali è particolarmente soddisfacente:

<dl> <dt>

<span id="Stretch"></span><span id="stretch"></span><span id="STRETCH"></span>Tratto
</dt> <dd>

Il buffer di fotogrammi 4:3 viene allungato in modo da coprire perfettamente la risoluzione nativa 16:9 dello schermo, in modo che gli oggetti della scena appaiano più larghi del desiderato. Alcuni TV offrono modalità di estensione aggiuntive che tentano di mantenere le proporzioni vicino al centro dello schermo e di aumentare gradualmente l'estensione ai lati dell'immagine.

</dd> <dt>

<span id="Center"></span><span id="center"></span><span id="CENTER"></span>Centro
</dt> <dd>

Il buffer dei fotogrammi 4:3 viene visualizzato senza distorti al centro dello schermo, con barre di colore a tinta unita che riempie i pixel rimanenti sui lati.

</dd> <dt>

<span id="Zoom"></span><span id="zoom"></span><span id="ZOOM"></span>Zoom
</dt> <dd>

Il buffer di frame 4:3 viene ritagliato in un'area 16:9, che quindi riempie la risoluzione nativa dello schermo senza distorsione; Si noti che i pixel sopra e sotto il rettangolo di ritaglio vengono completamente eliminati, ovvero aree comuni per gli elementi dell'interfaccia utente di un gioco.

</dd> </dl>

Un approccio migliore consiste nell'aggiungere il supporto per la visualizzazione su schermo wide al gioco. La modifica più importante è impostare la trasformazione di proiezione della fotocamera del gioco in modo da usare proporzioni 16:9, evitando così la distorsione dell'estensione. Anche se si lascia il buffer nascosto con una risoluzione 4:3, il passaggio della trasformazione di proiezione all'uso di 16:9 migliora notevolmente l'accuratezza percepita dell'immagine sottoposta a rendering. Naturalmente l'immagine finale viene filtrata per ridimensionare la risoluzione del buffer nascosto 4:3 per soddisfare la risoluzione dello schermo nativa 16:9, ma si tratta di un artefatto meno evidente rispetto alla distorsione di estensione causata da una mancata corrispondenza delle proporzioni.

Il costo del rendering della scena tramite la fotocamera 16:9 può essere superiore a una fotocamera 4:3 (anche a risoluzioni identiche), perché più oggetti della scena saranno visibili nel frustum di visualizzazione più ampio. È anche necessario tenere presente in che modo l'area visualizzabile ingrandita può influire sul gioco; Ad esempio, una fotocamera di gioco con un rapporto di 16:9 potrebbe rivelare più del mondo del gioco rispetto a una fotocamera 4:3.

Per ottenere risultati ottimali su uno schermo 16:9, è necessario eseguire il rendering in un buffer nascosto 16:9, ma questo richiede ovviamente il riempimento di più pixel. La differenza tra 640×480 e 720×480 è di quasi 38.400 pixel, un guadagno del 12,5%. Se è possibile sostenere il costo di riempimento di questa area più ampia, è consigliabile farlo.

## <a name="title-safe-region"></a>Title-Safe'area

Il buffer del frame dell'immagine potrebbe essere parzialmente nascosto all'utente, perché alcuni pixel intorno al bordo sono spesso coperti dalla cornice anteriore dello schermo. Per assicurarsi che gli elementi critici dell'interfaccia utente siano visibili in un'ampia gamma di hardware di visualizzazione, è necessario osservare i requisiti dell'area di sicurezza del titolo per la modalità di visualizzazione di destinazione. Per le modalità non HDTV, l'area title-safe è l'85% interno del buffer dei frame e per le modalità HDTV, l'area sicura per il titolo è il 90% interno. Pertanto, per la massima compatibilità tra l'hardware di visualizzazione corrente e futuro, è consigliabile mantenere tutti gli elementi critici dell'interfaccia utente e gli indicatori di visualizzazione heads-up all'interno dell'85% del buffer dei frame.

## <a name="ntsc-suggestions"></a>Suggerimenti NTSC

Poiché NTSC è lo standard video più comune nel Stati Uniti per l'hardware di visualizzazione consumer, è importante conoscere alcune delle linee guida da seguire per l'immagine di output.

### <a name="clamp-the-rgb-color-component-values-between-16-and-235"></a>Selezionare i valori del componente colore RGB compresi tra 16 e 235

I colori non compreso nell'intervallo 16-235 possono certamente essere inviati a un TV NTSC, ma è probabile che questi valori non in intervallo verranno interpretati come dati audio. Questo è spesso chiamato *ronzio audio* e sarebbe più evidente se il contenuto fosse presentato su uno sfondo bianco a tinta unita. È possibile implementare facilmente la chiusura dei colori di output all'interno di un pixel shader.

### <a name="avoid-similar-colors-that-might-appear-identical"></a>Evitare colori simili che potrebbero apparire identici

La gamma di colori NTSC non offre la stessa tavolozza di un tipico monitor del computer, quindi evitare di usare colori simili ovunque il gioco richieda che il giocatore riconosca la differenza.

### <a name="avoid-sharp-differences-in-contrast"></a>Evitare differenze nette nel contrasto

Anche se questa linea guida non è sempre pratica da seguire, è possibile attenuare alcuni dei problemi di disamina dei colori sugli schermi NTSC (noti anche come *chroma crawl*) selezionando i colori adatti per gli elementi di primo piano e di sfondo dell'interfaccia utente. il testo bianco su uno sfondo colorato probabilmente offrirà risultati migliori rispetto ai colori a contrasto.

## <a name="conclusion"></a>Conclusione

Questo articolo ha offerto uno sguardo all'esperienza di 10 metri dal punto di vista di uno sviluppatore di giochi Windows, ma non è affatto un sondaggio completo; È consigliabile approfondire questi argomenti se si sta sviluppando un titolo di gioco Windows (anche se non è destinato all'uso con Windows Media Center). Il vero test è provare il gioco su un'ampia gamma di schermi video per garantire che il gioco offra un'esperienza piacevole in ognuno di essi. In base all'intervallo di vita tipico di un gioco basato su Windows e alla crescita stimata nell'uso di Windows Media Center, è quasi garantito che un gioco rilasciato oggi sia parte dell'esperienza di un utente, indipendentemente dal fatto che i clienti possano provare il gioco dal comfort dei divano o che siano obbligati a sedersi sulle scrivanie.

 

 