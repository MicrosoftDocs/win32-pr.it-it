---
description: 'Metodo ID3DXMATRIXStack::MultMatrixLocal (D3DX10.h): determina il prodotto della matrice specificata e della matrice corrente.'
ms.assetid: 4d374a7b-99e0-4313-970d-b0e7cf3e97ce
title: Metodo ID3DXMATRIXStack::MultMatrixLocal (D3DX10.h)
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
ms.openlocfilehash: 4b777bd729810b6fd63bd71def9858203b2ac559
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107949"
---
# <a name="id3dxmatrixstackmultmatrixlocal-method-d3dx10h"></a><span data-ttu-id="4ddcc-103">Metodo ID3DXMATRIXStack::MultMatrixLocal (D3DX10.h)</span><span class="sxs-lookup"><span data-stu-id="4ddcc-103">ID3DXMATRIXStack::MultMatrixLocal method (D3DX10.h)</span></span>

<span data-ttu-id="4ddcc-104">Determina il prodotto della matrice specificata e della matrice corrente.</span><span class="sxs-lookup"><span data-stu-id="4ddcc-104">Determines the product of the given matrix and the current matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ddcc-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4ddcc-105">Syntax</span></span>


```C++
HRESULT MultMatrixLocal(
  [in] const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="4ddcc-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4ddcc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ddcc-107">*pM* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="4ddcc-107">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ddcc-108">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="4ddcc-108">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="4ddcc-109">Puntatore alla struttura D3DXMATRIX da moltiplicare con la matrice corrente.</span><span class="sxs-lookup"><span data-stu-id="4ddcc-109">Pointer to the D3DXMATRIX structure to be multiplied with the current matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ddcc-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4ddcc-110">Return value</span></span>

<span data-ttu-id="4ddcc-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4ddcc-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4ddcc-112">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4ddcc-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="4ddcc-113">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="4ddcc-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ddcc-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="4ddcc-114">Remarks</span></span>

<span data-ttu-id="4ddcc-115">Questo metodo moltiplica a sinistra la matrice specificata nella matrice corrente (la trasformazione riguarda l'origine locale dell'oggetto).</span><span class="sxs-lookup"><span data-stu-id="4ddcc-115">This method left-multiplies the given matrix to the current matrix (transformation is about the local origin of the object).</span></span>


```
m_pstack[m_currentPos] = (*pMat) * m_pstack[m_currentPos];
```



<span data-ttu-id="4ddcc-116">Questo metodo non aggiunge un elemento nello stack, ma sostituisce la matrice corrente con il prodotto della matrice specificata e la matrice corrente.</span><span class="sxs-lookup"><span data-stu-id="4ddcc-116">This method does not add an item to the stack, it replaces the current matrix with the product of the given matrix and the current matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ddcc-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4ddcc-117">Requirements</span></span>



| <span data-ttu-id="4ddcc-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ddcc-118">Requirement</span></span> | <span data-ttu-id="4ddcc-119">Valore</span><span class="sxs-lookup"><span data-stu-id="4ddcc-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4ddcc-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4ddcc-120">Header</span></span><br/>  | <dl> <span data-ttu-id="4ddcc-121"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="4ddcc-121"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="4ddcc-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="4ddcc-122">Library</span></span><br/> | <dl> <span data-ttu-id="4ddcc-123"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="4ddcc-123"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ddcc-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4ddcc-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ddcc-125">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="4ddcc-125">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="4ddcc-126">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="4ddcc-126">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
