---
description: Termina una scena.
ms.assetid: f721593e-6cba-4569-8276-6a4ffc0fc37a
title: 'Metodo ID3DXRenderToSurface:: EndScene (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToSurface.EndScene
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d5aa0c1fbccb756ac612b813ad151813a782b122
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103761993"
---
# <a name="id3dxrendertosurfaceendscene-method"></a><span data-ttu-id="62451-103">Metodo ID3DXRenderToSurface:: EndScene</span><span class="sxs-lookup"><span data-stu-id="62451-103">ID3DXRenderToSurface::EndScene method</span></span>

<span data-ttu-id="62451-104">Termina una scena.</span><span class="sxs-lookup"><span data-stu-id="62451-104">Ends a scene.</span></span>

## <a name="syntax"></a><span data-ttu-id="62451-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="62451-105">Syntax</span></span>


```C++
HRESULT EndScene(
  [in] DWORD MipFilter
);
```



## <a name="parameters"></a><span data-ttu-id="62451-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="62451-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62451-107">*MipFilter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="62451-107">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62451-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="62451-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="62451-109">Opzioni di filtro, enumerate [nel \_ filtro D3DX](d3dx-filter.md).</span><span class="sxs-lookup"><span data-stu-id="62451-109">Filter options, enumerated in [D3DX\_FILTER](d3dx-filter.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62451-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="62451-110">Return value</span></span>

<span data-ttu-id="62451-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="62451-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="62451-112">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="62451-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="62451-113">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="62451-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="62451-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="62451-114">Requirements</span></span>



| <span data-ttu-id="62451-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="62451-115">Requirement</span></span> | <span data-ttu-id="62451-116">Valore</span><span class="sxs-lookup"><span data-stu-id="62451-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="62451-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="62451-117">Header</span></span><br/>  | <dl> <span data-ttu-id="62451-118"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="62451-118"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="62451-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="62451-119">Library</span></span><br/> | <dl> <span data-ttu-id="62451-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="62451-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="62451-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="62451-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62451-122">ID3DXRenderToSurface</span><span class="sxs-lookup"><span data-stu-id="62451-122">ID3DXRenderToSurface</span></span>](id3dxrendertosurface.md)
</dt> <dt>

[<span data-ttu-id="62451-123">**ID3DXRenderToSurface:: BeginScene**</span><span class="sxs-lookup"><span data-stu-id="62451-123">**ID3DXRenderToSurface::BeginScene**</span></span>](id3dxrendertosurface--beginscene.md)
</dt> </dl>

 

 
