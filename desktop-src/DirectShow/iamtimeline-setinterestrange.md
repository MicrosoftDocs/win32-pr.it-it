---
description: Non implementato.
ms.assetid: b803ba33-d698-449f-a540-3981c4f0826a
title: 'Metodo IAMTimeline:: SetInterestRange (qedit. h)'
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
ms.openlocfilehash: 0a3c92848380bb71bcdca0e6f6de1069d6eb998a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328157"
---
# <a name="iamtimelinesetinterestrange-method"></a><span data-ttu-id="7ff81-103">Metodo IAMTimeline:: SetInterestRange</span><span class="sxs-lookup"><span data-stu-id="7ff81-103">IAMTimeline::SetInterestRange method</span></span>

> [!Note]  
> <span data-ttu-id="7ff81-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="7ff81-104">\[Deprecated.</span></span> <span data-ttu-id="7ff81-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="7ff81-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="7ff81-106">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="7ff81-106">Not implemented.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ff81-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7ff81-107">Syntax</span></span>


```C++
HRESULT SetInterestRange(
   REFERENCE_TIME Start,
   REFERENCE_TIME Stop
);
```



## <a name="parameters"></a><span data-ttu-id="7ff81-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="7ff81-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ff81-109">*Inizia*</span><span class="sxs-lookup"><span data-stu-id="7ff81-109">*Start*</span></span> 
</dt> <dd>

<span data-ttu-id="7ff81-110">Riservato.</span><span class="sxs-lookup"><span data-stu-id="7ff81-110">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="7ff81-111">*Stop*</span><span class="sxs-lookup"><span data-stu-id="7ff81-111">*Stop*</span></span> 
</dt> <dd>

<span data-ttu-id="7ff81-112">Riservato.</span><span class="sxs-lookup"><span data-stu-id="7ff81-112">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ff81-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7ff81-113">Return value</span></span>

<span data-ttu-id="7ff81-114">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="7ff81-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7ff81-115">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7ff81-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ff81-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="7ff81-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="7ff81-117">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="7ff81-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="7ff81-118">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="7ff81-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="7ff81-119">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="7ff81-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7ff81-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7ff81-120">Requirements</span></span>



| <span data-ttu-id="7ff81-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ff81-121">Requirement</span></span> | <span data-ttu-id="7ff81-122">Valore</span><span class="sxs-lookup"><span data-stu-id="7ff81-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7ff81-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7ff81-123">Header</span></span><br/>  | <dl> <span data-ttu-id="7ff81-124"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ff81-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="7ff81-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="7ff81-125">Library</span></span><br/> | <dl> <span data-ttu-id="7ff81-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7ff81-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ff81-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7ff81-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ff81-128">**Interfaccia IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="7ff81-128">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> </dl>

 

 




