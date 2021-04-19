---
description: Compila una matrice con i dati della chiave di conversione utilizzati per l'animazione del fotogramma chiave.
ms.assetid: ecb791ad-e586-4057-9239-facd37a47637
title: 'Metodo ID3DXKeyframedAnimationSet:: GetTranslationKeys (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.GetTranslationKeys
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d6cc56e5538eb45c01ba7c35115e94719119bc4e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323496"
---
# <a name="id3dxkeyframedanimationsetgettranslationkeys-method"></a><span data-ttu-id="761d8-103">Metodo ID3DXKeyframedAnimationSet:: GetTranslationKeys</span><span class="sxs-lookup"><span data-stu-id="761d8-103">ID3DXKeyframedAnimationSet::GetTranslationKeys method</span></span>

<span data-ttu-id="761d8-104">Compila una matrice con i dati della chiave di conversione utilizzati per l'animazione del fotogramma chiave.</span><span class="sxs-lookup"><span data-stu-id="761d8-104">Fills an array with translational key data used for key frame animation.</span></span>

## <a name="syntax"></a><span data-ttu-id="761d8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="761d8-105">Syntax</span></span>


```C++
HRESULT GetTranslationKeys(
  [in] UINT              Animation,
  [in] LPD3DXKEY_VECTOR3 pTranslationKeys
);
```



## <a name="parameters"></a><span data-ttu-id="761d8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="761d8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="761d8-107">*Animazione* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="761d8-107">*Animation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="761d8-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="761d8-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="761d8-109">Indice di animazione.</span><span class="sxs-lookup"><span data-stu-id="761d8-109">Animation index.</span></span>

</dd> <dt>

<span data-ttu-id="761d8-110">*pTranslationKeys* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="761d8-110">*pTranslationKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="761d8-111">Tipo: **[ **LPD3DXKEY \_ VECTOR3**](d3dxkey-vector3.md)**</span><span class="sxs-lookup"><span data-stu-id="761d8-111">Type: **[**LPD3DXKEY\_VECTOR3**](d3dxkey-vector3.md)**</span></span>

<span data-ttu-id="761d8-112">Puntatore a una matrice allocata dall'utente di vettori [**D3DXKEY \_ VECTOR3**](d3dxkey-vector3.md) che il metodo deve compilare con i dati di conversione dell'animazione.</span><span class="sxs-lookup"><span data-stu-id="761d8-112">Pointer to a user-allocated array of [**D3DXKEY\_VECTOR3**](d3dxkey-vector3.md) vectors that the method is to fill with animation translation data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="761d8-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="761d8-113">Return value</span></span>

<span data-ttu-id="761d8-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="761d8-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="761d8-115">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="761d8-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="761d8-116">Se il metodo ha esito negativo, verrà restituito il valore seguente: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="761d8-116">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="761d8-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="761d8-117">Requirements</span></span>



| <span data-ttu-id="761d8-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="761d8-118">Requirement</span></span> | <span data-ttu-id="761d8-119">Valore</span><span class="sxs-lookup"><span data-stu-id="761d8-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="761d8-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="761d8-120">Header</span></span><br/>  | <dl> <span data-ttu-id="761d8-121"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="761d8-121"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="761d8-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="761d8-122">Library</span></span><br/> | <dl> <span data-ttu-id="761d8-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="761d8-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="761d8-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="761d8-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="761d8-125">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="761d8-125">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> <dt>

[<span data-ttu-id="761d8-126">**ID3DXKeyframedAnimationSet::GetNumTranslationKeys**</span><span class="sxs-lookup"><span data-stu-id="761d8-126">**ID3DXKeyframedAnimationSet::GetNumTranslationKeys**</span></span>](id3dxkeyframedanimationset--getnumtranslationkeys.md)
</dt> </dl>

 

 
