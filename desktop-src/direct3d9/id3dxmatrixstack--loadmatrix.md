---
description: Carica la matrice specificata nella matrice corrente.
ms.assetid: c4c5ac50-238f-4b41-8ea9-7e48ffd03fc5
title: 'Metodo ID3DXMATRIXStack:: LoadMatrix (D3dx9math. h)'
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 292b4e147dfa99023f0b4d560a4ed41e6b41b3fe
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530859"
---
# <a name="id3dxmatrixstackloadmatrix-method-d3dx9mathh"></a><span data-ttu-id="e3c03-103">Metodo ID3DXMATRIXStack:: LoadMatrix (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="e3c03-103">ID3DXMATRIXStack::LoadMatrix method (D3dx9math.h)</span></span>

<span data-ttu-id="e3c03-104">Carica la matrice specificata nella matrice corrente.</span><span class="sxs-lookup"><span data-stu-id="e3c03-104">Loads the given matrix into the current matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3c03-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e3c03-105">Syntax</span></span>


```C++
HRESULT LoadMatrix(
  [in] const D3DXMATRIX *pMat
);
```



## <a name="parameters"></a><span data-ttu-id="e3c03-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e3c03-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3c03-107">*pMat* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e3c03-107">*pMat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3c03-108">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="e3c03-108">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="e3c03-109">Puntatore alla struttura [**D3DXMATRIX**](d3dxmatrix.md) caricata nella matrice corrente.</span><span class="sxs-lookup"><span data-stu-id="e3c03-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure loaded into the current matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3c03-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e3c03-110">Return value</span></span>

<span data-ttu-id="e3c03-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e3c03-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e3c03-112">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e3c03-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e3c03-113">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="e3c03-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3c03-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="e3c03-114">Remarks</span></span>

<span data-ttu-id="e3c03-115">Si noti che questo metodo non aggiunge un elemento allo stack; sostituisce invece la matrice corrente con la matrice fornita.</span><span class="sxs-lookup"><span data-stu-id="e3c03-115">Note that this method does not add an item to the stack; rather, it replaces the current matrix with the supplied matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3c03-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e3c03-116">Requirements</span></span>



| <span data-ttu-id="e3c03-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3c03-117">Requirement</span></span> | <span data-ttu-id="e3c03-118">Valore</span><span class="sxs-lookup"><span data-stu-id="e3c03-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e3c03-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e3c03-119">Header</span></span><br/>  | <dl> <span data-ttu-id="e3c03-120"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3c03-120"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="e3c03-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="e3c03-121">Library</span></span><br/> | <dl> <span data-ttu-id="e3c03-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e3c03-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e3c03-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e3c03-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3c03-124">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="e3c03-124">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="e3c03-125">**ID3DXMATRIXStack::LoadIdentity**</span><span class="sxs-lookup"><span data-stu-id="e3c03-125">**ID3DXMATRIXStack::LoadIdentity**</span></span>](id3dxmatrixstack--loadidentity.md)
</dt> </dl>

 

 




