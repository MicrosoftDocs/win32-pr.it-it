---
description: Il metodo GetCountOfType Recupera il numero di oggetti di un determinato tipo contenuto in questa composizione e in tutte le relative tracce virtuali, in modo ricorsivo.
ms.assetid: 2d14ccf7-77bc-4095-bfb8-12a52b4b9595
title: 'Metodo IAMTimelineComp:: GetCountOfType (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.GetCountOfType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 69c4c582a3883feedec962bfb88b4a833be3750b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332046"
---
# <a name="iamtimelinecompgetcountoftype-method"></a><span data-ttu-id="273b2-103">Metodo IAMTimelineComp:: GetCountOfType</span><span class="sxs-lookup"><span data-stu-id="273b2-103">IAMTimelineComp::GetCountOfType method</span></span>

> [!Note]  
> <span data-ttu-id="273b2-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="273b2-104">\[Deprecated.</span></span> <span data-ttu-id="273b2-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="273b2-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="273b2-106">Il `GetCountOfType` metodo recupera il numero di oggetti di un tipo specificato contenuto nella composizione e in tutte le relative tracce virtuali, in modo ricorsivo.</span><span class="sxs-lookup"><span data-stu-id="273b2-106">The `GetCountOfType` method retrieves the number of objects of a given type contained in this composition and all its virtual tracks, recursively.</span></span>

## <a name="syntax"></a><span data-ttu-id="273b2-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="273b2-107">Syntax</span></span>


```C++
HRESULT GetCountOfType(
   long                *pVal,
   long                *pValWithComps,
   TIMELINE_MAJOR_TYPE MajorType
);
```



## <a name="parameters"></a><span data-ttu-id="273b2-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="273b2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="273b2-109">*pVal*</span><span class="sxs-lookup"><span data-stu-id="273b2-109">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="273b2-110">Riceve il numero di oggetti del tipo specificato contenuti in questa composizione e in tutte le relative tracce virtuali, in modo ricorsivo.</span><span class="sxs-lookup"><span data-stu-id="273b2-110">Receives the number of objects of the specified type contained in this composition and all its virtual tracks, recursively.</span></span>

</dd> <dt>

<span data-ttu-id="273b2-111">*pValWithComps*</span><span class="sxs-lookup"><span data-stu-id="273b2-111">*pValWithComps*</span></span> 
</dt> <dd>

<span data-ttu-id="273b2-112">Riceve il conteggio restituito in *pval* più il numero di composizioni ricercate, incluso quello.</span><span class="sxs-lookup"><span data-stu-id="273b2-112">Receives the count returned in *pVal* plus the number of compositions searched, including this one.</span></span>

</dd> <dt>

<span data-ttu-id="273b2-113">*MajorType*</span><span class="sxs-lookup"><span data-stu-id="273b2-113">*MajorType*</span></span> 
</dt> <dd>

<span data-ttu-id="273b2-114">Membro del tipo enumerato della [**sequenza temporale \_ principale \_**](timeline-major-type.md) , che specifica il tipo di oggetto da contare.</span><span class="sxs-lookup"><span data-stu-id="273b2-114">Member of the [**TIMELINE\_MAJOR\_TYPE**](timeline-major-type.md) enumerated type, specifying the type of object to count.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="273b2-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="273b2-115">Return value</span></span>

<span data-ttu-id="273b2-116">Restituisce \_ OK se ha esito positivo o un \_ puntatore e in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="273b2-116">Returns S\_OK if successful, or E\_POINTER otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="273b2-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="273b2-117">Remarks</span></span>

<span data-ttu-id="273b2-118">In genere, un'applicazione non chiamerà questo metodo.</span><span class="sxs-lookup"><span data-stu-id="273b2-118">Typically, an application will not call this method.</span></span> <span data-ttu-id="273b2-119">Viene chiamato dal motore di rendering.</span><span class="sxs-lookup"><span data-stu-id="273b2-119">It is called by the render engine.</span></span>

<span data-ttu-id="273b2-120">Se si contano le composizioni, il valore restituito in *pval* è zero e il valore restituito in *pValWithComps* è il numero di composizioni.</span><span class="sxs-lookup"><span data-stu-id="273b2-120">If you count compositions, the value returned in *pVal* is zero and the value returned in *pValWithComps* is the number of compositions.</span></span> <span data-ttu-id="273b2-121">Il valore di *\* pValWithComps* include la composizione sulla quale viene chiamato il metodo.</span><span class="sxs-lookup"><span data-stu-id="273b2-121">The value of *\*pValWithComps* includes the composition on which you call the method.</span></span> <span data-ttu-id="273b2-122">Ad esempio, se si chiama questo metodo su una composizione vuota, *\* pValWithComps* è uguale a 1.</span><span class="sxs-lookup"><span data-stu-id="273b2-122">For example, if you call this method on an empty composition, *\*pValWithComps* equals 1.</span></span>

<span data-ttu-id="273b2-123">I gruppi non possono risiedere all'interno di composizioni, pertanto non è possibile usare questo metodo per conteggiare i gruppi.</span><span class="sxs-lookup"><span data-stu-id="273b2-123">Groups cannot reside inside compositions, so you cannot use this method to count groups.</span></span> <span data-ttu-id="273b2-124">Il conteggio restituito sarà sempre zero. Per conteggiare i gruppi, chiamare il metodo [**IAMTimeline:: GetGroupCount**](iamtimeline-getgroupcount.md) .</span><span class="sxs-lookup"><span data-stu-id="273b2-124">(The returned count will always be zero.) To count groups, call the [**IAMTimeline::GetGroupCount**](iamtimeline-getgroupcount.md) method.</span></span>

> [!Note]  
> <span data-ttu-id="273b2-125">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="273b2-125">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="273b2-126">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="273b2-126">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="273b2-127">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="273b2-127">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="273b2-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="273b2-128">Requirements</span></span>



| <span data-ttu-id="273b2-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="273b2-129">Requirement</span></span> | <span data-ttu-id="273b2-130">Valore</span><span class="sxs-lookup"><span data-stu-id="273b2-130">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="273b2-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="273b2-131">Header</span></span><br/>  | <dl> <span data-ttu-id="273b2-132"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="273b2-132"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="273b2-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="273b2-133">Library</span></span><br/> | <dl> <span data-ttu-id="273b2-134"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="273b2-134"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="273b2-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="273b2-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="273b2-136">**Interfaccia IAMTimelineComp**</span><span class="sxs-lookup"><span data-stu-id="273b2-136">**IAMTimelineComp Interface**</span></span>](iamtimelinecomp.md)
</dt> <dt>

[<span data-ttu-id="273b2-137">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="273b2-137">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




