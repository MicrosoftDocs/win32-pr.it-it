---
description: Termina un passaggio attivo.
ms.assetid: e20b3e0f-db9f-48e8-ab4e-761a5861f3ce
title: 'Metodo ID3DXEffect:: EndPass (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.EndPass
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 5cdba799f282e56bbe4565a4792906fd835e5c6c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355009"
---
# <a name="id3dxeffectendpass-method"></a><span data-ttu-id="fa4d6-103">Metodo ID3DXEffect:: EndPass</span><span class="sxs-lookup"><span data-stu-id="fa4d6-103">ID3DXEffect::EndPass method</span></span>

<span data-ttu-id="fa4d6-104">Termina un passaggio attivo.</span><span class="sxs-lookup"><span data-stu-id="fa4d6-104">End an active pass.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa4d6-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fa4d6-105">Syntax</span></span>


```C++
HRESULT EndPass();
```



## <a name="parameters"></a><span data-ttu-id="fa4d6-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="fa4d6-106">Parameters</span></span>

<span data-ttu-id="fa4d6-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="fa4d6-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fa4d6-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fa4d6-108">Return value</span></span>

<span data-ttu-id="fa4d6-109">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fa4d6-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fa4d6-110">Questo metodo restituisce sempre il valore S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="fa4d6-110">This method always returns the value S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa4d6-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="fa4d6-111">Remarks</span></span>

<span data-ttu-id="fa4d6-112">Un'applicazione segnala la fine del rendering di un passaggio attivo chiamando **ID3DXEffect:: EndPass**.</span><span class="sxs-lookup"><span data-stu-id="fa4d6-112">An application signals the end of rendering an active pass by calling **ID3DXEffect::EndPass**.</span></span> <span data-ttu-id="fa4d6-113">Ogni **ID3DXEffect:: EndPass** deve far parte di una coppia corrispondente di chiamate a [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md) e **ID3DXEffect:: EndPass** .</span><span class="sxs-lookup"><span data-stu-id="fa4d6-113">Each **ID3DXEffect::EndPass** must be part of a matching pair of [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md) and **ID3DXEffect::EndPass** calls.</span></span>

<span data-ttu-id="fa4d6-114">Ogni coppia corrispondente di chiamate [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md) e **ID3DXEffect:: EndPass** deve trovarsi all'interno di una coppia corrispondente di chiamate a [**ID3DXEffect:: Begin**](id3dxeffect--begin.md) e [**ID3DXEffect:: end**](id3dxeffect--end.md) .</span><span class="sxs-lookup"><span data-stu-id="fa4d6-114">Each matching pair of [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md) and **ID3DXEffect::EndPass** calls must be located within a matching pair of [**ID3DXEffect::Begin**](id3dxeffect--begin.md) and [**ID3DXEffect::End**](id3dxeffect--end.md) calls.</span></span>

<span data-ttu-id="fa4d6-115">Se l'applicazione modifica uno stato di effetto usando uno dei metodi [**Effect:: SETX**](id3dxeffect.md) all'interno di una coppia [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md) / **ID3DXEffect:: EndPass** matching, l'applicazione deve chiamare [**ID3DXEffect:: CommitChanges**](id3dxeffect--commitchanges.md) prima di qualsiasi chiamata DrawxPrimitive per propagare le modifiche di stato al dispositivo prima del rendering.</span><span class="sxs-lookup"><span data-stu-id="fa4d6-115">If the application changes any effect state using any of the [**Effect::Setx**](id3dxeffect.md) methods inside of a [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md)/**ID3DXEffect::EndPass** matching pair, the application must call [**ID3DXEffect::CommitChanges**](id3dxeffect--commitchanges.md) before any DrawxPrimitive call to propagate state changes to the device before rendering.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa4d6-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fa4d6-116">Requirements</span></span>



| <span data-ttu-id="fa4d6-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa4d6-117">Requirement</span></span> | <span data-ttu-id="fa4d6-118">Valore</span><span class="sxs-lookup"><span data-stu-id="fa4d6-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa4d6-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fa4d6-119">Header</span></span><br/>  | <dl> <span data-ttu-id="fa4d6-120"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="fa4d6-120"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="fa4d6-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="fa4d6-121">Library</span></span><br/> | <dl> <span data-ttu-id="fa4d6-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fa4d6-122"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="fa4d6-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fa4d6-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa4d6-124">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="fa4d6-124">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> </dl>

 

 




