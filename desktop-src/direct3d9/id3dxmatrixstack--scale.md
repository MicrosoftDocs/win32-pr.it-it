---
description: Ridimensiona la matrice corrente sull'origine della coordinata globale.
ms.assetid: 6c4ef625-736e-41a0-8a79-4d71e8685754
title: 'Metodo ID3DXMATRIXStack:: scale (D3dx9math. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.Scale
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5ed926a55c0dba6f74e819cd89a7fa75f6d087c4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104132298"
---
# <a name="id3dxmatrixstackscale-method-d3dx9mathh"></a><span data-ttu-id="59b88-103">Metodo ID3DXMATRIXStack:: scale (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="59b88-103">ID3DXMATRIXStack::Scale method (D3dx9math.h)</span></span>

<span data-ttu-id="59b88-104">Ridimensiona la matrice corrente sull'origine della coordinata globale.</span><span class="sxs-lookup"><span data-stu-id="59b88-104">Scale the current matrix about the world coordinate origin.</span></span>

## <a name="syntax"></a><span data-ttu-id="59b88-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="59b88-105">Syntax</span></span>


```C++
HRESULT Scale(
  [in] FLOAT x,
  [in] FLOAT y,
  [in] FLOAT z
);
```



## <a name="parameters"></a><span data-ttu-id="59b88-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="59b88-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59b88-107">*x* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="59b88-107">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59b88-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="59b88-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="59b88-109">Componente di scala nella direzione x.</span><span class="sxs-lookup"><span data-stu-id="59b88-109">The scaling component in the x-direction.</span></span>

</dd> <dt>

<span data-ttu-id="59b88-110">*y* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="59b88-110">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59b88-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="59b88-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="59b88-112">Componente di scala nella direzione y.</span><span class="sxs-lookup"><span data-stu-id="59b88-112">The scaling component in the y-direction.</span></span>

</dd> <dt>

<span data-ttu-id="59b88-113">*z* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="59b88-113">*z* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59b88-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="59b88-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="59b88-115">Componente di ridimensionamento nella direzione z.</span><span class="sxs-lookup"><span data-stu-id="59b88-115">The scaling component in the z-direction.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59b88-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="59b88-116">Return value</span></span>

<span data-ttu-id="59b88-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="59b88-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="59b88-118">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="59b88-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="59b88-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="59b88-119">Remarks</span></span>

<span data-ttu-id="59b88-120">Questo metodo moltiplica a destra la matrice corrente con la matrice di scala calcolata.</span><span class="sxs-lookup"><span data-stu-id="59b88-120">This method right-multiplies the current matrix with the computed scale matrix.</span></span> <span data-ttu-id="59b88-121">La trasformazione riguarda l'origine mondiale corrente.</span><span class="sxs-lookup"><span data-stu-id="59b88-121">The transformation is about the current world origin.</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixScaling(&tmp, x, y, z);
m_stack[m_currentPos] = m_stack[m_currentPos] * tmp;
```



## <a name="requirements"></a><span data-ttu-id="59b88-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="59b88-122">Requirements</span></span>



| <span data-ttu-id="59b88-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="59b88-123">Requirement</span></span> | <span data-ttu-id="59b88-124">Valore</span><span class="sxs-lookup"><span data-stu-id="59b88-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="59b88-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="59b88-125">Header</span></span><br/>  | <dl> <span data-ttu-id="59b88-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="59b88-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="59b88-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="59b88-127">Library</span></span><br/> | <dl> <span data-ttu-id="59b88-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="59b88-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="59b88-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="59b88-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59b88-130">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="59b88-130">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="59b88-131">**ID3DXMATRIXStack::ScaleLocal**</span><span class="sxs-lookup"><span data-stu-id="59b88-131">**ID3DXMATRIXStack::ScaleLocal**</span></span>](id3dxmatrixstack--scalelocal.md)
</dt> </dl>

 

 
