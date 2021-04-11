---
description: Le app non possono eseguire il rendering in stereo, a meno che il sistema operativo non indichi che Abilita il comportamento di visualizzazione stereoscopica 3D. Le app determinano se eseguire il rendering in 3D stereoscopico in modo diverso a seconda che siano a finestra o a schermo intero.
ms.assetid: FB8AC57E-38DD-47B5-8666-1F4B73488F8B
title: Rendering in stereo e notifica sullo stato stereo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 379c6335e0bd060cf0065fe92bf2ec6c086289c3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123327"
---
# <a name="rendering-in-stereo-and-notifying-about-stereo-status"></a>Rendering in stereo e notifica sullo stato stereo

Le app non possono eseguire il rendering in stereo, a meno che il sistema operativo non indichi che Abilita il comportamento di visualizzazione stereoscopica 3D. Le app determinano se eseguire il rendering in 3D stereoscopico in modo diverso a seconda che siano a finestra o a schermo intero.

Un'app finestra chiama il metodo [**IDXGIFactory2:: IsWindowedStereoEnabled**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-iswindowedstereoenabled) per determinare se eseguire il rendering in stereo. Un'app a schermo intero chiama il metodo [**IDXGIOutput1:: GetDisplayModeList1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutput1-getdisplaymodelist1) e quindi determina se una delle modalità di visualizzazione restituite supporta il rendering in stereo. Il metodo **GetDisplayModeList1** non enumera le modalità stereo a meno che non si specifichi il flag stereo delle [**\_ \_ modalità \_ di enumerazione DXGI**](dxgi-enum-modes.md) nel parametro *Flags* . Un'app a finestra o a schermo intero che supporta lo stereo consente innanzitutto di eseguire il rendering in stereo in base a una chiamata al metodo **IDXGIFactory2:: IsWindowedStereoEnabled** o **IDXGIOutput1:: GetDisplayModeList1** e quindi registra per la notifica delle modifiche dello stato stereo. Poiché l'app non può basarsi sulla notifica per indicare lo stato corrente del comportamento di visualizzazione stereoscopico 3D, quando riceve un messaggio di notifica o un evento della finestra, deve chiamare di nuovo **IDXGIFactory2:: IsWindowedStereoEnabled** o **IDXGIOutput1:: GetDisplayModeList1** per determinare lo stato corrente del comportamento di visualizzazione stereoscopica 3D del sistema operativo.

Se si desidera eseguire il rendering in stereo, è necessario registrarsi per le notifiche stereo per verificare quando l'utente disattiva o è in modalità stereo. Un'app può registrarsi per ricevere notifiche sulle modifiche dello stato 3D stereoscopico tramite un messaggio a una finestra o tramite la segnalazione degli eventi. Per eseguire la registrazione per ricevere messaggi di notifica a una finestra in merito alle modifiche dello stato stereo, un'app chiama il metodo [**IDXGIFactory2:: RegisterStereoStatusWindow**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-registerstereostatuswindow) . Per eseguire la registrazione per ricevere la notifica delle modifiche dello stato stereo tramite segnalazione eventi, un'app chiama il metodo [**IDXGIFactory2:: RegisterStereoStatusEvent**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-registerstereostatusevent) . Entrambi i metodi restituiscono un puntatore a un valore di chiave che l'app può usare per annullare la registrazione della notifica. Per annullare la registrazione della notifica, l'app passa il valore della chiave al metodo [**IDXGIFactory2:: UnregisterStereoStatus**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-unregisterstereostatus) .

Lo stato stereo può contenere gli elementi seguenti:

-   Configurazione utente.

    Gli utenti di Windows possono abilitare o disabilitare la visualizzazione stereo con l'opzione Abilita stereoscopica 3D nelle impostazioni di visualizzazione delle modifiche del pannello di controllo.

-   Funzionalità e configurazione del computer, inclusi scheda grafica, driver di grafica e configurazione del monitoraggio.

L' [esempio Direct3D 11,1 Simple Stereo 3D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20stereoscopic%203D%20sample) Mostra come aggiungere un effetto 3D stereoscopico e come rispondere alle modifiche apportate al sistema stereo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Miglioramenti di DXGI 1,2](dxgi-1-2-improvements.md)
</dt> </dl>

 

 
