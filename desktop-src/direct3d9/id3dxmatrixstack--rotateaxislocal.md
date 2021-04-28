---
description: Metodo ID3DXMATRIXStack::RotateAxisLocal (D3dx9math.h) - Ruota (rispetto allo spazio delle coordinate locale dell'oggetto) intorno a un asse arbitrario.
ms.assetid: c7ef11e9-f4c4-4801-8f25-190066baeb52
title: Metodo ID3DXMATRIXStack::RotateAxisLocal (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.RotateAxisLocal
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0bfcfd7301f90dcf49b03e7bbb3fd7e3b0de6c3e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093469"
---
# <a name="id3dxmatrixstackrotateaxislocal-method-d3dx9mathh"></a><span data-ttu-id="75c75-103">Metodo ID3DXMATRIXStack::RotateAxisLocal (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="75c75-103">ID3DXMATRIXStack::RotateAxisLocal method (D3dx9math.h)</span></span>

<span data-ttu-id="75c75-104">Ruota (rispetto allo spazio delle coordinate locale dell'oggetto) intorno a un asse arbitrario.</span><span class="sxs-lookup"><span data-stu-id="75c75-104">Rotates (relative to the object's local coordinate space) around an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="75c75-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="75c75-105">Syntax</span></span>


```C++
HRESULT RotateAxisLocal(
  [in] const D3DXVECTOR3 *pV,
  [in]       FLOAT       Angle
);
```



## <a name="parameters"></a><span data-ttu-id="75c75-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="75c75-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75c75-107">*pV* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="75c75-107">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75c75-108">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="75c75-108">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="75c75-109">Puntatore all'asse arbitrario di rotazione.</span><span class="sxs-lookup"><span data-stu-id="75c75-109">Pointer to the arbitrary axis of rotation.</span></span> <span data-ttu-id="75c75-110">Vedere [**D3DXVECTOR3**](d3dxvector3.md).</span><span class="sxs-lookup"><span data-stu-id="75c75-110">See [**D3DXVECTOR3**](d3dxvector3.md).</span></span>

</dd> <dt>

<span data-ttu-id="75c75-111">*Angolo* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="75c75-111">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75c75-112">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="75c75-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="75c75-113">Angolo di rotazione intorno all'asse arbitrario, espresso in radianti.</span><span class="sxs-lookup"><span data-stu-id="75c75-113">Rotation angle about the arbitrary axis, in radians.</span></span> <span data-ttu-id="75c75-114">Gli angoli vengono misurati in senso antiorario quando si cerca lungo l'asse arbitrario verso l'origine.</span><span class="sxs-lookup"><span data-stu-id="75c75-114">Angles are measured counterclockwise when looking along the arbitrary axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75c75-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="75c75-115">Return value</span></span>

<span data-ttu-id="75c75-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="75c75-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="75c75-117">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="75c75-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="75c75-118">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="75c75-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="75c75-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="75c75-119">Remarks</span></span>

<span data-ttu-id="75c75-120">Questo metodo aggiunge la rotazione allo stack di matrici con la matrice di rotazione calcolata simile alla seguente:</span><span class="sxs-lookup"><span data-stu-id="75c75-120">This method adds the rotation to the matrix stack with the computed rotation matrix similar to the following:</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixRotationAxis( &tmp, pV, angle );
m_stack[m_currentPos] = tmp * m_stack[m_currentPos];
```



<span data-ttu-id="75c75-121">Poiché la rotazione viene moltiplicata a sinistra nello stack della matrice, la rotazione è relativa allo spazio delle coordinate locale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="75c75-121">Because the rotation is left-multiplied to the matrix stack, the rotation is relative to the object's local coordinate space.</span></span>

## <a name="requirements"></a><span data-ttu-id="75c75-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="75c75-122">Requirements</span></span>



| <span data-ttu-id="75c75-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="75c75-123">Requirement</span></span> | <span data-ttu-id="75c75-124">Valore</span><span class="sxs-lookup"><span data-stu-id="75c75-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="75c75-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="75c75-125">Header</span></span><br/>  | <dl> <span data-ttu-id="75c75-126"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="75c75-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="75c75-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="75c75-127">Library</span></span><br/> | <dl> <span data-ttu-id="75c75-128"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="75c75-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="75c75-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="75c75-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75c75-130">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="75c75-130">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="75c75-131">**D3DXMatrixRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="75c75-131">**D3DXMatrixRotationAxis**</span></span>](d3dxmatrixrotationaxis.md)
</dt> <dt>

[<span data-ttu-id="75c75-132">**ID3DXMATRIXStack::RotateAxis**</span><span class="sxs-lookup"><span data-stu-id="75c75-132">**ID3DXMATRIXStack::RotateAxis**</span></span>](id3dxmatrixstack--rotateaxis.md)
</dt> <dt>

[<span data-ttu-id="75c75-133">**ID3DXMATRIXStack::RotateYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="75c75-133">**ID3DXMATRIXStack::RotateYawPitchRoll**</span></span>](id3dxmatrixstack--rotateyawpitchroll.md)
</dt> <dt>

[<span data-ttu-id="75c75-134">**ID3DXMATRIXStack::RotateYawPitchRollLocal**</span><span class="sxs-lookup"><span data-stu-id="75c75-134">**ID3DXMATRIXStack::RotateYawPitchRollLocal**</span></span>](id3dxmatrixstack--rotateyawpitchrolllocal.md)
</dt> </dl>

 

 
