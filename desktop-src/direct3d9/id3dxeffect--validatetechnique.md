---
description: Convalidare una tecnica.
ms.assetid: d69eaafa-da4d-4599-86fb-83d72e1664cc
title: 'Metodo ID3DXEffect:: ValidateTechnique (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.ValidateTechnique
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b48ffa8707a3f78e76555d57225c11f89160fdd7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322351"
---
# <a name="id3dxeffectvalidatetechnique-method"></a><span data-ttu-id="a12e3-103">Metodo ID3DXEffect:: ValidateTechnique</span><span class="sxs-lookup"><span data-stu-id="a12e3-103">ID3DXEffect::ValidateTechnique method</span></span>

<span data-ttu-id="a12e3-104">Convalidare una tecnica.</span><span class="sxs-lookup"><span data-stu-id="a12e3-104">Validate a technique.</span></span>

## <a name="syntax"></a><span data-ttu-id="a12e3-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a12e3-105">Syntax</span></span>


```C++
HRESULT ValidateTechnique(
  [in] D3DXHANDLE hTechnique
);
```



## <a name="parameters"></a><span data-ttu-id="a12e3-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a12e3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a12e3-107">*hTechnique* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a12e3-107">*hTechnique* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a12e3-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="a12e3-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="a12e3-109">Identificatore univoco.</span><span class="sxs-lookup"><span data-stu-id="a12e3-109">Unique identifier.</span></span> <span data-ttu-id="a12e3-110">Vedere [handle (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="a12e3-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a12e3-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a12e3-111">Return value</span></span>

<span data-ttu-id="a12e3-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a12e3-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a12e3-113">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a12e3-113">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a12e3-114">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DERR \_ CONFLICTINGRENDERSTATE, D3DERR CONFLICTINGTEXTUREFILTER, D3DERR DEVICELOST, D3DERR DRIVERINTERNALERROR, D3DERR TOOMANYOPERATIONS, D3DERR UNSUPPORTEDALPHAARG, D3DERR UNSUPPORTEDALPHAOPERATION, D3DERR UNSUPPORTEDCOLORARG, D3DERR UNSUPPORTEDCOLOROPERATION, D3DERR UNSUPPORTEDFACTORVALUE, \_ \_ D3DERR UNSUPPORTEDTEXTUREFILTER \_ \_ \_ \_ \_ \_ \_ \_ e D3DERR WRONGTEXTUREFORMAT \_ .</span><span class="sxs-lookup"><span data-stu-id="a12e3-114">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DERR\_CONFLICTINGRENDERSTATE, D3DERR\_CONFLICTINGTEXTUREFILTER, D3DERR\_DEVICELOST, D3DERR\_DRIVERINTERNALERROR, D3DERR\_TOOMANYOPERATIONS, D3DERR\_UNSUPPORTEDALPHAARG, D3DERR\_UNSUPPORTEDALPHAOPERATION, D3DERR\_UNSUPPORTEDCOLORARG, D3DERR\_UNSUPPORTEDCOLOROPERATION, D3DERR\_UNSUPPORTEDFACTORVALUE, D3DERR\_UNSUPPORTEDTEXTUREFILTER, and D3DERR\_WRONGTEXTUREFORMAT.</span></span>

## <a name="requirements"></a><span data-ttu-id="a12e3-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a12e3-115">Requirements</span></span>



| <span data-ttu-id="a12e3-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="a12e3-116">Requirement</span></span> | <span data-ttu-id="a12e3-117">Valore</span><span class="sxs-lookup"><span data-stu-id="a12e3-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a12e3-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a12e3-118">Header</span></span><br/>  | <dl> <span data-ttu-id="a12e3-119"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="a12e3-119"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="a12e3-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="a12e3-120">Library</span></span><br/> | <dl> <span data-ttu-id="a12e3-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a12e3-121"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="a12e3-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a12e3-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a12e3-123">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="a12e3-123">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> <dt>

[<span data-ttu-id="a12e3-124">**ID3DXEffect:: setechnique**</span><span class="sxs-lookup"><span data-stu-id="a12e3-124">**ID3DXEffect::SetTechnique**</span></span>](id3dxeffect--settechnique.md)
</dt> </dl>

 

 




