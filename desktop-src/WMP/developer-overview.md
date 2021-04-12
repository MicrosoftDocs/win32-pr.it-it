---
title: Panoramica degli sviluppatori
description: Panoramica degli sviluppatori
ms.assetid: 72a330b4-5957-4159-b5e8-0c9a4491b589
keywords:
- Plug-in di Windows Media Player, visualizzazioni
- plug-in, visualizzazioni
- Visualizzazioni, panoramica degli sviluppatori
- Visualizzazioni personalizzate, panoramica degli sviluppatori
- Visualizzazioni, controlli COM
- Visualizzazioni personalizzate, controlli COM
- Visualizzazioni, input audio
- Visualizzazioni personalizzate, input audio
- Visualizzazioni, output grafico
- Visualizzazioni personalizzate, output grafico
- Visualizzazioni, strumenti di disegno
- Visualizzazioni personalizzate, strumenti di disegno
- Visualizzazioni, linguaggio di programmazione
- Visualizzazioni personalizzate, linguaggio di programmazione
- Visualizzazioni, Visual C++
- Visualizzazioni personalizzate, Visual C++
- Visualizzazioni, creazione guidata plug-in
- Visualizzazioni personalizzate, creazione guidata plug-in
- procedura guidata plug-in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36ec8632bd5611e081a4a17d1b0390dc99a09703
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331116"
---
# <a name="developer-overview"></a>Panoramica degli sviluppatori

Dal punto di vista dello sviluppatore, le visualizzazioni sono programmi software che accettano i dati audio forniti da Windows Media Player e convertono i dati in un grafico che consente di osservare l'utente. Gli argomenti principali che uno sviluppatore deve conoscere per creare una nuova visualizzazione sono i seguenti:

## <a name="visualization-packaging"></a>Creazione di pacchetti di visualizzazione

Le visualizzazioni sono controlli COM usati da Windows Media Player per trasformare le forme d'onda audio in grafica animata in Microsoft Windows. I controlli COM vengono inclusi in un pacchetto come librerie di collegamento dinamico (dll) di Microsoft Windows e devono essere registrati nel registro di sistema di Windows. Quando si esegue Windows Media Player, le visualizzazioni personalizzate registrate vengono caricate e visualizzate in base alle istruzioni dell'interfaccia utilizzata da Windows Media Player.

## <a name="audio-input"></a>Input audio

Windows Media Player fornisce al codice snapshot di frequenza audio e dati di forma d'onda a intervalli temporizzati misurati in frazioni di secondo. L'intervallo di snapshot è determinato internamente dal Media Player di Windows.

## <a name="graphical-output"></a>Output grafico

L'output grafico della visualizzazione è un contesto di dispositivo Microsoft Windows. Si tratta di una superficie di disegno standard di Windows che è possibile disegnare ogni volta che viene fornito uno snapshot audio. Tutte le tecnologie Windows in background vengono gestite automaticamente. È sufficiente eseguire il progetto nel contesto di dispositivo con i dati audio forniti.

## <a name="drawing-tools"></a>Strumenti di disegno

È possibile creare il contesto di dispositivo con funzioni standard di Microsoft Windows Graphics Device Interface (GDI), usando penne e pennelli per creare progettazioni modificate dai dati audio forniti da Windows Media Player. GDI offre un set completo di strumenti di disegno che consentono di creare molti tipi di effetti visivi.

## <a name="programming-language"></a>Linguaggio di programmazione

Microsoft Visual C++ 6,0 e versioni successive è l'unico linguaggio supportato per la creazione di visualizzazioni personalizzate.

## <a name="plug-in-wizard"></a>Procedura guidata plug-in

Windows Media Player fornisce una procedura guidata COM che è possibile aggiungere ai Visual C++ che genereranno il codice sottostante necessario per la visualizzazione. Non solo sono disponibili tutti i file di origine, ma viene generata un'interfaccia di esempio che semplifica il test della visualizzazione. Il codice generato crea una visualizzazione simile a barre, con due set di impostazioni. È quindi possibile modificare il codice per creare una visualizzazione personalizzata. Viene inoltre generato un file del registro di sistema per registrare la visualizzazione in modo che Windows Media Player possa caricarla.

Nell'argomento seguente viene descritto il modo in cui il codice di visualizzazione elabora i dati audio:

-   [Flusso di controllo](flow-of-control.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni sulle visualizzazioni personalizzate**](about-custom-visualizations.md)
</dt> </dl>

 

 




