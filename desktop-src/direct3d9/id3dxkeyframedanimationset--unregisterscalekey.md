---
description: Rimuove i dati della scala in corrispondenza del fotogramma chiave specificato.
ms.assetid: b0bf5665-ccfb-4b87-8e88-9a717ef57955
title: 'Metodo ID3DXKeyframedAnimationSet:: UnregisterScaleKey (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.UnregisterScaleKey
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6d1ac3f500b80d8922646fddff9f05d8c91d9c48
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969494"
---
# <a name="id3dxkeyframedanimationsetunregisterscalekey-method"></a><span data-ttu-id="a2e14-103">Metodo ID3DXKeyframedAnimationSet:: UnregisterScaleKey</span><span class="sxs-lookup"><span data-stu-id="a2e14-103">ID3DXKeyframedAnimationSet::UnregisterScaleKey method</span></span>

<span data-ttu-id="a2e14-104">Rimuove i dati della scala in corrispondenza del fotogramma chiave specificato.</span><span class="sxs-lookup"><span data-stu-id="a2e14-104">Removes the scale data at the specified key frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2e14-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a2e14-105">Syntax</span></span>


```C++
HRESULT UnregisterScaleKey(
  [in] UINT Animation,
  [in] UINT Key
);
```



## <a name="parameters"></a><span data-ttu-id="a2e14-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a2e14-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2e14-107">*Animazione* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="a2e14-107">*Animation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2e14-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a2e14-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a2e14-109">Identificatore dell'animazione.</span><span class="sxs-lookup"><span data-stu-id="a2e14-109">Animation identifier.</span></span>

</dd> <dt>

<span data-ttu-id="a2e14-110">*Chiave* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="a2e14-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2e14-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a2e14-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a2e14-112">Fotogramma chiave.</span><span class="sxs-lookup"><span data-stu-id="a2e14-112">Key frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2e14-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a2e14-113">Return value</span></span>

<span data-ttu-id="a2e14-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a2e14-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a2e14-115">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a2e14-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="a2e14-116">Se il metodo ha esito negativo, verrà restituito il valore seguente: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="a2e14-116">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="a2e14-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="a2e14-117">Remarks</span></span>

<span data-ttu-id="a2e14-118">Questo metodo è lento e non deve essere usato dopo che è iniziata la riproduzione di un'animazione.</span><span class="sxs-lookup"><span data-stu-id="a2e14-118">This method is slow and should not be used after an animation has begun to play.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2e14-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a2e14-119">Requirements</span></span>



| <span data-ttu-id="a2e14-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2e14-120">Requirement</span></span> | <span data-ttu-id="a2e14-121">Valore</span><span class="sxs-lookup"><span data-stu-id="a2e14-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a2e14-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a2e14-122">Header</span></span><br/>  | <dl> <span data-ttu-id="a2e14-123"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2e14-123"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="a2e14-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="a2e14-124">Library</span></span><br/> | <dl> <span data-ttu-id="a2e14-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a2e14-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a2e14-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a2e14-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2e14-127">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="a2e14-127">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
