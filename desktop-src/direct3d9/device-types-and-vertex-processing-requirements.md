---
description: Le prestazioni delle operazioni di elaborazione dei vertici, incluse la trasformazione e l'illuminazione, dipendono in larga misura dal punto in cui è presente il buffer dei vertici in memoria e dal tipo di dispositivo di rendering utilizzato.
ms.assetid: 4f9ca83d-c9d6-4749-944d-78f831b0f44e
title: Tipi di dispositivi e requisiti di elaborazione dei vertici (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 590cf2f5423d9c3bdf3e19c91f30b3e8c0586687
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521442"
---
# <a name="device-types-and-vertex-processing-requirements-direct3d-9"></a>Tipi di dispositivi e requisiti di elaborazione dei vertici (Direct3D 9)

Le prestazioni delle operazioni di elaborazione dei vertici, incluse la trasformazione e l'illuminazione, dipendono in larga misura dal punto in cui è presente il buffer dei vertici in memoria e dal tipo di dispositivo di rendering utilizzato. Le applicazioni controllano l'allocazione di memoria per i buffer dei vertici quando vengono creati. Quando \_ viene impostato il flag di Memoria D3DPOOL SYSTEMMEM, il buffer dei vertici viene creato nella memoria di sistema. Quando \_ viene utilizzato il flag di memoria predefinito D3DPOOL, il driver di dispositivo determina la posizione in cui viene allocata la memoria per il buffer dei vertici, spesso denominata memoria ottimale del driver. Driver: la memoria ottimale può essere memoria video locale, memoria video non locale o memoria di sistema.

L'impostazione della \_ costante D3DUSAGE SOFTWAREPROCESSING con [**IDirect3DDevice9:: CreateVertexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer) Abilita l'elaborazione dei vertici software sui dati del buffer dei vertici. Questo flag è obbligatorio per l'elaborazione dei vertici software in modalità mista. Non è possibile usare il flag per la modalità di elaborazione dei vertici hardware. I buffer vertex usati con l'elaborazione dei vertici software includono quanto segue:

-   Tutti i flussi di input per [**IDirect3DDevice9::P rocessvertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices).
-   Tutti i flussi di input per [**IDirect3DDevice9::D rawprimitive**](/windows/desktop/api) e [**IDirect3DDevice9::D rawindexedprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive).

Il ragionamento usato per determinare la posizione di memoria, ovvero il sistema o il driver ottimale, per i buffer dei vertici è uguale a quello per le trame. L'elaborazione dei vertici, inclusa la trasformazione e l'illuminazione, nell'hardware funziona meglio quando i buffer dei vertici vengono allocati nella memoria ottimale del driver, mentre l'elaborazione dei vertici software funziona meglio con i buffer dei vertici allocati nella memoria di sistema. Per le trame, la rasterizzazione hardware funziona meglio quando le trame vengono allocate nella memoria ottimale del driver, mentre la rasterizzazione del software funziona meglio con le trame della memoria di sistema.

Microsoft Direct3D 9 supporta l'elaborazione autonoma dei vertici, senza eseguire il rendering di una primitiva con il metodo [**IDirect3DDevice9::P rocessvertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices) . Questa elaborazione di vertici autonomi viene sempre eseguita nel software sul processore host. Per questo motivo, è necessario creare i buffer dei vertici usati come origini impostate con [**IDirect3DDevice9:: SetStreamSource**](/windows/desktop/api) con il \_ flag D3DUSAGE SOFTWAREPROCESSING. La funzionalità fornita da **IDirect3DDevice9::P rocessvertices** è identica a quella dei metodi [**IDirect3DDevice9::D rawprimitive**](/windows/desktop/api) e [**IDirect3DDevice9::D rawindexedprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) durante l'uso dell'elaborazione dei vertici software.

Se l'applicazione esegue la propria elaborazione dei vertici e passa i vertici trasformati, illuminati e ritagliati ai metodi di rendering, l'applicazione può scrivere direttamente i vertici in un buffer vertex allocato nella memoria ottimale del driver. Questa tecnica impedisce un'operazione di copia ridondante in un secondo momento. Si noti che questa tecnica non funzionerà correttamente se l'applicazione legge i dati da un vertex buffer, perché le operazioni di lettura eseguite dall'host dalla memoria ottimale del driver possono essere molto lente. Pertanto, se l'applicazione deve leggere durante l'elaborazione o scrive i dati nel buffer in modo anomalo, è preferibile scegliere un buffer dei vertici della memoria di sistema.

Quando si usano le funzionalità di elaborazione dei vertici Direct3D (passando i vertici non trasformati ai metodi di rendering del buffer dei vertici), l'elaborazione può essere eseguita in hardware o software a seconda del tipo di dispositivo e dei flag di creazione del dispositivo. È consigliabile allocare i buffer dei vertici nel pool D3DPOOL \_ default per ottenere prestazioni ottimali in quasi tutti i casi. Quando un dispositivo usa l'elaborazione dei vertici hardware, è possibile eseguire alcune ottimizzazioni aggiuntive in base ai flag D3DUSAGE \_ Dynamic e D3DUSAGE \_ WRITEONLY. Per ulteriori informazioni sull'utilizzo di questi flag, vedere IDirect3DDevice9:: CreateVertexBuffer.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Buffer vertici](vertex-buffers.md)
</dt> </dl>

 

 
