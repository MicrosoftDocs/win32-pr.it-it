---
description: "Il metodo SetCutPoint2 imposta l'ora in cui la transizione passa da un'origine all'altra, se viene eseguito il rendering della transizione come taglia. Questo metodo è equivalente a IAMTimelineTrans:: SetCutPoint, ma accetta un valore REFTIME."
ms.assetid: d06d3ee7-04a2-4266-9995-bfabea24aef9
title: 'Metodo IAMTimelineTrans:: SetCutPoint2 (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.SetCutPoint2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 117ec522416f0d5722c8ef7aa17cd6e81720b4c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325035"
---
# <a name="iamtimelinetranssetcutpoint2-method"></a><span data-ttu-id="a1b0a-104">Metodo IAMTimelineTrans:: SetCutPoint2</span><span class="sxs-lookup"><span data-stu-id="a1b0a-104">IAMTimelineTrans::SetCutPoint2 method</span></span>

> [!Note]  
> <span data-ttu-id="a1b0a-105">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="a1b0a-105">\[Deprecated.</span></span> <span data-ttu-id="a1b0a-106">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a1b0a-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="a1b0a-107">Il `SetCutPoint2` metodo imposta l'ora in cui la transizione passa da un'origine all'altra, se viene eseguito il rendering della transizione come taglia.</span><span class="sxs-lookup"><span data-stu-id="a1b0a-107">The `SetCutPoint2` method sets the time at which the transition cuts from one source to the next, if the transition is rendered as a cut.</span></span> <span data-ttu-id="a1b0a-108">Questo metodo è equivalente a [**IAMTimelineTrans:: SetCutPoint**](iamtimelinetrans-setcutpoint.md), ma accetta un valore [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="a1b0a-108">This method is equivalent to [**IAMTimelineTrans::SetCutPoint**](iamtimelinetrans-setcutpoint.md), but takes a [**REFTIME**](reftime.md) value.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1b0a-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a1b0a-109">Syntax</span></span>


```C++
HRESULT SetCutPoint2(
   REFTIME TLTime
);
```



## <a name="parameters"></a><span data-ttu-id="a1b0a-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="a1b0a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1b0a-111">*TLTime*</span><span class="sxs-lookup"><span data-stu-id="a1b0a-111">*TLTime*</span></span> 
</dt> <dd>

<span data-ttu-id="a1b0a-112">Punto di taglio relativo all'inizio della transizione, in secondi.</span><span class="sxs-lookup"><span data-stu-id="a1b0a-112">Cut point relative to the start of the transition, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1b0a-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a1b0a-113">Return value</span></span>

<span data-ttu-id="a1b0a-114">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="a1b0a-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a1b0a-115">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a1b0a-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1b0a-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="a1b0a-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a1b0a-117">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="a1b0a-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="a1b0a-118">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="a1b0a-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="a1b0a-119">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="a1b0a-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a1b0a-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a1b0a-120">Requirements</span></span>



| <span data-ttu-id="a1b0a-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1b0a-121">Requirement</span></span> | <span data-ttu-id="a1b0a-122">Valore</span><span class="sxs-lookup"><span data-stu-id="a1b0a-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a1b0a-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a1b0a-123">Header</span></span><br/>  | <dl> <span data-ttu-id="a1b0a-124"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="a1b0a-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="a1b0a-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="a1b0a-125">Library</span></span><br/> | <dl> <span data-ttu-id="a1b0a-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a1b0a-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1b0a-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a1b0a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1b0a-128">**Interfaccia IAMTimelineTrans**</span><span class="sxs-lookup"><span data-stu-id="a1b0a-128">**IAMTimelineTrans Interface**</span></span>](iamtimelinetrans.md)
</dt> <dt>

[<span data-ttu-id="a1b0a-129">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="a1b0a-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




