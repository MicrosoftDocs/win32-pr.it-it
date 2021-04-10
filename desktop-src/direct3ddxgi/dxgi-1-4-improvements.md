---
description: Le funzionalità seguenti sono state aggiunte o modificate in Microsoft DirectX Graphics Infrastructure (DXGI) 1,4, in gran parte per supportare Direct3D 12.
ms.assetid: DEA901EA-B0F9-41D9-802C-ED1D6A7888E0
title: Miglioramenti di DXGI 1,4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24e9a8a48dd026248afac7c1a7df23a99176adef
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104048919"
---
# <a name="dxgi-14-improvements"></a>Miglioramenti di DXGI 1,4

Le funzionalità seguenti sono state aggiunte o modificate in Microsoft DirectX Graphics Infrastructure (DXGI) 1,4, in gran parte per supportare Direct3D 12.

## <a name="cheaper-adapter-enumeration"></a>Enumerazione di adapter più economica

Per Direct3D 12, non è più possibile eseguire il backtracking da un dispositivo al [**IDXGIAdapter**](/windows/win32/api/DXGI/nn-dxgi-idxgiadapter) usato per crearlo. Non è inoltre più possibile fornire la \_ distorsione del tipo di driver D3D \_ \_ in [**D3D12CreateDevice**](/windows/win32/api/d3d12/nf-d3d12-d3d12createdevice). Per semplificare lo sviluppo, è possibile usare [**IDXGIFactory4**](/windows/win32/api/DXGI1_4/nn-dxgi1_4-idxgifactory4) per gestire entrambe queste operazioni. [**IDXGIFactory4:: EnumAdapterByLuid**](/windows/win32/api/DXGI1_4/nf-dxgi1_4-idxgifactory4-enumadapterbyluid) (progettato per essere abbinato a [**ID3D12Device:: GetAdapterLuid**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getadapterluid)) consente a un'app di recuperare informazioni sull'adapter in cui è stato creato un dispositivo Direct3D 12. [**IDXGIFactory4:: EnumWarpAdapter**](/windows/win32/api/DXGI1_4/nf-dxgi1_4-idxgifactory4-enumwarpadapter) fornisce un adapter che può essere fornito a **D3D12CreateDevice** per usare il renderer Warp.

## <a name="video-memory-budget-tracking"></a>Rilevamento del budget di memoria video

Gli sviluppatori di applicazioni sono invitati a usare un sistema di prenotazione della memoria video, per informare il sistema operativo della quantità di memoria video fisica che l'app non può andare senza.

La quantità di memoria fisica disponibile per un processo è nota come "budget di memoria video". Il budget può variare in modo evidente dal momento che i processi in background riattivano e dormono; e variano notevolmente quando l'utente passa a un'altra applicazione. L'applicazione può ricevere una notifica quando il budget viene modificato e viene eseguito il polling del budget corrente e della quantità di memoria attualmente utilizzata. Se un'applicazione non rimane entro il suo budget, il processo verrà bloccato in modo intermittente per consentire l'esecuzione di altre applicazioni e/o le API di creazione restituiranno un errore. L'interfaccia [**IDXGIAdapter3**](/windows/win32/api/dxgi1_4/nn-dxgi1_4-idxgiadapter3) fornisce i metodi relativi a questa funzionalità, in particolare [**QueryVideoMemoryInfo**](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-queryvideomemoryinfo) e [**RegisterVideoMemoryBudgetChangeNotificationEvent**](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-registervideomemorybudgetchangenotificationevent).

Per ulteriori informazioni, vedere l'argomento relativo a Direct3D 12 sulla [residenza](../direct3d12/residency.md).

## <a name="direct3d-12-swapchain-changes"></a>Modifiche presentazione catena Direct3D 12

Alcune delle funzionalità esistenti di Direct3D 11 presentazione catena sono state deprecate per ottenere le riduzioni del sovraccarico in Direct3D 12. Mentre altre modifiche sono state apportate per essere allineate ai concetti di Direct3D 12 o fornire un supporto migliore per le funzionalità di Direct3D 12.

**Identità backBuffer invariante**

In Direct3D 11, le applicazioni possono chiamare [**GetBuffer**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-getbuffer)(0,... ) una sola volta. Ogni chiamata a [**present**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-present) ha modificato in modo implicito l'identità della risorsa dell'interfaccia restituita. Direct3D 12 non supporta più la modifica dell'identità della risorsa implicita, a causa dell'overhead della CPU necessario e della progettazione flessibile del descrittore delle risorse. Di conseguenza, l'applicazione deve chiamare manualmente **GetBuffer** per ogni buffer creato con presentazione catena. È necessario eseguire manualmente il rendering dell'applicazione nel buffer successivo della sequenza dopo aver chiamato **present**. Le applicazioni sono incoraggiate a creare una cache di descrittori **per ogni buffer**, anziché ricreare molti oggetti.

**Supporto per più adapter**

Quando viene creato un presentazione catena in un adapter per più GPU, tutti i buffer vengono creati nel nodo 1 ed è supportata solo una singola coda dei comandi. [**ResizeBuffers1**](/windows/win32/api/DXGI1_4/nf-dxgi1_4-idxgiswapchain3-resizebuffers1) consente alle applicazioni di creare backBuffer su nodi diversi, consentendo l'uso di una diversa coda dei comandi con ognuno di essi. Queste funzionalità consentono di usare le tecniche AFR (alternate frame rendering) con presentazione catena. Vedere sistemi con più [Adapter](../direct3d12/multi-engine.md).

**Varie**

-   Un oggetto della coda di comandi deve essere passato ai metodi [**CreateSwapChain**](/windows/win32/api/DXGI/nf-dxgi-idxgifactory-createswapchain) anziché all'oggetto dispositivo Direct3D 12.
-   Sono supportati solo i due effetti di swapping del modello Flip seguenti: <dl> DXGI \_ swap \_ Effect \_ Flip \_ ignorate deve essere preferito quando le applicazioni eseguono il rendering completo sul backBuffer prima di presentarlo o sono interessati a supportare facilmente scenari con più adapter.  
    \_ \_ \_ \_ Le applicazioni che si basano sulle ottimizzazioni di presentazione parziali devono essere utilizzate da applicazioni che si basano sulle ottimizzazioni di presentazione parziali o letti regolarmente dai buffer precedenti presentati precedentemente.  
    </dl>
-   [**SetFullscreenState**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-setfullscreenstate) no longer exclusively owns the display, so user-initiated operating system elements can seamlessly appear in front of application output. Volume settings is an example of this.

## <a name="related-topics"></a>Argomenti correlati

[Livelli di funzionalità hardware di Direct3D 12](../direct3d12/hardware-feature-levels.md)

[Guida per programmatori per DXGI](dx-graphics-dxgi-overviews.md)
