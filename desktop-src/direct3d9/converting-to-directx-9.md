---
description: Le funzionalità seguenti sono state modificate in Microsoft Direct3D 9. Se si usano queste funzionalità, vedere le modifiche elencate di seguito per trasferire l'applicazione a Direct3D 9.
ms.assetid: 6f5b2cc1-5415-4af8-a964-051a5af42680
title: Conversione in Direct3D 9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: becdb878ad462bfc0157fb15b3c9c1ef2ba158dd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305057"
---
# <a name="converting-to-direct3d-9"></a>Conversione in Direct3D 9

Le funzionalità seguenti sono state modificate in Microsoft Direct3D 9. Se si usano queste funzionalità, vedere le modifiche elencate di seguito per trasferire l'applicazione a Direct3D 9.

-   [BaseVertexIndex modifiche](#basevertexindex-changes)
-   [CreateImageSurface modifiche](#createimagesurface-changes)
-   [D3DENUM \_ Nessuna \_ modifica a livello di WHQL \_](/windows)
-   [Crea modifiche alle risorse](#create-resource-changes)
-   [EnumAdapterModes modifiche](#enumadaptermodes-changes)
-   [Modifiche Get/SetStreamSource \_](#getsetstreamsource-changes)
-   [Modifiche della qualità del campionamento multiplo](#multisampling-quality-changes)
-   [ResourceManagerDiscardBytes modifiche](#resourcemanagerdiscardbytes-changes)
-   [SetSoftwareVertexProcessing modifiche](#setsoftwarevertexprocessing-changes)
-   [Modifiche al campionatore trama](#texture-sampler-changes)
-   [Modifiche della dichiarazione vertici](#vertex-declaration-changes)
-   [Intervalli \_ e \_ modifiche SwapEffects \_](#intervals-and-swapeffects-changes)

## <a name="basevertexindex-changes"></a>BaseVertexIndex modifiche

In DirectX 8. x, IDirect3DDevice8:: SetIndices richiede un puntatore al buffer di indice e un BaseVertexIndex per la posizione iniziale nel buffer dei vertici. Un'applicazione che suddivide in batch oggetti diversi nel buffer dei vertici ha dovuto cambiare il buffer dell'indice (oppure effettuare una chiamata a IDirect3DDevice8:: SetIndices) prima di chiamare IDirect3DDevice8::D rawIndexedPrimitive.

In Direct3D 9, la posizione iniziale nel buffer vertex, *BaseVertexIndex*, è stata spostata in IDirect3DDevice9::D rawindexedprimitive e il tipo di dati è stato modificato da DWORD a int.


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



## <a name="createimagesurface-changes"></a>CreateImageSurface modifiche

IDirect3DDevice8:: CreateImageSurface è stato rinominato [**CreateOffscreenPlainSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createoffscreenplainsurface). È stato aggiunto un parametro aggiuntivo che accetta un tipo D3DPOOL. D3DPOOL \_ Scratch restituirà una superficie con caratteristiche identiche a una superficie creata da IDirect3DDevice8:: CreateImageSurface. D3DPOOL \_ default è il pool appropriato da usare con [**StretchRect**](/windows/desktop/api) e [**ColorFill**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-colorfill).

## <a name="d3denum_no_whql_level-changes"></a>D3DENUM \_ Nessuna \_ modifica a livello di WHQL \_

Le applicazioni devono ora richiedere in modo esplicito Microsoft Windows Hardware Quality Labs (WHQL) perché la risposta richiede tempo relativamente lungo (pochi secondi). D3DENUM \_ non \_ \_ è stato rimosso alcun livello WHQL ed \_ \_ è stato aggiunto il livello di D3DENUM WHQL.

## <a name="create-resource-changes"></a>Crea modifiche alle risorse

Un handle è stato aggiunto a diversi metodi e deve essere impostato su **null**. I metodi interessati includono:

-   [**CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture)
-   [**CreateVolumeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvolumetexture)
-   [**CreateCubeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture)
-   [**CreateVertexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer)
-   [**CreateIndexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createindexbuffer)
-   [**CreateRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createrendertarget)
-   [**CreateDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface)
-   [**CreateOffscreenPlainSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createoffscreenplainsurface)

## <a name="enumadaptermodes-changes"></a>EnumAdapterModes modifiche

Il [**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes) ora accetta un D3DFORMAT.


```
HRESULT IDirect3D9::EnumAdapterModes( 
       UINT Adapter, 
       D3DFORMAT Format, 
       UINT Mode, 
       D3DDISPLAYMODE *pMode); 
```



Il formato supporta un set di modalità di visualizzazione in espansione. Per proteggere le applicazioni dall'enumerazione dei formati che non sono stati inventati quando l'applicazione è stata spedita, l'applicazione deve indicare a Direct3D il formato per le modalità di visualizzazione da enumerare. La matrice di modalità di visualizzazione risultante si differenzia solo per larghezza, altezza e frequenza di aggiornamento.

L'applicazione specifica un formato pixel e l'enumerazione è limitata a tali modalità di visualizzazione che corrispondono esattamente al formato. Di seguito è riportato un elenco dei formati consentiti:

-   \_A1R5G5B5 D3DFMT
-   \_A2B10G10R10 D3DFMT
-   \_A8R8G8B8 D3DFMT
-   \_R5G6B5 D3DFMT
-   \_X1R5G5B5 D3DFMT
-   \_X8R8G8B8 D3DFMT

L'enumerazione è equivalente per le versioni alfa e non Alpha dello stesso formato. Il formato restituito verrà sempre riempito con lo stesso formato fornito dall'applicazione.

Questo metodo considera 565 e 555 come equivalente e restituisce la versione corretta nel formato. La differenza entra in gioco solo quando l'applicazione blocca il buffer nascosto ed esiste un flag esplicito che l'applicazione deve impostare per eseguire questa operazione.

## <a name="getsetstreamsource-changes"></a>Modifiche Get/SetStreamSource

È stato aggiunto un parametro ai metodi [**GetStreamSource**](/windows/desktop/api) e [**SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) . L'offset è il numero di byte tra l'inizio del flusso e l'inizio dei dati del vertice. È misurata in byte. Ciò consente alla pipeline di supportare gli offset del flusso. Per sapere se il dispositivo supporta gli offset del flusso, vedere D3DDEVCAPS2 \_ STREAMOFFSET.


```
HRESULT GetStreamSource(
    UINT StreamNumber,
    IDirect3DVertexBuffer9 **ppStreamData,
    UINT *pOffsetInBytes,
    UINT *pStride);
```



## <a name="multisampling-quality-changes"></a>Modifiche della qualità del campionamento multiplo

In precedenza era presente solo l' \_ enumerazione del tipo D3DMULTISAMPLE. Direct3D 9 mantiene questa enumerazione e aggiunge l'idea di un livello di qualità per ogni elemento dell'enumerazione. Il livello di qualità indica un compromesso tra qualità e prestazioni visive indicante il numero di campioni mascherabili (nel senso di D3DRS \_ MULTISAMPLEMASK).

Un'applicazione deve scegliere il numero di campioni mascherabili necessari e quindi consultare pQualityLevels. Se diverso da zero, questo valore indica il numero di livelli di qualità che l'applicazione può passare alle varie funzioni di creazione tramite MultiSampleQuality. Poiché i driver espongono tutti gli schemi multisample come livelli di qualità in D3DMULTISAMPLE \_ non mascherabili, è possibile enumerare tutti gli schemi multicampionamento disponibili tramite questo tipo se l'applicazione non deve mascherare gli esempi.

Il \_ bit D3DPRASTERCAPS STRETCHBLTMULTISAMPLE Caps è stato ritirato. Questo bit utilizzato per indicare che il metodo di campionamento multiplo non supporta le maschere di scrittura e non può essere attivato e disattivato tra [**BeginScene**](/windows/desktop/api) e [**EndScene**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endscene). Questi metodi non mascherabili sono ora esposti tramite D3DMULTISAMPLE non \_ mascherabile.


```
HRESULT CheckDeviceMultiSampleType( 
       UINT Adapter, 
       D3DDEVTYPE DeviceType, 
       D3DFORMAT SurfaceFormat, 
       BOOL Windowed, 
       D3DMULTISAMPLE_TYPE MultiSampleType, 
       DWORD * pQualityLevels); 
```



Per ogni numero di campioni mascherabili è disponibile un valore massimo diverso. Ad esempio, gli \_ \_ esempi di D3DMULTISAMPLE 4 potrebbero avere tre livelli di qualità, mentre gli esempi di D3DMULTISAMPLE \_ 2 \_ possono avere solo uno. Esistono al massimo otto livelli di qualità per ogni numero di campioni mascherabili (il driver non è autorizzato a esprimere più). La qualità varia da zero a ( \* pQualityLevels-1).

## <a name="resourcemanagerdiscardbytes-changes"></a>ResourceManagerDiscardBytes modifiche

ResourceManagerDiscardBytes è stato sostituito da IDirect3DDevice9:: EvictManagedResources. Consente di rimuovere tutte le risorse, sia Direct3D che i driver.

Resource Manager viene ora consultato quando la creazione di una risorsa (gestita o non gestita) ha esito negativo perché la memoria video è insufficiente. Al responsabile verrà automaticamente richiesto di liberare risorse sufficienti per la creazione. In DirectX 8,0, non si tratta di un processo automatizzato.

## <a name="setsoftwarevertexprocessing-changes"></a>SetSoftwareVertexProcessing modifiche

Un'applicazione può creare un dispositivo in modalità mista per usare l'elaborazione dei vertici software e hardware.

Per passare tra le due modalità di elaborazione dei vertici in DirectX 8. x, chiamare IDirect3DDevice8:: SetRenderState. Questa operazione è stata sostituita con [**SetSoftwareVertexProcessing**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsoftwarevertexprocessing) per semplificare i problemi causati da blocchi di stato. Questo nuovo metodo non viene registrato dai blocchi di stato.

## <a name="texture-sampler-changes"></a>Modifiche al campionatore trama

Direct3D 9 supporta fino a sedici superfici di trama in un unico passaggio usando il modello pixel shader 2 \_ 0. Tuttavia, il numero di coordinate di trama rimane limitato a otto. Lo stato della fase trama è associato a superfici, set di coordinate, elaborazione dei vertici e elaborazione pixel. Per gestire queste differenze in fase di compilazione, [**SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) è stato suddiviso in due metodi:

-   IDirect3DDevice9:: SetTextureStageState verrà comunque utilizzato per lo stato della coordinata di trama, ad esempio le modalità a capo e la generazione delle coordinate di trama.
-   [**SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) è stato aggiunto e verrà ora usato per filtrare, affiancare, bloccare, MIPLOD e così via. Questa operazione funzionerà per un massimo di sedici esempi.

### <a name="settexturestagestate-changes"></a>SetTextureStageState modifiche

IDirect3DDevice9:: SetTextureStageState ora imposta gli Stati seguenti:

-   Stato di elaborazione vertice funzione fisso. Questo stato controlla la manipolazione delle coordinate di trama D3DTSS \_ TEXTURETRANSFORMFLAGS e D3DTSS \_ TEXCOORDINDEX. È possibile impostare fino a otto, perché otto coordinate di trama sono sempre supportate. D3DTSS \_ TEXCOORDINDEX è uno stato di elaborazione Vertex della funzione fissa. Se viene usato un vertex shader programmabile, questo stato viene ignorato.
-   Funzione Fixed pixel shader stato (TextureStageState legacy).

    -   \_ALPHAARG0 D3DTSS
    -   \_ALPHAARG1 D3DTSS
    -   \_ALPHAARG2 D3DTSS
    -   \_ALPHAOP D3DTSS
    -   \_BUMPENVLOFFSET D3DTSS
    -   \_BUMPENVLSCALE D3DTSS
    -   \_BUMPENVMAT00 D3DTSS
    -   \_BUMPENVMAT01 D3DTSS
    -   \_BUMPENVMAT10 D3DTSS
    -   \_BUMPENVMAT11 D3DTSS
    -   \_COLORARG0 D3DTSS
    -   \_COLORARG1 D3DTSS
    -   \_COLORARG2 D3DTSS
    -   \_COLOROP D3DTSS
    -   \_RESULTARG D3DTSS

    Il numero degli Stati pixel shader di funzione fissa che è possibile impostare è minore o uguale al numero rappresentato da MaxTextureBlendStages.

Il numero di campioni di trama disponibili per l'applicazione è determinato dalla versione pixel shader, come indicato nella tabella seguente.



| Nome                    | Number                                                         |
|-------------------------|----------------------------------------------------------------|
| \_da PS 1 \_ 1 a PS \_ 1 \_ 3    | 4 campionatori trama                                             |
| PS \_ 1 \_ 4                | 6 esempi di trama                                             |
| PS \_ 2 \_ 0                | 16 Sampler trama                                            |
| pipeline della funzione fissa | MaxTextureBlendStages/MaxSimultaneousTextures trama Samplers |



 

I dispositivi che supportano il mapping di spostamento in Direct3D 9 supporteranno un campionatore aggiuntivo (D3DDMAPSAMPLER), che consente di campionare le mappe di spostamento nell'unità mosaico.

### <a name="setsamplerstate-changes"></a>SetSamplerState modifiche

IDirect3DDevice9:: SetSamplerState imposta lo stato del campionatore (incluso quello usato nell'unità mosaico per eseguire il campionamento delle mappe di spostamento). Questi sono stati rinominati con un \_ prefisso D3DSAMP per abilitare il rilevamento degli errori in fase di compilazione durante il porting da DirectX 8. x. Gli stati includono:

-   \_Indirizzo D3DSAMP
-   \_ADDRESSV D3DSAMP
-   \_ADDRESSW D3DSAMP
-   \_BorderColor D3DSAMP
-   \_MAGFILTER D3DSAMP
-   \_MAXANISOTROPY D3DSAMP
-   \_MAXMIPLEVEL D3DSAMP
-   \_MINFILTER D3DSAMP
-   \_MIPFILTER D3DSAMP
-   \_MIPMAPLODBIAS D3DSAMP

## <a name="vertex-declaration-changes"></a>Modifiche della dichiarazione vertici

Le dichiarazioni dei vertici sono ora disaccoppiate dalla creazione del vertex shader. Le dichiarazioni Vertex ora usano un'interfaccia Component Object Model (COM).

Per DirectX 8. x, le dichiarazioni di vertice sono associate a vertex shader.

-   Per la pipeline della funzione fissa, chiamare [**SetVertexShader**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader) con il codice FVF (Flexible Vertex Format) del buffer dei vertici.
-   Per i vertex shader, chiamare IDirect3DDevice9:: SetVertexShader con un handle per un vertex shader creato in precedenza. Lo shader include una dichiarazione del vertice.

Per Direct3D 9, le dichiarazioni dei vertici sono separate dai vertex shader e possono essere usate con la pipeline della funzione fissa o con gli shader.

-   Per la pipeline della funzione fixed, non è necessario chiamare IDirect3DDevice9:: SetVertexShader. Se tuttavia si desidera passare alla pipeline della funzione fissa e in precedenza è stato utilizzato un vertex shader, chiamare IDirect3DDevice9:: SetVertexShader (**null**). Al termine, sarà comunque necessario chiamare [**SetFVF**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setfvf) per dichiarare il codice FVF.
-   Quando si usano vertex shader, chiamare IDirect3DDevice9:: SetVertexShader con l'oggetto vertex shader. Inoltre, chiamare IDirect3DDevice9:: SetFVF per impostare una dichiarazione del vertice. Questa operazione usa le informazioni implicite in FVF. [**SetVertexDeclaration**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexdeclaration) può essere chiamato al posto di IDirect3DDevice9:: SetFVF perché supporta le dichiarazioni dei vertici che non possono essere espresse con un FVF.

## <a name="intervals-and-swapeffects-changes"></a>Intervalli e modifiche SwapEffects

Sono state apportate diverse modifiche per fornire all'utente un maggiore controllo sulla frequenza di aggiornamento del monitor, sulla velocità di presentazione e sul disegno di buffer back-buffer. Ecco quali sono:

-   Rimossi un effetto di swap, una \_ copia D3DSWAPEFFECT \_ vsync e una frequenza di presentazione, D3DPRESENT \_ rate \_ Unlimited.
-   Parametri D3DPRESENT rinominati \_ . \_PresentationInterval a schermo intero a PresentationIntervals.
-   Aggiunta \_ dell'intervallo \_ di D3DPRESENT immediate, il che significa che la presentazione non è sincronizzata con la sincronizzazione verticale. Come in DirectX 8. x, il \_ valore predefinito per l'intervallo di D3DPRESENT \_ è pari a zero ed è equivalente a D3DPRESENT \_ interval \_ One. D3DPRESENT \_ interval \_ default è una praticità per l'inizializzazione dei \_ parametri D3DPRESENT su zero.

Per una spiegazione dettagliata delle modalità e degli intervalli supportati, vedere D3DPRESENT.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Grafica Direct3D 9](dx9-graphics.md)
</dt> </dl>

 

 
