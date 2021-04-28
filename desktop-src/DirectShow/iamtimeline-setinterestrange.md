---
description: 'Metodo IAMTimeline::SetInterestRange: non implementato.'
ms.assetid: b803ba33-d698-449f-a540-3981c4f0826a
title: Metodo IAMTimeline::SetInterestRange (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.SetInterestRange
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 23485bbdc2292e0d341e3fef0646fb68616698c4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119569"
---
# <a name="iamtimelinesetinterestrange-method"></a><span data-ttu-id="4a116-103">Metodo IAMTimeline::SetInterestRange</span><span class="sxs-lookup"><span data-stu-id="4a116-103">IAMTimeline::SetInterestRange method</span></span>

> [!Note]  
> <span data-ttu-id="4a116-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="4a116-104">\[Deprecated.</span></span> <span data-ttu-id="4a116-105">Questa API potrebbe essere rimossa dalle versioni future di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4a116-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="4a116-106">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="4a116-106">Not implemented.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a116-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4a116-107">Syntax</span></span>


```C++
HRESULT SetInterestRange(
   REFERENCE_TIME Start,
   REFERENCE_TIME Stop
);
```



## <a name="parameters"></a><span data-ttu-id="4a116-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="4a116-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a116-109">*Inizia*</span><span class="sxs-lookup"><span data-stu-id="4a116-109">*Start*</span></span> 
</dt> <dd>

<span data-ttu-id="4a116-110">Riservato.</span><span class="sxs-lookup"><span data-stu-id="4a116-110">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="4a116-111">*Stop*</span><span class="sxs-lookup"><span data-stu-id="4a116-111">*Stop*</span></span> 
</dt> <dd>

<span data-ttu-id="4a116-112">Riservato.</span><span class="sxs-lookup"><span data-stu-id="4a116-112">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a116-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4a116-113">Return value</span></span>

<span data-ttu-id="4a116-114">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="4a116-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4a116-115">In caso contrario, restituisce un **codice di errore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="4a116-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a116-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="4a116-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4a116-117">Il file di intestazione Qedit.h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="4a116-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="4a116-118">Per ottenere Qedit.h, scaricare l'aggiornamento [Microsoft Windows SDK per Windows Vista e .NET Framework 3.0.](https://msdn.microsoft.com/windowsvista/bb980924.aspx)</span><span class="sxs-lookup"><span data-stu-id="4a116-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="4a116-119">Qedit.h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3.5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="4a116-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4a116-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4a116-120">Requirements</span></span>



| <span data-ttu-id="4a116-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a116-121">Requirement</span></span> | <span data-ttu-id="4a116-122">Valore</span><span class="sxs-lookup"><span data-stu-id="4a116-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4a116-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4a116-123">Header</span></span><br/>  | <dl> <span data-ttu-id="4a116-124"><dt>Qedit.h</dt></span><span class="sxs-lookup"><span data-stu-id="4a116-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="4a116-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="4a116-125">Library</span></span><br/> | <dl> <span data-ttu-id="4a116-126"><dt>Strmiids.lib</dt></span><span class="sxs-lookup"><span data-stu-id="4a116-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a116-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4a116-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a116-128">**Interfaccia IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="4a116-128">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> </dl>

 

 




