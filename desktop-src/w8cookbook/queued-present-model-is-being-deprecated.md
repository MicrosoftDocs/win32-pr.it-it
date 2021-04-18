---
title: Il modello presente in coda verrà deprecato
description: Il modello presente in coda verrà deprecato
ms.assetid: 271CD4F7-0992-47DB-AF5A-B77570EF681A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5713009cd5cd3a575d0d634f81fce7a289d1c1c
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/10/2020
ms.locfileid: "106300634"
---
# <a name="queued-present-model-is-being-deprecated"></a>Il modello presente in coda verrà deprecato

## <a name="platforms"></a>Piattaforme

**Client** -dopo Windows 8  
**Server** : dopo Windows Server 2012  


## <a name="description"></a>Descrizione

Nella versione di Windows dopo Windows 8, queste API restituiranno E \_ NOTIMPL:

-   DwmSetPresentParameters
-   DwmSetDxFrameDuration
-   DwmModifyPreviousDxFrameDuration

Inoltre, questa API accetterà solo il valore NULL per il parametro HWND:

-   DwmGetCompositionTimingInfo

Si interromperà il supporto di DwmGetCompositionTimingInfo con HWND! = NULL e si rimuove la funzionalità associata. Se viene specificato un valore non NULL per HWND, l'API restituirà E \_ INVALIDARG.

Viene anche sconsigliato l'uso dell'API DwmGetCompositionTimingInfo e si suggerisce agli sviluppatori di passare al modello DXGI Flip e alle API di DX present associate.

## <a name="manifestation"></a>Manifestazione

Le applicazioni che utilizzano il modello presente in coda non funzioneranno correttamente. La manifestazione esatta dipende dall'applicazione specifica, ma può variare da un intervallo di presentazione non corretto all'uscita dall'applicazione in modo imprevisto. In pratica, non ci si aspetta di vedere molte applicazioni di questo tipo. Questo modello è stato usato da Vista Media Player, che non verrà usato in Windows 8 (e possibilmente con il lettore Zune precedente). Al momento non sono disponibili informazioni su altre applicazioni che utilizzano effettivamente questo modello.

## <a name="solution"></a>Soluzione

Gli sviluppatori devono usare la modalità DXGI Flip Presentation invece della presente in coda (disponibile nel runtime di DX9 da Windows 7 e nei runtime DX10 e DX11 in Windows 8).

## <a name="tests"></a>Test

Eseguire test generali per assicurarsi che i componenti Windows della posta in arrivo e i prodotti principali continuino a funzionare alla prossima versione di Windows.

 

 




