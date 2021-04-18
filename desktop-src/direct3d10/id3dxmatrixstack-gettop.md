---
description: Recupera la matrice corrente all'inizio dello stack.
ms.assetid: cf379742-3e7d-4309-a7af-b97348428682
title: 'Metodo ID3DXMATRIXStack:: GetTop (D3DX10. h)'
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
ms.openlocfilehash: c545287ff3a4e7f9bfdccf21b9351fef06367433
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323666"
---
# <a name="id3dxmatrixstackgettop-method-d3dx10h"></a><span data-ttu-id="916c3-103">Metodo ID3DXMATRIXStack:: GetTop (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="916c3-103">ID3DXMATRIXStack::GetTop method (D3DX10.h)</span></span>

<span data-ttu-id="916c3-104">Recupera la matrice corrente all'inizio dello stack.</span><span class="sxs-lookup"><span data-stu-id="916c3-104">Retrieves the current matrix at the top of the stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="916c3-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="916c3-105">Syntax</span></span>


```C++
D3DXMATRIX* GetTop();
```



## <a name="parameters"></a><span data-ttu-id="916c3-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="916c3-106">Parameters</span></span>

<span data-ttu-id="916c3-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="916c3-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="916c3-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="916c3-108">Return value</span></span>

<span data-ttu-id="916c3-109">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="916c3-109">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="916c3-110">Questo metodo restituisce un puntatore a una struttura D3DXMATRIX che rappresenta la matrice corrente.</span><span class="sxs-lookup"><span data-stu-id="916c3-110">This method returns a pointer to a D3DXMATRIX structure representing the current matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="916c3-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="916c3-111">Remarks</span></span>

<span data-ttu-id="916c3-112">Il puntatore D3DXMATRIX restituito da questo metodo non è garantito come valido dopo le operazioni di stack successive.</span><span class="sxs-lookup"><span data-stu-id="916c3-112">The D3DXMATRIX pointer returned by this method is not guaranteed to be valid after subsequent stack operations.</span></span>

<span data-ttu-id="916c3-113">Si noti che questo metodo non rimuove la matrice corrente dall'inizio dello stack. piuttosto restituisce solo la matrice corrente.</span><span class="sxs-lookup"><span data-stu-id="916c3-113">Note that this method does not remove the current matrix from the top of the stack; rather, it just returns the current matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="916c3-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="916c3-114">Requirements</span></span>



| <span data-ttu-id="916c3-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="916c3-115">Requirement</span></span> | <span data-ttu-id="916c3-116">Valore</span><span class="sxs-lookup"><span data-stu-id="916c3-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="916c3-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="916c3-117">Header</span></span><br/>  | <dl> <span data-ttu-id="916c3-118"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="916c3-118"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="916c3-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="916c3-119">Library</span></span><br/> | <dl> <span data-ttu-id="916c3-120"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="916c3-120"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="916c3-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="916c3-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="916c3-122">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="916c3-122">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="916c3-123">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="916c3-123">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
