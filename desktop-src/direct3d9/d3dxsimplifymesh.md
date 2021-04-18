---
description: Genera una mesh semplificata usando i pesi specificati che sono più vicini possibile al valore MinValue specificato.
ms.assetid: 589356a9-f272-4851-92ae-54dbecc0b234
title: Funzione D3DXSimplifyMesh (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSimplifyMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0258047631a41e31d108ba45531988e4cb6a35ae
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322586"
---
# <a name="d3dxsimplifymesh-function"></a><span data-ttu-id="42b0f-103">D3DXSimplifyMesh (funzione)</span><span class="sxs-lookup"><span data-stu-id="42b0f-103">D3DXSimplifyMesh function</span></span>

<span data-ttu-id="42b0f-104">Genera una mesh semplificata usando i pesi specificati che sono più vicini possibile al valore MinValue specificato.</span><span class="sxs-lookup"><span data-stu-id="42b0f-104">Generates a simplified mesh using the provided weights that come as close as possible to the given MinValue.</span></span>

## <a name="syntax"></a><span data-ttu-id="42b0f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="42b0f-105">Syntax</span></span>


```C++
HRESULT D3DXSimplifyMesh(
  _In_        LPD3DXMESH           pMesh,
  _In_  const DWORD                *pAdjacency,
  _In_  const D3DXATTRIBUTEWEIGHTS *pVertexAttributeWeights,
  _In_  const FLOAT                *pVertexWeights,
  _In_        DWORD                MinValue,
  _In_        DWORD                Options,
  _Out_       LPD3DXMESH           *ppMesh
);
```



## <a name="parameters"></a><span data-ttu-id="42b0f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="42b0f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42b0f-107">*pMesh* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="42b0f-107">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42b0f-108">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="42b0f-108">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="42b0f-109">Puntatore a un'interfaccia [**ID3DXMesh**](id3dxmesh.md) , che rappresenta la mesh di origine.</span><span class="sxs-lookup"><span data-stu-id="42b0f-109">Pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the source mesh.</span></span>

</dd> <dt>

<span data-ttu-id="42b0f-110">*pAdjacency* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="42b0f-110">*pAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42b0f-111">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="42b0f-111">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="42b0f-112">Puntatore a una matrice di tre DWORD per volto che specificano i tre elementi adiacenti per ogni viso nella mesh da semplificare.</span><span class="sxs-lookup"><span data-stu-id="42b0f-112">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the mesh to be simplified.</span></span>

</dd> <dt>

<span data-ttu-id="42b0f-113">*pVertexAttributeWeights* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="42b0f-113">*pVertexAttributeWeights* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42b0f-114">Tipo: **const [**D3DXATTRIBUTEWEIGHTS**](d3dxattributeweights.md) \***</span><span class="sxs-lookup"><span data-stu-id="42b0f-114">Type: **const [**D3DXATTRIBUTEWEIGHTS**](d3dxattributeweights.md)\***</span></span>

<span data-ttu-id="42b0f-115">Puntatore a una struttura [**D3DXATTRIBUTEWEIGHTS**](d3dxattributeweights.md) contenente il peso per ogni componente del vertice.</span><span class="sxs-lookup"><span data-stu-id="42b0f-115">Pointer to a [**D3DXATTRIBUTEWEIGHTS**](d3dxattributeweights.md) structure, containing the weight for each vertex component.</span></span> <span data-ttu-id="42b0f-116">Se questo parametro è impostato su **null**, viene utilizzata una struttura predefinita.</span><span class="sxs-lookup"><span data-stu-id="42b0f-116">If this parameter is set to **NULL**, a default structure is used.</span></span> <span data-ttu-id="42b0f-117">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="42b0f-117">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="42b0f-118">*pVertexWeights* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="42b0f-118">*pVertexWeights* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42b0f-119">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="42b0f-119">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="42b0f-120">Puntatore a una matrice di pesi dei vertici.</span><span class="sxs-lookup"><span data-stu-id="42b0f-120">Pointer to an array of vertex weights.</span></span> <span data-ttu-id="42b0f-121">Se questo parametro è impostato su **null**, tutti i pesi dei vertici vengono impostati su 1,0.</span><span class="sxs-lookup"><span data-stu-id="42b0f-121">If this parameter is set to **NULL**, all vertex weights are set to 1.0.</span></span>

</dd> <dt>

<span data-ttu-id="42b0f-122">*MinValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="42b0f-122">*MinValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42b0f-123">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="42b0f-123">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="42b0f-124">Numero di vertici o visi, a seconda del flag impostato nel parametro *options* , in base al quale è possibile semplificare la mesh di origine.</span><span class="sxs-lookup"><span data-stu-id="42b0f-124">Number of vertices or faces, depending on the flag set in the *Options* parameter, by which to simplify the source mesh.</span></span>

</dd> <dt>

<span data-ttu-id="42b0f-125">*Opzioni* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="42b0f-125">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42b0f-126">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="42b0f-126">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="42b0f-127">Specifica le opzioni di semplificazione per la mesh.</span><span class="sxs-lookup"><span data-stu-id="42b0f-127">Specifies simplification options for the mesh.</span></span> <span data-ttu-id="42b0f-128">È possibile impostare uno dei flag in [**D3DXMESHSIMP**](./d3dxmeshsimp.md) .</span><span class="sxs-lookup"><span data-stu-id="42b0f-128">One of the flags in [**D3DXMESHSIMP**](./d3dxmeshsimp.md) can be set.</span></span>

</dd> <dt>

<span data-ttu-id="42b0f-129">*ppMesh* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="42b0f-129">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="42b0f-130">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="42b0f-130">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="42b0f-131">Indirizzo di un puntatore a un'interfaccia [**ID3DXMesh**](id3dxmesh.md) , che rappresenta la mesh di semplificazione restituita.</span><span class="sxs-lookup"><span data-stu-id="42b0f-131">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the returned simplification mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42b0f-132">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="42b0f-132">Return value</span></span>

<span data-ttu-id="42b0f-133">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="42b0f-133">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="42b0f-134">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="42b0f-134">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="42b0f-135">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="42b0f-135">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="42b0f-136">Commenti</span><span class="sxs-lookup"><span data-stu-id="42b0f-136">Remarks</span></span>

<span data-ttu-id="42b0f-137">Questa funzione genera una mesh con vertici o visi *MinValue* .</span><span class="sxs-lookup"><span data-stu-id="42b0f-137">This function generates a mesh that has *MinValue* vertices or faces.</span></span>

<span data-ttu-id="42b0f-138">Se il processo di semplificazione non è in grado di ridurre la mesh a *MinValue*, la chiamata ha ancora esito positivo perché *MinValue* è un valore minimo desiderato, non un valore minimo assoluto.</span><span class="sxs-lookup"><span data-stu-id="42b0f-138">If the simplification process cannot reduce the mesh to *MinValue*, the call still succeeds because *MinValue* is a desired minimum, not an absolute minimum.</span></span>

<span data-ttu-id="42b0f-139">Se *pVertexAttributeWeights* è impostato su **null**, alla struttura [**D3DXATTRIBUTEWEIGHTS**](d3dxattributeweights.md) predefinita vengono assegnati i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="42b0f-139">If *pVertexAttributeWeights* is set to **NULL**, the following values are assigned to the default [**D3DXATTRIBUTEWEIGHTS**](d3dxattributeweights.md) structure.</span></span>


```
D3DXATTRIBUTEWEIGHTS AttributeWeights;
    
AttributeWeights.Position  = 1.0;
AttributeWeights.Boundary =  1.0;
AttributeWeights.Normal   =  1.0;
AttributeWeights.Diffuse  =  0.0;
AttributeWeights.Specular =  0.0;
AttributeWeights.Tex[8]   =  {0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0};
```



<span data-ttu-id="42b0f-140">Questa struttura predefinita è quella che la maggior parte delle applicazioni deve usare perché considera solo la regolazione geometrica e normale.</span><span class="sxs-lookup"><span data-stu-id="42b0f-140">This default structure is what most applications should use because it considers only geometric and normal adjustment.</span></span> <span data-ttu-id="42b0f-141">Solo in casi particolari è necessario modificare gli altri campi dei membri.</span><span class="sxs-lookup"><span data-stu-id="42b0f-141">Only in special cases will the other member fields need to be modified.</span></span>

## <a name="requirements"></a><span data-ttu-id="42b0f-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="42b0f-142">Requirements</span></span>



| <span data-ttu-id="42b0f-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="42b0f-143">Requirement</span></span> | <span data-ttu-id="42b0f-144">Valore</span><span class="sxs-lookup"><span data-stu-id="42b0f-144">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="42b0f-145">Intestazione</span><span class="sxs-lookup"><span data-stu-id="42b0f-145">Header</span></span><br/>  | <dl> <span data-ttu-id="42b0f-146"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="42b0f-146"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="42b0f-147">Libreria</span><span class="sxs-lookup"><span data-stu-id="42b0f-147">Library</span></span><br/> | <dl> <span data-ttu-id="42b0f-148"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="42b0f-148"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="42b0f-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="42b0f-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42b0f-150">Funzioni mesh</span><span class="sxs-lookup"><span data-stu-id="42b0f-150">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
