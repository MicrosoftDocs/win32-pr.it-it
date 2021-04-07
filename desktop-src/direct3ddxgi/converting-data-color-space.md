---
description: Per comporre sullo schermo o eseguire operazioni a virgola mobile, è necessario lavorare nello spazio dei colori corretto.
ms.assetid: 1DD8E2D3-430F-4EE4-9C41-78736C904920
title: Conversione dei dati per lo spazio colore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91b5dbec2f826c40d5274cbddb3b54d1cdd9f695
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745935"
---
# <a name="converting-data-for-the-color-space"></a>Conversione dei dati per lo spazio colore

Per comporre sullo schermo o eseguire operazioni a virgola mobile, è necessario lavorare nello spazio dei colori corretto. Si consiglia di eseguire operazioni a virgola mobile in uno spazio cromatico lineare. Quindi, per presentare le immagini allo schermo, convertire i dati in uno spazio dei colori standard RGB (sRGB, gamma 2,2-con correzione). La presentazione sullo schermo nello spazio dei colori di sRGB è importante per la precisione dei colori. Se le immagini non sono con correzione di gamma 2,2, allocano troppi bit o troppa larghezza di banda per evidenziare che le persone non possono distinguere, a un numero troppo basso di bit o larghezza di banda per ombreggiare i valori a cui gli utenti sono sensibili e quindi richiedono più bit o larghezza di banda per mantenere la stessa qualità visiva. Pertanto, per garantire la migliore accuratezza del colore, presentare le immagini allo schermo con correzione gamma 2,2.

-   [Accuratezza colore](#color-accuracy)
-   [Argomenti correlati](#related-topics)

## <a name="color-accuracy"></a>Accuratezza colore

Per la presentazione, i formati di visualizzazione con valori integer, ad esempio [**DXGI \_ Format \_ B8G8R8A8 \_ UNORM \_ sRGB**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format), [**DXGI \_ Format \_ R10G10B10 \_ XR \_ Bias \_ a2 \_ UNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)e così via, contengono sempre dati con correzione a gamma di sRGB. I formati di visualizzazione con valori a virgola mobile (attualmente solo [**DXGI \_ Format \_ R16G16B16A16 \_ float**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)) contengono dati a valore lineare.

Il \_ [modificatore di formato](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) sRGB indica al sistema operativo di consentire all'app di inserire i dati sRGB sullo schermo. L'app deve sempre inserire i dati sRGB nei buffer indietro con formati con valori integer per presentare i dati sRGB sullo schermo, anche se i dati non hanno questo modificatore di formato nel nome del formato. Per un elenco completo dei formati di analisi della visualizzazione:

-   [Supporto del formato DXGI per l'hardware a livello di funzionalità Direct3D 12,1](hardware-support-for-direct3d-12-1-formats.md)
-   [Supporto del formato DXGI per l'hardware a livello di funzionalità Direct3D 12,0](hardware-support-for-direct3d-12-0-formats.md)
-   [Supporto del formato DXGI per l'hardware a livello di funzionalità Direct3D 11,1](format-support-for-direct3d-11-1-feature-level-hardware.md)
-   [Supporto del formato DXGI per l'hardware a livello di funzionalità Direct3D 11,0](format-support-for-direct3d-11-0-feature-level-hardware.md)
-   [Supporto hardware per i formati 10Level9 Direct3D](/previous-versions//ff471324(v=vs.85))
-   [Supporto hardware per formati Direct3D 10,1](/previous-versions//cc627091(v=vs.85))
-   [Supporto hardware per i formati Direct3D 10](/previous-versions//cc627090(v=vs.85))

Quando si scrivono valori di output a virgola mobile dal pixel shader in visualizzazioni di destinazione di rendering (**RenderTargetView**) con \_ il [modificatore di formato](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) sRGB associato alla [pipeline](/windows/desktop/direct3d11/overviews-direct3d-11-graphics-pipeline), questi vengono convertiti in uno spazio colore con correzione gamma 2,2. Analogamente, quando si esegue il binding delle visualizzazioni shader-Resource (**ShaderResourceView**) con il \_ modificatore di formato sRGB alla pipeline, si convertono i valori dallo spazio dei colori gamma 2,2 con correzione allo spazio colore lineare quando vengono letti dal **ShaderResourceView**. Lo shader è quindi in grado di eseguire operazioni su di essi.

Ad esempio, usare codice simile al seguente per scrivere i valori di output a virgola mobile da uno shader in un formato **RenderTargetView** :


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



Quando viene restituita la routine ' s', i valori a virgola mobile (1, 0, 0, 1) vengono convertiti nel formato **RenderTargetView** . Quindi, se si assegna il \_ [modificatore di formato](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) sRGB a **RenderTargetView**, viene eseguita la conversione gamma.

Questi sono i passaggi da seguire per assicurarsi che il contenuto visualizzato sullo schermo abbia la massima accuratezza dei colori.

**Per garantire l'accuratezza dei colori nella pipeline**

1.  Se una trama presenta contenuto sRGB, assicurarsi che **ShaderResourceView** disponga del \_ [modificatore di formato](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) sRGB, in modo che, quando si legge da **ShaderResourceView** nello shader, si converta il contenuto della trama dallo spazio colore con correzione gamma 2,2 allo spazio colore lineare.
2.  Verificare che **RenderTargetView** disponga anche del \_ [modificatore di formato](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) sRGB, in modo che i valori di output dello shader siano convertiti in gamma.

Se si seguono i passaggi precedenti, quando si chiama il metodo [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) , il contenuto visualizzato sullo schermo presenta la precisione del colore migliore.

È possibile usare il metodo [**ID3D11Device:: CreateRenderTargetView**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createrendertargetview) per creare visualizzazioni di **\_ formato DXGI \_ \* \_ sRGB** nei buffer indietro da una catena di scambio creata solo con un formato **DXGI \_ formato \_ \* \_ UNORM** . Si tratta di un'eccezione speciale alla regola per la creazione di visualizzazioni di destinazione di rendering, che indica che è possibile usare un formato diverso con **ID3D11Device:: CreateRenderTargetView** solo se è stata creata la risorsa che si vuole visualizzare con il **formato DXGI senza \_ \_ \* \_ tipo**.

Per altre informazioni sulle regole per la conversione dei dati, vedere [regole di conversione dei dati](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-data-conversion).

Per informazioni su come eseguire contemporaneamente la lettura e la scrittura in una trama, vedere [decomprimere e impacchettare il \_ formato DXGI per la modifica dell'immagine In-Place](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-unpacking-packing-dxgi-format).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Miglioramento della presentazione con il modello Flip, i rettangoli Dirty e le aree a scorrimento](dxgi-1-2-presentation-improvements.md)
</dt> </dl>

 

 
