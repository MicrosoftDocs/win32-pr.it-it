---
description: Gestione delle risorse è il processo in cui le risorse vengono promosse dall'archiviazione di memoria di sistema ad archiviazione accessibile dal dispositivo ed eliminate dall'archiviazione accessibile dal dispositivo.
ms.assetid: 4aa55313-b86c-48e7-829a-a0917c2ebae7
title: Gestione delle risorse (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30ef7a8be0e71c652b6e3f2ed467e866fd922791
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104225374"
---
# <a name="managing-resources-direct3d-9"></a>Gestione delle risorse (Direct3D 9)

Gestione delle risorse è il processo in cui le risorse vengono promosse dall'archiviazione di memoria di sistema ad archiviazione accessibile dal dispositivo ed eliminate dall'archiviazione accessibile dal dispositivo. Il tempo di esecuzione Direct3D dispone di un proprio algoritmo di gestione basato su una tecnica di priorità meno recente. Direct3D passa a una tecnica di priorità usata più di recente quando rileva che un maggior numero di risorse rispetto a quelle che possono coesistere nella memoria accessibile dal dispositivo viene usato in un singolo frame, tra [**IDirect3DDevice9:: BeginScene**](/windows/desktop/api) e [**IDirect3DDevice9:: EndScene**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endscene) chiamate.

Usare il [**flag \_ predefinito D3DPOOL**](./d3dpool.md) al momento della creazione per specificare che una risorsa è posizionata nel pool di memoria più appropriato per il set di utilizzi richiesti per la risorsa specificata. Si tratta in genere di memoria video, che include sia la memoria video locale che la memoria Accelerated Graphics Port (AGP). Le risorse nel pool predefinito non vengono mantenute attraverso le transizioni tra gli stati persi e operativi del dispositivo. Queste risorse devono essere rilasciate prima di chiamare Reset e devono quindi essere ricreate.

Usare il [**flag \_ gestito D3DPOOL**](./d3dpool.md) al momento della creazione per specificare una risorsa gestita. Le risorse gestite vengono mantenute attraverso le transizioni tra gli stati persi e operativi del dispositivo. Queste risorse sono disponibili sia nella memoria video che nella memoria di sistema. Una risorsa gestita verrà copiata nella memoria video quando necessario durante il rendering. Il dispositivo può essere ripristinato con una chiamata a [**IDirect3DDevice9:: Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)e tali risorse continuano a funzionare normalmente senza essere ricaricate con i dati. Tuttavia, se il dispositivo deve essere eliminato e ricreato, è necessario ricreare tutte le risorse.

La gestione delle risorse non è consigliata per le risorse che cambiano con frequenza elevata. Ad esempio, i buffer vertex e index usati per attraversare un grafico della scena ogni frame che esegue il rendering della geometria visibile all'utente cambia ogni frame. Poiché le risorse gestite sono supportate dalla memoria di sistema, le modifiche costanti devono essere aggiornate nella memoria di sistema, il che può causare un peggioramento delle prestazioni. Per questo scenario specifico, è necessario usare [**D3DPOOL \_ default**](./d3dpool.md) insieme a [**D3DUSAGE \_ Dynamic**](d3dusage.md) .

Un altro esempio per cui la gestione delle risorse non è consigliata e non è consentita in modo esplicito dal runtime è la gestione di una trama creata con [**D3DUSAGE \_ RENDERTARGET**](d3dusage.md). Se la memoria utilizzata dalle destinazioni di rendering è stata gestita dal runtime, è necessario che il relativo contenuto venga costantemente copiato nella memoria di sistema durante il rendering, causando un notevole calo delle prestazioni. Per questo motivo, è necessario creare le destinazioni di rendering nel pool predefinito. Se è necessario l'accesso alla CPU dei dati contenuti in una destinazione di rendering, i dati devono essere copiati in una risorsa creata in [**D3DPOOL \_ SYSTEMMEM**](./d3dpool.md) con [**IDirect3DDevice9:: UpdateTexture**](/windows/desktop/api)o [**IDirect3DDevice9:: UpdateSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface)

Per altre informazioni sullo stato di smarrimento di un dispositivo, vedere [dispositivi persi (Direct3D 9)](lost-devices.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Risorse Direct3D](direct3d-resources.md)
</dt> </dl>

 

 
