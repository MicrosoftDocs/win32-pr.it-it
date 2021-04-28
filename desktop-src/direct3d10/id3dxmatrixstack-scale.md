---
description: "Metodo ID3DXMATRIXStack::Scale (D3DX10.h): ridimensiona la matrice corrente sull'origine delle coordinate del mondo."
ms.assetid: d0f4b341-b3b6-42e4-84df-78f203c3728e
title: Metodo ID3DXMATRIXStack::Scale (D3DX10.h)
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
ms.openlocfilehash: a7b4aceb53659fc2b1a4a95f964d068e6d7d2554
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107789"
---
# <a name="id3dxmatrixstackscale-method-d3dx10h"></a><span data-ttu-id="60b2c-103">Metodo ID3DXMATRIXStack::Scale (D3DX10.h)</span><span class="sxs-lookup"><span data-stu-id="60b2c-103">ID3DXMATRIXStack::Scale method (D3DX10.h)</span></span>

<span data-ttu-id="60b2c-104">Ridimensionare la matrice corrente sull'origine delle coordinate del mondo.</span><span class="sxs-lookup"><span data-stu-id="60b2c-104">Scale the current matrix about the world coordinate origin.</span></span>

## <a name="syntax"></a><span data-ttu-id="60b2c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="60b2c-105">Syntax</span></span>


```C++
HRESULT Scale(
  [in] FLOAT x,
  [in] FLOAT y,
  [in] FLOAT z
);
```



## <a name="parameters"></a><span data-ttu-id="60b2c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="60b2c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60b2c-107">*x* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="60b2c-107">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60b2c-108">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="60b2c-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="60b2c-109">Componente di ridimensionamento nella direzione x.</span><span class="sxs-lookup"><span data-stu-id="60b2c-109">The scaling component in the x-direction.</span></span>

</dd> <dt>

<span data-ttu-id="60b2c-110">*y* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="60b2c-110">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60b2c-111">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="60b2c-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="60b2c-112">Componente di ridimensionamento nella direzione y.</span><span class="sxs-lookup"><span data-stu-id="60b2c-112">The scaling component in the y-direction.</span></span>

</dd> <dt>

<span data-ttu-id="60b2c-113">*z* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="60b2c-113">*z* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60b2c-114">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="60b2c-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="60b2c-115">Componente di ridimensionamento nella direzione z.</span><span class="sxs-lookup"><span data-stu-id="60b2c-115">The scaling component in the z-direction.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60b2c-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="60b2c-116">Return value</span></span>

<span data-ttu-id="60b2c-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="60b2c-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="60b2c-118">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="60b2c-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="60b2c-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="60b2c-119">Remarks</span></span>

<span data-ttu-id="60b2c-120">Questo metodo moltiplica a destra la matrice corrente con la matrice di scala calcolata.</span><span class="sxs-lookup"><span data-stu-id="60b2c-120">This method right-multiplies the current matrix with the computed scale matrix.</span></span> <span data-ttu-id="60b2c-121">La trasformazione riguarda l'origine globale corrente.</span><span class="sxs-lookup"><span data-stu-id="60b2c-121">The transformation is about the current world origin.</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixScaling(&tmp, x, y, z);
m_stack[m_currentPos] = m_stack[m_currentPos] * tmp;
```



## <a name="requirements"></a><span data-ttu-id="60b2c-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="60b2c-122">Requirements</span></span>



| <span data-ttu-id="60b2c-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="60b2c-123">Requirement</span></span> | <span data-ttu-id="60b2c-124">Valore</span><span class="sxs-lookup"><span data-stu-id="60b2c-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="60b2c-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="60b2c-125">Header</span></span><br/>  | <dl> <span data-ttu-id="60b2c-126"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="60b2c-126"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="60b2c-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="60b2c-127">Library</span></span><br/> | <dl> <span data-ttu-id="60b2c-128"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="60b2c-128"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60b2c-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="60b2c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60b2c-130">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="60b2c-130">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="60b2c-131">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="60b2c-131">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
