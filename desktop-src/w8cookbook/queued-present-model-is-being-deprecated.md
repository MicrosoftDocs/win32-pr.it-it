---
title: Il modello presente in coda è deprecato
description: Il modello presente in coda è deprecato
ms.assetid: 271CD4F7-0992-47DB-AF5A-B77570EF681A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7cb1d4d07a824c2c6f9d0136259aec98b89c53e1320ceb6402241f881e312fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118211346"
---
# <a name="queued-present-model-is-being-deprecated"></a>Il modello presente in coda è deprecato

## <a name="platforms"></a>Piattaforme

**Client:** dopo Windows 8  
**Server** : dopo Windows Server 2012  


## <a name="description"></a>Descrizione

Nella versione Windows dopo Windows 8, queste API restituiranno E \_ NOTIMPL:

-   DwmSetPresentParameters
-   DwmSetDxFrameDuration
-   DwmModifyPreviousDxFrameDuration

Inoltre, questa API accetterà solo il valore NULL per il parametro hwnd:

-   DwmGetCompositionTimingInfo

Il supporto di DwmGetCompositionTimingInfo con hwnd != NULL verrà interrotta e la funzionalità associata verrà rimosso. Se viene specificato un valore diverso da NULL per hwnd, questa API restituirà E \_ INVALIDARG.

È anche sconsigliato l'uso dell'API DwmGetCompositionTimingInfo e si consiglia agli sviluppatori di passare al modello flip DXGI e all'API delle statistiche DX present.

## <a name="manifestation"></a>Manifestazione

Le applicazioni che usano il modello presente in coda non funzioneranno correttamente. La manifestazione esatta dipende dall'applicazione specifica, ma può variare da un intervallo di presentazione non corretto all'uscita imprevista dell'applicazione. In pratica, non si prevede di visualizzare molte (se presenti) applicazioni di questo tipo. Questo modello è stato usato dal lettore multimediale Vista, che non verrà usato Windows 8 (ed eventualmente il lettore Zune precedente). Al momento non sono presenti informazioni su altre applicazioni che usano effettivamente questo modello.

## <a name="solution"></a>Soluzione

Gli sviluppatori devono usare la modalità di presentazione flip DXGI invece della presentazione in coda (disponibile nel runtime DX9 a partire da Windows 7 e nei runtime DX10 e DX11 in Windows 8).

## <a name="tests"></a>Test

Eseguire test generali per assicurarsi che i componenti Windows posta in arrivo e i prodotti principali continuino a funzionare nella versione successiva di Windows.

 

 




