---
description: "Il metodo ModifyStopTime2 imposta l'ora di arresto. Questo metodo è equivalente a IAMTimelineSrc:: ModifyStopTime, ma accetta un valore REFTIME."
ms.assetid: 8bebda47-3e52-42a2-870c-acc14561fa25
title: 'Metodo IAMTimelineSrc:: ModifyStopTime2 (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.ModifyStopTime2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 42ca3c9c1f8fa47abc7a9c21a44458540007939f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332751"
---
# <a name="iamtimelinesrcmodifystoptime2-method"></a><span data-ttu-id="4798a-104">Metodo IAMTimelineSrc:: ModifyStopTime2</span><span class="sxs-lookup"><span data-stu-id="4798a-104">IAMTimelineSrc::ModifyStopTime2 method</span></span>

> [!Note]  
> <span data-ttu-id="4798a-105">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="4798a-105">\[Deprecated.</span></span> <span data-ttu-id="4798a-106">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4798a-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="4798a-107">Il `ModifyStopTime2` metodo imposta l'ora di arresto.</span><span class="sxs-lookup"><span data-stu-id="4798a-107">The `ModifyStopTime2` method sets the stop time.</span></span> <span data-ttu-id="4798a-108">Questo metodo è equivalente a [**IAMTimelineSrc:: ModifyStopTime**](iamtimelinesrc-modifystoptime.md), ma accetta un valore [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="4798a-108">This method is equivalent to [**IAMTimelineSrc::ModifyStopTime**](iamtimelinesrc-modifystoptime.md), but takes a [**REFTIME**](reftime.md) value.</span></span>

## <a name="syntax"></a><span data-ttu-id="4798a-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4798a-109">Syntax</span></span>


```C++
HRESULT ModifyStopTime2(
   REFTIME Stop
);
```



## <a name="parameters"></a><span data-ttu-id="4798a-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="4798a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4798a-111">*Stop*</span><span class="sxs-lookup"><span data-stu-id="4798a-111">*Stop*</span></span> 
</dt> <dd>

<span data-ttu-id="4798a-112">Nuova ora di arresto, in secondi.</span><span class="sxs-lookup"><span data-stu-id="4798a-112">New stop time, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4798a-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4798a-113">Return value</span></span>

<span data-ttu-id="4798a-114">Restituisce \_ OK se ha esito positivo o E \_ INVALIDARG se l'ora specificata non è valida.</span><span class="sxs-lookup"><span data-stu-id="4798a-114">Returns S\_OK if successful, or E\_INVALIDARG if the specified time is not valid.</span></span>

## <a name="remarks"></a><span data-ttu-id="4798a-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="4798a-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4798a-116">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="4798a-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="4798a-117">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="4798a-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="4798a-118">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="4798a-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4798a-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4798a-119">Requirements</span></span>



| <span data-ttu-id="4798a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="4798a-120">Requirement</span></span> | <span data-ttu-id="4798a-121">Valore</span><span class="sxs-lookup"><span data-stu-id="4798a-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4798a-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4798a-122">Header</span></span><br/>  | <dl> <span data-ttu-id="4798a-123"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="4798a-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="4798a-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="4798a-124">Library</span></span><br/> | <dl> <span data-ttu-id="4798a-125"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4798a-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4798a-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4798a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4798a-127">**Interfaccia IAMTimelineSrc**</span><span class="sxs-lookup"><span data-stu-id="4798a-127">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="4798a-128">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="4798a-128">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




