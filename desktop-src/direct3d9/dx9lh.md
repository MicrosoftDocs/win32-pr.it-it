---
description: Questa documentazione si riferisce specificamente alle estensioni di Windows Vista per la grafica DirectX.
ms.assetid: 3cc0b08c-e126-4f1b-b5d1-0d6c1ebeb0c5
title: Riepilogo delle funzionalità (Direct3D 9 per Windows Vista)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d5cf2447297b7f24edf7d0200e640d5aef90bff
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304076"
---
# <a name="feature-summary-direct3d-9-for-windows-vista"></a>Riepilogo delle funzionalità (Direct3D 9 per Windows Vista)

Questa documentazione si riferisce specificamente alle estensioni di Windows Vista per la grafica DirectX. Per sviluppare la potenza di DirectX per Windows Vista, è necessario installare Windows Vista SDK e DirectX SDK. Le applicazioni che usano DirectX per Windows Vista devono usare hardware che usa il driver WDDM (modello di driver di dispositivo Windows) invece di XPDM (modello di driver XP); i driver che non implementano WDDM non possono creare un'istanza delle interfacce grafiche DirectX di Windows Vista.

Scopri le nuove funzionalità grafiche DirectX in Windows Vista in una delle seguenti sezioni:

-   [Modifiche del comportamento del dispositivo](#device-behavior-changes)
-   [Disabilitazione dell'elaborazione dei vertici software multithread](#disabling-multithreaded-software-vertex-processing)
-   [Superfici a un bit](#one-bit-surfaces)
-   [Lettura dei buffer di profondità/stencil](#reading-depthstencil-buffers)
-   [Condivisione di risorse](#sharing-resources)
-   [Conversione sRGB prima della fusione](#srgb-conversion-before-blending)
-   [Miglioramenti di StretchRect](#stretchrect-improvements)
-   [Creazione di trame nella memoria di sistema](#texture-creation-in-system-memory)

## <a name="device-behavior-changes"></a>Modifiche del comportamento del dispositivo

I dispositivi vengono ora persi solo in due circostanze; Quando l'hardware viene reimpostato perché è sospeso e quando il driver di dispositivo viene arrestato. Quando l'hardware si blocca, il dispositivo può essere reimpostato chiamando [**ResetEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-resetex). Se si blocca l'hardware, la memoria della trama viene persa.

Dopo l'arresto di un driver, è necessario ricreare l'oggetto IDirect9Ex per riprendere il rendering.

Quando l'area di presentazione è nascosta da un'altra finestra in modalità finestra o quando un'applicazione a schermo intero è ridotta a icona, [**PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) restituirà S \_ D3DPRESENTATIONOCCLUDED. Le applicazioni a schermo intero possono riprendere il rendering quando ricevono un messaggio di callback [**WM \_ ACTIVATEAPP**](../winmsg/wm-activateapp.md) .

Nelle versioni precedenti di DirectX, quando un'applicazione ha riscontrato una modifica della modalità, l'unico modo per eseguire il ripristino era ripristinare il dispositivo e ricreare tutte le risorse di memoria video e le catene di scambio. Con DirectX per Windows Vista, la chiamata di reset dopo una modifica della modalità non provoca la perdita di superfici di memoria di trama, le trame e le informazioni sullo stato e non è necessario ricreare tali risorse.

## <a name="disabling-multithreaded-software-vertex-processing"></a>Disabilitazione dell'elaborazione dei vertici software multithread

È stato aggiunto un nuovo bit di Caps (D3DCREATE \_ Disable \_ PSGP \_ Threading) che disabilita il multithreading per l'elaborazione dei vertici software (SWVP). Usare questa macro per generare un flag di comportamento per IDirect3D9:: CreateDevice.


```
#define D3DCREATE_DISABLE_PSGP_THREADING
```



## <a name="one-bit-surfaces"></a>Superfici a un bit

È disponibile un nuovo tipo di formato di superficie di un bit che può essere particolarmente utile per l'elaborazione di glifi di testo. Il nuovo formato è denominato D3DFMT \_ a1. Una superficie a un bit è progettata per essere usata come trama per pixel o per l'output della destinazione di rendering generato da ComposeRects o ColorFill. Non sono presenti estremità separate per la larghezza e l'altezza della superficie; un'implementazione di deve supportare una superficie di dimensioni singole che è 2K Texels x 8 Texel.

Una superficie a un bit ha un bit per Texel; Pertanto, un valore significherebbe che tutti i componenti (r, g, b, a) di un pixel sono pari a 1 e zero significherebbe che tutti i componenti sono uguali a 0. È possibile usare le superfici a un bit con le API seguenti: ColorFill, UpdateSurface e UpdateTexture.

Quando viene letta una superficie a un bit, il runtime può eseguire l'esempio di punto o il filtro convoluzione. Il filtro di convoluzione è regolabile (vedere [**SetConvolutionMonoKernel**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-setconvolutionmonokernel)).

Esistono alcune restrizioni per le superfici a un bit:

-   Il mapping MIP non è supportato
-   non è possibile leggere o scrivere dati sRGB in una superficie a un bit.
-   Non è possibile usare una superficie a un bit come trama del vertice o per il campionamento multiplo.

## <a name="reading-depthstencil-buffers"></a>Lettura dei buffer di profondità/stencil

Usare IDirect3DDevice9:: UpdateSurface per leggere o scrivere dati depth/stencil dalle superfici ottenute da IDirect3DDevice9:: CreateDepthStencilSurface o IDirect3DDevice9:: GetDepthStencilSurface.

Per prima cosa, creare una superficie bloccabile, solo Depth o stencil solo usando IDirect3DDevice9:: CreateOffscreenPlainSurface. Utilizzare uno dei seguenti formati:

-   D3DFMT \_ D16 \_ lockable
-   D3DFMT \_ D32F \_ lockable
-   D3DFMT \_ D32 \_ lockable
-   D3DFMT \_ S8 \_ bloccabile

In secondo luogo, trasferire i dati tra il buffer di profondità/stencil e la superficie di stencil o di profondità bloccabile appena creata. Il trasferimento viene eseguito utilizzando IDirect3DDevice9:: UpdateSurface.

UpdateSurface avrà esito negativo quando entrambe le superfici sono un formato BLOCCAbile o non sono bloccabili.

Il trasferimento di dati inesistenti provocherà un errore (ad esempio, il trasferimento da una superficie non bloccabile di sola profondità a una \_ \_ superficie bloccabile D3DFMT S8).

Il resto delle restrizioni per IDirect3DDevice9:: UpdateSurface è ancora applicabile.

## <a name="sharing-resources"></a>Condivisione di risorse

Le risorse Direct3D possono ora essere condivise tra dispositivi o processi. Questo vale per qualsiasi risorsa Direct3D, incluse trame, buffer di vertici, buffer di indice o superfici, ad esempio destinazioni di rendering, buffer depth stencil o superfici non semplici dello schermo. Per essere condivisi, è necessario designare una risorsa per la condivisione al momento della creazione, quindi individuare la risorsa nel pool predefinito (D3DPOOL \_ default). Una volta creata una risorsa per la condivisione, può essere condivisa tra i dispositivi all'interno di un processo o condivisa tra più processi.

Per abilitare le risorse condivise, le API per la creazione di risorse hanno un parametro handle aggiuntivo. Si tratta di un HANDLE che punta alla risorsa condivisa. Nelle revisioni precedenti di DirectX, questo argomento fa parte della firma dell'API, ma è stato inutilizzato e deve essere impostato su **null**. A partire da Windows Vista, usare pSharedHandle nei modi seguenti:

-   Impostare il puntatore (pSharedHandle) su **null** per non condividere una risorsa. Questo comportamento è analogo a quello di DirectX prima di Windows Vista.
-   Per creare una risorsa condivisa, chiamare qualsiasi API per la creazione di risorse (vedere di seguito) con un handle non inizializzato (il puntatore non è **null** (pSharedHandle! = **null**), ma il puntatore punta a un valore **null** ( \* pSharedHandle = = **null**)). L'API genererà una risorsa condivisa e restituirà un handle valido.
-   Per aprire e accedere a una risorsa condivisa creata in precedenza usando un handle di risorsa condiviso non NULL, impostare pSharedHandle sull'indirizzo di tale handle. Dopo aver aperto la risorsa condivisa precedentemente creata in questo modo, è possibile usare l'interfaccia restituita nell'API Direct3D 9 o Direct3D 9Ex come se l'interfaccia fosse una risorsa tipica di quel tipo.

Le API per la creazione di risorse includono- [**createTexture**](/windows/desktop/api), [**CreateVolumeTexture**](/windows/desktop/api), [**CreateCubeTexture**](/windows/desktop/api), [**CreateRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createrendertarget), [**CreateVertexBuffer**](/windows/desktop/api) [**, CreateIndexBuffer**](/windows/desktop/api) [**, CreateDepthStencilSurface,**](/windows/desktop/api) [**CreateOffscreenPlainSurface,**](/windows/desktop/api) [**CreateDepthStencilSurfaceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-createdepthstencilsurfaceex), [**CreateOffscreenPlainSurfaceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-createoffscreenplainsurfaceex)e [**CreateRenderTargetEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-createrendertargetex).

Esistono alcune restrizioni per l'uso di risorse condivise. Tra queste sono incluse:

-   L'API che si usa per aprire una risorsa condivisa deve corrispondere all'API usata per creare la risorsa condivisa. Se ad esempio è stato usato [**createTexture**](/windows/desktop/api) per creare una risorsa condivisa, è necessario usare **createTexture** per aprire la risorsa condivisa. Se è stato usato [**CreateRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createrendertarget) per creare una risorsa condivisa, è necessario usare **CreateRenderTarget** per aprire la risorsa condivisa e così via.
-   Quando si apre una risorsa condivisa, è necessario specificare il \_ valore predefinito di D3DPOOL.
-   Le risorse bloccabili, ad esempio le trame con D3DUSAGE \_ dinamici, i buffer di vertici e gli indici, possono comportare una riduzione delle prestazioni. Il Rendertargets bloccabile non verrà condiviso in alcuni componenti hardware.
-   I riferimenti a una risorsa condivisa tra processi devono avere le stesse dimensioni della risorsa originale. Quando si passa un handle tra più processi, includere le informazioni sulla dimensione in modo che sia possibile creare il riferimento in modo identico.
-   Le aree condivise tra processi non forniscono alcun meccanismo di sincronizzazione. Le modifiche di lettura/scrittura in una superficie condivisa potrebbero non riflettere la vista di un processo di riferimento della superficie quando previsto. Per fornire la sincronizzazione, utilizzare le query di evento o bloccare la trama.
-   Solo il processo che inizialmente crea una risorsa condivisa può bloccarlo, ovvero qualsiasi processo che apre un riferimento a tale risorsa condivisa non può bloccarlo.
-   Se una risorsa condivisa è bloccata, non viene convalidata da altri processi per verificare se la risorsa è disponibile.

## <a name="srgb-conversion-before-blending"></a>Conversione sRGB prima della fusione

È ora possibile verificare se il dispositivo è in grado di convertire i dati della pipeline in sRGB prima della fusione del buffer di frame. Ciò implica che il dispositivo converte i valori della destinazione di rendering da sRGB. Per verificare se la conversione è supportata dall'hardware, verificare la presenza di questo limite:


```
D3DPMISCCAPS_POSTBLENDSRGBCONVERT
```



Questo limite identifica l'hardware che supporta la conversione a sRGB prima della fusione. Questa funzionalità è importante per il rendering di alta qualità da FP16 Frame Buffers in Gestione finestre desktop (DWM).

## <a name="stretchrect-improvements"></a>Miglioramenti di StretchRect

Nelle versioni precedenti di DirectX, StretchRect presenta diverse restrizioni per gestire driver diversi (vedere IDirect3DDevice9:: StretchRect). Windows Vista è basato sul modello di driver di dispositivo Windows (WDDM). Questo nuovo modello di driver è molto più solido e consente ai driver di gestire i casi speciali nell'hardware.

In generale, l'unica restrizione rimanente è che la destinazione di rendering deve essere stata creata con l'utilizzo della destinazione di rendering (D3DUSAGE \_ RENDERTARGET). Questa restrizione viene sollevata se si esegue una copia semplice, in cui l'origine e la destinazione hanno lo stesso formato, le stesse dimensioni e non sono presenti sottorettangoli.

## <a name="texture-creation-in-system-memory"></a>Creazione di trame nella memoria di sistema

Le applicazioni che richiedono maggiore flessibilità sull'utilizzo, l'allocazione e l'eliminazione della memoria di sistema possono ora creare trame da un puntatore di memoria di sistema. Ad esempio, un'applicazione potrebbe creare una trama Direct3D da un puntatore bitmap di memoria di sistema GDI.

Per creare una trama di questo tipo, è necessario eseguire due operazioni:

-   Allocare memoria di sistema sufficiente per mantenere la superficie della trama. Il numero minimo di byte è larghezza x altezza x byte per pixel.
-   Passare l'indirizzo di un puntatore alla superficie di memoria di sistema per il \* parametro handle a IDirect3DDevice9:: createTexture.

Ecco il prototipo di funzione per IDirect3DDevice9:: CreateTexture:


```
STDMETHOD(CreateTexture)(THIS_ UINT Width, UINT Height, UINT Levels, 
    DWORD Usage, D3DFORMAT Format, D3DPOOL Pool, IDirect3DTexture9** ppTexture, 
    HANDLE* pSharedHandle)
```



Una trama con memoria di sistema presenta le restrizioni seguenti:

-   Il pitch della trama deve essere uguale alla larghezza della trama per il numero di byte per pixel.
-   Quando si usano formati compressi (formati DXT), l'applicazione è responsabile dell'allocazione delle dimensioni corrette.
-   Sono supportate solo le trame con un solo livello di mipmap.
-   Il valore passato a CreateTexture per l'argomento del pool deve essere D3DPOOL \_ SYSTEMMEM.
-   Questa API esegue il wrapping della memoria fornita in una trama. Non deallocare la memoria fino a quando non viene eseguita.

 

 
