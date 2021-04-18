---
description: Rimuove la matrice corrente dall'inizio dello stack.
ms.assetid: f4e4ff5d-a7a1-4f87-9b7e-53b9d044ba51
title: 'ID3DXMATRIXStack: Metodo op:P (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.Pop
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: a9a7b88cc749ef61c8b04395497fcc00ea9b36ca
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323661"
---
# <a name="id3dxmatrixstackpop-method-d3dx10h"></a><span data-ttu-id="64a91-103">ID3DXMATRIXStack: Metodo op:P (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="64a91-103">ID3DXMATRIXStack::Pop method (D3DX10.h)</span></span>

<span data-ttu-id="64a91-104">Rimuove la matrice corrente dall'inizio dello stack.</span><span class="sxs-lookup"><span data-stu-id="64a91-104">Removes the current matrix from the top of the stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="64a91-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="64a91-105">Syntax</span></span>


```C++
HRESULT Pop();
```



## <a name="parameters"></a><span data-ttu-id="64a91-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="64a91-106">Parameters</span></span>

<span data-ttu-id="64a91-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="64a91-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="64a91-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="64a91-108">Return value</span></span>

<span data-ttu-id="64a91-109">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="64a91-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="64a91-110">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="64a91-110">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="64a91-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="64a91-111">Remarks</span></span>

<span data-ttu-id="64a91-112">Si noti che questo metodo decrementa il numero di elementi nello stack di 1, rimuovendo in effetti la matrice corrente dalla parte superiore dello stack e innalzando di livello una matrice all'inizio dello stack.</span><span class="sxs-lookup"><span data-stu-id="64a91-112">Note that this method decrements the count of items on the stack by 1, effectively removing the current matrix from the top of the stack and promoting a matrix to the top of the stack.</span></span> <span data-ttu-id="64a91-113">Se il numero corrente di elementi nello stack è 0, questo metodo restituisce senza eseguire alcuna azione.</span><span class="sxs-lookup"><span data-stu-id="64a91-113">If the current count of items on the stack is 0, then this method returns without performing any action.</span></span> <span data-ttu-id="64a91-114">Se il numero corrente di elementi nello stack è 1, questo metodo svuota lo stack.</span><span class="sxs-lookup"><span data-stu-id="64a91-114">If the current count of items on the stack is 1, then this method empties the stack.</span></span>

## <a name="requirements"></a><span data-ttu-id="64a91-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="64a91-115">Requirements</span></span>



| <span data-ttu-id="64a91-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="64a91-116">Requirement</span></span> | <span data-ttu-id="64a91-117">Valore</span><span class="sxs-lookup"><span data-stu-id="64a91-117">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="64a91-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="64a91-118">Header</span></span><br/>  | <dl> <span data-ttu-id="64a91-119"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="64a91-119"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="64a91-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="64a91-120">Library</span></span><br/> | <dl> <span data-ttu-id="64a91-121"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="64a91-121"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64a91-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="64a91-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64a91-123">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="64a91-123">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="64a91-124">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="64a91-124">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




