---
description: "Metodo ID3DXMATRIXStack::Scale (D3dx9math.h): ridimensiona la matrice corrente sull'origine delle coordinate del mondo."
ms.assetid: 6c4ef625-736e-41a0-8a79-4d71e8685754
title: Metodo ID3DXMATRIXStack::Scale (D3dx9math.h)
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
ms.openlocfilehash: 6d877fccf5bfebfdc1f9cf3943c4334e5b8c7fff
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093369"
---
# <a name="id3dxmatrixstackscale-method-d3dx9mathh"></a><span data-ttu-id="41ca1-103">Metodo ID3DXMATRIXStack::Scale (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="41ca1-103">ID3DXMATRIXStack::Scale method (D3dx9math.h)</span></span>

<span data-ttu-id="41ca1-104">Ridimensionare la matrice corrente sull'origine delle coordinate del mondo.</span><span class="sxs-lookup"><span data-stu-id="41ca1-104">Scale the current matrix about the world coordinate origin.</span></span>

## <a name="syntax"></a><span data-ttu-id="41ca1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="41ca1-105">Syntax</span></span>


```C++
HRESULT Scale(
  [in] FLOAT x,
  [in] FLOAT y,
  [in] FLOAT z
);
```



## <a name="parameters"></a><span data-ttu-id="41ca1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="41ca1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41ca1-107">*x* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="41ca1-107">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41ca1-108">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="41ca1-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="41ca1-109">Componente di ridimensionamento nella direzione x.</span><span class="sxs-lookup"><span data-stu-id="41ca1-109">The scaling component in the x-direction.</span></span>

</dd> <dt>

<span data-ttu-id="41ca1-110">*y* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="41ca1-110">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41ca1-111">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="41ca1-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="41ca1-112">Componente di ridimensionamento nella direzione y.</span><span class="sxs-lookup"><span data-stu-id="41ca1-112">The scaling component in the y-direction.</span></span>

</dd> <dt>

<span data-ttu-id="41ca1-113">*z* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="41ca1-113">*z* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41ca1-114">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="41ca1-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="41ca1-115">Componente di ridimensionamento nella direzione z.</span><span class="sxs-lookup"><span data-stu-id="41ca1-115">The scaling component in the z-direction.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41ca1-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="41ca1-116">Return value</span></span>

<span data-ttu-id="41ca1-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="41ca1-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="41ca1-118">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="41ca1-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="41ca1-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="41ca1-119">Remarks</span></span>

<span data-ttu-id="41ca1-120">Questo metodo moltiplica a destra la matrice corrente con la matrice di scala calcolata.</span><span class="sxs-lookup"><span data-stu-id="41ca1-120">This method right-multiplies the current matrix with the computed scale matrix.</span></span> <span data-ttu-id="41ca1-121">La trasformazione riguarda l'origine globale corrente.</span><span class="sxs-lookup"><span data-stu-id="41ca1-121">The transformation is about the current world origin.</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixScaling(&tmp, x, y, z);
m_stack[m_currentPos] = m_stack[m_currentPos] * tmp;
```



## <a name="requirements"></a><span data-ttu-id="41ca1-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="41ca1-122">Requirements</span></span>



| <span data-ttu-id="41ca1-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="41ca1-123">Requirement</span></span> | <span data-ttu-id="41ca1-124">Valore</span><span class="sxs-lookup"><span data-stu-id="41ca1-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="41ca1-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="41ca1-125">Header</span></span><br/>  | <dl> <span data-ttu-id="41ca1-126"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="41ca1-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="41ca1-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="41ca1-127">Library</span></span><br/> | <dl> <span data-ttu-id="41ca1-128"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="41ca1-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="41ca1-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="41ca1-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41ca1-130">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="41ca1-130">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="41ca1-131">**ID3DXMATRIXStack::ScaleLocal**</span><span class="sxs-lookup"><span data-stu-id="41ca1-131">**ID3DXMATRIXStack::ScaleLocal**</span></span>](id3dxmatrixstack--scalelocal.md)
</dt> </dl>

 

 
