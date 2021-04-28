---
description: 'Metodo IAMTimeline::GetDirtyRange: non supportato.'
ms.assetid: 6e45b542-be3f-4da8-808a-6aa8b4299519
title: Metodo IAMTimeline::GetDirtyRange (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetDirtyRange
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: cb0ecbd8a93698d36354c251f0381c35acf288a2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119599"
---
# <a name="iamtimelinegetdirtyrange-method"></a><span data-ttu-id="b2de3-103">Metodo IAMTimeline::GetDirtyRange</span><span class="sxs-lookup"><span data-stu-id="b2de3-103">IAMTimeline::GetDirtyRange method</span></span>

> [!Note]  
> <span data-ttu-id="b2de3-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="b2de3-104">\[Deprecated.</span></span> <span data-ttu-id="b2de3-105">Questa API potrebbe essere rimossa dalle versioni future di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b2de3-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="b2de3-106">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="b2de3-106">Not supported.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2de3-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b2de3-107">Syntax</span></span>


```C++
HRESULT GetDirtyRange(
   REFERENCE_TIME *pStart,
   REFERENCE_TIME *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="b2de3-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="b2de3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2de3-109">*Pstart*</span><span class="sxs-lookup"><span data-stu-id="b2de3-109">*pStart*</span></span> 
</dt> <dd>

<span data-ttu-id="b2de3-110">Riservato.</span><span class="sxs-lookup"><span data-stu-id="b2de3-110">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="b2de3-111">*pStop*</span><span class="sxs-lookup"><span data-stu-id="b2de3-111">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="b2de3-112">Riservato.</span><span class="sxs-lookup"><span data-stu-id="b2de3-112">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2de3-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b2de3-113">Return value</span></span>

<span data-ttu-id="b2de3-114">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b2de3-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b2de3-115">In caso contrario, restituisce un **codice di errore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="b2de3-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2de3-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="b2de3-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b2de3-117">Il file di intestazione Qedit.h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="b2de3-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="b2de3-118">Per ottenere Qedit.h, scaricare l'aggiornamento [Microsoft Windows SDK per Windows Vista e .NET Framework 3.0.](https://msdn.microsoft.com/windowsvista/bb980924.aspx)</span><span class="sxs-lookup"><span data-stu-id="b2de3-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="b2de3-119">Qedit.h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3.5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="b2de3-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b2de3-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b2de3-120">Requirements</span></span>



| <span data-ttu-id="b2de3-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2de3-121">Requirement</span></span> | <span data-ttu-id="b2de3-122">Valore</span><span class="sxs-lookup"><span data-stu-id="b2de3-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b2de3-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b2de3-123">Header</span></span><br/>  | <dl> <span data-ttu-id="b2de3-124"><dt>Qedit.h</dt></span><span class="sxs-lookup"><span data-stu-id="b2de3-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="b2de3-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="b2de3-125">Library</span></span><br/> | <dl> <span data-ttu-id="b2de3-126"><dt>Strmiids.lib</dt></span><span class="sxs-lookup"><span data-stu-id="b2de3-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2de3-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b2de3-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2de3-128">**Interfaccia IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="b2de3-128">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> </dl>

 

 




