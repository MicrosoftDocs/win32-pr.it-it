---
description: "Metodo ID3DXMATRIXStack::RotateYawPitchRollLocal (D3dx9math.h): ruota (rispetto allo spazio delle coordinate locale dell'oggetto) intorno a un asse arbitrario."
ms.assetid: c69f5ea7-5d14-4187-9405-1ceff8230185
title: Metodo ID3DXMATRIXStack::RotateYawPitchRollLocal (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.RotateYawPitchRollLocal
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1d104676b6d346afd527552dbfba4bac23ed09cd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093449"
---
# <a name="id3dxmatrixstackrotateyawpitchrolllocal-method-d3dx9mathh"></a><span data-ttu-id="0dd32-103">Metodo ID3DXMATRIXStack::RotateYawPitchRollLocal (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="0dd32-103">ID3DXMATRIXStack::RotateYawPitchRollLocal method (D3dx9math.h)</span></span>

<span data-ttu-id="0dd32-104">Ruota (rispetto allo spazio delle coordinate locale dell'oggetto) intorno a un asse arbitrario.</span><span class="sxs-lookup"><span data-stu-id="0dd32-104">Rotates (relative to the object's local coordinate space) around an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="0dd32-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0dd32-105">Syntax</span></span>


```C++
HRESULT RotateYawPitchRollLocal(
  [in] FLOAT Yaw,
  [in] FLOAT Pitch,
  [in] FLOAT Roll
);
```



## <a name="parameters"></a><span data-ttu-id="0dd32-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0dd32-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0dd32-107">*Yaw* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="0dd32-107">*Yaw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0dd32-108">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0dd32-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0dd32-109">Yaw intorno all'asse y in radianti.</span><span class="sxs-lookup"><span data-stu-id="0dd32-109">The yaw around the y-axis in radians.</span></span>

</dd> <dt>

<span data-ttu-id="0dd32-110">*Tono* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="0dd32-110">*Pitch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0dd32-111">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0dd32-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0dd32-112">Passo intorno all'asse x in radianti.</span><span class="sxs-lookup"><span data-stu-id="0dd32-112">The pitch around the x-axis in radians.</span></span>

</dd> <dt>

<span data-ttu-id="0dd32-113">*Roll* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="0dd32-113">*Roll* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0dd32-114">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0dd32-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0dd32-115">Rullo intorno all'asse z in radianti.</span><span class="sxs-lookup"><span data-stu-id="0dd32-115">The roll around the z-axis in radians.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0dd32-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0dd32-116">Return value</span></span>

<span data-ttu-id="0dd32-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0dd32-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0dd32-118">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0dd32-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="0dd32-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="0dd32-119">Remarks</span></span>

<span data-ttu-id="0dd32-120">Questo metodo aggiunge la rotazione allo stack della matrice con la matrice di rotazione calcolata simile alla seguente:</span><span class="sxs-lookup"><span data-stu-id="0dd32-120">This method adds the rotation to the matrix stack with the computed rotation matrix similar to the following:</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixRotationYawPitchRoll( &tmp, yaw, pitch, roll );
m_stack[m_currentPos] = tmp * m_stack[m_currentPos];
```



<span data-ttu-id="0dd32-121">Poiché la rotazione viene moltiplicata a sinistra nello stack della matrice, la rotazione è relativa allo spazio delle coordinate locale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="0dd32-121">Because the rotation is left-multiplied to the matrix stack, the rotation is relative to the object's local coordinate space.</span></span>

## <a name="requirements"></a><span data-ttu-id="0dd32-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0dd32-122">Requirements</span></span>



| <span data-ttu-id="0dd32-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="0dd32-123">Requirement</span></span> | <span data-ttu-id="0dd32-124">Valore</span><span class="sxs-lookup"><span data-stu-id="0dd32-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0dd32-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0dd32-125">Header</span></span><br/>  | <dl> <span data-ttu-id="0dd32-126"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="0dd32-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="0dd32-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="0dd32-127">Library</span></span><br/> | <dl> <span data-ttu-id="0dd32-128"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="0dd32-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0dd32-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0dd32-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0dd32-130">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="0dd32-130">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="0dd32-131">**D3DXMatrixRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="0dd32-131">**D3DXMatrixRotationAxis**</span></span>](d3dxmatrixrotationaxis.md)
</dt> <dt>

[<span data-ttu-id="0dd32-132">**ID3DXMATRIXStack::RotateAxis**</span><span class="sxs-lookup"><span data-stu-id="0dd32-132">**ID3DXMATRIXStack::RotateAxis**</span></span>](id3dxmatrixstack--rotateaxis.md)
</dt> <dt>

[<span data-ttu-id="0dd32-133">**ID3DXMATRIXStack::RotateAxisLocal**</span><span class="sxs-lookup"><span data-stu-id="0dd32-133">**ID3DXMATRIXStack::RotateAxisLocal**</span></span>](id3dxmatrixstack--rotateaxislocal.md)
</dt> <dt>

[<span data-ttu-id="0dd32-134">**ID3DXMATRIXStack::RotateYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="0dd32-134">**ID3DXMATRIXStack::RotateYawPitchRoll**</span></span>](id3dxmatrixstack--rotateyawpitchroll.md)
</dt> </dl>

 

 
