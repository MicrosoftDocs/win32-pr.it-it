---
description: Il metodo TransAdd aggiunge una transizione all'oggetto. Un oggetto può avere più transizioni, ma non devono sovrapporsi nel tempo. Le transizioni devono rientrare nei limiti temporali dell'oggetto.
ms.assetid: 2c3f923f-c754-4cc8-82ca-d3979d4bda07
title: 'Metodo IAMTimelineTransable:: TransAdd (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTransable.TransAdd
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2636922549635c4a1c5e6e0b36f308f62328dc60
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332965"
---
# <a name="iamtimelinetransabletransadd-method"></a><span data-ttu-id="78f35-105">Metodo IAMTimelineTransable:: TransAdd</span><span class="sxs-lookup"><span data-stu-id="78f35-105">IAMTimelineTransable::TransAdd method</span></span>

> [!Note]  
> <span data-ttu-id="78f35-106">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="78f35-106">\[Deprecated.</span></span> <span data-ttu-id="78f35-107">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="78f35-107">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="78f35-108">Il `TransAdd` metodo aggiunge una transizione all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="78f35-108">The `TransAdd` method adds a transition to the object.</span></span> <span data-ttu-id="78f35-109">Un oggetto può avere più transizioni, ma non devono sovrapporsi nel tempo.</span><span class="sxs-lookup"><span data-stu-id="78f35-109">An object can have multiple transitions, but they must not overlap in time.</span></span> <span data-ttu-id="78f35-110">Le transizioni devono rientrare nei limiti temporali dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="78f35-110">Transitions must fall within the time boundaries of the object.</span></span>

## <a name="syntax"></a><span data-ttu-id="78f35-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="78f35-111">Syntax</span></span>


```C++
HRESULT TransAdd(
   IAMTimelineObj *pTrans
);
```



## <a name="parameters"></a><span data-ttu-id="78f35-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="78f35-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78f35-113">*pTrans*</span><span class="sxs-lookup"><span data-stu-id="78f35-113">*pTrans*</span></span> 
</dt> <dd>

<span data-ttu-id="78f35-114">Puntatore all'interfaccia [**IAMTimelineObj**](iamtimelineobj.md) della transizione da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="78f35-114">Pointer to the [**IAMTimelineObj**](iamtimelineobj.md) interface of the transition to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78f35-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="78f35-115">Return value</span></span>

<span data-ttu-id="78f35-116">Restituisce uno dei seguenti valori **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="78f35-116">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="78f35-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="78f35-117">Return code</span></span>                                                                                   | <span data-ttu-id="78f35-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="78f35-118">Description</span></span>                                           |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <span data-ttu-id="78f35-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="78f35-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="78f35-120">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="78f35-120">Success.</span></span><br/>                                   |
| <dl> <span data-ttu-id="78f35-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="78f35-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="78f35-122">Impossibile inserire la transizione.</span><span class="sxs-lookup"><span data-stu-id="78f35-122">Cannot insert the transition.</span></span><br/>              |
| <dl> <span data-ttu-id="78f35-123"><dt>**E \_ NOinterface**</dt></span><span class="sxs-lookup"><span data-stu-id="78f35-123"><dt>**E\_NOINTERFACE**</dt></span></span> </dl> | <span data-ttu-id="78f35-124">*pTrans* non è un puntatore a una transizione.</span><span class="sxs-lookup"><span data-stu-id="78f35-124">*pTrans* is not a pointer to a transition.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="78f35-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="78f35-125">Remarks</span></span>

<span data-ttu-id="78f35-126">Se la transizione si sovrappone a una transizione esistente, il metodo restituisce E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="78f35-126">If the transition overlaps an existing transition, the method returns E\_INVALIDARG.</span></span>

> [!Note]  
> <span data-ttu-id="78f35-127">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="78f35-127">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="78f35-128">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="78f35-128">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="78f35-129">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="78f35-129">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="78f35-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="78f35-130">Requirements</span></span>



| <span data-ttu-id="78f35-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="78f35-131">Requirement</span></span> | <span data-ttu-id="78f35-132">Valore</span><span class="sxs-lookup"><span data-stu-id="78f35-132">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="78f35-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="78f35-133">Header</span></span><br/>  | <dl> <span data-ttu-id="78f35-134"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="78f35-134"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="78f35-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="78f35-135">Library</span></span><br/> | <dl> <span data-ttu-id="78f35-136"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="78f35-136"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78f35-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="78f35-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78f35-138">**Interfaccia IAMTimelineTransable**</span><span class="sxs-lookup"><span data-stu-id="78f35-138">**IAMTimelineTransable Interface**</span></span>](iamtimelinetransable.md)
</dt> <dt>

[<span data-ttu-id="78f35-139">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="78f35-139">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




