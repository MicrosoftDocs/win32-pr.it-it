---
description: Il metodo EffectGetPriority Recupera il livello di priorità dell'effetto. Per un determinato oggetto, il motore di rendering applica gli effetti in ordine di priorità, a partire dal livello di priorità zero.
ms.assetid: 2504fa0c-f052-4d99-98c3-803b0c0d49e5
title: 'Metodo IAMTimelineEffect:: EffectGetPriority (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineEffect.EffectGetPriority
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 26ea9795e3ffe36a75c354e51ff2f7e64fae40ea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333699"
---
# <a name="iamtimelineeffecteffectgetpriority-method"></a><span data-ttu-id="b00f2-104">Metodo IAMTimelineEffect:: EffectGetPriority</span><span class="sxs-lookup"><span data-stu-id="b00f2-104">IAMTimelineEffect::EffectGetPriority method</span></span>

> [!Note]  
> <span data-ttu-id="b00f2-105">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="b00f2-105">\[Deprecated.</span></span> <span data-ttu-id="b00f2-106">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b00f2-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="b00f2-107">Il `EffectGetPriority` metodo recupera il livello di priorità dell'effetto.</span><span class="sxs-lookup"><span data-stu-id="b00f2-107">The `EffectGetPriority` method retrieves the effect's priority level.</span></span> <span data-ttu-id="b00f2-108">Per un determinato oggetto, il motore di rendering applica gli effetti in ordine di priorità, a partire dal livello di priorità zero.</span><span class="sxs-lookup"><span data-stu-id="b00f2-108">For a given object, the render engine applies effects in order of priority, starting with priority level zero.</span></span>

## <a name="syntax"></a><span data-ttu-id="b00f2-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b00f2-109">Syntax</span></span>


```C++
HRESULT EffectGetPriority(
   long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="b00f2-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="b00f2-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b00f2-111">*pVal*</span><span class="sxs-lookup"><span data-stu-id="b00f2-111">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="b00f2-112">Riceve il livello di priorità.</span><span class="sxs-lookup"><span data-stu-id="b00f2-112">Receives the priority level.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b00f2-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b00f2-113">Return value</span></span>

<span data-ttu-id="b00f2-114">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b00f2-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b00f2-115">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b00f2-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b00f2-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="b00f2-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b00f2-117">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="b00f2-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="b00f2-118">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="b00f2-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="b00f2-119">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="b00f2-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b00f2-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b00f2-120">Requirements</span></span>



| <span data-ttu-id="b00f2-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="b00f2-121">Requirement</span></span> | <span data-ttu-id="b00f2-122">Valore</span><span class="sxs-lookup"><span data-stu-id="b00f2-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b00f2-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b00f2-123">Header</span></span><br/>  | <dl> <span data-ttu-id="b00f2-124"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="b00f2-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="b00f2-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="b00f2-125">Library</span></span><br/> | <dl> <span data-ttu-id="b00f2-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b00f2-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b00f2-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b00f2-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b00f2-128">**Interfaccia IAMTimelineEffect**</span><span class="sxs-lookup"><span data-stu-id="b00f2-128">**IAMTimelineEffect Interface**</span></span>](iamtimelineeffect.md)
</dt> <dt>

[<span data-ttu-id="b00f2-129">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="b00f2-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




