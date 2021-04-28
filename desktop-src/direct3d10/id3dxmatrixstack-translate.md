---
description: 'Metodo ID3DXMATRIXStack::Translate (D3DX10.h): determina il prodotto della matrice corrente e della matrice di traslazione calcolata determinata dai fattori specifici (x, y e z).'
ms.assetid: d6e347a5-bb66-451d-b66e-49ea8eff70b3
title: Metodo ID3DXMATRIXStack::Translate (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.Translate
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 41e84b62c077da03806a5e781498c05ee3c8ee67
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107769"
---
# <a name="id3dxmatrixstacktranslate-method-d3dx10h"></a><span data-ttu-id="bb427-103">Metodo ID3DXMATRIXStack::Translate (D3DX10.h)</span><span class="sxs-lookup"><span data-stu-id="bb427-103">ID3DXMATRIXStack::Translate method (D3DX10.h)</span></span>

<span data-ttu-id="bb427-104">Determina il prodotto della matrice corrente e la matrice di traslazione calcolata determinata dai fattori (x, y e z) specifici.</span><span class="sxs-lookup"><span data-stu-id="bb427-104">Determines the product of the current matrix and the computed translation matrix determined by the given factors (x, y, and z).</span></span>

## <a name="syntax"></a><span data-ttu-id="bb427-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bb427-105">Syntax</span></span>


```C++
HRESULT Translate(
  [in] FLOAT x,
  [in] FLOAT y,
  [in] FLOAT z
);
```



## <a name="parameters"></a><span data-ttu-id="bb427-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="bb427-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb427-107">*x* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bb427-107">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb427-108">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bb427-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bb427-109">Fattore di traslazione nella direzione x.</span><span class="sxs-lookup"><span data-stu-id="bb427-109">The translation factor in the x-direction.</span></span>

</dd> <dt>

<span data-ttu-id="bb427-110">*y* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bb427-110">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb427-111">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bb427-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bb427-112">Fattore di traslazione nella direzione y.</span><span class="sxs-lookup"><span data-stu-id="bb427-112">The translation factor in the y-direction.</span></span>

</dd> <dt>

<span data-ttu-id="bb427-113">*z* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bb427-113">*z* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb427-114">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bb427-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bb427-115">Fattore di traslazione nella direzione z.</span><span class="sxs-lookup"><span data-stu-id="bb427-115">The translation factor in the z-direction.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb427-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bb427-116">Return value</span></span>

<span data-ttu-id="bb427-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bb427-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bb427-118">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="bb427-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb427-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="bb427-119">Remarks</span></span>

<span data-ttu-id="bb427-120">Questo metodo moltiplica a destra la matrice corrente con la matrice di traslazione calcolata (la trasformazione riguarda l'origine globale corrente).</span><span class="sxs-lookup"><span data-stu-id="bb427-120">This method right-multiplies the current matrix with the computed translation matrix (transformation is about the current world origin).</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixTranslation( &tmp, x, y, z );
m_stack[m_currentPos] = m_stack[m_currentPos] * tmp;
```



## <a name="requirements"></a><span data-ttu-id="bb427-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bb427-121">Requirements</span></span>



| <span data-ttu-id="bb427-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb427-122">Requirement</span></span> | <span data-ttu-id="bb427-123">Valore</span><span class="sxs-lookup"><span data-stu-id="bb427-123">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bb427-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bb427-124">Header</span></span><br/>  | <dl> <span data-ttu-id="bb427-125"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="bb427-125"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="bb427-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="bb427-126">Library</span></span><br/> | <dl> <span data-ttu-id="bb427-127"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="bb427-127"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb427-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bb427-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb427-129">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="bb427-129">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="bb427-130">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="bb427-130">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
