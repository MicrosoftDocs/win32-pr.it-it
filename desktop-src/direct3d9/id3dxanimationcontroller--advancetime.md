---
description: Aggiunge un'animazione alla mesh e sposta in avanti il tempo di animazione globale in base a un importo specificato.
ms.assetid: a822d92a-c301-4289-b67b-1df99808c79d
title: 'Metodo ID3DXAnimationController:: AdvanceTime (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.AdvanceTime
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 848e1f8aadd302b9194168e92b2b0abe732a2c2f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323508"
---
# <a name="id3dxanimationcontrolleradvancetime-method"></a><span data-ttu-id="ec5df-103">Metodo ID3DXAnimationController:: AdvanceTime</span><span class="sxs-lookup"><span data-stu-id="ec5df-103">ID3DXAnimationController::AdvanceTime method</span></span>

<span data-ttu-id="ec5df-104">Aggiunge un'animazione alla mesh e sposta in avanti il tempo di animazione globale in base a un importo specificato.</span><span class="sxs-lookup"><span data-stu-id="ec5df-104">Animates the mesh and advances the global animation time by a specified amount.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec5df-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ec5df-105">Syntax</span></span>


```C++
HRESULT AdvanceTime(
  [in] DOUBLE                         TimeDelta,
  [in] LPD3DXANIMATIONCALLBACKHANDLER pCallbackHandler
);
```



## <a name="parameters"></a><span data-ttu-id="ec5df-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ec5df-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec5df-107">*TimeDelta* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ec5df-107">*TimeDelta* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec5df-108">Tipo: **[ **Double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ec5df-108">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ec5df-109">Quantità, in secondi, in base alla quale avanzare il tempo di animazione globale.</span><span class="sxs-lookup"><span data-stu-id="ec5df-109">Amount, in seconds, by which to advance the global animation time.</span></span> <span data-ttu-id="ec5df-110">Il valore di TimeDelta deve essere non negativo o zero.</span><span class="sxs-lookup"><span data-stu-id="ec5df-110">TimeDelta value must be non-negative or zero.</span></span>

</dd> <dt>

<span data-ttu-id="ec5df-111">*pCallbackHandler* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ec5df-111">*pCallbackHandler* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec5df-112">Tipo: **[ **LPD3DXANIMATIONCALLBACKHANDLER**](id3dxanimationcallbackhandler.md)**</span><span class="sxs-lookup"><span data-stu-id="ec5df-112">Type: **[**LPD3DXANIMATIONCALLBACKHANDLER**](id3dxanimationcallbackhandler.md)**</span></span>

<span data-ttu-id="ec5df-113">Puntatore a un'interfaccia del gestore di callback di animazione definita dall'utente, [**ID3DXAnimationCallbackHandler**](id3dxanimationcallbackhandler.md).</span><span class="sxs-lookup"><span data-stu-id="ec5df-113">Pointer to a user-defined animation callback handler interface, [**ID3DXAnimationCallbackHandler**](id3dxanimationcallbackhandler.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec5df-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ec5df-114">Return value</span></span>

<span data-ttu-id="ec5df-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ec5df-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ec5df-116">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ec5df-116">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="ec5df-117">Se il metodo ha esito negativo, il valore restituito può essere uno dei valori seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="ec5df-117">If the method fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec5df-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ec5df-118">Requirements</span></span>



| <span data-ttu-id="ec5df-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec5df-119">Requirement</span></span> | <span data-ttu-id="ec5df-120">Valore</span><span class="sxs-lookup"><span data-stu-id="ec5df-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ec5df-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ec5df-121">Header</span></span><br/>  | <dl> <span data-ttu-id="ec5df-122"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="ec5df-122"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="ec5df-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="ec5df-123">Library</span></span><br/> | <dl> <span data-ttu-id="ec5df-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ec5df-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ec5df-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ec5df-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec5df-126">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="ec5df-126">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
