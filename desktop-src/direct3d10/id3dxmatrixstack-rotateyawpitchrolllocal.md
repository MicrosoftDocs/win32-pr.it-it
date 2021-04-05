---
description: Ruota (relativo allo spazio delle coordinate locali dell'oggetto) intorno a un asse arbitrario.
ms.assetid: da023816-5176-460d-ab6b-909b89cc46cd
title: 'Metodo ID3DXMATRIXStack:: RotateYawPitchRollLocal (D3DX10. h)'
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 2a7b9e08adb7e66f78b3823c71e07fadfd561201
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762370"
---
# <a name="id3dxmatrixstackrotateyawpitchrolllocal-method-d3dx10h"></a><span data-ttu-id="b1461-103">Metodo ID3DXMATRIXStack:: RotateYawPitchRollLocal (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="b1461-103">ID3DXMATRIXStack::RotateYawPitchRollLocal method (D3DX10.h)</span></span>

<span data-ttu-id="b1461-104">Ruota (relativo allo spazio delle coordinate locali dell'oggetto) intorno a un asse arbitrario.</span><span class="sxs-lookup"><span data-stu-id="b1461-104">Rotates (relative to the object's local coordinate space) around an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1461-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b1461-105">Syntax</span></span>


```C++
HRESULT RotateYawPitchRollLocal(
  [in] FLOAT Yaw,
  [in] FLOAT Pitch,
  [in] FLOAT Roll
);
```



## <a name="parameters"></a><span data-ttu-id="b1461-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b1461-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1461-107">*Imbardata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b1461-107">*Yaw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1461-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b1461-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b1461-109">Imbardata intorno all'asse y in radianti.</span><span class="sxs-lookup"><span data-stu-id="b1461-109">The yaw around the y-axis in radians.</span></span>

</dd> <dt>

<span data-ttu-id="b1461-110">*Passo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b1461-110">*Pitch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1461-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b1461-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b1461-112">Il passo intorno all'asse x, in radianti.</span><span class="sxs-lookup"><span data-stu-id="b1461-112">The pitch around the x-axis in radians.</span></span>

</dd> <dt>

<span data-ttu-id="b1461-113">Esegui *rollforward* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b1461-113">*Roll* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1461-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b1461-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b1461-115">Il roll intorno all'asse z, in radianti.</span><span class="sxs-lookup"><span data-stu-id="b1461-115">The roll around the z-axis in radians.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1461-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b1461-116">Return value</span></span>

<span data-ttu-id="b1461-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b1461-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b1461-118">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b1461-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="b1461-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="b1461-119">Remarks</span></span>

<span data-ttu-id="b1461-120">Questo metodo aggiunge la rotazione allo stack della matrice con la matrice di rotazione calcolata simile alla seguente:</span><span class="sxs-lookup"><span data-stu-id="b1461-120">This method adds the rotation to the matrix stack with the computed rotation matrix similar to the following:</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixRotationYawPitchRoll( &tmp, yaw, pitch, roll );
m_stack[m_currentPos] = tmp * m_stack[m_currentPos];
```



<span data-ttu-id="b1461-121">Poiché la rotazione viene moltiplicata a sinistra nello stack della matrice, la rotazione è relativa allo spazio delle coordinate locali dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b1461-121">Because the rotation is left-multiplied to the matrix stack, the rotation is relative to the object's local coordinate space.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1461-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b1461-122">Requirements</span></span>



| <span data-ttu-id="b1461-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1461-123">Requirement</span></span> | <span data-ttu-id="b1461-124">Valore</span><span class="sxs-lookup"><span data-stu-id="b1461-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b1461-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b1461-125">Header</span></span><br/>  | <dl> <span data-ttu-id="b1461-126"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1461-126"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="b1461-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="b1461-127">Library</span></span><br/> | <dl> <span data-ttu-id="b1461-128"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b1461-128"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1461-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b1461-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1461-130">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="b1461-130">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="b1461-131">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="b1461-131">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
