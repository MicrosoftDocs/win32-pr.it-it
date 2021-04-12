---
description: Carica la matrice specificata nella matrice corrente.
ms.assetid: b898f344-db90-48e0-b457-0eb8d7b31dca
title: 'Metodo ID3DXMATRIXStack:: LoadMatrix (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.LoadMatrix
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: ce6b99abf4c9a82a8b9d1c7643a1098d19e18c15
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104356014"
---
# <a name="id3dxmatrixstackloadmatrix-method-d3dx10h"></a><span data-ttu-id="4cb8f-103">Metodo ID3DXMATRIXStack:: LoadMatrix (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="4cb8f-103">ID3DXMATRIXStack::LoadMatrix method (D3DX10.h)</span></span>

<span data-ttu-id="4cb8f-104">Carica la matrice specificata nella matrice corrente.</span><span class="sxs-lookup"><span data-stu-id="4cb8f-104">Loads the given matrix into the current matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="4cb8f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4cb8f-105">Syntax</span></span>


```C++
HRESULT LoadMatrix(
  [in] const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="4cb8f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4cb8f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4cb8f-107">*PM* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4cb8f-107">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4cb8f-108">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="4cb8f-108">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="4cb8f-109">Puntatore alla struttura D3DXMATRIX caricata nella matrice corrente.</span><span class="sxs-lookup"><span data-stu-id="4cb8f-109">Pointer to the D3DXMATRIX structure loaded into the current matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4cb8f-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4cb8f-110">Return value</span></span>

<span data-ttu-id="4cb8f-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4cb8f-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4cb8f-112">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4cb8f-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="4cb8f-113">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="4cb8f-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="4cb8f-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="4cb8f-114">Remarks</span></span>

<span data-ttu-id="4cb8f-115">Si noti che questo metodo non aggiunge un elemento allo stack; sostituisce invece la matrice corrente con la matrice fornita.</span><span class="sxs-lookup"><span data-stu-id="4cb8f-115">Note that this method does not add an item to the stack; rather, it replaces the current matrix with the supplied matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="4cb8f-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4cb8f-116">Requirements</span></span>



| <span data-ttu-id="4cb8f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="4cb8f-117">Requirement</span></span> | <span data-ttu-id="4cb8f-118">Valore</span><span class="sxs-lookup"><span data-stu-id="4cb8f-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4cb8f-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4cb8f-119">Header</span></span><br/>  | <dl> <span data-ttu-id="4cb8f-120"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="4cb8f-120"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="4cb8f-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="4cb8f-121">Library</span></span><br/> | <dl> <span data-ttu-id="4cb8f-122"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4cb8f-122"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4cb8f-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4cb8f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cb8f-124">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="4cb8f-124">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="4cb8f-125">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="4cb8f-125">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
