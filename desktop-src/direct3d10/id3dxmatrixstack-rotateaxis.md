---
description: Ruota (rispetto allo spazio delle coordinate globali) intorno a un asse arbitrario.
ms.assetid: 7c842bf6-2d13-422e-8136-0506a76ce9fe
title: 'Metodo ID3DXMATRIXStack:: RotateAxis (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.RotateAxis
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: badd26d61fa6580b0193039e29a8fceedabe2d3c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355999"
---
# <a name="id3dxmatrixstackrotateaxis-method-d3dx10h"></a><span data-ttu-id="6a594-103">Metodo ID3DXMATRIXStack:: RotateAxis (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="6a594-103">ID3DXMATRIXStack::RotateAxis method (D3DX10.h)</span></span>

<span data-ttu-id="6a594-104">Ruota (rispetto allo spazio delle coordinate globali) intorno a un asse arbitrario.</span><span class="sxs-lookup"><span data-stu-id="6a594-104">Rotates (relative to world coordinate space) around an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a594-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6a594-105">Syntax</span></span>


```C++
HRESULT RotateAxis(
  [in] const D3DXVECTOR3 *pV,
  [in]       FLOAT       Angle
);
```



## <a name="parameters"></a><span data-ttu-id="6a594-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6a594-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a594-107">*PV* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6a594-107">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a594-108">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="6a594-108">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="6a594-109">Puntatore all'asse arbitrario della rotazione.</span><span class="sxs-lookup"><span data-stu-id="6a594-109">Pointer to the arbitrary axis of rotation.</span></span> <span data-ttu-id="6a594-110">Vedere [**D3DXVECTOR3**](d3d10-d3dxvector3.md).</span><span class="sxs-lookup"><span data-stu-id="6a594-110">See [**D3DXVECTOR3**](d3d10-d3dxvector3.md).</span></span>

</dd> <dt>

<span data-ttu-id="6a594-111">*Angolo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6a594-111">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a594-112">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6a594-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6a594-113">Angolo di rotazione dell'asse arbitrario, in radianti.</span><span class="sxs-lookup"><span data-stu-id="6a594-113">Rotation angle about the arbitrary axis, in radians.</span></span> <span data-ttu-id="6a594-114">Gli angoli vengono misurati in senso antiorario quando si osserva lungo l'asse arbitrario verso l'origine.</span><span class="sxs-lookup"><span data-stu-id="6a594-114">Angles are measured counterclockwise when looking along the arbitrary axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a594-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6a594-115">Return value</span></span>

<span data-ttu-id="6a594-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6a594-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6a594-117">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6a594-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="6a594-118">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="6a594-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a594-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="6a594-119">Remarks</span></span>

<span data-ttu-id="6a594-120">Questo metodo aggiunge la rotazione allo stack della matrice con la matrice di rotazione calcolata simile alla seguente:</span><span class="sxs-lookup"><span data-stu-id="6a594-120">This method adds the rotation to the matrix stack with the computed rotation matrix similar to the following:</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixRotationAxis( &tmp, pV, angle );
m_stack[m_currentPos] = m_stack[m_currentPos] * tmp;
```



<span data-ttu-id="6a594-121">Poiché la rotazione viene moltiplicata a destra nello stack della matrice, la rotazione è relativa allo spazio delle coordinate globali.</span><span class="sxs-lookup"><span data-stu-id="6a594-121">Because the rotation is right-multiplied to the matrix stack, the rotation is relative to world coordinate space.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a594-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6a594-122">Requirements</span></span>



| <span data-ttu-id="6a594-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a594-123">Requirement</span></span> | <span data-ttu-id="6a594-124">Valore</span><span class="sxs-lookup"><span data-stu-id="6a594-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6a594-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6a594-125">Header</span></span><br/>  | <dl> <span data-ttu-id="6a594-126"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a594-126"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="6a594-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="6a594-127">Library</span></span><br/> | <dl> <span data-ttu-id="6a594-128"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6a594-128"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a594-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6a594-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a594-130">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="6a594-130">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="6a594-131">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="6a594-131">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
