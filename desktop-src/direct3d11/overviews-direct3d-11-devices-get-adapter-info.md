---
title: Come ottenere le modalità di visualizzazione dell'adapter
description: Questo argomento illustra come usare Microsoft DirectX Graphic Infrastructure (DXGI) per ottenere le modalità di visualizzazione valide associate a un adattatore.
ms.assetid: 3d182f29-48d4-4e25-b34e-b424cc9eed0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 921d373a9ff0f79baaf848a55cbab0d08fd4e119d30a0a0cb917832830589dfa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119571"
---
# <a name="how-to-get-adapter-display-modes"></a>Procedura: Ottenere le modalità di visualizzazione dell'adapter

Questo argomento illustra come usare Microsoft DirectX Graphic Infrastructure (DXGI) per ottenere le modalità di visualizzazione valide associate a un adattatore. DirectX 10 e 11 possono usare DXGI per ottenere le modalità di visualizzazione valide. Conoscere le modalità di visualizzazione valide garantisce che l'applicazione possa scegliere correttamente una modalità a schermo intero valida.

**Per ottenere le modalità di visualizzazione dell'adattatore**

1.  Creare un [**oggetto IDXGIFactory**](/windows/desktop/api/dxgi/nn-dxgi-idxgifactory) e usarlo per enumerare gli adattatori disponibili. Per altre informazioni, vedere [Procedura: Enumerare gli adapter.](overviews-direct3d-11-devices-enum.md)
2.  Chiamare IDXGIAdapter::EnumOutputs per enumerare gli output per ogni adapter.
    ```
    IDXGIOutput* pOutput = NULL; 
    HRESULT hr;

    hr = pAdapter->EnumOutputs(0,&pOutput);
    ```

    

3.  Chiamare IDXGIOutput::GetDisplayModeList per recuperare una matrice di strutture [**\_ \_ DESC DXGI MODE**](/previous-versions/windows/desktop/legacy/bb173064(v=vs.85)) e il numero di elementi nella matrice. Ogni **struttura \_ DXGI MODE \_ DESC** rappresenta una modalità di visualizzazione valida per l'output.
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

 

 