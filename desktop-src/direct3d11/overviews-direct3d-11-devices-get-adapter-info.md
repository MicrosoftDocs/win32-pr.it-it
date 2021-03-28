---
title: Come ottenere le modalità di visualizzazione degli adapter
description: In questo argomento viene illustrato come utilizzare Microsoft DirectX Graphics Infrastructure (DXGI) per ottenere le modalità di visualizzazione valide associate a un adapter.
ms.assetid: 3d182f29-48d4-4e25-b34e-b424cc9eed0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63c2602fcd4e1baa4476bb89273eda676f444e38
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337574"
---
# <a name="how-to-get-adapter-display-modes"></a><span data-ttu-id="d7b1b-103">Procedura: ottenere le modalità di visualizzazione dell'adapter</span><span class="sxs-lookup"><span data-stu-id="d7b1b-103">How To: Get Adapter Display Modes</span></span>

<span data-ttu-id="d7b1b-104">In questo argomento viene illustrato come utilizzare Microsoft DirectX Graphics Infrastructure (DXGI) per ottenere le modalità di visualizzazione valide associate a un adapter.</span><span class="sxs-lookup"><span data-stu-id="d7b1b-104">This topic shows how to use Microsoft DirectX Graphics Infrastructure (DXGI) to get the valid display modes associated with an adapter.</span></span> <span data-ttu-id="d7b1b-105">DirectX 10 e 11 possono usare DXGI per ottenere le modalità di visualizzazione valide.</span><span class="sxs-lookup"><span data-stu-id="d7b1b-105">DirectX 10 and 11 can use DXGI to get the valid display modes.</span></span> <span data-ttu-id="d7b1b-106">Conoscere le modalità di visualizzazione valide garantisce che l'applicazione possa scegliere correttamente una modalità a schermo intero valida.</span><span class="sxs-lookup"><span data-stu-id="d7b1b-106">Knowing the valid display modes ensures that your application can properly choose a valid full-screen mode.</span></span>

<span data-ttu-id="d7b1b-107">**Per ottenere le modalità di visualizzazione dell'adapter**</span><span class="sxs-lookup"><span data-stu-id="d7b1b-107">**To get adapter display modes**</span></span>

1.  <span data-ttu-id="d7b1b-108">Creare un oggetto [**IDXGIFactory**](/windows/desktop/api/dxgi/nn-dxgi-idxgifactory) e usarlo per enumerare gli adapter disponibili.</span><span class="sxs-lookup"><span data-stu-id="d7b1b-108">Create an [**IDXGIFactory**](/windows/desktop/api/dxgi/nn-dxgi-idxgifactory) object and use it to enumerate the available adapters.</span></span> <span data-ttu-id="d7b1b-109">Per altre informazioni, vedere [procedura: enumerare gli adapter](overviews-direct3d-11-devices-enum.md).</span><span class="sxs-lookup"><span data-stu-id="d7b1b-109">For more information, see [How To: Enumerate Adapters](overviews-direct3d-11-devices-enum.md).</span></span>
2.  <span data-ttu-id="d7b1b-110">Chiamare IDXGIAdapter:: EnumOutputs per enumerare gli output per ogni adapter.</span><span class="sxs-lookup"><span data-stu-id="d7b1b-110">Call IDXGIAdapter::EnumOutputs to enumerate the outputs for each adapter.</span></span>
    ```
    IDXGIOutput* pOutput = NULL; 
    HRESULT hr;

    hr = pAdapter->EnumOutputs(0,&pOutput);
    ```

    

3.  <span data-ttu-id="d7b1b-111">Chiamare IDXGIOutput:: GetDisplayModeList per recuperare una matrice di [**strutture \_ \_ DESC in modalità DXGI**](/previous-versions/windows/desktop/legacy/bb173064(v=vs.85)) e il numero di elementi nella matrice.</span><span class="sxs-lookup"><span data-stu-id="d7b1b-111">Call IDXGIOutput::GetDisplayModeList to retrieve an array of [**DXGI\_MODE\_DESC**](/previous-versions/windows/desktop/legacy/bb173064(v=vs.85)) structures and the number of elements in the array.</span></span> <span data-ttu-id="d7b1b-112">Ogni **struttura \_ \_ desc della modalità DXGI** rappresenta una modalità di visualizzazione valida per l'output.</span><span class="sxs-lookup"><span data-stu-id="d7b1b-112">Each **DXGI\_MODE\_DESC** structure represents a valid display mode for the output.</span></span>
    ```
    UINT numModes = 0;
    DXGI_MODE_DESC* displayModes = NULL;
    DXGI_FORMAT format = DXGI_FORMAT_R32G32B32A32_FLOAT;

        // Get the number of elements
        hr = pOutput->GetDisplayModeList( format, 0, &numModes, NULL);

        displayModes = new DXGI_MODE_DESC[numModes]; 

        // Get the list
        hr = pOutput->GetDisplayModeList( format, 0, &numModes, displayModes);
    ```

    

## <a name="related-topics"></a><span data-ttu-id="d7b1b-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d7b1b-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d7b1b-114">Dispositivi</span><span class="sxs-lookup"><span data-stu-id="d7b1b-114">Devices</span></span>](overviews-direct3d-11-devices.md)
</dt> <dt>

[<span data-ttu-id="d7b1b-115">Come usare Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="d7b1b-115">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> </dl>

 

 