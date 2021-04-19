---
description: Il metodo AddGroup aggiunge un gruppo alla sequenza temporale.
ms.assetid: c7fc3b59-5852-4a3c-b9bf-f87e659819b5
title: 'Metodo IAMTimeline:: AddGroup (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.AddGroup
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0de10defd5e7aa840322599fb32104f1dc5bb5a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326807"
---
# <a name="iamtimelineaddgroup-method"></a><span data-ttu-id="2e79e-103">Metodo IAMTimeline:: AddGroup</span><span class="sxs-lookup"><span data-stu-id="2e79e-103">IAMTimeline::AddGroup method</span></span>

> [!Note]  
> <span data-ttu-id="2e79e-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="2e79e-104">\[Deprecated.</span></span> <span data-ttu-id="2e79e-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="2e79e-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="2e79e-106">Il `AddGroup` metodo aggiunge un gruppo alla sequenza temporale.</span><span class="sxs-lookup"><span data-stu-id="2e79e-106">The `AddGroup` method adds a group to the timeline.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e79e-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2e79e-107">Syntax</span></span>


```C++
HRESULT AddGroup(
   IAMTimelineObj *pGroup
);
```



## <a name="parameters"></a><span data-ttu-id="2e79e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="2e79e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e79e-109">*pGroup*</span><span class="sxs-lookup"><span data-stu-id="2e79e-109">*pGroup*</span></span> 
</dt> <dd>

<span data-ttu-id="2e79e-110">Puntatore all'interfaccia [**IAMTimelineObj**](iamtimelineobj.md) del gruppo.</span><span class="sxs-lookup"><span data-stu-id="2e79e-110">Pointer to the [**IAMTimelineObj**](iamtimelineobj.md) interface of the group.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e79e-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2e79e-111">Return value</span></span>

<span data-ttu-id="2e79e-112">Restituisce uno dei seguenti valori **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="2e79e-112">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="2e79e-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="2e79e-113">Return code</span></span>                                                                                   | <span data-ttu-id="2e79e-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2e79e-114">Description</span></span>                                   |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="2e79e-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2e79e-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="2e79e-116">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="2e79e-116">Success.</span></span><br/>                           |
| <dl> <span data-ttu-id="2e79e-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="2e79e-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="2e79e-118">È stato superato il numero massimo di gruppi.</span><span class="sxs-lookup"><span data-stu-id="2e79e-118">Maximum number of groups exceeded.</span></span><br/> |
| <dl> <span data-ttu-id="2e79e-119"><dt>**E \_ NOinterface**</dt></span><span class="sxs-lookup"><span data-stu-id="2e79e-119"><dt>**E\_NOINTERFACE**</dt></span></span> </dl> | <span data-ttu-id="2e79e-120">L'oggetto non è un gruppo.</span><span class="sxs-lookup"><span data-stu-id="2e79e-120">The object is not a group.</span></span><br/>         |



 

## <a name="remarks"></a><span data-ttu-id="2e79e-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="2e79e-121">Remarks</span></span>

<span data-ttu-id="2e79e-122">Attualmente, le sequenze temporali supportano un massimo di 32 gruppi.</span><span class="sxs-lookup"><span data-stu-id="2e79e-122">Currently, timelines support a maximum of 32 groups.</span></span>

> [!Note]  
> <span data-ttu-id="2e79e-123">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="2e79e-123">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="2e79e-124">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="2e79e-124">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="2e79e-125">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="2e79e-125">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2e79e-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2e79e-126">Requirements</span></span>



| <span data-ttu-id="2e79e-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e79e-127">Requirement</span></span> | <span data-ttu-id="2e79e-128">Valore</span><span class="sxs-lookup"><span data-stu-id="2e79e-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2e79e-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2e79e-129">Header</span></span><br/>  | <dl> <span data-ttu-id="2e79e-130"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e79e-130"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="2e79e-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="2e79e-131">Library</span></span><br/> | <dl> <span data-ttu-id="2e79e-132"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2e79e-132"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e79e-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2e79e-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e79e-134">**Interfaccia IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="2e79e-134">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="2e79e-135">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="2e79e-135">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




