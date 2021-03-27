---
title: Come registrare un elenco di comandi
description: In questo argomento viene illustrato come creare e registrare un elenco di comandi.
ms.assetid: f5b90dfb-0b07-432e-813b-1541efbe3de5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 712f48386e0625c58a1f11c122d105064477ca8c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711545"
---
# <a name="how-to-record-a-command-list"></a>Procedura: registrare un elenco di comandi

Un [elenco](overviews-direct3d-11-render-multi-thread-command-list.md) di comandi è un elenco registrato di comandi per il rendering. In questo argomento viene illustrato come creare e registrare un [elenco di comandi](overviews-direct3d-11-render-multi-thread-command-list.md). Usare un elenco di comandi per registrare i comandi di rendering e riprodurli in un secondo momento. Un elenco di comandi è utile per suddividere le attività di rendering tra thread.

**Per registrare un elenco di comandi**

1.  È necessario creare un elenco di comandi da un contesto posticipato, che contiene lo stato del dispositivo e le azioni di rendering. Dato un dispositivo, creare un contesto posticipato chiamando [**ID3D11Device:: CreateDeferredContext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdeferredcontext).

    ```
    HRESULT hr;
    ID3D11DeviceContext* pDeferredContext = NULL;

    hr = g_pd3dDevice->CreateDeferredContext(0, &pDeferredContext);
    ```

    

2.  Usare il contesto posticipato per eseguire il rendering.

    ```
    float ClearColor[4] = { 0.0f, 0.125f, 0.3f, 1.0f };
    pDeferredContext->ClearRenderTargetView( g_pRenderTargetView, ClearColor );
        
    // Add additional rendering commands
    ...
    ```

    

    Questo semplice esempio cancella una destinazione di rendering, ma è possibile aggiungere altri comandi di rendering.

3.  Creare o registrare un elenco di comandi chiamando [**sul ID3D11DeviceContext:: FinishCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-finishcommandlist) e passando un puntatore a un'interfaccia [**ID3D11CommandList**](/windows/desktop/api/D3D11/nn-d3d11-id3d11commandlist) non inizializzata.

    ```
    ID3D11CommandList* pd3dCommandList = NULL;
    HRESULT hr;
    hr = pDeferredContext->FinishCommandList(FALSE, &pd3dCommandList);
    ```

    

    Quando il metodo restituisce un risultato, viene creato un elenco di comandi contenente tutti i comandi di rendering e un'interfaccia viene restituita all'applicazione.

    Il parametro booleano indica al runtime cosa fare con lo stato della pipeline nel contesto posticipato. **True** significa ripristinare lo stato del contesto di dispositivo alla condizione dell'elenco di pre-comandi al termine della registrazione, **false** significa che non modifica lo stato dopo la registrazione. Ciò significa che il contesto di dispositivo rifletterà le modifiche di stato contenute nell'elenco dei comandi.

Per vedere un esempio per la riproduzione di un elenco di comandi, vedere [procedura: riprodurre un elenco di comandi](overviews-direct3d-11-render-multi-thread-command-list-play.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Elenco comandi](overviews-direct3d-11-render-multi-thread-command-list.md)
</dt> <dt>

[Come usare Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




