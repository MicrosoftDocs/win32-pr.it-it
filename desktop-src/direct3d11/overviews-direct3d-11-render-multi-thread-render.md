---
title: Rendering immediato e posticipato
description: Direct3D 11 supporta due tipi di rendering immediato e posticipato. Entrambi vengono implementati usando l'interfaccia ID3D11DeviceContext.
ms.assetid: 8991be9f-c882-4752-9048-704fe4ae1725
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8740a957ec4b7f2edacb4b753c7f68230494b10cf33721ef6c2d869de334517b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117912933"
---
# <a name="immediate-and-deferred-rendering"></a>Rendering immediato e posticipato

Direct3D 11 supporta due tipi di rendering: immediato e posticipato. Entrambi vengono implementati usando [**l'interfaccia ID3D11DeviceContext.**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)

## <a name="immediate-rendering"></a>Rendering immediato

Il rendering immediato si riferisce alla chiamata di API o comandi di rendering da un dispositivo, che accoda i comandi in un buffer per l'esecuzione nella GPU. Usare un contesto immediato per eseguire il rendering, impostare lo stato della pipeline e riprodurre un elenco di comandi.

Creare un contesto immediato [**usando D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) o [**D3D11CreateDeviceAndSwapChain.**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain)

## <a name="deferred-rendering"></a>Rendering posticipato

Il rendering posticipato registra i comandi grafici in un buffer dei comandi in modo che possano essere riprodotti in un altro momento. Usare un contesto posticipato per registrare i comandi (rendering e impostazione dello stato) in un elenco di comandi. Il rendering posticipato è un nuovo concetto di Direct3D 11. Il rendering posticipato è progettato per supportare il rendering in un thread durante la registrazione dei comandi per il rendering in thread aggiuntivi. Questa strategia multithreading parallela consente di suddividere scene complesse in attività simultanee. Per altre informazioni sul rendering di scene complesse, vedere [Rendering a più passi.](overviews-direct3d-11-render-multipass.md)

Creare un contesto posticipato [**usando ID3D11Device::CreateDeferredContext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdeferredcontext).

Direct3D genera un sovraccarico di rendering quando accoda i comandi nel buffer dei comandi. Al contrario, un [elenco di comandi](overviews-direct3d-11-render-multi-thread-command-list.md) viene eseguito in modo molto più efficiente durante la riproduzione. Per usare un elenco di comandi, registrare i comandi di rendering con un contesto posticipato e riprodurli usando un contesto immediato.

È possibile generare un solo elenco di comandi in modalità a thread singolo. Tuttavia, è possibile creare e usare più contesti posticied contemporaneamente, ognuno in un thread separato. È quindi possibile usare questi più contesti posticied per creare contemporaneamente più elenchi di comandi.

Non è possibile riprodurre contemporaneamente due o più elenchi di comandi nel contesto immediato.

Per determinare se un contesto di dispositivo è immediato o posticipato, chiamare [**ID3D11DeviceContext::GetType**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-gettype).

Il [**metodo ID3D11DeviceContext::Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) è supportato solo in un contesto posticipato per le risorse dinamiche [**(D3D11 \_ USAGE \_ DYNAMIC)**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)in cui la prima chiamata all'interno dell'elenco di comandi è [**D3D11 \_ MAP WRITE \_ \_ DISCARD.**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) **D3D11 \_ MAP \_ WRITE NO OVERWRITE \_ \_ è** supportato nelle chiamate successive, se disponibile per il tipo di risorsa specificato.

Le query in un contesto posticipato sono limitate alla generazione di dati e al disegno predicato. Non è possibile chiamare [**ID3D11DeviceContext::GetData**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-getdata) su un contesto posticipato per ottenere i dati su una query. È possibile chiamare **GetData solo** nel contesto immediato per ottenere dati su una query. È possibile impostare un predicato di rendering (un tipo di query) chiamando [**D3D11DeviceContext::SetPredication**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-setpredication) per usare i risultati della query nella GPU. È possibile generare dati di query tramite chiamate [**a ID3D11DeviceContext::Begin**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-begin) e [**ID3D11DeviceContext::End.**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-end) Tuttavia, i dati della query non saranno disponibili fino a quando non si chiama [**ID3D11DeviceContext::ExecuteCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-executecommandlist) sul contesto immediato per inviare l'elenco di comandi di contesto posticipato. I dati della query vengono quindi elaborati dalla GPU.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Multithreading](overviews-direct3d-11-render-multi-thread.md)
</dt> </dl>

 

 




