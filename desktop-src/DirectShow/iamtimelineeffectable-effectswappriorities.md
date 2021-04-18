---
description: Il metodo EffectSwapPriorities passa i livelli di priorità di due effetti.
ms.assetid: ff5ab294-3963-4df7-9299-ee7c7165e72f
title: 'Metodo IAMTimelineEffectable:: EffectSwapPriorities (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineEffectable.EffectSwapPriorities
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fb6a7dbee2d7f90da8f32e2a034e82df485f1ef4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333696"
---
# <a name="iamtimelineeffectableeffectswappriorities-method"></a><span data-ttu-id="7d483-103">Metodo IAMTimelineEffectable:: EffectSwapPriorities</span><span class="sxs-lookup"><span data-stu-id="7d483-103">IAMTimelineEffectable::EffectSwapPriorities method</span></span>

> [!Note]  
> <span data-ttu-id="7d483-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="7d483-104">\[Deprecated.</span></span> <span data-ttu-id="7d483-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="7d483-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="7d483-106">Il `EffectSwapPriorities` metodo passa i livelli di priorità di due effetti.</span><span class="sxs-lookup"><span data-stu-id="7d483-106">The `EffectSwapPriorities` method switches the priority levels of two effects.</span></span>

<span data-ttu-id="7d483-107">Dato due valori di priorità, questo metodo scambia gli effetti con tali priorità.</span><span class="sxs-lookup"><span data-stu-id="7d483-107">Given two priority values, this method swaps the effects at those priorities.</span></span> <span data-ttu-id="7d483-108">Quando il metodo restituisce un risultato, l'effetto che si trovava al primo livello di priorità è il secondo livello di priorità e viceversa.</span><span class="sxs-lookup"><span data-stu-id="7d483-108">When the method returns, the effect that was at the first priority level is at the second priority level, and vice versa.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d483-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7d483-109">Syntax</span></span>


```C++
HRESULT EffectSwapPriorities(
   long PriorityA,
   long PriorityB
);
```



## <a name="parameters"></a><span data-ttu-id="7d483-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="7d483-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d483-111">*Priorità*</span><span class="sxs-lookup"><span data-stu-id="7d483-111">*PriorityA*</span></span> 
</dt> <dd>

<span data-ttu-id="7d483-112">Primo livello di priorità in corrispondenza del quale scambiare gli effetti.</span><span class="sxs-lookup"><span data-stu-id="7d483-112">First priority level at which to swap effects.</span></span>

</dd> <dt>

<span data-ttu-id="7d483-113">*PriorityB*</span><span class="sxs-lookup"><span data-stu-id="7d483-113">*PriorityB*</span></span> 
</dt> <dd>

<span data-ttu-id="7d483-114">Secondo livello di priorità in corrispondenza del quale scambiare gli effetti.</span><span class="sxs-lookup"><span data-stu-id="7d483-114">Second priority level at which to swap effects.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d483-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7d483-115">Return value</span></span>

<span data-ttu-id="7d483-116">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="7d483-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7d483-117">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7d483-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="7d483-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="7d483-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="7d483-119">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="7d483-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="7d483-120">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="7d483-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="7d483-121">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="7d483-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7d483-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7d483-122">Requirements</span></span>



| <span data-ttu-id="7d483-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="7d483-123">Requirement</span></span> | <span data-ttu-id="7d483-124">Valore</span><span class="sxs-lookup"><span data-stu-id="7d483-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7d483-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7d483-125">Header</span></span><br/>  | <dl> <span data-ttu-id="7d483-126"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d483-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="7d483-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="7d483-127">Library</span></span><br/> | <dl> <span data-ttu-id="7d483-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7d483-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d483-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7d483-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d483-130">**Interfaccia IAMTimelineEffectable**</span><span class="sxs-lookup"><span data-stu-id="7d483-130">**IAMTimelineEffectable Interface**</span></span>](iamtimelineeffectable.md)
</dt> <dt>

[<span data-ttu-id="7d483-131">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="7d483-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




