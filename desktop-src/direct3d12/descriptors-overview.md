---
title: Cenni preliminari sui descrittori
description: I descrittori vengono creati dalle chiamate API e identificano le risorse.
ms.assetid: 64721226-5533-4816-865E-9429032FCC86
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17d83b2fbfd5c5df2738c61aea4f1d1115d6c874
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "104548844"
---
# <a name="descriptors-overview"></a>Cenni preliminari sui descrittori

I descrittori vengono creati dalle chiamate API e identificano le risorse.

-   [Dati del descrittore](#descriptor-data)
-   [Handle descrittore](#descriptor-handles)
-   [Descrittori null](#null-descriptors)
-   [Descrittori predefiniti](#default-descriptors)
-   [Argomenti correlati](#related-topics)

## <a name="descriptor-data"></a>Dati del descrittore

Un descrittore è un blocco di dati relativamente piccolo che descrive completamente un oggetto alla GPU, in un formato opaco specifico della GPU. Sono disponibili diversi tipi di descrittori di &mdash; visualizzazioni di destinazione di rendering (RTVs), viste depth stencil (viste origine dati), viste di risorse shader (SRVs), viste di accesso non ordinate (UAV), viste del buffer costanti (CBVs) e Samplers.

I descrittori variano in base alle dimensioni, a seconda dell'hardware della GPU. È possibile eseguire una query per le dimensioni di un SRV, un UAV o un CBV chiamando [**ID3D12Device:: GetDescriptorHandleIncrementSize**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getdescriptorhandleincrementsize). I descrittori sono mostrati in questa documentazione come unità indivisibili; Ecco un esempio.

![SRV, CBV, UAV e Sampler](images/single-descriptor.png)

I descrittori vengono creati dalle chiamate API e includono informazioni quali la risorsa e le mappe MIP che si desidera includere nel descrittore.

Il driver non tiene traccia dei riferimenti ai descrittori, ma spetta all'app verificare che sia in uso il tipo di descrittore corretto e che le informazioni siano aggiornate. Esiste una piccola eccezione a questo. il driver controlla le associazioni di destinazione di rendering per verificare il corretto funzionamento delle catene di scambio.

Non è necessario liberare o rilasciare i descrittori di oggetti. I driver non alleghino allocazioni alla creazione di un descrittore. Un descrittore, tuttavia, può codificare i riferimenti ad altre allocazioni per cui l'applicazione è proprietaria della durata. Ad esempio, un descrittore per un SRV deve contenere l'indirizzo virtuale della risorsa D3D (ad esempio, una trama) a cui fa riferimento il valore SRV. È responsabilità dell'applicazione verificare che non utilizzi un descrittore SRV quando la risorsa D3D sottostante da cui dipende è stata distrutta o è stata modificata, ad esempio se è stata dichiarata come non residente.

Il modo principale per usare i descrittori consiste nel posizionarli negli heap dei descrittori, che eseguono il backup della memoria per i descrittori.

## <a name="descriptor-handles"></a>Handle descrittore

Un handle del descrittore è l'indirizzo univoco del descrittore. È simile a un puntatore, ma è opaco perché l'implementazione è specifica dell'hardware. L'handle è univoco tra gli heap del descrittore, quindi, ad esempio, una matrice di handle può fare riferimento a descrittori in più heap.

Gli handle della CPU sono per l'uso immediato, ad esempio per la copia in cui è necessario identificare sia l'origine che la destinazione. Immediatamente dopo l'utilizzo (ad esempio, una chiamata a [**ID3D12GraphicsCommandList:: OMSetRenderTargets**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets)), possono essere riutilizzati o l'heap sottostante può essere eliminato.

Gli handle GPU non sono per l'uso immediato &mdash; identificano le posizioni da un elenco di comandi, da usare in fase di esecuzione della GPU. Devono essere conservati fino a quando non vengono eseguiti interamente gli elenchi di comandi che vi fanno riferimento.

Per creare un handle del descrittore per l'inizio di un heap, dopo aver creato l'heap del descrittore stesso, chiamare uno dei metodi seguenti:

-   [**ID3D12DescriptorHeap::GetCPUDescriptorHandleForHeapStart**](/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart)
-   [**ID3D12DescriptorHeap::GetGPUDescriptorHandleForHeapStart**](/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getgpudescriptorhandleforheapstart)

Questi metodi restituiscono le strutture seguenti:

-   [**\_ \_ Handle descrittore CPU D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle)
-   [**\_ \_ Handle descrittore GPU D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle)

Poiché le dimensioni dei descrittori variano in base all'hardware, per ottenere l'incremento tra i descrittori in un heap usare:

-   [**ID3D12Device::GetDescriptorHandleIncrementSize**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getdescriptorhandleincrementsize)

È possibile compensare in modo sicuro una posizione iniziale con un numero di incrementi, per copiare gli handle e per passare gli handle alle chiamate API. Non è sicuro dereferenziare un handle come se fosse un puntatore alla CPU valido, né analizzare i bit all'interno di un handle.

Sono state aggiunte alcune strutture helper, con i membri di inizializzazione, in modo da semplificare la gestione degli handle.

-   [**\_ \_ Handle descrittore CPU CD3DX12 \_**](cd3dx12-cpu-descriptor-handle.md)
-   [**\_ \_ Handle descrittore GPU CD3DX12 \_**](cd3dx12-gpu-descriptor-handle.md)

## <a name="null-descriptors"></a>Descrittori null

Quando si creano descrittori usando chiamate API, le applicazioni passano NULL per il puntatore di risorsa nella definizione del descrittore per ottenere l'effetto di nessun limite quando si accede da uno shader.

Il resto del descrittore deve essere popolato il più possibile. Ad esempio, nel caso di viste di risorse shader (SRVs), il descrittore può essere usato per distinguere il tipo di visualizzazione, ovvero Texture1D, Texture2D e così via. I parametri numerici nel descrittore della vista, ad esempio il numero di mipmap, devono essere tutti impostati su valori validi per una risorsa.

In molti casi, esiste un comportamento definito per l'accesso a una risorsa non associata, ad esempio SRVs, che restituisce valori predefiniti. Questi verranno rispettati quando si accede a un descrittore NULL, purché il tipo di accesso dello shader sia compatibile con il tipo di descrittore. Se, ad esempio, uno shader prevede un Texture2D SRV e accede a un SRV NULL definito come Texture1D, il comportamento non è definito e potrebbe causare la reimpostazione del dispositivo.

In sintesi, per creare un descrittore null, passare `null` per il parametro *PreSource* quando si crea la vista con metodi quali [**CreateShaderResourceView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview). Per il parametro View Description *pDesc*, impostare una configurazione che funzioni se la risorsa non è null. in caso contrario, potrebbe verificarsi un arresto anomalo in alcuni componenti hardware.

I descrittori radice, tuttavia, non devono essere impostati su null.

Nell'hardware Tier1 (vedere i [**livelli hardware**](./hardware-support.md), tutti i descrittori associati (tramite tabelle descrittore) devono essere inizializzati, come descrittori reali o descrittori null, anche se non è possibile accedervi dall'hardware; in caso contrario, il comportamento non è definito.

Nell'hardware livello 2, questo vale per i descrittori CBV e UAV associati, ma non per i descrittori SRV.

Nell'hardware di livello 3 non esiste alcuna restrizione, purché non venga mai eseguito l'accesso a descrittori non inizializzati.

## <a name="default-descriptors"></a>Descrittori predefiniti

Per creare un descrittore predefinito per una determinata visualizzazione, passare un parametro *PreSource* valido al metodo Create View (ad esempio [**CreateShaderResourceView**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview)), ma passare **null** per il parametro *pDesc* . Ad esempio, se la risorsa conteneva 14 MIPS, la vista conterrebbe 14 MIPS. Il caso predefinito riguarda il mapping più ovvio di una risorsa a una vista. Questa operazione richiede che la risorsa venga allocata con un nome di formato completo (ad esempio **DXGI_FORMAT_R8G8B8A8_UNORM_SRGB** anziché **DXGI_FORMAT_R8G8B8A8_TYPELESS**).

I descrittori predefiniti non possono essere usati con una visualizzazione struttura di accelerazione raytracing, perché il parametro *PreSource* specificato deve essere **null** e il percorso deve essere passato tramite un d3d12_raytracing_acceleration_structure_srv [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_SRV**]/Windows/Win32/API/d3d12/NS-d3d12-).

## <a name="related-topics"></a>Argomenti correlati

[Descrittori](descriptors.md)