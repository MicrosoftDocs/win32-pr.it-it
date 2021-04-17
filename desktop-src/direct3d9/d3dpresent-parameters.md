---
description: Descrive i parametri di presentazione.
ms.assetid: d677aeb7-a188-4ddc-b8c9-48e13676e9c8
title: Struttura D3DPRESENT_PARAMETERS (D3D9Types. h)
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
ms.openlocfilehash: f83ab03773356a01c8c6ac490bb099c6e7508be2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355059"
---
# <a name="d3dpresent_parameters-structure"></a><span data-ttu-id="ba1c9-103">\_Struttura dei parametri D3DPRESENT</span><span class="sxs-lookup"><span data-stu-id="ba1c9-103">D3DPRESENT\_PARAMETERS structure</span></span>

<span data-ttu-id="ba1c9-104">Descrive i parametri di presentazione.</span><span class="sxs-lookup"><span data-stu-id="ba1c9-104">Describes the presentation parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba1c9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ba1c9-105">Syntax</span></span>


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



## <a name="members"></a><span data-ttu-id="ba1c9-106">Members</span><span class="sxs-lookup"><span data-stu-id="ba1c9-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="ba1c9-107">**BackBufferWidth**</span><span class="sxs-lookup"><span data-stu-id="ba1c9-107">**BackBufferWidth**</span></span>
</dt> <dd>

<span data-ttu-id="ba1c9-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ba1c9-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ba1c9-109">Larghezza dei buffer indietro della nuova catena di scambio, in pixel.</span><span class="sxs-lookup"><span data-stu-id="ba1c9-109">Width of the new swap chain's back buffers, in pixels.</span></span> <span data-ttu-id="ba1c9-110">Se la **finestra** è **impostata su false** (la presentazione è a schermo intero), questo valore deve essere uguale alla larghezza di una delle modalità di visualizzazione enumerate trovate tramite [**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes).</span><span class="sxs-lookup"><span data-stu-id="ba1c9-110">If **Windowed** is **FALSE** (the presentation is full-screen), this value must equal the width of one of the enumerated display modes found through [**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes).</span></span> <span data-ttu-id="ba1c9-111">Se la **finestra** è **true** e **BackBufferWidth** o **BackBufferHeight** è zero, viene acquisita la dimensione corrispondente dell'area client di **hDeviceWindow** (o la finestra di stato attivo, se **hDeviceWindow** è **null**).</span><span class="sxs-lookup"><span data-stu-id="ba1c9-111">If **Windowed** is **TRUE** and either **BackBufferWidth** or **BackBufferHeight** is zero, the corresponding dimension of the client area of the **hDeviceWindow** (or the focus window, if **hDeviceWindow** is **NULL**) is taken.</span></span>

</dd> <dt>

<span data-ttu-id="ba1c9-112">**BackBufferHeight**</span><span class="sxs-lookup"><span data-stu-id="ba1c9-112">**BackBufferHeight**</span></span>
</dt> <dd>

<span data-ttu-id="ba1c9-113">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ba1c9-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ba1c9-114">Altezza dei buffer indietro della nuova catena di scambio, in pixel.</span><span class="sxs-lookup"><span data-stu-id="ba1c9-114">Height of the new swap chain's back buffers, in pixels.</span></span> <span data-ttu-id="ba1c9-115">Se la **finestra** è **impostata su false** (la presentazione è a schermo intero), questo valore deve corrispondere all'altezza di una delle modalità di visualizzazione enumerate individuate tramite [**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes).</span><span class="sxs-lookup"><span data-stu-id="ba1c9-115">If **Windowed** is **FALSE** (the presentation is full-screen), this value must equal the height of one of the enumerated display modes found through [**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes).</span></span> <span data-ttu-id="ba1c9-116">Se la **finestra** è **true** e **BackBufferWidth** o **BackBufferHeight** è zero, viene acquisita la dimensione corrispondente dell'area client di **hDeviceWindow** (o la finestra di stato attivo, se **hDeviceWindow** è **null**).</span><span class="sxs-lookup"><span data-stu-id="ba1c9-116">If **Windowed** is **TRUE** and either **BackBufferWidth** or **BackBufferHeight** is zero, the corresponding dimension of the client area of the **hDeviceWindow** (or the focus window, if **hDeviceWindow** is **NULL**) is taken.</span></span>

</dd> <dt>

<span data-ttu-id="ba1c9-117">**BackBufferFormat**</span><span class="sxs-lookup"><span data-stu-id="ba1c9-117">**BackBufferFormat**</span></span>
</dt> <dd>

<span data-ttu-id="ba1c9-118">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="ba1c9-118">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ba1c9-119">Il formato del buffer nascosto.</span><span class="sxs-lookup"><span data-stu-id="ba1c9-119">The back buffer format.</span></span> <span data-ttu-id="ba1c9-120">Per ulteriori informazioni sui formati, vedere [D3DFORMAT](d3dformat.md).</span><span class="sxs-lookup"><span data-stu-id="ba1c9-120">For more information about formats, see [D3DFORMAT](d3dformat.md).</span></span> <span data-ttu-id="ba1c9-121">Questo valore deve essere uno dei formati di destinazione di rendering convalidato da [**CheckDeviceType**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="ba1c9-121">This value must be one of the render-target formats as validated by [**CheckDeviceType**](/windows/desktop/api).</span></span> <span data-ttu-id="ba1c9-122">È possibile usare [**GetDisplayMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdisplaymode) per ottenere il formato corrente.</span><span class="sxs-lookup"><span data-stu-id="ba1c9-122">You can use [**GetDisplayMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdisplaymode) to obtain the current format.</span></span>

<span data-ttu-id="ba1c9-123">In realtà, \_ è possibile specificare D3DFMT Unknown per **BackBufferFormat** in modalità Window.</span><span class="sxs-lookup"><span data-stu-id="ba1c9-123">In fact, D3DFMT\_UNKNOWN can be specified for the **BackBufferFormat** while in windowed mode.</span></span> <span data-ttu-id="ba1c9-124">In questo modo si indica al runtime di usare il formato di visualizzazione corrente e si elimina la necessità di chiamare [**GetDisplayMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdisplaymode).</span><span class="sxs-lookup"><span data-stu-id="ba1c9-124">This tells the runtime to use the current display-mode format and eliminates the need to call [**GetDisplayMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdisplaymode).</span></span>

<span data-ttu-id="ba1c9-125">Per le applicazioni a finestra, il formato del buffer nascosto non deve più corrispondere al formato della modalità di visualizzazione, perché la conversione dei colori può ora essere eseguita dall'hardware (se l'hardware supporta la conversione dei colori).</span><span class="sxs-lookup"><span data-stu-id="ba1c9-125">For windowed applications, the back buffer format no longer needs to match the display-mode format because color conversion can now be done by the hardware (if the hardware supports color conversion).</span></span> <span data-ttu-id="ba1c9-126">Il set di possibili formati di buffer indietro è vincolato, ma il runtime consentirà di presentare qualsiasi formato di buffer nascosto valido da presentare a qualsiasi formato desktop.</span><span class="sxs-lookup"><span data-stu-id="ba1c9-126">The set of possible back buffer formats is constrained, but the runtime will allow any valid back buffer format to be presented to any desktop format.</span></span> <span data-ttu-id="ba1c9-127">È necessario che il dispositivo sia utilizzabile sul desktop. i dispositivi in genere non funzionano in modalità a 8 bit per pixel.</span><span class="sxs-lookup"><span data-stu-id="ba1c9-127">(There is the additional requirement that the device be operable in the desktop; devices typically do not operate in 8 bits per pixel modes.)</span></span>

<span data-ttu-id="ba1c9-128">Le applicazioni a schermo intero non possono eseguire la conversione di colori.</span><span class="sxs-lookup"><span data-stu-id="ba1c9-128">Full-screen applications cannot do color conversion.</span></span>

</dd> <dt>

<span data-ttu-id="ba1c9-129">**BackBufferCount**</span><span class="sxs-lookup"><span data-stu-id="ba1c9-129">**BackBufferCount**</span></span>
</dt> <dd>

<span data-ttu-id="ba1c9-130">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ba1c9-130">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ba1c9-131">Questo valore può essere compreso tra 0 e [D3DPRESENT \_ back \_ buffers \_ Max](d3dpresent-back-buffers.md) (o [D3DPRESENT \_ buffer back \_ \_ Max \_ ex](d3dpresent-back-buffers.md) quando si usa Direct3D 9Ex).</span><span class="sxs-lookup"><span data-stu-id="ba1c9-131">This value can be between 0 and [D3DPRESENT\_BACK\_BUFFERS\_MAX](d3dpresent-back-buffers.md) (or [D3DPRESENT\_BACK\_BUFFERS\_MAX\_EX](d3dpresent-back-buffers.md) when using Direct3D 9Ex).</span></span> <span data-ttu-id="ba1c9-132">I valori 0 vengono considerati come 1.</span><span class="sxs-lookup"><span data-stu-id="ba1c9-132">Values of 0 are treated as 1.</span></span> <span data-ttu-id="ba1c9-133">Se non è possibile creare il numero di buffer indietro, il runtime non riuscirà a eseguire la chiamata al metodo e a riempire questo valore con il numero di buffer back che è possibile creare.</span><span class="sxs-lookup"><span data-stu-id="ba1c9-133">If the number of back buffers cannot be created, the runtime will fail the method call and fill this value with the number of back buffers that could be created.</span></span> <span data-ttu-id="ba1c9-134">Di conseguenza, un'applicazione può chiamare il metodo due volte con la stessa \_ struttura di parametri D3DPRESENT e prevedere che funzioni la seconda volta.</span><span class="sxs-lookup"><span data-stu-id="ba1c9-134">As a result, an application can call the method twice with the same D3DPRESENT\_PARAMETERS structure and expect it to work the second time.</span></span>

<span data-ttu-id="ba1c9-135">Il metodo ha esito negativo se non è possibile creare un buffer nascosto.</span><span class="sxs-lookup"><span data-stu-id="ba1c9-135">The method fails if one back buffer cannot be created.</span></span> <span data-ttu-id="ba1c9-136">Il valore di **BackBufferCount** influenza il set di effetti di scambio consentito.</span><span class="sxs-lookup"><span data-stu-id="ba1c9-136">The value of **BackBufferCount** influences what set of swap effects are allowed.</span></span> <span data-ttu-id="ba1c9-137">In particolare, qualsiasi \_ effetto di scambio di copia di D3DSWAPEFFECT richiede che esista esattamente un buffer nascosto.</span><span class="sxs-lookup"><span data-stu-id="ba1c9-137">Specifically, any D3DSWAPEFFECT\_COPY swap effect requires that there be exactly one back buffer.</span></span>

</dd> <dt>

<span data-ttu-id="ba1c9-138">**MultiSampleType**</span><span class="sxs-lookup"><span data-stu-id="ba1c9-138">**MultiSampleType**</span></span>
</dt> <dd>

<span data-ttu-id="ba1c9-139">Tipo: **[ **D3DMULTISAMPLE \_**](./d3dmultisample-type.md)**</span><span class="sxs-lookup"><span data-stu-id="ba1c9-139">Type: **[**D3DMULTISAMPLE\_TYPE**](./d3dmultisample-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ba1c9-140">Membro del tipo enumerato di [**\_ tipo D3DMULTISAMPLE**](./d3dmultisample-type.md) .</span><span class="sxs-lookup"><span data-stu-id="ba1c9-140">Member of the [**D3DMULTISAMPLE\_TYPE**](./d3dmultisample-type.md) enumerated type.</span></span> <span data-ttu-id="ba1c9-141">Il valore deve essere D3DMULTISAMPLE \_ None, a meno che **SwapEffect** non sia stato impostato su D3DSWAPEFFECT \_ Ignora.</span><span class="sxs-lookup"><span data-stu-id="ba1c9-141">The value must be D3DMULTISAMPLE\_NONE unless **SwapEffect** has been set to D3DSWAPEFFECT\_DISCARD.</span></span> <span data-ttu-id="ba1c9-142">Il campionamento multiplo è supportato solo se l'effetto di scambio è D3DSWAPEFFECT \_ scarto.</span><span class="sxs-lookup"><span data-stu-id="ba1c9-142">Multisampling is supported only if the swap effect is D3DSWAPEFFECT\_DISCARD.</span></span>

</dd> <dt>

<span data-ttu-id="ba1c9-143">**MultiSampleQuality**</span><span class="sxs-lookup"><span data-stu-id="ba1c9-143">**MultiSampleQuality**</span></span>
</dt> <dd>

<span data-ttu-id="ba1c9-144">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ba1c9-144">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ba1c9-145">Livello di qualità.</span><span class="sxs-lookup"><span data-stu-id="ba1c9-145">Quality level.</span></span> <span data-ttu-id="ba1c9-146">L'intervallo valido è compreso tra zero e uno minore del livello restituito da pQualityLevels usato da [**CheckDeviceMultiSampleType**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="ba1c9-146">The valid range is between zero and one less than the level returned by pQualityLevels used by [**CheckDeviceMultiSampleType**](/windows/desktop/api).</span></span> <span data-ttu-id="ba1c9-147">Se si passa un valore maggiore, viene restituito l'errore D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="ba1c9-147">Passing a larger value returns the error D3DERR\_INVALIDCALL.</span></span> <span data-ttu-id="ba1c9-148">I valori abbinati delle destinazioni di rendering o delle superfici di depth stencil e del [**\_ tipo D3DMULTISAMPLE**](./d3dmultisample-type.md) devono corrispondere.</span><span class="sxs-lookup"><span data-stu-id="ba1c9-148">Paired values of render targets or of depth stencil surfaces and [**D3DMULTISAMPLE\_TYPE**](./d3dmultisample-type.md) must match.</span></span>

</dd> <dt>

<span data-ttu-id="ba1c9-149">**SwapEffect**</span><span class="sxs-lookup"><span data-stu-id="ba1c9-149">**SwapEffect**</span></span>
</dt> <dd>

<span data-ttu-id="ba1c9-150">Tipo: **[ **D3DSWAPEFFECT**](./d3dswapeffect.md)**</span><span class="sxs-lookup"><span data-stu-id="ba1c9-150">Type: **[**D3DSWAPEFFECT**](./d3dswapeffect.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ba1c9-151">Membro del tipo enumerato [**D3DSWAPEFFECT**](./d3dswapeffect.md) .</span><span class="sxs-lookup"><span data-stu-id="ba1c9-151">Member of the [**D3DSWAPEFFECT**](./d3dswapeffect.md) enumerated type.</span></span> <span data-ttu-id="ba1c9-152">Il runtime garantirà la semantica implicita sul comportamento di scambio del buffer; Se, pertanto, la **finestra** è **true** e **SwapEffect** è impostato su D3DSWAPEFFECT \_ Flip, il runtime creerà un ulteriore buffer indietro e copierà a seconda di quale diventa il buffer anteriore al momento della presentazione.</span><span class="sxs-lookup"><span data-stu-id="ba1c9-152">The runtime will guarantee the implied semantics concerning buffer swap behavior; therefore, if **Windowed** is **TRUE** and **SwapEffect** is set to D3DSWAPEFFECT\_FLIP, the runtime will create one extra back buffer and copy whichever becomes the front buffer at presentation time.</span></span>

<span data-ttu-id="ba1c9-153">\_Per la copia di D3DSWAPEFFECT è necessario che **BackBufferCount** sia impostato su 1.</span><span class="sxs-lookup"><span data-stu-id="ba1c9-153">D3DSWAPEFFECT\_COPY requires that **BackBufferCount** be set to 1.</span></span>

<span data-ttu-id="ba1c9-154">D3DSWAPEFFECT \_ scarto verrà applicato nel runtime di debug riempiendo qualsiasi buffer con rumore dopo la presentazione.</span><span class="sxs-lookup"><span data-stu-id="ba1c9-154">D3DSWAPEFFECT\_DISCARD will be enforced in the debug runtime by filling any buffer with noise after it is presented.</span></span>



|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba1c9-155">Differenze tra Direct3D9 e Direct3D9Ex</span><span class="sxs-lookup"><span data-stu-id="ba1c9-155">Differences between Direct3D9 and Direct3D9Ex</span></span><br/> <span data-ttu-id="ba1c9-156">In Direct3D9Ex, D3DSWAPEFFECT \_ FLIPEX viene aggiunto per indicare quando un'applicazione sta adottando la modalità Flip.</span><span class="sxs-lookup"><span data-stu-id="ba1c9-156">In Direct3D9Ex, D3DSWAPEFFECT\_FLIPEX is added to designate when an application is adopting flip mode.</span></span> <span data-ttu-id="ba1c9-157">Ovvero, whan il frame di un'applicazione viene passato in modalità della finestra (anziché copiato) al Gestione finestre desktop (DWM) per la composizione.</span><span class="sxs-lookup"><span data-stu-id="ba1c9-157">That is, whan an application's frame is passed in window's mode (instead of copied) to the Desktop Window Manager(DWM) for composition.</span></span> <span data-ttu-id="ba1c9-158">La modalità Flip garantisce una larghezza di banda di memoria più efficiente e consente a un'applicazione di sfruttare le statistiche presenti a schermo intero.</span><span class="sxs-lookup"><span data-stu-id="ba1c9-158">Flip mode provides more efficient memory bandwidth and enables an application to take advantage of full-screen-present statistics.</span></span> <span data-ttu-id="ba1c9-159">Non modifica il comportamento a schermo intero.</span><span class="sxs-lookup"><span data-stu-id="ba1c9-159">It does not change full screen behavior.</span></span> <span data-ttu-id="ba1c9-160">Il comportamento della modalità Flip è disponibile a partire da Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ba1c9-160">Flip mode behavior is available beginning with Windows 7.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="ba1c9-161">**hDeviceWindow**</span><span class="sxs-lookup"><span data-stu-id="ba1c9-161">**hDeviceWindow**</span></span>
</dt> <dd>

<span data-ttu-id="ba1c9-162">Tipo: **[ **HWND**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ba1c9-162">Type: **[**HWND**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ba1c9-163">La finestra del dispositivo determina la posizione e le dimensioni del buffer nascosto sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="ba1c9-163">The device window determines the location and size of the back buffer on screen.</span></span> <span data-ttu-id="ba1c9-164">Viene usato da Direct3D quando il contenuto del buffer nascosto viene copiato nel buffer anteriore durante il [**presente**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present).</span><span class="sxs-lookup"><span data-stu-id="ba1c9-164">This is used by Direct3D when the back buffer contents are copied to the front buffer during [**Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present).</span></span>

-   <span data-ttu-id="ba1c9-165">Per un'applicazione a schermo intero, si tratta di un handle per la finestra superiore (ovvero la finestra di stato attivo).</span><span class="sxs-lookup"><span data-stu-id="ba1c9-165">For a full-screen application, this is a handle to the top window (which is the focus window).</span></span>

    <span data-ttu-id="ba1c9-166">Per le applicazioni che usano più dispositivi a schermo intero, ad esempio un sistema a più monitor, un solo dispositivo può usare la finestra di stato attivo come finestra del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ba1c9-166">For applications that use multiple full-screen devices (such as a multimonitor system), exactly one device can use the focus window as the device window.</span></span> <span data-ttu-id="ba1c9-167">Tutti gli altri dispositivi devono avere finestre del dispositivo univoche.</span><span class="sxs-lookup"><span data-stu-id="ba1c9-167">All other devices must have unique device windows.</span></span>

-   <span data-ttu-id="ba1c9-168">Per un'applicazione in modalità finestra, questo handle sarà la finestra di destinazione predefinita per il [**presente**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present).</span><span class="sxs-lookup"><span data-stu-id="ba1c9-168">For a windowed-mode application, this handle will be the default target window for [**Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present).</span></span> <span data-ttu-id="ba1c9-169">Se questo handle è **null**, verrà eseguita la finestra messa a fuoco.</span><span class="sxs-lookup"><span data-stu-id="ba1c9-169">If this handle is **NULL**, the focus window will be taken.</span></span>

<span data-ttu-id="ba1c9-170">Si noti che non viene eseguito alcun tentativo da parte del runtime di riflettere le modifiche dell'utente nelle dimensioni della finestra.</span><span class="sxs-lookup"><span data-stu-id="ba1c9-170">Note that no attempt is made by the runtime to reflect user changes in window size.</span></span> <span data-ttu-id="ba1c9-171">Il buffer nascosto non viene reimpostato in modo implicito quando viene reimpostata questa finestra.</span><span class="sxs-lookup"><span data-stu-id="ba1c9-171">The back buffer is not implicitly reset when this window is reset.</span></span> <span data-ttu-id="ba1c9-172">Tuttavia, il metodo [**attuale**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) rileva automaticamente le modifiche alla posizione della finestra.</span><span class="sxs-lookup"><span data-stu-id="ba1c9-172">However, the [**Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) method does automatically track window position changes.</span></span>

</dd> <dt>

<span data-ttu-id="ba1c9-173">**Finestra**</span><span class="sxs-lookup"><span data-stu-id="ba1c9-173">**Windowed**</span></span>
</dt> <dd>

<span data-ttu-id="ba1c9-174">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ba1c9-174">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ba1c9-175">**True** se l'applicazione viene eseguita con finestra; **False** se l'applicazione viene eseguita a schermo intero.</span><span class="sxs-lookup"><span data-stu-id="ba1c9-175">**TRUE** if the application runs windowed; **FALSE** if the application runs full-screen.</span></span>

</dd> <dt>

<span data-ttu-id="ba1c9-176">**EnableAutoDepthStencil**</span><span class="sxs-lookup"><span data-stu-id="ba1c9-176">**EnableAutoDepthStencil**</span></span>
</dt> <dd>

<span data-ttu-id="ba1c9-177">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ba1c9-177">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ba1c9-178">Se questo valore è **true**, Direct3D gestirà i buffer di profondità per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ba1c9-178">If this value is **TRUE**, Direct3D will manage depth buffers for the application.</span></span> <span data-ttu-id="ba1c9-179">Il dispositivo creerà un buffer di stencil Depth quando viene creato.</span><span class="sxs-lookup"><span data-stu-id="ba1c9-179">The device will create a depth-stencil buffer when it is created.</span></span> <span data-ttu-id="ba1c9-180">Il buffer di stencil Depth verrà impostato automaticamente come destinazione di rendering del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ba1c9-180">The depth-stencil buffer will be automatically set as the render target of the device.</span></span> <span data-ttu-id="ba1c9-181">Quando il dispositivo viene reimpostato, il buffer di stencil Depth verrà automaticamente eliminato e ricreato con le nuove dimensioni.</span><span class="sxs-lookup"><span data-stu-id="ba1c9-181">When the device is reset, the depth-stencil buffer will be automatically destroyed and recreated in the new size.</span></span>

<span data-ttu-id="ba1c9-182">Se EnableAutoDepthStencil è **true**, AutoDepthStencilFormat deve essere un formato di stencil Depth valido.</span><span class="sxs-lookup"><span data-stu-id="ba1c9-182">If EnableAutoDepthStencil is **TRUE**, then AutoDepthStencilFormat must be a valid depth-stencil format.</span></span>

</dd> <dt>

<span data-ttu-id="ba1c9-183">**AutoDepthStencilFormat**</span><span class="sxs-lookup"><span data-stu-id="ba1c9-183">**AutoDepthStencilFormat**</span></span>
</dt> <dd>

<span data-ttu-id="ba1c9-184">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="ba1c9-184">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ba1c9-185">Membro del tipo enumerato [D3DFORMAT](d3dformat.md) .</span><span class="sxs-lookup"><span data-stu-id="ba1c9-185">Member of the [D3DFORMAT](d3dformat.md) enumerated type.</span></span> <span data-ttu-id="ba1c9-186">Formato della superficie di stencil di profondità automatica che il dispositivo creerà.</span><span class="sxs-lookup"><span data-stu-id="ba1c9-186">The format of the automatic depth-stencil surface that the device will create.</span></span> <span data-ttu-id="ba1c9-187">Questo membro viene ignorato a meno che **EnableAutoDepthStencil** non sia **true**.</span><span class="sxs-lookup"><span data-stu-id="ba1c9-187">This member is ignored unless **EnableAutoDepthStencil** is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="ba1c9-188">**Flag**</span><span class="sxs-lookup"><span data-stu-id="ba1c9-188">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="ba1c9-189">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ba1c9-189">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ba1c9-190">Una delle costanti [D3DPRESENTFLAG](d3dpresentflag.md) .</span><span class="sxs-lookup"><span data-stu-id="ba1c9-190">One of the [D3DPRESENTFLAG](d3dpresentflag.md) constants.</span></span>

</dd> <dt>

<span data-ttu-id="ba1c9-191">**RefreshRateInHz a schermo intero \_**</span><span class="sxs-lookup"><span data-stu-id="ba1c9-191">**FullScreen\_RefreshRateInHz**</span></span>
</dt> <dd>

<span data-ttu-id="ba1c9-192">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ba1c9-192">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ba1c9-193">Velocità con cui l'adattatore di visualizzazione aggiorna lo schermo.</span><span class="sxs-lookup"><span data-stu-id="ba1c9-193">The rate at which the display adapter refreshes the screen.</span></span> <span data-ttu-id="ba1c9-194">Il valore dipende dalla modalità in cui l'applicazione è in esecuzione:</span><span class="sxs-lookup"><span data-stu-id="ba1c9-194">The value depends on the mode in which the application is running:</span></span>

-   <span data-ttu-id="ba1c9-195">Per la modalità finestra, la frequenza di aggiornamento deve essere 0.</span><span class="sxs-lookup"><span data-stu-id="ba1c9-195">For windowed mode, the refresh rate must be 0.</span></span>
-   <span data-ttu-id="ba1c9-196">Per la modalità schermo intero, la frequenza di aggiornamento è una delle frequenze di aggiornamento restituite da [**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes).</span><span class="sxs-lookup"><span data-stu-id="ba1c9-196">For full-screen mode, the refresh rate is one of the refresh rates returned by [**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes).</span></span>

</dd> <dt>

<span data-ttu-id="ba1c9-197">**PresentationInterval**</span><span class="sxs-lookup"><span data-stu-id="ba1c9-197">**PresentationInterval**</span></span>
</dt> <dd>

<span data-ttu-id="ba1c9-198">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ba1c9-198">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ba1c9-199">Frequenza massima con cui i buffer indietro della catena di scambio possono essere presentati al buffer anteriore.</span><span class="sxs-lookup"><span data-stu-id="ba1c9-199">The maximum rate at which the swap chain's back buffers can be presented to the front buffer.</span></span> <span data-ttu-id="ba1c9-200">Per una spiegazione dettagliata delle modalità e degli intervalli supportati, vedere [D3DPRESENT](d3dpresent.md).</span><span class="sxs-lookup"><span data-stu-id="ba1c9-200">For a detailed explanation of the modes and the intervals that are supported, see [D3DPRESENT](d3dpresent.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ba1c9-201">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ba1c9-201">Requirements</span></span>



| <span data-ttu-id="ba1c9-202">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba1c9-202">Requirement</span></span> | <span data-ttu-id="ba1c9-203">Valore</span><span class="sxs-lookup"><span data-stu-id="ba1c9-203">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ba1c9-204">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ba1c9-204">Header</span></span><br/> | <dl> <span data-ttu-id="ba1c9-205"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba1c9-205"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba1c9-206">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ba1c9-206">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba1c9-207">Strutture Direct3D</span><span class="sxs-lookup"><span data-stu-id="ba1c9-207">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="ba1c9-208">**CreateDevice**</span><span class="sxs-lookup"><span data-stu-id="ba1c9-208">**CreateDevice**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice)
</dt> <dt>

[<span data-ttu-id="ba1c9-209">**CreateAdditionalSwapChain**</span><span class="sxs-lookup"><span data-stu-id="ba1c9-209">**CreateAdditionalSwapChain**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain)
</dt> <dt>

[<span data-ttu-id="ba1c9-210">**Presente**</span><span class="sxs-lookup"><span data-stu-id="ba1c9-210">**Present**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)
</dt> <dt>

[<span data-ttu-id="ba1c9-211">**Reset**</span><span class="sxs-lookup"><span data-stu-id="ba1c9-211">**Reset**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)
</dt> </dl>

 

 
