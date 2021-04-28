---
description: "Metodo ID3DXCompressedAnimationSet::GetCallbackKeys: riempie una matrice con i dati della chiave di callback usati per l'animazione con fotogrammi chiave."
ms.assetid: 0dc30c1f-9ffb-42ec-8074-84293f16c344
title: Metodo ID3DXCompressedAnimationSet::GetCallbackKeys (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXCompressedAnimationSet.GetCallbackKeys
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d7c430358b5ba7f66c5a79b08ae01925141e659f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115329"
---
# <a name="id3dxcompressedanimationsetgetcallbackkeys-method"></a><span data-ttu-id="841da-103">Metodo ID3DXCompressedAnimationSet::GetCallbackKeys</span><span class="sxs-lookup"><span data-stu-id="841da-103">ID3DXCompressedAnimationSet::GetCallbackKeys method</span></span>

<span data-ttu-id="841da-104">Riempie una matrice con i dati della chiave di callback usati per l'animazione con fotogrammi chiave.</span><span class="sxs-lookup"><span data-stu-id="841da-104">Fills an array with callback key data used for key frame animation.</span></span>

## <a name="syntax"></a><span data-ttu-id="841da-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="841da-105">Syntax</span></span>


```C++
HRESULT GetCallbackKeys(
  [out] LPD3DXKEY_CALLBACK pCallbackKeys
);
```



## <a name="parameters"></a><span data-ttu-id="841da-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="841da-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="841da-107">*pCallbackKeys* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="841da-107">*pCallbackKeys* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="841da-108">Tipo: **[ **CALLBACK LPD3DXKEY \_**](d3dxkey-callback.md)**</span><span class="sxs-lookup"><span data-stu-id="841da-108">Type: **[**LPD3DXKEY\_CALLBACK**](d3dxkey-callback.md)**</span></span>

<span data-ttu-id="841da-109">Puntatore a una matrice allocata dall'utente [**di strutture \_ CALLBACK D3DXKEY**](d3dxkey-callback.md) che il metodo deve riempire con i dati di callback.</span><span class="sxs-lookup"><span data-stu-id="841da-109">Pointer to a user-allocated array of [**D3DXKEY\_CALLBACK**](d3dxkey-callback.md) structures that the method is to fill with callback data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="841da-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="841da-110">Return value</span></span>

<span data-ttu-id="841da-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="841da-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="841da-112">Se il metodo ha esito positivo, il valore restituito è S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="841da-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="841da-113">Se il metodo ha esito negativo, verrà restituito il valore seguente: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="841da-113">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="841da-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="841da-114">Requirements</span></span>



| <span data-ttu-id="841da-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="841da-115">Requirement</span></span> | <span data-ttu-id="841da-116">Valore</span><span class="sxs-lookup"><span data-stu-id="841da-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="841da-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="841da-117">Header</span></span><br/>  | <dl> <span data-ttu-id="841da-118"><dt>D3dx9anim.h</dt></span><span class="sxs-lookup"><span data-stu-id="841da-118"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="841da-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="841da-119">Library</span></span><br/> | <dl> <span data-ttu-id="841da-120"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="841da-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="841da-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="841da-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="841da-122">ID3DXCompressedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="841da-122">ID3DXCompressedAnimationSet</span></span>](id3dxcompressedanimationset.md)
</dt> <dt>

[<span data-ttu-id="841da-123">**ID3DXCompressedAnimationSet::GetNumCallbackKeys**</span><span class="sxs-lookup"><span data-stu-id="841da-123">**ID3DXCompressedAnimationSet::GetNumCallbackKeys**</span></span>](id3dxcompressedanimationset--getnumcallbackkeys.md)
</dt> </dl>

 

 




