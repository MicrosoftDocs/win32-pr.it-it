---
description: Crea una mesh contenente il testo specificato, usando il tipo di carattere associato al contesto di dispositivo.
ms.assetid: 1c8b0dc6-51b8-45bf-b4c0-b67e3d128097
title: Funzione D3DXCreateText (D3dx9shape. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateText
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4f6202a534dde727e21b6513ad30077f2e3b3e52
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322724"
---
# <a name="d3dxcreatetext-function"></a><span data-ttu-id="6af5c-103">D3DXCreateText (funzione)</span><span class="sxs-lookup"><span data-stu-id="6af5c-103">D3DXCreateText function</span></span>

<span data-ttu-id="6af5c-104">Crea una mesh contenente il testo specificato, usando il tipo di carattere associato al contesto di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6af5c-104">Creates a mesh containing the specified text, using the font associated with the device context.</span></span>

## <a name="syntax"></a><span data-ttu-id="6af5c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6af5c-105">Syntax</span></span>


```C++
HRESULT D3DXCreateText(
  _In_  LPDIRECT3DDEVICE9   pDevice,
  _In_  HDC                 hDC,
  _In_  LPCTSTR             pText,
  _In_  FLOAT               Deviation,
  _In_  FLOAT               Extrusion,
  _Out_ LPD3DXMESH          *ppMesh,
  _Out_ LPD3DXBUFFER        *ppAdjacency,
  _Out_ LPGLYPHMETRICSFLOAT pGlyphMetrics
);
```



## <a name="parameters"></a><span data-ttu-id="6af5c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6af5c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6af5c-107">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6af5c-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6af5c-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="6af5c-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="6af5c-109">Puntatore al dispositivo che ha creato la mesh.</span><span class="sxs-lookup"><span data-stu-id="6af5c-109">Pointer to the device that created the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="6af5c-110">*HDC* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6af5c-110">*hDC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6af5c-111">Tipo: **HDC**</span><span class="sxs-lookup"><span data-stu-id="6af5c-111">Type: **HDC**</span></span>

<span data-ttu-id="6af5c-112">Contesto di dispositivo, contenente il tipo di carattere per l'output.</span><span class="sxs-lookup"><span data-stu-id="6af5c-112">Device context, containing the font for output.</span></span> <span data-ttu-id="6af5c-113">Il tipo di carattere selezionato dal contesto di dispositivo deve essere un tipo di carattere TrueType.</span><span class="sxs-lookup"><span data-stu-id="6af5c-113">The font selected by the device context must be a TrueType font.</span></span>

</dd> <dt>

<span data-ttu-id="6af5c-114">*ptext* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6af5c-114">*pText* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6af5c-115">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6af5c-115">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6af5c-116">Puntatore a una stringa che specifica il testo da generare.</span><span class="sxs-lookup"><span data-stu-id="6af5c-116">Pointer to a string that specifies the text to generate.</span></span> <span data-ttu-id="6af5c-117">Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="6af5c-117">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="6af5c-118">In caso contrario, il tipo di dati String viene risolto in LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="6af5c-118">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="6af5c-119">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="6af5c-119">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="6af5c-120">*Deviazione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6af5c-120">*Deviation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6af5c-121">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6af5c-121">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6af5c-122">Deviazione massima delle linee dei tipi di carattere TrueType.</span><span class="sxs-lookup"><span data-stu-id="6af5c-122">Maximum chordal deviation from TrueType font outlines.</span></span>

</dd> <dt>

<span data-ttu-id="6af5c-123">*Estrusione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6af5c-123">*Extrusion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6af5c-124">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6af5c-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6af5c-125">Quantità per estrudere il testo nella direzione della z negativa.</span><span class="sxs-lookup"><span data-stu-id="6af5c-125">Amount to extrude text in the negative z-direction.</span></span>

</dd> <dt>

<span data-ttu-id="6af5c-126">*ppMesh* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="6af5c-126">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6af5c-127">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="6af5c-127">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="6af5c-128">Puntatore alla mesh restituita.</span><span class="sxs-lookup"><span data-stu-id="6af5c-128">Pointer to the returned mesh.</span></span>

</dd> <dt>

<span data-ttu-id="6af5c-129">*ppAdjacency* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="6af5c-129">*ppAdjacency* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6af5c-130">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="6af5c-130">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="6af5c-131">Puntatore a un buffer contenente le informazioni adiacenza.</span><span class="sxs-lookup"><span data-stu-id="6af5c-131">Pointer to a buffer containing adjacency information.</span></span> <span data-ttu-id="6af5c-132">Può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="6af5c-132">May be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="6af5c-133">*pGlyphMetrics* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="6af5c-133">*pGlyphMetrics* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6af5c-134">Tipo: **[ **LPGLYPHMETRICSFLOAT**](/windows/win32/api/wingdi/ns-wingdi-glyphmetricsfloat)**</span><span class="sxs-lookup"><span data-stu-id="6af5c-134">Type: **[**LPGLYPHMETRICSFLOAT**](/windows/win32/api/wingdi/ns-wingdi-glyphmetricsfloat)**</span></span>

<span data-ttu-id="6af5c-135">Puntatore a una matrice di strutture [**GLYPHMETRICSFLOAT**](/windows/win32/api/wingdi/ns-wingdi-glyphmetricsfloat) che contengono i dati della metrica del glifo.</span><span class="sxs-lookup"><span data-stu-id="6af5c-135">Pointer to an array of [**GLYPHMETRICSFLOAT**](/windows/win32/api/wingdi/ns-wingdi-glyphmetricsfloat) structures that contain the glyph metric data.</span></span> <span data-ttu-id="6af5c-136">Ogni elemento contiene informazioni sulla posizione e sull'orientamento del glifo corrispondente nella stringa.</span><span class="sxs-lookup"><span data-stu-id="6af5c-136">Each element contains information about the position and orientation of the corresponding glyph in the string.</span></span> <span data-ttu-id="6af5c-137">Il numero di elementi nella matrice deve essere uguale al numero di caratteri nella stringa.</span><span class="sxs-lookup"><span data-stu-id="6af5c-137">The number of elements in the array should be equal to the number of characters in the string.</span></span> <span data-ttu-id="6af5c-138">Si noti che l'origine in ogni struttura non è relativa all'intera stringa, bensì è relativa a tale cella di caratteri.</span><span class="sxs-lookup"><span data-stu-id="6af5c-138">Note that the origin in each structure is not relative to the entire string, but rather is relative to that character cell.</span></span> <span data-ttu-id="6af5c-139">Per calcolare l'intero rettangolo di delimitazione, aggiungere l'incremento per ogni glifo durante l'attraversamento della stringa.</span><span class="sxs-lookup"><span data-stu-id="6af5c-139">To compute the entire bounding box, add the increment for each glyph while traversing the string.</span></span> <span data-ttu-id="6af5c-140">Se non si è interessati alle dimensioni del glifo, impostare questo parametro su **null**.</span><span class="sxs-lookup"><span data-stu-id="6af5c-140">If you are not concerned with the glyph sizes, set this parameter to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6af5c-141">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6af5c-141">Return value</span></span>

<span data-ttu-id="6af5c-142">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6af5c-142">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6af5c-143">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6af5c-143">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="6af5c-144">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="6af5c-144">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="6af5c-145">Commenti</span><span class="sxs-lookup"><span data-stu-id="6af5c-145">Remarks</span></span>

<span data-ttu-id="6af5c-146">L'impostazione del compilatore determina anche la versione della funzione.</span><span class="sxs-lookup"><span data-stu-id="6af5c-146">The compiler setting also determines the function version.</span></span> <span data-ttu-id="6af5c-147">Se è definito Unicode, la chiamata di funzione viene risolta in D3DXCreateTextW.</span><span class="sxs-lookup"><span data-stu-id="6af5c-147">If Unicode is defined, the function call resolves to D3DXCreateTextW.</span></span> <span data-ttu-id="6af5c-148">In caso contrario, la chiamata di funzione viene risolta in D3DXCreateTextA perché vengono utilizzate le stringhe ANSI.</span><span class="sxs-lookup"><span data-stu-id="6af5c-148">Otherwise, the function call resolves to D3DXCreateTextA because ANSI strings are being used.</span></span>

<span data-ttu-id="6af5c-149">Questa funzione crea una mesh con l' \_ opzione di creazione gestita D3DXMESH e [D3DFVF \_ xyz \| D3DFVF \_ Normal](d3dfvf.md) Flexible Vertex Format (FVF).</span><span class="sxs-lookup"><span data-stu-id="6af5c-149">This function creates a mesh with the D3DXMESH\_MANAGED creation option and [D3DFVF\_XYZ \| D3DFVF\_NORMAL](d3dfvf.md) flexible vertex format (FVF).</span></span>

## <a name="requirements"></a><span data-ttu-id="6af5c-150">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6af5c-150">Requirements</span></span>



| <span data-ttu-id="6af5c-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="6af5c-151">Requirement</span></span> | <span data-ttu-id="6af5c-152">Valore</span><span class="sxs-lookup"><span data-stu-id="6af5c-152">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6af5c-153">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6af5c-153">Header</span></span><br/>  | <dl> <span data-ttu-id="6af5c-154"><dt>D3dx9shape. h</dt></span><span class="sxs-lookup"><span data-stu-id="6af5c-154"><dt>D3dx9shape.h</dt></span></span> </dl> |
| <span data-ttu-id="6af5c-155">Libreria</span><span class="sxs-lookup"><span data-stu-id="6af5c-155">Library</span></span><br/> | <dl> <span data-ttu-id="6af5c-156"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6af5c-156"><dt>D3dx9.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="6af5c-157">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6af5c-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6af5c-158">Funzioni di disegno di forme</span><span class="sxs-lookup"><span data-stu-id="6af5c-158">Shape Drawing Functions</span></span>](dx9-graphics-reference-d3dx-functions-shape.md)
</dt> </dl>

 

 
