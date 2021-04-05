---
description: Carica la prima gerarchia di frame da un file con estensione x.
ms.assetid: 1d446b23-9028-4187-b97c-a61edfe68e39
title: Funzione D3DXLoadMeshHierarchyFromX (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadMeshHierarchyFromX
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 308ebf127708849bec8ee8a4f2601f029562634a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969305"
---
# <a name="d3dxloadmeshhierarchyfromx-function"></a><span data-ttu-id="e897c-103">D3DXLoadMeshHierarchyFromX (funzione)</span><span class="sxs-lookup"><span data-stu-id="e897c-103">D3DXLoadMeshHierarchyFromX function</span></span>

<span data-ttu-id="e897c-104">Carica la prima gerarchia di frame da un file con estensione x.</span><span class="sxs-lookup"><span data-stu-id="e897c-104">Loads the first frame hierarchy from a .x file.</span></span>

## <a name="syntax"></a><span data-ttu-id="e897c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e897c-105">Syntax</span></span>


```C++
HRESULT D3DXLoadMeshHierarchyFromX(
  _In_  LPCTSTR                   Filename,
  _In_  DWORD                     MeshOptions,
  _In_  LPDIRECT3DDEVICE9         pDevice,
  _In_  LPD3DXALLOCATEHIERARCHY   pAlloc,
  _In_  LPD3DXLOADUSERDATA        pUserDataLoader,
  _Out_ LPD3DXFRAME               *ppFrameHierarchy,
  _Out_ LPD3DXANIMATIONCONTROLLER *ppAnimController
);
```



## <a name="parameters"></a><span data-ttu-id="e897c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e897c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e897c-107">*Nome file* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e897c-107">*Filename* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e897c-108">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e897c-108">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e897c-109">Puntatore a una stringa che specifica il nome del file.</span><span class="sxs-lookup"><span data-stu-id="e897c-109">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="e897c-110">Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="e897c-110">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="e897c-111">In caso contrario, il tipo di dati String viene risolto in LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="e897c-111">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="e897c-112">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="e897c-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="e897c-113">*MeshOptions* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e897c-113">*MeshOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e897c-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e897c-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e897c-115">Combinazione di uno o più flag dell'enumerazione [**D3DXMESH**](./d3dxmesh.md) che specificano le opzioni di creazione per la mesh.</span><span class="sxs-lookup"><span data-stu-id="e897c-115">Combination of one or more flags from the [**D3DXMESH**](./d3dxmesh.md) enumeration that specify creation options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="e897c-116">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e897c-116">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e897c-117">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="e897c-117">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="e897c-118">Puntatore a un'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , l'oggetto dispositivo associato alla mesh.</span><span class="sxs-lookup"><span data-stu-id="e897c-118">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, the device object associated with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="e897c-119">*pAlloc* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e897c-119">*pAlloc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e897c-120">Tipo: **[ **LPD3DXALLOCATEHIERARCHY**](id3dxallocatehierarchy.md)**</span><span class="sxs-lookup"><span data-stu-id="e897c-120">Type: **[**LPD3DXALLOCATEHIERARCHY**](id3dxallocatehierarchy.md)**</span></span>

<span data-ttu-id="e897c-121">Puntatore a un'interfaccia [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md) .</span><span class="sxs-lookup"><span data-stu-id="e897c-121">Pointer to an [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="e897c-122">*pUserDataLoader* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e897c-122">*pUserDataLoader* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e897c-123">Tipo: **[ **LPD3DXLOADUSERDATA**](id3dxloaduserdata.md)**</span><span class="sxs-lookup"><span data-stu-id="e897c-123">Type: **[**LPD3DXLOADUSERDATA**](id3dxloaduserdata.md)**</span></span>

<span data-ttu-id="e897c-124">Interfaccia fornita dall'applicazione che consente il caricamento dei dati utente.</span><span class="sxs-lookup"><span data-stu-id="e897c-124">Application provided interface that allows loading of user data.</span></span> <span data-ttu-id="e897c-125">Vedere [**ID3DXLoadUserData**](id3dxloaduserdata.md).</span><span class="sxs-lookup"><span data-stu-id="e897c-125">See [**ID3DXLoadUserData**](id3dxloaduserdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="e897c-126">*ppFrameHierarchy* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="e897c-126">*ppFrameHierarchy* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e897c-127">Tipo: **[ **LPD3DXFRAME**](d3dxframe.md)\***</span><span class="sxs-lookup"><span data-stu-id="e897c-127">Type: **[**LPD3DXFRAME**](d3dxframe.md)\***</span></span>

<span data-ttu-id="e897c-128">Restituisce un puntatore alla gerarchia dei frame caricati.</span><span class="sxs-lookup"><span data-stu-id="e897c-128">Returns a pointer to the loaded frame hierarchy.</span></span> <span data-ttu-id="e897c-129">Vedere [**D3DXFRAME**](d3dxframe.md).</span><span class="sxs-lookup"><span data-stu-id="e897c-129">See [**D3DXFRAME**](d3dxframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="e897c-130">*ppAnimController* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="e897c-130">*ppAnimController* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e897c-131">Tipo: **[ **LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)\***</span><span class="sxs-lookup"><span data-stu-id="e897c-131">Type: **[**LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)\***</span></span>

<span data-ttu-id="e897c-132">Restituisce un puntatore al controller di animazione corrispondente all'animazione nel file con estensione x.</span><span class="sxs-lookup"><span data-stu-id="e897c-132">Returns a pointer to the animation controller corresponding to animation in the .x file.</span></span> <span data-ttu-id="e897c-133">Questa operazione viene creata con tracce ed eventi predefiniti.</span><span class="sxs-lookup"><span data-stu-id="e897c-133">This is created with default tracks and events.</span></span> <span data-ttu-id="e897c-134">Vedere [**ID3DXAnimationController**](id3dxanimationcontroller.md).</span><span class="sxs-lookup"><span data-stu-id="e897c-134">See [**ID3DXAnimationController**](id3dxanimationcontroller.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e897c-135">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e897c-135">Return value</span></span>

<span data-ttu-id="e897c-136">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e897c-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e897c-137">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e897c-137">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e897c-138">Se la funzione ha esito negativo, il valore restituito può essere uno dei valori seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="e897c-138">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="e897c-139">Commenti</span><span class="sxs-lookup"><span data-stu-id="e897c-139">Remarks</span></span>

<span data-ttu-id="e897c-140">L'impostazione del compilatore determina anche la versione della funzione.</span><span class="sxs-lookup"><span data-stu-id="e897c-140">The compiler setting also determines the function version.</span></span> <span data-ttu-id="e897c-141">Se è definito Unicode, la chiamata di funzione viene risolta in D3DXLoadMeshHierarchyFromXW.</span><span class="sxs-lookup"><span data-stu-id="e897c-141">If Unicode is defined, the function call resolves to D3DXLoadMeshHierarchyFromXW.</span></span> <span data-ttu-id="e897c-142">In caso contrario, la chiamata di funzione viene risolta in D3DXLoadMeshHierarchyFromXA.</span><span class="sxs-lookup"><span data-stu-id="e897c-142">Otherwise, the function call resolves to D3DXLoadMeshHierarchyFromXA.</span></span>

<span data-ttu-id="e897c-143">Tutte le mesh nel file verranno compresse in una mesh di output.</span><span class="sxs-lookup"><span data-stu-id="e897c-143">All the meshes in the file will be collapsed into one output mesh.</span></span> <span data-ttu-id="e897c-144">Se il file contiene una gerarchia di frame, tutte le trasformazioni verranno applicate alla rete.</span><span class="sxs-lookup"><span data-stu-id="e897c-144">If the file contains a frame hierarchy, all the transformations will be applied to the mesh.</span></span>

<span data-ttu-id="e897c-145">**D3DXLoadMeshHierarchyFromX** carica i dati di animazione e la gerarchia dei frame da un file con estensione x.</span><span class="sxs-lookup"><span data-stu-id="e897c-145">**D3DXLoadMeshHierarchyFromX** loads the animation data and frame hierarchy from a .x file.</span></span> <span data-ttu-id="e897c-146">Analizza il file con estensione x e compila una gerarchia dei frame e un controller di animazione in base all'oggetto derivato da [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md)passato attraverso pAlloc.</span><span class="sxs-lookup"><span data-stu-id="e897c-146">It scans the .x file and builds a frame hierarchy and animation controller according to the [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md)-derived object passed to it through pAlloc.</span></span> <span data-ttu-id="e897c-147">Il caricamento dei dati richiede diversi passaggi, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="e897c-147">Loading the data requires several steps as follows:</span></span>

1.  <span data-ttu-id="e897c-148">Derivare [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md), implementando ogni metodo.</span><span class="sxs-lookup"><span data-stu-id="e897c-148">Derive [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md), implementing each method.</span></span> <span data-ttu-id="e897c-149">Questa operazione Controlla la modalità di allocazione e liberazione di frame e mesh.</span><span class="sxs-lookup"><span data-stu-id="e897c-149">This controls how frames and meshes are allocated and freed.</span></span>
2.  <span data-ttu-id="e897c-150">Derivare [**ID3DXLoadUserData**](id3dxloaduserdata.md), implementando ogni metodo.</span><span class="sxs-lookup"><span data-stu-id="e897c-150">Derive [**ID3DXLoadUserData**](id3dxloaduserdata.md), implementing each method.</span></span> <span data-ttu-id="e897c-151">Se il file con estensione x non contiene dati incorporati definiti dall'utente o se non è necessario, è possibile ignorare questa parte.</span><span class="sxs-lookup"><span data-stu-id="e897c-151">If your .x file has no embedded user-defined data, or if you do not need it, you can skip this part.</span></span>
3.  <span data-ttu-id="e897c-152">Creare un oggetto della classe [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md) e, facoltativamente, la classe LoadUserData.</span><span class="sxs-lookup"><span data-stu-id="e897c-152">Create an object of your [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md) class, and optionally of your LoadUserData class.</span></span> <span data-ttu-id="e897c-153">Non è necessario chiamare alcun metodo di questi oggetti.</span><span class="sxs-lookup"><span data-stu-id="e897c-153">You do not need to call any methods of these objects yourself.</span></span>
4.  <span data-ttu-id="e897c-154">Chiamare **D3DXLoadMeshHierarchyFromX**, passando l'oggetto [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md) e l'oggetto [**ID3DXLoadUserData**](id3dxloaduserdata.md) (o **null**) per creare la gerarchia dei frame e il controller di animazione.</span><span class="sxs-lookup"><span data-stu-id="e897c-154">Call **D3DXLoadMeshHierarchyFromX**, passing in your [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md) object and your [**ID3DXLoadUserData**](id3dxloaduserdata.md) object (or **NULL**) to create the frame hierarchy and animation controller.</span></span> <span data-ttu-id="e897c-155">Tutti i set di animazioni e i frame vengono registrati automaticamente nel controller di animazione.</span><span class="sxs-lookup"><span data-stu-id="e897c-155">All the animation sets and frames are automatically registered to the animation controller.</span></span>

<span data-ttu-id="e897c-156">Durante il caricamento, [**CreateFrame**](id3dxallocatehierarchy--createframe.md) e [**LoadFrameChildData**](id3dxloaduserdata--loadframechilddata.md) vengono richiamati in ogni frame per controllare il caricamento e l'allocazione del frame.</span><span class="sxs-lookup"><span data-stu-id="e897c-156">During the load, [**CreateFrame**](id3dxallocatehierarchy--createframe.md) and [**LoadFrameChildData**](id3dxloaduserdata--loadframechilddata.md) are called back on each frame to control loading and allocation of the frame.</span></span> <span data-ttu-id="e897c-157">L'applicazione definisce questi metodi per controllare la modalità di archiviazione dei frame.</span><span class="sxs-lookup"><span data-stu-id="e897c-157">The application defines these methods to control how frames are stored.</span></span> <span data-ttu-id="e897c-158">[**CreateMeshContainer**](id3dxallocatehierarchy--createmeshcontainer.md) e [**LoadMeshChildData**](id3dxloaduserdata--loadmeshchilddata.md) vengono richiamati in ogni oggetto mesh per controllare il caricamento e l'allocazione di oggetti mesh.</span><span class="sxs-lookup"><span data-stu-id="e897c-158">[**CreateMeshContainer**](id3dxallocatehierarchy--createmeshcontainer.md) and [**LoadMeshChildData**](id3dxloaduserdata--loadmeshchilddata.md) are called back on each mesh object to control loading and allocation of mesh objects.</span></span> <span data-ttu-id="e897c-159">[**LoadTopLevelData**](id3dxloaduserdata--loadtopleveldata.md) viene richiamato per ogni oggetto di primo livello che non viene caricato dagli altri metodi.</span><span class="sxs-lookup"><span data-stu-id="e897c-159">[**LoadTopLevelData**](id3dxloaduserdata--loadtopleveldata.md) is called back for each top level object that doesn't get loaded by the other methods.</span></span>

<span data-ttu-id="e897c-160">Per liberare questi dati, chiamare ID3DXAnimationController:: Release per liberare i set di animazioni e [**D3DXFRAMEDestroy**](d3dxframedestroy.md), passando il nodo radice della gerarchia dei frame e un oggetto della classe [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md) derivata.</span><span class="sxs-lookup"><span data-stu-id="e897c-160">To free this data, call ID3DXAnimationController::Release to free the animation sets, and [**D3DXFRAMEDestroy**](d3dxframedestroy.md), passing in the root node of the frame hierarchy and an object of your derived [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md) class.</span></span> <span data-ttu-id="e897c-161">[**DestroyFrame**](id3dxallocatehierarchy--destroyframe.md) e [**DestroyMeshContainer**](id3dxallocatehierarchy--destroymeshcontainer.md) verranno chiamati per ogni oggetto frame e mesh nella gerarchia dei frame.</span><span class="sxs-lookup"><span data-stu-id="e897c-161">[**DestroyFrame**](id3dxallocatehierarchy--destroyframe.md) and [**DestroyMeshContainer**](id3dxallocatehierarchy--destroymeshcontainer.md) will each be called for every frame and mesh object in the frame hierarchy.</span></span> <span data-ttu-id="e897c-162">L'implementazione di **DestroyFrame** deve rilasciare tutti gli elementi allocati da [**CreateFrame**](id3dxallocatehierarchy--createframe.md)e allo stesso modo per i metodi del contenitore mesh.</span><span class="sxs-lookup"><span data-stu-id="e897c-162">Your implementation of **DestroyFrame** should release everything allocated by [**CreateFrame**](id3dxallocatehierarchy--createframe.md), and likewise for the mesh container methods.</span></span>

## <a name="requirements"></a><span data-ttu-id="e897c-163">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e897c-163">Requirements</span></span>



| <span data-ttu-id="e897c-164">Requisito</span><span class="sxs-lookup"><span data-stu-id="e897c-164">Requirement</span></span> | <span data-ttu-id="e897c-165">Valore</span><span class="sxs-lookup"><span data-stu-id="e897c-165">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e897c-166">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e897c-166">Header</span></span><br/>  | <dl> <span data-ttu-id="e897c-167"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="e897c-167"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="e897c-168">Libreria</span><span class="sxs-lookup"><span data-stu-id="e897c-168">Library</span></span><br/> | <dl> <span data-ttu-id="e897c-169"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e897c-169"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e897c-170">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e897c-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e897c-171">Funzioni di animazione</span><span class="sxs-lookup"><span data-stu-id="e897c-171">Animation Functions</span></span>](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
