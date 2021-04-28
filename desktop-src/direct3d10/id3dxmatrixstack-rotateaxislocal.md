---
description: "Metodo ID3DXMATRIXStack::RotateAxisLocal (D3DX10.h): ruota (rispetto allo spazio delle coordinate locale dell'oggetto) intorno a un asse arbitrario."
ms.assetid: 90837762-9bfe-4065-94b3-1ca61184a78e
title: Metodo ID3DXMATRIXStack::RotateAxisLocal (D3DX10.h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 8a81a4c4bd9a2f738274f98ce925799b34986fbb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107879"
---
# <a name="id3dxmatrixstackrotateaxislocal-method-d3dx10h"></a><span data-ttu-id="f8e3f-103">Metodo ID3DXMATRIXStack::RotateAxisLocal (D3DX10.h)</span><span class="sxs-lookup"><span data-stu-id="f8e3f-103">ID3DXMATRIXStack::RotateAxisLocal method (D3DX10.h)</span></span>

<span data-ttu-id="f8e3f-104">Ruota (rispetto allo spazio delle coordinate locale dell'oggetto) intorno a un asse arbitrario.</span><span class="sxs-lookup"><span data-stu-id="f8e3f-104">Rotates (relative to the object's local coordinate space) around an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8e3f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f8e3f-105">Syntax</span></span>


```C++
HRESULT RotateAxisLocal(
  [in] const D3DXVECTOR3 *pV,
  [in]       FLOAT       Angle
);
```



## <a name="parameters"></a><span data-ttu-id="f8e3f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f8e3f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8e3f-107">*pV* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="f8e3f-107">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8e3f-108">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="f8e3f-108">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="f8e3f-109">Puntatore all'asse arbitrario di rotazione.</span><span class="sxs-lookup"><span data-stu-id="f8e3f-109">Pointer to the arbitrary axis of rotation.</span></span> <span data-ttu-id="f8e3f-110">Vedere [**D3DXVECTOR3.**](d3d10-d3dxvector3.md)</span><span class="sxs-lookup"><span data-stu-id="f8e3f-110">See [**D3DXVECTOR3**](d3d10-d3dxvector3.md).</span></span>

</dd> <dt>

<span data-ttu-id="f8e3f-111">*Angolo* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="f8e3f-111">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8e3f-112">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f8e3f-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f8e3f-113">Angolo di rotazione intorno all'asse arbitrario, espresso in radianti.</span><span class="sxs-lookup"><span data-stu-id="f8e3f-113">Rotation angle about the arbitrary axis, in radians.</span></span> <span data-ttu-id="f8e3f-114">Gli angoli vengono misurati in senso antiorario quando si guarda lungo l'asse arbitrario verso l'origine.</span><span class="sxs-lookup"><span data-stu-id="f8e3f-114">Angles are measured counterclockwise when looking along the arbitrary axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8e3f-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f8e3f-115">Return value</span></span>

<span data-ttu-id="f8e3f-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f8e3f-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f8e3f-117">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f8e3f-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="f8e3f-118">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="f8e3f-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8e3f-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="f8e3f-119">Remarks</span></span>

<span data-ttu-id="f8e3f-120">Questo metodo aggiunge la rotazione allo stack della matrice con la matrice di rotazione calcolata simile alla seguente:</span><span class="sxs-lookup"><span data-stu-id="f8e3f-120">This method adds the rotation to the matrix stack with the computed rotation matrix similar to the following:</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixRotationAxis( &tmp, pV, angle );
m_stack[m_currentPos] = tmp * m_stack[m_currentPos];
```



<span data-ttu-id="f8e3f-121">Poiché la rotazione viene moltiplicata a sinistra nello stack della matrice, la rotazione è relativa allo spazio delle coordinate locale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f8e3f-121">Because the rotation is left-multiplied to the matrix stack, the rotation is relative to the object's local coordinate space.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8e3f-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f8e3f-122">Requirements</span></span>



| <span data-ttu-id="f8e3f-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8e3f-123">Requirement</span></span> | <span data-ttu-id="f8e3f-124">Valore</span><span class="sxs-lookup"><span data-stu-id="f8e3f-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f8e3f-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f8e3f-125">Header</span></span><br/>  | <dl> <span data-ttu-id="f8e3f-126"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="f8e3f-126"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="f8e3f-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="f8e3f-127">Library</span></span><br/> | <dl> <span data-ttu-id="f8e3f-128"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="f8e3f-128"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8e3f-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f8e3f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8e3f-130">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="f8e3f-130">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="f8e3f-131">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="f8e3f-131">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
