---
description: Determina il prodotto della matrice specificata e della matrice corrente.
ms.assetid: 6f909b38-821c-4173-aba9-fd4392f70551
title: 'Metodo ID3DXMATRIXStack:: MultMatrixLocal (D3dx9math. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.MultMatrixLocal
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 547856e01cfdcb79110780136c1bbab59c0d7073
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322334"
---
# <a name="id3dxmatrixstackmultmatrixlocal-method-d3dx9mathh"></a><span data-ttu-id="a8108-103">Metodo ID3DXMATRIXStack:: MultMatrixLocal (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="a8108-103">ID3DXMATRIXStack::MultMatrixLocal method (D3dx9math.h)</span></span>

<span data-ttu-id="a8108-104">Determina il prodotto della matrice specificata e della matrice corrente.</span><span class="sxs-lookup"><span data-stu-id="a8108-104">Determines the product of the given matrix and the current matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8108-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a8108-105">Syntax</span></span>


```C++
HRESULT MultMatrixLocal(
  [in] const D3DXMATRIX *pMat
);
```



## <a name="parameters"></a><span data-ttu-id="a8108-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a8108-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8108-107">*pMat* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a8108-107">*pMat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8108-108">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="a8108-108">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="a8108-109">Puntatore alla struttura [**D3DXMATRIX**](d3dxmatrix.md) da moltiplicare con la matrice corrente.</span><span class="sxs-lookup"><span data-stu-id="a8108-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure to be multiplied with the current matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8108-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a8108-110">Return value</span></span>

<span data-ttu-id="a8108-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a8108-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a8108-112">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a8108-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a8108-113">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="a8108-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8108-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="a8108-114">Remarks</span></span>

<span data-ttu-id="a8108-115">Questo metodo consente di moltiplicare la matrice specificata con la matrice corrente (la trasformazione è relativa all'origine locale dell'oggetto).</span><span class="sxs-lookup"><span data-stu-id="a8108-115">This method left-multiplies the given matrix to the current matrix (transformation is about the local origin of the object).</span></span>


```
m_pstack[m_currentPos] = (*pMat) * m_pstack[m_currentPos];
```



<span data-ttu-id="a8108-116">Questo metodo non aggiunge un elemento allo stack, sostituisce la matrice corrente con il prodotto della matrice specificata e della matrice corrente.</span><span class="sxs-lookup"><span data-stu-id="a8108-116">This method does not add an item to the stack, it replaces the current matrix with the product of the given matrix and the current matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8108-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a8108-117">Requirements</span></span>



| <span data-ttu-id="a8108-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8108-118">Requirement</span></span> | <span data-ttu-id="a8108-119">Valore</span><span class="sxs-lookup"><span data-stu-id="a8108-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a8108-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a8108-120">Header</span></span><br/>  | <dl> <span data-ttu-id="a8108-121"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8108-121"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="a8108-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="a8108-122">Library</span></span><br/> | <dl> <span data-ttu-id="a8108-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a8108-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a8108-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a8108-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8108-125">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="a8108-125">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="a8108-126">**ID3DXMATRIXStack::MultMatrix**</span><span class="sxs-lookup"><span data-stu-id="a8108-126">**ID3DXMATRIXStack::MultMatrix**</span></span>](id3dxmatrixstack--multmatrix.md)
</dt> </dl>

 

 




