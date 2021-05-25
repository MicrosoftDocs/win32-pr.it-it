---
description: Descrive i parametri di presentazione.
ms.assetid: d677aeb7-a188-4ddc-b8c9-48e13676e9c8
title: D3DPRESENT_PARAMETERS struttura (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DPRESENT_PARAMETERS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: f113b3df247765b958dfe47bb04fafb6c9a13bbe
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343106"
---
# <a name="d3dpresent_parameters-structure"></a><span data-ttu-id="6d3d1-103">Struttura PARAMETERS \_ D3DPRESENT</span><span class="sxs-lookup"><span data-stu-id="6d3d1-103">D3DPRESENT\_PARAMETERS structure</span></span>

<span data-ttu-id="6d3d1-104">Descrive i parametri di presentazione.</span><span class="sxs-lookup"><span data-stu-id="6d3d1-104">Describes the presentation parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d3d1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6d3d1-105">Syntax</span></span>


```C++
typedef struct D3DPRESENT_PARAMETERS {
  UINT                BackBufferWidth;
  UINT                BackBufferHeight;
  D3DFORMAT           BackBufferFormat;
  UINT                BackBufferCount;
  D3DMULTISAMPLE_TYPE MultiSampleType;
  DWORD               MultiSampleQuality;
  D3DSWAPEFFECT       SwapEffect;
  HWND                hDeviceWindow;
  BOOL                Windowed;
  BOOL                EnableAutoDepthStencil;
  D3DFORMAT           AutoDepthStencilFormat;
  DWORD               Flags;
  UINT                FullScreen_RefreshRateInHz;
  UINT                PresentationInterval;
} D3DPRESENT_PARAMETERS, *LPD3DPRESENT_PARAMETERS;
```



## <a name="members"></a><span data-ttu-id="6d3d1-106">Members</span><span class="sxs-lookup"><span data-stu-id="6d3d1-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="6d3d1-107">**BackBufferWidth**</span><span class="sxs-lookup"><span data-stu-id="6d3d1-107">**BackBufferWidth**</span></span>
</dt> <dd>

<span data-ttu-id="6d3d1-108">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6d3d1-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6d3d1-109">Larghezza in pixel dei buffer indietro della nuova catena di scambio.</span><span class="sxs-lookup"><span data-stu-id="6d3d1-109">Width of the new swap chain's back buffers, in pixels.</span></span> <span data-ttu-id="6d3d1-110">Se **Windowed** è **FALSE** (la presentazione è a schermo intero), questo valore deve corrispondere alla larghezza di una delle modalità di visualizzazione enumerate trovate tramite [**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes).</span><span class="sxs-lookup"><span data-stu-id="6d3d1-110">If **Windowed** is **FALSE** (the presentation is full-screen), this value must equal the width of one of the enumerated display modes found through [**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes).</span></span> <span data-ttu-id="6d3d1-111">Se **Windowed** è **TRUE** e **BackBufferWidth** o **BackBufferHeight** è zero, viene presa la dimensione corrispondente dell'area client di **hDeviceWindow** (o della finestra di stato attivo, se **hDeviceWindow** è **NULL).**</span><span class="sxs-lookup"><span data-stu-id="6d3d1-111">If **Windowed** is **TRUE** and either **BackBufferWidth** or **BackBufferHeight** is zero, the corresponding dimension of the client area of the **hDeviceWindow** (or the focus window, if **hDeviceWindow** is **NULL**) is taken.</span></span>

</dd> <dt>

<span data-ttu-id="6d3d1-112">**BackBufferHeight**</span><span class="sxs-lookup"><span data-stu-id="6d3d1-112">**BackBufferHeight**</span></span>
</dt> <dd>

<span data-ttu-id="6d3d1-113">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6d3d1-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6d3d1-114">Altezza in pixel dei buffer indietro della nuova catena di scambio.</span><span class="sxs-lookup"><span data-stu-id="6d3d1-114">Height of the new swap chain's back buffers, in pixels.</span></span> <span data-ttu-id="6d3d1-115">Se **Windowed** è **FALSE** (la presentazione è a schermo intero), questo valore deve corrispondere all'altezza di una delle modalità di visualizzazione enumerate trovate tramite [**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes).</span><span class="sxs-lookup"><span data-stu-id="6d3d1-115">If **Windowed** is **FALSE** (the presentation is full-screen), this value must equal the height of one of the enumerated display modes found through [**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes).</span></span> <span data-ttu-id="6d3d1-116">Se **Windowed** è **TRUE** e **BackBufferWidth** o **BackBufferHeight** è zero, viene presa la dimensione corrispondente dell'area client di **hDeviceWindow** (o della finestra di stato attivo, se **hDeviceWindow** è **NULL).**</span><span class="sxs-lookup"><span data-stu-id="6d3d1-116">If **Windowed** is **TRUE** and either **BackBufferWidth** or **BackBufferHeight** is zero, the corresponding dimension of the client area of the **hDeviceWindow** (or the focus window, if **hDeviceWindow** is **NULL**) is taken.</span></span>

</dd> <dt>

<span data-ttu-id="6d3d1-117">**BackBufferFormat**</span><span class="sxs-lookup"><span data-stu-id="6d3d1-117">**BackBufferFormat**</span></span>
</dt> <dd>

<span data-ttu-id="6d3d1-118">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="6d3d1-118">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6d3d1-119">Formato del buffer nascosto.</span><span class="sxs-lookup"><span data-stu-id="6d3d1-119">The back buffer format.</span></span> <span data-ttu-id="6d3d1-120">Per altre informazioni sui formati, vedere [D3DFORMAT](d3dformat.md).</span><span class="sxs-lookup"><span data-stu-id="6d3d1-120">For more information about formats, see [D3DFORMAT](d3dformat.md).</span></span> <span data-ttu-id="6d3d1-121">Questo valore deve essere uno dei formati di destinazione di rendering convalidati da [**CheckDeviceType.**](/windows/desktop/api)</span><span class="sxs-lookup"><span data-stu-id="6d3d1-121">This value must be one of the render-target formats as validated by [**CheckDeviceType**](/windows/desktop/api).</span></span> <span data-ttu-id="6d3d1-122">È possibile usare [**GetDisplayMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdisplaymode) per ottenere il formato corrente.</span><span class="sxs-lookup"><span data-stu-id="6d3d1-122">You can use [**GetDisplayMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdisplaymode) to obtain the current format.</span></span>

<span data-ttu-id="6d3d1-123">È infatti possibile specificare D3DFMT \_ UNKNOWN per **BackBufferFormat** in modalità finestra.</span><span class="sxs-lookup"><span data-stu-id="6d3d1-123">In fact, D3DFMT\_UNKNOWN can be specified for the **BackBufferFormat** while in windowed mode.</span></span> <span data-ttu-id="6d3d1-124">Questo indica al runtime di usare il formato della modalità di visualizzazione corrente ed elimina la necessità di [**chiamare GetDisplayMode.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdisplaymode)</span><span class="sxs-lookup"><span data-stu-id="6d3d1-124">This tells the runtime to use the current display-mode format and eliminates the need to call [**GetDisplayMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdisplaymode).</span></span>

<span data-ttu-id="6d3d1-125">Per le applicazioni con finestra, il formato del buffer nascosto non deve più corrispondere al formato della modalità di visualizzazione perché la conversione dei colori può ora essere eseguita dall'hardware (se l'hardware supporta la conversione dei colori).</span><span class="sxs-lookup"><span data-stu-id="6d3d1-125">For windowed applications, the back buffer format no longer needs to match the display-mode format because color conversion can now be done by the hardware (if the hardware supports color conversion).</span></span> <span data-ttu-id="6d3d1-126">Il set di possibili formati di buffer nascosto è vincolato, ma il runtime consentirà di presentare qualsiasi formato di buffer nascosto valido a qualsiasi formato desktop.</span><span class="sxs-lookup"><span data-stu-id="6d3d1-126">The set of possible back buffer formats is constrained, but the runtime will allow any valid back buffer format to be presented to any desktop format.</span></span> <span data-ttu-id="6d3d1-127">Esiste il requisito aggiuntivo che il dispositivo sia operabile nel desktop. I dispositivi in genere non funzionano in modalità a 8 bit per pixel.</span><span class="sxs-lookup"><span data-stu-id="6d3d1-127">(There is the additional requirement that the device be operable in the desktop; devices typically do not operate in 8 bits per pixel modes.)</span></span>

<span data-ttu-id="6d3d1-128">Le applicazioni a schermo intero non possono eseguire la conversione dei colori.</span><span class="sxs-lookup"><span data-stu-id="6d3d1-128">Full-screen applications cannot do color conversion.</span></span>

</dd> <dt>

<span data-ttu-id="6d3d1-129">**BackBufferCount**</span><span class="sxs-lookup"><span data-stu-id="6d3d1-129">**BackBufferCount**</span></span>
</dt> <dd>

<span data-ttu-id="6d3d1-130">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6d3d1-130">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6d3d1-131">Questo valore può essere compreso tra 0 e [D3DPRESENT \_ BACK \_ BUFFERS \_ MAX](d3dpresent-back-buffers.md) (o [D3DPRESENT \_ BACK \_ BUFFERS MAX \_ \_ EX](d3dpresent-back-buffers.md) quando si usa Direct3D 9Ex).</span><span class="sxs-lookup"><span data-stu-id="6d3d1-131">This value can be between 0 and [D3DPRESENT\_BACK\_BUFFERS\_MAX](d3dpresent-back-buffers.md) (or [D3DPRESENT\_BACK\_BUFFERS\_MAX\_EX](d3dpresent-back-buffers.md) when using Direct3D 9Ex).</span></span> <span data-ttu-id="6d3d1-132">I valori 0 vengono considerati come 1.</span><span class="sxs-lookup"><span data-stu-id="6d3d1-132">Values of 0 are treated as 1.</span></span> <span data-ttu-id="6d3d1-133">Se non è possibile creare il numero di buffer nascosto, il runtime non riuscirà a chiamare il metodo e riempirà questo valore con il numero di buffer che è possibile creare.</span><span class="sxs-lookup"><span data-stu-id="6d3d1-133">If the number of back buffers cannot be created, the runtime will fail the method call and fill this value with the number of back buffers that could be created.</span></span> <span data-ttu-id="6d3d1-134">Di conseguenza, un'applicazione può chiamare il metodo due volte con la stessa struttura PARAMETERS D3DPRESENT e aspettarsi che \_ funzioni la seconda volta.</span><span class="sxs-lookup"><span data-stu-id="6d3d1-134">As a result, an application can call the method twice with the same D3DPRESENT\_PARAMETERS structure and expect it to work the second time.</span></span>

<span data-ttu-id="6d3d1-135">Il metodo ha esito negativo se non è possibile creare un buffer nascosto.</span><span class="sxs-lookup"><span data-stu-id="6d3d1-135">The method fails if one back buffer cannot be created.</span></span> <span data-ttu-id="6d3d1-136">Il valore di **BackBufferCount** influenza il set di effetti di scambio consentiti.</span><span class="sxs-lookup"><span data-stu-id="6d3d1-136">The value of **BackBufferCount** influences what set of swap effects are allowed.</span></span> <span data-ttu-id="6d3d1-137">In particolare, qualsiasi effetto di scambio COPY D3DSWAPEFFECT richiede \_ che sia presente esattamente un buffer nascosto.</span><span class="sxs-lookup"><span data-stu-id="6d3d1-137">Specifically, any D3DSWAPEFFECT\_COPY swap effect requires that there be exactly one back buffer.</span></span>

</dd> <dt>

<span data-ttu-id="6d3d1-138">**MultiSampleType**</span><span class="sxs-lookup"><span data-stu-id="6d3d1-138">**MultiSampleType**</span></span>
</dt> <dd>

<span data-ttu-id="6d3d1-139">Tipo: **[ **D3DMULTISAMPLE \_ TYPE**](./d3dmultisample-type.md)**</span><span class="sxs-lookup"><span data-stu-id="6d3d1-139">Type: **[**D3DMULTISAMPLE\_TYPE**](./d3dmultisample-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6d3d1-140">Membro del [**tipo enumerato D3DMULTISAMPLE \_ TYPE.**](./d3dmultisample-type.md)</span><span class="sxs-lookup"><span data-stu-id="6d3d1-140">Member of the [**D3DMULTISAMPLE\_TYPE**](./d3dmultisample-type.md) enumerated type.</span></span> <span data-ttu-id="6d3d1-141">Il valore deve essere D3DMULTISAMPLE NONE a meno che SwapEffect non sia stato \_ impostato su  D3DSWAPEFFECT \_ DISCARD.</span><span class="sxs-lookup"><span data-stu-id="6d3d1-141">The value must be D3DMULTISAMPLE\_NONE unless **SwapEffect** has been set to D3DSWAPEFFECT\_DISCARD.</span></span> <span data-ttu-id="6d3d1-142">Il multisampling è supportato solo se l'effetto di scambio è D3DSWAPEFFECT \_ DISCARD.</span><span class="sxs-lookup"><span data-stu-id="6d3d1-142">Multisampling is supported only if the swap effect is D3DSWAPEFFECT\_DISCARD.</span></span>

</dd> <dt>

<span data-ttu-id="6d3d1-143">**MultiSampleQuality**</span><span class="sxs-lookup"><span data-stu-id="6d3d1-143">**MultiSampleQuality**</span></span>
</dt> <dd>

<span data-ttu-id="6d3d1-144">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6d3d1-144">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6d3d1-145">Livello di qualità.</span><span class="sxs-lookup"><span data-stu-id="6d3d1-145">Quality level.</span></span> <span data-ttu-id="6d3d1-146">L'intervallo valido è compreso tra zero e uno minore del livello restituito da pQualityLevels usato da [**CheckDeviceMultiSampleType.**](/windows/desktop/api)</span><span class="sxs-lookup"><span data-stu-id="6d3d1-146">The valid range is between zero and one less than the level returned by pQualityLevels used by [**CheckDeviceMultiSampleType**](/windows/desktop/api).</span></span> <span data-ttu-id="6d3d1-147">Il passaggio di un valore più grande restituisce l'errore D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="6d3d1-147">Passing a larger value returns the error D3DERR\_INVALIDCALL.</span></span> <span data-ttu-id="6d3d1-148">I valori associati delle destinazioni di rendering o depth stencil superfici e [**D3DMULTISAMPLE \_ TYPE**](./d3dmultisample-type.md) devono corrispondere.</span><span class="sxs-lookup"><span data-stu-id="6d3d1-148">Paired values of render targets or of depth stencil surfaces and [**D3DMULTISAMPLE\_TYPE**](./d3dmultisample-type.md) must match.</span></span>

</dd> <dt>

<span data-ttu-id="6d3d1-149">**SwapEffect**</span><span class="sxs-lookup"><span data-stu-id="6d3d1-149">**SwapEffect**</span></span>
</dt> <dd>

<span data-ttu-id="6d3d1-150">Tipo: **[ **D3DSWAPEFFECT**](./d3dswapeffect.md)**</span><span class="sxs-lookup"><span data-stu-id="6d3d1-150">Type: **[**D3DSWAPEFFECT**](./d3dswapeffect.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6d3d1-151">Membro del [**tipo enumerato D3DSWAPEFFECT.**](./d3dswapeffect.md)</span><span class="sxs-lookup"><span data-stu-id="6d3d1-151">Member of the [**D3DSWAPEFFECT**](./d3dswapeffect.md) enumerated type.</span></span> <span data-ttu-id="6d3d1-152">Il runtime garantirà la semantica implicita relativa al comportamento di scambio del buffer. Pertanto, se **Windowed** è **TRUE** e **SwapEffect** è impostato su D3DSWAPEFFECT FLIP, il runtime creerà un buffer nascosto aggiuntivo e copierà quello che diventa il front buffer in fase di \_ presentazione.</span><span class="sxs-lookup"><span data-stu-id="6d3d1-152">The runtime will guarantee the implied semantics concerning buffer swap behavior; therefore, if **Windowed** is **TRUE** and **SwapEffect** is set to D3DSWAPEFFECT\_FLIP, the runtime will create one extra back buffer and copy whichever becomes the front buffer at presentation time.</span></span>

<span data-ttu-id="6d3d1-153">D3DSWAPEFFECT \_ COPY richiede che **BackBufferCount** sia impostato su 1.</span><span class="sxs-lookup"><span data-stu-id="6d3d1-153">D3DSWAPEFFECT\_COPY requires that **BackBufferCount** be set to 1.</span></span>

<span data-ttu-id="6d3d1-154">D3DSWAPEFFECT DISCARD verrà applicato nel runtime di debug riempiendo qualsiasi buffer con \_ rumore dopo la presentazione.</span><span class="sxs-lookup"><span data-stu-id="6d3d1-154">D3DSWAPEFFECT\_DISCARD will be enforced in the debug runtime by filling any buffer with noise after it is presented.</span></span>

<span data-ttu-id="6d3d1-155">Differenze tra Direct3D9 e Direct3D9Ex:</span><span class="sxs-lookup"><span data-stu-id="6d3d1-155">Differences between Direct3D9 and Direct3D9Ex:</span></span>

- <span data-ttu-id="6d3d1-156">In Direct3D9Ex, D3DSWAPEFFECT FLIPEX viene aggiunto per designare quando un'applicazione \_ adotta la modalità flip.</span><span class="sxs-lookup"><span data-stu-id="6d3d1-156">In Direct3D9Ex, D3DSWAPEFFECT\_FLIPEX is added to designate when an application is adopting flip mode.</span></span> <span data-ttu-id="6d3d1-157">Ovvero, il frame di un'applicazione viene passato in modalità finestra (anziché copiato) al Gestione finestre desktop (DWM) per la composizione.</span><span class="sxs-lookup"><span data-stu-id="6d3d1-157">That is, whan an application's frame is passed in window's mode (instead of copied) to the Desktop Window Manager(DWM) for composition.</span></span> <span data-ttu-id="6d3d1-158">La modalità flip offre una larghezza di banda di memoria più efficiente e consente a un'applicazione di sfruttare le statistiche presenti a schermo intero.</span><span class="sxs-lookup"><span data-stu-id="6d3d1-158">Flip mode provides more efficient memory bandwidth and enables an application to take advantage of full-screen-present statistics.</span></span> <span data-ttu-id="6d3d1-159">Non modifica il comportamento a schermo intero.</span><span class="sxs-lookup"><span data-stu-id="6d3d1-159">It does not change full screen behavior.</span></span> <span data-ttu-id="6d3d1-160">Il comportamento della modalità capovolgimento è disponibile a partire da Windows 7.</span><span class="sxs-lookup"><span data-stu-id="6d3d1-160">Flip mode behavior is available beginning with Windows 7.</span></span>



 

</dd> <dt>

<span data-ttu-id="6d3d1-161">**hDeviceWindow**</span><span class="sxs-lookup"><span data-stu-id="6d3d1-161">**hDeviceWindow**</span></span>
</dt> <dd>

<span data-ttu-id="6d3d1-162">Tipo: **[ **HWND**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6d3d1-162">Type: **[**HWND**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6d3d1-163">La finestra del dispositivo determina la posizione e le dimensioni del buffer nascosto sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="6d3d1-163">The device window determines the location and size of the back buffer on screen.</span></span> <span data-ttu-id="6d3d1-164">Viene usato da Direct3D quando il contenuto del buffer nascosto viene copiato nel front buffer durante [**present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present).</span><span class="sxs-lookup"><span data-stu-id="6d3d1-164">This is used by Direct3D when the back buffer contents are copied to the front buffer during [**Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present).</span></span>

-   <span data-ttu-id="6d3d1-165">Per un'applicazione a schermo intero, si tratta di un handle per la finestra superiore, ovvero la finestra attiva.</span><span class="sxs-lookup"><span data-stu-id="6d3d1-165">For a full-screen application, this is a handle to the top window (which is the focus window).</span></span>

    <span data-ttu-id="6d3d1-166">Per le applicazioni che usano più dispositivi a schermo intero(ad esempio un sistema multimonitor), esattamente un dispositivo può usare la finestra di attivazione come finestra del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6d3d1-166">For applications that use multiple full-screen devices (such as a multimonitor system), exactly one device can use the focus window as the device window.</span></span> <span data-ttu-id="6d3d1-167">Tutti gli altri dispositivi devono avere finestre univoche del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6d3d1-167">All other devices must have unique device windows.</span></span>

-   <span data-ttu-id="6d3d1-168">Per un'applicazione in modalità finestra, questo handle sarà la finestra di destinazione predefinita per [**Present.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)</span><span class="sxs-lookup"><span data-stu-id="6d3d1-168">For a windowed-mode application, this handle will be the default target window for [**Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present).</span></span> <span data-ttu-id="6d3d1-169">Se questo handle è **NULL,** verrà attivata la finestra attiva.</span><span class="sxs-lookup"><span data-stu-id="6d3d1-169">If this handle is **NULL**, the focus window will be taken.</span></span>

<span data-ttu-id="6d3d1-170">Si noti che il runtime non tenta di riflettere le modifiche apportate dall'utente alle dimensioni della finestra.</span><span class="sxs-lookup"><span data-stu-id="6d3d1-170">Note that no attempt is made by the runtime to reflect user changes in window size.</span></span> <span data-ttu-id="6d3d1-171">Il buffer nascosto non viene reimpostato in modo implicito quando questa finestra viene reimpostata.</span><span class="sxs-lookup"><span data-stu-id="6d3d1-171">The back buffer is not implicitly reset when this window is reset.</span></span> <span data-ttu-id="6d3d1-172">Tuttavia, il [**metodo Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) tiene traccia automaticamente delle modifiche apportate alla posizione della finestra.</span><span class="sxs-lookup"><span data-stu-id="6d3d1-172">However, the [**Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) method does automatically track window position changes.</span></span>

</dd> <dt>

<span data-ttu-id="6d3d1-173">**Finestra**</span><span class="sxs-lookup"><span data-stu-id="6d3d1-173">**Windowed**</span></span>
</dt> <dd>

<span data-ttu-id="6d3d1-174">Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6d3d1-174">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6d3d1-175">**TRUE se** l'applicazione viene eseguita in finestra; **FALSE** se l'applicazione viene eseguita a schermo intero.</span><span class="sxs-lookup"><span data-stu-id="6d3d1-175">**TRUE** if the application runs windowed; **FALSE** if the application runs full-screen.</span></span>

</dd> <dt>

<span data-ttu-id="6d3d1-176">**EnableAutoDepthStencil**</span><span class="sxs-lookup"><span data-stu-id="6d3d1-176">**EnableAutoDepthStencil**</span></span>
</dt> <dd>

<span data-ttu-id="6d3d1-177">Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6d3d1-177">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6d3d1-178">Se questo valore è **TRUE,** Direct3D gestirà i buffer di profondità per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6d3d1-178">If this value is **TRUE**, Direct3D will manage depth buffers for the application.</span></span> <span data-ttu-id="6d3d1-179">Il dispositivo creerà un buffer depth-stencil al momento della creazione.</span><span class="sxs-lookup"><span data-stu-id="6d3d1-179">The device will create a depth-stencil buffer when it is created.</span></span> <span data-ttu-id="6d3d1-180">Il buffer depth-stencil verrà impostato automaticamente come destinazione di rendering del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6d3d1-180">The depth-stencil buffer will be automatically set as the render target of the device.</span></span> <span data-ttu-id="6d3d1-181">Quando il dispositivo viene reimpostato, il buffer depth-stencil verrà eliminato e ricreato automaticamente con le nuove dimensioni.</span><span class="sxs-lookup"><span data-stu-id="6d3d1-181">When the device is reset, the depth-stencil buffer will be automatically destroyed and recreated in the new size.</span></span>

<span data-ttu-id="6d3d1-182">Se EnableAutoDepthStencil è **TRUE,** AutoDepthStencilFormat deve essere un formato di stencil di profondità valido.</span><span class="sxs-lookup"><span data-stu-id="6d3d1-182">If EnableAutoDepthStencil is **TRUE**, then AutoDepthStencilFormat must be a valid depth-stencil format.</span></span>

</dd> <dt>

<span data-ttu-id="6d3d1-183">**AutoDepthStencilFormat**</span><span class="sxs-lookup"><span data-stu-id="6d3d1-183">**AutoDepthStencilFormat**</span></span>
</dt> <dd>

<span data-ttu-id="6d3d1-184">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="6d3d1-184">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6d3d1-185">Membro del [tipo enumerato D3DFORMAT.](d3dformat.md)</span><span class="sxs-lookup"><span data-stu-id="6d3d1-185">Member of the [D3DFORMAT](d3dformat.md) enumerated type.</span></span> <span data-ttu-id="6d3d1-186">Formato della superficie depth-stencil automatica che verrà creata dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6d3d1-186">The format of the automatic depth-stencil surface that the device will create.</span></span> <span data-ttu-id="6d3d1-187">Questo membro viene ignorato a meno **che EnableAutoDepthStencil** non sia **TRUE.**</span><span class="sxs-lookup"><span data-stu-id="6d3d1-187">This member is ignored unless **EnableAutoDepthStencil** is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="6d3d1-188">**Flag**</span><span class="sxs-lookup"><span data-stu-id="6d3d1-188">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="6d3d1-189">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6d3d1-189">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6d3d1-190">Una delle [costanti D3DPRESENTFLAG.](d3dpresentflag.md)</span><span class="sxs-lookup"><span data-stu-id="6d3d1-190">One of the [D3DPRESENTFLAG](d3dpresentflag.md) constants.</span></span>

</dd> <dt>

<span data-ttu-id="6d3d1-191">**\_RefreshRateInHz a schermo intero**</span><span class="sxs-lookup"><span data-stu-id="6d3d1-191">**FullScreen\_RefreshRateInHz**</span></span>
</dt> <dd>

<span data-ttu-id="6d3d1-192">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6d3d1-192">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6d3d1-193">Frequenza con cui la scheda di visualizzazione aggiorna lo schermo.</span><span class="sxs-lookup"><span data-stu-id="6d3d1-193">The rate at which the display adapter refreshes the screen.</span></span> <span data-ttu-id="6d3d1-194">Il valore dipende dalla modalità di esecuzione dell'applicazione:</span><span class="sxs-lookup"><span data-stu-id="6d3d1-194">The value depends on the mode in which the application is running:</span></span>

-   <span data-ttu-id="6d3d1-195">Per la modalità finestra, la frequenza di aggiornamento deve essere 0.</span><span class="sxs-lookup"><span data-stu-id="6d3d1-195">For windowed mode, the refresh rate must be 0.</span></span>
-   <span data-ttu-id="6d3d1-196">Per la modalità schermo intero, la frequenza di aggiornamento è una delle frequenze di aggiornamento restituite da [**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes).</span><span class="sxs-lookup"><span data-stu-id="6d3d1-196">For full-screen mode, the refresh rate is one of the refresh rates returned by [**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes).</span></span>

</dd> <dt>

<span data-ttu-id="6d3d1-197">**PresentationInterval**</span><span class="sxs-lookup"><span data-stu-id="6d3d1-197">**PresentationInterval**</span></span>
</dt> <dd>

<span data-ttu-id="6d3d1-198">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6d3d1-198">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6d3d1-199">Velocità massima con cui i buffer back della catena di scambio possono essere presentati al front buffer.</span><span class="sxs-lookup"><span data-stu-id="6d3d1-199">The maximum rate at which the swap chain's back buffers can be presented to the front buffer.</span></span> <span data-ttu-id="6d3d1-200">Per una spiegazione dettagliata delle modalità e degli intervalli supportati, vedere [D3DPRESENT](d3dpresent.md).</span><span class="sxs-lookup"><span data-stu-id="6d3d1-200">For a detailed explanation of the modes and the intervals that are supported, see [D3DPRESENT](d3dpresent.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6d3d1-201">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6d3d1-201">Requirements</span></span>



| <span data-ttu-id="6d3d1-202">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d3d1-202">Requirement</span></span> | <span data-ttu-id="6d3d1-203">Valore</span><span class="sxs-lookup"><span data-stu-id="6d3d1-203">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6d3d1-204">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6d3d1-204">Header</span></span><br/> | <dl> <span data-ttu-id="6d3d1-205"><dt>D3D9Types.h</dt></span><span class="sxs-lookup"><span data-stu-id="6d3d1-205"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d3d1-206">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6d3d1-206">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d3d1-207">Strutture Direct3D</span><span class="sxs-lookup"><span data-stu-id="6d3d1-207">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="6d3d1-208">**CreateDevice**</span><span class="sxs-lookup"><span data-stu-id="6d3d1-208">**CreateDevice**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice)
</dt> <dt>

[<span data-ttu-id="6d3d1-209">**CreateAdditionalSwapChain**</span><span class="sxs-lookup"><span data-stu-id="6d3d1-209">**CreateAdditionalSwapChain**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain)
</dt> <dt>

[<span data-ttu-id="6d3d1-210">**Presente**</span><span class="sxs-lookup"><span data-stu-id="6d3d1-210">**Present**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)
</dt> <dt>

[<span data-ttu-id="6d3d1-211">**Reset**</span><span class="sxs-lookup"><span data-stu-id="6d3d1-211">**Reset**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)
</dt> </dl>

 

 
