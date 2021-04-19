---
description: Crea un file con estensione x e salva la gerarchia mesh e le relative animazioni corrispondenti.
ms.assetid: 803926fe-8cb7-422a-9920-56f7d0b0d0ea
title: Funzione D3DXSaveMeshHierarchyToFile (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSaveMeshHierarchyToFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f2de65f9bc2f9e40a5bc07c6f0b4d00112f0df21
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322604"
---
# <a name="d3dxsavemeshhierarchytofile-function"></a><span data-ttu-id="e7754-103">D3DXSaveMeshHierarchyToFile (funzione)</span><span class="sxs-lookup"><span data-stu-id="e7754-103">D3DXSaveMeshHierarchyToFile function</span></span>

<span data-ttu-id="e7754-104">Crea un file con estensione x e salva la gerarchia mesh e le relative animazioni corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="e7754-104">Creates a .x file and saves the mesh hierarchy and corresponding animations in it.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7754-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e7754-105">Syntax</span></span>


```C++
HRESULT D3DXSaveMeshHierarchyToFile(
  _In_       LPCSTR                    pFilename,
  _In_       DWORD                     XFormat,
  _In_ const D3DXFRAME                 *pFrameRoot,
  _In_       LPD3DXANIMATIONCONTROLLER pAnimController,
  _In_       LPD3DXSAVEUSERDATA        pUserDataSaver
);
```



## <a name="parameters"></a><span data-ttu-id="e7754-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e7754-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7754-107">*pFilename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e7754-107">*pFilename* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7754-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e7754-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e7754-109">Puntatore a una stringa che specifica il nome del file con estensione x che identifica la mesh salvata.</span><span class="sxs-lookup"><span data-stu-id="e7754-109">Pointer to a string that specifies the name of the .x file identifying the saved mesh.</span></span> <span data-ttu-id="e7754-110">Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="e7754-110">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="e7754-111">In caso contrario, il tipo di dati String viene risolto in LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="e7754-111">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="e7754-112">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="e7754-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="e7754-113">*XFormat* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e7754-113">*XFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7754-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e7754-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e7754-115">Formato del file con estensione x (testo o binario, compresso o meno).</span><span class="sxs-lookup"><span data-stu-id="e7754-115">Format of the .x file (text or binary, compressed or not).</span></span> <span data-ttu-id="e7754-116">Vedere D3DXF \_ FILEformat.</span><span class="sxs-lookup"><span data-stu-id="e7754-116">See D3DXF\_FILEFORMAT.</span></span> <span data-ttu-id="e7754-117">D3DXF \_ FileFormat \_ compresso può essere combinato (usando un OR logico) con i flag di testo FileFormat D3DXF \_ \_ o D3DXF \_ \_ per ridurre le dimensioni del file di output.</span><span class="sxs-lookup"><span data-stu-id="e7754-117">D3DXF\_FILEFORMAT\_COMPRESSED can be combined (using a logical OR) with either the D3DXF\_FILEFORMAT\_BINARY or D3DXF\_FILEFORMAT\_TEXT flags to reduce the output file size.</span></span>

</dd> <dt>

<span data-ttu-id="e7754-118">*pFrameRoot* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e7754-118">*pFrameRoot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7754-119">Tipo: **const [**D3DXFRAME**](d3dxframe.md) \***</span><span class="sxs-lookup"><span data-stu-id="e7754-119">Type: **const [**D3DXFRAME**](d3dxframe.md)\***</span></span>

<span data-ttu-id="e7754-120">Nodo radice della gerarchia da salvare.</span><span class="sxs-lookup"><span data-stu-id="e7754-120">Root node of the hierarchy to be saved.</span></span> <span data-ttu-id="e7754-121">Vedere [**D3DXFRAME**](d3dxframe.md).</span><span class="sxs-lookup"><span data-stu-id="e7754-121">See [**D3DXFRAME**](d3dxframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="e7754-122">*pAnimController* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e7754-122">*pAnimController* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7754-123">Tipo: **[ **LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="e7754-123">Type: **[**LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="e7754-124">Controller di animazione con set di animazioni da archiviare.</span><span class="sxs-lookup"><span data-stu-id="e7754-124">Animation controller that has animation sets to be stored.</span></span> <span data-ttu-id="e7754-125">Vedere [**ID3DXAnimationController**](id3dxanimationcontroller.md).</span><span class="sxs-lookup"><span data-stu-id="e7754-125">See [**ID3DXAnimationController**](id3dxanimationcontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="e7754-126">*pUserDataSaver* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e7754-126">*pUserDataSaver* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7754-127">Tipo: **[ **LPD3DXSAVEUSERDATA**](id3dxsaveuserdata.md)**</span><span class="sxs-lookup"><span data-stu-id="e7754-127">Type: **[**LPD3DXSAVEUSERDATA**](id3dxsaveuserdata.md)**</span></span>

<span data-ttu-id="e7754-128">Interfaccia fornita dall'applicazione che consente il salvataggio dei dati utente.</span><span class="sxs-lookup"><span data-stu-id="e7754-128">Application-provided interface that allows saving of user data.</span></span> <span data-ttu-id="e7754-129">Vedere [**ID3DXSaveUserData**](id3dxsaveuserdata.md).</span><span class="sxs-lookup"><span data-stu-id="e7754-129">See [**ID3DXSaveUserData**](id3dxsaveuserdata.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7754-130">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e7754-130">Return value</span></span>

<span data-ttu-id="e7754-131">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e7754-131">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e7754-132">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e7754-132">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e7754-133">Se la funzione ha esito negativo, il valore restituito può essere: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="e7754-133">If the function fails, the return value can be: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7754-134">Commenti</span><span class="sxs-lookup"><span data-stu-id="e7754-134">Remarks</span></span>

<span data-ttu-id="e7754-135">L'impostazione del compilatore determina anche la versione della funzione.</span><span class="sxs-lookup"><span data-stu-id="e7754-135">The compiler setting also determines the function version.</span></span> <span data-ttu-id="e7754-136">Se è definito Unicode, la chiamata di funzione viene risolta in D3DXSaveMeshHierarchyToFileW.</span><span class="sxs-lookup"><span data-stu-id="e7754-136">If Unicode is defined, the function call resolves to D3DXSaveMeshHierarchyToFileW.</span></span> <span data-ttu-id="e7754-137">In caso contrario, la chiamata di funzione viene risolta in D3DXSaveMeshHierarchyToFileA.</span><span class="sxs-lookup"><span data-stu-id="e7754-137">Otherwise, the function call resolves to D3DXSaveMeshHierarchyToFileA.</span></span>

<span data-ttu-id="e7754-138">Questa funzione non salva i set di animazioni compressi.</span><span class="sxs-lookup"><span data-stu-id="e7754-138">This function does not save compressed animation sets.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7754-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e7754-139">Requirements</span></span>



| <span data-ttu-id="e7754-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7754-140">Requirement</span></span> | <span data-ttu-id="e7754-141">Valore</span><span class="sxs-lookup"><span data-stu-id="e7754-141">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e7754-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e7754-142">Header</span></span><br/>  | <dl> <span data-ttu-id="e7754-143"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7754-143"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="e7754-144">Libreria</span><span class="sxs-lookup"><span data-stu-id="e7754-144">Library</span></span><br/> | <dl> <span data-ttu-id="e7754-145"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e7754-145"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e7754-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e7754-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7754-147">Funzioni di animazione</span><span class="sxs-lookup"><span data-stu-id="e7754-147">Animation Functions</span></span>](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> <dt>

[<span data-ttu-id="e7754-148">Riferimento al file X</span><span class="sxs-lookup"><span data-stu-id="e7754-148">X File Reference</span></span>](dx9-graphics-reference-d3dx-x-file.md)
</dt> </dl>

 

 
