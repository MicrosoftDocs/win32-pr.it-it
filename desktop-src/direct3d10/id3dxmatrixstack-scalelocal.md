---
description: "Metodo ID3DXMATRIXStack::ScaleLocal (D3DX10.h): ridimensiona la matrice corrente sull'origine dell'oggetto."
ms.assetid: 748fce3a-a33c-4975-bbf0-dd3167a036f1
title: Metodo ID3DXMATRIXStack::ScaleLocal (D3DX10.h)
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
ms.openlocfilehash: 3961db0794703e3974dbd92d8eae8293173c2354
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107779"
---
# <a name="id3dxmatrixstackscalelocal-method-d3dx10h"></a><span data-ttu-id="95b35-103">Metodo ID3DXMATRIXStack::ScaleLocal (D3DX10.h)</span><span class="sxs-lookup"><span data-stu-id="95b35-103">ID3DXMATRIXStack::ScaleLocal method (D3DX10.h)</span></span>

<span data-ttu-id="95b35-104">Ridimensionare la matrice corrente sull'origine dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="95b35-104">Scale the current matrix about the object origin.</span></span>

## <a name="syntax"></a><span data-ttu-id="95b35-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="95b35-105">Syntax</span></span>


```C++
HRESULT ScaleLocal(
  [in] FLOAT x,
  [in] FLOAT y,
  [in] FLOAT z
);
```



## <a name="parameters"></a><span data-ttu-id="95b35-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="95b35-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95b35-107">*x* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="95b35-107">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95b35-108">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="95b35-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="95b35-109">Componente di ridimensionamento nella direzione x.</span><span class="sxs-lookup"><span data-stu-id="95b35-109">The scaling component in the x-direction.</span></span>

</dd> <dt>

<span data-ttu-id="95b35-110">*y* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="95b35-110">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95b35-111">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="95b35-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="95b35-112">Componente di ridimensionamento nella direzione y.</span><span class="sxs-lookup"><span data-stu-id="95b35-112">The scaling component in the y-direction.</span></span>

</dd> <dt>

<span data-ttu-id="95b35-113">*z* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="95b35-113">*z* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95b35-114">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="95b35-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="95b35-115">Componente di ridimensionamento nella direzione z.</span><span class="sxs-lookup"><span data-stu-id="95b35-115">The scaling component in the z-direction.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95b35-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="95b35-116">Return value</span></span>

<span data-ttu-id="95b35-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="95b35-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="95b35-118">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="95b35-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="95b35-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="95b35-119">Remarks</span></span>

<span data-ttu-id="95b35-120">Questo metodo moltiplica a sinistra la matrice corrente con la matrice di scala calcolata.</span><span class="sxs-lookup"><span data-stu-id="95b35-120">This method left-multiplies the current matrix with the computed scale matrix.</span></span> <span data-ttu-id="95b35-121">La trasformazione riguarda l'origine locale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="95b35-121">The transformation is about the local origin of the object.</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixScaling(&tmp, x, y, z);
m_stack[m_currentPos] = tmp * m_stack[m_currentPos];
```



## <a name="requirements"></a><span data-ttu-id="95b35-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="95b35-122">Requirements</span></span>



| <span data-ttu-id="95b35-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="95b35-123">Requirement</span></span> | <span data-ttu-id="95b35-124">Valore</span><span class="sxs-lookup"><span data-stu-id="95b35-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="95b35-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="95b35-125">Header</span></span><br/>  | <dl> <span data-ttu-id="95b35-126"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="95b35-126"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="95b35-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="95b35-127">Library</span></span><br/> | <dl> <span data-ttu-id="95b35-128"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="95b35-128"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95b35-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="95b35-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95b35-130">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="95b35-130">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="95b35-131">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="95b35-131">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
