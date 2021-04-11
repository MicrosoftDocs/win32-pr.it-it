---
description: Propagare le modifiche di stato che si verificano all'interno di un passaggio attivo al dispositivo prima del rendering.
ms.assetid: 3a779b63-c106-4a81-afeb-82bd6e556de4
title: 'Metodo ID3DXEffect:: CommitChanges (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.CommitChanges
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 41516c52b29dfe277cc857e44003de7783282a3a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235049"
---
# <a name="id3dxeffectcommitchanges-method"></a><span data-ttu-id="00e76-103">Metodo ID3DXEffect:: CommitChanges</span><span class="sxs-lookup"><span data-stu-id="00e76-103">ID3DXEffect::CommitChanges method</span></span>

<span data-ttu-id="00e76-104">Propagare le modifiche di stato che si verificano all'interno di un passaggio attivo al dispositivo prima del rendering.</span><span class="sxs-lookup"><span data-stu-id="00e76-104">Propagate state changes that occur inside of an active pass to the device before rendering.</span></span>

## <a name="syntax"></a><span data-ttu-id="00e76-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="00e76-105">Syntax</span></span>


```C++
HRESULT CommitChanges();
```



## <a name="parameters"></a><span data-ttu-id="00e76-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="00e76-106">Parameters</span></span>

<span data-ttu-id="00e76-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="00e76-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="00e76-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="00e76-108">Return value</span></span>

<span data-ttu-id="00e76-109">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="00e76-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="00e76-110">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="00e76-110">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="00e76-111">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="00e76-111">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="00e76-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="00e76-112">Remarks</span></span>

<span data-ttu-id="00e76-113">Se l'applicazione modifica uno stato di effetto usando uno dei metodi [**ID3DXEffect:: SETX**](id3dxeffect.md) all'interno di una coppia [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md) / [**ID3DXEffect:: EndPass**](id3dxeffect--endpass.md) matching, l'applicazione deve chiamare **ID3DXEffect:: CommitChanges** prima di qualsiasi chiamata DrawxPrimitive per propagare le modifiche di stato al dispositivo prima del rendering.</span><span class="sxs-lookup"><span data-stu-id="00e76-113">If the application changes any effect state using any of the [**ID3DXEffect::Setx**](id3dxeffect.md) methods inside of an [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md)/[**ID3DXEffect::EndPass**](id3dxeffect--endpass.md) matching pair, the application must call **ID3DXEffect::CommitChanges** before any DrawxPrimitive call to propagate state changes to the device before rendering.</span></span> <span data-ttu-id="00e76-114">Se non vengono apportate modifiche allo stato all'interno di una coppia di **ID3DXEffect:: BeginPass** e **ID3DXEffect:: EndPass** , non è necessario chiamare **ID3DXEffect:: CommitChanges**.</span><span class="sxs-lookup"><span data-stu-id="00e76-114">If no state changes occur within a **ID3DXEffect::BeginPass** and **ID3DXEffect::EndPass** matching pair, it is not necessary to call **ID3DXEffect::CommitChanges**.</span></span>

<span data-ttu-id="00e76-115">Si tratta di un valore leggermente diverso per tutti i parametri condivisi in un effetto clonato.</span><span class="sxs-lookup"><span data-stu-id="00e76-115">This is slightly different for any shared parameters in a cloned effect.</span></span> <span data-ttu-id="00e76-116">Quando una tecnica è attiva in un effetto clonato, ovvero quando [**ID3DXEffect:: Begin**](id3dxeffect--begin.md) è stato chiamato ma e [**ID3DXEffect:: end**](id3dxeffect--end.md) non è stato chiamato, **ID3DXEffect:: CommitChanges** aggiorna i parametri che non sono condivisi come previsto.</span><span class="sxs-lookup"><span data-stu-id="00e76-116">When a technique is active on a cloned effect (that is, when [**ID3DXEffect::Begin**](id3dxeffect--begin.md) has been called but and [**ID3DXEffect::End**](id3dxeffect--end.md) has not been called), **ID3DXEffect::CommitChanges** updates parameters that are not shared as expected.</span></span> <span data-ttu-id="00e76-117">Per aggiornare un parametro condiviso (solo per un effetto clonato la cui tecnica è attiva), chiamare **ID3DXEffect:: end** per disattivare la tecnica e **ID3DXEffect:: Begin** per riattivare la tecnica prima di chiamare **ID3DXEffect:: CommitChanges**.</span><span class="sxs-lookup"><span data-stu-id="00e76-117">To update a shared parameter (only for a cloned effect whose technique is active), call **ID3DXEffect::End** to deactivate the technique and **ID3DXEffect::Begin** to reactivate the technique before calling **ID3DXEffect::CommitChanges**.</span></span>

## <a name="requirements"></a><span data-ttu-id="00e76-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="00e76-118">Requirements</span></span>



| <span data-ttu-id="00e76-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="00e76-119">Requirement</span></span> | <span data-ttu-id="00e76-120">Valore</span><span class="sxs-lookup"><span data-stu-id="00e76-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="00e76-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="00e76-121">Header</span></span><br/>  | <dl> <span data-ttu-id="00e76-122"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="00e76-122"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="00e76-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="00e76-123">Library</span></span><br/> | <dl> <span data-ttu-id="00e76-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="00e76-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="00e76-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="00e76-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00e76-126">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="00e76-126">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> </dl>

 

 




