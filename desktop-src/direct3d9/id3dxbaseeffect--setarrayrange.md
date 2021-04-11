---
description: Consente di impostare l'intervallo di una matrice da passare al dispositivo.
ms.assetid: 43f1c258-770c-4756-9033-e5667b379fe6
title: 'Metodo ID3DXBaseEffect:: SetArrayRange (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetArrayRange
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 59b981c1f2aff18d4bdb57f5726136945203f5fe
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104132286"
---
# <a name="id3dxbaseeffectsetarrayrange-method"></a><span data-ttu-id="a65f7-103">Metodo ID3DXBaseEffect:: SetArrayRange</span><span class="sxs-lookup"><span data-stu-id="a65f7-103">ID3DXBaseEffect::SetArrayRange method</span></span>

<span data-ttu-id="a65f7-104">Consente di impostare l'intervallo di una matrice da passare al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a65f7-104">Set the range of an array to pass to the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="a65f7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a65f7-105">Syntax</span></span>


```C++
HRESULT SetArrayRange(
  [in] D3DXHANDLE hParameter,
  [in] UINT       Start,
  [in] UINT       Stop
);
```



## <a name="parameters"></a><span data-ttu-id="a65f7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a65f7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a65f7-107">*hParameter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a65f7-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a65f7-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="a65f7-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="a65f7-109">Identificatore univoco.</span><span class="sxs-lookup"><span data-stu-id="a65f7-109">Unique identifier.</span></span> <span data-ttu-id="a65f7-110">Vedere [handle (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="a65f7-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="a65f7-111">*Inizio* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a65f7-111">*Start* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a65f7-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a65f7-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a65f7-113">Indice iniziale.</span><span class="sxs-lookup"><span data-stu-id="a65f7-113">Start index.</span></span>

</dd> <dt>

<span data-ttu-id="a65f7-114">*Arresta* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a65f7-114">*Stop* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a65f7-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a65f7-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a65f7-116">Arresta indice.</span><span class="sxs-lookup"><span data-stu-id="a65f7-116">Stop index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a65f7-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a65f7-117">Return value</span></span>

<span data-ttu-id="a65f7-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a65f7-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a65f7-119">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a65f7-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a65f7-120">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="a65f7-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="a65f7-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a65f7-121">Requirements</span></span>



| <span data-ttu-id="a65f7-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="a65f7-122">Requirement</span></span> | <span data-ttu-id="a65f7-123">Valore</span><span class="sxs-lookup"><span data-stu-id="a65f7-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a65f7-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a65f7-124">Header</span></span><br/>  | <dl> <span data-ttu-id="a65f7-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="a65f7-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="a65f7-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="a65f7-126">Library</span></span><br/> | <dl> <span data-ttu-id="a65f7-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a65f7-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="a65f7-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a65f7-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a65f7-129">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="a65f7-129">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 
