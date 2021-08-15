---
description: Il modello vertex shader 3.0 supporta la ricerca di trame nel vertex shader usando l'istruzione texldl - vs texture load.
ms.assetid: 595cb5c0-da12-4fe9-944c-a61d8ed990b4
title: Vertex Textures in vs_3_0 (DirectX HLSL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4cbd4aa1e1830d29656fea2bc7b028191bee158eede119c9a47ae2457d10e99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118519448"
---
# <a name="vertex-textures-in-vs_3_0-directx-hlsl"></a>Vertex Textures in vs \_ 3 \_ 0 (DirectX HLSL)

Il modello vertex shader 3.0 supporta la ricerca di trame nel vertex shader usando l'istruzione [texldl - vs](../direct3dhlsl/texldl---vs.md) texture load. Il motore dei vertici contiene quattro fasi del campionatore di trama, denominate [D3DVERTEXTEXTURESAMPLER0,](d3dvertextexturesampler.md)D3DVERTEXTEXTURESAMPLER1, D3DVERTEXTEXTURESAMPLER2 e D3DVERTEXTEXTURESAMPLER3. Si differenziano dal campionatore della mappa di spostamento e dai campionatori di trama nel motore pixel.

Per campionare le trame impostate in queste quattro fasi, è possibile usare il motore dei vertici e programmare le fasi con il [**metodo CheckDeviceFormat.**](/windows/desktop/api) Impostare le trame in queste fasi usando [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture), con l'indice della fase [da D3DVERTEXTEXTURESAMPLER0](d3dvertextexturesampler.md) a D3DVERTEXTEXTURESAMPLER3. È stato introdotto un nuovo registro nel vertex shader, il registro del campionatore (come in ps \_ 2 0), che rappresenta il campionatore di \_ trama dei vertici. Questo registro deve essere definito nello shader prima di usarlo.

Un'applicazione può eseguire una query se un formato è supportato come trama vertice chiamando [**CheckDeviceFormat**](/windows/desktop/api) con [D3DUSAGE \_ QUERY \_ VERTEXTEXTURE.](d3dusage-query.md)

> [!Note]  
> Si tratta di un flag di query, pertanto non viene accettato in alcuna funzione Createxxx. Una trama vertice creata nel pool predefinito può essere impostata come trama in pixel e viceversa. Tuttavia, per usare l'elaborazione dei vertici software, è necessario creare la trama dei vertici nel pool di file scratch, indipendentemente dal fatto che si tratta di un dispositivo in modalità mista o di un dispositivo di elaborazione dei vertici software.

 

La funzionalità è identica alle trame pixel, ad eccezione delle seguenti:

-   Il filtro anisotropo delle trame non è supportato, quindi D3DSAMP MAXANISOTROPY viene ignorato e \_ D3DTEXF ANISOTROP non può essere impostato per la ingrandimento o la minimizione per \_ queste fasi.
-   La frequenza delle informazioni sulle modifiche non è disponibile, quindi l'applicazione deve calcolare il livello di dettaglio e fornire le informazioni come parametro a [texldl - rispetto a](../direct3dhlsl/texldl---vs.md).

Tali restrizioni includono:

-   Come per i pixel shader, se sono supportate trame a più elementi, per determinare l'elemento da cui eseguire il campionamento viene usato ELEMENTINDEX D3DSAMP. \_
-   Lo stato D3DSAMP \_ DMAPOFFSET viene ignorato per queste fasi.
-   Usare [**CheckDeviceFormat**](/windows/desktop/api) con [D3DUSAGE \_ QUERY \_ VERTEXTEXTURE"](d3dusage-query.md) per eseguire una query su una trama per verificare se può essere usata come trama vertice.
-   VertexTextureFilterCaps indica il tipo di filtri consentiti nei campionatori di trama dei vertici. [D3DPTFILTERCAPS \_ MINFANISOTROP](d3dptfiltercaps.md) e D3DPTFILTERCAPS \_ MAGFANISOTROP non sono consentiti.

## <a name="sampling-stage-registers"></a>Registri delle fasi di campionamento

Un registro di fase di campionamento identifica un'unità di campionamento che può essere usata nelle istruzioni di caricamento della trama. Un'unità di campionamento corrisponde alla fase di campionamento della trama, incapsulando lo stato specifico del campionamento fornito in [**SetSamplerState.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate)

Ogni campionatore identifica in modo univoco una singola superficie di trama impostata sul campionatore corrispondente usando [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture). Tuttavia, la stessa superficie di trama può essere impostata su più campionatori.

In fase di disegno, una trama non può essere impostata contemporaneamente come destinazione di rendering e come trama in una fase.

Poiché vs 3 0 supporta quattro campionatori, è possibile leggere fino a quattro superfici di trama \_ in un singolo passaggio dello \_ shader. Un registro sampler potrebbe essere visualizzato solo come argomento nell'istruzione di caricamento della trama: [texldl - vs](../direct3dhlsl/texldl---vs.md).

In vs 3 0, se si usa un campionatore, deve essere dichiarato all'inizio del programma shader, usando \_ \_ [dcl \_ samplerType (sm3 - vs asm)](../direct3dhlsl/dcl-samplertype---vs.md) (come in ps \_ 2 \_ 0).

## <a name="software-processing"></a>Elaborazione software

Questa funzionalità sarà supportata nell'elaborazione dei vertici software. I tipi di filtro specifici supportati possono essere controllati chiamando [**GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) e controllando VertexTextureFilterCaps. Tutti i formati di trama pubblicati saranno supportati come trame dei vertici nell'elaborazione dei vertici software.

Le applicazioni possono verificare se un particolare formato di trama è supportato nella modalità di elaborazione dei vertici software chiamando [**CheckDeviceFormat**](/windows/desktop/api) e specificando (D3DVERTEXTEXTURESAMPLER \| [**D3DUSAGE \_ SOFTWAREPROCESSING)**](d3dusage.md)come utilizzo. Tutti i formati sono supportati per l'elaborazione dei vertici software. Il pool di file scratch è necessario per l'elaborazione dei vertici software.

## <a name="api-changes"></a>Modifiche all'API


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

[Vertex Pipeline](vertex-pipeline.md)
</dt> </dl>

 

 
