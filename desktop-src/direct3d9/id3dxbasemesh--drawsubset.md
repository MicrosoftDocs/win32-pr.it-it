---
description: 'Metodo ID3DXBaseMesh::D rawSubset: disegna un subset di una mesh.'
ms.assetid: 99eaa185-b681-47f2-aed8-5ca1697ff73c
title: Metodo ID3DXBaseMesh::D rawSubset (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.DrawSubset
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 252c9b9921c7eafd8f0c2a54cfa14a85e91b8f7d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115469"
---
# <a name="id3dxbasemeshdrawsubset-method"></a><span data-ttu-id="b5214-103">Metodo ID3DXBaseMesh::D rawSubset</span><span class="sxs-lookup"><span data-stu-id="b5214-103">ID3DXBaseMesh::DrawSubset method</span></span>

<span data-ttu-id="b5214-104">Disegna un subset di una mesh.</span><span class="sxs-lookup"><span data-stu-id="b5214-104">Draws a subset of a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5214-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b5214-105">Syntax</span></span>


```C++
HRESULT DrawSubset(
  [in] DWORD AttribId
);
```



## <a name="parameters"></a><span data-ttu-id="b5214-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b5214-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5214-107">*AttribId* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="b5214-107">*AttribId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5214-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b5214-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b5214-109">Valore DWORD che specifica il subset della mesh da disegnare.</span><span class="sxs-lookup"><span data-stu-id="b5214-109">DWORD that specifies which subset of the mesh to draw.</span></span> <span data-ttu-id="b5214-110">Questo valore viene usato per distinguere i visi in una mesh come appartenenti a uno o più gruppi di attributi.</span><span class="sxs-lookup"><span data-stu-id="b5214-110">This value is used to differentiate faces in a mesh as belonging to one or more attribute groups.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5214-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b5214-111">Return value</span></span>

<span data-ttu-id="b5214-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b5214-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b5214-113">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b5214-113">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b5214-114">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="b5214-114">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5214-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="b5214-115">Remarks</span></span>

<span data-ttu-id="b5214-116">Il subset specificato da AttribId verrà sottoposto a rendering dal metodo [**IDirect3DDevice9::D rawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) usando il tipo primitivo D3DPT TRIANGLELIST, quindi un index buffer deve essere inizializzato \_ correttamente.</span><span class="sxs-lookup"><span data-stu-id="b5214-116">The subset that is specified by AttribId will be rendered by the [**IDirect3DDevice9::DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) method, using the D3DPT\_TRIANGLELIST primitive type, so an index buffer must be properly initialized.</span></span>

<span data-ttu-id="b5214-117">Una tabella di attributi viene usata per identificare le aree della mesh che devono essere disegnate con trame, stati di rendering, materiali e così via diversi.</span><span class="sxs-lookup"><span data-stu-id="b5214-117">An attribute table is used to identify areas of the mesh that need to be drawn with different textures, render states, materials, and so on.</span></span> <span data-ttu-id="b5214-118">Inoltre, l'applicazione può usare la tabella degli attributi per nascondere parti di una mesh non disegnando un identificatore di attributo specificato (*AttribId*) durante il disegno del frame.</span><span class="sxs-lookup"><span data-stu-id="b5214-118">In addition, the application can use the attribute table to hide portions of a mesh by not drawing a given attribute identifier (*AttribId*) when drawing the frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5214-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b5214-119">Requirements</span></span>



| <span data-ttu-id="b5214-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5214-120">Requirement</span></span> | <span data-ttu-id="b5214-121">Valore</span><span class="sxs-lookup"><span data-stu-id="b5214-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b5214-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b5214-122">Header</span></span><br/>  | <dl> <span data-ttu-id="b5214-123"><dt>D3DX9Mesh.h</dt></span><span class="sxs-lookup"><span data-stu-id="b5214-123"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="b5214-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="b5214-124">Library</span></span><br/> | <dl> <span data-ttu-id="b5214-125"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="b5214-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b5214-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b5214-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5214-127">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="b5214-127">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
