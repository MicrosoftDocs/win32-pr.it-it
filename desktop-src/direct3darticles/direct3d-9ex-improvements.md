---
title: Miglioramenti di Direct3D 9Ex
description: In questo argomento viene descritto il supporto aggiunto di Windows 7 per la modalità Flip presente e le statistiche presenti associate in Direct3D 9Ex e Gestione finestre desktop.
ms.assetid: cb92a162-57eb-4aee-af7a-c8ece37075a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42eef10b6caaa959cb750f073c97a0f665384463
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399482"
---
# <a name="direct3d-9ex-improvements"></a><span data-ttu-id="bfd77-103">Miglioramenti di Direct3D 9Ex</span><span class="sxs-lookup"><span data-stu-id="bfd77-103">Direct3D 9Ex improvements</span></span>

<span data-ttu-id="bfd77-104">In questo argomento viene descritto il supporto aggiunto di Windows 7 per la modalità Flip presente e le statistiche presenti associate in Direct3D 9Ex e Gestione finestre desktop.</span><span class="sxs-lookup"><span data-stu-id="bfd77-104">This topic describes Windows 7's added support for Flip Mode Present and its associated present statistics in Direct3D 9Ex and Desktop Window Manager.</span></span> <span data-ttu-id="bfd77-105">Le applicazioni di destinazione includono video o applicazioni di presentazione basate sulla frequenza dei fotogrammi.</span><span class="sxs-lookup"><span data-stu-id="bfd77-105">Target applications include video or frame rate-based presentation applications.</span></span> <span data-ttu-id="bfd77-106">Le applicazioni che usano la modalità Flip 9Ex Direct3D presentano una riduzione del carico delle risorse di sistema quando DWM è abilitato.</span><span class="sxs-lookup"><span data-stu-id="bfd77-106">Applications that use Direct3D 9Ex Flip Mode Present reduce the system resource load when DWM is enabled.</span></span> <span data-ttu-id="bfd77-107">I miglioramenti attuali delle statistiche associati alla modalità Flip consentono alle applicazioni Direct3D 9Ex di controllare meglio la frequenza di presentazione fornendo i meccanismi di correzione e feedback in tempo reale.</span><span class="sxs-lookup"><span data-stu-id="bfd77-107">Present statistics enhancements associated with Flip Mode Present enable Direct3D 9Ex applications to better control the rate of presentation by providing real-time feedback and correction mechanisms.</span></span> <span data-ttu-id="bfd77-108">Sono incluse spiegazioni dettagliate e puntatori alle risorse di esempio.</span><span class="sxs-lookup"><span data-stu-id="bfd77-108">Detailed explanations and pointers to sample resources are included.</span></span>

<span data-ttu-id="bfd77-109">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="bfd77-109">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="bfd77-110">Miglioramenti di Direct3D 9Ex per Windows 7</span><span class="sxs-lookup"><span data-stu-id="bfd77-110">What's Improved about Direct3D 9Ex for Windows 7</span></span>](#whats-improved-about-direct3d-9ex-for-windows-7)
-   [<span data-ttu-id="bfd77-111">Presentazione della modalità Flip 9EX Direct3D</span><span class="sxs-lookup"><span data-stu-id="bfd77-111">Direct3D 9EX Flip Mode Presentation</span></span>](#direct3d-9ex-flip-mode-presentation)
-   [<span data-ttu-id="bfd77-112">Modello di programmazione e API</span><span class="sxs-lookup"><span data-stu-id="bfd77-112">Programming Model and APIs</span></span>](#programming-model-and-apis)
    -   [<span data-ttu-id="bfd77-113">Come acconsentire esplicitamente al modello di Flip 9Ex Direct3D</span><span class="sxs-lookup"><span data-stu-id="bfd77-113">How to Opt Into the Direct3D 9Ex Flip Model</span></span>](#how-to-opt-into-the-direct3d-9ex-flip-model)
    -   [<span data-ttu-id="bfd77-114">Linee guida di progettazione per Direct3D 9Ex flip model Applications</span><span class="sxs-lookup"><span data-stu-id="bfd77-114">Design Guidelines for Direct3D 9Ex Flip Model Applications</span></span>](#design-guidelines-for-direct3d-9ex-flip-model-applications)
    -   [<span data-ttu-id="bfd77-115">Sincronizzazione dei frame delle applicazioni di modelli 9Ex Flip Direct3D</span><span class="sxs-lookup"><span data-stu-id="bfd77-115">Frame Synchronization of Direct3D 9Ex Flip Model Applications</span></span>](#frame-synchronization-of-direct3d-9ex-flip-model-applications)
    -   [<span data-ttu-id="bfd77-116">Sincronizzazione dei frame per le applicazioni con finestra quando DWM è disattivato</span><span class="sxs-lookup"><span data-stu-id="bfd77-116">Frame Synchronization for Windowed Applications When DWM is Off</span></span>](#frame-synchronization-for-windowed-applications-when-dwm-is-off)
-   [<span data-ttu-id="bfd77-117">Procedura dettagliata di un esempio Direct3D 9Ex flip model e present Statistics</span><span class="sxs-lookup"><span data-stu-id="bfd77-117">Walk-Through of a Direct3D 9Ex Flip Model and Present Statistics Sample</span></span>](#walk-through-of-a-direct3d-9ex-flip-model-and-present-statistics-sample)
    -   [<span data-ttu-id="bfd77-118">Riepilogo dei consigli di programmazione per la sincronizzazione dei frame</span><span class="sxs-lookup"><span data-stu-id="bfd77-118">Summary of Programming Recommendations for Frame Synchronization</span></span>](#summary-of-programming-recommendations-for-frame-synchronization)
-   [<span data-ttu-id="bfd77-119">Conclusione dei miglioramenti di Direct3D 9Ex</span><span class="sxs-lookup"><span data-stu-id="bfd77-119">Conclusion about Direct3D 9Ex Improvements</span></span>](#conclusion-about-direct3d-9ex-improvements)
-   [<span data-ttu-id="bfd77-120">Chiamata all'azione</span><span class="sxs-lookup"><span data-stu-id="bfd77-120">Call to Action</span></span>](#call-to-action)
-   [<span data-ttu-id="bfd77-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bfd77-121">Related topics</span></span>](#related-topics)

## <a name="whats-improved-about-direct3d-9ex-for-windows-7"></a><span data-ttu-id="bfd77-122">Miglioramenti di Direct3D 9Ex per Windows 7</span><span class="sxs-lookup"><span data-stu-id="bfd77-122">What's Improved about Direct3D 9Ex for Windows 7</span></span>

<span data-ttu-id="bfd77-123">La presentazione della modalità Flip di Direct3D 9Ex è una modalità migliorata per presentare immagini in Direct3D 9Ex che consente di passare in modo efficiente le immagini sottoposte a rendering a Windows 7 Gestione finestre desktop (DWM) per la composizione.</span><span class="sxs-lookup"><span data-stu-id="bfd77-123">Flip Mode Presentation of Direct3D 9Ex is an improved mode of presenting images in Direct3D 9Ex that efficiently hands off rendered images to Windows 7 Desktop Window Manager (DWM) for composition.</span></span> <span data-ttu-id="bfd77-124">A partire da Windows Vista, DWM compone l'intero desktop.</span><span class="sxs-lookup"><span data-stu-id="bfd77-124">Beginning in Windows Vista, DWM composes the entire Desktop.</span></span> <span data-ttu-id="bfd77-125">Quando DWM è abilitato, le applicazioni in modalità finestra presentano il proprio contenuto sul desktop usando un metodo denominato modalità BLT presente in DWM (o modello BLT).</span><span class="sxs-lookup"><span data-stu-id="bfd77-125">When DWM is enabled, windowed mode applications present their contents on the Desktop by using a method called Blt Mode Present to DWM (or Blt Model).</span></span> <span data-ttu-id="bfd77-126">Con il modello BLT, DWM mantiene una copia della superficie di rendering di Direct3D 9Ex per la composizione del desktop.</span><span class="sxs-lookup"><span data-stu-id="bfd77-126">With Blt Model, DWM maintains a copy of the Direct3D 9Ex rendered surface for Desktop composition.</span></span> <span data-ttu-id="bfd77-127">Quando l'applicazione viene aggiornata, il nuovo contenuto viene copiato nell'area di DWM tramite un BLT.</span><span class="sxs-lookup"><span data-stu-id="bfd77-127">When the application updates, the new content is copied to the DWM surface through a blt.</span></span> <span data-ttu-id="bfd77-128">Per le applicazioni che contengono contenuto Direct3D e GDI, i dati GDI vengono anche copiati nella superficie di DWM.</span><span class="sxs-lookup"><span data-stu-id="bfd77-128">For applications that contain Direct3D and GDI content, the GDI data is also copied onto the DWM surface.</span></span>

<span data-ttu-id="bfd77-129">Disponibile in Windows 7, la modalità Flip presente in DWM (o Capovolgi modello) è un nuovo metodo di presentazione che consente essenzialmente di passare handle di superfici dell'applicazione tra applicazioni in modalità finestra e DWM.</span><span class="sxs-lookup"><span data-stu-id="bfd77-129">Available in Windows 7, Flip Mode Present to DWM (or Flip Model) is a new presentation method that essentially enables passing handles of application surfaces between windowed mode applications and DWM.</span></span> <span data-ttu-id="bfd77-130">Oltre al salvataggio delle risorse, il modello Flip supporta statistiche attuali avanzate.</span><span class="sxs-lookup"><span data-stu-id="bfd77-130">In addition to saving resources, Flip Model supports enhanced present statistics.</span></span>

<span data-ttu-id="bfd77-131">Le statistiche attuali sono informazioni sugli intervalli di frame che possono essere usate dalle applicazioni per sincronizzare flussi video e audio e per eseguire il ripristino da problemi di riproduzione video.</span><span class="sxs-lookup"><span data-stu-id="bfd77-131">Present statistics are frame-timing information that applications can use to synchronize video and audio streams and recover from video playback glitches.</span></span> <span data-ttu-id="bfd77-132">Le informazioni relative alla temporizzazione dei frame nelle statistiche attuali consentono alle applicazioni di regolare la frequenza di presentazione dei fotogrammi video per una presentazione più uniforme.</span><span class="sxs-lookup"><span data-stu-id="bfd77-132">The frame-timing information in present statistics allows applications to adjust the presentation rate of their video frames for smoother presentation.</span></span> <span data-ttu-id="bfd77-133">In Windows Vista, in cui DWM gestisce una copia corrispondente della superficie del frame per la composizione del desktop, le applicazioni possono utilizzare le statistiche presenti disponibili in DWM.</span><span class="sxs-lookup"><span data-stu-id="bfd77-133">In Windows Vista, where DWM maintains a corresponding copy of the frame surface for Desktop composition, applications can use present statistics provided by DWM.</span></span> <span data-ttu-id="bfd77-134">Questo metodo per ottenere le statistiche attuali sarà ancora disponibile in Windows 7 per le applicazioni esistenti.</span><span class="sxs-lookup"><span data-stu-id="bfd77-134">This method of obtaining present statistics will still be available in Windows 7 for existing applications.</span></span>

<span data-ttu-id="bfd77-135">In Windows 7, le applicazioni basate su Direct3D 9Ex che adottano il modello Flip devono usare le API D3D9Ex per ottenere le statistiche attuali.</span><span class="sxs-lookup"><span data-stu-id="bfd77-135">In Windows 7, Direct3D 9Ex-based applications that adopt Flip Model should use D3D9Ex APIs to obtain present statistics.</span></span> <span data-ttu-id="bfd77-136">Quando DWM è abilitato, la modalità a finestra e le applicazioni Direct3D 9Ex in modalità esclusiva a schermo intero possono prevedere le stesse informazioni sulle statistiche presenti quando si usa Capovolgi modello.</span><span class="sxs-lookup"><span data-stu-id="bfd77-136">When DWM is enabled, windowed mode and full-screen exclusive mode Direct3D 9Ex applications can expect the same present statistics information when using Flip Model.</span></span> <span data-ttu-id="bfd77-137">Direct3D 9Ex flip model present Statistics consente alle applicazioni di eseguire query per le statistiche presenti in tempo reale, anziché dopo che il frame è stato visualizzato sullo schermo; le stesse informazioni sulle statistiche sono disponibili per le applicazioni abilitate per la Flip-Model in modalità finestra come applicazioni a schermo intero. un flag aggiunto nelle API D3D9Ex consente alle applicazioni flip model di eliminare in modo efficace i frame tardivi in fase di presentazione.</span><span class="sxs-lookup"><span data-stu-id="bfd77-137">Direct3D 9Ex Flip Model present statistics enable applications to query for present statistics in real time, rather than after the frame has been shown on screen; the same present statistics information is available for windowed-mode Flip-Model enabled applications as full-screen applications; an added flag in D3D9Ex APIs allows Flip Model applications to effectively discard late frames at presentation time.</span></span>

<span data-ttu-id="bfd77-138">Il modello Direct3D 9Ex Flip deve essere usato dalle nuove applicazioni di presentazione basate su video o frequenza dei fotogrammi destinate a Windows 7.</span><span class="sxs-lookup"><span data-stu-id="bfd77-138">Direct3D 9Ex Flip Model should be used by new video or frame rate-based presentation applications that target Windows 7.</span></span> <span data-ttu-id="bfd77-139">A causa della sincronizzazione tra DWM e il runtime 9Ex Direct3D, le applicazioni che utilizzano il modello Flip devono specificare tra 2 e 4 buffer per garantire una presentazione uniforme.</span><span class="sxs-lookup"><span data-stu-id="bfd77-139">Because of the synchronization between DWM and the Direct3D 9Ex runtime, applications that use Flip Model should specify between 2 to 4 backbuffers to ensure smooth presentation.</span></span> <span data-ttu-id="bfd77-140">Le applicazioni che usano le informazioni statistiche attuali trarranno vantaggio dall'uso dei miglioramenti delle statistiche presenti in flip model Enabled.</span><span class="sxs-lookup"><span data-stu-id="bfd77-140">Those applications that use present statistics information will benefit from using Flip Model enabled present statistics enhancements.</span></span>

## <a name="direct3d-9ex-flip-mode-presentation"></a><span data-ttu-id="bfd77-141">Presentazione della modalità Flip 9EX Direct3D</span><span class="sxs-lookup"><span data-stu-id="bfd77-141">Direct3D 9EX Flip Mode Presentation</span></span>

<span data-ttu-id="bfd77-142">I miglioramenti delle prestazioni della modalità Flip 9Ex di Direct3D sono significativi nel sistema quando DWM è acceso e quando l'applicazione è in modalità finestra, anziché in modalità esclusiva a schermo intero.</span><span class="sxs-lookup"><span data-stu-id="bfd77-142">Performance improvements of Direct3D 9Ex Flip Mode Present are significant on the system when DWM is on and when the application is in windowed mode, rather than in full screen exclusive mode.</span></span> <span data-ttu-id="bfd77-143">Nella tabella e nell'illustrazione seguenti viene illustrato un confronto semplificato degli utilizzi della larghezza di banda della memoria e delle letture e scritture di sistema delle applicazioni con finestra che scelgono Capovolgi modello rispetto al modello BLT utilizzo predefinito.</span><span class="sxs-lookup"><span data-stu-id="bfd77-143">The following table and illustration show a simplified comparison of memory bandwidth usages and system reads and writes of windowed applications that choose Flip Model versus the default usage Blt Model.</span></span>



| <span data-ttu-id="bfd77-144">Modalità BLT presente in DWM</span><span class="sxs-lookup"><span data-stu-id="bfd77-144">Blt mode present to DWM</span></span>                                                                                                 | <span data-ttu-id="bfd77-145">Modalità D3D9Ex Flip presente in DWM</span><span class="sxs-lookup"><span data-stu-id="bfd77-145">D3D9Ex Flip Mode Present to DWM</span></span>                                             |
|-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="bfd77-146">1. l'applicazione aggiorna il frame (scrittura)</span><span class="sxs-lookup"><span data-stu-id="bfd77-146">1. The application updates its frame (Write)</span></span><br/>                                                                 | <span data-ttu-id="bfd77-147">1. l'applicazione aggiorna il frame (scrittura)</span><span class="sxs-lookup"><span data-stu-id="bfd77-147">1. The application updates its frame (Write)</span></span><br/>                     |
| <span data-ttu-id="bfd77-148">2. il runtime Direct3D copia il contenuto della superficie in una superficie di reindirizzamento DWM (lettura, scrittura)</span><span class="sxs-lookup"><span data-stu-id="bfd77-148">2. Direct3D runtime copies surface contents to a DWM redirection surface (Read, Write)</span></span><br/>                       | <span data-ttu-id="bfd77-149">2. il runtime Direct3D passa l'area dell'applicazione a DWM</span><span class="sxs-lookup"><span data-stu-id="bfd77-149">2. Direct3D runtime passes the application surface to DWM</span></span><br/>        |
| <span data-ttu-id="bfd77-150">3. una volta completata la copia della superficie condivisa, DWM esegue il rendering dell'area dell'applicazione sullo schermo (lettura, scrittura)</span><span class="sxs-lookup"><span data-stu-id="bfd77-150">3. After the shared surface copy is completed, DWM renders the application surface onto screen (Read, Write)</span></span><br/> | <span data-ttu-id="bfd77-151">3. DWM esegue il rendering dell'area dell'applicazione sullo schermo (lettura, scrittura)</span><span class="sxs-lookup"><span data-stu-id="bfd77-151">3. DWM renders the application surface onto screen (Read, Write)</span></span><br/> |



 

![illustrazione di un confronto tra il modello BLT e il modello Flip](images/blt-flip-mode-present.png)

<span data-ttu-id="bfd77-153">La modalità Flip consente di ridurre l'utilizzo della memoria di sistema riducendo il numero di letture e scritture da parte del runtime Direct3D per la composizione del frame finestra di DWM.</span><span class="sxs-lookup"><span data-stu-id="bfd77-153">Flip Mode Present reduces system memory usage by reducing the number of reads and writes by the Direct3D runtime for the windowed frame composition by DWM.</span></span> <span data-ttu-id="bfd77-154">In questo modo si riduce il consumo di energia del sistema e l'utilizzo complessivo della memoria.</span><span class="sxs-lookup"><span data-stu-id="bfd77-154">This reduces the system power consumption and overall memory usage.</span></span>

<span data-ttu-id="bfd77-155">Le applicazioni possono sfruttare i vantaggi di Direct3D 9Ex Flip mode presenta i miglioramenti delle statistiche quando DWM è acceso, indipendentemente dal fatto che l'applicazione sia in modalità finestra o in modalità esclusiva a schermo intero.</span><span class="sxs-lookup"><span data-stu-id="bfd77-155">Applications can take advantage of Direct3D 9Ex Flip Mode present statistics enhancements when DWM is on, regardless of whether the application is in windowed mode or in full screen exclusive mode.</span></span>

## <a name="programming-model-and-apis"></a><span data-ttu-id="bfd77-156">Modello di programmazione e API</span><span class="sxs-lookup"><span data-stu-id="bfd77-156">Programming Model and APIs</span></span>

<span data-ttu-id="bfd77-157">Le nuove applicazioni per la misurazione della frequenza dei fotogrammi e dei video che usano le API Direct3D 9Ex in Windows 7 possono sfruttare i vantaggi della memoria e del risparmio energetico e della presentazione migliorata offerta dalla modalità Flip presente durante l'esecuzione in Windows 7.</span><span class="sxs-lookup"><span data-stu-id="bfd77-157">New video or frame rate-gauging applications that use Direct3D 9Ex APIs on Windows 7 can take advantage of the memory and power savings and of the improved presentation offered by Flip Mode Present when running on Windows 7.</span></span> <span data-ttu-id="bfd77-158">Quando è in esecuzione in versioni precedenti di Windows, il runtime di Direct3D usa per impostazione predefinita l'applicazione in modalità BLT.</span><span class="sxs-lookup"><span data-stu-id="bfd77-158">(When running on previous Windows versions, the Direct3D runtime defaults the application to Blt Mode Present.)</span></span>

<span data-ttu-id="bfd77-159">La modalità Flip prevede che l'applicazione possa sfruttare i vantaggi dei meccanismi di correzione e feedback delle statistiche presenti in tempo reale quando DWM è acceso.</span><span class="sxs-lookup"><span data-stu-id="bfd77-159">Flip Mode Present entails that the application can take advantage of real-time present statistics feedback and correction mechanisms when DWM is on.</span></span> <span data-ttu-id="bfd77-160">Tuttavia, le applicazioni che usano la modalità Flip presentano le limitazioni quando usano il rendering dell'API GDI simultaneo.</span><span class="sxs-lookup"><span data-stu-id="bfd77-160">However, applications that use Flip Mode Present should be aware of limitations when they use concurrent GDI API rendering.</span></span>

<span data-ttu-id="bfd77-161">È possibile modificare le applicazioni esistenti per sfruttare i vantaggi della modalità Flip presente, con gli stessi vantaggi e avvertenze delle applicazioni appena sviluppate.</span><span class="sxs-lookup"><span data-stu-id="bfd77-161">You can modify existing applications to take advantage of Flip Mode Present, with the same benefits and caveats as the newly developed applications.</span></span>

### <a name="how-to-opt-into-the-direct3d-9ex-flip-model"></a><span data-ttu-id="bfd77-162">Come acconsentire esplicitamente al modello di Flip 9Ex Direct3D</span><span class="sxs-lookup"><span data-stu-id="bfd77-162">How to Opt Into the Direct3D 9Ex Flip Model</span></span>

<span data-ttu-id="bfd77-163">Le applicazioni Direct3D 9Ex destinate a Windows 7 possono optare per il modello Flip creando la catena di scambio con il valore di enumerazione [**\_ FLIPEX D3DSWAPEFFECT**](/windows/desktop/direct3d9/d3dswapeffect) .</span><span class="sxs-lookup"><span data-stu-id="bfd77-163">Direct3D 9Ex applications that target Windows 7 can opt into the Flip Model by creating the swap chain with the [**D3DSWAPEFFECT\_FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) enumeration value.</span></span> <span data-ttu-id="bfd77-164">Per acconsentire esplicitamente al modello Flip, le applicazioni specificano la struttura dei [**\_ parametri D3DPRESENT**](/windows/desktop/direct3d9/d3dpresent-parameters) , quindi passano un puntatore a questa struttura quando chiamano l'API [**IDirect3D9Ex:: CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) .</span><span class="sxs-lookup"><span data-stu-id="bfd77-164">To opt into the Flip Model, applications specify the [**D3DPRESENT\_PARAMETERS**](/windows/desktop/direct3d9/d3dpresent-parameters) structure, and then pass a pointer to this structure when they call the [**IDirect3D9Ex::CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) API.</span></span> <span data-ttu-id="bfd77-165">In questa sezione viene descritto in che modo le applicazioni destinate a Windows 7 utilizzano **IDirect3D9Ex:: CreateDeviceEx** per acconsentire esplicitamente al modello flip.</span><span class="sxs-lookup"><span data-stu-id="bfd77-165">This section describes how applications that target Windows 7 use **IDirect3D9Ex::CreateDeviceEx** to opt into the Flip Model.</span></span> <span data-ttu-id="bfd77-166">Per ulteriori informazioni sull'API **IDirect3D9Ex:: CreateDeviceEx** , vedere **IDirect3D9Ex:: CreateDeviceEx su MSDN**.</span><span class="sxs-lookup"><span data-stu-id="bfd77-166">For more information about the **IDirect3D9Ex::CreateDeviceEx** API, see **IDirect3D9Ex::CreateDeviceEx on MSDN**.</span></span>

<span data-ttu-id="bfd77-167">Per praticità, la sintassi [**dei \_ parametri D3DPRESENT**](/windows/desktop/direct3d9/d3dpresent-parameters) e [**IDirect3D9Ex:: CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) viene ripetuta qui.</span><span class="sxs-lookup"><span data-stu-id="bfd77-167">For convenience, the syntax of [**D3DPRESENT\_PARAMETERS**](/windows/desktop/direct3d9/d3dpresent-parameters) and [**IDirect3D9Ex::CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) is repeated here.</span></span>

``` syntax
HRESULT CreateDeviceEx(
  UINT Adapter,
  D3DDEVTYPE DeviceType,
  HWND hFocusWindow,
  DWORD BehaviorFlags,
  D3DPRESENT_PARAMETERS* pPresentationParameters,
  D3DDISPLAYMODEEX *pFullscreenDisplayMode,
  IDirect3DDevice9Ex **ppReturnedDeviceInterface
);
```

``` syntax
typedef struct D3DPRESENT_PARAMETERS {
    UINT BackBufferWidth, BackBufferHeight;
    D3DFORMAT BackBufferFormat;
    UINT BackBufferCount;
    D3DMULTISAMPLE_TYPE MultiSampleType;
    DWORD MultiSampleQuality;
    D3DSWAPEFFECT SwapEffect;
    HWND hDeviceWindow;
    BOOL Windowed;
    BOOL EnableAutoDepthStencil;
    D3DFORMAT AutoDepthStencilFormat;
    DWORD Flags;
    UINT FullScreen_RefreshRateInHz;
    UINT PresentationInterval;
} D3DPRESENT_PARAMETERS, *LPD3DPRESENT_PARAMETERS;
```

<span data-ttu-id="bfd77-168">Quando si modificano le applicazioni Direct3D 9Ex per Windows 7 per acconsentire al modello Flip, è necessario considerare gli elementi seguenti sui membri specificati [**dei \_ parametri D3DPRESENT**](/windows/desktop/direct3d9/d3dpresent-parameters):</span><span class="sxs-lookup"><span data-stu-id="bfd77-168">When you modify Direct3D 9Ex applications for Windows 7 to opt into the Flip Model, you should consider the following items about the specified members of [**D3DPRESENT\_PARAMETERS**](/windows/desktop/direct3d9/d3dpresent-parameters):</span></span>

<dl> <dt>

<span data-ttu-id="bfd77-169">**BackBufferCount**</span><span class="sxs-lookup"><span data-stu-id="bfd77-169">**BackBufferCount**</span></span>
</dt> <dd>

<span data-ttu-id="bfd77-170">(Solo Windows 7)</span><span class="sxs-lookup"><span data-stu-id="bfd77-170">(Windows 7 Only)</span></span>

<span data-ttu-id="bfd77-171">Quando **SwapEffect** è impostato sul nuovo tipo di \_ effetto catena di scambio D3DSWAPEFFECT FLIPEX, il numero di buffer nascosto deve essere uguale o maggiore di 2, per evitare una riduzione delle prestazioni dell'applicazione come conseguenza dell'attesa del rilascio di DWM da parte del buffer presente precedente.</span><span class="sxs-lookup"><span data-stu-id="bfd77-171">When **SwapEffect** is set to the new D3DSWAPEFFECT\_FLIPEX swap chain effect type, the back buffer count should be equal or greater than 2, to prevent an application performance penalty as a result of waiting on the previous Present buffer to be released by DWM.</span></span>

<span data-ttu-id="bfd77-172">Quando l'applicazione usa anche le statistiche presenti associate a D3DSWAPEFFECT \_ FLIPEX, è consigliabile impostare il numero di buffer indietro su da 2 a 4.</span><span class="sxs-lookup"><span data-stu-id="bfd77-172">When the application also uses present statistics associated with D3DSWAPEFFECT\_FLIPEX, we recommend that you set the back buffer count to from 2 to 4.</span></span>

<span data-ttu-id="bfd77-173">L'utilizzo \_ di D3DSWAPEFFECT FLIPEX in Windows Vista o nelle versioni precedenti del sistema operativo restituirà FAIL da [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex).</span><span class="sxs-lookup"><span data-stu-id="bfd77-173">Using D3DSWAPEFFECT\_FLIPEX on Windows Vista or previous operating system versions will return fail from [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex).</span></span>

</dd> <dt>

<span data-ttu-id="bfd77-174">**SwapEffect**</span><span class="sxs-lookup"><span data-stu-id="bfd77-174">**SwapEffect**</span></span>
</dt> <dd>

<span data-ttu-id="bfd77-175">(Solo Windows 7)</span><span class="sxs-lookup"><span data-stu-id="bfd77-175">(Windows 7 Only)</span></span>

<span data-ttu-id="bfd77-176">Il nuovo \_ tipo di effetto catena di scambio FLIPEX di D3DSWAPEFFECT designa quando un'applicazione sta adottando la modalità di capovolgimento presente in DWM.</span><span class="sxs-lookup"><span data-stu-id="bfd77-176">The new D3DSWAPEFFECT\_FLIPEX swap chain effect type designates when an application is adopting Flip Mode Present to DWM.</span></span> <span data-ttu-id="bfd77-177">Consente all'applicazione un utilizzo più efficiente della memoria e della potenza e consente inoltre all'applicazione di sfruttare le statistiche presenti a schermo intero in modalità finestra.</span><span class="sxs-lookup"><span data-stu-id="bfd77-177">It allows the application more efficient usage of memory and power, and also enables the application to take advantage of full-screen present statistics in windowed mode.</span></span> <span data-ttu-id="bfd77-178">Il comportamento dell'applicazione a schermo intero non è interessato.</span><span class="sxs-lookup"><span data-stu-id="bfd77-178">Full-screen application behavior is not affected.</span></span> <span data-ttu-id="bfd77-179">Se Windowed è impostato su **true** e **SwapEffect** è impostato su D3DSWAPEFFECT \_ FLIPEX, il runtime crea un ulteriore buffer aggiuntivo e ruota a seconda di quale handle appartiene al buffer che diventa il buffer anteriore al momento della presentazione.</span><span class="sxs-lookup"><span data-stu-id="bfd77-179">If Windowed is set to **TRUE** and **SwapEffect** is set to D3DSWAPEFFECT\_FLIPEX, the runtime creates one extra back buffer and rotates whichever handle belongs to the buffer that becomes the front buffer at presentation time.</span></span>

</dd> <dt>

<span data-ttu-id="bfd77-180">**Flag**</span><span class="sxs-lookup"><span data-stu-id="bfd77-180">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="bfd77-181">(Solo Windows 7)</span><span class="sxs-lookup"><span data-stu-id="bfd77-181">(Windows 7 Only)</span></span>

<span data-ttu-id="bfd77-182">Non è possibile impostare il flag [ \_ \_ backBuffer bloccabile D3DPRESENTFLAG](/windows/desktop/direct3d9/d3dpresentflag) se **SwapEffect** è impostato sul nuovo tipo di effetto catena di scambio [**D3DSWAPEFFECT \_ FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) .</span><span class="sxs-lookup"><span data-stu-id="bfd77-182">The [D3DPRESENTFLAG\_LOCKABLE\_BACKBUFFER](/windows/desktop/direct3d9/d3dpresentflag) flag cannot be set if **SwapEffect** is set to the new [**D3DSWAPEFFECT\_FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) swap chain effect type.</span></span>

</dd> </dl>

### <a name="design-guidelines-for-direct3d-9ex-flip-model-applications"></a><span data-ttu-id="bfd77-183">Linee guida di progettazione per Direct3D 9Ex flip model Applications</span><span class="sxs-lookup"><span data-stu-id="bfd77-183">Design Guidelines for Direct3D 9Ex Flip Model Applications</span></span>

<span data-ttu-id="bfd77-184">Usare le linee guida riportate nelle sezioni riportate di seguito per progettare le applicazioni Direct3D 9Ex flip model.</span><span class="sxs-lookup"><span data-stu-id="bfd77-184">Use the guidelines in the following sections to design your Direct3D 9Ex Flip Model applications.</span></span>

### <a name="use-flip-mode-present-in-a-separate-hwnd-from-blt-mode-present"></a><span data-ttu-id="bfd77-185">Utilizzare la modalità Flip presente in un HWND separato dalla modalità BLT presente</span><span class="sxs-lookup"><span data-stu-id="bfd77-185">Use Flip Mode Present in a Separate HWND from Blt Mode Present</span></span>

<span data-ttu-id="bfd77-186">Le applicazioni devono utilizzare la modalità Flip 9Ex di Direct3D presente in un HWND che non è anche di destinazione di altre API, inclusa la modalità BLT che presenta 9Ex Direct3D, altre versioni di Direct3D o GDI.</span><span class="sxs-lookup"><span data-stu-id="bfd77-186">Applications should use Direct3D 9Ex Flip Mode Present in an HWND that is not also targeted by other APIs, including Blt Mode Present Direct3D 9Ex, other versions of Direct3D, or GDI.</span></span> <span data-ttu-id="bfd77-187">La modalità Flip presente può essere usata per presentare le finestre figlio; in altre condizioni, le applicazioni possono utilizzare Capovolgi modello quando non è misto al modello BLT nello stesso HWND, come illustrato nelle illustrazioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="bfd77-187">Flip Mode Present can be used to present to child windows; that is, applications can use Flip Model when it is not mixed with Blt Model in the same HWND, as shown in the following illustrations.</span></span>

![illustrazione della finestra padre Direct3D e di una finestra figlio GDI, ciascuna con il proprio HWND](images/parent-d3d.png)

![illustrazione della finestra padre GDI e di una finestra figlio Direct3D, ciascuna con il proprio HWND](images/parent-gdi.png)

<span data-ttu-id="bfd77-190">Poiché il modello BLT mantiene una copia aggiuntiva della superficie, è possibile aggiungere GDI e altri contenuti Direct3D allo stesso HWND tramite aggiornamenti a fasi da Direct3D e GDI.</span><span class="sxs-lookup"><span data-stu-id="bfd77-190">Because Blt Model maintains an additional copy of the surface, GDI and other Direct3D contents can be added to the same HWND through piecemeal updates from Direct3D and GDI.</span></span> <span data-ttu-id="bfd77-191">Utilizzando il modello Flip, solo il contenuto Direct3D 9Ex nelle catene di scambio [**D3DSWAPEFFECT \_ FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) passate a DWM sarà visibile.</span><span class="sxs-lookup"><span data-stu-id="bfd77-191">Using the Flip Model, only Direct3D 9Ex content in [**D3DSWAPEFFECT\_FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) swap chains that are passed to DWM will be visible.</span></span> <span data-ttu-id="bfd77-192">Tutti gli altri aggiornamenti del contenuto Direct3D o GDI del modello BLT verranno ignorati, come illustrato nelle illustrazioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="bfd77-192">All other Blt Model Direct3D or GDI content updates will be ignored, as shown in the following illustrations.</span></span>

![illustrazione del testo GDI che potrebbe non essere visualizzato se si utilizza il modello Flip e il contenuto Direct3D e GDI si trovano nello stesso HWND](images/d3d-gdi-same-hwnd.png)

![illustrazione del contenuto Direct3D e GDI in cui DWM è abilitato e l'applicazione è in modalità finestra](images/d3d-gdinotext-same-hwnd.png)

<span data-ttu-id="bfd77-195">Per questo motivo, è necessario abilitare il modello Flip per i buffer della catena di scambio, in cui il modello di 9Ex Flip solo per il rendering dell'intero HWND.</span><span class="sxs-lookup"><span data-stu-id="bfd77-195">Therefore, Flip Model should be enabled for swap chain buffers surfaces where the Direct3D 9Ex Flip Model alone renders to the entire HWND.</span></span>

### <a name="do-not-use-flip-model-with-gdis-scrollwindow-or-scrollwindowex"></a><span data-ttu-id="bfd77-196">Non usare Capovolgi modello con ScrollWindow o ScrollWindowEx di GDI</span><span class="sxs-lookup"><span data-stu-id="bfd77-196">Do Not Use Flip Model with GDI's ScrollWindow or ScrollWindowEx</span></span>

<span data-ttu-id="bfd77-197">Alcune applicazioni Direct3D 9Ex utilizzano le funzioni ScrollWindow o ScrollWindowEx di GDI per aggiornare il contenuto della finestra quando viene attivato un evento Scroll utente.</span><span class="sxs-lookup"><span data-stu-id="bfd77-197">Some Direct3D 9Ex applications use GDI's ScrollWindow or ScrollWindowEx functions to update window contents when a user scroll event is triggered.</span></span> <span data-ttu-id="bfd77-198">ScrollWindow e ScrollWindowEx eseguono BLTs del contenuto della finestra sullo schermo durante lo scorrimento di una finestra.</span><span class="sxs-lookup"><span data-stu-id="bfd77-198">ScrollWindow and ScrollWindowEx perform blts of window contents on screen as a window is scrolled.</span></span> <span data-ttu-id="bfd77-199">Queste funzioni richiedono anche aggiornamenti del modello BLT per il contenuto GDI e 9Ex di Direct3D.</span><span class="sxs-lookup"><span data-stu-id="bfd77-199">These functions also require Blt Model updates for GDI and Direct3D 9Ex content.</span></span> <span data-ttu-id="bfd77-200">Nelle applicazioni in cui viene utilizzata una delle due funzioni non verrà necessariamente visualizzato lo scorrimento del contenuto della finestra visibile sullo schermo quando l'applicazione è in modalità finestra e DWM è abilitato.</span><span class="sxs-lookup"><span data-stu-id="bfd77-200">Applications that use either function will not necessarily display visible window contents scrolling on screen when the application is in windowed mode and DWM is enabled.</span></span> <span data-ttu-id="bfd77-201">Si consiglia di non utilizzare le API ScrollWindow e ScrollWindowEx di GDI nelle applicazioni e di ricreare il contenuto sullo schermo in risposta allo scorrimento.</span><span class="sxs-lookup"><span data-stu-id="bfd77-201">We recommend that you not use GDI's ScrollWindow and ScrollWindowEx APIs in your applications, and instead redraw their contents on screen in response to scrolling.</span></span>

### <a name="use-one-d3dswapeffect_flipex-swap-chain-per-hwnd"></a><span data-ttu-id="bfd77-202">Usare una \_ catena di scambio FLIPEX di D3DSWAPEFFECT per HWND</span><span class="sxs-lookup"><span data-stu-id="bfd77-202">Use One D3DSWAPEFFECT\_FLIPEX Swap Chain per HWND</span></span>

<span data-ttu-id="bfd77-203">Le applicazioni che usano Capovolgi modello non devono usare più catene di scambio del modello Flip destinate allo stesso HWND.</span><span class="sxs-lookup"><span data-stu-id="bfd77-203">Applications that use Flip Model should not use multiple Flip Model swap chains targeting the same HWND.</span></span>

### <a name="frame-synchronization-of-direct3d-9ex-flip-model-applications"></a><span data-ttu-id="bfd77-204">Sincronizzazione dei frame delle applicazioni di modelli 9Ex Flip Direct3D</span><span class="sxs-lookup"><span data-stu-id="bfd77-204">Frame Synchronization of Direct3D 9Ex Flip Model Applications</span></span>

<span data-ttu-id="bfd77-205">Le statistiche attuali sono informazioni sulla tempistica dei frame utilizzate dalle applicazioni multimediali per sincronizzare flussi video e audio e per eseguire il ripristino da problemi di riproduzione video.</span><span class="sxs-lookup"><span data-stu-id="bfd77-205">Present statistics are frame timing information that media applications use to synchronize video and audio streams and recover from video playback glitches.</span></span> <span data-ttu-id="bfd77-206">Per abilitare la disponibilità delle statistiche, l'applicazione Direct3D 9Ex deve garantire che il parametro *BehaviorFlags* passato dall'applicazione a [**IDirect3D9Ex:: CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) contenga il flag di comportamento del dispositivo [D3DCREATE \_ enable \_ PRESENTSTATS](/windows/desktop/direct3d9/d3dcreate).</span><span class="sxs-lookup"><span data-stu-id="bfd77-206">To enable present statistics availability, the Direct3D 9Ex application must ensure that the *BehaviorFlags* parameter that the application passes to [**IDirect3D9Ex::CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) contains the device behavior flag [D3DCREATE\_ENABLE\_PRESENTSTATS](/windows/desktop/direct3d9/d3dcreate).</span></span>

<span data-ttu-id="bfd77-207">Per praticità, la sintassi di [**IDirect3D9Ex:: CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) è ripetuta qui.</span><span class="sxs-lookup"><span data-stu-id="bfd77-207">For convenience, the syntax of [**IDirect3D9Ex::CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) is repeated here.</span></span>

``` syntax
HRESULT CreateDeviceEx(
  UINT Adapter,
  D3DDEVTYPE DeviceType,
  HWND hFocusWindow,
  DWORD BehaviorFlags,
  D3DPRESENT_PARAMETERS* pPresentationParameters,
  D3DDISPLAYMODEEX *pFullscreenDisplayMode,
  IDirect3DDevice9Ex **ppReturnedDeviceInterface
);
```

<span data-ttu-id="bfd77-208">Il modello Direct3D 9Ex flip aggiunge il flag di presentazione di [D3DPRESENT \_ FORCEIMMEDIATE](/windows/desktop/direct3d9/d3dpresent) che impone il comportamento del flag di presentazione [ \_ \_ immediato dell'intervallo D3DPRESENT](/windows/desktop/direct3d9/d3dpresent) .</span><span class="sxs-lookup"><span data-stu-id="bfd77-208">Direct3D 9Ex Flip Model adds the [D3DPRESENT\_FORCEIMMEDIATE](/windows/desktop/direct3d9/d3dpresent) presentation flag that enforces the [D3DPRESENT\_INTERVAL\_IMMEDIATE](/windows/desktop/direct3d9/d3dpresent) presentation-flag behavior.</span></span> <span data-ttu-id="bfd77-209">L'applicazione Direct3D 9Ex specifica questi flag di presentazione nel parametro *dwFlags* che l'applicazione passa a [**IDirect3DDevice9Ex::P resentex**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex), come illustrato di seguito.</span><span class="sxs-lookup"><span data-stu-id="bfd77-209">The Direct3D 9Ex application specifies these presentation flags in the *dwFlags* parameter that the application passes to [**IDirect3DDevice9Ex::PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex), as shown here.</span></span>

``` syntax
HRESULT PresentEx(
  CONST RECT *pSourceRect,
  CONST RECT *pDestRect,
  HWND hDestWindowOverride,
  CONST RGNDATA *pDirtyRegion,
  DWORD dwFlags
);
```

<span data-ttu-id="bfd77-210">Quando si modifica l'applicazione Direct3D 9Ex per Windows 7, è necessario considerare le seguenti informazioni sui flag di presentazione di [D3DPRESENT](/windows/desktop/direct3d9/d3dpresent) specificati:</span><span class="sxs-lookup"><span data-stu-id="bfd77-210">When you modify your Direct3D 9Ex application for Windows 7, you should consider the following information about the specified [D3DPRESENT](/windows/desktop/direct3d9/d3dpresent) presentation flags:</span></span>

<dl> <dt>

[<span data-ttu-id="bfd77-211">\_DONOTFLIP D3DPRESENT</span><span class="sxs-lookup"><span data-stu-id="bfd77-211">D3DPRESENT\_DONOTFLIP</span></span>](/windows/desktop/direct3d9/d3dpresent)
</dt> <dd>

<span data-ttu-id="bfd77-212">Questo flag è disponibile solo in modalità schermo intero o</span><span class="sxs-lookup"><span data-stu-id="bfd77-212">This flag is available only in full-screen mode or</span></span>

<span data-ttu-id="bfd77-213">(Solo Windows 7)</span><span class="sxs-lookup"><span data-stu-id="bfd77-213">(Windows 7 Only)</span></span>

<span data-ttu-id="bfd77-214">Quando l'applicazione imposta il membro **SwapEffect** dei [**\_ parametri D3DPRESENT**](/windows/desktop/direct3d9/d3dpresent-parameters) su [**D3DSWAPEFFECT \_ FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) in una chiamata a [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex).</span><span class="sxs-lookup"><span data-stu-id="bfd77-214">when the application sets the **SwapEffect** member of [**D3DPRESENT\_PARAMETERS**](/windows/desktop/direct3d9/d3dpresent-parameters) to [**D3DSWAPEFFECT\_FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) in a call to [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex).</span></span>

</dd> <dt>

[<span data-ttu-id="bfd77-215">\_FORCEIMMEDIATE D3DPRESENT</span><span class="sxs-lookup"><span data-stu-id="bfd77-215">D3DPRESENT\_FORCEIMMEDIATE</span></span>](/windows/desktop/direct3d9/d3dpresent)
</dt> <dd>

<span data-ttu-id="bfd77-216">(Solo Windows 7)</span><span class="sxs-lookup"><span data-stu-id="bfd77-216">(Windows 7 Only)</span></span>

<span data-ttu-id="bfd77-217">Questo flag può essere specificato solo se l'applicazione imposta il membro **SwapEffect** dei [**\_ parametri D3DPRESENT**](/windows/desktop/direct3d9/d3dpresent-parameters) su [**D3DSWAPEFFECT \_ FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) in una chiamata a [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex).</span><span class="sxs-lookup"><span data-stu-id="bfd77-217">This flag can be specified only if the application sets the **SwapEffect** member of [**D3DPRESENT\_PARAMETERS**](/windows/desktop/direct3d9/d3dpresent-parameters) to [**D3DSWAPEFFECT\_FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) in a call to [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex).</span></span> <span data-ttu-id="bfd77-218">L'applicazione può utilizzare questo flag per aggiornare immediatamente una superficie con diversi frame in un secondo momento nella coda del presente DWM, ignorando essenzialmente i frame intermedi.</span><span class="sxs-lookup"><span data-stu-id="bfd77-218">The application can use this flag to immediately update a surface with several frames later in the DWM Present queue, essentially skipping intermediate frames.</span></span>

<span data-ttu-id="bfd77-219">Le applicazioni abilitate per FlipEx con finestra possono usare questo flag per aggiornare immediatamente una superficie con un frame che si trova in un secondo momento nella coda del presente DWM, ignorando i frame intermedi.</span><span class="sxs-lookup"><span data-stu-id="bfd77-219">Windowed FlipEx-enabled applications can use this flag to immediately update a surface with a frame that is later in the DWM Present queue, skipping intermediate frames.</span></span> <span data-ttu-id="bfd77-220">Questa operazione è particolarmente utile per le applicazioni multimediali che desiderano rimuovere i frame rilevati in ritardo e presentare i frame successivi al momento della composizione.</span><span class="sxs-lookup"><span data-stu-id="bfd77-220">This is especially useful for media applications that want to discard frames that have been detected as late and present subsequent frames at composition time.</span></span> <span data-ttu-id="bfd77-221">[**IDirect3DDevice9Ex::P resentex**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) restituisce un errore di parametro non valido se il flag non è specificato correttamente.</span><span class="sxs-lookup"><span data-stu-id="bfd77-221">[**IDirect3DDevice9Ex::PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) returns invalid parameter error if this flag is improperly specified.</span></span>

</dd> </dl>

<span data-ttu-id="bfd77-222">Per ottenere le informazioni sulle statistiche presenti, l'applicazione ottiene la struttura [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) chiamando l'API [**IDirect3DSwapChain9Ex:: GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="bfd77-222">To obtain present statistics information, the application obtains the [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) structure by calling the [**IDirect3DSwapChain9Ex::GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) API.</span></span>

<span data-ttu-id="bfd77-223">La struttura [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) contiene statistiche sulle chiamate [**IDirect3DDevice9Ex::P resentex**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) .</span><span class="sxs-lookup"><span data-stu-id="bfd77-223">The [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) structure contains statistics about [**IDirect3DDevice9Ex::PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) calls.</span></span> <span data-ttu-id="bfd77-224">Il dispositivo deve essere creato tramite una chiamata [**IDirect3D9Ex:: CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) con il flag [di \_ Abilitazione di \_ PRESENTSTATS D3DCREATE](/windows/desktop/direct3d9/d3dcreate) .</span><span class="sxs-lookup"><span data-stu-id="bfd77-224">The device must be created by using a [**IDirect3D9Ex::CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) call with the [D3DCREATE\_ENABLE\_PRESENTSTATS](/windows/desktop/direct3d9/d3dcreate) flag.</span></span> <span data-ttu-id="bfd77-225">In caso contrario, i dati restituiti da [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) non sono definiti.</span><span class="sxs-lookup"><span data-stu-id="bfd77-225">Otherwise, the data returned by [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) is undefined.</span></span> <span data-ttu-id="bfd77-226">Una catena di swap 9Ex Direct3D abilitata per il modello fornisce informazioni sulle statistiche presenti nelle modalità finestra e a schermo intero.</span><span class="sxs-lookup"><span data-stu-id="bfd77-226">A Flip-Model-enabled Direct3D 9Ex swap chain provides present statistics information in both windowed and full-screen modes.</span></span>

<span data-ttu-id="bfd77-227">Per le catene di scambio Direct3D 9Ex abilitate per il modello BLT in modalità finestra, tutti i valori della struttura [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) saranno zeri.</span><span class="sxs-lookup"><span data-stu-id="bfd77-227">For Blt-Model-enabled Direct3D 9Ex swap chains in windowed mode, all [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) structure values will be zeroes.</span></span>

<span data-ttu-id="bfd77-228">Per FlipEx present Statistics, [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) restituisce \_ D3DERR \_ le statistiche presenti \_ nelle situazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="bfd77-228">For FlipEx present statistics, [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) returns D3DERR\_PRESENT\_STATISTICS\_DISJOINT in the following situations:</span></span>

-   <span data-ttu-id="bfd77-229">Prima chiamata a [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) ever, che indica l'inizio di una sequenza</span><span class="sxs-lookup"><span data-stu-id="bfd77-229">First call to [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) ever, which indicates the beginning of a sequence</span></span>
-   <span data-ttu-id="bfd77-230">Transizione di DWM da on a off</span><span class="sxs-lookup"><span data-stu-id="bfd77-230">DWM transition from on to off</span></span>
-   <span data-ttu-id="bfd77-231">Modifica della modalità: in modalità finestra a o da schermo intero o a schermo intero a transizioni a schermo intero</span><span class="sxs-lookup"><span data-stu-id="bfd77-231">Mode change: either windowed mode to or from full screen or full screen to full screen transitions</span></span>

<span data-ttu-id="bfd77-232">Per praticità, la sintassi di [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) viene ripetuta qui.</span><span class="sxs-lookup"><span data-stu-id="bfd77-232">For convenience, the syntax of [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) is repeated here.</span></span>

``` syntax
HRESULT GetPresentStatistics(
  D3DPRESENTSTATS * pPresentationStatistics
);
```

<span data-ttu-id="bfd77-233">Il metodo [**IDirect3DSwapChain9Ex:: GetLastPresentCount**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount) restituisce l'ultimo PresentCount, ovvero l'ID attuale dell'ultima chiamata a present riuscita effettuata da un dispositivo di visualizzazione associato alla catena di scambio.</span><span class="sxs-lookup"><span data-stu-id="bfd77-233">The [**IDirect3DSwapChain9Ex::GetLastPresentCount**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount) method returns the last PresentCount, that is, the Present ID of the last successful Present call that was made by a display device that is associated with the swap chain.</span></span> <span data-ttu-id="bfd77-234">Questo ID presenta il valore del membro **PresentCount** della struttura [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) .</span><span class="sxs-lookup"><span data-stu-id="bfd77-234">This Present ID is the value of the **PresentCount** member of the [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) structure.</span></span> <span data-ttu-id="bfd77-235">Per le catene di scambio Direct3D 9Ex abilitate per il modello, in modalità finestra, tutti i valori della struttura **D3DPRESENTSTATS** saranno zeri.</span><span class="sxs-lookup"><span data-stu-id="bfd77-235">For Blt-Model-enabled Direct3D 9Ex swap chains, while in windowed mode, all **D3DPRESENTSTATS** structure values will be zeroes.</span></span>

<span data-ttu-id="bfd77-236">Per praticità, la sintassi di [**IDirect3DSwapChain9Ex:: GetLastPresentCount**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount) è ripetuta qui.</span><span class="sxs-lookup"><span data-stu-id="bfd77-236">For convenience, the syntax of [**IDirect3DSwapChain9Ex::GetLastPresentCount**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount) is repeated here.</span></span>

``` syntax
HRESULT GetLastPresentCount(
  UINT * pLastPresentCount
);
```

<span data-ttu-id="bfd77-237">Quando si modifica l'applicazione Direct3D 9Ex per Windows 7, è necessario considerare le informazioni seguenti sulla struttura [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) :</span><span class="sxs-lookup"><span data-stu-id="bfd77-237">When you modify your Direct3D 9Ex application for Windows 7, you should consider the following information about the [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) structure:</span></span>

-   <span data-ttu-id="bfd77-238">Il valore di PresentCount restituito da [**GetLastPresentCount**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount) non viene aggiornato quando una chiamata [**PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) con D3DPRESENT \_ DONOTWAIT specificato nel parametro *dwFlags* restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="bfd77-238">The PresentCount value that [**GetLastPresentCount**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount) returns does not update when a [**PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) call with D3DPRESENT\_DONOTWAIT specified in the *dwFlags* parameter returns failure.</span></span>
-   <span data-ttu-id="bfd77-239">Quando [**PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) viene chiamato con D3DPRESENT \_ DONOTFLIP, una chiamata [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) ha esito positivo ma non restituisce una struttura [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) aggiornata quando l'applicazione è in modalità finestra.</span><span class="sxs-lookup"><span data-stu-id="bfd77-239">When [**PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) is called with D3DPRESENT\_DONOTFLIP, a [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) call succeeds but does not return an updated [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) structure when the application is in windowed mode.</span></span>
-   <span data-ttu-id="bfd77-240">**PresentRefreshCount** rispetto a **SyncRefreshCount** in [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats):</span><span class="sxs-lookup"><span data-stu-id="bfd77-240">**PresentRefreshCount** versus **SyncRefreshCount** in [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats):</span></span>
    -   <span data-ttu-id="bfd77-241">**PresentRefreshCount** è uguale a **SyncRefreshCount** quando l'applicazione presenta ogni vsync.</span><span class="sxs-lookup"><span data-stu-id="bfd77-241">**PresentRefreshCount** is equal to **SyncRefreshCount** when the application presents on every vsync.</span></span>
    -   <span data-ttu-id="bfd77-242">**SyncRefreshCount** viene ottenuto nell'intervallo vsync quando è stato inviato il presente, **SyncQPCTime** è approssimativamente il tempo associato all'intervallo vsync.</span><span class="sxs-lookup"><span data-stu-id="bfd77-242">**SyncRefreshCount** is obtained on the vsync interval when the present was submitted, **SyncQPCTime** is approximately the time associated with the vsync interval.</span></span>

``` syntax
typedef struct _D3DPRESENTSTATS {
    UINT PresentCount;
    UINT PresentRefreshCount;
    UINT SyncRefreshCount;
    LARGE_INTEGER SyncQPCTime;
    LARGE_INTEGER SyncGPUTime;
} D3DPRESENTSTATS;
```

### <a name="frame-synchronization-for-windowed-applications-when-dwm-is-off"></a><span data-ttu-id="bfd77-243">Sincronizzazione dei frame per le applicazioni con finestra quando DWM è disattivato</span><span class="sxs-lookup"><span data-stu-id="bfd77-243">Frame Synchronization for Windowed Applications When DWM is Off</span></span>

<span data-ttu-id="bfd77-244">Quando DWM è disattivato, le applicazioni finestra vengono visualizzate direttamente nella schermata di monitoraggio senza passare attraverso una catena di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="bfd77-244">When DWM is off, windowed applications display directly to the monitor screen without going through a flip chain.</span></span> <span data-ttu-id="bfd77-245">In Windows Vista non è disponibile alcun supporto per ottenere informazioni sulle statistiche dei frame per le applicazioni con finestra quando DWM è disattivato.</span><span class="sxs-lookup"><span data-stu-id="bfd77-245">In Windows Vista, there is no support for obtaining frame statistics information for windowed applications when DWM is off.</span></span> <span data-ttu-id="bfd77-246">Per mantenere un'API in cui le applicazioni non devono essere compatibili con DWM, Windows 7 restituirà le informazioni sulle statistiche dei frame per le applicazioni con finestra quando DWM è disattivato.</span><span class="sxs-lookup"><span data-stu-id="bfd77-246">To maintain an API where applications need not be DWM- aware, Windows 7 will return frame statistics information for windowed applications when DWM is off.</span></span> <span data-ttu-id="bfd77-247">Le statistiche dei frame restituite quando DWM è disattivato sono solo stime.</span><span class="sxs-lookup"><span data-stu-id="bfd77-247">The frame statistics returned when DWM is off are estimations only.</span></span>

## <a name="walk-through-of-a-direct3d-9ex-flip-model-and-present-statistics-sample"></a><span data-ttu-id="bfd77-248">Walk-Through di un esempio Direct3D 9Ex flip model e present Statistics</span><span class="sxs-lookup"><span data-stu-id="bfd77-248">Walk-Through of a Direct3D 9Ex Flip Model and Present Statistics Sample</span></span>

<span data-ttu-id="bfd77-249">**Per acconsentire esplicitamente all'esempio FlipEx Presentation for Direct3D 9Ex**</span><span class="sxs-lookup"><span data-stu-id="bfd77-249">**To opt into FlipEx presentation for Direct3D 9Ex sample**</span></span>

1.  <span data-ttu-id="bfd77-250">Verificare che l'applicazione di esempio sia in esecuzione in Windows 7 o versione successiva del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="bfd77-250">Ensure the sample application is running on Windows 7 or later operating system version.</span></span>
2.  <span data-ttu-id="bfd77-251">Impostare il membro **SwapEffect** dei [**\_ parametri D3DPRESENT**](/windows/desktop/direct3d9/d3dpresent-parameters) su [**D3DSWAPEFFECT \_ FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) in una chiamata a [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex).</span><span class="sxs-lookup"><span data-stu-id="bfd77-251">Set the **SwapEffect** member of [**D3DPRESENT\_PARAMETERS**](/windows/desktop/direct3d9/d3dpresent-parameters) to [**D3DSWAPEFFECT\_FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) in a call to [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex).</span></span>


```C++
    OSVERSIONINFO version;
    ZeroMemory(&version, sizeof(version));
    version.dwOSVersionInfoSize = sizeof(version);
    GetVersionEx(&version);
    
    // Sample would run only on Win7 or higher
    // Flip Model present and its associated present statistics behavior are only available on Windows 7 or higher operating system
    bool bIsWin7 = (version.dwMajorVersion > 6) || 
        ((version.dwMajorVersion == 6) && (version.dwMinorVersion >= 1));

    if (!bIsWin7)
    {
        MessageBox(NULL, L"This sample requires Windows 7 or higher", NULL, MB_OK);
        return 0;
    }
```



<span data-ttu-id="bfd77-252">**Per acconsentire esplicitamente all'esempio FlipEx Associated present Statistics for Direct3D 9Ex**</span><span class="sxs-lookup"><span data-stu-id="bfd77-252">**To also opt into FlipEx associated Present Statistics for Direct3D 9Ex sample**</span></span>

-   <span data-ttu-id="bfd77-253">Impostare [D3DCREATE \_ enable \_ PRESENTSTATS](/windows/desktop/direct3d9/d3dcreate) nel parametro *BehaviorFlags* di [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex).</span><span class="sxs-lookup"><span data-stu-id="bfd77-253">Set [D3DCREATE\_ENABLE\_PRESENTSTATS](/windows/desktop/direct3d9/d3dcreate) in the *BehaviorFlags* parameter of [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex).</span></span>


```C++
    // Set up the structure used to create the D3DDevice
    D3DPRESENT_PARAMETERS d3dpp;
    ZeroMemory(&d3dpp, sizeof(d3dpp));

    d3dpp.Windowed = TRUE;
    d3dpp.SwapEffect = D3DSWAPEFFECT_FLIPEX;        // Opts into Flip Model present for D3D9Ex swapchain
    d3dpp.BackBufferFormat = D3DFMT_X8R8G8B8;
    d3dpp.BackBufferWidth = 256;                
    d3dpp.BackBufferHeight = 256;
    d3dpp.BackBufferCount = QUEUE_SIZE;
    d3dpp.PresentationInterval = D3DPRESENT_INTERVAL_ONE;

    g_iWidth = d3dpp.BackBufferWidth;
    g_iHeight = d3dpp.BackBufferHeight;

    // Create the D3DDevice with present statistics enabled - set D3DCREATE_ENABLE_PRESENTSTATS for behaviorFlags parameter
    if(FAILED(g_pD3D->CreateDeviceEx(D3DADAPTER_DEFAULT, D3DDEVTYPE_HAL, hWnd,
                                      D3DCREATE_HARDWARE_VERTEXPROCESSING | D3DCREATE_ENABLE_PRESENTSTATS,
                                      &d3dpp, NULL, &g_pd3dDevice)))
    {
        return E_FAIL;
    }
```



<span data-ttu-id="bfd77-254">**Per evitare, rilevare e ripristinare le anomalie**</span><span class="sxs-lookup"><span data-stu-id="bfd77-254">**To avoid, detect and recover from glitches**</span></span>

1.  <span data-ttu-id="bfd77-255">Chiamate di coda presenti: il numero consigliato di backBuffer è compreso tra 2 e 4.</span><span class="sxs-lookup"><span data-stu-id="bfd77-255">Queue Present calls: recommended backbuffer count is from 2 to 4.</span></span>
2.  <span data-ttu-id="bfd77-256">L'esempio Direct3D 9Ex aggiunge un backBuffer implicito. la lunghezza effettiva della coda attuale è il conteggio delle sottobuffer + 1.</span><span class="sxs-lookup"><span data-stu-id="bfd77-256">Direct3D 9Ex sample adds an implicit backbuffer, actual Present queue length is backbuffer count + 1.</span></span>
3.  <span data-ttu-id="bfd77-257">Creare una struttura di coda presente nell'helper per archiviare tutti gli ID presenti (PresentCount) e i PresentRefreshCount associati, calcolati/previsti.</span><span class="sxs-lookup"><span data-stu-id="bfd77-257">Create helper Present queue structure to store all successfully submitted Present's Present ID (PresentCount) and associated, calculated/expected PresentRefreshCount.</span></span>
4.  <span data-ttu-id="bfd77-258">Per rilevare l'occorrenza glitch:</span><span class="sxs-lookup"><span data-stu-id="bfd77-258">To detect glitch occurrence:</span></span>

    -   <span data-ttu-id="bfd77-259">Chiamare [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="bfd77-259">Call [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)).</span></span>
    -   <span data-ttu-id="bfd77-260">Ottenere l'ID attuale (PresentCount) e il numero di VSync in cui viene visualizzato il frame (PresentRefreshCount) del fotogramma con le statistiche attuali ottenute.</span><span class="sxs-lookup"><span data-stu-id="bfd77-260">Get the Present ID (PresentCount) and vsync count where the frame is shown (PresentRefreshCount) of the frame whose present statistics is obtained.</span></span>
    -   <span data-ttu-id="bfd77-261">Recuperare il PresentRefreshCount previsto (TargetRefresh nel codice di esempio) associato all'ID presente.</span><span class="sxs-lookup"><span data-stu-id="bfd77-261">Retrieve the expected PresentRefreshCount (TargetRefresh in sample code) associated with the Present ID.</span></span>
    -   <span data-ttu-id="bfd77-262">Se il valore di PresentRefreshCount effettivo è successivo al previsto, si è verificato un problema.</span><span class="sxs-lookup"><span data-stu-id="bfd77-262">If actual PresentRefreshCount is later than expected, a glitch has occurred.</span></span>

5.  <span data-ttu-id="bfd77-263">Per risolvere il problema:</span><span class="sxs-lookup"><span data-stu-id="bfd77-263">To recover from glitch:</span></span>

    -   <span data-ttu-id="bfd77-264">Calcolare il numero di frame da ignorare ( \_ variabile g iImmediates nel codice di esempio).</span><span class="sxs-lookup"><span data-stu-id="bfd77-264">Calculate how many frames to skip (g\_ iImmediates variable in sample code).</span></span>
    -   <span data-ttu-id="bfd77-265">Presentare i frame ignorati con intervallo D3DPRESENT \_ FORCEIMMEDIATE.</span><span class="sxs-lookup"><span data-stu-id="bfd77-265">Present the skipped frames with interval D3DPRESENT\_FORCEIMMEDIATE.</span></span>

<span data-ttu-id="bfd77-266">**Considerazioni per il rilevamento e il ripristino di problemi**</span><span class="sxs-lookup"><span data-stu-id="bfd77-266">**Considerations for glitch detection and recovery**</span></span>

1.  <span data-ttu-id="bfd77-267">Il recupero glitch accetta N ( \_ variabile iQueueDelay nel codice di esempio) numero di chiamate presenti in cui N (g \_ iQueueDelay) è uguale \_ a g iImmediates più la lunghezza della coda corrente, ovvero:</span><span class="sxs-lookup"><span data-stu-id="bfd77-267">Glitch recovery takes N (g\_iQueueDelay variable in sample code) number of Present calls where N (g\_iQueueDelay) equals g\_iImmediates plus length of the Present queue, that is:</span></span>

    -   <span data-ttu-id="bfd77-268">I frame ignorati con l'intervallo presente D3DPRESENT \_ FORCEIMMEDIATE, più</span><span class="sxs-lookup"><span data-stu-id="bfd77-268">Skipping frames with Present interval D3DPRESENT\_FORCEIMMEDIATE, plus</span></span>
    -   <span data-ttu-id="bfd77-269">Present in coda che devono essere elaborati</span><span class="sxs-lookup"><span data-stu-id="bfd77-269">Queued Presents that need to be processed</span></span>

2.  <span data-ttu-id="bfd77-270">Impostare un limite per la lunghezza del glitch ( \_ limite di recupero glitch \_ nell'esempio).</span><span class="sxs-lookup"><span data-stu-id="bfd77-270">Set a limit to the glitch length (GLITCH\_RECOVERY\_LIMIT in sample).</span></span> <span data-ttu-id="bfd77-271">Se l'applicazione di esempio non è in grado di eseguire il ripristino da un problema troppo lungo (ad esempio, 1 secondo o 60 vsyncs su 60Hz monitor), passare all'animazione intermittente e reimpostare la coda Helper presente.</span><span class="sxs-lookup"><span data-stu-id="bfd77-271">If the sample application cannot recover from a glitch that is too long (that is say, 1 second, or 60 vsyncs on 60Hz monitor), jump over the intermittent animation and reset the Present helper queue.</span></span>


```C++
VOID Render()
{
    g_pd3dDevice->Clear(0, NULL, D3DCLEAR_TARGET, D3DCOLOR_XRGB(0, 0, 0), 1.0f, 0);

    g_pd3dDevice->BeginScene();

    // Compute new animation parameters for time and frame based animations

    // Time-based is a difference between base and current SyncRefreshCount
    g_aTimeBasedHistory[g_iBlurHistoryCounter] = g_iStartFrame + g_LastSyncRefreshCount - g_SyncRefreshCount;
    // Frame-based is incrementing frame value
    g_aFrameBasedHistory[g_iBlurHistoryCounter] = g_iStartFrame + g_iFrameNumber;

    RenderBlurredMesh(TRUE);    // Time-based
    RenderBlurredMesh(FALSE);   // Frame-based

    g_iBlurHistoryCounter = (g_iBlurHistoryCounter + 1) % BLUR_FRAMES;

    DrawText();

    g_pd3dDevice->EndScene();

    // Performs glitch recovery if glitch was detected
    if (g_bGlitchRecovery && (g_iImmediates > 0))
    {
        // If we have present immediates queued as a result of glitch detected, issue forceimmediate Presents for glitch recovery 
        g_pd3dDevice->PresentEx(NULL, NULL, NULL, NULL, D3DPRESENT_FORCEIMMEDIATE);
        g_iImmediates--;
        g_iShowingGlitchRecovery = MESSAGE_SHOW;
    }
    // Otherwise, Present normally
    else
    {
        g_pd3dDevice->PresentEx(NULL, NULL, NULL, NULL, 0);
    }

    // Add to helper Present queue: PresentID + expected present refresh count of last submitted Present
    UINT PresentCount;
    g_pd3dSwapChain->GetLastPresentCount(&PresentCount);
    g_Queue.QueueFrame(PresentCount, g_TargetRefreshCount);
    
    // QueueDelay specifies # Present calls to be processed before another glitch recovery attempt
    if (g_iQueueDelay > 0)
    {
        g_iQueueDelay--;
    }

    if (g_bGlitchRecovery)
    {
        // Additional DONOTFLIP presents for frame conversions, which basically follows the same logic, but without rendering
        for (DWORD i = 0; i < g_iDoNotFlipNum; i++)
        {
            if (g_TargetRefreshCount != -1)
            {
                g_TargetRefreshCount++;
                g_iFrameNumber++;
                g_aTimeBasedHistory[g_iBlurHistoryCounter] = g_iStartFrame + g_LastSyncRefreshCount - g_SyncRefreshCount;
                g_aFrameBasedHistory[g_iBlurHistoryCounter] = g_iStartFrame + g_iFrameNumber;
                g_iBlurHistoryCounter = (g_iBlurHistoryCounter + 1) % BLUR_FRAMES;
            }
            
            if (g_iImmediates > 0)
            {
                g_pd3dDevice->PresentEx(NULL, NULL, NULL, NULL, D3DPRESENT_FORCEIMMEDIATE | D3DPRESENT_DONOTFLIP);
                g_iImmediates--;
            }
            else
            {
                g_pd3dDevice->PresentEx(NULL, NULL, NULL, NULL, D3DPRESENT_DONOTFLIP);
            }
            UINT PresentCount;
            g_pd3dSwapChain->GetLastPresentCount(&PresentCount);
            g_Queue.QueueFrame(PresentCount, g_TargetRefreshCount);

            if (g_iQueueDelay > 0)
            {
                g_iQueueDelay--;
            }
        }
    }

    // Check Present Stats info for glitch detection 
    D3DPRESENTSTATS PresentStats;

    // Obtain present statistics information for successfully displayed presents
    HRESULT hr = g_pd3dSwapChain->GetPresentStats(&PresentStats);

    if (SUCCEEDED(hr))
    {
        // Time-based update
        g_LastSyncRefreshCount = PresentStats.SyncRefreshCount;
        if ((g_SyncRefreshCount == -1) && (PresentStats.PresentCount != 0))
        {
            // First time SyncRefreshCount is reported, use it as base
            g_SyncRefreshCount = PresentStats.SyncRefreshCount;
        }

        // Fetch frame from the queue...
        UINT TargetRefresh = g_Queue.DequeueFrame(PresentStats.PresentCount);

        // If PresentStats returned a really old frame that we no longer have in the queue, just don't do any glitch detection
        if (TargetRefresh == FRAME_NOT_FOUND)
            return;

        if (g_TargetRefreshCount == -1)
        {
            // This is first time issued frame is confirmed by present stats, so fill target refresh count for all frames in the queue
            g_TargetRefreshCount = g_Queue.FillRefreshCounts(PresentStats.PresentCount, g_SyncRefreshCount);
        } 
        else
        {
            g_TargetRefreshCount++;
            g_iFrameNumber++;

            // To determine whether we're glitching, see if our estimated refresh count is confirmed
            // if the frame is displayed later than the expected vsync count
            if (TargetRefresh < PresentStats.PresentRefreshCount)
            {
                // then, glitch is detected!

                // If glitch is too big, don't bother recovering from it, just jump animation
                if ((PresentStats.PresentRefreshCount - TargetRefresh) > GLITCH_RECOVERY_LIMIT)
                {
                    g_iStartFrame += PresentStats.SyncRefreshCount - g_SyncRefreshCount;
                    ResetAnimation();
                    if (g_bGlitchRecovery)
                        g_iGlitchesInaRow++;    
                } 
                // Otherwise, compute number of immediate presents to recover from it -- if we?re not still trying to recover from another glitch
                else if (g_iQueueDelay == 0)
                {
                      // skip frames to catch up to expected refresh count
                    g_iImmediates = PresentStats.PresentRefreshCount - TargetRefresh;
                    // QueueDelay specifies # Present calls before another glitch recovery 
                    g_iQueueDelay = g_iImmediates + QUEUE_SIZE;
                    if (g_bGlitchRecovery)
                        g_iGlitchesInaRow++;
                }
            }
            else
            {
                // No glitch, reset glitch count
                g_iGlitchesInaRow = 0;
            }
        }
    }
    else if (hr == D3DERR_PRESENT_STATISTICS_DISJOINT)
    {
        // D3DERR_PRESENT_STATISTICS_DISJOINT means measurements should be started from the scratch (could be caused by mode change or DWM on/off transition)
        ResetAnimation();
    }

    // If we got too many glitches in a row, reduce framerate conversion factor (that is, render less frames)
    if (g_iGlitchesInaRow == FRAMECONVERSION_GLITCH_LIMIT)
    {
        if (g_iDoNotFlipNum < FRAMECONVERSION_LIMIT)
        {
            g_iDoNotFlipNum++;
        }
        g_iGlitchesInaRow = 0;
        g_iShowingDoNotFlipBump = MESSAGE_SHOW;
    }
}
```



<span data-ttu-id="bfd77-272">**Scenario di esempio**</span><span class="sxs-lookup"><span data-stu-id="bfd77-272">**Sample scenario**</span></span>

-   <span data-ttu-id="bfd77-273">Nell'illustrazione seguente viene mostrata un'applicazione con conteggio del buffer di 4.</span><span class="sxs-lookup"><span data-stu-id="bfd77-273">The following illustration shows an application with backbuffer count of 4.</span></span> <span data-ttu-id="bfd77-274">La lunghezza effettiva della coda attuale è pertanto 5.</span><span class="sxs-lookup"><span data-stu-id="bfd77-274">The actual Present queue length is therefore 5.</span></span>

    ![illustrazione di un frame sottoposto a rendering applicas e della coda presente](images/sample-scenario.png)

    <span data-ttu-id="bfd77-276">Il frame A è destinato a andare sullo schermo sul numero di intervalli di sincronizzazione 1 ma è stato rilevato che è stato visualizzato sul numero di intervalli di sincronizzazione pari a 4.</span><span class="sxs-lookup"><span data-stu-id="bfd77-276">Frame A is targeted to go on screen on sync interval count of 1 but was detected that it was shown on sync interval count of 4.</span></span> <span data-ttu-id="bfd77-277">Si è quindi verificato un problema.</span><span class="sxs-lookup"><span data-stu-id="bfd77-277">Therefore a glitch has occurred.</span></span> <span data-ttu-id="bfd77-278">I 3 frame successivi vengono presentati con l'intervallo di D3DPRESENT \_ \_ FORCEIMMEDIATE.</span><span class="sxs-lookup"><span data-stu-id="bfd77-278">Subsequent 3 frames are presented with D3DPRESENT\_INTERVAL\_FORCEIMMEDIATE.</span></span> <span data-ttu-id="bfd77-279">Il glitch dovrebbe richiedere un totale di 8 chiamate presenti prima del ripristino. il frame successivo verrà visualizzato in base al numero di intervalli di sincronizzazione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="bfd77-279">The glitch should take a total of 8 Present calls before it is recovered - the next frame will be shown as per its targeted sync interval count.</span></span>

### <a name="summary-of-programming-recommendations-for-frame-synchronization"></a><span data-ttu-id="bfd77-280">Riepilogo dei consigli di programmazione per la sincronizzazione dei frame</span><span class="sxs-lookup"><span data-stu-id="bfd77-280">Summary of Programming Recommendations for Frame Synchronization</span></span>

-   <span data-ttu-id="bfd77-281">Creare un elenco di backup di tutti gli ID LastPresentCount (ottenuti tramite [**GetLastPresentCount**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount)) e i PresentRefreshCount stimati associati di tutti i presentamenti inviati.</span><span class="sxs-lookup"><span data-stu-id="bfd77-281">Create a backup list of all the LastPresentCount IDs (obtained via [**GetLastPresentCount**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount)) and associated estimated PresentRefreshCount of all the Presents submitted.</span></span>
    > [!Note]  
    > <span data-ttu-id="bfd77-282">Quando l'applicazione chiama [**PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) con D3DPRESENT \_ DONOTFLIP, la chiamata [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) ha esito positivo ma non restituisce una struttura [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) aggiornata quando l'applicazione è in modalità finestra.</span><span class="sxs-lookup"><span data-stu-id="bfd77-282">When the application calls [**PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) with D3DPRESENT\_DONOTFLIP, the [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) call succeeds but does not return an updated [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) structure when the application is in windowed mode.</span></span>

     

-   <span data-ttu-id="bfd77-283">Chiamare [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) per ottenere il PresentRefreshCount effettivo associato a ogni ID presente dei frame visualizzati, per assicurarsi che l'applicazione gestisca gli errori restituiti dalla chiamata.</span><span class="sxs-lookup"><span data-stu-id="bfd77-283">Call [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) to obtain the actual PresentRefreshCount associated with each Present ID of frames shown, to make sure that the application handles failure returns from the call.</span></span>
-   <span data-ttu-id="bfd77-284">Se il valore di PresentRefreshCount effettivo è successivo al valore di PresentRefreshCount stimato, viene rilevato un problema.</span><span class="sxs-lookup"><span data-stu-id="bfd77-284">If actual PresentRefreshCount is later than estimated PresentRefreshCount, a glitch is detected.</span></span> <span data-ttu-id="bfd77-285">Compensare inviando frame in ritardo ' presenti con D3DPRESENT \_ FORCEIMMEDIATE.</span><span class="sxs-lookup"><span data-stu-id="bfd77-285">Compensate by submitting lagging frames' Present with D3DPRESENT\_FORCEIMMEDIATE.</span></span>
-   <span data-ttu-id="bfd77-286">Quando un frame viene presentato in ritardo nella coda corrente, tutti i frame successivi in coda saranno presentati in ritardo.</span><span class="sxs-lookup"><span data-stu-id="bfd77-286">When one frame is presented late in the Present queue, all subsequent queued frames will be presented late.</span></span> <span data-ttu-id="bfd77-287">D3DPRESENT \_ FORCEIMMEDIATE correggerà solo il frame successivo che verrà visualizzato dopo tutti i frame in coda.</span><span class="sxs-lookup"><span data-stu-id="bfd77-287">D3DPRESENT\_FORCEIMMEDIATE will correct only the next frame to be presented after all the queued frames.</span></span> <span data-ttu-id="bfd77-288">Pertanto, il conteggio della coda o del buffer non deve essere troppo lungo, quindi è possibile che si verifichino problemi di frame minori.</span><span class="sxs-lookup"><span data-stu-id="bfd77-288">Therefore, the Present queue or backbuffer count should not be too long -- so there are less frame glitches to catch up with.</span></span> <span data-ttu-id="bfd77-289">Il numero di backBuffer ottimale è da 2 a 4.</span><span class="sxs-lookup"><span data-stu-id="bfd77-289">The optimal backbuffer count is 2 to 4.</span></span>
-   <span data-ttu-id="bfd77-290">Se il valore di PresentRefreshCount stimato è successivo al valore effettivo di PresentRefreshCount, potrebbe essersi verificata la limitazione di DWM.</span><span class="sxs-lookup"><span data-stu-id="bfd77-290">If estimated PresentRefreshCount is later than the actual PresentRefreshCount, DWM throttling might have occurred.</span></span> <span data-ttu-id="bfd77-291">Sono possibili le soluzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="bfd77-291">The following solutions are possible:</span></span>

    -   <span data-ttu-id="bfd77-292">riduzione della lunghezza della coda presente</span><span class="sxs-lookup"><span data-stu-id="bfd77-292">reducing Present queue length</span></span>
    -   <span data-ttu-id="bfd77-293">riduzione dei requisiti di memoria della GPU con qualsiasi altro mezzo, oltre a ridurre la lunghezza della coda presente (ovvero, diminuire la qualità, rimuovere gli effetti e così via)</span><span class="sxs-lookup"><span data-stu-id="bfd77-293">reducing GPU memory requirements with any other means besides reducing Present Queue length (that is, decreasing quality, removing effects, and so on)</span></span>
    -   <span data-ttu-id="bfd77-294">specifica di [**DwmEnableMMCSS**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmenablemmcss) per impedire la limitazione di DWM in generale</span><span class="sxs-lookup"><span data-stu-id="bfd77-294">specifying [**DwmEnableMMCSS**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmenablemmcss) to prevent DWM throttling in general</span></span>

-   <span data-ttu-id="bfd77-295">Verificare le prestazioni delle funzionalità di visualizzazione delle applicazioni e delle statistiche dei frame negli scenari seguenti:</span><span class="sxs-lookup"><span data-stu-id="bfd77-295">Verify application display functionality and frame statistics performance in the following scenarios:</span></span>

    -   <span data-ttu-id="bfd77-296">con DWM acceso e disattivato</span><span class="sxs-lookup"><span data-stu-id="bfd77-296">with DWM on and off</span></span>
    -   <span data-ttu-id="bfd77-297">modalità esclusive e con finestra a schermo intero</span><span class="sxs-lookup"><span data-stu-id="bfd77-297">fullscreen exclusive and windowed modes</span></span>
    -   <span data-ttu-id="bfd77-298">hardware con funzionalità più bassa</span><span class="sxs-lookup"><span data-stu-id="bfd77-298">lower capability hardware</span></span>

-   <span data-ttu-id="bfd77-299">Quando le applicazioni non possono eseguire il ripristino da un numero elevato di frame glitch con D3DPRESENT \_ FORCEIMMEDIATE presenti, possono eseguire potenzialmente le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="bfd77-299">When applications cannot recover from large numbers of glitched frames with D3DPRESENT\_FORCEIMMEDIATE Present, they can potentially perform the following operations:</span></span>

    -   <span data-ttu-id="bfd77-300">ridurre l'utilizzo della CPU e della GPU eseguendo il rendering con minor carico di lavoro.</span><span class="sxs-lookup"><span data-stu-id="bfd77-300">reduce CPU and GPU usage by rendering with less workload.</span></span>
    -   <span data-ttu-id="bfd77-301">nel caso di decodifica video, decodifica più velocemente riducendo la qualità e, pertanto, l'utilizzo della CPU e della GPU.</span><span class="sxs-lookup"><span data-stu-id="bfd77-301">in the case of video decode, decode faster by reducing quality and, therefore, CPU and GPU usage.</span></span>

## <a name="conclusion-about-direct3d-9ex-improvements"></a><span data-ttu-id="bfd77-302">Conclusione dei miglioramenti di Direct3D 9Ex</span><span class="sxs-lookup"><span data-stu-id="bfd77-302">Conclusion about Direct3D 9Ex Improvements</span></span>

<span data-ttu-id="bfd77-303">In Windows 7, le applicazioni che visualizzano la frequenza dei fotogrammi video o misuratore durante la presentazione possono scegliere di capovolgere il modello.</span><span class="sxs-lookup"><span data-stu-id="bfd77-303">On Windows 7, applications that display video or gauge frame rate during presentation can opt into Flip Model.</span></span> <span data-ttu-id="bfd77-304">I miglioramenti attuali delle statistiche associati a flip model Direct3D 9Ex possono trarre vantaggio dalle applicazioni che sincronizzano la presentazione per frequenza dei fotogrammi, con feedback in tempo reale per il rilevamento e il recupero di problemi.</span><span class="sxs-lookup"><span data-stu-id="bfd77-304">The present statistics improvements that are associated with Flip Model Direct3D 9Ex can benefit applications that synchronize presentation per frame rate, with real time feedback for glitch detection and recovery.</span></span> <span data-ttu-id="bfd77-305">Gli sviluppatori che adottano il modello Direct3D 9Ex Flip devono considerare come destinazione un HWND separato dal contenuto GDI e dalla sincronizzazione della frequenza dei fotogrammi.</span><span class="sxs-lookup"><span data-stu-id="bfd77-305">Developers that adopt the Direct3D 9Ex Flip Model should take targeting a separate HWND from GDI content and frame rate synchronization into account.</span></span> <span data-ttu-id="bfd77-306">Vedere i dettagli in questo argomento e la documentazione MSDN.</span><span class="sxs-lookup"><span data-stu-id="bfd77-306">Refer to details in this topic, and MSDN documentation.</span></span> <span data-ttu-id="bfd77-307">Per ulteriori informazioni, vedere la pagina relativa [al centro per sviluppatori DirectX su MSDN](/previous-versions/windows/apps/hh452744(v=win.10)).</span><span class="sxs-lookup"><span data-stu-id="bfd77-307">For additional documentation, see [DirectX Developer Center on MSDN](/previous-versions/windows/apps/hh452744(v=win.10)).</span></span>

## <a name="call-to-action"></a><span data-ttu-id="bfd77-308">Invito all'azione ##</span><span class="sxs-lookup"><span data-stu-id="bfd77-308">Call to Action</span></span>

<span data-ttu-id="bfd77-309">Quando si creano applicazioni che tentano di sincronizzare la frequenza dei fotogrammi di presentazione o il ripristino da anomalie di visualizzazione, si consiglia di usare Direct3D 9Ex flip model e le statistiche presenti in Windows 7.</span><span class="sxs-lookup"><span data-stu-id="bfd77-309">We encourage you to use Direct3D 9Ex Flip Model and its present statistics on Windows 7 when you create applications that attempt to synchronize presentation frame rate or recover from display glitches.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bfd77-310">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bfd77-310">Related topics</span></span>

<span data-ttu-id="bfd77-311">[Centro per sviluppatori DirectX su MSDN](/previous-versions/windows/apps/hh452744(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="bfd77-311">[DirectX Developer Center on MSDN](/previous-versions/windows/apps/hh452744(v=win.10))</span></span>
</dt> </dl>