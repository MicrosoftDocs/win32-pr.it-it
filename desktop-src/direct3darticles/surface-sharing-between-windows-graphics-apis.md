---
title: Condivisione della superficie tra le API di grafica Windows
description: Questo argomento fornisce una panoramica tecnica dell'interoperabilità con la condivisione della superficie tra API di grafica Windows, tra cui Direct3D 11, Direct2D, DirectWrite, Direct3D 10 e Direct3D 9Ex.
ms.assetid: 65abf33e-3d15-42ff-99bd-674f24da773e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d889797902c964e603adefc51b25039afca7d46
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/01/2020
ms.locfileid: "103730762"
---
# <a name="surface-sharing-between-windows-graphics-apis"></a>Condivisione della superficie tra le API di grafica Windows

Questo argomento fornisce una panoramica tecnica dell'interoperabilità con la condivisione della superficie tra API di grafica Windows, tra cui Direct3D 11, Direct2D, DirectWrite, Direct3D 10 e Direct3D 9Ex. Se si ha già una conoscenza approfondita di queste API, questo documento consente di usare più API per eseguire il rendering nella stessa area in un'applicazione progettata per i sistemi operativi Windows 7 o Windows Vista. Questo argomento fornisce anche le linee guida per le procedure consigliate e i puntatori a risorse aggiuntive.

> [!Note]  
> Per l'interoperabilità Direct2D e DirectWrite nel runtime di DirectX 11,1, è possibile usare i [dispositivi Direct2D e i contesti di dispositivo](/windows/desktop/Direct2D/devices-and-device-contexts) per eseguire il rendering direttamente nei dispositivi Direct3D 11.

 

In questo argomento sono contenute le sezioni seguenti.

-   [Introduzione](#introduction)
-   [Panoramica dell'interoperabilità API](#api-interoperability-overview)
-   [Scenari di interoperabilità](#interoperability-scenarios)
    -   [Condivisione di dispositivi Direct3D 10,1 con Direct2D](#direct3d-101-device-sharing-with-direct2d)
    -   [DXGI 1,1-superfici condivise sincronizzate](#dxgi-11-synchronized-shared-surfaces)
    -   [Interoperabilità tra Direct3D 9Ex e le API basate su DXGI](#interoperability-between-direct3d-9ex-and-dxgi-based-apis)
-   [Conclusione](#conclusion)

## <a name="introduction"></a>Introduzione

In questo documento, l'interoperabilità dell'API grafica di Windows si riferisce alla condivisione della stessa superficie di rendering da diverse API. Questo tipo di interoperabilità consente alle applicazioni di creare visualizzazioni accattivanti sfruttando più API grafiche di Windows e di semplificare la migrazione alle nuove tecnologie mantenendo la compatibilità con le API esistenti.

In Windows 7 (e Windows Vista SP2 con Windows 7 Interop Pack, vista 7IP), le API di rendering della grafica sono Direct3D 11, Direct2D, Direct3D 10,1, Direct3D 10,0, Direct3D 9Ex, Direct3D 9C e le API Direct3D precedenti, nonché GDI e GDI+. Windows Imaging Component (WIC) e DirectWrite sono tecnologie correlate per l'elaborazione di immagini e Direct2D esegue il rendering del testo. DirectX Video Acceleration API (DXVA), basato su Direct3D 9C e Direct3D 9Ex, viene usato per l'elaborazione video.

Poiché le API di grafica Windows si evolvono in base a Direct3D, Microsoft investe più sforzi per garantire l'interoperabilità tra le API. Le API Direct3D appena sviluppate e le API di livello superiore basate sulle API Direct3D forniscono anche il supporto per la compatibilità con le API precedenti. Per illustrare, le applicazioni Direct2D possono usare Direct3D 10,1 condividendo un dispositivo Direct3D 10,1. Inoltre, le API Direct3D 11, Direct2D e Direct3D 10,1 possono sfruttare tutti i vantaggi offerti da DirectX Graphics Infrastructure (DXGI) 1,1, che consente l'uso di superfici condivise sincronizzate che supportano completamente l'interoperabilità tra queste API. Le API basate su DXGI 1,1 interagiscono con GDI e con GDI+ per associazione, ottenendo il contesto di dispositivo GDI da una superficie di DXGI 1,1. Per ulteriori informazioni, vedere la documentazione relativa all'interoperabilità DXGI e GDI disponibile in MSDN.

La condivisione di superficie non sincronizzata è supportata dal runtime 9Ex di Direct3D. Le applicazioni video basate su DXVA possono usare l'helper Direct3D 9Ex e DXGI Interoperability per l'interoperabilità DXVA basata su Direct3D 9Ex con Direct3D 11 per compute shader oppure possono interagire con Direct2D per i controlli 2D o il rendering del testo. WIC e DirectWrite interagiscono anche con GDI, Direct2D e per associazione, altre API Direct3D.

Direct3D 10,0, Direct3D 9C e i runtime Direct3D precedenti non supportano le aree condivise. Le copie di memoria di sistema continueranno a essere usate per l'interoperabilità con le API basate su GDI o DXGI.

Si noti che gli scenari di interoperabilità all'interno di questo documento si riferiscono al rendering di più API grafiche in una superficie di rendering condivisa anziché alla stessa finestra dell'applicazione. La sincronizzazione per le API separate destinate a superfici diverse che vengono quindi composite nella stessa finestra esula dall'ambito di questo documento.

## <a name="api-interoperability-overview"></a>Panoramica dell'interoperabilità API

L'interoperabilità della condivisione della superficie delle API di grafica Windows può essere descritta in termini di scenari da API ad API e della corrispondente funzionalità di interoperabilità. A partire da Windows 7 e a partire da Windows Vista SP2 con 7IP, le nuove API e i runtime associati includono Direct2D e le tecnologie correlate: Direct3D 11 e DXGI 1,1. Anche le prestazioni GDI sono state migliorate in Windows 7. Direct3D 10,1 è stato introdotto in Windows Vista SP1. Il diagramma seguente illustra il supporto per l'interoperabilità tra le API.

![diagramma del supporto per l'interoperabilità tra API di grafica Windows](images/surface-sharing-interoperability.png)

In questo diagramma, le frecce mostrano scenari di interoperabilità in cui la stessa superficie può essere accessibile dalle API connesse. Le frecce blu indicano i meccanismi di interoperabilità introdotti in Windows Vista. Le frecce verdi indicano il supporto dell'interoperabilità per nuove API o miglioramenti che consentono alle API precedenti di interagire con le API più recenti. Ad esempio, le frecce verdi rappresentano la condivisione dei dispositivi, il supporto della superficie condivisa sincronizzata, l'helper di sincronizzazione 9Ex/DXGI di Direct3D e il recupero di un contesto di dispositivo GDI da una superficie compatibile.

## <a name="interoperability-scenarios"></a>Scenari di interoperabilità

A partire da Windows 7 e Windows Vista 7IP, le offerte mainstream delle API di grafica Windows supportano il rendering di più API nella stessa superficie DXGI 1,1.

**Direct3D 11, Direct3D 10,1, Direct2D-interoperabilità tra loro**

Le API Direct3D 11, Direct3D 10,1 e Direct2D (e le relative API, ad esempio DirectWrite e WIC) possono interagire tra loro tramite la condivisione di dispositivi Direct3D 10,1 o le superfici condivise sincronizzate.

### <a name="direct3d-101-device-sharing-with-direct2d"></a>Condivisione di dispositivi Direct3D 10,1 con Direct2D

La condivisione dei dispositivi tra Direct2D e Direct3D 10,1 consente a un'applicazione di usare entrambe le API per eseguire il rendering in modo semplice ed efficiente sulla stessa superficie DXGI 1,1, usando lo stesso oggetto dispositivo Direct3D sottostante. Direct2D consente di chiamare le API Direct2D usando un dispositivo Direct3D 10,1 esistente, sfruttando il fatto che Direct2D è basato sui runtime Direct3D 10,1 e DXGI 1,1. I frammenti di codice seguenti illustrano il modo in cui Direct2D ottiene la destinazione di rendering del dispositivo Direct3D 10,1 da una superficie DXGI 1,1 associata al dispositivo. La destinazione di rendering del dispositivo Direct3D 10,1 può eseguire chiamate di disegno Direct2D tra le API BeginDraw e EndDraw.


```C++
// Direct3D 10.1 Device and Swapchain creation
HRESULT hr = D3D10CreateDeviceandSwapChain1(
                pAdapter,
                DriverType,
                Software,
                D3D10_CREATE_DEVICE_BGRA_SUPPORT,
                featureLevel,
                D3D10_1_SDK_VERSION,
                pSwapChainDesc,
                &pSwapChain,
                &pDevice
                );

hr = pSwapChain->GetBuffer(
        0,
        __uuidof(IDXGISurface),
        (void **)&pDXGIBackBuffer
        ));

// Direct3D 10.1 API rendering calls
...

hr = D2D1CreateFactory(
        D2D1_FACTORY_TYPE_SINGLE_THREADED,
        &m_spD2DFactory
        ));

pD2DFactory->CreateDxgiSurfaceRenderTarget(
        pDXGIBackBuffer,
        &renderTargetProperties,
        &pD2DBackBufferRenderTarget
        ));
...

pD2DBackBufferRenderTarget->BeginDraw();
//Direct2D API rendering calls
...

pD2DBackBufferRenderTarget->EndDraw();

pSwapChain->Present(0, 0);
```



**Osservazioni:**

-   Il dispositivo Direct3D 10,1 associato deve supportare il formato BGRA. Il dispositivo è stato creato chiamando D3D10CreateDevice1 con il parametro D3D10 per \_ creare il \_ \_ supporto BGRA del dispositivo \_ . Il formato BGRA è supportato a partire dal livello di funzionalità Direct3D 10 9,1.
-   L'applicazione non deve creare più ID2D1RenderTargets associati allo stesso dispositivo Direct3D 10.1.
-   Per ottenere prestazioni ottimali, è possibile gestire almeno una risorsa in qualsiasi momento, ad esempio trame o superfici associate al dispositivo.

La condivisione dei dispositivi è adatta per l'utilizzo a thread singolo in-process di un dispositivo di rendering condiviso dalle API per il rendering Direct3D 10,1 e Direct2D. Le superfici condivise sincronizzate consentono l'utilizzo multithread, in-process e out-of-process di più dispositivi di rendering usati dalle API Direct3D 10,1, Direct2D e Direct3D 11.

Un altro metodo per l'interoperabilità di Direct3D 10,1 e Direct2D consiste nell'usare ID3D1RenderTarget:: CreateSharedBitmap, che crea un oggetto ID2D1Bitmap da IDXGISurface. È possibile scrivere una scena Direct3D 10.1 nella bitmap ed eseguirne il rendering con Direct2D. Per ulteriori informazioni, vedere [ID2D1RenderTarget:: CreateSharedBitmap Method](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap).

### <a name="direct2d-software-rasterization"></a>Rasterizzazione del software Direct2D

La condivisione di dispositivi con Direct3D 10,1 non è supportata quando si usa il renderer del software Direct2D, ad esempio, specificando l'utilizzo della destinazione di rendering D2D1 per il \_ \_ \_ \_ \_ \_ rendering del software nell'utilizzo della destinazione di rendering d2d1 \_ \_ \_ durante la creazione di una destinazione di rendering Direct2D.

Direct2D può usare l'rasterizzatore software WARP10 per condividere il dispositivo con Direct3D 10 o Direct3D 11, ma le prestazioni diminuiscono significativamente.

### <a name="dxgi-11-synchronized-shared-surfaces"></a>DXGI 1,1-superfici condivise sincronizzate

Le API Direct3D 11, Direct3D 10,1 e Direct2D utilizzano tutti DXGI 1,1, che fornisce la funzionalità per sincronizzare la lettura e la scrittura nella stessa area di memoria video (DXGISurface1) da due o più dispositivi Direct3D. I dispositivi di rendering che usano superfici condivise sincronizzate possono essere dispositivi Direct3D 10,1 o Direct3D 11, ognuno in esecuzione nello stesso processo o tra processi.

Le applicazioni possono usare superfici condivise sincronizzate per interoperare tra qualsiasi dispositivo basato su DXGI 1,1, ad esempio Direct3D 11 e Direct3D 10,1, oppure tra Direct3D 11 e Direct2D, ottenendo il dispositivo Direct3D 10,1 dall'oggetto di destinazione di rendering Direct2D.

Nelle API Direct3D 10,1 e versioni successive, per usare DXGI 1,1, verificare che il dispositivo Direct3D venga creato usando un oggetto adattatore DXGI 1,1, che viene enumerato dall'oggetto Factory DXGI 1,1. Chiamare CreateDXGIFactory1 per creare l'oggetto IDXGIFactory1 e EnumAdapters1 per enumerare l'oggetto IDXGIAdapter1. È necessario passare l'oggetto IDXGIAdapter1 come parte della chiamata a D3D10CreateDevice o D3D10CreateDeviceAndSwapChain. Per ulteriori informazioni sulle API DXGI 1,1, consultare la guida alla [programmazione di DXGI](https://msdn.microsoft.com/library/ee418147(VS.85).aspx).

### <a name="apis"></a>API

**D3D10 \_ risorse \_ varie \_ \_ KEYEDMUTEX condivise**  
Quando si crea la risorsa condivisa sincronizzata, impostare D3D10 \_ risorse \_ varie \_ \_ KEYEDMUTEX in \_ flag varie della risorsa D3D10 \_ \_ .  


```C++
typedef enum D3D10_RESOURCE_MISC_FLAG {
    D3D10_RESOURCE_MISC_GENERATE_MIPS      = 0x1L,
    D3D10_RESOURCE_MISC_SHARED             = 0x2L,
    D3D10_RESOURCE_MISC_TEXTURECUBE        = 0x4L,
    D3D10_RESOURCE_MISC_SHARED_KEYEDMUTEX  = 0x10L,
    D3D10_RESOURCE_MISC_GDI_COMPATIBLE     = 0x20L,
}   D3D10_RESOURCE_MISC_FLAG;
```



**D3D10 \_ risorse \_ varie \_ \_ KEYEDMUTEX condivise**  
Consente la sincronizzazione della risorsa creata usando le API IDXGIKeyedMutex:: AcquireSync e ReleaseSync. Le seguenti API per la creazione di risorse Direct3D 10,1 che accettano \_ un \_ parametro del flag varie della risorsa D3D10 \_ sono state estese per supportare il nuovo flag.  

-   ID3D10Device1::CreateTexture1D
-   ID3D10Device1::CreateTexture2D
-   ID3D10Device1::CreateTexture3D
-   ID3D10Device1:: CreateBuffer

  
Se una qualsiasi delle funzioni elencate viene chiamata con il \_ \_ \_ flag KEYEDMUTEX condiviso di D3D10 varie \_ , l'interfaccia restituita può essere sottoposta a query per un'interfaccia IDXGIKeyedMutex che implementa le API AcquireSync e ReleaseSync per sincronizzare l'accesso alla superficie. Il dispositivo che crea la superficie e qualsiasi altro dispositivo che apre la superficie (usando OpenSharedResource) è necessario per chiamare IDXGIKeyedMutex:: AcquireSync prima di qualsiasi comando di rendering sulla superficie e IDXGIKeyedMutex:: ReleaseSync al termine del rendering.  
I dispositivi WARP e REF non supportano le risorse condivise. Il tentativo di creare una risorsa con questo flag in un dispositivo WARP o REF provocherà la restituzione di un codice di errore E OutOfMemory da parte del metodo Create \_ .  
**INTERFACCIA IDXGIKEYEDMUTEX**  
Una nuova interfaccia in DXGI 1,1, IDXGIKeyedMutex, rappresenta un mutex con chiave, che consente l'accesso esclusivo a una risorsa condivisa usata da più dispositivi. Per la documentazione di riferimento relativa a questa interfaccia e ai relativi due metodi, AcquireSync e ReleaseSync, vedere [IDXGIKeyedMutex](https://msdn.microsoft.com/library/ee421920(VS.85).aspx).  
</dl>

### <a name="sample-synchronized-surface-sharing-between-two-direct3d-101-devices"></a>Esempio: condivisione della superficie sincronizzata tra due dispositivi Direct3D 10,1

Nell'esempio seguente viene illustrata la condivisione di una superficie tra due dispositivi Direct3D 10,1. La superficie condivisa sincronizzata viene creata da un dispositivo Direct3D 10.1.


```C++
// Create Sync Shared Surface using Direct3D10.1 Device 1.
D3D10_TEXTURE2D_DESC desc;
ZeroMemory( &desc, sizeof(desc) );
desc.Width = width;
desc.Height = height;
desc.MipLevels = 1;
desc.ArraySize = 1;
// must match swapchain format in order to CopySubresourceRegion.
desc.Format = DXGI_FORMAT_R8G8B8A8_UNORM;
desc.SampleDesc.Count = 1;
desc.Usage = D3D10_USAGE_DEFAULT;
// creates 2D texture as a Synchronized Shared Surface.
desc.MiscFlags = D3D10_RESOURCE_MISC_SHARED_KEYEDMUTEX;
desc.BindFlags = D3D10_BIND_RENDER_TARGET | D3D10_BIND_SHADER_RESOURCE;
ID3D10Texture2D* g_pShared = NULL;
g_pd3dDevice1->CreateTexture2D( &desc, NULL, &g_pShared );

// QI IDXGIResource interface to synchronized shared surface.
IDXGIResource* pDXGIResource = NULL;
g_pShared->QueryInterface(__uuidof(IDXGIResource), (LPVOID*) &pDXGIResource);

// obtain handle to IDXGIResource object.
pDXGIResource->GetSharedHandle(&g_hsharedHandle);
pDXGIResource->Release();
if ( !g_hsharedHandle )
    return E_FAIL;

// QI IDXGIKeyedMutex interface of synchronized shared surface's resource handle.
hr = g_pShared->QueryInterface( __uuidof(IDXGIKeyedMutex),
    (LPVOID*)&g_pDXGIKeyedMutex_dev1 );
If ( FAILED( hr ) || ( g_pDXGIKeyedMutex_dev1 == NULL ) )
    return E_FAIL;
```



Lo stesso dispositivo Direct3D 10.1 può ottenere la superficie condivisa sincronizzata per il rendering chiamando AcquireSync, quindi rilasciando la superficie per il rendering dell'altro dispositivo chiamando ReleaseSync. Quando non si condivide la superficie condivisa sincronizzata con qualsiasi altro dispositivo Direct3D, l'autore può ottenere e rilasciare la superficie condivisa sincronizzata (per iniziare e terminare il rendering) acquisendo e rilasciando con lo stesso valore di chiave.


```C++
// Obtain handle to Sync Shared Surface created by Direct3D10.1 Device 1.
hr = g_pd3dDevice2->OpenSharedResource( g_hsharedHandle,__uuidof(ID3D10Texture2D),
                                        (LPVOID*) &g_pdev2Shared);
if (FAILED (hr))
    return hr;
hr = g_pdev2Shared->QueryInterface( __uuidof(IDXGIKeyedMutex),
                                    (LPVOID*) &g_pDXGIKeyedMutex_dev2);
if( FAILED( hr ) || ( g_pDXGIKeyedMutex_dev2 == NULL ) )
    return E_FAIL;

// Rendering onto Sync Shared Surface from D3D10.1 Device 1 using D3D10.1 Device 2.
UINT acqKey = 1;
UINT relKey = 0;
DWORD timeOut = 5;
DWORD result = g_pDXGIKeyedMutex_dev2->AcquireSync(acqKey, timeOut);
if ( result == WAIT_OBJECT_0 )
    // Rendering calls using Device 2.
else
    // Handle unable to acquire shared surface error.
result = g_pDXGIKeyedMutex_dev2->ReleaseSync(relKey));
if (result == WAIT_OBJECT_0)
    return S_OK;
```



Il secondo dispositivo Direct3D 10.1 può ottenere la superficie condivisa sincronizzata per il rendering chiamando AcquireSync, quindi rilasciando la superficie per il rendering del primo dispositivo chiamando ReleaseSync. Si noti che il dispositivo 2 è in grado di acquisire la superficie condivisa sincronizzata usando lo stesso valore chiave di quello specificato nella chiamata ReleaseSync dal dispositivo 1.


```C++
// Rendering onto Sync Shared Surface from D3D10.1 Device 1 using D3D10.1 Device 1.
UINT acqKey = 0;
UINT relKey = 1;
DWORD timeOut = 5;
DWORD result = g_pDXGIKeyedMutex_dev1->AcquireSync(acqKey, timeOut);
if (result == WAIT_OBJECT_0)
    // Rendering calls using Device 1.
else
    // Handle unable to acquire shared surface error.
result = g_pDXGIKeyedMutex_dev1->ReleaseSync(relKey));
if ( result == WAIT_OBJECT_0 )
    return S_OK;
```



I dispositivi aggiuntivi che condividono la stessa superficie possono richiedere l'acquisizione e il rilascio della superficie usando chiavi aggiuntive, come illustrato nelle chiamate seguenti.


```C++
// Within Device 1's process/thread:
// Rendering onto Sync Shared Surface from D3D10.1 Device 1 using D3D10.1 Device 1
result = g_pDXGIKeyedMutex_dev1->AcquireSync(0, timeOut);
// Rendering calls using Device 1
...
result = g_pDXGIKeyedMutex_dev1->ReleaseSync(1);
...
////////////////////////////////////////////////////////////////////////////
// Within Device 2's process/thread:
// Rendering onto Sync Shared Surface from D3D10.1 Device 1 using D3D10.1 Device 2
result = g_pDXGIKeyedMutex_dev2->AcquireSync(1, timeOut);
// Rendering calls using Device 2
...
result = g_pDXGIKeyedMutex_dev1->ReleaseSync(2);

////////////////////////////////////////////////////////////////////////////
// Within Device 3's process/thread:
// Rendering onto Sync Shared Surface from D3D10.1 Device 1 using D3D10.1 Device 3
result = g_pDXGIKeyedMutex_dev1->AcquireSync(2, timeOut);
// Rendering calls using Device 3
...
result = g_pDXGIKeyedMutex_dev1->ReleaseSync(0);
...
```



Si noti che un'applicazione reale può sempre eseguire il rendering in una superficie intermedia che viene quindi copiata nella superficie condivisa per evitare che un dispositivo sia in attesa di un altro dispositivo che condivide la superficie.

### <a name="using-synchronized-shared-surfaces-with-direct2d-and-direct3d-11"></a>Uso di superfici condivise sincronizzate con Direct2D e Direct3D 11

Analogamente, per la condivisione tra le API Direct3D 11 e Direct3D 10,1, è possibile creare una superficie condivisa sincronizzata dal dispositivo API e condividerla con gli altri dispositivi API, in o out-of-process.

Le applicazioni che utilizzano Direct2D possono condividere un dispositivo Direct3D 10,1 e utilizzare una superficie condivisa sincronizzata per interagire con Direct3D 11 o altri dispositivi Direct3D 10,1, che appartengano allo stesso processo o a processi diversi. Tuttavia, per le applicazioni a thread singolo a singolo processo, la condivisione dei dispositivi è il metodo di interoperabilità più elevato ed efficiente tra Direct2D e Direct3D 10 o Direct3D 11.

### <a name="software-rasterizer"></a>Rasterizzatore software

Le superfici condivise sincronizzate non sono supportate se le applicazioni usano i rasterizzatori software Direct3D o Direct2D, inclusi l'rasterizzatore dei riferimenti e la DISTORSIONe, invece di usare l'accelerazione hardware grafica.

### <a name="interoperability-between-direct3d-9ex-and-dxgi-based-apis"></a>Interoperabilità tra Direct3D 9Ex e le API basate su DXGI

Le API Direct3D 9Ex includono la nozione di condivisione della superficie per consentire ad altre API di leggere dalla superficie condivisa. Per condividere la lettura e la scrittura in una superficie condivisa Direct3D 9Ex, è necessario aggiungere la sincronizzazione manuale all'applicazione stessa.

### <a name="direct3d-9ex-shared-surfaces-plus-manual-synchronization-helper"></a>Direct3D 9Ex Shared Surfaces Plus Manual Synchronization Helper

L'attività più fondamentale nell'interoperabilità di Direct3D 9Ex e Direct3D 10 o 11 è il passaggio di una singola superficie dal primo dispositivo (dispositivo A) al secondo (dispositivo B), in modo che quando il dispositivo B acquisisce un handle sulla superficie, il rendering del dispositivo A è garantito che sia stato completato. Quindi, il dispositivo B può usare questa superficie senza preoccuparsi. Si tratta di un problema molto simile a quello di producer-consumer classico e questa discussione modella il problema in questo modo. Il primo dispositivo che usa la superficie e quindi lo cede è il produttore (dispositivo A) e il dispositivo che inizialmente è in attesa è il consumer (dispositivo B). Tutte le applicazioni reali sono più sofisticate e concatenano più blocchi predefiniti producer-consumer per creare le funzionalità desiderate.

I blocchi predefiniti producer-consumer vengono implementati nell'helper utilizzando una coda di superfici. Le superfici vengono accodate dal Producer ed eliminate dalla coda da parte del consumer. L'helper introduce tre interfacce COM: ISurfaceQueue, ISurfaceProducer e ISurfaceConsumer.

### <a name="high-level-overview-of-helper"></a>High-Level Panoramica dell'helper

L'oggetto ISurfaceQueue è il blocco predefinito per l'utilizzo delle superfici condivise. Viene creato con un dispositivo Direct3D inizializzato e una descrizione per creare un numero fisso di superfici condivise. L'oggetto Queue gestisce la creazione delle risorse e l'apertura del codice. Il numero e il tipo di superfici sono fissi; una volta create le superfici, l'applicazione non può aggiungerle o rimuoverle.

Ogni istanza dell'oggetto ISurfaceQueue fornisce un tipo di strada unidirezionale che può essere usata per inviare le superfici dal dispositivo producente al dispositivo consumer. È possibile utilizzare più strade unidirezionali per abilitare scenari di condivisione di superficie tra dispositivi di applicazioni specifiche.

**Creazione/durata degli oggetti**  
Esistono due modi per creare l'oggetto Queue: tramite CreateSurfaceQueue o tramite il metodo clone di ISurfaceQueue. Poiché le interfacce sono oggetti COM, viene applicata la gestione della durata COM standard.  
**Modello producer/consumer**  
Accoda (): il producer chiama questa funzione per indicare che viene eseguita con la superficie, che ora può diventare disponibile per un altro dispositivo. Al ritorno da questa funzione, il dispositivo Producer non dispone più dei diritti per la superficie e non è sicuro continuare a usarlo.  
Dequeue (): il dispositivo consumer chiama questa funzione per ottenere una superficie condivisa. L'API garantisce che eventuali superfici rimossi dalla coda siano pronte per essere utilizzate.  
**Metadata**  
L'API supporta l'associazione di metadati con le aree condivise.  
Accodamento () consente di specificare metadati aggiuntivi che verranno passati al dispositivo consumer. I metadati devono essere inferiori a un valore massimo noto al momento della creazione.  
La funzione di rimozione dalla coda () può facoltativamente passare un buffer e un puntatore alla dimensione del buffer. La coda riempie il buffer con i metadati della chiamata di Accodamento corrispondente.  
**Clonazione**  
Ogni oggetto ISurfaceQueue risolve una sincronizzazione unidirezionale. Si presuppone che la maggior parte delle applicazioni che usano questa API utilizzerà un sistema chiuso. Il sistema chiuso più semplice con due dispositivi che inviano superfici in avanti e indietro richiede due code. L'oggetto ISurfaceQueue dispone di un metodo Clone () che rende possibile la creazione di più code che fanno parte della stessa pipeline di dimensioni maggiori.  
Clone crea un nuovo oggetto ISurfaceQueue da uno esistente e condivide tutte le risorse aperte tra di essi. L'oggetto risultante ha esattamente le stesse superfici della coda di origine. Le code clonate possono avere dimensioni dei metadati diverse l'una dall'altra.  
**Superfici**  
Il ISurfaceQueue si assume la responsabilità di creare e gestire le relative superfici. Non è valido per l'accodamento di superfici arbitrarie. Inoltre, una superficie deve avere solo un "proprietario" attivo. Deve trovarsi in una coda specifica o essere usata da un dispositivo specifico. Non è possibile utilizzarlo in più code o per i dispositivi per continuare a utilizzare la superficie dopo l'accodamento.  
</dl>

### <a name="api-details"></a>Dettagli API

### <a name="isurfacequeue"></a>IsurfaceQueue

La coda è responsabile della creazione e della gestione delle risorse condivise. Fornisce anche la funzionalità per concatenare più code usando Clone. La coda dispone di metodi che aprono il dispositivo producente e un dispositivo consumer. È possibile aprire solo uno di ciascuno di essi in qualsiasi momento.

La coda espone le API seguenti:



|                             |                                                                                  |
|-----------------------------|----------------------------------------------------------------------------------|
| CreateSurfaceQueue          | Crea un oggetto ISurfaceQueue (coda "radice").                              |
| ISurfaceQueue::OpenConsumer | Restituisce un'interfaccia per il dispositivo che utilizza la rimozione dalla coda.                        |
| ISurfaceQueue::OpenProducer | Restituisce un'interfaccia per il dispositivo di produzione da accodare.                        |
| ISurfaceQueue:: Clone        | Crea un oggetto ISurfaceQueue che condivide le superfici con l'oggetto coda radice. |



 

**CreateSurfaceQueue**  


```C++
typedef struct SURFACE_QUEUE_DESC {
  UINT            Width;
  UINT            Height;
  DXGI_FORMAT     Format;
  UINT            NumSurfaces;
  UINT            MetaDataSize;
  DWORD           Flags;
} SURFACE_QUEUE_DESC;
```



**Members**  

**Larghezza**, **altezza**  delle dimensioni delle superfici condivise. Tutte le superfici condivise devono avere le stesse dimensioni.  
**Formato** Formato delle superfici condivise. Tutte le superfici condivise devono avere lo stesso formato. I formati validi dipendono dai dispositivi che verranno usati, perché diverse coppie di dispositivi possono condividere tipi di formato diversi.  
**NumSurfaces**  Numero di superfici che fanno parte della coda. Si tratta di un numero fisso.  
 **MetaDataSize**  Dimensione massima del buffer dei metadati.  
**Flag**  Flag per controllare il comportamento della coda. Vedere la sezione Osservazioni.  



```C++
HRESULT CreateSurfaceQueue(
  [in]   SURFACE_QUEUE_DESC *pDesc,
  [in]   IUnknown *pDevice,
  [out]  IDXGIXSurfaceQueue **ppQueue
);
```



**Parametri**

 *pDesc* \[ nella \]  Descrizione della coda della superficie condivisa da creare.  

 *PDEVICE* \[ nel \]  dispositivo da usare per creare le aree condivise. Si tratta di un parametro esplicito a causa di una funzionalità di Windows Vista. Per le superfici condivise tra Direct3D 9 e Direct3D 10, è necessario creare le superfici con Direct3D 9.  

 *ppQueue* \[ out \]  al ritorno, contiene un puntatore all'oggetto ISurfaceQueue.  


**Valori restituiti**

Se *PDEVICE* non è in grado di condividere le risorse, questa funzione restituisce l' \_ errore DXGI \_ chiamata non valida \_ . Questa funzione crea le risorse. Se ha esito negativo, viene restituito un errore. Se ha esito positivo, restituisce S \_ OK.

**Osservazioni:**

La creazione dell'oggetto Queue crea anche tutte le superfici. Si presuppone che tutte le superfici siano destinazioni di rendering 2D e verranno create con la \_ destinazione di rendering bind D3D10 \_ \_ e D3D10 \_ Bind \_ shader \_ resource flags set (o i flag equivalenti per i diversi Runtime).

Lo sviluppatore può specificare un flag che indica se la coda sarà accessibile da più thread. Se non è impostato alcun flag (**Flags** = = 0), la coda verrà utilizzata da più thread. Lo sviluppatore può specificare l'accesso a thread singolo, che disattiva il codice di sincronizzazione e fornisce un miglioramento delle prestazioni per questi casi. Ogni coda clonata dispone di un proprio flag, pertanto è possibile che diverse code del sistema dispongano di diversi controlli di sincronizzazione.

 **Aprire un Producer**  


```C++
HRESULT OpenProducer(
  [in]   IUnknown *pDevice,
  [out]  IDXGIXSurfaceProducer **ppProducer
);
```



**Parametri**  

*PDEVICE* \[ in\]  

Il dispositivo Producer che accoda le superfici nella coda della superficie. 

*ppProducer* \[ out \] restituisce un oggetto all'interfaccia Producer.  


**Valori restituiti**

Se il dispositivo non è in grado di condividere le superfici, restituisce l' \_ errore DXGI \_ chiamata non valida \_ .

**Apri un consumer**  


```C++
HRESULT OpenConsumer(
  [in]   IUnknown *pDevice,
  [out]  IDXGIXSurfaceConsumer **ppConsumer
);
```



**Parametri**  
 *PDEVICE* \[ in\]  
 Il dispositivo consumer che rimuove le superfici dalla coda della superficie. 
 *ppConsumer* \[ out \]  restituisce un oggetto all'interfaccia utente.  


**Valori restituiti**

Se il dispositivo non è in grado di condividere le superfici, restituisce l' \_ errore DXGI \_ chiamata non valida \_ .

**Osservazioni:**

Questa funzione apre tutte le superfici nella coda per il dispositivo di input e le memorizza nella cache. Le chiamate successive alla rimozione dalla coda passeranno semplicemente alla cache e non dovranno riaprirle ogni volta.



### <a name="cloning-an-idxgixsurfacequeue"></a>Clonazione di un IDXGIXSurfaceQueue




```C++
typedef struct SHARED_SURFACE_QUEUE_CLONE_DESC {
  UINT         MetaDataSize;
  DWORD        Flags;
} SHARED_SURFACE_QUEUE_CLONE_DESC;
```



I **membri** **MetaDataSize** e **Flags** hanno lo stesso comportamento di CreateSurfaceQueue.  



```C++
HRESULT Clone(
  [in]   SHARED_SURFACE_QUEUE_CLONE_DESC *pDesc,
  [out]  IDXGIXSurfaceQueue **ppQueue
);
```



**Parametri**

*pDesc* \[ in \] uno struct che fornisce una descrizione dell'oggetto clone da creare. Questo parametro deve essere inizializzato.  
*ppQueue* \[ out \] restituisce l'oggetto inizializzato.  
</dl>

**Osservazioni:**

È possibile clonare da qualsiasi oggetto Queue esistente, anche se non è la radice.  
</dl>

### <a name="idxgixsurfaceconsumer"></a>IDXGIXSurfaceConsumer

<dl>


```C++
HRESULT Dequeue(
  [in]      REFIID    id,
  [out]     void      **ppSurface,
  [in,out]  void      *pBuffer,
  [in,out]  UINT      *pBufferSize,
  [in]      DWORD     dwTimeout
);
```



**Parametri**  
*ID* \[ in\]  
REFIID di una superficie 2D del dispositivo consumer.  

-   Per IDirect3DDevice9, REFIID deve essere \_ \_ uuidof (IDirect3DTexture9).
-   Per ID3D10Device, REFIID deve essere \_ \_ uuidof (ID3D10Texture2D).
-   Per ID3D11Device, REFIID deve essere \_ \_ uuidof (ID3D11Texture2D).

*ppSurface* \[ out \] restituisce un puntatore alla superficie.  
*pbuffer* \[ in, out \] an optional parametro e If Not **null**, in return, contiene i metadati passati alla chiamata di Accodamento corrispondente.  
*pBufferSize* \[ in, out \] The size of *pbuffer*, in bytes. Restituisce il numero di byte restituiti in *pbuffer*. Se la chiamata di Accodamento non ha fornito metadati, *pbuffer* è impostato su 0.  
*dwTimeOut* \[ in \] specifica un valore di timeout. Per ulteriori informazioni, vedere la sezione Osservazioni.  
</dl>

**Valori restituiti**

Questa funzione può restituire il \_ timeout di attesa se viene specificato un valore di timeout e la funzione non restituisce prima del valore di timeout. Vedere la sezione Osservazioni. Se non sono disponibili superfici, la funzione restituisce con *ppSurface* impostato su **null**, *pBufferSize* impostato su 0 e il valore restituito è 0x80070120 ( \_ da Win32 a \_ HRESULT ( \_ timeout di attesa)).  
</dl>

**Osservazioni:**

Questa API può bloccare se la coda è vuota. Il parametro *dwTimeOut* funziona in modo identico alle API di sincronizzazione di Windows, ad esempio WaitForSingleObject. Per il comportamento non di blocco, usare un timeout di 0.  
</dl>

### <a name="isurfaceproducer"></a>ISurfaceProducer

Questa interfaccia fornisce due metodi che consentono all'app di accodare le superfici. Dopo l'accodamento di una superficie, il puntatore della superficie non è più valido e non è sicuro da usare. L'unica azione che l'applicazione deve eseguire con il puntatore è rilasciarla.



|                           |                                                                                                                                                       |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| ISurfaceProducer:: Accoda | Accoda una superficie all'oggetto Queue. Al termine della chiamata, il producer viene eseguito con la superficie e la superficie è pronta per un altro dispositivo. |
| ISurfaceProducer:: Flush   | Utilizzato se le applicazioni devono avere un comportamento non bloccante. Per ulteriori informazioni, vedere Note.                                                                  |



 

**Accodamento**  


```C++
HRESULT Enqueue(
  [in]  IUnknown *pSurface,
  [in]  void *pBuffer,
  [in]  UINT BufferSize,
  [in]  DWORD Flags
);
```



**Parametri**  
*pSurface* \[ in\]  
Superficie del dispositivo di produzione da accodare. Questa superficie deve essere una superficie rimossi dalla coda dalla stessa rete di Accodamento. *pbuffer* \[ in \] un parametro facoltativo, utilizzato per passare i metadati. Deve puntare ai dati che verranno passati alla chiamata di rimozione dalla coda.  
*BufferSize* \[ \] dimensioni di *pbuffer* in byte.  
*Flag* \[ in \] un parametro facoltativo che controlla il comportamento di questa funzione. L'unico flag è flag della coda della superficie non in \_ \_ \_ \_ \_ attesa. Vedere le note per lo scaricamento. Se non viene passato alcun flag (*Flags* = = 0), viene utilizzato il comportamento di blocco predefinito.  
</dl>

**Valori restituiti**

Questa funzione può restituire l' \_ errore DXGI \_ è ancora in corso \_ \_ il disegno se viene utilizzato un flag di coda della superficie \_ non di \_ \_ \_ \_ attesa.  
</dl>

**Osservazioni:**

-   Questa funzione inserisce la superficie nella coda. Se l'applicazione non specifica che il \_ flag della coda di superficie non \_ \_ \_ \_ è in attesa, questa funzione è bloccata ed esegue una sincronizzazione GPU CPU per garantire che tutto il rendering sull'area accodata sia completato. Se questa funzione ha esito positivo, sarà disponibile una superficie per la rimozione dalla coda. Se si desidera un comportamento non di blocco, utilizzare il \_ \_ flag non aspettare. Per informazioni dettagliate, vedere Flush ().
-   In base alle regole di conteggio dei riferimenti COM, la superficie restituita dalla rimozione dalla coda sarà AddRef () in modo che l'applicazione non debba eseguire questa operazione. Dopo aver chiamato l'accodamento, l'applicazione deve rilasciare la superficie perché non la utilizza più.

**Svuotamento**  


```C++
HRESULT Flush(
  [in]  DWORD Flags,
  [out] UINT *nSurfaces
);
```



**Parametri**  
*Flag* \[ in\]  
L'unico flag è flag della coda della superficie non in \_ \_ \_ \_ \_ attesa. Vedere la sezione Osservazioni. *nSurfaces* \[ out \] restituisce il numero di superfici ancora in sospeso e non svuotate.  
</dl>

**Valori restituiti**

Questa funzione può restituire \_ l'errore DXGI \_ è ancora in corso \_ \_ il disegno se viene usato il flag di coda della superficie \_ non di \_ \_ \_ \_ attesa. Questa funzione restituisce \_ OK se una superficie è stata scaricata correttamente. Questa funzione restituisce \_ un errore DXGI che \_ è stato \_ ancora \_ disegnato solo se nessuna superficie è stata scaricata. Insieme, il valore restituito e *nSurfaces* indicano all'applicazione quale operazione è stata eseguita e se il lavoro è rimasto.  
</dl>

**Osservazioni:**

Lo svuotamento è significativo solo se la chiamata precedente all'accodamento ha usato \_ il \_ flag do not wait; in caso contrario, sarà un no-op. Se la chiamata all'accodamento usa il \_ flag non \_ attendere, l'accodamento viene restituito immediatamente e la sincronizzazione della CPU GPU non è garantita. La superficie viene comunque considerata accodata, il dispositivo di produzione non può continuare a utilizzarlo, ma non è disponibile per la rimozione dalla coda. Per tentare di eseguire il commit della superficie per la rimozione dalla coda, è necessario chiamare lo svuotamento. Flush tenta di eseguire il commit di tutte le superfici attualmente accodate. Se non viene passato alcun flag a Flush, bloccherà e cancellerà l'intera coda, preparando tutte le superfici per la rimozione dalla coda. Se \_ \_ viene utilizzato il flag non di attesa, la coda verificherà le superfici per verificare se una di esse è pronta. questo passaggio non è bloccante. Le superfici che hanno terminato la sincronizzazione GPU CPU saranno pronte per il dispositivo consumer. Le superfici ancora in sospeso non saranno interessate. La funzione restituisce il numero di superfici che devono ancora essere scaricate.

> [!Note]  
> Lo svuotamento non interrompe la semantica della coda. L'API garantisce che venga eseguito il commit delle superfici accodate prima che le superfici vengano accodate in un secondo momento, indipendentemente dal momento in cui viene eseguita la sincronizzazione GPU CPU.

 

  
</dl>

### <a name="direct3d-9ex-and-dxgi-interop-helper-how-to-use"></a>Helper di interoperabilità Direct3D 9Ex e DXGI: come usare

Si prevede che la maggior parte dei casi di utilizzo coinvolga due dispositivi che condividono un certo numero di superfici. Poiché questo è lo scenario più semplice, questo documento descrive come usare le API per raggiungere questo obiettivo, illustra una variazione senza blocco e termina con una breve sezione sull'inizializzazione per tre dispositivi.

### <a name="two-devices"></a>Due dispositivi

L'applicazione di esempio che usa questo helper può usare Direct3D 9Ex e Direct3D 11 insieme. L'applicazione può elaborare contenuto con entrambi i dispositivi e presentare contenuto con Direct3D 9. L'elaborazione potrebbe significare il rendering del contenuto, la decodifica del video, l'esecuzione di compute shader e così via. Per ogni frame, l'applicazione viene elaborata prima con Direct3D 11, quindi elabora con Direct3D 9 e infine presenta con Direct3D 9. Inoltre, l'elaborazione con Direct3D 11 produrrà alcuni metadati che dovranno essere utilizzati da Direct3D 9. In questa sezione viene illustrata l'utilizzo dell'helper in tre parti che corrispondono a questa sequenza: inizializzazione, ciclo principale e pulizia.

**Inizializzazione**  
L'inizializzazione prevede i passaggi seguenti:  

1.  Inizializzare entrambi i dispositivi.
2.  Creare la coda radice: m \_ 11to9Queue.
3.  Clonare dalla coda radice: m \_ 9to11Queue.
4.  Chiamare OpenProducer/OpenConsumer in entrambe le code.

I nomi delle code usano i numeri 9 e 11 per indicare quale API è il producer e qual è il consumer: **m \_ ***Producer*** a ***consumer*** Queue**. Di conseguenza, m \_ 11to9Queue indica una coda per la quale il dispositivo Direct3D 11 produce superfici utilizzate dal dispositivo Direct3D 9. Analogamente, m \_ 9to11Queue indica una coda per la quale Direct3D 9 produce superfici utilizzate da Direct3D 11.  
Inizialmente la coda radice è piena e tutte le code clonate sono inizialmente vuote. Questo non dovrebbe costituire un problema per l'applicazione, ad eccezione del primo ciclo di Accodamento e rimozione dalla coda e della disponibilità dei metadati. Se una rimozione dalla coda richiede i metadati, ma non ne è stata impostata nessuna, perché non è presente alcun elemento inizialmente oppure l'accodamento non ha impostato alcun valore, la rimozione dalla coda rileva che non è stato ricevuto alcun metadati.  

1.  **Inizializzare entrambi i dispositivi.**  
    ```C++
    m_pD3D9Device = InitializeD3D9ExDevice();
    m_pD3D11Device = InitializeD3D11Device();
    ```

    

2.  **Creare la coda radice.**  
    Questo passaggio crea anche le superfici. Le restrizioni relative alle dimensioni e al formato sono identiche a quelle della creazione di risorse condivise. La dimensione del buffer dei metadati viene fissata in fase di creazione e in questo caso verrà semplicemente passato un UINT.  
    La coda deve essere creata con un numero fisso di superfici. Le prestazioni variano a seconda dello scenario. La presenza di più aree aumenta le probabilità che i dispositivi siano occupati. Se, ad esempio, è presente una sola superficie, non vi sarà alcuna parallelizzazione tra i due dispositivi. D'altra parte, l'aumento del numero di superfici aumenta il footprint di memoria, che può influire negativamente sulle prestazioni. In questo esempio vengono utilizzate due superfici.  
    ```C++
    SURFACE_QUEUE_DESC Desc;
    Desc.Width        = 640;
    Desc.Height       = 480;
    Desc.Format       = DXGI_FORMAT_R16G16B16A16_FLOAT;
    Desc.NumSurfaces  = 2;
    Desc.MetaDataSize = sizeof(UINT);
    Desc.Flags        = 0;

    CreateSurfaceQueue(&Desc, m_pD3D9Device, &m_11to9Queue);
    ```

    

3.  **Clonare la coda radice.**  
    Ogni coda clonata deve usare le stesse superfici ma può avere dimensioni del buffer di metadati diverse e flag diversi. In questo caso, non sono presenti metadati da Direct3D 9 a Direct3D 11.  
    ```C++
    SURFACE_QUEUE_CLONE_DESC Desc;
    Desc.MetaDataSize = 0;
    Desc.Flags        = 0;

    m_11to9Queue->Clone(&Desc, &m_9to11Queue);
    ```

    

4.  **Aprire i dispositivi Producer e consumer.**  
    L'applicazione deve eseguire questo passaggio prima della chiamata di Accodamento e rimozione dalla coda. L'apertura di un producer e di un consumer restituisce interfacce che contengono le API di Accodamento/rimozione dalla coda.  
    ```C++
    // Open for m_p9to11Queue.
    m_p9to11Queue->OpenProducer(m_pD3D9Device, &m_pD3D9Producer);
    m_p9to11Queue->OpenConsumer(m_pD3D11Device, &m_pD3D11Consumer);

    // Open for m_p11to9Queue.
    m_p11to9Queue->OpenProducer(m_pD3D11Device, &m_pD3D11Producer);
    m_p11to9Queue->OpenConsumer(m_pD3D9Device, &m_pD3D9Consumer);
    ```

    

**Ciclo principale**  
L'utilizzo della coda viene modellato dopo il problema classico di producer/consumer. Si può pensare a questo aspetto dal punto di vista del singolo dispositivo. Ogni dispositivo deve eseguire i passaggi seguenti: rimuovere la coda per ottenere una superficie dalla coda che lo utilizza, elaborarla sulla superficie e quindi accodarla nella coda di produzione. Per il dispositivo Direct3D 11, l'utilizzo di Direct3D 9 è quasi identico.  


```C++
// Direct3D 9 Device.
IDirect3DTexture9* pTexture9 = NULL;
REFIID             surfaceID9 = _uuidof(IDirect3DTexture9);
UINT               metaData;
UINT               metaDataSize;
while (!done)
{
    // Dequeue surface.
    m_pD3D9Consumer->Dequeue(surfaceID9, (void**)&pSurface9,
                             &metaData, &metaDataSize, INFINITE);

    // Process the surface.
    ProcessD3D9(pSurface9);

    // Present the surface using the meta data.
    PresentD3D9(pSurface9, metaData, metaDataSize);

    // Enqueue surface.
    m_pD3D9Producer->Enqueue(pSurface9, NULL, 0, 0);
}
```



**Pulizia**  
Questo passaggio è molto semplice. Oltre ai normali passaggi per la pulizia delle API Direct3D, l'applicazione deve rilasciare le interfacce COM restituite.  


```C++
m_pD3D9Producer->Release();
m_pD3D9Consumer->Release();
m_pD3D11Producer->Release();
m_pD3D11Consumer->Release();
m_p9to11Queue->Release();
m_p11to9Queue->Release();
```



</dl>

### <a name="non-blocking-use"></a>Uso non bloccante

L'esempio precedente è utile per un caso di utilizzo multithreading in cui ogni dispositivo dispone di un proprio thread. Nell'esempio vengono usate le versioni di blocco delle API: infinito per il timeout e nessun flag da accodare. Se si desidera utilizzare l'helper in modo non bloccante, è necessario apportare solo alcune modifiche. Questa sezione illustra l'uso non bloccante con entrambi i dispositivi in un thread.

**Inizializzazione**  
L'inizializzazione è identica a eccezione dei flag. Poiché l'applicazione è a thread singolo, usare tale flag per la creazione. In questo modo si disattiva parte del codice di sincronizzazione, che potenzialmente migliora le prestazioni.  


```C++
SURFACE_QUEUE_DESC Desc;
Desc.Width        = 640;
Desc.Height       = 480;
Desc.Format       = DXGI_FORMAT_R16G16B16A16_FLOAT;
Desc.NumSurfaces  = 2;
Desc.MetaDataSize = sizeof(UINT);
Desc.Flags        = SURFACE_QUEUE_FLAG_SINGLE_THREADED;

CreateSurfaceQueue(&Desc, m_pD3D9Device, &m_11to9Queue);
```




```C++
SURFACE_QUEUE_CLONE_DESC Desc;
Desc.MetaDataSize = 0;
Desc.Flags        = SURFACE_QUEUE_FLAG_SINGLE_THREADED;

m_11to9Queue->Clone(&Desc, &m_9to11Queue);
```



L'apertura dei dispositivi Producer e consumer è identica a quella dell'esempio di blocco.  
**Uso della coda**  
Esistono molti modi per usare la coda in modo non bloccante con diverse caratteristiche di prestazioni. L'esempio seguente è semplice ma presenta prestazioni ridotte a causa di un numero eccessivo di operazioni di filatura e polling. Nonostante questi problemi, l'esempio Mostra come usare l'helper. L'approccio consiste nel rimanere sempre in un ciclo e rimuovere dalla coda, elaborare, accodare e scaricare. Se uno dei passaggi ha esito negativo perché la risorsa non è disponibile, l'applicazione ritenta semplicemente il ciclo successivo.  


```C++
// Direct3D 11 Device.
ID3D11Texture2D* pSurface11 = NULL;
REFIID           surfaceID11 = __uuidof(ID3D11Texture2D);
UINT             metaData;
while (!done)
{
    //
    // D3D11 Portion.
    //

    // Dequeue surface.
    hr = m_pD3D11Consumer->Dequeue(surfaceID11,
                                   (void**)&pSurface11,
                                   NULL, 0, 0);
    // Only continue if we got a surface.
    if (SUCCEEDED(hr))
    {
        // Process the surface and return some meta data.
        ProcessD3D11(pSurface11, &metaData);

        // Enqueue surface.
        m_pD3D11Producer->Enqueue(pSurface11, &metaData,
                                  sizeof(UINT),
                                  SURFACE_QUEUE_FLAG_DO_NOT_WAIT);
    }
    // Flush the queue to check if any surfaces completed.
    m_pD3D11Producer->Flush(NULL,SURFACE_QUEUE_FLAG_DO_NOT_WAIT);

    //
    // Do the same with the Direct3D 9 Device.
    //

    // Dequeue surface.
    hr = m_pD3D9Consumer->Dequeue(surfaceID9,
                                  (void**)&pSurface9,
                                  &metaData,
                                  &metaDataSize, 0);
    // Only continue if we got a surface.
    if (SUCCEEDED(hr)))
    {
        // Process the surface.
        ProcessD3D9(pSurface9);

        // Present the surface using the meta data.
        PresentD3D9(pSurface9, metaData, metaDataSize);

        // Enqueue surface.
        m_pD3D9Producer->Enqueue(pSurface9, NULL, 0,
                                 SURFACE_QUEUE_FLAG_DO_NOT_WAIT);
    }
    // Flush the queue to check if any surfaces completed.
    m_pD3D9Producer->Flush(NULL,SURFACE_QUEUE_FLAG_DO_NOT_WAIT);
}
```



Una soluzione più complessa potrebbe controllare il valore restituito dall'accodamento e dallo svuotamento per determinare se lo scaricamento è necessario.  
</dl>

### <a name="three-devices"></a>Tre dispositivi

L'estensione degli esempi precedenti per coprire più dispositivi è semplice. Il codice seguente esegue l'inizializzazione. Una volta creati gli oggetti producer/consumer, il codice per utilizzarli è lo stesso. Questo esempio presenta tre dispositivi e pertanto tre code. Il flusso delle superfici da Direct3D 9 a Direct3D 10 a Direct3D 11.


```C++
SURFACE_QUEUE_DESC Desc;
Desc.Width        = 640;
Desc.Height       = 480;
Desc.Format       = DXGI_FORMAT_R16G16B16A16_FLOAT;
Desc.NumSurfaces  = 2;
Desc.MetaDataSize = sizeof(UINT);
Desc.Flags        = 0;

SURFACE_QUEUE_CLONE_DESC Desc;
Desc.MetaDataSize = 0;
Desc.Flags        = 0;

CreateSurfaceQueue(&Desc, m_pD3D9Device, &m_11to9Queue);
m_11to9Queue->Clone(&Desc, &m_9to10Queue);
m_11to9Queue->Clone(&Desc, &m_10to11Queue);
```



Come indicato in precedenza, la clonazione funziona allo stesso modo, indipendentemente dalla coda clonata. Ad esempio, la seconda chiamata di clonazione potrebbe essere disattivata dall' \_ oggetto 9to10Queue m.


```C++
// Open for m_p9to10Queue.
m_p9to10Queue->OpenProducer(m_pD3D9Device, &m_pD3D9Producer);
m_p9to10Queue->OpenConsumer(m_pD3D10Device, &m_pD3D10Consumer);

// Open for m_p10to11Queue.
m_p10to11Queue->OpenProducer(m_pD3D10Device, &m_pD3D10Producer);
m_p10to11Queue->OpenConsumer(m_pD3D11Device, &m_pD3D11Consumer);

// Open for m_p11to9Queue.
m_p11to9Queue->OpenProducer(m_pD3D11Device, &m_pD3D11Producer);
m_p11to9Queue->OpenConsumer(m_pD3D9Device, &m_pD3D9Consumer);
```



## <a name="conclusion"></a>Conclusione

È possibile creare soluzioni che usano l'interoperabilità per sfruttare la potenza di più API DirectX. L'interoperabilità dell'API grafica di Windows offre ora un runtime di Common Surface Management DXGI 1,1. Questo runtime Abilita il supporto per la condivisione di superficie sincronizzata nelle API appena sviluppate, ad esempio Direct3D 11, Direct3D 10,1 e Direct2D. I miglioramenti per l'interoperabilità tra le nuove API e le API esistenti facilitano la migrazione delle applicazioni e la compatibilità Le API di consumer Direct3D 9Ex e DXGI 1,1 possono interagire, come illustrato nel meccanismo di sincronizzazione fornito tramite il codice di supporto di esempio in MSDN Code Gallery.

 

 