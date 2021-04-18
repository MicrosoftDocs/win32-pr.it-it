---
description: Il metodo SetCutPoint imposta l'ora in cui la transizione passa da un'origine all'altra, se viene eseguito il rendering della transizione come taglia.
ms.assetid: 2660f4a8-e249-45d7-8866-02a9f2ef52b8
title: 'Metodo IAMTimelineTrans:: SetCutPoint (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.SetCutPoint
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c1dad934d373a52b7e6c076c8c20dc8e1c6809ac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327330"
---
# <a name="iamtimelinetranssetcutpoint-method"></a><span data-ttu-id="46578-103">Metodo IAMTimelineTrans:: SetCutPoint</span><span class="sxs-lookup"><span data-stu-id="46578-103">IAMTimelineTrans::SetCutPoint method</span></span>

> [!Note]  
> <span data-ttu-id="46578-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="46578-104">\[Deprecated.</span></span> <span data-ttu-id="46578-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="46578-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="46578-106">Il `SetCutPoint` metodo imposta l'ora in cui la transizione passa da un'origine all'altra, se viene eseguito il rendering della transizione come taglia.</span><span class="sxs-lookup"><span data-stu-id="46578-106">The `SetCutPoint` method sets the time at which the transition cuts from one source to the next, if the transition is rendered as a cut.</span></span>

## <a name="syntax"></a><span data-ttu-id="46578-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="46578-107">Syntax</span></span>


```C++
HRESULT SetCutPoint(
   REFERENCE_TIME TLTime
);
```



## <a name="parameters"></a><span data-ttu-id="46578-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="46578-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46578-109">*TLTime*</span><span class="sxs-lookup"><span data-stu-id="46578-109">*TLTime*</span></span> 
</dt> <dd>

<span data-ttu-id="46578-110">Punto di taglio relativo all'inizio della transizione, in unità di 100 nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="46578-110">Cut point relative to the start of the transition, in 100-nanosecond units.</span></span> <span data-ttu-id="46578-111">Se il valore non rientra nei limiti della transizione, viene troncato all'ora valida più vicina.</span><span class="sxs-lookup"><span data-stu-id="46578-111">If the value falls outside the bounds of the transition, it is truncated to the nearest valid time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46578-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="46578-112">Return value</span></span>

<span data-ttu-id="46578-113">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="46578-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="46578-114">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="46578-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="46578-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="46578-115">Remarks</span></span>

<span data-ttu-id="46578-116">Per impostazione predefinita, il punto di taglio è il centro della transizione.</span><span class="sxs-lookup"><span data-stu-id="46578-116">By default, the cut-point is the middle of the transition.</span></span> <span data-ttu-id="46578-117">Ad esempio, in una transizione che si estende su un secondo, il punto di taglio predefinito è di 0,5 secondi nella transizione.</span><span class="sxs-lookup"><span data-stu-id="46578-117">For example, in a transition that spans one second, the default cut point is 0.5 seconds into the transition.</span></span>

> [!Note]  
> <span data-ttu-id="46578-118">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="46578-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="46578-119">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="46578-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="46578-120">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="46578-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="46578-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="46578-121">Requirements</span></span>



| <span data-ttu-id="46578-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="46578-122">Requirement</span></span> | <span data-ttu-id="46578-123">Valore</span><span class="sxs-lookup"><span data-stu-id="46578-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="46578-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="46578-124">Header</span></span><br/>  | <dl> <span data-ttu-id="46578-125"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="46578-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="46578-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="46578-126">Library</span></span><br/> | <dl> <span data-ttu-id="46578-127"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="46578-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46578-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="46578-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46578-129">**Interfaccia IAMTimelineTrans**</span><span class="sxs-lookup"><span data-stu-id="46578-129">**IAMTimelineTrans Interface**</span></span>](iamtimelinetrans.md)
</dt> <dt>

[<span data-ttu-id="46578-130">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="46578-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




