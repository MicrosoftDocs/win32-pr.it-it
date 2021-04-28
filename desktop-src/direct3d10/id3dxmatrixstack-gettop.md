---
description: "Metodo ID3DXMATRIXStack::GetTop (D3DX10.h): recupera la matrice corrente all'inizio dello stack."
ms.assetid: cf379742-3e7d-4309-a7af-b97348428682
title: Metodo ID3DXMATRIXStack::GetTop (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.GetTop
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d1d96cfe8124b47a9b6ce546379af1313a02ea26
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108039"
---
# <a name="id3dxmatrixstackgettop-method-d3dx10h"></a><span data-ttu-id="f9337-103">Metodo ID3DXMATRIXStack::GetTop (D3DX10.h)</span><span class="sxs-lookup"><span data-stu-id="f9337-103">ID3DXMATRIXStack::GetTop method (D3DX10.h)</span></span>

<span data-ttu-id="f9337-104">Recupera la matrice corrente all'inizio dello stack.</span><span class="sxs-lookup"><span data-stu-id="f9337-104">Retrieves the current matrix at the top of the stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9337-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f9337-105">Syntax</span></span>


```C++
D3DXMATRIX* GetTop();
```



## <a name="parameters"></a><span data-ttu-id="f9337-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f9337-106">Parameters</span></span>

<span data-ttu-id="f9337-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="f9337-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f9337-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f9337-108">Return value</span></span>

<span data-ttu-id="f9337-109">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="f9337-109">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="f9337-110">Questo metodo restituisce un puntatore a una struttura D3DXMATRIX che rappresenta la matrice corrente.</span><span class="sxs-lookup"><span data-stu-id="f9337-110">This method returns a pointer to a D3DXMATRIX structure representing the current matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9337-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="f9337-111">Remarks</span></span>

<span data-ttu-id="f9337-112">Non è garantito che il puntatore D3DXMATRIX restituito da questo metodo sia valido dopo le successive operazioni dello stack.</span><span class="sxs-lookup"><span data-stu-id="f9337-112">The D3DXMATRIX pointer returned by this method is not guaranteed to be valid after subsequent stack operations.</span></span>

<span data-ttu-id="f9337-113">Si noti che questo metodo non rimuove la matrice corrente dall'inizio dello stack. restituisce invece solo la matrice corrente.</span><span class="sxs-lookup"><span data-stu-id="f9337-113">Note that this method does not remove the current matrix from the top of the stack; rather, it just returns the current matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9337-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f9337-114">Requirements</span></span>



| <span data-ttu-id="f9337-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9337-115">Requirement</span></span> | <span data-ttu-id="f9337-116">Valore</span><span class="sxs-lookup"><span data-stu-id="f9337-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f9337-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f9337-117">Header</span></span><br/>  | <dl> <span data-ttu-id="f9337-118"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="f9337-118"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="f9337-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="f9337-119">Library</span></span><br/> | <dl> <span data-ttu-id="f9337-120"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="f9337-120"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9337-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f9337-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9337-122">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="f9337-122">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="f9337-123">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="f9337-123">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
