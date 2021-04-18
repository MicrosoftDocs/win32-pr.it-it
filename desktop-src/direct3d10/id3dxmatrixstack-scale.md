---
description: Ridimensiona la matrice corrente sull'origine della coordinata globale.
ms.assetid: d0f4b341-b3b6-42e4-84df-78f203c3728e
title: 'Metodo ID3DXMATRIXStack:: scale (D3DX10. h)'
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 361c1fcbdc3f793bcf3e21d569eee740ca0b4ee2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323655"
---
# <a name="id3dxmatrixstackscale-method-d3dx10h"></a><span data-ttu-id="7efa7-103">Metodo ID3DXMATRIXStack:: scale (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="7efa7-103">ID3DXMATRIXStack::Scale method (D3DX10.h)</span></span>

<span data-ttu-id="7efa7-104">Ridimensiona la matrice corrente sull'origine della coordinata globale.</span><span class="sxs-lookup"><span data-stu-id="7efa7-104">Scale the current matrix about the world coordinate origin.</span></span>

## <a name="syntax"></a><span data-ttu-id="7efa7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7efa7-105">Syntax</span></span>


```C++
HRESULT Scale(
  [in] FLOAT x,
  [in] FLOAT y,
  [in] FLOAT z
);
```



## <a name="parameters"></a><span data-ttu-id="7efa7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7efa7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7efa7-107">*x* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7efa7-107">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7efa7-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7efa7-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7efa7-109">Componente di scala nella direzione x.</span><span class="sxs-lookup"><span data-stu-id="7efa7-109">The scaling component in the x-direction.</span></span>

</dd> <dt>

<span data-ttu-id="7efa7-110">*y* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7efa7-110">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7efa7-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7efa7-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7efa7-112">Componente di scala nella direzione y.</span><span class="sxs-lookup"><span data-stu-id="7efa7-112">The scaling component in the y-direction.</span></span>

</dd> <dt>

<span data-ttu-id="7efa7-113">*z* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7efa7-113">*z* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7efa7-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7efa7-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7efa7-115">Componente di ridimensionamento nella direzione z.</span><span class="sxs-lookup"><span data-stu-id="7efa7-115">The scaling component in the z-direction.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7efa7-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7efa7-116">Return value</span></span>

<span data-ttu-id="7efa7-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7efa7-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7efa7-118">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7efa7-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="7efa7-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="7efa7-119">Remarks</span></span>

<span data-ttu-id="7efa7-120">Questo metodo moltiplica a destra la matrice corrente con la matrice di scala calcolata.</span><span class="sxs-lookup"><span data-stu-id="7efa7-120">This method right-multiplies the current matrix with the computed scale matrix.</span></span> <span data-ttu-id="7efa7-121">La trasformazione riguarda l'origine mondiale corrente.</span><span class="sxs-lookup"><span data-stu-id="7efa7-121">The transformation is about the current world origin.</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixScaling(&tmp, x, y, z);
m_stack[m_currentPos] = m_stack[m_currentPos] * tmp;
```



## <a name="requirements"></a><span data-ttu-id="7efa7-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7efa7-122">Requirements</span></span>



| <span data-ttu-id="7efa7-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="7efa7-123">Requirement</span></span> | <span data-ttu-id="7efa7-124">Valore</span><span class="sxs-lookup"><span data-stu-id="7efa7-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7efa7-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7efa7-125">Header</span></span><br/>  | <dl> <span data-ttu-id="7efa7-126"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="7efa7-126"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="7efa7-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="7efa7-127">Library</span></span><br/> | <dl> <span data-ttu-id="7efa7-128"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7efa7-128"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7efa7-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7efa7-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7efa7-130">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="7efa7-130">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="7efa7-131">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="7efa7-131">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
