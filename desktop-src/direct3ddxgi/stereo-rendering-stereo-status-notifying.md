---
description: Le app non possono eseguire il rendering in stereo a meno che il sistema operativo non indichi che abilita il comportamento di visualizzazione 3D stereoscopica. Le app determinano se eseguire il rendering in 3D stereoscopico in modo diverso a seconda che siano a finestra o a schermo intero.
ms.assetid: FB8AC57E-38DD-47B5-8666-1F4B73488F8B
title: Rendering in stereo e notifica dello stato dello stereo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f17f324a884c5784c98a8f5c21ef9c9dac7b048fc72ae7ed0ea1a75e61e2551
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987011"
---
# <a name="rendering-in-stereo-and-notifying-about-stereo-status"></a>Rendering in stereo e notifica dello stato dello stereo

Le app non possono eseguire il rendering in stereo a meno che il sistema operativo non indichi che abilita il comportamento di visualizzazione 3D stereoscopica. Le app determinano se eseguire il rendering in 3D stereoscopico in modo diverso a seconda che siano a finestra o a schermo intero.

Un'app con finestra chiama il [**metodo IDXGIFactory2::IsWindowedStereoEnabled**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-iswindowedstereoenabled) per determinare se eseguire il rendering in stereo. Un'app a schermo intero chiama il metodo [**IDXGIOutput1::GetDisplayModeList1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutput1-getdisplaymodelist1) e quindi determina se una delle modalità di visualizzazione restituite supporta il rendering in stereo. Il **metodo GetDisplayModeList1** non enumera le modalità stereo a meno che non si specifica il flag [**STEREO DXGI \_ ENUM MODES \_ \_ NEL**](dxgi-enum-modes.md) *parametro Flags.* Un'app con finestra o a schermo intero che supporta stereo determina prima di tutto di eseguire il rendering in stereo in base a una chiamata al metodo **IDXGIFactory2::IsWindowedStereoEnabled** o **IDXGIOutput1::GetDisplayModeList1** e quindi esegue la registrazione per la notifica delle modifiche dello stato stereo. Poiché l'app non può basarsi sulla notifica per indicare lo stato corrente del comportamento di visualizzazione 3D stereoscopica, quando riceve un evento di notifica o un messaggio di finestra, deve chiamare di nuovo **IDXGIFactory2::IsWindowedStereoEnabled** o **IDXGIOutput1::GetDisplayModeList1** per determinare lo stato corrente del comportamento di visualizzazione 3D stereoscopica del sistema operativo.

Se si vuole eseguire il rendering in stereo, è necessario registrarsi per le notifiche stereo per sapere quando l'utente disattiva o attiva il comportamento stereo. Un'app può registrarsi per ricevere una notifica sulle modifiche dello stato 3D stereoscopico tramite un messaggio a una finestra o tramite la segnalazione di eventi. Per registrarsi per ricevere messaggi di notifica in una finestra sulle modifiche dello stato stereo, un'app chiama il [**metodo IDXGIFactory2::RegisterStereoStatusWindow.**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-registerstereostatuswindow) Per registrarsi per ricevere la notifica delle modifiche dello stato stereo tramite la segnalazione di eventi, un'app chiama il [**metodo IDXGIFactory2::RegisterStereoStatusEvent.**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-registerstereostatusevent) Entrambi i metodi restituiscono un puntatore a un valore di chiave che l'app può usare per annullare la registrazione della notifica. Per annullare la registrazione della notifica, l'app passa questo valore di chiave al [**metodo IDXGIFactory2::UnregisterStereoStatus.**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-unregisterstereostatus)

Lo stato stereo può contenere gli elementi seguenti:

-   Configurazione utente.

    Windows gli utenti possono abilitare o disabilitare la visualizzazione stereo con l'opzione abilita 3 Pannello di controllo D stereoscopica nella finestra di dialogo Cambia Impostazioni.

-   Funzionalità e configurazione del computer, che includono la scheda grafica, il driver di grafica e la configurazione del monitor.

[L'esempio 3D Simple Stereo 3D direct3D 11.1](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20stereoscopic%203D%20sample) illustra come aggiungere un effetto 3D stereoscopico e come rispondere alle modifiche stereo del sistema.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Miglioramenti di DXGI 1.2](dxgi-1-2-improvements.md)
</dt> </dl>

 

 
