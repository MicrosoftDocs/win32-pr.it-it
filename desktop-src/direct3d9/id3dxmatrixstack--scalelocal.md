---
description: Ridimensiona la matrice corrente sull'origine dell'oggetto.
ms.assetid: fe71da67-c8c9-4c78-9055-9bc3cadc0780
title: 'Metodo ID3DXMATRIXStack:: ScaleLocal (D3dx9math. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.ScaleLocal
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 05b188e3f1b0322225584bc0ef7c194c52ef949f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104234965"
---
# <a name="id3dxmatrixstackscalelocal-method-d3dx9mathh"></a><span data-ttu-id="a0555-103">Metodo ID3DXMATRIXStack:: ScaleLocal (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="a0555-103">ID3DXMATRIXStack::ScaleLocal method (D3dx9math.h)</span></span>

<span data-ttu-id="a0555-104">Ridimensiona la matrice corrente sull'origine dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a0555-104">Scale the current matrix about the object origin.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0555-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a0555-105">Syntax</span></span>


```C++
HRESULT ScaleLocal(
  [in] FLOAT x,
  [in] FLOAT y,
  [in] FLOAT z
);
```



## <a name="parameters"></a><span data-ttu-id="a0555-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a0555-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0555-107">*x* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a0555-107">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0555-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a0555-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a0555-109">Componente di scala nella direzione x.</span><span class="sxs-lookup"><span data-stu-id="a0555-109">The scaling component in the x-direction.</span></span>

</dd> <dt>

<span data-ttu-id="a0555-110">*y* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a0555-110">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0555-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a0555-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a0555-112">Componente di scala nella direzione y.</span><span class="sxs-lookup"><span data-stu-id="a0555-112">The scaling component in the y-direction.</span></span>

</dd> <dt>

<span data-ttu-id="a0555-113">*z* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a0555-113">*z* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0555-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a0555-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a0555-115">Componente di ridimensionamento nella direzione z.</span><span class="sxs-lookup"><span data-stu-id="a0555-115">The scaling component in the z-direction.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0555-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a0555-116">Return value</span></span>

<span data-ttu-id="a0555-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a0555-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a0555-118">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a0555-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0555-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="a0555-119">Remarks</span></span>

<span data-ttu-id="a0555-120">Questo metodo consente di moltiplicare a sinistra la matrice corrente con la matrice di scala calcolata.</span><span class="sxs-lookup"><span data-stu-id="a0555-120">This method left-multiplies the current matrix with the computed scale matrix.</span></span> <span data-ttu-id="a0555-121">La trasformazione riguarda l'origine locale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a0555-121">The transformation is about the local origin of the object.</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixScaling(&tmp, x, y, z);
m_stack[m_currentPos] = tmp * m_stack[m_currentPos];
```



## <a name="requirements"></a><span data-ttu-id="a0555-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a0555-122">Requirements</span></span>



| <span data-ttu-id="a0555-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0555-123">Requirement</span></span> | <span data-ttu-id="a0555-124">Valore</span><span class="sxs-lookup"><span data-stu-id="a0555-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a0555-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a0555-125">Header</span></span><br/>  | <dl> <span data-ttu-id="a0555-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0555-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="a0555-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="a0555-127">Library</span></span><br/> | <dl> <span data-ttu-id="a0555-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a0555-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a0555-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a0555-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0555-130">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="a0555-130">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="a0555-131">**ID3DXMATRIXStack:: scale**</span><span class="sxs-lookup"><span data-stu-id="a0555-131">**ID3DXMATRIXStack::Scale**</span></span>](id3dxmatrixstack--scale.md)
</dt> </dl>

 

 
