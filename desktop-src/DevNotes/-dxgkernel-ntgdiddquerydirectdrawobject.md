---
description: Esegue una query su una rappresentazione in modalità kernel creata in precedenza di un oggetto DirectDraw Microsoft per le relative funzionalità.
ms.assetid: ec07c7ef-4c57-4ed9-849b-f30692cc3181
title: Funzione NtGdiDdQueryDirectDrawObject (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdQueryDirectDrawObject
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 557854f70f4f1a55022b16d1bfe045efbc017a13
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878118"
---
# <a name="ntgdiddquerydirectdrawobject-function"></a><span data-ttu-id="cf033-103">NtGdiDdQueryDirectDrawObject (funzione)</span><span class="sxs-lookup"><span data-stu-id="cf033-103">NtGdiDdQueryDirectDrawObject function</span></span>

<span data-ttu-id="cf033-104">\[Questa funzione è soggetta a modifiche a ogni revisione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="cf033-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="cf033-105">Usare invece il DirectDraw e Microsoft Direct3DAPIs; Queste API isolano le applicazioni da tali modifiche del sistema operativo e nascondono molte altre difficoltà legate all'interazione diretta con i driver di visualizzazione.\]</span><span class="sxs-lookup"><span data-stu-id="cf033-105">Instead, use the DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="cf033-106">Esegue una query su una rappresentazione in modalità kernel creata in precedenza di un oggetto DirectDraw Microsoft per le relative funzionalità.</span><span class="sxs-lookup"><span data-stu-id="cf033-106">Queries a previously created kernel-mode representation of a Microsoft DirectDraw object for its capabilities.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf033-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cf033-107">Syntax</span></span>


```C++
BOOL APIENTRY NtGdiDdQueryDirectDrawObject(
  _In_  HANDLE                      hDirectDrawLocal,
  _Out_ DD_HALINFO                  *pHalInfo,
        DWORD                       *pCallBackFlags,
  _Out_ LPD3DNTHAL_CALLBACKS        puD3dCallbacks,
  _Out_ LPD3DNTHAL_GLOBALDRIVERDATA puD3dDriverData,
  _Out_ PDD_D3DBUFCALLBACKS         puD3dBufferCallbacks,
  _Out_ LPDDSURFACEDESC             puD3dTextureFormats,
  _Out_ DWORD                       *puNumHeaps,
  _Out_ VIDEOMEMORY                 *puvmList,
  _Out_ DWORD                       *puNumFourCC,
  _Out_ DWORD                       *puFourCC
);
```



## <a name="parameters"></a><span data-ttu-id="cf033-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="cf033-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf033-109">*hDirectDrawLocal* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cf033-109">*hDirectDrawLocal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf033-110">Handle per il dispositivo DirectDraw in modalità kernel creato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="cf033-110">Handle to the previously-created kernel-mode DirectDraw device.</span></span>

</dd> <dt>

<span data-ttu-id="cf033-111">*pHalInfo* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="cf033-111">*pHalInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cf033-112">Puntatore a una [**struttura \_ HALINFO DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo) che verrà compilata con le funzionalità del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cf033-112">Pointer to a [**DD\_HALINFO**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo) structure that will be filled with the device's capabilities.</span></span> <span data-ttu-id="cf033-113">Per informazioni dettagliate, vedere la documentazione di DDK.</span><span class="sxs-lookup"><span data-stu-id="cf033-113">See DDK documentation for details.</span></span>

</dd> <dt>

<span data-ttu-id="cf033-114">*pCallBackFlags*</span><span class="sxs-lookup"><span data-stu-id="cf033-114">*pCallBackFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="cf033-115">Puntatore a un buffer fornito dal chiamante che archivia i flag di callback segnalati dal driver.</span><span class="sxs-lookup"><span data-stu-id="cf033-115">Pointer to a caller-provided buffer that stores driver-reported callback flags.</span></span> <span data-ttu-id="cf033-116">Il buffer deve essere di dimensioni 3 \* sizeof (DWORD) e archivia i flag di callback nell'ordine seguente: pCallBackFlags \[ 0 \] per i flag nei [**\_ callback GG**](/windows/win32/api/ddrawint/ns-ddrawint-dd_callbacks), PCallBackFlags \[ 1 per i \] flag in [**DD \_ SURFACECALLBACKS**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surfacecallbacks)e pCallBackFlags \[ 2 per i \] flag in [**DD \_ PALETTECALLBACKS**](/windows/win32/api/ddrawint/ns-ddrawint-dd_palettecallbacks).</span><span class="sxs-lookup"><span data-stu-id="cf033-116">The buffer should be of size 3\*sizeof(DWORD) and stores callback flags in the following order: pCallBackFlags\[0\] for flags in [**DD\_CALLBACKS**](/windows/win32/api/ddrawint/ns-ddrawint-dd_callbacks), pCallBackFlags\[1\] for flags in [**DD\_SURFACECALLBACKS**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surfacecallbacks), and pCallBackFlags\[2\] for flags in [**DD\_PALETTECALLBACKS**](/windows/win32/api/ddrawint/ns-ddrawint-dd_palettecallbacks).</span></span> <span data-ttu-id="cf033-117">Per informazioni dettagliate, vedere la documentazione di DDK.</span><span class="sxs-lookup"><span data-stu-id="cf033-117">See DDK documentation for details.</span></span>

</dd> <dt>

<span data-ttu-id="cf033-118">*puD3dCallbacks* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="cf033-118">*puD3dCallbacks* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cf033-119">Puntatore a una tabella di puntatori di callback Direct3D.</span><span class="sxs-lookup"><span data-stu-id="cf033-119">Pointer to a table of Direct3D callback pointers.</span></span> <span data-ttu-id="cf033-120">La tabella viene compilata con i puntatori alle funzioni all'interno Gdi32.dll che imitano un driver di visualizzazione Direct3D.</span><span class="sxs-lookup"><span data-stu-id="cf033-120">The table is filled with pointers to functions within Gdi32.dll that imitate a Direct3D display driver.</span></span> <span data-ttu-id="cf033-121">Questa tabella di callback è identica alla \_ struttura D3DHAL D3DCALLBACKS descritta nella documentazione di DDK.</span><span class="sxs-lookup"><span data-stu-id="cf033-121">This callback table is identical to the D3DHAL\_D3DCALLBACKS structure discussed in the DDK documentation.</span></span>

</dd> <dt>

<span data-ttu-id="cf033-122">*puD3dDriverData* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="cf033-122">*puD3dDriverData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cf033-123">Puntatore ai [**dati \_ GLOBALDRIVERDATA di D3DHAL**](/windows-hardware/drivers/ddi/d3dhal/ns-d3dhal-_d3dhal_globaldriverdata) , come descritto nella documentazione di DDK.</span><span class="sxs-lookup"><span data-stu-id="cf033-123">Pointer to [**D3DHAL\_GLOBALDRIVERDATA**](/windows-hardware/drivers/ddi/d3dhal/ns-d3dhal-_d3dhal_globaldriverdata) data, as described in the DDK documentation.</span></span>

</dd> <dt>

<span data-ttu-id="cf033-124">*puD3dBufferCallbacks* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="cf033-124">*puD3dBufferCallbacks* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cf033-125">Puntatore a una tabella di puntatori di callback.</span><span class="sxs-lookup"><span data-stu-id="cf033-125">Pointer to a table of callback pointers.</span></span> <span data-ttu-id="cf033-126">La tabella viene compilata con i puntatori alle funzioni all'interno Gdi32.dll che imitano un driver di visualizzazione Direct3D.</span><span class="sxs-lookup"><span data-stu-id="cf033-126">The table is filled with pointers to functions within Gdi32.dll that imitate a Direct3D display driver.</span></span> <span data-ttu-id="cf033-127">Questa tabella di callback è identica alla \_ struttura DDEXEBUFCALLBACKS di DDHAL, che esegue il mapping alla struttura [**DD \_ D3DBUFCALLBACKS**](/windows/win32/api/ddrawint/ns-ddrawint-dd_d3dbufcallbacks) descritta nella documentazione di DDK, con la differenza che i membri XxxD3DBuffer in **DD \_ D3DBUFCALLBACKS** vengono sostituiti con XxxExecuteBuffer in DDHAL \_ DDEXEBUFCALLBACKS.</span><span class="sxs-lookup"><span data-stu-id="cf033-127">This callback table is identical to the DDHAL\_DDEXEBUFCALLBACKS structure, which maps to the [**DD\_D3DBUFCALLBACKS**](/windows/win32/api/ddrawint/ns-ddrawint-dd_d3dbufcallbacks) structure discussed in the DDK documentation, except that members XxxD3DBuffer in **DD\_D3DBUFCALLBACKS** are replaced with XxxExecuteBuffer in DDHAL\_DDEXEBUFCALLBACKS.</span></span>

</dd> <dt>

<span data-ttu-id="cf033-128">*puD3dTextureFormats* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="cf033-128">*puD3dTextureFormats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cf033-129">Puntatore a una matrice di strutture [**DDSURFACEDESC**](/previous-versions/windows/hardware/drivers/ff550339(v=vs.85)) che definiscono il set di formati di trama consentiti.</span><span class="sxs-lookup"><span data-stu-id="cf033-129">Pointer to an array of [**DDSURFACEDESC**](/previous-versions/windows/hardware/drivers/ff550339(v=vs.85)) structures that define the set of permissible texture formats.</span></span>

</dd> <dt>

<span data-ttu-id="cf033-130">*puNumHeaps* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="cf033-130">*puNumHeaps* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cf033-131">Puntatore al membro **dwNumHeaps** di [**DD \_ HALINFO**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo).**vmiData**.</span><span class="sxs-lookup"><span data-stu-id="cf033-131">Pointer to the **dwNumHeaps** member of [**DD\_HALINFO**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo).**vmiData**.</span></span> <span data-ttu-id="cf033-132">Il membro **dwNumHeaps** specifica il numero di heap di memoria in *puvmList*.</span><span class="sxs-lookup"><span data-stu-id="cf033-132">The **dwNumHeaps** member specifies the number of memory heaps in *puvmList*.</span></span> <span data-ttu-id="cf033-133">Per informazioni dettagliate, vedere la documentazione di DDK.</span><span class="sxs-lookup"><span data-stu-id="cf033-133">See DDK documentation for details.</span></span>

</dd> <dt>

<span data-ttu-id="cf033-134">*puvmList* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="cf033-134">*puvmList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cf033-135">Puntatore a un elenco di descrittori di heap di memoria video.</span><span class="sxs-lookup"><span data-stu-id="cf033-135">Pointer to a list of video memory heap descriptors.</span></span> <span data-ttu-id="cf033-136">Può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="cf033-136">Can be **NULL**.</span></span> <span data-ttu-id="cf033-137">Questo parametro non viene utilizzato perché la gestione della memoria video viene gestita interamente in modalità kernel.</span><span class="sxs-lookup"><span data-stu-id="cf033-137">This parameter is not used because video memory management is handled entirely within kernel mode.</span></span>

</dd> <dt>

<span data-ttu-id="cf033-138">*puNumFourCC* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="cf033-138">*puNumFourCC* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cf033-139">Puntatore al membro **puNumFourCCCodes** di [**DD \_ HALINFO**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo).**ddCaps**.</span><span class="sxs-lookup"><span data-stu-id="cf033-139">Pointer to the **puNumFourCCCodes** member of [**DD\_HALINFO**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo).**ddCaps**.</span></span> <span data-ttu-id="cf033-140">Il membro **puNumFourCCCodes** specifica il numero di codici di [quattro caratteri (fourcc)](../directshow/fourcc-codes.md) supportati dal driver.</span><span class="sxs-lookup"><span data-stu-id="cf033-140">The **puNumFourCCCodes** member specifies the number of [Four-Character Codes (FOURCC)](../directshow/fourcc-codes.md) codes that the driver supports.</span></span> <span data-ttu-id="cf033-141">Per informazioni dettagliate, vedere la documentazione di DDK.</span><span class="sxs-lookup"><span data-stu-id="cf033-141">See DDK documentation for details.</span></span>

</dd> <dt>

<span data-ttu-id="cf033-142">*puFourCC* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="cf033-142">*puFourCC* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cf033-143">Puntatore a un elenco di formati di superficie supportati per i [codici a quattro caratteri (fourcc)](../directshow/fourcc-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="cf033-143">Pointer to a list of supported [Four-Character Codes (FOURCC)](../directshow/fourcc-codes.md) surface formats.</span></span> <span data-ttu-id="cf033-144">Può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="cf033-144">Can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf033-145">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cf033-145">Return value</span></span>

<span data-ttu-id="cf033-146">Se l'esito è positivo, la funzione restituisce **true**. in caso contrario, restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="cf033-146">If successful, this function returns **TRUE**; otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf033-147">Commenti</span><span class="sxs-lookup"><span data-stu-id="cf033-147">Remarks</span></span>

<span data-ttu-id="cf033-148">Una chiamata a questa funzione è progettata per essere eseguita in un processo in due passaggi.</span><span class="sxs-lookup"><span data-stu-id="cf033-148">A call to this function is designed to be made in a two-step process.</span></span> <span data-ttu-id="cf033-149">Nel primo passaggio, *puFourCC*, *puvmList* e *PuD3dTextureFormats* devono essere **null** e [**DdQueryDirectDrawObject**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddquerydirectdrawobject) compilerà [**gg \_ HALINFO**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo).**ddCaps**. **dwNumFourCCCodes**, **gg \_ HALINFO**.**vmiData**. **dwNumHeaps** e [**D3DHAL \_ GLOBALDRIVERDATA**](/windows-hardware/drivers/ddi/d3dhal/ns-d3dhal-_d3dhal_globaldriverdata).**dwNumTextureFormats** con il numero di voci da restituire.</span><span class="sxs-lookup"><span data-stu-id="cf033-149">In the first step, *puFourCC*, *puvmList* and *puD3dTextureFormats* should be **NULL**, and [**DdQueryDirectDrawObject**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddquerydirectdrawobject) will fill in [**DD\_HALINFO**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo).**ddCaps**.**dwNumFourCCCodes**, **DD\_HALINFO**.**vmiData**.**dwNumHeaps**, and [**D3DHAL\_GLOBALDRIVERDATA**](/windows-hardware/drivers/ddi/d3dhal/ns-d3dhal-_d3dhal_globaldriverdata).**dwNumTextureFormats** with the number of entries that are to be returned.</span></span> <span data-ttu-id="cf033-150">Nella seconda chiamata, il chiamante deve allocare matrici della dimensione indicata e passare tali puntatori invece dei valori **null** nei parametri *puFourCC*, *puvmList* e *puD3dTextureFormats* .</span><span class="sxs-lookup"><span data-stu-id="cf033-150">In the second call, the caller should allocate arrays of the indicated size and pass those pointers instead of **NULL** values in the *puFourCC*, *puvmList* and *puD3dTextureFormats* parameters.</span></span> <span data-ttu-id="cf033-151">Le matrici verranno quindi popolate con i dati appropriati.</span><span class="sxs-lookup"><span data-stu-id="cf033-151">The arrays will then be populated with appropriate data.</span></span>

<span data-ttu-id="cf033-152">Per creare e gestire oggetti dispositivo di grafica, è consigliabile usare le API DirectDraw e [Direct3D](../direct3d10/d3d10-graphics-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="cf033-152">Applications are advised to use the DirectDraw and [Direct3D](../direct3d10/d3d10-graphics-reference.md) APIs to create and manage graphics device objects.</span></span> <span data-ttu-id="cf033-153">Questi costrutti astraggono il processo di creazione del dispositivo in modo semplificato e indipendente dal sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="cf033-153">These constructs abstract the device creation process in a simplified and operating-system-independent way.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf033-154">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cf033-154">Requirements</span></span>



| <span data-ttu-id="cf033-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf033-155">Requirement</span></span> | <span data-ttu-id="cf033-156">Valore</span><span class="sxs-lookup"><span data-stu-id="cf033-156">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cf033-157">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cf033-157">Minimum supported client</span></span><br/> | <span data-ttu-id="cf033-158">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="cf033-158">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="cf033-159">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cf033-159">Minimum supported server</span></span><br/> | <span data-ttu-id="cf033-160">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="cf033-160">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="cf033-161">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cf033-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf033-162"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf033-162"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf033-163">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cf033-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf033-164">Supporto client di livello inferiore grafica</span><span class="sxs-lookup"><span data-stu-id="cf033-164">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[<span data-ttu-id="cf033-165">**DdQueryDirectDrawObject**</span><span class="sxs-lookup"><span data-stu-id="cf033-165">**DdQueryDirectDrawObject**</span></span>](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddquerydirectdrawobject)
</dt> <dt>

[<span data-ttu-id="cf033-166">**NtGdiDdCreateDirectDrawObject**</span><span class="sxs-lookup"><span data-stu-id="cf033-166">**NtGdiDdCreateDirectDrawObject**</span></span>](-dxgkernel-ntgdiddcreatedirectdrawobject.md)
</dt> </dl>

 

 
