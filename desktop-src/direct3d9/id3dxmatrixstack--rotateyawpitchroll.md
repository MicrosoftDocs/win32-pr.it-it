---
description: Ruota (rispetto allo spazio delle coordinate globali) intorno a un asse arbitrario.
ms.assetid: 25a7eff4-a575-4ddb-85eb-ef3fa2d6ae3b
title: 'Metodo ID3DXMATRIXStack:: RotateYawPitchRoll (D3dx9math. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.RotateYawPitchRoll
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5020cb6ff3af41b9ef32ef77bb71607f6cd5ea6f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322326"
---
# <a name="id3dxmatrixstackrotateyawpitchroll-method-d3dx9mathh"></a><span data-ttu-id="5bf5b-103">Metodo ID3DXMATRIXStack:: RotateYawPitchRoll (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="5bf5b-103">ID3DXMATRIXStack::RotateYawPitchRoll method (D3dx9math.h)</span></span>

<span data-ttu-id="5bf5b-104">Ruota (rispetto allo spazio delle coordinate globali) intorno a un asse arbitrario.</span><span class="sxs-lookup"><span data-stu-id="5bf5b-104">Rotates (relative to world coordinate space) around an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="5bf5b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5bf5b-105">Syntax</span></span>


```C++
HRESULT RotateYawPitchRoll(
  [in] FLOAT Yaw,
  [in] FLOAT Pitch,
  [in] FLOAT Roll
);
```



## <a name="parameters"></a><span data-ttu-id="5bf5b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5bf5b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5bf5b-107">*Imbardata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5bf5b-107">*Yaw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5bf5b-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5bf5b-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5bf5b-109">Imbardata intorno all'asse y in radianti.</span><span class="sxs-lookup"><span data-stu-id="5bf5b-109">The yaw around the y-axis in radians.</span></span>

</dd> <dt>

<span data-ttu-id="5bf5b-110">*Passo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5bf5b-110">*Pitch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5bf5b-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5bf5b-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5bf5b-112">Il passo intorno all'asse x, in radianti.</span><span class="sxs-lookup"><span data-stu-id="5bf5b-112">The pitch around the x-axis in radians.</span></span>

</dd> <dt>

<span data-ttu-id="5bf5b-113">Esegui *rollforward* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5bf5b-113">*Roll* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5bf5b-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5bf5b-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5bf5b-115">Il roll intorno all'asse z, in radianti.</span><span class="sxs-lookup"><span data-stu-id="5bf5b-115">The roll around the z-axis in radians.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5bf5b-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5bf5b-116">Return value</span></span>

<span data-ttu-id="5bf5b-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5bf5b-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5bf5b-118">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5bf5b-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="5bf5b-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="5bf5b-119">Remarks</span></span>

<span data-ttu-id="5bf5b-120">Questo metodo aggiunge la rotazione allo stack della matrice con la matrice di rotazione calcolata simile alla seguente:</span><span class="sxs-lookup"><span data-stu-id="5bf5b-120">This method adds the rotation to the matrix stack with the computed rotation matrix similar to the following:</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixRotationYawPitchRoll( &tmp, yaw, pitch, roll );
m_stack[m_currentPos] = m_stack[m_currentPos] * tmp;
```



<span data-ttu-id="5bf5b-121">Poiché la rotazione viene moltiplicata a destra nello stack della matrice, la rotazione è relativa allo spazio delle coordinate globali.</span><span class="sxs-lookup"><span data-stu-id="5bf5b-121">Because the rotation is right-multiplied to the matrix stack, the rotation is relative to world coordinate space.</span></span>

## <a name="requirements"></a><span data-ttu-id="5bf5b-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5bf5b-122">Requirements</span></span>



| <span data-ttu-id="5bf5b-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="5bf5b-123">Requirement</span></span> | <span data-ttu-id="5bf5b-124">Valore</span><span class="sxs-lookup"><span data-stu-id="5bf5b-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5bf5b-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5bf5b-125">Header</span></span><br/>  | <dl> <span data-ttu-id="5bf5b-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="5bf5b-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="5bf5b-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="5bf5b-127">Library</span></span><br/> | <dl> <span data-ttu-id="5bf5b-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5bf5b-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5bf5b-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5bf5b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5bf5b-130">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="5bf5b-130">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="5bf5b-131">**D3DXMatrixRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="5bf5b-131">**D3DXMatrixRotationAxis**</span></span>](d3dxmatrixrotationaxis.md)
</dt> <dt>

[<span data-ttu-id="5bf5b-132">**ID3DXMATRIXStack::RotateAxis**</span><span class="sxs-lookup"><span data-stu-id="5bf5b-132">**ID3DXMATRIXStack::RotateAxis**</span></span>](id3dxmatrixstack--rotateaxis.md)
</dt> <dt>

[<span data-ttu-id="5bf5b-133">**ID3DXMATRIXStack::RotateAxisLocal**</span><span class="sxs-lookup"><span data-stu-id="5bf5b-133">**ID3DXMATRIXStack::RotateAxisLocal**</span></span>](id3dxmatrixstack--rotateaxislocal.md)
</dt> <dt>

[<span data-ttu-id="5bf5b-134">**ID3DXMATRIXStack::RotateYawPitchRollLocal**</span><span class="sxs-lookup"><span data-stu-id="5bf5b-134">**ID3DXMATRIXStack::RotateYawPitchRollLocal**</span></span>](id3dxmatrixstack--rotateyawpitchrolllocal.md)
</dt> </dl>

 

 
