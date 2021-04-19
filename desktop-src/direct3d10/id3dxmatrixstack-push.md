---
description: Aggiunge una matrice allo stack.
ms.assetid: 8660047f-64bc-4b34-8270-3087412db942
title: Metodo ID3DXMATRIXStack::P USH (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.Push
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 694bb8b02f340be14f38b7d2a44ec2038d175098
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323660"
---
# <a name="id3dxmatrixstackpush-method-d3dx10h"></a><span data-ttu-id="69c4c-103">Metodo ID3DXMATRIXStack::P USH (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="69c4c-103">ID3DXMATRIXStack::Push method (D3DX10.h)</span></span>

<span data-ttu-id="69c4c-104">Aggiunge una matrice allo stack.</span><span class="sxs-lookup"><span data-stu-id="69c4c-104">Adds a matrix to the stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="69c4c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="69c4c-105">Syntax</span></span>


```C++
HRESULT Push();
```



## <a name="parameters"></a><span data-ttu-id="69c4c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="69c4c-106">Parameters</span></span>

<span data-ttu-id="69c4c-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="69c4c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="69c4c-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="69c4c-108">Return value</span></span>

<span data-ttu-id="69c4c-109">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="69c4c-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="69c4c-110">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="69c4c-110">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="69c4c-111">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="69c4c-111">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="69c4c-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="69c4c-112">Remarks</span></span>

<span data-ttu-id="69c4c-113">Questo metodo incrementa il numero di elementi nello stack di 1, duplicando la matrice corrente.</span><span class="sxs-lookup"><span data-stu-id="69c4c-113">This method increments the count of items on the stack by 1, duplicating the current matrix.</span></span> <span data-ttu-id="69c4c-114">Lo stack aumenterà in modo dinamico man mano che vengono aggiunti altri elementi.</span><span class="sxs-lookup"><span data-stu-id="69c4c-114">The stack will grow dynamically as more items are added.</span></span>

## <a name="requirements"></a><span data-ttu-id="69c4c-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="69c4c-115">Requirements</span></span>



| <span data-ttu-id="69c4c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="69c4c-116">Requirement</span></span> | <span data-ttu-id="69c4c-117">Valore</span><span class="sxs-lookup"><span data-stu-id="69c4c-117">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="69c4c-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="69c4c-118">Header</span></span><br/>  | <dl> <span data-ttu-id="69c4c-119"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="69c4c-119"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="69c4c-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="69c4c-120">Library</span></span><br/> | <dl> <span data-ttu-id="69c4c-121"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="69c4c-121"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69c4c-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="69c4c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69c4c-123">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="69c4c-123">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="69c4c-124">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="69c4c-124">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




