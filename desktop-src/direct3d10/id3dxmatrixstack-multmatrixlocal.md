---
description: Determina il prodotto della matrice specificata e della matrice corrente.
ms.assetid: 4d374a7b-99e0-4313-970d-b0e7cf3e97ce
title: 'Metodo ID3DXMATRIXStack:: MultMatrixLocal (D3DX10. h)'
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 095882c98169159beaca0ef6c98d13fe03b9aed2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235209"
---
# <a name="id3dxmatrixstackmultmatrixlocal-method-d3dx10h"></a><span data-ttu-id="b69b7-103">Metodo ID3DXMATRIXStack:: MultMatrixLocal (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="b69b7-103">ID3DXMATRIXStack::MultMatrixLocal method (D3DX10.h)</span></span>

<span data-ttu-id="b69b7-104">Determina il prodotto della matrice specificata e della matrice corrente.</span><span class="sxs-lookup"><span data-stu-id="b69b7-104">Determines the product of the given matrix and the current matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="b69b7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b69b7-105">Syntax</span></span>


```C++
HRESULT MultMatrixLocal(
  [in] const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="b69b7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b69b7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b69b7-107">*PM* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b69b7-107">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b69b7-108">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="b69b7-108">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="b69b7-109">Puntatore alla struttura D3DXMATRIX da moltiplicare con la matrice corrente.</span><span class="sxs-lookup"><span data-stu-id="b69b7-109">Pointer to the D3DXMATRIX structure to be multiplied with the current matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b69b7-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b69b7-110">Return value</span></span>

<span data-ttu-id="b69b7-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b69b7-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b69b7-112">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b69b7-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b69b7-113">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="b69b7-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="b69b7-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="b69b7-114">Remarks</span></span>

<span data-ttu-id="b69b7-115">Questo metodo consente di moltiplicare la matrice specificata con la matrice corrente (la trasformazione è relativa all'origine locale dell'oggetto).</span><span class="sxs-lookup"><span data-stu-id="b69b7-115">This method left-multiplies the given matrix to the current matrix (transformation is about the local origin of the object).</span></span>


```
m_pstack[m_currentPos] = (*pMat) * m_pstack[m_currentPos];
```



<span data-ttu-id="b69b7-116">Questo metodo non aggiunge un elemento allo stack, sostituisce la matrice corrente con il prodotto della matrice specificata e della matrice corrente.</span><span class="sxs-lookup"><span data-stu-id="b69b7-116">This method does not add an item to the stack, it replaces the current matrix with the product of the given matrix and the current matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="b69b7-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b69b7-117">Requirements</span></span>



| <span data-ttu-id="b69b7-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b69b7-118">Requirement</span></span> | <span data-ttu-id="b69b7-119">Valore</span><span class="sxs-lookup"><span data-stu-id="b69b7-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b69b7-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b69b7-120">Header</span></span><br/>  | <dl> <span data-ttu-id="b69b7-121"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="b69b7-121"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="b69b7-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="b69b7-122">Library</span></span><br/> | <dl> <span data-ttu-id="b69b7-123"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b69b7-123"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b69b7-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b69b7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b69b7-125">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="b69b7-125">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="b69b7-126">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="b69b7-126">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
