---
description: Disegna un subset di una mesh.
ms.assetid: 99eaa185-b681-47f2-aed8-5ca1697ff73c
title: Metodo ID3DXBaseMesh::D rawSubset (D3DX9Mesh. h)
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
ms.openlocfilehash: d0da6e9fc57e0fc5e7b4b263ba3d97185333881c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322552"
---
# <a name="id3dxbasemeshdrawsubset-method"></a><span data-ttu-id="ee670-103">ID3DXBaseMesh::D Metodo rawSubset</span><span class="sxs-lookup"><span data-stu-id="ee670-103">ID3DXBaseMesh::DrawSubset method</span></span>

<span data-ttu-id="ee670-104">Disegna un subset di una mesh.</span><span class="sxs-lookup"><span data-stu-id="ee670-104">Draws a subset of a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee670-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ee670-105">Syntax</span></span>


```C++
HRESULT DrawSubset(
  [in] DWORD AttribId
);
```



## <a name="parameters"></a><span data-ttu-id="ee670-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ee670-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee670-107">*AttribId* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ee670-107">*AttribId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee670-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ee670-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ee670-109">DWORD che specifica il subset della mesh da creare.</span><span class="sxs-lookup"><span data-stu-id="ee670-109">DWORD that specifies which subset of the mesh to draw.</span></span> <span data-ttu-id="ee670-110">Questo valore viene utilizzato per distinguere i visi in una mesh come appartenenti a uno o più gruppi di attributi.</span><span class="sxs-lookup"><span data-stu-id="ee670-110">This value is used to differentiate faces in a mesh as belonging to one or more attribute groups.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee670-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ee670-111">Return value</span></span>

<span data-ttu-id="ee670-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ee670-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ee670-113">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ee670-113">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ee670-114">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="ee670-114">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee670-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="ee670-115">Remarks</span></span>

<span data-ttu-id="ee670-116">Il sottoinsieme specificato da AttribId verrà sottoposto a rendering dal metodo [**IDirect3DDevice9::D rawindexedprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) , usando il \_ tipo PRIMItivo triangolico D3DPT, in modo che un buffer di indice deve essere inizializzato correttamente.</span><span class="sxs-lookup"><span data-stu-id="ee670-116">The subset that is specified by AttribId will be rendered by the [**IDirect3DDevice9::DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) method, using the D3DPT\_TRIANGLELIST primitive type, so an index buffer must be properly initialized.</span></span>

<span data-ttu-id="ee670-117">Una tabella degli attributi viene utilizzata per identificare le aree della mesh che devono essere disegnate con trame, Stati di rendering, materiali e così via.</span><span class="sxs-lookup"><span data-stu-id="ee670-117">An attribute table is used to identify areas of the mesh that need to be drawn with different textures, render states, materials, and so on.</span></span> <span data-ttu-id="ee670-118">Inoltre, l'applicazione può usare la tabella attribute per nascondere parti di una mesh senza disegnare un identificatore di attributo specificato (*AttribId*) durante il disegno del frame.</span><span class="sxs-lookup"><span data-stu-id="ee670-118">In addition, the application can use the attribute table to hide portions of a mesh by not drawing a given attribute identifier (*AttribId*) when drawing the frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee670-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ee670-119">Requirements</span></span>



| <span data-ttu-id="ee670-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee670-120">Requirement</span></span> | <span data-ttu-id="ee670-121">Valore</span><span class="sxs-lookup"><span data-stu-id="ee670-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ee670-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ee670-122">Header</span></span><br/>  | <dl> <span data-ttu-id="ee670-123"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee670-123"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="ee670-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="ee670-124">Library</span></span><br/> | <dl> <span data-ttu-id="ee670-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ee670-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ee670-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ee670-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee670-127">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="ee670-127">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
