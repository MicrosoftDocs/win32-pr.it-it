---
description: Imposta un vettore normale per ogni Texel in un oggetto trama. Questo metodo viene usato per archiviare i vettori normali dei vertici da una mesh (o le normali del vertice interpolato se viene calcolato il trasferimento di luminosità precalcolata basata su pixel).
ms.assetid: 165a3ef6-c142-4988-b4fb-5aafd8ff11fe
title: 'Metodo ID3DXPRTEngine:: SetPerTexelNormal (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetPerTexelNormal
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5220ad500312792cd158967e9502381f49b0e3e7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104401981"
---
# <a name="id3dxprtenginesetpertexelnormal-method"></a><span data-ttu-id="c0420-104">Metodo ID3DXPRTEngine:: SetPerTexelNormal</span><span class="sxs-lookup"><span data-stu-id="c0420-104">ID3DXPRTEngine::SetPerTexelNormal method</span></span>

<span data-ttu-id="c0420-105">Imposta un vettore normale per ogni Texel in un oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="c0420-105">Sets a normal vector for each texel in a texture object.</span></span> <span data-ttu-id="c0420-106">Questo metodo viene usato per archiviare i vettori normali dei vertici da una mesh (o le normali del vertice interpolato se viene calcolato il trasferimento di luminosità precalcolata basata su pixel).</span><span class="sxs-lookup"><span data-stu-id="c0420-106">This method is used to store vertex normal vectors from a mesh (or interpolated vertex normals if pixel-based precomputed radiance transfer (PRT) is being computed).</span></span>

## <a name="syntax"></a><span data-ttu-id="c0420-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c0420-107">Syntax</span></span>


```C++
HRESULT SetPerTexelNormal(
  [in] LPDIRECT3DTEXTURE9 pNormalTexture
);
```



## <a name="parameters"></a><span data-ttu-id="c0420-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="c0420-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0420-109">*pNormalTexture* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c0420-109">*pNormalTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0420-110">Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="c0420-110">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="c0420-111">Puntatore a un oggetto trama [**IDirect3DTexture9**](/windows/desktop/api) che funge da mappa normale dello spazio degli oggetti in cui archiviare i vettori normali.</span><span class="sxs-lookup"><span data-stu-id="c0420-111">Pointer to an [**IDirect3DTexture9**](/windows/desktop/api) texture object that serves as an object space normal map in which to store normal vectors.</span></span> <span data-ttu-id="c0420-112">La trama deve avere le stesse dimensioni di [**ID3DXPRTBuffer**](id3dxprtbuffer.md) e deve essere in grado di archiviare i formati di trama firmati.</span><span class="sxs-lookup"><span data-stu-id="c0420-112">The texture must have the same dimensions as [**ID3DXPRTBuffer**](id3dxprtbuffer.md) and must be able to store signed texture formats.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0420-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c0420-113">Return value</span></span>

<span data-ttu-id="c0420-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c0420-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c0420-115">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c0420-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="c0420-116">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="c0420-116">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0420-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c0420-117">Requirements</span></span>



| <span data-ttu-id="c0420-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0420-118">Requirement</span></span> | <span data-ttu-id="c0420-119">Valore</span><span class="sxs-lookup"><span data-stu-id="c0420-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c0420-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c0420-120">Header</span></span><br/>  | <dl> <span data-ttu-id="c0420-121"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0420-121"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="c0420-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="c0420-122">Library</span></span><br/> | <dl> <span data-ttu-id="c0420-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c0420-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c0420-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c0420-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0420-125">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="c0420-125">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 
