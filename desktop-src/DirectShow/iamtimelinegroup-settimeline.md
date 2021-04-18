---
description: 'Non supportata. Chiamare invece il metodo IAMTimeline:: AddGroup.'
ms.assetid: dd671fa5-ed5a-46e2-b4bd-a37f0e7458ca
title: 'Metodo IAMTimelineGroup:: setimeline (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetTimeline
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 166d65f5ae9a14f58ed7b20763ab5e4a136df598
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331437"
---
# <a name="iamtimelinegroupsettimeline-method"></a><span data-ttu-id="f6d3a-104">Metodo IAMTimelineGroup:: setimeline</span><span class="sxs-lookup"><span data-stu-id="f6d3a-104">IAMTimelineGroup::SetTimeline method</span></span>

> [!Note]  
> <span data-ttu-id="f6d3a-105">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="f6d3a-105">\[Deprecated.</span></span> <span data-ttu-id="f6d3a-106">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f6d3a-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="f6d3a-107">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="f6d3a-107">Not supported.</span></span> <span data-ttu-id="f6d3a-108">Chiamare invece il metodo [**IAMTimeline:: addgroup**](iamtimeline-addgroup.md) .</span><span class="sxs-lookup"><span data-stu-id="f6d3a-108">Call the [**IAMTimeline::AddGroup**](iamtimeline-addgroup.md) method instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6d3a-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f6d3a-109">Syntax</span></span>


```C++
HRESULT SetTimeline(
   IAMTimeline *pTimeline
);
```



## <a name="parameters"></a><span data-ttu-id="f6d3a-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="f6d3a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6d3a-111">*pTimeline*</span><span class="sxs-lookup"><span data-stu-id="f6d3a-111">*pTimeline*</span></span> 
</dt> <dd>

<span data-ttu-id="f6d3a-112">Riservato.</span><span class="sxs-lookup"><span data-stu-id="f6d3a-112">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6d3a-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f6d3a-113">Return value</span></span>

<span data-ttu-id="f6d3a-114">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="f6d3a-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f6d3a-115">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f6d3a-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f6d3a-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="f6d3a-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f6d3a-117">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="f6d3a-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="f6d3a-118">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="f6d3a-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="f6d3a-119">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="f6d3a-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f6d3a-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f6d3a-120">Requirements</span></span>



| <span data-ttu-id="f6d3a-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6d3a-121">Requirement</span></span> | <span data-ttu-id="f6d3a-122">Valore</span><span class="sxs-lookup"><span data-stu-id="f6d3a-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f6d3a-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f6d3a-123">Header</span></span><br/>  | <dl> <span data-ttu-id="f6d3a-124"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="f6d3a-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="f6d3a-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="f6d3a-125">Library</span></span><br/> | <dl> <span data-ttu-id="f6d3a-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f6d3a-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6d3a-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f6d3a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6d3a-128">**Interfaccia IAMTimelineGroup**</span><span class="sxs-lookup"><span data-stu-id="f6d3a-128">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> </dl>

 

 




