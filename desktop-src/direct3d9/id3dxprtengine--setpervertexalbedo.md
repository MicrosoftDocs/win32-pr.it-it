---
description: Imposta un valore albedo per ogni vertice mesh, sovrascrivendo i valori albedo precedenti.
ms.assetid: 5220dfe3-8d41-480c-a850-b9aad3d2bb2f
title: 'Metodo ID3DXPRTEngine:: SetPerVertexAlbedo (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetPerVertexAlbedo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: da7a33a79cc50963e87d0eff15baf22ee8d79ce3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322975"
---
# <a name="id3dxprtenginesetpervertexalbedo-method"></a><span data-ttu-id="a0263-103">Metodo ID3DXPRTEngine:: SetPerVertexAlbedo</span><span class="sxs-lookup"><span data-stu-id="a0263-103">ID3DXPRTEngine::SetPerVertexAlbedo method</span></span>

<span data-ttu-id="a0263-104">Imposta un valore albedo per ogni vertice mesh, sovrascrivendo i valori albedo precedenti.</span><span class="sxs-lookup"><span data-stu-id="a0263-104">Sets an albedo value for each mesh vertex, overwriting previous albedo values.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0263-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a0263-105">Syntax</span></span>


```C++
HRESULT SetPerVertexAlbedo(
  [in] const VOID *pDataIn,
  [in]       UINT NumChannels,
  [in]       UINT Stride
);
```



## <a name="parameters"></a><span data-ttu-id="a0263-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a0263-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0263-107">*pDataIn* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a0263-107">*pDataIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0263-108">Tipo: **const \* void**</span><span class="sxs-lookup"><span data-stu-id="a0263-108">Type: **const VOID\***</span></span>

<span data-ttu-id="a0263-109">Puntatore ai dati di albedo FLOAT del primo campione.</span><span class="sxs-lookup"><span data-stu-id="a0263-109">Pointer to FLOAT albedo data of the first sample.</span></span>

</dd> <dt>

<span data-ttu-id="a0263-110">*NumChannels* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a0263-110">*NumChannels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0263-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a0263-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a0263-112">Numero di canali dei colori da impostare.</span><span class="sxs-lookup"><span data-stu-id="a0263-112">Number of color channels to set.</span></span> <span data-ttu-id="a0263-113">Impostare su 1 per specificare i materiali grigi (R = G = B) o 3 per abilitare gli effetti di emorragia del colore.</span><span class="sxs-lookup"><span data-stu-id="a0263-113">Set to 1 to specify gray materials (R = G = B), or 3 to enable color bleeding effects.</span></span>

</dd> <dt>

<span data-ttu-id="a0263-114">*Stride* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a0263-114">*Stride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0263-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a0263-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a0263-116">Stride in byte necessario per ottenere il valore albedo del campione successivo.</span><span class="sxs-lookup"><span data-stu-id="a0263-116">Stride in bytes needed to get to next sample's albedo value.</span></span> <span data-ttu-id="a0263-117">Vedere [Width e pitch (Direct3D 9)](width-vs--pitch.md).</span><span class="sxs-lookup"><span data-stu-id="a0263-117">See [Width vs. Pitch (Direct3D 9)](width-vs--pitch.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0263-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a0263-118">Return value</span></span>

<span data-ttu-id="a0263-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a0263-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a0263-120">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a0263-120">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="a0263-121">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="a0263-121">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0263-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a0263-122">Requirements</span></span>



| <span data-ttu-id="a0263-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0263-123">Requirement</span></span> | <span data-ttu-id="a0263-124">Valore</span><span class="sxs-lookup"><span data-stu-id="a0263-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a0263-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a0263-125">Header</span></span><br/>  | <dl> <span data-ttu-id="a0263-126"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0263-126"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="a0263-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="a0263-127">Library</span></span><br/> | <dl> <span data-ttu-id="a0263-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a0263-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a0263-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a0263-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0263-130">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="a0263-130">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 
