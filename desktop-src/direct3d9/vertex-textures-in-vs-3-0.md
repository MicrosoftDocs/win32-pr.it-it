---
description: Il modello vertex shader 3,0 supporta la ricerca di trame nel vertex shader usando l'istruzione texldl-vs texture Load.
ms.assetid: 595cb5c0-da12-4fe9-944c-a61d8ed990b4
title: Trame di vertici in vs_3_0 (DirectX HLSL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a4e8e7bbf7e1ae9764fe5b30647f318dfaeb3ba
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747159"
---
# <a name="vertex-textures-in-vs_3_0-directx-hlsl"></a>Trame di vertici in vs \_ 3 \_ 0 (DirectX HLSL)

Il modello vertex shader 3,0 supporta la ricerca di trame nel vertex shader usando l'istruzione [texldl-vs](../direct3dhlsl/texldl---vs.md) texture Load. Il motore Vertex contiene quattro fasi del campionatore di trama, denominate [D3DVERTEXTEXTURESAMPLER0](d3dvertextexturesampler.md), D3DVERTEXTEXTURESAMPLER1, D3DVERTEXTEXTURESAMPLER2 e D3DVERTEXTEXTURESAMPLER3. Sono distinti dal campionatore della mappa di spostamento e dagli esempi di trama nel motore di pixel.

Per eseguire il campionamento delle trame in queste quattro fasi, è possibile usare il motore di Vertex e programmare le fasi con il metodo [**CheckDeviceFormat**](/windows/desktop/api) . Impostare le trame in tali fasi usando la [**trama**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture)con l'indice della fase [D3DVERTEXTEXTURESAMPLER0](d3dvertextexturesampler.md) tramite D3DVERTEXTEXTURESAMPLER3. Nel vertex shader è stato introdotto un nuovo registro, ovvero il registro del campionatore, come in PS \_ 2 \_ 0, che rappresenta il campionatore di trame dei vertici. Questo registro deve essere definito nello shader prima di usarlo.

Un'applicazione può eseguire una query se un formato è supportato come trama del vertice chiamando [**CheckDeviceFormat**](/windows/desktop/api) con [D3DUSAGE \_ query \_ VERTEXTEXTURE](d3dusage-query.md).

> [!Note]  
> Si tratta di un flag di query in modo che non venga accettato in alcuna funzione CreateXXX. Una trama del vertice creata nel pool predefinito può essere impostata come trama in pixel e viceversa. Tuttavia, per usare l'elaborazione dei vertici software, è necessario creare la trama del vertice nel pool di Scratch (indipendentemente dal fatto che si tratta di un dispositivo in modalità mista o di un dispositivo di elaborazione dei vertici software).

 

La funzionalità è identica alle trame in pixel, ad eccezione di quanto segue:

-   Il filtro di trama anisotropico non è supportato, di conseguenza D3DSAMP \_ MAXANISOTROPY viene ignorato e \_ non è possibile impostare D3DTEXF anisotropico per ingrandire o minimizzare per queste fasi.
-   La frequenza delle informazioni sulle modifiche non è disponibile, di conseguenza l'applicazione deve calcolare il livello di dettaglio e fornire tali informazioni come parametro a [texldl-vs](../direct3dhlsl/texldl---vs.md).

Tali restrizioni includono:

-   Come nei pixel shader, se sono supportate le trame a più elementi, \_ viene usato D3DSAMP ELEMENTINDEX per determinare l'elemento da campionare.
-   Lo stato D3DSAMP \_ DMAPOFFSET viene ignorato per queste fasi.
-   Usare [**CheckDeviceFormat**](/windows/desktop/api) con [D3DUSAGE \_ query \_ VERTEXTEXTURE "](d3dusage-query.md) per eseguire una query su una trama per verificare se può essere usata come trama del vertice.
-   VertexTextureFilterCaps indica il tipo di filtro consentito nei campioni di trama dei vertici. [D3DPTFILTERCAPS \_ MINFANISOTROPIC](d3dptfiltercaps.md) e D3DPTFILTERCAPS \_ MAGFANISOTROPIC non sono consentiti.

## <a name="sampling-stage-registers"></a>Registri fasi di campionamento

Un registro della fase di campionamento identifica un'unità di campionamento che può essere usata nelle istruzioni per il caricamento di trame. Un'unità di campionamento corrisponde alla fase di campionamento della trama, che incapsula lo stato specifico del campionamento fornito in [**SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate).

Ogni campionatore identifica in modo univoco una singola superficie di trama impostata sul campionatore corrispondente usando la [**texture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture). Tuttavia, la stessa superficie di trama può essere impostata su più Sampler.

In fase di disegnare non è possibile impostare contemporaneamente una trama come destinazione di rendering e una trama in una fase.

Poiché vs \_ 3 \_ 0 supporta quattro campionatori, è possibile leggere fino a quattro superfici di trama in un unico passaggio dello shader. Un registro campionatore può apparire solo come argomento nell'istruzione Load di trama: [texldl-vs](../direct3dhlsl/texldl---vs.md).

In vs \_ 3 \_ 0, se si usa un campionatore, è necessario dichiararlo all'inizio del programma shader, usando [DCL \_ samplerType (SM3-vs ASM)](../direct3dhlsl/dcl-samplertype---vs.md) (come in PS \_ 2 \_ 0).

## <a name="software-processing"></a>Elaborazione software

Questa funzionalità sarà supportata nell'elaborazione dei vertici software. I tipi di filtro specifici supportati possono essere controllati chiamando [**GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) e controllando VertexTextureFilterCaps. Tutti i formati di trama pubblicati saranno supportati come trame di vertici nell'elaborazione dei vertici software.

Le applicazioni possono verificare se un particolare formato di trama è supportato nella modalità di elaborazione dei vertici software chiamando [**CheckDeviceFormat**](/windows/desktop/api) e specificando (D3DVERTEXTEXTURESAMPLER \| [**D3DUSAGE \_ SOFTWAREPROCESSING**](d3dusage.md)) come utilizzo. Tutti i formati sono supportati per l'elaborazione dei vertici software. Il pool di Scratch è necessario per l'elaborazione dei vertici software.

## <a name="api-changes"></a>Modifiche API


```
   
// New define
#define D3DVERTEXTEXTURESAMPLER0 (D3DDMAPSAMPLER+1)
#define D3DVERTEXTEXTURESAMPLER1 (D3DDMAPSAMPLER+2)
#define D3DVERTEXTEXTURESAMPLER2 (D3DDMAPSAMPLER+3)
#define D3DVERTEXTEXTURESAMPLER3 (D3DDMAPSAMPLER+4)
    

#define D3DVERTEXTEXTURESAMPLER  (0x00100000L)

// New caps field in D3DCAPS9
DWORD VertexTextureFilterCaps;
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Pipeline Vertex](vertex-pipeline.md)
</dt> </dl>

 

 
