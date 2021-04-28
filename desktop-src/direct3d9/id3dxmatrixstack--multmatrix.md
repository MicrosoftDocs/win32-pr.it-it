---
description: 'Metodo ID3DXMATRIXStack::MultMatrix (D3dx9math.h): determina il prodotto della matrice corrente e della matrice specificata.'
ms.assetid: a673ce82-6fed-4a3f-8c37-d0db11195f06
title: Metodo ID3DXMATRIXStack::MultMatrix (D3dx9math.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7361223e8fbcbae0f81641718b216c5903ff6319
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093529"
---
# <a name="id3dxmatrixstackmultmatrix-method-d3dx9mathh"></a><span data-ttu-id="5e4a9-103">Metodo ID3DXMATRIXStack::MultMatrix (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="5e4a9-103">ID3DXMATRIXStack::MultMatrix method (D3dx9math.h)</span></span>

<span data-ttu-id="5e4a9-104">Determina il prodotto della matrice corrente e della matrice specificata.</span><span class="sxs-lookup"><span data-stu-id="5e4a9-104">Determines the product of the current matrix and the given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e4a9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5e4a9-105">Syntax</span></span>


```C++
HRESULT MultMatrix(
  [in] const D3DXMATRIX *pMat
);
```



## <a name="parameters"></a><span data-ttu-id="5e4a9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5e4a9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e4a9-107">*pMat* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="5e4a9-107">*pMat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e4a9-108">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="5e4a9-108">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="5e4a9-109">Puntatore alla [**struttura D3DXMATRIX**](d3dxmatrix.md) da moltiplicare con la matrice corrente.</span><span class="sxs-lookup"><span data-stu-id="5e4a9-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure to be multiplied with the current matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e4a9-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5e4a9-110">Return value</span></span>

<span data-ttu-id="5e4a9-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5e4a9-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5e4a9-112">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5e4a9-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="5e4a9-113">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="5e4a9-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e4a9-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="5e4a9-114">Remarks</span></span>

<span data-ttu-id="5e4a9-115">Questo metodo moltiplica a destra la matrice specificata nella matrice corrente (la trasformazione riguarda l'origine globale corrente).</span><span class="sxs-lookup"><span data-stu-id="5e4a9-115">This method right-multiplies the given matrix to the current matrix (transformation is about the current world origin).</span></span>


```
m_pstack[m_currentPos] = m_pstack[m_currentPos] * (*pMat);
```



<span data-ttu-id="5e4a9-116">Questo metodo non aggiunge un elemento nello stack, ma sostituisce la matrice corrente con il prodotto della matrice corrente e la matrice specificata.</span><span class="sxs-lookup"><span data-stu-id="5e4a9-116">This method does not add an item to the stack, it replaces the current matrix with the product of the current matrix and the given matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e4a9-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5e4a9-117">Requirements</span></span>



| <span data-ttu-id="5e4a9-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e4a9-118">Requirement</span></span> | <span data-ttu-id="5e4a9-119">Valore</span><span class="sxs-lookup"><span data-stu-id="5e4a9-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5e4a9-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5e4a9-120">Header</span></span><br/>  | <dl> <span data-ttu-id="5e4a9-121"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="5e4a9-121"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="5e4a9-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="5e4a9-122">Library</span></span><br/> | <dl> <span data-ttu-id="5e4a9-123"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="5e4a9-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5e4a9-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5e4a9-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e4a9-125">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="5e4a9-125">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="5e4a9-126">**ID3DXMATRIXStack::MultMatrixLocal**</span><span class="sxs-lookup"><span data-stu-id="5e4a9-126">**ID3DXMATRIXStack::MultMatrixLocal**</span></span>](id3dxmatrixstack--multmatrixlocal.md)
</dt> </dl>

 

 




