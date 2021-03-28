---
title: Come riprodurre un elenco di comandi
description: In questo argomento viene illustrato come riprodurre un elenco di comandi.
ms.assetid: 4e6c0a98-85ff-45ca-963b-7d5c55f47195
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d04df73b481adea17e1f985e2c1851039fd016a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104992800"
---
# <a name="how-to-play-back-a-command-list"></a>Procedura: riprodurre un elenco di comandi

Un [elenco](overviews-direct3d-11-render-multi-thread-command-list.md) di comandi è un elenco registrato di comandi per il rendering. Usare un elenco di comandi per pre-registrare i comandi di disegno e riprodurli in un secondo momento. In questo argomento viene illustrato come riprodurre un [elenco di comandi](overviews-direct3d-11-render-multi-thread-command-list.md). È possibile utilizzare un elenco di comandi per suddividere le attività di rendering tra thread.

In questa sezione viene descritto come riprodurre un elenco di comandi. Per la registrazione di un elenco di comandi, vedere [procedura: registrare un elenco di comandi](overviews-direct3d-11-render-multi-thread-command-list-record.md).

**Per riprodurre un elenco di comandi**

-   Chiamare [**sul ID3D11DeviceContext:: ExecuteCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-executecommandlist) e passare un oggetto [**ID3D11CommandList**](/windows/desktop/api/D3D11/nn-d3d11-id3d11commandlist) valido.
    ```
    if(g_pd3dCommandList)
    {
        g_pImmediateContext->ExecuteCommandList(g_pd3dCommandList, TRUE);
    }
    ```

    

[**ExecuteCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-executecommandlist) deve essere eseguito nel [contesto immediato](overviews-direct3d-11-devices-intro.md) per i comandi registrati da eseguire nell'unità di elaborazione grafica (GPU). Usare il contesto immediato per inviare i comandi alla GPU per l'esecuzione, usare un contesto posticipato per registrare i comandi per la riproduzione in un altro elenco di comandi. Quando si chiama **ExecuteCommandList** in un altro contesto posticipato, viene creato un elenco di comandi posticipato "merge". Per eseguire i comandi nell'elenco dei comandi posticipati Uniti, è necessario eseguirli nel contesto immediato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Elenco comandi](overviews-direct3d-11-render-multi-thread-command-list.md)
</dt> <dt>

[Come usare Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




