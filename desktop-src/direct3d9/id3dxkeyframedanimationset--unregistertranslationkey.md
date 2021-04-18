---
description: Rimuove i dati di traduzione in corrispondenza del fotogramma chiave specificato.
ms.assetid: 58cadf5d-f687-4644-83b0-e124ef2bcb5a
title: 'Metodo ID3DXKeyframedAnimationSet:: UnregisterTranslationKey (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.UnregisterTranslationKey
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 127aaa707c364e51815af09b8222d73102281b10
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323481"
---
# <a name="id3dxkeyframedanimationsetunregistertranslationkey-method"></a><span data-ttu-id="3d8f6-103">Metodo ID3DXKeyframedAnimationSet:: UnregisterTranslationKey</span><span class="sxs-lookup"><span data-stu-id="3d8f6-103">ID3DXKeyframedAnimationSet::UnregisterTranslationKey method</span></span>

<span data-ttu-id="3d8f6-104">Rimuove i dati di traduzione in corrispondenza del fotogramma chiave specificato.</span><span class="sxs-lookup"><span data-stu-id="3d8f6-104">Removes the translation data at the specified key frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d8f6-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3d8f6-105">Syntax</span></span>


```C++
HRESULT UnregisterTranslationKey(
  [in] UINT Animation,
  [in] UINT Key
);
```



## <a name="parameters"></a><span data-ttu-id="3d8f6-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3d8f6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d8f6-107">*Animazione* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="3d8f6-107">*Animation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d8f6-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3d8f6-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3d8f6-109">Identificatore dell'animazione.</span><span class="sxs-lookup"><span data-stu-id="3d8f6-109">Animation identifier.</span></span>

</dd> <dt>

<span data-ttu-id="3d8f6-110">*Chiave* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="3d8f6-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d8f6-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3d8f6-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3d8f6-112">Fotogramma chiave.</span><span class="sxs-lookup"><span data-stu-id="3d8f6-112">Key frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d8f6-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3d8f6-113">Return value</span></span>

<span data-ttu-id="3d8f6-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3d8f6-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3d8f6-115">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3d8f6-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="3d8f6-116">Se il metodo ha esito negativo, verrà restituito il valore seguente: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="3d8f6-116">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d8f6-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="3d8f6-117">Remarks</span></span>

<span data-ttu-id="3d8f6-118">Questo metodo è lento e non deve essere usato dopo che è iniziata la riproduzione di un'animazione.</span><span class="sxs-lookup"><span data-stu-id="3d8f6-118">This method is slow and should not be used after an animation has begun to play.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d8f6-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3d8f6-119">Requirements</span></span>



| <span data-ttu-id="3d8f6-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d8f6-120">Requirement</span></span> | <span data-ttu-id="3d8f6-121">Valore</span><span class="sxs-lookup"><span data-stu-id="3d8f6-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3d8f6-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3d8f6-122">Header</span></span><br/>  | <dl> <span data-ttu-id="3d8f6-123"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="3d8f6-123"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="3d8f6-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="3d8f6-124">Library</span></span><br/> | <dl> <span data-ttu-id="3d8f6-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3d8f6-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3d8f6-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3d8f6-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d8f6-127">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="3d8f6-127">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
