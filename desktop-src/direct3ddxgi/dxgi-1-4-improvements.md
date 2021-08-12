---
description: Le funzionalità seguenti sono state aggiunte o modificate in Microsoft DirectX Graphic Infrastructure (DXGI) 1.4, in gran parte per supportare Direct3D 12.
ms.assetid: DEA901EA-B0F9-41D9-802C-ED1D6A7888E0
title: Miglioramenti di DXGI 1.4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aef5777f50a149da6ccb2893bcac8a8f509c86cdff40d94889155c2e5e1eb12c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118289555"
---
# <a name="dxgi-14-improvements"></a>Miglioramenti di DXGI 1.4

Le funzionalità seguenti sono state aggiunte o modificate in Microsoft DirectX Graphic Infrastructure (DXGI) 1.4, in gran parte per supportare Direct3D 12.

## <a name="cheaper-adapter-enumeration"></a>Enumerazione degli adapter più economica

Per Direct3D 12, non è più possibile eseguire il backtracking da un dispositivo [**all'oggetto IDXGIAdapter**](/windows/win32/api/DXGI/nn-dxgi-idxgiadapter) usato per crearlo. Inoltre, non è più possibile fornire D3D \_ DRIVER \_ TYPE \_ WARP in [**D3D12CreateDevice**](/windows/win32/api/d3d12/nf-d3d12-d3d12createdevice). Per semplificare lo sviluppo, è possibile usare [**IDXGIFactory4**](/windows/win32/api/DXGI1_4/nn-dxgi1_4-idxgifactory4) per gestire entrambi questi elementi. [**IDXGIFactory4::EnumAdapterByLuid**](/windows/win32/api/DXGI1_4/nf-dxgi1_4-idxgifactory4-enumadapterbyluid) (progettato per essere associato a [**ID3D12Device::GetAdapterLuid)**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getadapterluid)consente a un'app di recuperare informazioni sull'adattatore in cui è stato creato un dispositivo Direct3D 12. [**IDXGIFactory4::EnumWarpAdapter**](/windows/win32/api/DXGI1_4/nf-dxgi1_4-idxgifactory4-enumwarpadapter) fornisce un adattatore che può essere fornito a **D3D12CreateDevice** per usare il renderer WARP.

## <a name="video-memory-budget-tracking"></a>Monitoraggio del budget per la memoria video

Gli sviluppatori di applicazioni sono invitati a usare un sistema di prenotazione della memoria video per informare il sistema operativo della quantità di memoria video fisica a cui l'app non può fare a meno.

La quantità di memoria fisica disponibile per un processo è nota come "budget di memoria video". Il budget può variare notevolmente durante la riattivazione e la sospensione dei processi in background. e fluttuano notevolmente quando l'utente passa a un'altra applicazione. L'applicazione può ricevere una notifica quando il budget cambia ed eseguire il polling sia del budget corrente che della quantità di memoria attualmente utilizzata. Se un'applicazione non rimane entro il budget, il processo verrà bloccato in modo intermittente per consentire l'esecuzione di altre applicazioni e/o le API di creazione restituiranno un errore. [**L'interfaccia IDXGIAdapter3**](/windows/win32/api/dxgi1_4/nn-dxgi1_4-idxgiadapter3) fornisce i metodi relativi a questa funzionalità, in particolare [**QueryVideoMemoryInfo**](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-queryvideomemoryinfo) e [**RegisterVideoMemoryBudgetChangeNotificationEvent.**](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-registervideomemorybudgetchangenotificationevent)

Per altre informazioni, vedere l'argomento Direct3D 12 su [Residency.](../direct3d12/residency.md)

## <a name="direct3d-12-swapchain-changes"></a>Modifiche dello swapchain Direct3D 12

Alcune delle funzionalità di swapchain Direct3D 11 esistenti sono state deprecate per ottenere le riduzioni del sovraccarico in Direct3D 12. Anche se sono state apportate altre modifiche per allinearsi ai concetti di Direct3D 12 o per offrire un supporto migliore per le funzionalità di Direct3D 12.

**Identità backbuffer invariante**

In Direct3D 11 le applicazioni possono chiamare [**GetBuffer**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-getbuffer)( 0, ... ) una sola volta. Ogni chiamata a [**Present ha**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-present) modificato in modo implicito l'identità della risorsa dell'interfaccia restituita. Direct3D 12 non supporta più tale modifica implicita dell'identità delle risorse, a causa dell'overhead della CPU richiesto e della progettazione flessibile del descrittore di risorse. Di conseguenza, l'applicazione deve chiamare **manualmente GetBuffer** per ogni buffer creato con il swapchain. L'applicazione deve eseguire manualmente il rendering nel buffer successivo nella sequenza dopo la chiamata a **Present.** Le applicazioni sono invitate a creare una cache di descrittori per ogni buffer, invece di creare di nuovo molti oggetti per **ogni oggetto Presente.**

**Supporto di più schede**

Quando viene creato un swapchain in una scheda con più GPU, i backbuffer vengono tutti creati nel nodo 1 ed è supportata una sola coda di comandi. [**ResizeBuffers1 consente**](/windows/win32/api/DXGI1_4/nf-dxgi1_4-idxgiswapchain3-resizebuffers1) alle applicazioni di creare backbuffer in nodi diversi, consentendo l'uso di una coda di comandi diversa con ognuno di essi. Queste funzionalità consentono l'uso di tecniche AFR (Alternate Frame Rendering) con lo swapchain. Fare riferimento a [Sistemi con più schede.](../direct3d12/multi-engine.md)

**Varie**

-   È necessario passare un oggetto coda di comandi [**ai metodi CreateSwapChain**](/windows/win32/api/DXGI/nf-dxgi-idxgifactory-createswapchain) anziché all'oggetto dispositivo Direct3D 12.
-   Sono supportati solo i due effetti di scambio del modello di capovolgimento seguenti: <dl> È consigliabile preferire DXGI SWAP EFFECT FLIP DISCARD quando le applicazioni eseguono il rendering completo sul buffer backbuffer prima di presentarlo o sono interessate a supportare facilmente scenari \_ \_ con più \_ \_ adattatori.  
    DXGI \_ SWAP EFFECT FLIP \_ \_ SEQUENTIAL deve essere usato da applicazioni che si basano su ottimizzazioni parziali della presentazione o leggono regolarmente da backbuffer presentati \_ in precedenza.  
    </dl>
-   [**SetFullscreenState**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-setfullscreenstate) no longer exclusively owns the display, so user-initiated operating system elements can seamlessly appear in front of application output. Volume settings is an example of this.

## <a name="related-topics"></a>Argomenti correlati

[Livelli di funzionalità hardware Direct3D 12](../direct3d12/hardware-feature-levels.md)

[Guida di programmazione per DXGI](dx-graphics-dxgi-overviews.md)
