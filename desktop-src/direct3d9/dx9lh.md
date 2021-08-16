---
description: Questa documentazione si riferisce in modo specifico alle Windows Vista per la grafica DirectX.
ms.assetid: 3cc0b08c-e126-4f1b-b5d1-0d6c1ebeb0c5
title: Riepilogo delle funzionalità (Direct3D 9 per Windows Vista)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 242af80fa4d6f00c1e55d4852884f9fbbf8de287c6792b3b4aaaad196a6cd113
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118523078"
---
# <a name="feature-summary-direct3d-9-for-windows-vista"></a>Riepilogo delle funzionalità (Direct3D 9 per Windows Vista)

Questa documentazione si riferisce in modo specifico alle Windows Vista per la grafica DirectX. Per sviluppare la potenza di DirectX per Windows Vista, è necessario installare Windows Vista SDK e DirectX SDK. Le applicazioni che usano DirectX per Windows Vista devono usare hardware che usa il driver WDDM (Windows Device Driver Model) anziché XPDM (XP Driver Model); I driver che non implementano WDDM non possono creare istanze Windows grafica DirectX di Vista.

Informazioni sulle nuove funzionalità di grafica DirectX in Windows Vista in una di queste sezioni:

-   [Modifiche al comportamento del dispositivo](#device-behavior-changes)
-   [Disabilitazione dell'elaborazione di vertici software multithreading](#disabling-multithreaded-software-vertex-processing)
-   [One Bit Surfaces](#one-bit-surfaces)
-   [Profondità di lettura/buffer degli stencil](#reading-depthstencil-buffers)
-   [Condivisione di risorse](#sharing-resources)
-   [Conversione di sRGB prima della fusione](#srgb-conversion-before-blending)
-   [Miglioramenti di StretchRect](#stretchrect-improvements)
-   [Creazione di trame nella memoria di sistema](#texture-creation-in-system-memory)

## <a name="device-behavior-changes"></a>Modifiche al comportamento del dispositivo

I dispositivi vengono ora persi solo in due circostanze: quando l'hardware viene reimpostato perché è in sospeso e quando il driver di dispositivo viene arrestato. Quando l'hardware si blocca, il dispositivo può essere reimpostato chiamando [**ResetEx.**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-resetex) Se l'hardware si blocca, la memoria della trama viene persa.

Dopo l'arresto di un driver, è necessario ricreare l'oggetto IDirect9Ex per riprendere il rendering.

Quando l'area di presentazione viene nascosta da un'altra finestra in modalità finestra o quando un'applicazione a schermo intero è ridotta a icona, [**PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) restituirà S \_ D3DPRESENTATIONOCCLUDED. Le applicazioni a schermo intero possono riprendere il rendering quando ricevono un messaggio di callback [**\_ WM ACTIVATEAPP.**](../winmsg/wm-activateapp.md)

Nelle versioni precedenti di DirectX, quando in un'applicazione si verificava una modifica della modalità, l'unico modo per eseguire il ripristino era reimpostare il dispositivo e creare nuovamente tutte le risorse di memoria video e le catene di scambio. Con DirectX per Windows Vista, la chiamata di Reset dopo una modifica della modalità non causa la perdita delle superfici di memoria della trama, delle trame e delle informazioni sullo stato e non è necessario ricreare queste risorse.

## <a name="disabling-multithreaded-software-vertex-processing"></a>Disabilitazione dell'elaborazione di vertici software multithreading

È stato aggiunto un nuovo bit di estremità (D3DCREATE DISABLE PSGP THREADING) che disabilita il multithreading per l'elaborazione dei vertici \_ \_ software \_ (swvp). Usare questa macro per generare un flag di comportamento per IDirect3D9::CreateDevice.


```
#define D3DCREATE_DISABLE_PSGP_THREADING
```



## <a name="one-bit-surfaces"></a>One Bit Surfaces

È disponibile un nuovo tipo di formato di superficie di bit che può essere particolarmente utile per l'elaborazione di glifi di testo. Il nuovo formato è denominato D3DFMT \_ A1. Una superficie a 1 bit è progettata per essere usata come trama per pixel o come output di destinazione di rendering generato da ComposeRects o ColorFill. Non sono presenti estremità separate per la larghezza e l'altezza della superficie. Un'implementazione di deve supportare una singola superficie di 2K texel x 8K texel.

Una superficie a 1 bit ha un bit per texel; Pertanto, uno significa che tutti i componenti (r,g,b,a) di un pixel sono 1 e zero significa che tutti i componenti sono uguali a 0. È possibile usare superfici a 1 bit con le API seguenti: ColorFill, UpdateSurface e UpdateTexture.

Quando viene letta una superficie a 1 bit, il runtime può eseguire un campione di punto o un filtro di convoluzione. Il filtro di convoluzione è regolabile (vedere [**SetConvolutionMonoKernel).**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-setconvolutionmonokernel)

Esistono alcune restrizioni per le superfici a 1 bit:

-   Il mapping mip non è supportato
-   I dati sRGB non possono essere letti o scritti in una superficie a 1 bit.
-   Una superficie a 1 bit non può essere usata come trama di vertici o per il multicampionamento.

## <a name="reading-depthstencil-buffers"></a>Profondità di lettura/buffer degli stencil

Usare IDirect3DDevice9::UpdateSurface per leggere o scrivere dati di profondità/stencil dalle superfici ottenute da IDirect3DDevice9::CreateDepthStencilSurface o IDirect3DDevice9::GetDepthStencilSurface.

Creare prima di tutto una superficie bloccabile, solo profondità o stencil usando IDirect3DDevice9::CreateOffscreenPlainSurface. Utilizzare uno dei seguenti formati:

-   D3DFMT \_ D16 \_ BLOCCABILE
-   D3DFMT \_ D32F \_ LOCKABLE
-   D3DFMT \_ D32 \_ LOCKABLE
-   D3DFMT \_ S8 \_ BLOCCABILE

In secondo momento, trasferire i dati tra il buffer di profondità/stencil e la profondità bloccabile o la superficie degli stencil appena creata. Il trasferimento viene eseguito usando IDirect3DDevice9::UpdateSurface.

UpdateSurface avrà esito negativo quando entrambe le superfici sono in un formato BLOCCABILE o entrambe non sono bloccabili.

Il trasferimento di dati inesistenti restituirà un errore, ad esempio il trasferimento da una superficie non bloccabile con solo profondità a una superficie bloccabile D3DFMT \_ \_ S8.

Il resto delle restrizioni per IDirect3DDevice9::UpdateSurface è ancora applicabile.

## <a name="sharing-resources"></a>Condivisione di risorse

Le risorse Direct3D possono ora essere condivise tra dispositivi o processi. Questo vale per qualsiasi risorsa Direct3D, inclusi trame, buffer dei vertici, buffer di indice o superfici (ad esempio destinazioni di rendering, buffer depth stencil o superfici semplici fuori schermo). Per essere condivisi, è necessario designare una risorsa per la condivisione al momento della creazione e individuare la risorsa nel pool predefinito (D3DPOOL \_ DEFAULT). Una volta creata per la condivisione, una risorsa può essere condivisa tra i dispositivi all'interno di un processo o tra processi.

Per abilitare le risorse condivise, le API di creazione delle risorse hanno un parametro di handle aggiuntivo. Si tratta di un HANDLE che punta alla risorsa condivisa. Nelle revisioni precedenti di DirectX questo argomento fa parte della firma dell'API, ma non è stato usato e deve essere impostato su **NULL.** A partire Windows Vista, usare pSharedHandle nei modi seguenti:

-   Impostare il puntatore (pSharedHandle) su **NULL** per non condividere una risorsa. Questo comportamento è simile a quello di DirectX prima di Windows Vista.
-   Per creare una risorsa condivisa, chiamare qualsiasi API di creazione di risorse (vedere di seguito) con un handle non inizializzato (il puntatore stesso non è **NULL** (pSharedHandle != **NULL),** ma il puntatore punta a un **valore NULL** ( \* pSharedHandle == **NULL**)). L'API genererà una risorsa condivisa e restituirà un handle valido.
-   Per aprire e accedere a una risorsa condivisa creata in precedenza usando un handle di risorsa condivisa non NULL, impostare pSharedHandle sull'indirizzo di tale handle. Dopo aver aperto la risorsa condivisa creata in precedenza in questo modo, è possibile usare l'interfaccia restituita nell'API Direct3D 9 o Direct3D 9Ex come se l'interfaccia fosse una risorsa tipica di quel tipo.

Le API di creazione delle risorse includono [**CreateTexture**](/windows/desktop/api), [**CreateVolumeTexture**](/windows/desktop/api), [**CreateCubeTexture**](/windows/desktop/api), [**CreateRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createrendertarget), [**CreateVertexBuffer**](/windows/desktop/api), [**CreateIndexBuffer**](/windows/desktop/api), [**CreateDepthStencilSurface**](/windows/desktop/api), [**CreateOffscreenPlainSurface**](/windows/desktop/api), [**CreateDepthStencilSurfaceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-createdepthstencilsurfaceex), [**CreateOffscreenPlainSurfaceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-createoffscreenplainsurfaceex)e [**CreateRenderTargetEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-createrendertargetex).

Esistono alcune restrizioni per l'uso delle risorse condivise. Queste includono:

-   L'API usata per aprire una risorsa condivisa deve corrispondere all'API usata per creare la risorsa condivisa. Ad esempio, se è stato usato [**CreateTexture**](/windows/desktop/api) per creare una risorsa condivisa, è necessario usare **CreateTexture** per aprire la risorsa condivisa; Se è stato [**usato CreateRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createrendertarget) per creare una risorsa condivisa, è necessario usare **CreateRenderTarget** per aprire la risorsa condivisa e così via.
-   Quando si apre una risorsa condivisa, è necessario specificare D3DPOOL \_ DEFAULT.
-   Le risorse bloccabili (trame con D3DUSAGE DYNAMIC, buffer dei vertici e buffer di indice, ad esempio) possono avere prestazioni scarse \_ se condivise. Le destinazione di rendering bloccabili non verranno condivise in alcuni componenti hardware.
-   I riferimenti a una risorsa condivisa tra processi devono avere le stesse dimensioni della risorsa originale. Quando si passa un handle tra processi, includere le informazioni sulla dimensione in modo che il riferimento possa essere creato in modo identico.
-   Le superfici tra processi condivise non forniscono alcun meccanismo di sincronizzazione. Le modifiche di lettura/scrittura a una superficie condivisa potrebbero non riflettere la visualizzazione della superficie di un processo di riferimento quando previsto. Per fornire la sincronizzazione, usare query di eventi o bloccare la trama.
-   Solo il processo che crea inizialmente una risorsa condivisa può bloccarla (qualsiasi processo che apre un riferimento a tale risorsa condivisa non può bloccarla).
-   Se una risorsa condivisa è bloccata, non viene eseguita alcuna convalida per altri processi per sapere se la risorsa è disponibile.

## <a name="srgb-conversion-before-blending"></a>Conversione di sRGB prima della fusione

È ora possibile verificare se il dispositivo può convertire i dati della pipeline in sRGB prima della fusione del buffer dei frame. Ciò implica che il dispositivo converte i valori di destinazione di rendering da sRGB. Per verificare se la conversione è supportata dall'hardware, verificare questo limite:


```
D3DPMISCCAPS_POSTBLENDSRGBCONVERT
```



Questo limite identifica l'hardware che supporta la conversione in sRGB prima della fusione. Questa funzionalità è importante per il rendering di alta qualità da buffer di frame fp16 in Gestione finestre desktop (DWM).

## <a name="stretchrect-improvements"></a>Miglioramenti di StretchRect

Nelle versioni precedenti di DirectX StretchRect presenta molte restrizioni per supportare driver diversi (vedere IDirect3DDevice9::StretchRect). Windows Vista si basa sul modello Windows (WDDM). Questo nuovo modello di driver è molto più affidabile e consente ai driver di gestire casi speciali nell'hardware.

In generale, l'unica restrizione rimanente è che la destinazione di rendering deve essere stata creata con l'utilizzo della destinazione di rendering (D3DUSAGE \_ RENDERTARGET). Questa restrizione viene revocata se si sta eseguendo una copia semplice (in cui l'origine e la dest hanno lo stesso formato, le stesse dimensioni e non sono presenti rettangoli secondari).

## <a name="texture-creation-in-system-memory"></a>Creazione di trame nella memoria di sistema

Le applicazioni che necessitano di maggiore flessibilità rispetto all'uso, all'allocazione e all'eliminazione della memoria di sistema possono ora creare trame da un puntatore di memoria di sistema. Ad esempio, un'applicazione potrebbe creare una trama Direct3D da un puntatore bitmap della memoria di sistema GDI.

Per creare una trama di questo tipo, è necessario eseguire due operazioni:

-   Allocare memoria di sistema sufficiente per contenere la superficie della trama. Il numero minimo di byte è larghezza x altezza x byte per pixel.
-   Passare l'indirizzo di un puntatore alla superficie di memoria di sistema per il parametro HANDLE \* a IDirect3DDevice9::CreateTexture.

Ecco il prototipo di funzione per IDirect3DDevice9::CreateTexture:


```
STDMETHOD(CreateTexture)(THIS_ UINT Width, UINT Height, UINT Levels, 
    DWORD Usage, D3DFORMAT Format, D3DPOOL Pool, IDirect3DTexture9** ppTexture, 
    HANDLE* pSharedHandle)
```



Una trama di memoria di sistema presenta le restrizioni seguenti:

-   L'altezza della trama deve essere uguale alla larghezza della trama per il numero di byte per pixel.
-   Quando si usano formati compressi (formati DXT), l'applicazione è responsabile dell'allocazione delle dimensioni corrette.
-   Sono supportate solo trame con un singolo livello mipmap.
-   Il valore passato a CreateTexture per l'argomento Pool deve essere D3DPOOL \_ SYSTEMMEM.
-   Questa API esegue il wrapping della memoria fornita in una trama. Non deallocare questa memoria fino a quando non è stata completata.

 

 
