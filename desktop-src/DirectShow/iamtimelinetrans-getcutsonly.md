---
description: Il metodo GetCutsOnly determina se viene eseguito il rendering della transizione come taglia. In tal caso, la transizione viene eseguita immediatamente in corrispondenza del punto di taglio.
ms.assetid: d7959816-1152-4bc4-b3f8-bed69b450530
title: 'Metodo IAMTimelineTrans:: GetCutsOnly (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.GetCutsOnly
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d3bbec55ddfe77c053135054fde9b64efce516a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333262"
---
# <a name="iamtimelinetransgetcutsonly-method"></a><span data-ttu-id="8ed99-104">Metodo IAMTimelineTrans:: GetCutsOnly</span><span class="sxs-lookup"><span data-stu-id="8ed99-104">IAMTimelineTrans::GetCutsOnly method</span></span>

> [!Note]  
> <span data-ttu-id="8ed99-105">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="8ed99-105">\[Deprecated.</span></span> <span data-ttu-id="8ed99-106">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8ed99-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="8ed99-107">Il `GetCutsOnly` metodo determina se viene eseguito il rendering della transizione come taglia.</span><span class="sxs-lookup"><span data-stu-id="8ed99-107">The `GetCutsOnly` method determines whether the transition is rendered as a cut.</span></span> <span data-ttu-id="8ed99-108">In tal caso, la transizione viene eseguita immediatamente in corrispondenza del punto di taglio.</span><span class="sxs-lookup"><span data-stu-id="8ed99-108">If so, the transition occurs instantaneously at the cut point.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ed99-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8ed99-109">Syntax</span></span>


```C++
HRESULT GetCutsOnly(
   BOOL *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="8ed99-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="8ed99-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ed99-111">*pVal*</span><span class="sxs-lookup"><span data-stu-id="8ed99-111">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="8ed99-112">Riceve un valore booleano che specifica se viene eseguito il rendering della transizione come taglia.</span><span class="sxs-lookup"><span data-stu-id="8ed99-112">Receives a Boolean value specifying whether the transition is rendered as a cut.</span></span> <span data-ttu-id="8ed99-113">Se **true**, la transizione è un taglio istantaneo.</span><span class="sxs-lookup"><span data-stu-id="8ed99-113">If **TRUE**, the transition is an instantaneous cut.</span></span> <span data-ttu-id="8ed99-114">Se **false**, la transizione viene eseguita per la durata normale.</span><span class="sxs-lookup"><span data-stu-id="8ed99-114">If **FALSE**, the transition occurs over its normal duration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ed99-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8ed99-115">Return value</span></span>

<span data-ttu-id="8ed99-116">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="8ed99-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8ed99-117">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8ed99-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ed99-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="8ed99-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="8ed99-119">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="8ed99-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="8ed99-120">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="8ed99-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="8ed99-121">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="8ed99-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8ed99-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8ed99-122">Requirements</span></span>



| <span data-ttu-id="8ed99-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ed99-123">Requirement</span></span> | <span data-ttu-id="8ed99-124">Valore</span><span class="sxs-lookup"><span data-stu-id="8ed99-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8ed99-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8ed99-125">Header</span></span><br/>  | <dl> <span data-ttu-id="8ed99-126"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ed99-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="8ed99-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="8ed99-127">Library</span></span><br/> | <dl> <span data-ttu-id="8ed99-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8ed99-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ed99-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8ed99-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ed99-130">**Interfaccia IAMTimelineTrans**</span><span class="sxs-lookup"><span data-stu-id="8ed99-130">**IAMTimelineTrans Interface**</span></span>](iamtimelinetrans.md)
</dt> <dt>

[<span data-ttu-id="8ed99-131">**IAMTimelineTrans::SetCutsOnly**</span><span class="sxs-lookup"><span data-stu-id="8ed99-131">**IAMTimelineTrans::SetCutsOnly**</span></span>](iamtimelinetrans-setcutsonly.md)
</dt> <dt>

[<span data-ttu-id="8ed99-132">**IAMTimelineTrans::GetCutPoint**</span><span class="sxs-lookup"><span data-stu-id="8ed99-132">**IAMTimelineTrans::GetCutPoint**</span></span>](iamtimelinetrans-getcutpoint.md)
</dt> <dt>

[<span data-ttu-id="8ed99-133">**IAMTimeline::TransitionsEnabled**</span><span class="sxs-lookup"><span data-stu-id="8ed99-133">**IAMTimeline::TransitionsEnabled**</span></span>](iamtimeline-transitionsenabled.md)
</dt> <dt>

[<span data-ttu-id="8ed99-134">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="8ed99-134">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




