---
description: Metodo ID3DXMATRIXStack::RotateYawPitchRoll (D3DX10.h) - Ruota (rispetto allo spazio delle coordinate del mondo) intorno a un asse arbitrario.
ms.assetid: 35e237f6-40f2-4001-adb0-f489d61f64e7
title: Metodo ID3DXMATRIXStack::RotateYawPitchRoll (D3DX10.h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 8c4f167f769a1ed46404028916477d6784e4a436
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107829"
---
# <a name="id3dxmatrixstackrotateyawpitchroll-method-d3dx10h"></a><span data-ttu-id="8868b-103">Metodo ID3DXMATRIXStack::RotateYawPitchRoll (D3DX10.h)</span><span class="sxs-lookup"><span data-stu-id="8868b-103">ID3DXMATRIXStack::RotateYawPitchRoll method (D3DX10.h)</span></span>

<span data-ttu-id="8868b-104">Ruota (rispetto allo spazio delle coordinate del mondo) intorno a un asse arbitrario.</span><span class="sxs-lookup"><span data-stu-id="8868b-104">Rotates (relative to world coordinate space) around an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="8868b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8868b-105">Syntax</span></span>


```C++
HRESULT RotateYawPitchRoll(
  [in] FLOAT Yaw,
  [in] FLOAT Pitch,
  [in] FLOAT Roll
);
```



## <a name="parameters"></a><span data-ttu-id="8868b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8868b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8868b-107">*Yaw* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="8868b-107">*Yaw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8868b-108">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8868b-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8868b-109">Yaw intorno all'asse y in radianti.</span><span class="sxs-lookup"><span data-stu-id="8868b-109">The yaw around the y-axis in radians.</span></span>

</dd> <dt>

<span data-ttu-id="8868b-110">*Pitch* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="8868b-110">*Pitch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8868b-111">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8868b-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8868b-112">Passo intorno all'asse x in radianti.</span><span class="sxs-lookup"><span data-stu-id="8868b-112">The pitch around the x-axis in radians.</span></span>

</dd> <dt>

<span data-ttu-id="8868b-113">*Roll* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="8868b-113">*Roll* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8868b-114">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8868b-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8868b-115">Rotazione intorno all'asse z in radianti.</span><span class="sxs-lookup"><span data-stu-id="8868b-115">The roll around the z-axis in radians.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8868b-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8868b-116">Return value</span></span>

<span data-ttu-id="8868b-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8868b-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8868b-118">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8868b-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="8868b-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="8868b-119">Remarks</span></span>

<span data-ttu-id="8868b-120">Questo metodo aggiunge la rotazione allo stack matrice con la matrice di rotazione calcolata simile alla seguente:</span><span class="sxs-lookup"><span data-stu-id="8868b-120">This method adds the rotation to the matrix stack with the computed rotation matrix similar to the following:</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixRotationYawPitchRoll( &tmp, yaw, pitch, roll );
m_stack[m_currentPos] = m_stack[m_currentPos] * tmp;
```



<span data-ttu-id="8868b-121">Poiché la rotazione viene moltiplicata a destra nello stack della matrice, la rotazione è relativa allo spazio delle coordinate del mondo.</span><span class="sxs-lookup"><span data-stu-id="8868b-121">Because the rotation is right-multiplied to the matrix stack, the rotation is relative to world coordinate space.</span></span>

## <a name="requirements"></a><span data-ttu-id="8868b-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8868b-122">Requirements</span></span>



| <span data-ttu-id="8868b-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="8868b-123">Requirement</span></span> | <span data-ttu-id="8868b-124">Valore</span><span class="sxs-lookup"><span data-stu-id="8868b-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8868b-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8868b-125">Header</span></span><br/>  | <dl> <span data-ttu-id="8868b-126"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="8868b-126"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="8868b-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="8868b-127">Library</span></span><br/> | <dl> <span data-ttu-id="8868b-128"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="8868b-128"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8868b-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8868b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8868b-130">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="8868b-130">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="8868b-131">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="8868b-131">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
