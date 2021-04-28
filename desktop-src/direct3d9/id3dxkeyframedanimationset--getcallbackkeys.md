---
description: "Metodo ID3DXKeyframedAnimationSet::GetCallbackKeys: riempie una matrice con i dati della chiave di callback usati per l'animazione con fotogrammi chiave."
ms.assetid: 2a2aa04a-a889-415b-8aa2-cc5f2bed1f9a
title: Metodo ID3DXKeyframedAnimationSet::GetCallbackKeys (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.GetCallbackKeys
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5f3bdb7049de3b5d6aad10b5ff5100d01d05e3ee
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093719"
---
# <a name="id3dxkeyframedanimationsetgetcallbackkeys-method"></a><span data-ttu-id="619f7-103">Metodo ID3DXKeyframedAnimationSet::GetCallbackKeys</span><span class="sxs-lookup"><span data-stu-id="619f7-103">ID3DXKeyframedAnimationSet::GetCallbackKeys method</span></span>

<span data-ttu-id="619f7-104">Riempie una matrice con i dati chiave di callback usati per l'animazione del fotogramma chiave.</span><span class="sxs-lookup"><span data-stu-id="619f7-104">Fills an array with callback key data used for key frame animation.</span></span>

## <a name="syntax"></a><span data-ttu-id="619f7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="619f7-105">Syntax</span></span>


```C++
HRESULT GetCallbackKeys(
  [out] LPD3DXKEY_CALLBACK pCallbackKeys
);
```



## <a name="parameters"></a><span data-ttu-id="619f7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="619f7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="619f7-107">*pCallbackKeys* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="619f7-107">*pCallbackKeys* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="619f7-108">Tipo: **[ **CALLBACK LPD3DXKEY \_**](d3dxkey-callback.md)**</span><span class="sxs-lookup"><span data-stu-id="619f7-108">Type: **[**LPD3DXKEY\_CALLBACK**](d3dxkey-callback.md)**</span></span>

<span data-ttu-id="619f7-109">Puntatore a una matrice allocata dall'utente di [**strutture \_ CALLBACK D3DXKEY**](d3dxkey-callback.md) che il metodo deve riempire con i dati di callback.</span><span class="sxs-lookup"><span data-stu-id="619f7-109">Pointer to a user-allocated array of [**D3DXKEY\_CALLBACK**](d3dxkey-callback.md) structures that the method is to fill with callback data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="619f7-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="619f7-110">Return value</span></span>

<span data-ttu-id="619f7-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="619f7-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="619f7-112">Se il metodo ha esito positivo, il valore restituito è S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="619f7-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="619f7-113">Se il metodo ha esito negativo, verrà restituito il valore seguente: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="619f7-113">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="619f7-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="619f7-114">Requirements</span></span>



| <span data-ttu-id="619f7-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="619f7-115">Requirement</span></span> | <span data-ttu-id="619f7-116">Valore</span><span class="sxs-lookup"><span data-stu-id="619f7-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="619f7-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="619f7-117">Header</span></span><br/>  | <dl> <span data-ttu-id="619f7-118"><dt>D3dx9anim.h</dt></span><span class="sxs-lookup"><span data-stu-id="619f7-118"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="619f7-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="619f7-119">Library</span></span><br/> | <dl> <span data-ttu-id="619f7-120"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="619f7-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="619f7-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="619f7-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="619f7-122">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="619f7-122">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> <dt>

[<span data-ttu-id="619f7-123">**ID3DXKeyframedAnimationSet::GetNumCallbackKeys**</span><span class="sxs-lookup"><span data-stu-id="619f7-123">**ID3DXKeyframedAnimationSet::GetNumCallbackKeys**</span></span>](id3dxkeyframedanimationset--getnumcallbackkeys.md)
</dt> </dl>

 

 




