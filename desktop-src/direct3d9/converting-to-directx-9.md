---
description: Le funzionalità seguenti sono state modificate in Microsoft Direct3D 9. Se si usano queste funzionalità, vedere le modifiche elencate di seguito per convertire l'applicazione in Direct3D 9.
ms.assetid: 6f5b2cc1-5415-4af8-a964-051a5af42680
title: Conversione a Direct3D 9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fdf5ec812ede4e9d5d356d36b01bbcfcc7732fdb5946e2a13af90c9d9428fc1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119850531"
---
# <a name="converting-to-direct3d-9"></a>Conversione a Direct3D 9

Le funzionalità seguenti sono state modificate in Microsoft Direct3D 9. Se si usano queste funzionalità, vedere le modifiche elencate di seguito per convertire l'applicazione in Direct3D 9.

-   [Modifiche a BaseVertexIndex](#basevertexindex-changes)
-   [Modifiche di CreateImageSurface](#createimagesurface-changes)
-   [D3DENUM \_ NO \_ WHQL \_ LEVEL Changes](/windows)
-   [Creare modifiche alle risorse](#create-resource-changes)
-   [Modifiche a EnumAdapterModes](#enumadaptermodes-changes)
-   [Modifiche di Get/SetStreamSource \_](#getsetstreamsource-changes)
-   [Modifiche di qualità del multicampionamento](#multisampling-quality-changes)
-   [Modifiche a ResourceManagerDiscardBytes](#resourcemanagerdiscardbytes-changes)
-   [SetSoftwareVertexProcessing Changes](#setsoftwarevertexprocessing-changes)
-   [Modifiche al campionatore di trama](#texture-sampler-changes)
-   [Modifiche alla dichiarazione dei vertici](#vertex-declaration-changes)
-   [Modifiche a \_ intervalli \_ e \_ swapeffects](#intervals-and-swapeffects-changes)

## <a name="basevertexindex-changes"></a>Modifiche a BaseVertexIndex

In DirectX 8.x IDirect3DDevice8::SetIndices richiedeva un puntatore all'index buffer e un oggetto BaseVertexIndex per la posizione iniziale nel vertex buffer. Un'applicazione che creava in batch oggetti diversi nel buffer dei vertici doveva cambiare il index buffer (o effettuare una chiamata a IDirect3DDevice8::SetIndices) prima di chiamare IDirect3DDevice8::D rawIndexedPrimitive.

In Direct3D 9 la posizione iniziale nel buffer dei vertici, *BaseVertexIndex,* è stata spostata in IDirect3DDevice9::D rawIndexedPrimitive e il relativo tipo di dati è stato modificato da DWORD a INT.


```
HRESULT IDirect3DDevice9::DrawIndexedPrimitive( 
    D3DPRIMITIVETYPE PrimType, 
    INT BaseVertexIndex, 
    UINT minIndex, 
    UINT NumVertices, 
    UINT startIndex, 
    UINT primCount); 

HRESULT SetIndices(IDirect3DIndexBuffer9* pIndexData); 
```



## <a name="createimagesurface-changes"></a>Modifiche di CreateImageSurface

IDirect3DDevice8::CreateImageSurface è stato rinominato [**CreateOffscreenPlainSurface.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createoffscreenplainsurface) È stato aggiunto un parametro aggiuntivo che accetta un tipo D3DPOOL. D3DPOOL SCRATCH restituirà una superficie con caratteristiche identiche a una superficie \_ creata da IDirect3DDevice8::CreateImageSurface. D3DPOOL \_ DEFAULT è il pool appropriato per l'uso con [**StretchRect**](/windows/desktop/api) [**e ColorFill.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-colorfill)

## <a name="d3denum_no_whql_level-changes"></a>D3DENUM \_ NO \_ WHQL \_ LEVEL Changes

Le applicazioni devono ora richiedere in modo esplicito Microsoft Windows Hardware Quality Labs (WHQL) perché la risposta richiede relativamente tempo (pochi secondi). D3DENUM \_ NO \_ WHQL \_ LEVEL è stato rimosso e D3DENUM \_ WHQL \_ LEVEL è stato aggiunto.

## <a name="create-resource-changes"></a>Creare modifiche alle risorse

È stato aggiunto un handle a diversi metodi e deve essere impostato su **NULL.** I metodi interessati includono:

-   [**CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture)
-   [**CreateVolumeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvolumetexture)
-   [**CreateCubeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture)
-   [**CreateVertexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer)
-   [**CreateIndexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createindexbuffer)
-   [**CreateRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createrendertarget)
-   [**CreateDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface)
-   [**CreateOffscreenPlainSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createoffscreenplainsurface)

## <a name="enumadaptermodes-changes"></a>Modifiche a EnumAdapterModes

[**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes) accetta ora un valore D3DFORMAT.


```
HRESULT IDirect3D9::EnumAdapterModes( 
       UINT Adapter, 
       D3DFORMAT Format, 
       UINT Mode, 
       D3DDISPLAYMODE *pMode); 
```



Il formato supporta un set di modalità di visualizzazione in espansione. Per proteggere le applicazioni dall'enumerazione di formati che non erano inerti al momento della distribuzione dell'applicazione, l'applicazione deve indicare a Direct3D il formato per le modalità di visualizzazione che devono essere enumerate. La matrice risultante delle modalità di visualizzazione sarà diversa solo per larghezza, altezza e frequenza di aggiornamento.

L'applicazione specifica un formato pixel e l'enumerazione è limitata alle modalità di visualizzazione che corrispondono esattamente al formato. Di seguito è riportato un elenco dei formati consentiti:

-   D3DFMT \_ A1R5G5B5
-   D3DFMT \_ A2B10G10R10
-   D3DFMT \_ A8R8G8B8
-   D3DFMT \_ R5G6B5
-   D3DFMT \_ X1R5G5B5
-   D3DFMT \_ X8R8G8B8

L'enumerazione è equivalente per le versioni alfa e non alfa dello stesso formato. Il formato restituito verrà sempre compilato con lo stesso formato fornito dall'applicazione.

Questo metodo considera 565 e 555 come equivalenti e restituisce la versione corretta nel formato . La differenza entra in gioco solo quando l'applicazione blocca il buffer nascosto ed è presente un flag esplicito che l'applicazione deve impostare per eseguire questa operazione.

## <a name="getsetstreamsource-changes"></a>Modifiche di Get/SetStreamSource

È stato aggiunto un parametro ai [**metodi GetStreamSource**](/windows/desktop/api) [**e SetStreamSource.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) L'offset è il numero di byte tra l'inizio del flusso e l'inizio dei dati del vertice. È misurata in byte. In questo modo la pipeline può supportare gli offset del flusso. Per scoprire se il dispositivo supporta gli offset di flusso, vedere D3DDEVCAPS2 \_ STREAMOFFSET.


```
HRESULT GetStreamSource(
    UINT StreamNumber,
    IDirect3DVertexBuffer9 **ppStreamData,
    UINT *pOffsetInBytes,
    UINT *pStride);
```



## <a name="multisampling-quality-changes"></a>Modifiche di qualità del multicampionamento

In precedenza era presente solo l'enumerazione TYPE D3DMULTISAMPLE. \_ Direct3D 9 mantiene questa enumerazione e aggiunge l'idea di un livello di qualità per ogni elemento dell'enumerazione. Il livello di qualità indica un compromesso tra qualità visiva e prestazioni indicando il numero di campioni mascherabili (nel senso di D3DRS \_ MULTISAMPLEMASK).

Un'applicazione deve scegliere il numero di esempi mascherabili necessari e quindi consultare pQualityLevels. Se diverso da zero, questo valore indica il numero di livelli di qualità che l'applicazione può passare alle varie funzioni di creazione tramite MultiSampleQuality. Poiché i driver espongono tutti i relativi schemi multicampionamento come livelli di qualità in D3DMULTISAMPLE NONMASKABLE, è possibile enumerare tutti gli schemi di multicampionamento disponibili tramite questo tipo se l'applicazione non deve mascherare i \_ campioni.

Il bit di estremità D3DPRASTERCAPS \_ STRETCHBLTMULTISAMPLE è stato ritirato. Questo bit indicava che il metodo multisampling non supportava le maschere di scrittura e non poteva essere attivato e disattivato tra [**BeginScene**](/windows/desktop/api) [**ed EndScene.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endscene) Questi metodi non mascherabili vengono ora esposti tramite D3DMULTISAMPLE \_ NONMASKABLE.


```
HRESULT CheckDeviceMultiSampleType( 
       UINT Adapter, 
       D3DDEVTYPE DeviceType, 
       D3DFORMAT SurfaceFormat, 
       BOOL Windowed, 
       D3DMULTISAMPLE_TYPE MultiSampleType, 
       DWORD * pQualityLevels); 
```



Esiste un valore massimo diverso per ogni numero di campioni mascherabili. Ad esempio, D3DMULTISAMPLE 4 SAMPLES potrebbe avere tre livelli di qualità, mentre \_ \_ D3DMULTISAMPLE \_ 2 \_ SAMPLES potrebbe avere solo uno. Esistono al massimo otto livelli di qualità per ogni numero di campioni mascherabili (il driver non può esprimere più). La qualità varia da zero a ( \* pQualityLevels - 1).

## <a name="resourcemanagerdiscardbytes-changes"></a>Modifiche a ResourceManagerDiscardBytes

ResourceManagerDiscardBytes è stato sostituito da IDirect3DDevice9::EvictManagedResources. È possibile che tutte le risorse, sia Le risorse Direct3D che le risorse driver.

Il gestore di risorse viene ora consultato quando la creazione di una risorsa (gestita o non gestita) non riesce perché la memoria video è insufficiente. Al responsabile verrà automaticamente richiesto di liberare risorse sufficienti per la creazione. In DirectX 8.0 non si tratta di un processo automatizzato.

## <a name="setsoftwarevertexprocessing-changes"></a>SetSoftwareVertexProcessing Changes

Un'applicazione può creare un dispositivo in modalità mista per usare l'elaborazione dei vertici software e hardware.

Per passare tra le due modalità di elaborazione dei vertici in DirectX 8.x, chiamare IDirect3DDevice8::SetRenderState. Questa funzionalità è stata sostituita [**con SetSoftwareVertexProcessing**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsoftwarevertexprocessing) per semplificare i problemi causati da blocchi di stato. Questo nuovo metodo non viene registrato dai blocchi di stato.

## <a name="texture-sampler-changes"></a>Modifiche al campionatore di trama

Direct3D 9 supporta fino a sedici superfici di trama in un unico passaggio usando il modello pixel shader 2 0. Tuttavia, il numero di coordinate della trama rimane limitato a \_ otto. Lo stato della fase della trama è associato a superfici, set di coordinate, elaborazione dei vertici ed elaborazione pixel. Per gestire queste differenze in fase di compilazione, [**SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) è stato suddiviso in due metodi:

-   IDirect3DDevice9::SetTextureStageState verrà comunque usato per lo stato delle coordinate della trama, ad esempio le modalità di ritorno a capo e la generazione delle coordinate di trama.
-   [**SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) è stato aggiunto e ora verrà usato per filtrare, affiancare, stringere, MIPLOD e così via. Questa operazione funzionerà per un massimo di sedici campionatori.

### <a name="settexturestagestate-changes"></a>Modifiche a SetTextureStageState

IDirect3DDevice9::SetTextureStageState imposta ora gli stati seguenti:

-   Correzione dello stato di elaborazione dei vertici delle funzioni. Questo stato controlla la manipolazione delle coordinate di trama D3DTSS \_ TEXTURETRANSFORMFLAGS e D3DTSS \_ TEXCOORDINDEX. È possibile impostare fino a otto coordinate di trama, perché sono sempre supportate otto coordinate di trama. D3DTSS \_ TEXCOORDINDEX è uno stato di elaborazione dei vertici di funzione fissa. Se viene usato un vertex shader programmabile, questo stato viene ignorato.
-   Correzione dello stato pixel shader funzione (TextureStageState legacy).

    -   D3DTSS \_ ALPHAARG0
    -   D3DTSS \_ ALPHAARG1
    -   D3DTSS \_ ALPHAARG2
    -   D3DTSS \_ ALPHAOP
    -   D3DTSS \_ BUMPENVLOFFSET
    -   D3DTSS \_ BUMPENVLSCALE
    -   D3DTSS \_ BUMPENVMAT00
    -   D3DTSS \_ BUMPENVMAT01
    -   D3DTSS \_ BUMPENVMAT10
    -   D3DTSS \_ BUMPENVMAT11
    -   D3DTSS \_ COLORARG0
    -   D3DTSS \_ COLORARG1
    -   D3DTSS \_ COLORARG2
    -   D3DTSS \_ COLOROP
    -   D3DTSS \_ RESULTARG

    Il numero di pixel shader fissi che è possibile impostare è minore o uguale al numero rappresentato da MaxTextureBlendStages.

Il numero di campionatori di trama disponibili per l'applicazione è determinato dalla versione pixel shader, come indicato nella tabella seguente.



| Nome                    | Numero                                                         |
|-------------------------|----------------------------------------------------------------|
| ps \_ 1 \_ da 1 a ps \_ 1 \_ 3    | 4 campionatori di trama                                             |
| ps \_ 1 \_ 4                | 6 campionatori di trama                                             |
| ps \_ 2 \_ 0                | 16 campionatori di trama                                            |
| pipeline di funzioni fisse | Campionatori di trama MaxTextureBlendStages/MaxSimultaneousTextures |



 

I dispositivi che supportano il mapping dello spostamento in Direct3D 9 supporteranno un campionatore aggiuntivo (D3DDMAPSAMPLER), che esegue il campionamento delle mappe di spostamento nell'unità a tessellatore.

### <a name="setsamplerstate-changes"></a>Modifiche di SetSamplerState

IDirect3DDevice9::SetSamplerState imposta lo stato del campionatore (incluso quello usato nell'unità a tessellatore per campionare le mappe di spostamento). Questi elementi sono stati rinominati con un prefisso D3DSAMP per abilitare il rilevamento degli errori in fase di compilazione durante la \_ portabilità da DirectX 8.x. Gli stati includono:

-   D3DSAMP \_ ADDRESSU
-   D3DSAMP \_ ADDRESSV
-   D3DSAMP \_ ADDRESSW
-   D3DSAMP \_ BORDERCOLOR
-   D3DSAMP \_ MAGFILTER
-   D3DSAMP \_ MAXANISOTROPY
-   D3DSAMP \_ MAXMIPLEVEL
-   D3DSAMP \_ MINFILTER
-   D3DSAMP \_ MIPFILTER
-   D3DSAMP \_ MIPMAPLODBIAS

## <a name="vertex-declaration-changes"></a>Modifiche alla dichiarazione dei vertici

Le dichiarazioni dei vertici sono ora disaccoccoppate dalla creazione di vertex shader. Le dichiarazioni dei vertici usano ora un'Component Object Model (COM).

Per DirectX 8.x, le dichiarazioni dei vertici sono collegate ai vertex shader.

-   Per la pipeline di funzioni fisse, chiamare [**SetVertexShader**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader) con il codice FVF (Flexible Vertex Format) del vertex buffer.
-   Per i vertex shader, chiamare IDirect3DDevice9::SetVertexShader con un handle per un vertex shader creato in precedenza. Lo shader include una dichiarazione di vertice.

Per Direct3D 9, le dichiarazioni dei vertici vengono disaccoccoppate dai vertex shader e possono essere usate con la pipeline di funzioni fisse o con gli shader.

-   Per la pipeline di funzioni fisse, non è necessario chiamare IDirect3DDevice9::SetVertexShader. Se, tuttavia, si vuole passare alla pipeline di funzioni fisse e in precedenza è stato usato un vertex shader, chiamare IDirect3DDevice9::SetVertexShader(**NULL**). Al termine, sarà comunque necessario chiamare [**SetFVF**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setfvf) per dichiarare il codice FVF.
-   Quando si usano vertex shader, chiamare IDirect3DDevice9::SetVertexShader con l'oggetto vertex shader. Chiamare anche IDirect3DDevice9::SetFVF per configurare una dichiarazione di vertice. In questo modo vengono utilizzate le informazioni implicite in FVF. [**È possibile chiamare SetVertexDeclaration**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexdeclaration) al posto di IDirect3DDevice9::SetFVF perché supporta dichiarazioni di vertici che non possono essere espresse con FVF.

## <a name="intervals-and-swapeffects-changes"></a>Intervalli e modifiche swapEffects

Sono state apportate diverse modifiche per offrire all'utente un maggiore controllo sulla frequenza di aggiornamento del monitoraggio, sulla velocità di presentazione e sul front-buffer rispetto al disegno del buffer nascosto. Ecco quali sono:

-   Rimozione di un effetto di scambio, D3DSWAPEFFECT COPY VSYNC e di una frequenza di \_ \_ presentazione, D3DPRESENT \_ RATE \_ UNLIMITED.
-   Rinominato D3DPRESENT \_ PARAMETERS. Presentazione \_ fullscreenInterval a PresentationIntervals.
-   Aggiunta di D3DPRESENT INTERVAL IMMEDIATE, che significa che la presentazione \_ \_ non è sincronizzata con la sincronizzazione verticale. Come in DirectX 8.x, D3DPRESENT INTERVAL DEFAULT è definito come zero ed è \_ \_ equivalente a D3DPRESENT \_ INTERVAL \_ ONE. D3DPRESENT \_ INTERVAL DEFAULT è una \_ comodità per l'inizializzazione di D3DPRESENT \_ PARAMETERS su zero.

Per una spiegazione dettagliata delle modalità e degli intervalli supportati, vedere D3DPRESENT.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Grafica Direct3D 9](dx9-graphics.md)
</dt> </dl>

 

 
