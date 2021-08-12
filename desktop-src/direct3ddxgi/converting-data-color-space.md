---
description: Per comporre sullo schermo o eseguire operazioni a virgola mobile, è necessario lavorare nello spazio colore corretto.
ms.assetid: 1DD8E2D3-430F-4EE4-9C41-78736C904920
title: Conversione dei dati per lo spazio colore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 391d7e1cfd2882603529e28261e6872020dfbb1bbf461a9fd6f5d03efb3aaee3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118289636"
---
# <a name="converting-data-for-the-color-space"></a>Conversione dei dati per lo spazio colore

Per comporre sullo schermo o eseguire operazioni a virgola mobile, è necessario lavorare nello spazio colore corretto. È consigliabile eseguire operazioni a virgola mobile in uno spazio colore lineare. Quindi, per presentare le immagini sullo schermo, convertire i dati in dati RGB standard (sRGB, con correzione gamma 2.2) dello spazio dei colori. La presentazione sullo schermo nello spazio colore sRGB è importante per l'accuratezza del colore. Se le immagini non sono corrette con gamma 2.2, allocano troppi bit o una larghezza di banda troppo elevata per evidenziare che gli utenti non possono distinguere e un numero troppo piccolo di bit o larghezza di banda per nascondere i valori a cui gli utenti sono sensibili e quindi richiedono più bit o larghezza di banda per mantenere la stessa qualità visiva. Pertanto, per garantire la migliore accuratezza del colore, presentare sullo schermo immagini con correzione gamma 2.2.

-   [Accuratezza del colore](#color-accuracy)
-   [Argomenti correlati](#related-topics)

## <a name="color-accuracy"></a>Accuratezza del colore

Per la presentazione, i formati di visualizzazione con valori interi (ad esempio [**DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM \_ SRGB,**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) [**DXGI \_ FORMAT \_ R10G10B10 \_ XR BIAS \_ \_ A2 \_ UNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)e così via) contengono sempre dati con correzione gamma sRGB. I formati di visualizzazione a valori float (attualmente solo [**DXGI \_ FORMAT \_ R16G16B16A16 \_ FLOAT)**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)contengono dati a valori lineari.

Il modificatore di formato SRGB indica al sistema operativo di consentire all'app di inserire i dati \_ sRGB [](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) sullo schermo. L'app deve sempre inserire i dati sRGB nei buffer back con formati con valori interi per presentare i dati sRGB sullo schermo, anche se i dati non hanno questo modificatore di formato nel nome del formato. Per un elenco completo dei formati di analisi della visualizzazione:

-   [Supporto del formato DXGI per l'hardware Direct3D Feature Level 12.1](hardware-support-for-direct3d-12-1-formats.md)
-   [Supporto del formato DXGI per l'hardware Direct3D a livello di funzionalità 12.0](hardware-support-for-direct3d-12-0-formats.md)
-   [Supporto del formato DXGI per l'hardware Direct3D Feature Level 11.1](format-support-for-direct3d-11-1-feature-level-hardware.md)
-   [Supporto del formato DXGI per l'hardware Direct3D a livello di funzionalità 11.0](format-support-for-direct3d-11-0-feature-level-hardware.md)
-   [Supporto hardware per formati Direct3D 10Level9](/previous-versions//ff471324(v=vs.85))
-   [Supporto hardware per i formati Direct3D 10.1](/previous-versions//cc627091(v=vs.85))
-   [Supporto hardware per i formati Direct3D 10](/previous-versions//cc627090(v=vs.85))

Quando si scrivono valori di output a virgola mobile dall'pixel shader nelle visualizzazioni di destinazione di rendering **(RenderTargetView** s) con il modificatore di formato SRGB associato alla pipeline, li si converte nello spazio colore con correzione \_ gamma 2.2. [](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) [](/windows/desktop/direct3d11/overviews-direct3d-11-graphics-pipeline) Analogamente, quando le visualizzazioni shader-risorsa **(ShaderResourceView** s) con il modificatore di formato SRGB sono associate alla pipeline, converti i valori dallo spazio colore corretto gamma 2.2 allo spazio colore lineare quando li leggi dagli oggetti \_ **ShaderResourceView.** Lo shader può quindi eseguire operazioni su di essi.

Ad esempio, usare codice simile al seguente per scrivere valori di output a virgola mobile da uno shader in un **formato RenderTargetView:**


```
struct PSOut
{
    float4 color : SV_Target;
};

PSOut S( PSIn input )
{
    PSOut output;
    output.color = float4( 1.0, 0.0, 0.0, 1.0 );
    return output;
}
```



Quando la routine 'S' viene restituita, i valori a virgola mobile (1, 0, 0, 1) vengono convertiti nel **formato RenderTargetView.** Quindi, se si assegna il modificatore di formato \_ SRGB a **RenderTargetView,** viene eseguita la conversione gamma. [](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)

Questi sono i passaggi da seguire per garantire che il contenuto visualizzato sullo schermo abbia la migliore accuratezza del colore.

**Per garantire l'accuratezza del colore nella pipeline**

1.  Se una trama ha contenuto sRGB, assicurati che **ShaderResourceView** abbia il modificatore di formato SRGB, quindi quando leggi da ShaderResourceView nello shader, converti il contenuto della trama dallo spazio colore corretto gamma \_ [](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) 2.2 allo spazio colore lineare. 
2.  Assicurarsi che **RenderTargetView abbia** anche il modificatore di formato SRGB in modo che i valori di output dello \_ shader siano convertiti in gamma. [](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)

Se si seguono i passaggi precedenti, quando si chiama il metodo [**IDXGISwapChain1::P resent1,**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) il contenuto visualizzato sullo schermo ha la migliore accuratezza del colore.

È possibile usare il metodo [**ID3D11Device::CreateRenderTargetView**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createrendertargetview) per creare visualizzazioni **\_ \_ \* \_ SRGB DXGI FORMAT** nei buffer back da una catena di scambio creata solo con un formato **DXGI \_ FORMAT \_ \* \_ UNORM.** Si tratta di un'eccezione speciale alla regola per la creazione di visualizzazioni di destinazione di rendering, che indica che è possibile usare un formato diverso con **ID3D11Device::CreateRenderTargetView** solo se è stata creata la risorsa che si vuole visualizzare con **DXGI \_ FORMAT \_ \* \_ TYPELESS.**

Per altre informazioni sulle regole per la conversione dei dati, vedere [Regole di conversione dei dati.](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-data-conversion)

Per informazioni su come leggere e scrivere contemporaneamente in una trama, vedi Decompressione e creazione di un pacchetto [DXGI \_ FORMAT](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-unpacking-packing-dxgi-format)per la modifica di In-Place immagini.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Miglioramento della presentazione con il modello di capovolgimento, rettangoli dirty e aree di scorrimento](dxgi-1-2-presentation-improvements.md)
</dt> </dl>

 

 
