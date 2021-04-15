---
title: Determinazione e modifica della posizione corrente
description: Determinazione e modifica della posizione corrente
ms.assetid: 20f78dcd-3259-43c2-8da3-8cfc299252e6
keywords:
- MCIWndGetStart (macro)
- MCIWndGetEnd (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84a8e7022bdfcede526a730014a07deaf22fe66d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471398"
---
# <a name="determining-and-changing-the-current-position"></a>Determinazione e modifica della posizione corrente

Quando un file o un dispositivo è associato a una finestra MCIWnd, la posizione di riproduzione viene inizialmente impostata all'inizio del contenuto, indipendentemente dal tipo di supporto. Durante la riproduzione, la posizione di riproduzione viene spostata in modo lineare tramite il contenuto e, se la riproduzione non viene interrotta, raggiunge la fine del contenuto. Se si verifica un'interruzione, la posizione di riproduzione corrente è la posizione in cui la riproduzione è stata interrotta o sospesa.

È possibile recuperare i percorsi per l'inizio e la fine del contenuto usando le macro [**MCIWndGetStart**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstart) e [**MCIWndGetEnd**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetend) . È possibile determinare la lunghezza del contenuto sottraendo il valore restituito da **MCIWndGetStart** dal valore restituito da **MCIWndGetEnd** o usando la macro [**MCIWndGetLength**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetlength) . È possibile recuperare la posizione di riproduzione corrente usando la macro [**MCIWndGetPosition**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetposition) oppure è possibile recuperare la posizione di riproduzione come stringa con terminazione null usando la macro [**MCIWndGetPositionString**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpositionstring) .

Per modificare la posizione di riproduzione corrente, usare le macro [**MCIWndHome**](/windows/desktop/api/Vfw/nf-vfw-mciwndhome), [**MCIWndEnd**](/windows/desktop/api/Vfw/nf-vfw-mciwndend)e [**MCIWndSeek**](/windows/desktop/api/Vfw/nf-vfw-mciwndseek) . È possibile spostare la posizione di riproduzione all'inizio del contenuto utilizzando **MCIWndHome** o alla fine del contenuto utilizzando **MCIWndEnd**. Usare **MCIWndSeek** per spostare la posizione di riproduzione in qualsiasi posizione nel contenuto.

È anche possibile esaminare il contenuto usando la macro [**MCIWndStep**](/windows/desktop/api/Vfw/nf-vfw-mciwndstep) . A partire dalla posizione di riproduzione corrente, questa macro sposta la posizione di riproduzione avanti o indietro in base a un incremento specificato.

> [!Note]  
> Le unità usate per specificare la posizione variano tra i diversi tipi di supporti e dispositivi. Ad esempio, la posizione di riproduzione per i file AVI usati dal dispositivo MCIAVI viene misurata in frame; la posizione di riproduzione per i file audio CD, waveform e audio e MIDI è misurata in millisecondi.

 

I dispositivi per altri tipi di supporti e dispositivi di terze parti potrebbero usare altre unità. Per informazioni su come determinare queste unità, vedere [miglioramenti della riproduzione](playback-enhancements.md).

 

 




