---
description: 'Il metodo GetDefaultFPS recupera la frequenza dei fotogrammi di output predefinita, in frame al secondo (FPS). I gruppi utilizzano questo valore come frequenza dei fotogrammi predefinita. Per impostare la frequenza dei fotogrammi di un gruppo, chiamare il metodo IAMTimelineGroup:: SetOutputFPS sul gruppo.'
ms.assetid: 91c83512-4295-440e-b3b2-09fe3629f827
title: 'Metodo IAMTimeline:: GetDefaultFPS (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetDefaultFPS
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4e1e6aef61a34831571de345c8dd18c7aeef474d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327428"
---
# <a name="iamtimelinegetdefaultfps-method"></a><span data-ttu-id="63b00-105">Metodo IAMTimeline:: GetDefaultFPS</span><span class="sxs-lookup"><span data-stu-id="63b00-105">IAMTimeline::GetDefaultFPS method</span></span>

> [!Note]  
> <span data-ttu-id="63b00-106">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="63b00-106">\[Deprecated.</span></span> <span data-ttu-id="63b00-107">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="63b00-107">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="63b00-108">Il `GetDefaultFPS` metodo recupera la frequenza dei fotogrammi di output predefinita, in frame al secondo (fps).</span><span class="sxs-lookup"><span data-stu-id="63b00-108">The `GetDefaultFPS` method retrieves the default output frame rate, in frames per second (FPS).</span></span> <span data-ttu-id="63b00-109">I gruppi utilizzano questo valore come frequenza dei fotogrammi predefinita.</span><span class="sxs-lookup"><span data-stu-id="63b00-109">Groups use this value as their default frame rate.</span></span> <span data-ttu-id="63b00-110">Per impostare la frequenza dei fotogrammi di un gruppo, chiamare il metodo [**IAMTimelineGroup:: SetOutputFPS**](iamtimelinegroup-setoutputfps.md) sul gruppo.</span><span class="sxs-lookup"><span data-stu-id="63b00-110">To set a group's frame rate, call the [**IAMTimelineGroup::SetOutputFPS**](iamtimelinegroup-setoutputfps.md) method on the group.</span></span>

## <a name="syntax"></a><span data-ttu-id="63b00-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="63b00-111">Syntax</span></span>


```C++
HRESULT GetDefaultFPS(
   double *pFPS
);
```



## <a name="parameters"></a><span data-ttu-id="63b00-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="63b00-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63b00-113">*pFPS*</span><span class="sxs-lookup"><span data-stu-id="63b00-113">*pFPS*</span></span> 
</dt> <dd>

<span data-ttu-id="63b00-114">Riceve la frequenza dei fotogrammi predefinita, in frame al secondo.</span><span class="sxs-lookup"><span data-stu-id="63b00-114">Receives the default frame rate, in frames per second.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63b00-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="63b00-115">Return value</span></span>

<span data-ttu-id="63b00-116">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="63b00-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="63b00-117">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="63b00-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="63b00-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="63b00-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="63b00-119">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="63b00-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="63b00-120">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="63b00-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="63b00-121">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="63b00-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="63b00-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="63b00-122">Requirements</span></span>



| <span data-ttu-id="63b00-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="63b00-123">Requirement</span></span> | <span data-ttu-id="63b00-124">Valore</span><span class="sxs-lookup"><span data-stu-id="63b00-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="63b00-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="63b00-125">Header</span></span><br/>  | <dl> <span data-ttu-id="63b00-126"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="63b00-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="63b00-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="63b00-127">Library</span></span><br/> | <dl> <span data-ttu-id="63b00-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="63b00-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63b00-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="63b00-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63b00-130">**Interfaccia IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="63b00-130">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="63b00-131">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="63b00-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




