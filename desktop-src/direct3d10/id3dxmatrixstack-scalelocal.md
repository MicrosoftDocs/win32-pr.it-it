---
description: Ridimensiona la matrice corrente sull'origine dell'oggetto.
ms.assetid: 748fce3a-a33c-4975-bbf0-dd3167a036f1
title: 'Metodo ID3DXMATRIXStack:: ScaleLocal (D3DX10. h)'
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 868aae418ebedbc54cb8f15ba4fa4e11d47c7f50
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103886324"
---
# <a name="id3dxmatrixstackscalelocal-method-d3dx10h"></a><span data-ttu-id="c827f-103">Metodo ID3DXMATRIXStack:: ScaleLocal (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="c827f-103">ID3DXMATRIXStack::ScaleLocal method (D3DX10.h)</span></span>

<span data-ttu-id="c827f-104">Ridimensiona la matrice corrente sull'origine dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="c827f-104">Scale the current matrix about the object origin.</span></span>

## <a name="syntax"></a><span data-ttu-id="c827f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c827f-105">Syntax</span></span>


```C++
HRESULT ScaleLocal(
  [in] FLOAT x,
  [in] FLOAT y,
  [in] FLOAT z
);
```



## <a name="parameters"></a><span data-ttu-id="c827f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c827f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c827f-107">*x* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c827f-107">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c827f-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c827f-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c827f-109">Componente di scala nella direzione x.</span><span class="sxs-lookup"><span data-stu-id="c827f-109">The scaling component in the x-direction.</span></span>

</dd> <dt>

<span data-ttu-id="c827f-110">*y* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c827f-110">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c827f-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c827f-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c827f-112">Componente di scala nella direzione y.</span><span class="sxs-lookup"><span data-stu-id="c827f-112">The scaling component in the y-direction.</span></span>

</dd> <dt>

<span data-ttu-id="c827f-113">*z* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c827f-113">*z* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c827f-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c827f-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c827f-115">Componente di ridimensionamento nella direzione z.</span><span class="sxs-lookup"><span data-stu-id="c827f-115">The scaling component in the z-direction.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c827f-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c827f-116">Return value</span></span>

<span data-ttu-id="c827f-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c827f-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c827f-118">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c827f-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="c827f-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="c827f-119">Remarks</span></span>

<span data-ttu-id="c827f-120">Questo metodo consente di moltiplicare a sinistra la matrice corrente con la matrice di scala calcolata.</span><span class="sxs-lookup"><span data-stu-id="c827f-120">This method left-multiplies the current matrix with the computed scale matrix.</span></span> <span data-ttu-id="c827f-121">La trasformazione riguarda l'origine locale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="c827f-121">The transformation is about the local origin of the object.</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixScaling(&tmp, x, y, z);
m_stack[m_currentPos] = tmp * m_stack[m_currentPos];
```



## <a name="requirements"></a><span data-ttu-id="c827f-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c827f-122">Requirements</span></span>



| <span data-ttu-id="c827f-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="c827f-123">Requirement</span></span> | <span data-ttu-id="c827f-124">Valore</span><span class="sxs-lookup"><span data-stu-id="c827f-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c827f-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c827f-125">Header</span></span><br/>  | <dl> <span data-ttu-id="c827f-126"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="c827f-126"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="c827f-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="c827f-127">Library</span></span><br/> | <dl> <span data-ttu-id="c827f-128"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c827f-128"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c827f-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c827f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c827f-130">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="c827f-130">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="c827f-131">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="c827f-131">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
