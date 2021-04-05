---
title: Implementazione di rendering
description: Implementazione di rendering
ms.assetid: 9b3a64f6-6803-457c-8e63-e8a799089e18
keywords:
- Visualizzazioni, eventi temporizzati
- Visualizzazioni personalizzate, eventi temporizzati
- Visualizzazioni, funzione render
- Visualizzazioni personalizzate, funzione render
- Visualizzazioni, funzione RenderWindow
- Visualizzazioni personalizzate, funzione RenderWindow
- Funzione di rendering, parametri
- RenderWindow (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99db0a96a07c361d18de579fb0235befa11838c8
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104046313"
---
# <a name="implementing-render"></a>Implementazione di rendering

Il modo più semplice per considerare la programmazione della visualizzazione è che si sta creando un gestore per un evento temporizzato. A intervalli specifici, Windows Media Player acquisisce uno snapshot dei dati audio che sta eseguendo e fornisce i dati dello snapshot alla visualizzazione attualmente caricata. Questa operazione è simile alla programmazione basata su eventi ed è parte del modello di programmazione di Microsoft Windows. Si scrive il codice e si attende che venga chiamato da un particolare evento.

Se il codice è un'implementazione della funzione [IWMPEffects:: Render](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-render) per il rendering in modalità senza finestra, riceve i parametri seguenti:

*TimedLevel*

Si tratta di una struttura che definisce i dati audio che verranno analizzati dal codice. La struttura è costituita da due matrici. La prima matrice è basata sulle informazioni sulla frequenza e contiene uno snapshot dello spettro audio diviso in 1024 porzioni. Ogni cella della matrice contiene un valore compreso tra 0 e 255. La prima cella inizia a 20 Hz e l'ultimo a 22050 Hz. La matrice è bidimensionale per rappresentare audio stereo. La seconda matrice è basata sulle informazioni sulla forma d'onda e corrisponde alla potenza audio, in cui l'onda è più forte, maggiore è il valore. La matrice di forme d'onda è uno snapshot granulare delle ultime 1024 sezioni di alimentazione audio acquisite a intervalli di tempo molto piccoli. Questa matrice è anche di due dimensioni per rappresentare audio stereo.

*HDC*

Si tratta di un handle Microsoft Windows per un contesto di dispositivo. In questo modo è possibile identificare la superficie di disegno in Windows. Non è necessario crearlo, ma è sufficiente utilizzarlo per chiamate di funzioni di disegno specifiche.

*RECT*

Si tratta di un rettangolo di Microsoft Windows che definisce la dimensione di una superficie di disegno. Si tratta di un rettangolo semplice con quattro proprietà: **Left**, **right**, **Top** e **Bottom**. I valori effettivi vengono forniti da Windows Media Player in modo che sia possibile determinare il modo in cui l'utente o lo sviluppatore di Skin ha ridimensionato la finestra da cui verrà disegnato. Determina anche la posizione sull'HDC su cui deve essere eseguito il rendering dell'effetto.

Se il codice è un'implementazione della funzione **IWMPEffects2:: RenderWindowed** per il rendering in una finestra, riceve i parametri seguenti:

*TimedLevel*

Si tratta delle stesse informazioni ricevute dalla funzione **Render** .

*fRequiredRender*

Il parametro *fRequiredRender* informa che la visualizzazione deve essere ridisegnata, ad esempio quando viene trascinata un'altra finestra. Quando questo valore è false, è possibile ignorare il codice di rendering se l'elemento multimediale corrente viene arrestato o sospeso. Ciò consente di evitare l'utilizzo inutilmente di cicli della CPU.

Il plug-in di esempio generato dalla procedura guidata plug-in non fornisce un'implementazione personalizzata per **RenderWindowed**. Al contrario, il codice del plug-in di esempio recupera il contesto di dispositivo dalla finestra padre fornita da Windows Media Player in [IWMPEffects2:: create](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects2-create), quindi recupera le dimensioni della finestra padre come struttura Rect, quindi chiama per **eseguire il rendering** usando il contesto di dispositivo, il recto e il puntatore a livello temporizzato da **RenderWindowed**.

Nelle sezioni seguenti vengono fornite ulteriori informazioni sull'implementazione di **Render**:

-   [Utilizzo di livelli temporizzati](using-timed-levels.md)
-   [Uso dei contesti di dispositivo](using-device-contexts.md)
-   [Uso di rettangoli](using-rectangles.md)
-   [Esempio di codice di rendering](sample-render-code.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Implementazione del codice**](implementing-your-code.md)
</dt> </dl>

 

 




