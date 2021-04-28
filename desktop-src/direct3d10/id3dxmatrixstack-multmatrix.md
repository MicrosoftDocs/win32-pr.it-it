---
description: 'Metodo ID3DXMATRIXStack::MultMatrix (D3DX10.h): determina il prodotto della matrice corrente e della matrice specificata.'
ms.assetid: 72388919-e474-4433-b219-41e2d312848e
title: Metodo ID3DXMATRIXStack::MultMatrix (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.MultMatrix
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 969cdebcee34add15cbf6bbcfbb1048387b2d7e8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107969"
---
# <a name="id3dxmatrixstackmultmatrix-method-d3dx10h"></a><span data-ttu-id="5b2f0-103">Metodo ID3DXMATRIXStack::MultMatrix (D3DX10.h)</span><span class="sxs-lookup"><span data-stu-id="5b2f0-103">ID3DXMATRIXStack::MultMatrix method (D3DX10.h)</span></span>

<span data-ttu-id="5b2f0-104">Determina il prodotto della matrice corrente e della matrice specificata.</span><span class="sxs-lookup"><span data-stu-id="5b2f0-104">Determines the product of the current matrix and the given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b2f0-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5b2f0-105">Syntax</span></span>


```C++
HRESULT MultMatrix(
  [in] const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="5b2f0-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5b2f0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b2f0-107">*pM* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="5b2f0-107">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b2f0-108">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="5b2f0-108">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="5b2f0-109">Puntatore alla struttura D3DXMATRIX da moltiplicare con la matrice corrente.</span><span class="sxs-lookup"><span data-stu-id="5b2f0-109">Pointer to the D3DXMATRIX structure to be multiplied with the current matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b2f0-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5b2f0-110">Return value</span></span>

<span data-ttu-id="5b2f0-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5b2f0-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5b2f0-112">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5b2f0-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="5b2f0-113">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="5b2f0-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b2f0-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="5b2f0-114">Remarks</span></span>

<span data-ttu-id="5b2f0-115">Questo metodo moltiplica a destra la matrice specificata per la matrice corrente (la trasformazione riguarda l'origine globale corrente).</span><span class="sxs-lookup"><span data-stu-id="5b2f0-115">This method right-multiplies the given matrix to the current matrix (transformation is about the current world origin).</span></span>


```
m_pstack[m_currentPos] = m_pstack[m_currentPos] * (*pMat);
```



<span data-ttu-id="5b2f0-116">Questo metodo non aggiunge un elemento nello stack, ma sostituisce la matrice corrente con il prodotto della matrice corrente e della matrice specificata.</span><span class="sxs-lookup"><span data-stu-id="5b2f0-116">This method does not add an item to the stack, it replaces the current matrix with the product of the current matrix and the given matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b2f0-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5b2f0-117">Requirements</span></span>



| <span data-ttu-id="5b2f0-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b2f0-118">Requirement</span></span> | <span data-ttu-id="5b2f0-119">Valore</span><span class="sxs-lookup"><span data-stu-id="5b2f0-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5b2f0-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5b2f0-120">Header</span></span><br/>  | <dl> <span data-ttu-id="5b2f0-121"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="5b2f0-121"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="5b2f0-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="5b2f0-122">Library</span></span><br/> | <dl> <span data-ttu-id="5b2f0-123"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="5b2f0-123"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b2f0-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5b2f0-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b2f0-125">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="5b2f0-125">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="5b2f0-126">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="5b2f0-126">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
