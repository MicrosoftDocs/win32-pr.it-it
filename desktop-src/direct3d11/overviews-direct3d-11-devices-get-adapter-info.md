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
# <a name="how-to-get-adapter-display-modes"></a>Procedura: ottenere le modalità di visualizzazione dell'adapter

In questo argomento viene illustrato come utilizzare Microsoft DirectX Graphics Infrastructure (DXGI) per ottenere le modalità di visualizzazione valide associate a un adapter. DirectX 10 e 11 possono usare DXGI per ottenere le modalità di visualizzazione valide. Conoscere le modalità di visualizzazione valide garantisce che l'applicazione possa scegliere correttamente una modalità a schermo intero valida.

**Per ottenere le modalità di visualizzazione dell'adapter**

1.  Creare un oggetto [**IDXGIFactory**](/windows/desktop/api/dxgi/nn-dxgi-idxgifactory) e usarlo per enumerare gli adapter disponibili. Per altre informazioni, vedere [procedura: enumerare gli adapter](overviews-direct3d-11-devices-enum.md).
2.  Chiamare IDXGIAdapter:: EnumOutputs per enumerare gli output per ogni adapter.
    ```
    IDXGIOutput* pOutput = NULL; 
    HRESULT hr;

    hr = pAdapter->EnumOutputs(0,&pOutput);
    ```

    

3.  Chiamare IDXGIOutput:: GetDisplayModeList per recuperare una matrice di [**strutture \_ \_ DESC in modalità DXGI**](/previous-versions/windows/desktop/legacy/bb173064(v=vs.85)) e il numero di elementi nella matrice. Ogni **struttura \_ \_ desc della modalità DXGI** rappresenta una modalità di visualizzazione valida per l'output.
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

    

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Dispositivi](overviews-direct3d-11-devices.md)
</dt> <dt>

[Come usare Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 