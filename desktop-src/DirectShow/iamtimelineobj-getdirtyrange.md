---
description: 'Metodo IAMTimelineObj::GetDirtyRange : non supportato.'
ms.assetid: 7f97b1c4-0508-45a5-a6fd-5dae17f0fa60
title: Metodo IAMTimelineObj::GetDirtyRange (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetDirtyRange
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 828bb5a88d3bcefcf10f0a6e4f07070a4b60322d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098569"
---
# <a name="iamtimelineobjgetdirtyrange-method"></a><span data-ttu-id="95d20-103">Metodo IAMTimelineObj::GetDirtyRange</span><span class="sxs-lookup"><span data-stu-id="95d20-103">IAMTimelineObj::GetDirtyRange method</span></span>

> [!Note]  
> <span data-ttu-id="95d20-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="95d20-104">\[Deprecated.</span></span> <span data-ttu-id="95d20-105">Questa API potrebbe essere rimossa dalle versioni future di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="95d20-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="95d20-106">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="95d20-106">Not supported.</span></span>

## <a name="syntax"></a><span data-ttu-id="95d20-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="95d20-107">Syntax</span></span>


```C++
HRESULT GetDirtyRange(
   REFERENCE_TIME *pStart,
   REFERENCE_TIME *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="95d20-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="95d20-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95d20-109">*Pstart*</span><span class="sxs-lookup"><span data-stu-id="95d20-109">*pStart*</span></span> 
</dt> <dd>

<span data-ttu-id="95d20-110">Riservato.</span><span class="sxs-lookup"><span data-stu-id="95d20-110">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="95d20-111">*pStop*</span><span class="sxs-lookup"><span data-stu-id="95d20-111">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="95d20-112">Riservato.</span><span class="sxs-lookup"><span data-stu-id="95d20-112">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95d20-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="95d20-113">Return value</span></span>

<span data-ttu-id="95d20-114">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="95d20-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="95d20-115">In caso contrario, restituisce un **codice di errore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="95d20-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="95d20-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="95d20-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="95d20-117">Il file di intestazione Qedit.h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="95d20-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="95d20-118">Per ottenere Qedit.h, scaricare Microsoft Windows SDK [Update per Windows Vista e .NET Framework 3.0.](https://msdn.microsoft.com/windowsvista/bb980924.aspx)</span><span class="sxs-lookup"><span data-stu-id="95d20-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="95d20-119">Qedit.h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3.5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="95d20-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="95d20-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="95d20-120">Requirements</span></span>



| <span data-ttu-id="95d20-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="95d20-121">Requirement</span></span> | <span data-ttu-id="95d20-122">Valore</span><span class="sxs-lookup"><span data-stu-id="95d20-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="95d20-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="95d20-123">Header</span></span><br/>  | <dl> <span data-ttu-id="95d20-124"><dt>Qedit.h</dt></span><span class="sxs-lookup"><span data-stu-id="95d20-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="95d20-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="95d20-125">Library</span></span><br/> | <dl> <span data-ttu-id="95d20-126"><dt>Strmiids.lib</dt></span><span class="sxs-lookup"><span data-stu-id="95d20-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95d20-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="95d20-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95d20-128">**Interfaccia IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="95d20-128">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> </dl>

 

 




