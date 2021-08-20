---
title: Panoramica dei descrittori
description: I descrittori vengono creati dalle chiamate API e identificano le risorse.
ms.assetid: 64721226-5533-4816-865E-9429032FCC86
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95cb5834c513b99e737ba8a106ea5303a978751573ffd2ca1a97fb59e385b5ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117733844"
---
# <a name="descriptors-overview"></a>Panoramica dei descrittori

I descrittori vengono creati dalle chiamate API e identificano le risorse.

-   [Dati del descrittore](#descriptor-data)
-   [Handle del descrittore](#descriptor-handles)
-   [Descrittori Null](#null-descriptors)
-   [Descrittori predefiniti](#default-descriptors)
-   [Argomenti correlati](#related-topics)

## <a name="descriptor-data"></a>Dati del descrittore

Un descrittore è un blocco di dati relativamente piccolo che descrive completamente un oggetto per la GPU, in un formato opaco specifico della GPU. Esistono diversi tipi di descrittori che eseguono il rendering delle visualizzazioni di destinazione (RTV), viste depth stencil (DVS), viste di risorse shader (SV), viste di accesso non ordinato (UAV), visualizzazioni di buffer costanti &mdash; (CPV) e campionatori.

Le dimensioni dei descrittori variano a seconda dell'hardware GPU. È possibile eseguire una query per ottenere le dimensioni di un oggetto SRV, UAV o CBV chiamando [**ID3D12Device::GetDescriptorHandleIncrementSize**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getdescriptorhandleincrementsize). I descrittori vengono visualizzati in questa documentazione come unità indivisibili. Di seguito è riportato un esempio.

![srv, cbv, uav e sampler](images/single-descriptor.png)

I descrittori vengono creati dalle chiamate API e includeranno informazioni quali la risorsa e le mappe mip che si vuole includere nel descrittore.

Il driver non tiene traccia o contiene riferimenti ai descrittori, è responsabilità dell'app verificare che sia in uso il tipo di descrittore corretto e che le informazioni siano aggiornate. C'è una piccola eccezione a questo; il driver controlla le associazioni di destinazione di rendering per garantire il corretto funzionamento delle catene di scambio.

I descrittori di oggetto non devono essere liberati o rilasciati. I driver non collegano alcuna allocazione alla creazione di un descrittore. Un descrittore può tuttavia codificare riferimenti ad altre allocazioni per le quali l'applicazione è proprietaria della durata. Ad esempio, un descrittore per un SRV deve contenere l'indirizzo virtuale della risorsa D3D (ad esempio una trama) a cui fa riferimento SRV. È responsabilità dell'applicazione assicurarsi che non usi un descrittore SRV quando la risorsa D3D sottostante da cui dipende è stata distrutta o viene modificata (ad esempio viene dichiarata come non rientrante).

Il modo principale per usare i descrittori è posizionarli negli heap dei descrittori, che sono memoria di backup per i descrittori.

## <a name="descriptor-handles"></a>Handle del descrittore

Un handle del descrittore è l'indirizzo univoco del descrittore. È simile a un puntatore, ma è opaco perché l'implementazione è specifica dell'hardware. L'handle è univoco tra gli heap dei descrittori, quindi, ad esempio, una matrice di handle può fare riferimento ai descrittori in più heap.

Gli handle della CPU sono per l'uso immediato, ad esempio la copia in cui è necessario identificare sia l'origine che la destinazione. Immediatamente dopo l'uso ( ad esempio, una chiamata a [**ID3D12GraphicsCommandList::OMSetRenderTargets**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets)), possono essere riutilizzati o l'heap sottostante può essere eliminato.

Gli handle GPU non sono per uso immediato e identificano i percorsi da un elenco di &mdash; comandi, per l'uso in fase di esecuzione della GPU. Devono essere mantenuti fino a quando tutti gli elenchi di comandi che vi fanno riferimento non sono stati eseguiti interamente.

Per creare un handle del descrittore per l'inizio di un heap, dopo aver creato l'heap del descrittore stesso, chiamare uno dei metodi seguenti:

-   [**ID3D12DescriptorHeap::GetCPUDescriptorHandleForHeapStart**](/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart)
-   [**ID3D12DescriptorHeap::GetGPUDescriptorHandleForHeapStart**](/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getgpudescriptorhandleforheapstart)

Questi metodi restituiscono le strutture seguenti:

-   [**HANDLE DESCRITTORE CPU D3D12 \_ \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle)
-   [**HANDLE DESCRITTORE GPU D3D12 \_ \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle)

Poiché le dimensioni dei descrittori variano in base all'hardware, per ottenere l'incremento tra ogni descrittore in un uso dell'heap:

-   [**ID3D12Device::GetDescriptorHandleIncrementSize**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getdescriptorhandleincrementsize)

È possibile eseguire l'offset di una posizione iniziale con un numero di incrementi, copiare gli handle e passare gli handle nelle chiamate API. Non è sicuro dereferenziare un handle come se fosse un puntatore alla CPU valido, né analizzare i bit all'interno di un handle.

Sono state aggiunte alcune strutture helper, con membri di inizializzazione, per semplificare la gestione degli handle.

-   [**HANDLE DESCRITTORE CPU CD3DX12 \_ \_ \_**](cd3dx12-cpu-descriptor-handle.md)
-   [**HANDLE DESCRITTORE GPU CD3DX12 \_ \_ \_**](cd3dx12-gpu-descriptor-handle.md)

## <a name="null-descriptors"></a>Descrittori Null

Quando si creano descrittori usando chiamate API, le applicazioni passano NULL per il puntatore di risorsa nella definizione del descrittore per ottenere l'effetto di nessun elemento associato quando vi si accede da uno shader.

Il resto del descrittore deve essere popolato il più possibile. Ad esempio, nel caso di visualizzazioni di risorse shader (SRV), il descrittore può essere usato per distinguere il tipo di visualizzazione (Texture1D, Texture2D e così via). I parametri numerici nel descrittore di visualizzazione, ad esempio il numero di mipmap, devono essere tutti impostati su valori validi per una risorsa.

In molti casi, esiste un comportamento definito per l'accesso a una risorsa non associata, ad esempio gli SPV che restituiscono valori predefiniti. Tali valori verranno rispettati quando si accede a un descrittore NULL, purché il tipo di accesso allo shader sia compatibile con il tipo di descrittore. Ad esempio, se uno shader prevede un SRV Texture2D e accede a un SRV NULL definito come Texture1D, il comportamento non è definito e potrebbe causare la reimpostazione del dispositivo.

In sintesi, per creare un descrittore Null, passare per il parametro pResource durante la creazione della vista con metodi come `null` [**CreateShaderResourceView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview).  Per il parametro *pDesc* della descrizione della vista, impostare una configurazione che funzioni se la risorsa non fosse Null (in caso contrario, potrebbe verificarsi un arresto anomalo in alcuni componenti hardware).

I descrittori radice, tuttavia, non devono essere impostati su Null.

Nell'hardware di livello 1 (vedere [**Livelli**](./hardware-support.md)hardware, tutti i descrittori associati (tramite tabelle descrittori) devono essere inizializzati come descrittori reali o null, anche se non sono accessibili dall'hardware, altrimenti il comportamento non è definito.

Nell'hardware di livello 2, ciò si applica ai descrittori CBV e UAV associati, ma non ai descrittori SRV.

Nell'hardware di livello 3 non è prevista alcuna restrizione, a condizione che i descrittori non inizializzati non siano mai accessibili.

## <a name="default-descriptors"></a>Descrittori predefiniti

Per creare un descrittore predefinito per una determinata vista, passare un parametro *pResource* valido al metodo di creazione della vista ( ad esempio [**CreateShaderResourceView**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview)), ma passare **NULL** per il *parametro pDesc.* Ad esempio, se la risorsa contiene 14 mips, la vista conterrà 14 mips. Il caso predefinito riguarda il mapping più ovvio di una risorsa a una vista. Ciò richiede che la risorsa sia allocata con un nome di formato completo ( ad esempio **DXGI_FORMAT_R8G8B8A8_UNORM_SRGB** anziché **DXGI_FORMAT_R8G8B8A8_TYPELESS**).

I descrittori predefiniti non possono essere usati con una visualizzazione struttura di accelerazione raytracing, perché il parametro *pResource* fornito deve essere **NULL** e il percorso deve essere passato tramite un [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_SRV**]/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_srv).

## <a name="related-topics"></a>Argomenti correlati

[Descrittori](descriptors.md)