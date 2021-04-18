---
description: Il metodo getTimeline recupera la sequenza temporale a cui appartiene il gruppo.
ms.assetid: a57d75c9-6e2e-426f-9403-ad32188b2211
title: 'Metodo IAMTimelineGroup:: getTimeline (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.GetTimeline
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 6b85b0c6f1730c2946134a36d33537f311b6603f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328616"
---
# <a name="iamtimelinegroupgettimeline-method"></a><span data-ttu-id="119db-103">Metodo IAMTimelineGroup:: getTimeline</span><span class="sxs-lookup"><span data-stu-id="119db-103">IAMTimelineGroup::GetTimeline method</span></span>

> [!Note]  
> <span data-ttu-id="119db-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="119db-104">\[Deprecated.</span></span> <span data-ttu-id="119db-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="119db-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="119db-106">Il `GetTimeline` metodo recupera la sequenza temporale a cui appartiene il gruppo.</span><span class="sxs-lookup"><span data-stu-id="119db-106">The `GetTimeline` method retrieves the timeline to which this group belongs.</span></span>

## <a name="syntax"></a><span data-ttu-id="119db-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="119db-107">Syntax</span></span>


```C++
HRESULT GetTimeline(
  [out] IAMTimeline **ppTimeline
);
```



## <a name="parameters"></a><span data-ttu-id="119db-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="119db-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="119db-109">*ppTimeline* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="119db-109">*ppTimeline* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="119db-110">Riceve l'interfaccia [**IAMTimeline**](iamtimeline.md) della sequenza temporale.</span><span class="sxs-lookup"><span data-stu-id="119db-110">Receives the timeline's [**IAMTimeline**](iamtimeline.md) interface.</span></span> <span data-ttu-id="119db-111">Se il gruppo non fa parte di una sequenza temporale, il valore viene impostato su **null**.</span><span class="sxs-lookup"><span data-stu-id="119db-111">If the group is not part of a timeline, the value is set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="119db-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="119db-112">Return value</span></span>

<span data-ttu-id="119db-113">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="119db-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="119db-114">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="119db-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="119db-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="119db-115">Remarks</span></span>

<span data-ttu-id="119db-116">Se il valore restituito in *ppTimeline* non è **null**, l'interfaccia **IAMTimeline** include un conteggio dei riferimenti in attesa.</span><span class="sxs-lookup"><span data-stu-id="119db-116">If the value returned in *ppTimeline* is not **NULL**, the **IAMTimeline** interface has an outstanding reference count.</span></span> <span data-ttu-id="119db-117">Assicurarsi di rilasciare l'interfaccia al termine dell'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="119db-117">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="119db-118">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="119db-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="119db-119">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="119db-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="119db-120">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="119db-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="119db-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="119db-121">Requirements</span></span>



| <span data-ttu-id="119db-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="119db-122">Requirement</span></span> | <span data-ttu-id="119db-123">Valore</span><span class="sxs-lookup"><span data-stu-id="119db-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="119db-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="119db-124">Header</span></span><br/>  | <dl> <span data-ttu-id="119db-125"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="119db-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="119db-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="119db-126">Library</span></span><br/> | <dl> <span data-ttu-id="119db-127"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="119db-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="119db-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="119db-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="119db-129">**Interfaccia IAMTimelineGroup**</span><span class="sxs-lookup"><span data-stu-id="119db-129">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="119db-130">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="119db-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




