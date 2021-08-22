---
title: Panoramica degli sviluppatori
description: Panoramica degli sviluppatori
ms.assetid: 72a330b4-5957-4159-b5e8-0c9a4491b589
keywords:
- Windows Media Player plug-in, visualizzazioni
- plug-in, visualizzazioni
- visualizzazioni,panoramica per sviluppatori
- visualizzazioni personalizzate, panoramica per sviluppatori
- visualizzazioni,controlli COM
- visualizzazioni personalizzate,controlli COM
- visualizzazioni,input audio
- visualizzazioni personalizzate,input audio
- visualizzazioni, output grafico
- visualizzazioni personalizzate, output grafico
- visualizzazioni, strumenti di disegno
- visualizzazioni personalizzate, strumenti di disegno
- visualizzazioni, linguaggio di programmazione
- visualizzazioni personalizzate, linguaggio di programmazione
- visualizzazioni, Visual C++
- visualizzazioni personalizzate, Visual C++
- visualizzazioni, creazione guidata plug-in
- visualizzazioni personalizzate, creazione guidata plug-in
- Creazione guidata plug-in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d20988a8cf1b7923699ec9cee7990b99840b8acdf9371e74da5940ddb8fc8d4e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118579413"
---
# <a name="developer-overview"></a>Panoramica degli sviluppatori

Dal punto di vista dello sviluppatore, le visualizzazioni sono programmi software che prendono i dati audio forniti da Windows Media Player e convertono i dati in grafica che piacerà all'occhio dell'utente. Gli argomenti principali che uno sviluppatore deve comprendere per creare una nuova visualizzazione sono i seguenti:

## <a name="visualization-packaging"></a>Creazione di pacchetti di visualizzazioni

Le visualizzazioni sono controlli COM che Windows Media Player per trasformare le forme d'onda audio in grafica animata in Microsoft Windows. I controlli COM vengono in pacchetto come librerie a collegamento dinamico (DLL) di Microsoft Windows e devono essere registrati nel registro Windows dati. Quando Windows Media Player, le visualizzazioni personalizzate registrate vengono caricate e visualizzate in base alle istruzioni dell'interfaccia Windows Media Player in uso.

## <a name="audio-input"></a>Audio Input

Windows Media Player codice con snapshot della frequenza audio e dei dati della forma d'onda a intervalli temporati misurati in frazioni di secondo. L'intervallo di snapshot è determinato internamente dal Windows Media Player.

## <a name="graphical-output"></a>Output grafico

L'output grafico della visualizzazione è un contesto di Windows Microsoft. Si tratta di una superficie Windows di disegno standard su cui è possibile disegnare ogni volta che viene fornito uno snapshot audio. Tutto il background Windows tecnologia è curato per l'utente. È sufficiente disegnare sul contesto di dispositivo con i dati audio forniti.

## <a name="drawing-tools"></a>Strumenti di disegno

È possibile disegnare sul contesto di dispositivo con le funzioni standard di Microsoft Windows Graphics Device Interface (GDI), usando penna e pennelli per creare progettazioni che vengono modificate dai dati audio forniti da Windows Media Player. GDI offre un set di strumenti di disegno avanzati in grado di creare molti tipi di effetti visivi.

## <a name="programming-language"></a>Linguaggio di programmazione

Microsoft Visual C++ 6.0 e versioni successive è l'unica lingua supportata per la creazione di visualizzazioni personalizzate.

## <a name="plug-in-wizard"></a>Creazione guidata plug-in

Windows Media Player una procedura guidata COM che è possibile aggiungere a Visual C++ che genererà il codice sottostante necessario per la visualizzazione. Non solo vengono forniti tutti i file di origine, ma viene generata un'interfaccia di esempio per semplificare il test della visualizzazione. Il codice generato crea una visualizzazione simile a Bars, con due set di impostazioni. È quindi possibile modificare il codice per creare una visualizzazione personale. Viene generato anche un file del Registro di sistema per registrare la visualizzazione in modo Windows Media Player possibile caricarla.

L'argomento seguente descrive il modo in cui il codice di visualizzazione elabora i dati audio:

-   [Flow di controllo](flow-of-control.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni sulle visualizzazioni personalizzate**](about-custom-visualizations.md)
</dt> </dl>

 

 




