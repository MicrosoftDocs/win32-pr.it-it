---
title: Rendering immediato e posticipato
description: Direct3D 11 supporta due tipi di rendering immediato e posticipato. Entrambe le implementazioni sono implementate tramite l'interfaccia sul ID3D11DeviceContext.
ms.assetid: 8991be9f-c882-4752-9048-704fe4ae1725
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef954a8e794755e1405c8e1e07505a5f39189b03
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104992821"
---
# <a name="immediate-and-deferred-rendering"></a>Rendering immediato e posticipato

Direct3D 11 supporta due tipi di rendering: immediato e posticipato. Entrambe le implementazioni sono implementate tramite l'interfaccia [**sul ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) .

## <a name="immediate-rendering"></a>Rendering immediato

Il rendering immediato si riferisce alla chiamata di API o comandi di rendering da un dispositivo, che accoda i comandi in un buffer per l'esecuzione sulla GPU. Usare un contesto immediato per eseguire il rendering, impostare lo stato della pipeline e riprodurre un elenco di comandi.

Creare un contesto immediato usando [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) o [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain).

## <a name="deferred-rendering"></a>Rendering posticipato

Il rendering posticipato registra i comandi grafici in un buffer dei comandi in modo che possano essere riprodotti in un altro momento. Usare un contesto posticipato per registrare i comandi (rendering e impostazione dello stato) in un elenco di comandi. Il rendering posticipato è un nuovo concetto in Direct3D 11; il rendering posticipato è progettato per supportare il rendering in un thread durante la registrazione dei comandi per il rendering su thread aggiuntivi. Questa strategia parallela multithread consente di suddividere le scene complesse in attività simultanee. Per altre informazioni sul rendering di scene complesse, vedere [rendering a più passaggi](overviews-direct3d-11-render-multipass.md).

Creare un contesto posticipato usando [**ID3D11Device:: CreateDeferredContext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdeferredcontext).

Direct3D genera un sovraccarico di rendering quando accoda i comandi nel buffer dei comandi. Al contrario, un [elenco di comandi](overviews-direct3d-11-render-multi-thread-command-list.md) viene eseguito in modo molto più efficiente durante la riproduzione. Per usare un elenco di comandi, registrare i comandi di rendering con un contesto posticipato e riprodurli usando un contesto immediato.

È possibile generare solo un singolo elenco di comandi in modalità a thread singolo. Tuttavia, è possibile creare e usare contemporaneamente più contesti posticipati, ognuno in un thread separato. Quindi, è possibile usare questi più contesti posticipati per creare simultaneamente più elenchi di comandi.

Non è possibile riprodurre contemporaneamente due o più elenchi di comandi nel contesto immediato.

Per determinare se un contesto di dispositivo è un contesto immediato o posticipato, chiamare [**sul ID3D11DeviceContext:: GetType**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-gettype).

Il metodo [**sul ID3D11DeviceContext:: Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) è supportato solo in un contesto posticipato per le risorse dinamiche ([**\_ \_ Dynamic Usage d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)), in cui la prima chiamata all'interno dell'elenco di comandi è [**d3d11 \_ mapping \_ Write \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map). **D3d11 \_ \_ \_ Non \_** è supportata la sovrascrittura della mappa per le chiamate successive, se disponibili per il tipo di risorsa specificato.

Le query in un contesto posticipato sono limitate alla generazione dei dati e al disegno predicato. Non è possibile chiamare [**sul ID3D11DeviceContext:: GetData**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-getdata) in un contesto posticipato per ottenere i dati relativi a una query. è possibile chiamare **GetData** solo nel contesto immediato per ottenere i dati relativi a una query. È possibile impostare un predicato di rendering, ovvero un tipo di query, chiamando [**su D3D11DeviceContext:: SetPredication**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-setpredication) per utilizzare i risultati della query nella GPU. È possibile generare dati di query tramite chiamate a [**sul ID3D11DeviceContext:: Begin**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-begin) e [**sul ID3D11DeviceContext:: end**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-end). Tuttavia, i dati della query non saranno disponibili fino a quando non si chiama [**sul ID3D11DeviceContext:: ExecuteCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-executecommandlist) nel contesto immediato per inviare l'elenco di comandi del contesto posticipato. I dati della query vengono quindi elaborati dalla GPU.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Multithreading](overviews-direct3d-11-render-multi-thread.md)
</dt> </dl>

 

 




