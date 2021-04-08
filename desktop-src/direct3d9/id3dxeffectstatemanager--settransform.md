---
description: Funzione di callback che deve essere implementata da un utente per impostare una trasformazione.
ms.assetid: 5d886554-ddb6-4b8a-a7fd-453e94b9516f
title: 'Metodo ID3DXEffectStateManager:: setransform (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetTransform
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b19a060cfeb09d5d1a92e5e7a1a1f25b58e64f4d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969416"
---
# <a name="id3dxeffectstatemanagersettransform-method"></a><span data-ttu-id="281c2-103">Metodo ID3DXEffectStateManager:: setransform</span><span class="sxs-lookup"><span data-stu-id="281c2-103">ID3DXEffectStateManager::SetTransform method</span></span>

<span data-ttu-id="281c2-104">Funzione di callback che deve essere implementata da un utente per impostare una trasformazione.</span><span class="sxs-lookup"><span data-stu-id="281c2-104">A callback function that must be implemented by a user to set a transform.</span></span>

## <a name="syntax"></a><span data-ttu-id="281c2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="281c2-105">Syntax</span></span>


```C++
HRESULT SetTransform(
  [in]       D3DTRANSFORMSTATETYPE State,
  [in] const D3DMATRIX             *pMatrix
);
```



## <a name="parameters"></a><span data-ttu-id="281c2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="281c2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="281c2-107">*Stato* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="281c2-107">*State* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="281c2-108">Tipo: **[ **D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md)**</span><span class="sxs-lookup"><span data-stu-id="281c2-108">Type: **[**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md)**</span></span>

<span data-ttu-id="281c2-109">Tipo di trasformazione a cui applicare la matrice.</span><span class="sxs-lookup"><span data-stu-id="281c2-109">The type of transform to apply the matrix to.</span></span> <span data-ttu-id="281c2-110">Vedere [**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md).</span><span class="sxs-lookup"><span data-stu-id="281c2-110">See [**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md).</span></span>

</dd> <dt>

<span data-ttu-id="281c2-111">*pmatrix* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="281c2-111">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="281c2-112">Tipo: **const [**D3DMATRIX**](d3dmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="281c2-112">Type: **const [**D3DMATRIX**](d3dmatrix.md)\***</span></span>

<span data-ttu-id="281c2-113">Matrice di trasformazione.</span><span class="sxs-lookup"><span data-stu-id="281c2-113">A transformation matrix.</span></span> <span data-ttu-id="281c2-114">Vedere [**D3DMATRIX**](d3dmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="281c2-114">See [**D3DMATRIX**](d3dmatrix.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="281c2-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="281c2-115">Return value</span></span>

<span data-ttu-id="281c2-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="281c2-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="281c2-117">Il metodo implementato dall'utente deve restituire S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="281c2-117">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="281c2-118">Se il callback ha esito negativo quando si imposta lo stato del dispositivo, si verificherà una delle condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="281c2-118">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="281c2-119">L'effetto avrà esito negativo durante [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md).</span><span class="sxs-lookup"><span data-stu-id="281c2-119">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="281c2-120">La chiamata allo stato dell'effetto dinamico, ad esempio [**IDirect3DDevice9:: setransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform), avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="281c2-120">The dynamic effect state call (such as [**IDirect3DDevice9::SetTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="281c2-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="281c2-121">Requirements</span></span>



| <span data-ttu-id="281c2-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="281c2-122">Requirement</span></span> | <span data-ttu-id="281c2-123">Valore</span><span class="sxs-lookup"><span data-stu-id="281c2-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="281c2-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="281c2-124">Header</span></span><br/>  | <dl> <span data-ttu-id="281c2-125"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="281c2-125"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="281c2-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="281c2-126">Library</span></span><br/> | <dl> <span data-ttu-id="281c2-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="281c2-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="281c2-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="281c2-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="281c2-129">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="281c2-129">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
