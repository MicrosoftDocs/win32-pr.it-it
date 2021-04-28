---
description: 'Metodo ID3DXMATRIXStack::LoadMatrix (D3dx9math.h): carica la matrice specificata nella matrice corrente.'
ms.assetid: c4c5ac50-238f-4b41-8ea9-7e48ffd03fc5
title: Metodo ID3DXMATRIXStack::LoadMatrix (D3dx9math.h)
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
ms.openlocfilehash: f2ee7e5cae4d28b81b805faa4f113d0819f1eae9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093539"
---
# <a name="id3dxmatrixstackloadmatrix-method-d3dx9mathh"></a><span data-ttu-id="d12a2-103">Metodo ID3DXMATRIXStack::LoadMatrix (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="d12a2-103">ID3DXMATRIXStack::LoadMatrix method (D3dx9math.h)</span></span>

<span data-ttu-id="d12a2-104">Carica la matrice specificata nella matrice corrente.</span><span class="sxs-lookup"><span data-stu-id="d12a2-104">Loads the given matrix into the current matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="d12a2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d12a2-105">Syntax</span></span>


```C++
HRESULT LoadMatrix(
  [in] const D3DXMATRIX *pMat
);
```



## <a name="parameters"></a><span data-ttu-id="d12a2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d12a2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d12a2-107">*pMat* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="d12a2-107">*pMat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d12a2-108">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="d12a2-108">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="d12a2-109">Puntatore alla [**struttura D3DXMATRIX**](d3dxmatrix.md) caricata nella matrice corrente.</span><span class="sxs-lookup"><span data-stu-id="d12a2-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure loaded into the current matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d12a2-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d12a2-110">Return value</span></span>

<span data-ttu-id="d12a2-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d12a2-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d12a2-112">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d12a2-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d12a2-113">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="d12a2-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="d12a2-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="d12a2-114">Remarks</span></span>

<span data-ttu-id="d12a2-115">Si noti che questo metodo non aggiunge un elemento nello stack. sostituisce invece la matrice corrente con la matrice fornita.</span><span class="sxs-lookup"><span data-stu-id="d12a2-115">Note that this method does not add an item to the stack; rather, it replaces the current matrix with the supplied matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="d12a2-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d12a2-116">Requirements</span></span>



| <span data-ttu-id="d12a2-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="d12a2-117">Requirement</span></span> | <span data-ttu-id="d12a2-118">Valore</span><span class="sxs-lookup"><span data-stu-id="d12a2-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d12a2-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d12a2-119">Header</span></span><br/>  | <dl> <span data-ttu-id="d12a2-120"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="d12a2-120"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="d12a2-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="d12a2-121">Library</span></span><br/> | <dl> <span data-ttu-id="d12a2-122"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="d12a2-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d12a2-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d12a2-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d12a2-124">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="d12a2-124">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="d12a2-125">**ID3DXMATRIXStack::LoadIdentity**</span><span class="sxs-lookup"><span data-stu-id="d12a2-125">**ID3DXMATRIXStack::LoadIdentity**</span></span>](id3dxmatrixstack--loadidentity.md)
</dt> </dl>

 

 




