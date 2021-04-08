---
description: Imposta le proprietà di campionamento utilizzate dal simulatore di trasferimento di luminosità (PRT) pre-calcolato.
ms.assetid: a33963a7-fbcb-4e1c-a4f3-fb20a99fcf9f
title: 'Metodo ID3DXPRTEngine:: SetSamplingInfo (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetSamplingInfo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ab229652fe9e333519acce7d8474d3c4f0cf7ef9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762125"
---
# <a name="id3dxprtenginesetsamplinginfo-method"></a><span data-ttu-id="708e3-103">Metodo ID3DXPRTEngine:: SetSamplingInfo</span><span class="sxs-lookup"><span data-stu-id="708e3-103">ID3DXPRTEngine::SetSamplingInfo method</span></span>

<span data-ttu-id="708e3-104">Imposta le proprietà di campionamento utilizzate dal simulatore di trasferimento di luminosità (PRT) pre-calcolato.</span><span class="sxs-lookup"><span data-stu-id="708e3-104">Sets sampling properties used by the precomputed radiance transfer (PRT) simulator.</span></span>

## <a name="syntax"></a><span data-ttu-id="708e3-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="708e3-105">Syntax</span></span>


```C++
HRESULT SetSamplingInfo(
  [in] UINT  NumRays,
  [in] BOOL  UseSphere,
  [in] BOOL  UseCosine,
  [in] BOOL  Adaptive,
  [in] FLOAT AdaptiveThresh
);
```



## <a name="parameters"></a><span data-ttu-id="708e3-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="708e3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="708e3-107">*NumRays* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="708e3-107">*NumRays* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="708e3-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="708e3-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="708e3-109">Numero di raggi luminosi da indirizzare a ogni campione.</span><span class="sxs-lookup"><span data-stu-id="708e3-109">Number of light rays to direct at each sample.</span></span> <span data-ttu-id="708e3-110">Deve essere maggiore di zero.</span><span class="sxs-lookup"><span data-stu-id="708e3-110">Must be greater than zero.</span></span>

</dd> <dt>

<span data-ttu-id="708e3-111">*UseSphere* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="708e3-111">*UseSphere* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="708e3-112">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="708e3-112">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="708e3-113">Se **true**, gli esempi verranno calcolati su una sfera completa.</span><span class="sxs-lookup"><span data-stu-id="708e3-113">If **TRUE**, samples will be computed over a full sphere.</span></span> <span data-ttu-id="708e3-114">Se **false**, gli esempi verranno calcolati su un emisfero.</span><span class="sxs-lookup"><span data-stu-id="708e3-114">If **FALSE**, samples will be computed over a hemisphere.</span></span>

</dd> <dt>

<span data-ttu-id="708e3-115">*UseCosine* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="708e3-115">*UseCosine* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="708e3-116">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="708e3-116">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="708e3-117">Se **true**, usare una ponderazione del coseno degli esempi.</span><span class="sxs-lookup"><span data-stu-id="708e3-117">If **TRUE**, use a cosine weighting of samples.</span></span> <span data-ttu-id="708e3-118">Se UseCosine e UseSphere sono **true**, il metodo avrà esito negativo e verrà restituito un errore.</span><span class="sxs-lookup"><span data-stu-id="708e3-118">If both UseCosine and UseSphere are **TRUE**, the method will fail and an error will be returned.</span></span>

</dd> <dt>

<span data-ttu-id="708e3-119">*Adattivo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="708e3-119">*Adaptive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="708e3-120">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="708e3-120">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="708e3-121">Deve essere **false**.</span><span class="sxs-lookup"><span data-stu-id="708e3-121">Must be **FALSE**.</span></span> <span data-ttu-id="708e3-122">Il campionamento adattivo non è attualmente implementato.</span><span class="sxs-lookup"><span data-stu-id="708e3-122">Adaptive sampling is currently not implemented.</span></span>

</dd> <dt>

<span data-ttu-id="708e3-123">*AdaptiveThresh* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="708e3-123">*AdaptiveThresh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="708e3-124">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="708e3-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="708e3-125">Ignorato.</span><span class="sxs-lookup"><span data-stu-id="708e3-125">Ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="708e3-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="708e3-126">Return value</span></span>

<span data-ttu-id="708e3-127">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="708e3-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="708e3-128">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="708e3-128">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="708e3-129">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, e \_ NOTIMPL, e \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="708e3-129">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_NOTIMPL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="708e3-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="708e3-130">Requirements</span></span>



| <span data-ttu-id="708e3-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="708e3-131">Requirement</span></span> | <span data-ttu-id="708e3-132">Valore</span><span class="sxs-lookup"><span data-stu-id="708e3-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="708e3-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="708e3-133">Header</span></span><br/>  | <dl> <span data-ttu-id="708e3-134"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="708e3-134"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="708e3-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="708e3-135">Library</span></span><br/> | <dl> <span data-ttu-id="708e3-136"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="708e3-136"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="708e3-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="708e3-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="708e3-138">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="708e3-138">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 
