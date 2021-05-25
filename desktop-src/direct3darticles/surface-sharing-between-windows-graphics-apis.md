---
title: Condivisione della superficie tra LE API grafiche di Windows
description: Questo argomento offre una panoramica tecnica dell'interoperabilità tramite la condivisione di superfici tra LE API grafiche di Windows, tra cui Direct3D 11, Direct2D, DirectWrite, Direct3D 10 e Direct3D 9Ex.
ms.assetid: 65abf33e-3d15-42ff-99bd-674f24da773e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1032cb1cf9b16280088f00e79e7e59bb7f1510b1
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343616"
---
# <a name="surface-sharing-between-windows-graphics-apis"></a>Condivisione della superficie tra LE API grafiche di Windows

Questo argomento offre una panoramica tecnica dell'interoperabilità tramite la condivisione di superfici tra LE API grafiche di Windows, tra cui Direct3D 11, Direct2D, DirectWrite, Direct3D 10 e Direct3D 9Ex. Se si ha già una conoscenza di queste API, questo documento consente di usare più API per il rendering sulla stessa superficie in un'applicazione progettata per i sistemi operativi Windows 7 o Windows Vista. Questo argomento fornisce anche linee guida per le procedure consigliate e puntatori a risorse aggiuntive.

> [!Note]  
> Per l'interoperabilità Direct2D e DirectWrite nel runtime DirectX 11.1, è possibile usare i [dispositivi Direct2D](/windows/desktop/Direct2D/devices-and-device-contexts) e i contesti di dispositivo per eseguire il rendering direttamente nei dispositivi Direct3D 11.

 

In questo argomento sono contenute le sezioni seguenti.

-   [Introduzione](#introduction)
-   [Panoramica dell'interoperabilità delle API](#api-interoperability-overview)
-   [Scenari di interoperabilità](#interoperability-scenarios)
    -   [Condivisione di dispositivi Direct3D 10.1 con Direct2D](#direct3d-101-device-sharing-with-direct2d)
    -   [Superfici condivise sincronizzate DXGI 1.1](#dxgi-11-synchronized-shared-surfaces)
    -   [Interoperabilità tra LE API basate su Direct3D 9Ex e DXGI](#interoperability-between-direct3d-9ex-and-dxgi-based-apis)
-   [Conclusione](#conclusion)

## <a name="introduction"></a>Introduzione

In questo documento l'interoperabilità dell'API grafica di Windows si riferisce alla condivisione della stessa superficie di rendering da parte di API diverse. Questo tipo di interoperabilità consente alle applicazioni di creare visualizzazioni accattivanti sfruttando più API grafiche di Windows e di semplificare la migrazione alle nuove tecnologie mantenendo la compatibilità con le API esistenti.

In Windows 7 (e Windows Vista SP2 con Windows 7 Interop Pack, Vista 7IP), le API di rendering della grafica sono Direct3D 11, Direct2D, Direct3D 10.1, Direct3D 10.0, Direct3D 9Ex, Direct3D 9c e api Direct3D precedenti, nonché GDI e GDI+. Windows Imaging Component (WIC) e DirectWrite sono tecnologie correlate per l'elaborazione delle immagini e Direct2D esegue il rendering del testo. L'API DirectX Video Acceleration (DXVA), basata su Direct3D 9c e Direct3D 9Ex, viene usata per l'elaborazione video.

Con l'evolversi delle API grafiche di Windows verso l'essere basate su Direct3D, Microsoft sta investendo più impegno per garantire l'interoperabilità tra le API. Le API Direct3D appena sviluppate e le API di livello superiore basate su API Direct3D forniscono anche il supporto quando necessario per il bridging della compatibilità con le API meno recenti. Per illustrare, le applicazioni Direct2D possono usare Direct3D 10.1 condividendo un dispositivo Direct3D 10.1. Inoltre, le API Direct3D 11, Direct2D e Direct3D 10.1 possono sfruttare tutti i vantaggi di DirectX Graphic Infrastructure (DXGI) 1.1, che abilita le superfici condivise sincronizzate che supportano completamente l'interoperabilità tra queste API. Le API basate su DXGI 1.1 interagisce con GDI e con GDI+ per associazione, ottenendo il contesto di dispositivo GDI da una superficie DXGI 1.1. Per altre informazioni, vedere la documentazione sull'interoperabilità DXGI e GDI disponibile in MSDN.

La condivisione della superficie non sincronizzata è supportata dal runtime Direct3D 9Ex. Le applicazioni video basate su DXVA possono usare l'helper di interoperabilità Direct3D 9Ex e DXGI per l'interoperabilità DXVA basata su Direct3D 9Ex con Direct3D 11 per compute shader oppure possono interagire con Direct2D per il rendering del testo o i controlli 2D. WIC e DirectWrite interagisce anche con GDI, Direct2D e, per associazione, altre API Direct3D.

Direct3D 10.0, Direct3D 9c e i runtime Direct3D precedenti non supportano le superfici condivise. Le copie della memoria di sistema continueranno a essere usate per l'interoperabilità con le API basate su GDI o DXGI.

Si noti che gli scenari di interoperabilità all'interno di questo documento fanno riferimento a più API grafiche per il rendering in una superficie di rendering condivisa, anziché nella stessa finestra dell'applicazione. La sincronizzazione per API separate che hanno come destinazione superfici diverse che vengono quindi composte nella stessa finestra non rientra nell'ambito di questo documento.

## <a name="api-interoperability-overview"></a>Panoramica dell'interoperabilità delle API

L'interoperabilità della condivisione della superficie delle API grafiche di Windows può essere descritta in termini di scenari da API ad API e dalla funzionalità di interoperabilità corrispondente. A partire da Windows 7 e a partire da Windows Vista SP2 con 7IP, le nuove API e i runtime associati includono Direct2D e le tecnologie correlate: Direct3D 11 e DXGI 1.1. Le prestazioni di GDI sono state migliorate anche in Windows 7. Direct3D 10.1 è stato introdotto in Windows Vista SP1. Il diagramma seguente illustra il supporto dell'interoperabilità tra le API.

![Diagramma del supporto dell'interoperabilità tra api grafiche di Windows](images/surface-sharing-interoperability.png)

In questo diagramma le frecce mostrano scenari di interoperabilità in cui la stessa superficie può essere accessibile dalle API connesse. Le frecce blu indicano i meccanismi di interoperabilità introdotti in Windows Vista. Le frecce verdi indicano il supporto per l'interoperabilità per le nuove API o miglioramenti che consentono alle API meno recenti di interagire con le API più recenti. Ad esempio, le frecce verdi rappresentano la condivisione dei dispositivi, il supporto della superficie condivisa sincronizzata, l'helper di sincronizzazione Direct3D 9Ex/DXGI e l'ottenimento di un contesto di dispositivo GDI da una superficie compatibile.

## <a name="interoperability-scenarios"></a>Scenari di interoperabilità

A partire da Windows 7 e Windows Vista 7IP, le offerte mainstream delle API grafiche di Windows supportano il rendering di più API nella stessa superficie DXGI 1.1.

**Direct3D 11, Direct3D 10.1, Direct2D : interoperabilità tra loro**

Le API Direct3D 11, Direct3D 10.1 e Direct2D (e le API correlate come DirectWrite e WIC) possono interagire tra loro usando la condivisione di dispositivi Direct3D 10.1 o superfici condivise sincronizzate.

### <a name="direct3d-101-device-sharing-with-direct2d"></a>Condivisione di dispositivi Direct3D 10.1 con Direct2D

La condivisione dei dispositivi tra Direct2D e Direct3D 10.1 consente a un'applicazione di usare entrambe le API per eseguire il rendering in modo semplice ed efficiente sulla stessa superficie DXGI 1.1, usando lo stesso oggetto dispositivo Direct3D sottostante. Direct2D offre la possibilità di chiamare le API Direct2D usando un dispositivo Direct3D 10.1 esistente, sfruttando il fatto che Direct2D è basato sui runtime Direct3D 10.1 e DXGI 1.1. I frammenti di codice seguenti illustrano come Direct2D ottiene la destinazione di rendering del dispositivo Direct3D 10.1 da una superficie DXGI 1.1 associata al dispositivo. La destinazione di rendering del dispositivo Direct3D 10.1 può eseguire chiamate di disegno Direct2D tra le API BeginDraw ed EndDraw.


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

-   Il dispositivo Direct3D 10.1 associato deve supportare il formato BGRA. Il dispositivo è stato creato chiamando D3D10CreateDevice1 con il parametro D3D10 \_ CREATE \_ DEVICE \_ BGRA \_ SUPPORT. Il formato BGRA è supportato a partire dal livello di funzionalità 9.1 di Direct3D 10.
-   L'applicazione non deve creare più id2D1RenderTargets associati allo stesso dispositivo Direct3D10.1.
-   Per ottenere prestazioni ottimali, tenere sempre presente almeno una risorsa, ad esempio trame o superfici associate al dispositivo.

La condivisione dei dispositivi è adatta per l'utilizzo in-process a thread singolo di un dispositivo di rendering condiviso dalle API di rendering Direct3D 10.1 e Direct2D. Le superfici condivise sincronizzate consentono l'uso multi-thread, in-process e out-of-process di più dispositivi di rendering usati dalle API Direct3D 10.1, Direct2D e Direct3D 11.

Un altro metodo di interoperabilità di Direct3D 10.1 e Direct2D è l'uso di ID3D1RenderTarget::CreateSharedBitmap, che crea un oggetto ID2D1Bitmap da IDXGISurface. È possibile scrivere una scena Direct3D10.1 nella bitmap ed eseguirne il rendering con Direct2D. Per altre informazioni, vedere [Metodo ID2D1RenderTarget::CreateSharedBitmap](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap).

### <a name="direct2d-software-rasterization"></a>Rasterizzazione del software Direct2D

La condivisione dei dispositivi con Direct3D 10.1 non è supportata quando si usa il renderer software Direct2D, ad esempio specificando D2D1 \_ RENDER TARGET USAGE FORCE SOFTWARE RENDERING in D2D1 RENDER TARGET USAGE durante la creazione di una destinazione di \_ \_ rendering \_ \_ \_ \_ \_ \_ Direct2D.

Direct2D può usare l'rasterizzazione software WARP10 per condividere il dispositivo con Direct3D 10 o Direct3D 11, ma le prestazioni diminuiscono significativamente.

### <a name="dxgi-11-synchronized-shared-surfaces"></a>Superfici condivise sincronizzate DXGI 1.1

Le API Direct3D 11, Direct3D 10.1 e Direct2D usano tutte DXGI 1.1, che fornisce la funzionalità per sincronizzare la lettura e la scrittura nella stessa superficie di memoria video (DXGISurface1) da due o più dispositivi Direct3D. I dispositivi di rendering che usano superfici condivise sincronizzate possono essere dispositivi Direct3D 10.1 o Direct3D 11, ognuno in esecuzione nello stesso processo o tra processi.

Le applicazioni possono usare superfici condivise sincronizzate per interagire tra qualsiasi dispositivo basato su DXGI 1.1, ad esempio Direct3D 11 e Direct3D 10.1 o tra Direct3D 11 e Direct2D, ottenendo il dispositivo Direct3D 10.1 dall'oggetto di destinazione di rendering Direct2D.

Nelle API Direct3D 10.1 e versioni successive, per usare DXGI 1.1, assicurarsi che il dispositivo Direct3D sia creato usando un oggetto adattatore DXGI 1.1, enumerato dall'oggetto factory DXGI 1.1. Chiamare CreateDXGIFactory1 per creare l'oggetto IDXGIFactory1 ed EnumAdapters1 per enumerare l'oggetto IDXGIAdapter1. L'oggetto IDXGIAdapter1 deve essere passato come parte della chiamata D3D10CreateDevice o D3D10CreateDeviceAndSwapChain. Per altre informazioni sulle API DXGI 1.1, vedere la Guida alla [programmazione per DXGI.](https://msdn.microsoft.com/library/ee418147(VS.85).aspx)

### <a name="apis"></a>API

**RISORSA D3D10 \_ \_ MISC \_ SHARED \_ KEYEDMUTEX**  
Quando si crea la risorsa condivisa sincronizzata, impostare D3D10 \_ RESOURCE \_ MISC \_ SHARED \_ KEYEDMUTEX in D3D10 \_ RESOURCE \_ MISC \_ FLAG.  


```C++
typedef enum D3D10_RESOURCE_MISC_FLAG {
    D3D10_RESOURCE_MISC_GENERATE_MIPS      = 0x1L,
    D3D10_RESOURCE_MISC_SHARED             = 0x2L,
    D3D10_RESOURCE_MISC_TEXTURECUBE        = 0x4L,
    D3D10_RESOURCE_MISC_SHARED_KEYEDMUTEX  = 0x10L,
    D3D10_RESOURCE_MISC_GDI_COMPATIBLE     = 0x20L,
}   D3D10_RESOURCE_MISC_FLAG;
```



**RISORSA D3D10 \_ \_ MISC \_ SHARED \_ KEYEDMUTEX**  
Consente la sincronizzazione della risorsa creata usando le API IDXGIKeyedMutex::AcquireSync e ReleaseSync. Le API Direct3D 10.1 di creazione di risorse seguenti che accettano tutti un parametro D3D10 RESOURCE MISC FLAG sono state estese per \_ \_ \_ supportare il nuovo flag.  

-   ID3D10Device1::CreateTexture1D
-   ID3D10Device1::CreateTexture2D
-   ID3D10Device1::CreateTexture3D
-   ID3D10Device1::CreateBuffer

  
Se una delle funzioni elencate viene chiamata con il flag D3D10 RESOURCE MISC SHARED KEYEDMUTEX impostato, è possibile eseguire query sull'interfaccia restituita per un'interfaccia \_ \_ \_ IDXGIKeyedMutex, che implementa le API AcquireSync e ReleaseSync per sincronizzare l'accesso \_ alla superficie. Il dispositivo che crea la superficie e qualsiasi altro dispositivo che apre la superficie (usando OpenSharedResource) è necessario per chiamare IDXGIKeyedMutex::AcquireSync prima di qualsiasi comando di rendering sulla superficie e IDXGIKeyedMutex::ReleaseSync al termine del rendering.  
I dispositivi WARP e REF non supportano le risorse condivise. Se si tenta di creare una risorsa con questo flag in un dispositivo WARP o REF, il metodo create restituirà un codice di errore E \_ OUTOFMEMORY.  
**INTERFACCIA IDXGIKEYEDMUTEX**  
Una nuova interfaccia in DXGI 1.1, IDXGIKeyedMutex, rappresenta un mutex con chiave, che consente l'accesso esclusivo a una risorsa condivisa usata da più dispositivi. Per la documentazione di riferimento su questa interfaccia e i relativi due metodi, AcquireSync e ReleaseSync, vedere [IDXGIKeyedMutex.](https://msdn.microsoft.com/library/ee421920(VS.85).aspx)  
</dl>

### <a name="sample-synchronized-surface-sharing-between-two-direct3d-101-devices"></a>Esempio: Condivisione della superficie sincronizzata tra due dispositivi Direct3D 10.1

L'esempio seguente illustra la condivisione di una superficie tra due dispositivi Direct3D 10.1. La superficie condivisa sincronizzata viene creata da un dispositivo Direct3D10.1.


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



Lo stesso dispositivo Direct3D10.1 può ottenere la superficie condivisa sincronizzata per il rendering chiamando AcquireSync, quindi rilasciando la superficie per il rendering dell'altro dispositivo chiamando ReleaseSync. Quando non condivide la superficie condivisa sincronizzata con altri dispositivi Direct3D, l'autore può ottenere e rilasciare la superficie condivisa sincronizzata (per avviare e terminare il rendering) acquisendo e rilasciando usando lo stesso valore chiave.


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



Il secondo dispositivo Direct3D10.1 può ottenere la superficie condivisa sincronizzata per il rendering chiamando AcquireSync, quindi rilasciando la superficie per il rendering del primo dispositivo chiamando ReleaseSync. Si noti che il dispositivo 2 è in grado di acquisire la superficie condivisa sincronizzata usando lo stesso valore di chiave specificato nella chiamata a ReleaseSync dal dispositivo 1.


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



I dispositivi aggiuntivi che condividono la stessa superficie possono acquisire e rilasciare la superficie a turno usando chiavi aggiuntive, come illustrato nelle chiamate seguenti.


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



Si noti che un'applicazione reale potrebbe sempre eseguire il rendering su una superficie intermedia che viene quindi copiata nella superficie condivisa per evitare che un dispositivo in attesa su un altro dispositivo che condivide la superficie.

### <a name="using-synchronized-shared-surfaces-with-direct2d-and-direct3d-11"></a>Uso di superfici condivise sincronizzate con Direct2D e Direct3D 11

Analogamente, per la condivisione tra le API Direct3D 11 e Direct3D 10.1, è possibile creare una superficie condivisa sincronizzata da un dispositivo API e condividerla con gli altri dispositivi API, in o fuori processo.

Le applicazioni che usano Direct2D possono condividere un dispositivo Direct3D 10.1 e usare una superficie condivisa sincronizzata per interagire con Direct3D 11 o altri dispositivi Direct3D 10.1, indipendentemente dal fatto che appartengano allo stesso processo o a processi diversi. Tuttavia, per le applicazioni a thread singolo a processo singolo, la condivisione dei dispositivi è il metodo di interoperabilità più efficiente e ad alte prestazioni tra Direct2D e Direct3D 10 o Direct3D 11.

### <a name="software-rasterizer"></a>Rasterizzazione software

Le superfici condivise sincronizzate non sono supportate quando le applicazioni usano i rasterizzatori software Direct3D o Direct2D, inclusi il rasterizzatore di riferimento e WARP, anziché l'accelerazione hardware grafica.

### <a name="interoperability-between-direct3d-9ex-and-dxgi-based-apis"></a>Interoperabilità tra LE API basate su Direct3D 9Ex e DXGI

Le API Direct3D 9Ex includevano la nozione di condivisione della superficie per consentire ad altre API di leggere dalla superficie condivisa. Per condividere la lettura e la scrittura in una superficie condivisa Direct3D 9Ex, è necessario aggiungere la sincronizzazione manuale all'applicazione stessa.

### <a name="direct3d-9ex-shared-surfaces-plus-manual-synchronization-helper"></a>Direct3D 9Ex Shared Surfaces Plus Manual Synchronization Helper

L'attività più fondamentale nell'interoperabilità Direct3D 9Ex e Direct3D 10 o 11 è il passaggio di una singola superficie dal primo dispositivo (dispositivo A) al secondo (dispositivo B) in modo che, quando il dispositivo B acquisisce un handle sulla superficie, il rendering del dispositivo A sia stato completato. Pertanto, il dispositivo B può usare questa superficie senza preoccuparsi. Questo problema è molto simile al problema producer-consumer classico e questa discussione modella il problema in questo modo. Il primo dispositivo che usa la superficie e quindi lo cesa è il producer (dispositivo A) e il dispositivo che inizialmente è in attesa è il consumer (dispositivo B). Qualsiasi applicazione reale è più sofisticata di questa e concatena più blocchi predefiniti producer-consumer per creare la funzionalità desiderata.

I blocchi predefiniti producer-consumer vengono implementati nell'helper usando una coda di superfici. Le superfici vengono accodati dal producer e accodati dal consumer. L'helper introduce tre interfacce COM: ISurfaceQueue, ISurfaceProducer e ISurfaceConsumer.

### <a name="high-level-overview-of-helper"></a>High-Level panoramica dell'helper

L'oggetto ISurfaceQueue è il blocco predefinito per l'uso delle superfici condivise. Viene creato con un dispositivo Direct3D inizializzato e una descrizione per creare un numero fisso di superfici condivise. L'oggetto coda gestisce la creazione di risorse e l'apertura del codice. Il numero e il tipo di superfici sono fissi. Dopo aver creato le superfici, l'applicazione non può aggiungerle o rimuoverle.

Ogni istanza dell'oggetto ISurfaceQueue fornisce una sorta di strada unidireale che può essere usata per inviare superfici dal dispositivo di produzione al dispositivo che li utilizza. È possibile usare più strade unidireali di questo tipo per abilitare scenari di condivisione della superficie tra dispositivi di applicazioni specifiche.

**Durata creazione/oggetto**  
Esistono due modi per creare l'oggetto coda: tramite CreateSurfaceQueue o tramite il metodo Clone di ISurfaceQueue. Poiché le interfacce sono oggetti COM, si applica la gestione della durata COM standard.  
**Modello producer/consumer**  
Accodamento (): il producer chiama questa funzione per indicare che è stata completata con la superficie, che ora può diventare disponibile per un altro dispositivo. Al ritorno da questa funzione, il dispositivo producer non ha più diritti per la superficie ed è non sicuro continuare a usarlo.  
Dequeue (): il dispositivo che utilizza chiama questa funzione per ottenere una superficie condivisa. L'API garantisce che tutte le superfici accodati siano pronte per l'uso.  
**Metadata**  
L'API supporta l'associazione di metadati alle superfici condivise.  
Enqueue() consente di specificare metadati aggiuntivi che verranno passati al dispositivo utilizzatore. I metadati devono essere inferiori al valore massimo noto al momento della creazione.  
Dequeue() può facoltativamente passare un buffer e un puntatore alle dimensioni del buffer. La coda riempie il buffer con i metadati della chiamata enqueue corrispondente.  
**Clonazione**  
Ogni oggetto ISurfaceQueue risolve una sincronizzazione unidirezionale. Si presuppone che la maggior parte delle applicazioni che usano questa API userà un sistema chiuso. Il sistema chiuso più semplice con due dispositivi che inviano superfici avanti e indietro richiede due code. L'oggetto ISurfaceQueue ha un metodo Clone() per rendere possibile la creazione di più code che fanno tutte parte della stessa pipeline più grande.  
Clone crea un nuovo oggetto ISurfaceQueue da uno esistente e condivide tutte le risorse aperte tra di essi. L'oggetto risultante ha esattamente le stesse superfici della coda di origine. Le code clonate possono avere dimensioni di metadati diverse l'una dall'altra.  
**Superfici**  
ISurfaceQueue è responsabile della creazione e della gestione delle superfici. Non è valido accodare superfici arbitrarie. Inoltre, una superficie deve avere un solo "proprietario" attivo. Deve essere in una coda specifica o usata da un dispositivo specifico. Non è valido che sia in più code o che i dispositivi continuino a usare la superficie dopo essere stati accodati.  
</dl>

### <a name="api-details"></a>Dettagli DELL'API

### <a name="isurfacequeue"></a>IsurfaceQueue

La coda è responsabile della creazione e della gestione delle risorse condivise. Fornisce anche la funzionalità per concatenare più code usando Clone. La coda dispone di metodi che aprono il dispositivo di produzione e un dispositivo che lo utilizza. È possibile aprire solo uno di essi in qualsiasi momento.

La coda espone le API seguenti:



| API                            | Descrizione                                                                                 |
|-----------------------------|----------------------------------------------------------------------------------|
| CreateSurfaceQueue          | Crea un oggetto ISurfaceQueue (la coda "radice").                              |
| ISurfaceQueue::OpenConsumer | Restituisce un'interfaccia per il dispositivo che utilizza la coda.                        |
| ISurfaceQueue::OpenProducer | Restituisce un'interfaccia per il dispositivo di produzione da accodare.                        |
| ISurfaceQueue::Clone        | Crea un oggetto ISurfaceQueue che condivide le superfici con l'oggetto coda radice. |



 

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

**Width**, **Height**  Le dimensioni delle superfici condivise. Tutte le superfici condivise devono avere le stesse dimensioni.  
**Formato** Formato delle superfici condivise. Tutte le superfici condivise devono avere lo stesso formato. I formati validi dipendono dai dispositivi che verranno usati, perché coppie diverse di dispositivi possono condividere tipi di formato diversi.  
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

 *pDesc* \[ in \]  Descrizione della coda della superficie condivisa da creare.  

 *pDevice* \[ in \]  Il dispositivo da usare per creare le superfici condivise. Si tratta di un parametro esplicito a causa di una funzionalità in Windows Vista. Per le superfici condivise tra Direct3D 9 e Direct3D 10, le superfici devono essere create con Direct3D 9.  

 *ppQueue* \[ out \]  In caso di restituzione, contiene un puntatore all'oggetto ISurfaceQueue.  


**Valori restituiti**

Se *pDevice non* è in grado di condividere le risorse, questa funzione restituisce DXGI \_ ERROR INVALID \_ \_ CALL. Questa funzione crea le risorse. Se non riesce, restituisce un errore. Se ha esito positivo, restituisce S \_ OK.

**Osservazioni:**

La creazione dell'oggetto coda crea anche tutte le superfici. Si presuppone che tutte le superfici siano destinazioni di rendering 2D e verranno create con i flag D3D10 BIND RENDER TARGET e \_ \_ \_ D3D10 BIND SHADER RESOURCE impostati \_ \_ (o i flag \_ equivalenti per i diversi runtime).

Lo sviluppatore può specificare un flag che indica se la coda sarà accessibile da più thread. Se non è impostato alcun flag (**Flags** == 0), la coda verrà usata da più thread. Lo sviluppatore può specificare l'accesso a thread singolo, che disattiva il codice di sincronizzazione e offre un miglioramento delle prestazioni per questi casi. Ogni coda clonata ha un proprio flag, pertanto è possibile che diverse code nel sistema abbia controlli di sincronizzazione diversi.

 **Aprire un producer**  


```C++
HRESULT OpenProducer(
  [in]   IUnknown *pDevice,
  [out]  IDXGIXSurfaceProducer **ppProducer
);
```



**Parametri**  

*pDevice* \[ Pollici\]  

Dispositivo producer che accoda le superfici alla coda di superficie. 

*ppProducer* \[ out \] Restituisce un oggetto all'interfaccia producer.  


**Valori restituiti**

Se il dispositivo non è in grado di condividere le superfici, restituisce ERRORE DXGI \_ \_ CHIAMATA NON \_ VALIDA.

**Aprire un consumer**  


```C++
HRESULT OpenConsumer(
  [in]   IUnknown *pDevice,
  [out]  IDXGIXSurfaceConsumer **ppConsumer
);
```



**Parametri**  
 *pDevice* \[ Pollici\]  
 Dispositivo consumer che consente di accodare le superfici dalla coda di superficie. 
 *ppConsumer* \[ out \]  Restituisce un oggetto all'interfaccia del consumer.  


**Valori restituiti**

Se il dispositivo non è in grado di condividere le superfici, restituisce ERRORE DXGI \_ \_ CHIAMATA NON \_ VALIDA.

**Osservazioni:**

Questa funzione apre tutte le superfici nella coda per il dispositivo di input e le memorizza nella cache. Le chiamate successive a Dequeue verranno semplicemente memorizzate nella cache e non sarà necessario riaprire le superfici ogni volta.



### <a name="cloning-an-idxgixsurfacequeue"></a>Clonazione di un oggetto IDXGIXSurfaceQueue




```C++
typedef struct SHARED_SURFACE_QUEUE_CLONE_DESC {
  UINT         MetaDataSize;
  DWORD        Flags;
} SHARED_SURFACE_QUEUE_CLONE_DESC;
```



**I** **membri MetaDataSize** **e Flags** hanno lo stesso comportamento di CreateSurfaceQueue.  



```C++
HRESULT Clone(
  [in]   SHARED_SURFACE_QUEUE_CLONE_DESC *pDesc,
  [out]  IDXGIXSurfaceQueue **ppQueue
);
```



**Parametri**

*pDesc* \[ in \] uno struct che fornisce una descrizione dell'oggetto Clone da creare. Questo parametro deve essere inizializzato.  
*ppQueue* \[ out \] Restituisce l'oggetto inizializzato.  
</dl>

**Osservazioni:**

È possibile clonare da qualsiasi oggetto coda esistente, anche se non è la radice.  
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
*id* \[ in\]  
REFIID di una superficie 2D del dispositivo che consuma.  

-   Per un dispositivo IDirect3DDevice9, REFIID deve essere \_ \_ uuidof(IDirect3DTexture9).
-   Per un dispositivo ID3D10, REFIID deve essere \_ \_ uuidof(ID3D10Texture2D).
-   Per un dispositivo ID3D11, REFIID deve essere \_ \_ uuidof(ID3D11Texture2D).

*ppSurface* \[ out \] Restituisce un puntatore alla superficie.  
*pBuffer* \[ in, out Un parametro facoltativo e se non NULL, in caso di restituzione, contiene i metadati passati \] nella chiamata di accodamento corrispondente.   
*pBufferSize* \[ in, out \] Le dimensioni di *pBuffer*, in byte. Restituisce il numero di byte restituiti in *pBuffer*. Se la chiamata di accodamento non ha fornito metadati, *pBuffer* è impostato su 0.  
*dwTimeout* \[ in \] Specifica un valore di timeout. Per altre informazioni, vedere Note.  
</dl>

**Valori restituiti**

Questa funzione può restituire WAIT TIMEOUT se viene specificato un valore di timeout e \_ la funzione non restituisce prima del valore di timeout. Vedere la sezione Osservazioni. Se non sono disponibili superfici, la funzione restituisce con *ppSurface* impostato su **NULL,** *pBufferSize* impostato su 0 e il valore restituito è 0x80070120 (WIN32 \_ TO \_ HRESULT(WAIT \_ TIMEOUT)).  
</dl>

**Osservazioni:**

Questa API può bloccarsi se la coda è vuota. Il *parametro dwTimeout* funziona in modo identico alle API di sincronizzazione di Windows, ad esempio WaitForSingleObject. Per un comportamento non bloccante, usare un timeout di 0.  
</dl>

### <a name="isurfaceproducer"></a>ISurfaceProducer

Questa interfaccia fornisce due metodi che consentono all'app di accodare superfici. Dopo l'accodamento di una superficie, il puntatore di superficie non è più valido e non è sicuro da usare. L'unica azione che l'applicazione deve eseguire con il puntatore è rilasciarla.



| Metodo                          | Descrizione                                                                                                                                                      |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| ISurfaceProducer::Enqueue | Accoda una superficie all'oggetto coda. Al termine della chiamata, il producer viene eseguito con la superficie e la superficie è pronta per un altro dispositivo. |
| ISurfaceProducer::Flush   | Utilizzato se le applicazioni devono avere un comportamento non bloccante. Per ulteriori informazioni, vedere Note.                                                                  |



 

**Enqueue**  


```C++
HRESULT Enqueue(
  [in]  IUnknown *pSurface,
  [in]  void *pBuffer,
  [in]  UINT BufferSize,
  [in]  DWORD Flags
);
```



**Parametri**  
*pSurface* \[ Pollici\]  
La superficie del dispositivo di produzione che deve essere accodata. Questa superficie deve essere una superficie disaccodata dalla stessa rete di accodamento. *pBuffer* \[ in \] Parametro facoltativo, usato per passare i metadati. Deve puntare ai dati che verranno passati alla chiamata di annullamento della coda.  
*BufferSize* \[ in \] Dimensioni di *pBuffer*, in byte.  
*Flag* \[ in \] Parametro facoltativo che controlla il comportamento di questa funzione. L'unico flag è SURFACE \_ QUEUE FLAG DO NOT \_ \_ \_ \_ WAIT. Vedere la sezione Osservazioni per Flush. Se non viene passato alcun flag (*Flags* == 0), viene usato il comportamento di blocco predefinito.  
</dl>

**Valori restituiti**

Questa funzione può restituire DXGI ERROR WAS STILL DRAWING se viene usato un \_ flag SURFACE QUEUE FLAG DO \_ NOT \_ \_ \_ \_ \_ \_ \_ WAIT.  
</dl>

**Osservazioni:**

-   Questa funzione inserisce la superficie nella coda. Se l'applicazione non specifica SURFACE QUEUE FLAG DO NOT WAIT, questa funzione è bloccata e esegue una sincronizzazione GPU-CPU per garantire che tutto il rendering sulla superficie \_ \_ \_ \_ \_ accodata sia completo. Se questa funzione ha esito positivo, sarà disponibile una superficie per la deaccodazione. Se si vuole un comportamento non bloccante, usare il flag DO \_ NOT \_ WAIT. Per informazioni dettagliate, vedere Flush().
-   In base alle regole di conteggio dei riferimenti COM, la superficie restituita da Dequeue sarà AddRef(), quindi l'applicazione non deve eseguire questa operazione. Dopo aver chiamato Enqueue, l'applicazione deve rilasciare la superficie perché non la usa più.

**Svuotamento**  


```C++
HRESULT Flush(
  [in]  DWORD Flags,
  [out] UINT *nSurfaces
);
```



**Parametri**  
*Flag* \[ Pollici\]  
L'unico flag è SURFACE \_ QUEUE FLAG DO NOT \_ \_ \_ \_ WAIT. Vedere la sezione Osservazioni. *nSurfaces* \[ out \] Restituisce il numero di superfici ancora in sospeso e non scaricate.  
</dl>

**Valori restituiti**

Questa funzione può restituire DXGI ERROR WAS STILL DRAWING se viene usato il \_ flag SURFACE QUEUE FLAG DO \_ NOT \_ \_ \_ \_ \_ \_ \_ WAIT. Questa funzione restituisce S \_ OK se le superfici sono state scaricate correttamente. Questa funzione restituisce DXGI \_ ERROR WAS STILL DRAWING solo se non sono state \_ \_ \_ scaricate superfici. Insieme, il valore restituito *e nSurfaces* indicano all'applicazione quali operazioni sono state eseguite e se è rimasto del lavoro da eseguire.  
</dl>

**Osservazioni:**

Lo scaricamento è significativo solo se la chiamata precedente all'accodamento ha usato il flag DO NOT WAIT; in caso contrario, sarà \_ \_ un'operazione no-op. Se la chiamata all'accodamento usa il flag DO NOT WAIT, l'accodamento viene restituito immediatamente e la sincronizzazione \_ \_ GPU-CPU non è garantita. La superficie è ancora considerata accodata, il dispositivo di produzione non può continuare a usarlo, ma non è disponibile per la rimozione della coda. Per provare a eseguire il commit della superficie per la deaccodazione, è necessario chiamare Flush. Lo scaricamento tenta di eseguire il commit di tutte le superfici attualmente accodate. Se non viene passato alcun flag a Flush, blocca e cancella l'intera coda, preparando tutte le superfici in essa presenti per la rimozione dalla coda. Se viene usato il flag DO NOT WAIT, la coda controlla le superfici per verificare se una di esse è pronta. Questo passaggio non \_ \_ è bloccante. Le superfici che hanno completato la sincronizzazione GPU-CPU saranno pronte per il dispositivo consumer. Le superfici ancora in sospeso non saranno interessate. La funzione restituisce il numero di superfici che devono ancora essere scaricate.

> [!Note]  
> Lo scaricamento non interrompe la semantica della coda. L'API garantisce che venga eseguito il commit delle superfici accodati prima delle superfici accodati in un secondo momento, indipendentemente dal momento in cui viene eseguita la sincronizzazione GPU-CPU.

 

  
</dl>

### <a name="direct3d-9ex-and-dxgi-interop-helper-how-to-use"></a>Helper di interoperabilità Direct3D 9Ex e DXGI: come usare

Si prevede che la maggior parte dei casi di utilizzo coinvolgono due dispositivi che condividono una serie di superfici. Poiché questo è anche lo scenario più semplice, questo documento descrive in dettaglio come usare le API per raggiungere questo obiettivo, illustra una variante non bloccante e termina con una breve sezione sull'inizializzazione per tre dispositivi.

### <a name="two-devices"></a>Due dispositivi

L'applicazione di esempio che usa questo helper può usare Direct3D 9Ex e Direct3D 11 insieme. L'applicazione può elaborare il contenuto con entrambi i dispositivi e presentare il contenuto usando Direct3D 9. L'elaborazione può significare il rendering del contenuto, la decodifica di video, l'esecuzione di compute shader e così via. Per ogni frame, l'applicazione verrà prima elaborata con Direct3D 11, quindi verrà elaborata con Direct3D 9 e infine presente con Direct3D 9. Inoltre, l'elaborazione con Direct3D 11 produrrà alcuni metadati che direct3D 9 presente dovrà utilizzare. Questa sezione illustra l'utilizzo dell'helper in tre parti che corrispondono a questa sequenza: inizializzazione, ciclo principale e pulizia.

**Inizializzazione**  
L'inizializzazione prevede i passaggi seguenti:  

1.  Inizializzare entrambi i dispositivi.
2.  Creare la coda radice: m \_ 11to9Queue.
3.  Clonare dalla coda radice: m \_ 9to11Queue.
4.  Chiamare OpenProducer/OpenConsumer in entrambe le code.

I nomi delle code usano i numeri 9 e 11 per indicare quale API è il producer e quale consumer: **m \_**_producer_*_to_*_consumer_*_Queue_*. Di conseguenza, m 11to9Queue indica una coda per cui il dispositivo Direct3D 11 produce superfici utilizzate dal dispositivo \_ Direct3D 9. Analogamente, m 9to11Queue indica una coda per cui Direct3D 9 produce superfici utilizzate da \_ Direct3D 11.  
La coda radice è inizialmente piena e tutte le code clonate sono inizialmente vuote. Questo non deve essere un problema per l'applicazione, ad eccezione del primo ciclo delle code e delle code e della disponibilità dei metadati. Se una coda richiede metadati ma non ne è stato impostato alcuno (perché inizialmente non è presente alcun elemento o l'accodamento non ha impostato alcun valore), la coda visualizza che non è stato ricevuto alcun metadati.  

1.  **Inizializzare entrambi i dispositivi.**  
    ```C++
    m_pD3D9Device = InitializeD3D9ExDevice();
    m_pD3D11Device = InitializeD3D11Device();
    ```

    

2.  **Creare la coda radice.**  
    Questo passaggio crea anche le superfici. Le restrizioni relative alle dimensioni e al formato sono identiche alla creazione di qualsiasi risorsa condivisa. Le dimensioni del buffer dei metadati sono fisse in fase di creazione e in questo caso si passerà semplicemente un UINT.  
    La coda deve essere creata con un numero fisso di superfici. Le prestazioni variano a seconda dello scenario. La presenza di più superfici aumenta le probabilità che i dispositivi siano occupati. Ad esempio, se è presente una sola superficie, non sarà presente alcuna parallelizzazione tra i due dispositivi. D'altra parte, l'aumento del numero di superfici aumenta il footprint di memoria, con un possibile peggioramento delle prestazioni. In questo esempio vengono utilizzate due superfici.  
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
    Ogni coda clonata deve usare le stesse superfici, ma può avere dimensioni del buffer di metadati diverse e flag diversi. In questo caso, non sono presenti metadati da Direct3D 9 a Direct3D 11.  
    ```C++
    SURFACE_QUEUE_CLONE_DESC Desc;
    Desc.MetaDataSize = 0;
    Desc.Flags        = 0;

    m_11to9Queue->Clone(&Desc, &m_9to11Queue);
    ```

    

4.  **Aprire i dispositivi producer e consumer.**  
    L'applicazione deve eseguire questo passaggio prima di chiamare Enqueue e Dequeue. L'apertura di un producer e di un consumer restituisce interfacce che contengono le API di accodamento/annullamento della coda.  
    ```C++
    // Open for m_p9to11Queue.
    m_p9to11Queue->OpenProducer(m_pD3D9Device, &m_pD3D9Producer);
    m_p9to11Queue->OpenConsumer(m_pD3D11Device, &m_pD3D11Consumer);

    // Open for m_p11to9Queue.
    m_p11to9Queue->OpenProducer(m_pD3D11Device, &m_pD3D11Producer);
    m_p11to9Queue->OpenConsumer(m_pD3D9Device, &m_pD3D9Consumer);
    ```

    

**Ciclo Main**  
L'utilizzo della coda è modellato in base al problema producer/consumer classico. Si pensi a questo dal punto di vista dei dispositivi. Ogni dispositivo deve eseguire questi passaggi: rimozione dalla coda per ottenere una superficie dalla coda di utilizzo, elaborazione in superficie e quindi accodamento nella coda di produzione. Per il dispositivo Direct3D 11, l'utilizzo di Direct3D 9 è quasi identico.  


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

L'esempio precedente ha senso per un caso di utilizzo multithreading in cui ogni dispositivo ha un proprio thread. L'esempio usa le versioni di blocco delle API: INFINITE per il timeout e nessun flag da accodare. Se si vuole usare l'helper in modo non bloccante, è necessario apportare solo alcune modifiche. Questa sezione illustra l'uso non bloccante con entrambi i dispositivi in un unico thread.

**Inizializzazione**  
L'inizializzazione è identica ad eccezione dei flag . Poiché l'applicazione è a thread singolo, usare tale flag per la creazione. In questo modo viene disattivata parte del codice di sincronizzazione, che potrebbe migliorare le prestazioni.  


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



L'apertura dei dispositivi producer e consumer è la stessa dell'esempio di blocco.  
**Uso della coda**  
Esistono molti modi per usare la coda in modo non bloccante con diverse caratteristiche delle prestazioni. L'esempio seguente è semplice, ma presenta prestazioni scarse a causa di un numero eccessivo di operazioni di rotazione e polling. Nonostante questi problemi, l'esempio mostra come usare l'helper. L'approccio consiste nel restare costantemente in un ciclo e dequeue, elaborare, accodare e scaricare. Se uno dei passaggi ha esito negativo perché la risorsa non è disponibile, l'applicazione prova semplicemente a eseguire di nuovo il ciclo successivo.  


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



Una soluzione più complessa potrebbe controllare il valore restituito dalla coda e dallo scaricamento per determinare se è necessario lo scaricamento.  
</dl>

### <a name="three-devices"></a>Tre dispositivi

Estendere gli esempi precedenti per coprire più dispositivi è semplice. Il codice seguente esegue l'inizializzazione. Dopo aver creato gli oggetti Producer/Consumer, il codice per usarli è lo stesso. In questo esempio sono disponibili tre dispositivi e quindi tre code. Le superfici fluire da Direct3D 9 a Direct3D 10 a Direct3D 11.


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



Come accennato in precedenza, la clonazione funziona allo stesso modo, indipendentemente dalla coda clonata. Ad esempio, la seconda chiamata Clone potrebbe essere stata rimossa dall'oggetto m \_ 9to10Queue.


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

È possibile creare soluzioni che usano l'interoperabilità per usare la potenza di più API DirectX. L'interoperabilità dell'API grafica di Windows offre ora un common surface management runtime DXGI 1.1. Questo runtime abilita il supporto della condivisione della superficie sincronizzata all'interno delle API appena sviluppate, ad esempio Direct3D 11, Direct3D 10.1 e Direct2D. I miglioramenti dell'interoperabilità tra le nuove API e le API esistenti migliorano la migrazione delle applicazioni e la compatibilità con le versioni precedenti. Le API consumer Direct3D 9Ex e DXGI 1.1 possono interagire, come illustrato con il meccanismo di sincronizzazione fornito tramite codice helper di esempio in MSDN Code Gallery.

 

 