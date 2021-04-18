---
description: Ruota (rispetto allo spazio delle coordinate globali) intorno a un asse arbitrario.
ms.assetid: b7ae5195-a2af-429f-9a0d-51cd7e955362
title: 'Metodo ID3DXMATRIXStack:: RotateAxis (D3dx9math. h)'
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 476b8e01da6265e9bdf4642d24647d0e804949d6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322332"
---
# <a name="id3dxmatrixstackrotateaxis-method-d3dx9mathh"></a><span data-ttu-id="47d17-103">Metodo ID3DXMATRIXStack:: RotateAxis (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="47d17-103">ID3DXMATRIXStack::RotateAxis method (D3dx9math.h)</span></span>

<span data-ttu-id="47d17-104">Ruota (rispetto allo spazio delle coordinate globali) intorno a un asse arbitrario.</span><span class="sxs-lookup"><span data-stu-id="47d17-104">Rotates (relative to world coordinate space) around an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="47d17-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="47d17-105">Syntax</span></span>


```C++
HRESULT RotateAxis(
  [in] const D3DXVECTOR3 *pV,
  [in]       FLOAT       Angle
);
```



## <a name="parameters"></a><span data-ttu-id="47d17-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="47d17-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47d17-107">*PV* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="47d17-107">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47d17-108">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="47d17-108">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="47d17-109">Puntatore all'asse arbitrario della rotazione.</span><span class="sxs-lookup"><span data-stu-id="47d17-109">Pointer to the arbitrary axis of rotation.</span></span> <span data-ttu-id="47d17-110">Vedere [**D3DXVECTOR3**](d3dxvector3.md).</span><span class="sxs-lookup"><span data-stu-id="47d17-110">See [**D3DXVECTOR3**](d3dxvector3.md).</span></span>

</dd> <dt>

<span data-ttu-id="47d17-111">*Angolo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="47d17-111">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47d17-112">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="47d17-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="47d17-113">Angolo di rotazione dell'asse arbitrario, in radianti.</span><span class="sxs-lookup"><span data-stu-id="47d17-113">Rotation angle about the arbitrary axis, in radians.</span></span> <span data-ttu-id="47d17-114">Gli angoli vengono misurati in senso antiorario quando si osserva lungo l'asse arbitrario verso l'origine.</span><span class="sxs-lookup"><span data-stu-id="47d17-114">Angles are measured counterclockwise when looking along the arbitrary axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47d17-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="47d17-115">Return value</span></span>

<span data-ttu-id="47d17-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="47d17-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="47d17-117">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="47d17-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="47d17-118">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="47d17-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="47d17-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="47d17-119">Remarks</span></span>

<span data-ttu-id="47d17-120">Questo metodo aggiunge la rotazione allo stack della matrice con la matrice di rotazione calcolata simile alla seguente:</span><span class="sxs-lookup"><span data-stu-id="47d17-120">This method adds the rotation to the matrix stack with the computed rotation matrix similar to the following:</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixRotationAxis( &tmp, pV, angle );
m_stack[m_currentPos] = m_stack[m_currentPos] * tmp;
```



<span data-ttu-id="47d17-121">Poiché la rotazione viene moltiplicata a destra nello stack della matrice, la rotazione è relativa allo spazio delle coordinate globali.</span><span class="sxs-lookup"><span data-stu-id="47d17-121">Because the rotation is right-multiplied to the matrix stack, the rotation is relative to world coordinate space.</span></span>

## <a name="requirements"></a><span data-ttu-id="47d17-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="47d17-122">Requirements</span></span>



| <span data-ttu-id="47d17-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="47d17-123">Requirement</span></span> | <span data-ttu-id="47d17-124">Valore</span><span class="sxs-lookup"><span data-stu-id="47d17-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="47d17-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="47d17-125">Header</span></span><br/>  | <dl> <span data-ttu-id="47d17-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="47d17-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="47d17-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="47d17-127">Library</span></span><br/> | <dl> <span data-ttu-id="47d17-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="47d17-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="47d17-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="47d17-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47d17-130">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="47d17-130">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="47d17-131">**D3DXMatrixRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="47d17-131">**D3DXMatrixRotationAxis**</span></span>](d3dxmatrixrotationaxis.md)
</dt> <dt>

[<span data-ttu-id="47d17-132">**ID3DXMATRIXStack::RotateAxisLocal**</span><span class="sxs-lookup"><span data-stu-id="47d17-132">**ID3DXMATRIXStack::RotateAxisLocal**</span></span>](id3dxmatrixstack--rotateaxislocal.md)
</dt> <dt>

[<span data-ttu-id="47d17-133">**ID3DXMATRIXStack::RotateYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="47d17-133">**ID3DXMATRIXStack::RotateYawPitchRoll**</span></span>](id3dxmatrixstack--rotateyawpitchroll.md)
</dt> <dt>

[<span data-ttu-id="47d17-134">**ID3DXMATRIXStack::RotateYawPitchRollLocal**</span><span class="sxs-lookup"><span data-stu-id="47d17-134">**ID3DXMATRIXStack::RotateYawPitchRollLocal**</span></span>](id3dxmatrixstack--rotateyawpitchrolllocal.md)
</dt> </dl>

 

 
