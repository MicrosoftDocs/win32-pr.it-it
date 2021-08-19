---
description: La gestione delle risorse è il processo in cui le risorse vengono promosse dall'archiviazione della memoria di sistema all'archiviazione accessibile dal dispositivo e rimosse dall'archiviazione accessibile dal dispositivo.
ms.assetid: 4aa55313-b86c-48e7-829a-a0917c2ebae7
title: Gestione delle risorse (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b860f1c394de932f167de94a3552315b1b70396e9900fccc079ab09142c9e31c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117728464"
---
# <a name="managing-resources-direct3d-9"></a>Gestione delle risorse (Direct3D 9)

La gestione delle risorse è il processo in cui le risorse vengono promosse dall'archiviazione della memoria di sistema all'archiviazione accessibile dal dispositivo e rimosse dall'archiviazione accessibile dal dispositivo. Il tempo di esecuzione Direct3D ha un proprio algoritmo di gestione basato su una tecnica di priorità usata meno di recente. Direct3D passa a una tecnica di priorità usata più di recente quando rileva che più risorse di quelle che possono coesistere nella memoria accessibile dal dispositivo vengono usate in un singolo frame, tra le chiamate [**IDirect3DDevice9::BeginScene**](/windows/desktop/api) e [**IDirect3DDevice9::EndScene.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endscene)

Usare il flag [**D3DPOOL \_ DEFAULT**](./d3dpool.md) al momento della creazione per specificare che una risorsa viene inserita nel pool di memoria più appropriato per il set di utilizzi richiesti per la risorsa specificata. Si tratta in genere di memoria video, inclusa la memoria video locale e la memoria AGP (Accelerated Graphics Port). Le risorse nel pool predefinito non vengono mantenute tramite transizioni tra gli stati di perdita e operativi del dispositivo. Queste risorse devono essere rilasciate prima di chiamare reset e quindi devono essere ri create di nuovo.

Usare il flag [**D3DPOOL \_ MANAGED**](./d3dpool.md) al momento della creazione per specificare una risorsa gestita. Le risorse gestite vengono mantenute tramite transizioni tra lo stato perso e quello operativo del dispositivo. Queste risorse esistono sia nella memoria video che nella memoria di sistema. Una risorsa gestita verrà copiata nella memoria video quando è necessaria durante il rendering. Il dispositivo può essere ripristinato con una chiamata a [**IDirect3DDevice9::Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)e tali risorse continuano a funzionare normalmente senza essere ricaricate con i dati. Tuttavia, se il dispositivo deve essere eliminato e ri-creato, tutte le risorse devono essere ri create di nuovo.

La gestione delle risorse non è consigliata per le risorse che cambiano con frequenza elevata. Ad esempio, i buffer dei vertici e degli indici usati per attraversare un grafico della scena ogni fotogramma che esegue il rendering solo della geometria visibile all'utente cambia ogni fotogramma. Poiché le risorse gestite sono supportate dalla memoria di sistema, le modifiche costanti devono essere aggiornate nella memoria di sistema, causando una grave riduzione delle prestazioni. Per questo scenario specifico, è consigliabile usare [**D3DPOOL \_ DEFAULT**](./d3dpool.md) insieme [**a D3DUSAGE \_ DYNAMIC.**](d3dusage.md)

Un altro esempio per cui la gestione delle risorse non è consigliata (e non esplicitamente consentita dal runtime) è la gestione di una trama creata con [**D3DUSAGE \_ RENDERTARGET.**](d3dusage.md) Se la memoria usata dalle destinazioni di rendering fosse gestita dal runtime, il relativo contenuto deve essere costantemente copiato nella memoria di sistema durante il rendering, causando un elevato livello di riduzione delle prestazioni. Per questo motivo, le destinazioni di rendering devono essere create nel pool predefinito. Se è necessario l'accesso alla CPU dei dati contenuti in una destinazione di rendering, i dati devono essere copiati in una risorsa creata in [**D3DPOOL \_ SYSTEMMEM**](./d3dpool.md) [**usando IDirect3DDevice9::UpdateTexture**](/windows/desktop/api)o [**IDirect3DDevice9::UpdateSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface)

Per altre informazioni sullo stato perso di un dispositivo, vedere [Dispositivi persi (Direct3D 9).](lost-devices.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Risorse Direct3D](direct3d-resources.md)
</dt> </dl>

 

 
