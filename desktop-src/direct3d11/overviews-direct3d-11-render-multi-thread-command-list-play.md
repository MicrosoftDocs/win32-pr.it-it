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
# <a name="how-to-play-back-a-command-list"></a><span data-ttu-id="bb558-103">Procedura: riprodurre un elenco di comandi</span><span class="sxs-lookup"><span data-stu-id="bb558-103">How to: Play Back a Command List</span></span>

<span data-ttu-id="bb558-104">Un [elenco](overviews-direct3d-11-render-multi-thread-command-list.md) di comandi è un elenco registrato di comandi per il rendering.</span><span class="sxs-lookup"><span data-stu-id="bb558-104">A [command list](overviews-direct3d-11-render-multi-thread-command-list.md) is a recorded list of rendering commands.</span></span> <span data-ttu-id="bb558-105">Usare un elenco di comandi per pre-registrare i comandi di disegno e riprodurli in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="bb558-105">Use a command list to pre-record drawing commands and play them back later.</span></span> <span data-ttu-id="bb558-106">In questo argomento viene illustrato come riprodurre un [elenco di comandi](overviews-direct3d-11-render-multi-thread-command-list.md).</span><span class="sxs-lookup"><span data-stu-id="bb558-106">This topic shows how to play back a [command list](overviews-direct3d-11-render-multi-thread-command-list.md).</span></span> <span data-ttu-id="bb558-107">È possibile utilizzare un elenco di comandi per suddividere le attività di rendering tra thread.</span><span class="sxs-lookup"><span data-stu-id="bb558-107">A command list can be used to split rendering tasks between threads.</span></span>

<span data-ttu-id="bb558-108">In questa sezione viene descritto come riprodurre un elenco di comandi.</span><span class="sxs-lookup"><span data-stu-id="bb558-108">This section describes how to play back a command list.</span></span> <span data-ttu-id="bb558-109">Per la registrazione di un elenco di comandi, vedere [procedura: registrare un elenco di comandi](overviews-direct3d-11-render-multi-thread-command-list-record.md).</span><span class="sxs-lookup"><span data-stu-id="bb558-109">For recording a command list, see [How to: Record a Command List](overviews-direct3d-11-render-multi-thread-command-list-record.md).</span></span>

<span data-ttu-id="bb558-110">**Per riprodurre un elenco di comandi**</span><span class="sxs-lookup"><span data-stu-id="bb558-110">**To play back a command list**</span></span>

-   <span data-ttu-id="bb558-111">Chiamare [**sul ID3D11DeviceContext:: ExecuteCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-executecommandlist) e passare un oggetto [**ID3D11CommandList**](/windows/desktop/api/D3D11/nn-d3d11-id3d11commandlist) valido.</span><span class="sxs-lookup"><span data-stu-id="bb558-111">Call [**ID3D11DeviceContext::ExecuteCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-executecommandlist) and pass a valid [**ID3D11CommandList**](/windows/desktop/api/D3D11/nn-d3d11-id3d11commandlist) object.</span></span>
    ```
    if(g_pd3dCommandList)
    {
        g_pImmediateContext->ExecuteCommandList(g_pd3dCommandList, TRUE);
    }
    ```

    

<span data-ttu-id="bb558-112">[**ExecuteCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-executecommandlist) deve essere eseguito nel [contesto immediato](overviews-direct3d-11-devices-intro.md) per i comandi registrati da eseguire nell'unità di elaborazione grafica (GPU).</span><span class="sxs-lookup"><span data-stu-id="bb558-112">[**ExecuteCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-executecommandlist) must be executed on the [immediate context](overviews-direct3d-11-devices-intro.md) for recorded commands to be run on the graphics processing unit (GPU).</span></span> <span data-ttu-id="bb558-113">Usare il contesto immediato per inviare i comandi alla GPU per l'esecuzione, usare un contesto posticipato per registrare i comandi per la riproduzione in un altro elenco di comandi.</span><span class="sxs-lookup"><span data-stu-id="bb558-113">Use the immediate context to feed commands to the GPU for execution, use a deferred context to record commands for playback onto another command list.</span></span> <span data-ttu-id="bb558-114">Quando si chiama **ExecuteCommandList** in un altro contesto posticipato, viene creato un elenco di comandi posticipato "merge".</span><span class="sxs-lookup"><span data-stu-id="bb558-114">When you call **ExecuteCommandList** onto another deferred context, you create a ‘merged’ deferred command list.</span></span> <span data-ttu-id="bb558-115">Per eseguire i comandi nell'elenco dei comandi posticipati Uniti, è necessario eseguirli nel contesto immediato.</span><span class="sxs-lookup"><span data-stu-id="bb558-115">To run the commands on the merged deferred command list, you need to execute them on the immediate context.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bb558-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bb558-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bb558-117">Elenco comandi</span><span class="sxs-lookup"><span data-stu-id="bb558-117">Command List</span></span>](overviews-direct3d-11-render-multi-thread-command-list.md)
</dt> <dt>

[<span data-ttu-id="bb558-118">Come usare Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="bb558-118">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




