---
description: Il metodo GetCountOfType Recupera il numero di oggetti del tipo specificato contenuti in un gruppo specificato e in tutti i relativi elementi figlio.
ms.assetid: f3571fa5-8020-4079-ab7e-ba9ff280c0c5
title: 'Metodo IAMTimeline:: GetCountOfType (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetCountOfType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: f0636eac7c651ed003c618e258f7dbf2bdd60996
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326796"
---
# <a name="iamtimelinegetcountoftype-method"></a><span data-ttu-id="83e07-103">Metodo IAMTimeline:: GetCountOfType</span><span class="sxs-lookup"><span data-stu-id="83e07-103">IAMTimeline::GetCountOfType method</span></span>

> [!Note]  
> <span data-ttu-id="83e07-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="83e07-104">\[Deprecated.</span></span> <span data-ttu-id="83e07-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="83e07-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="83e07-106">Il `GetCountOfType` metodo recupera il numero di oggetti del tipo specificato contenuti in un gruppo specificato e in tutti i relativi elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="83e07-106">The `GetCountOfType` method retrieves the number of objects of the specified type that are contained in a specified group and all of its children.</span></span>

## <a name="syntax"></a><span data-ttu-id="83e07-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="83e07-107">Syntax</span></span>


```C++
HRESULT GetCountOfType(
   long                Group,
   long                *pVal,
   long                *pValWithComps,
   TIMELINE_MAJOR_TYPE MajorType
);
```



## <a name="parameters"></a><span data-ttu-id="83e07-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="83e07-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83e07-109">*Gruppo*</span><span class="sxs-lookup"><span data-stu-id="83e07-109">*Group*</span></span> 
</dt> <dd>

<span data-ttu-id="83e07-110">Numero di indice del gruppo per il quale recuperare il conteggio.</span><span class="sxs-lookup"><span data-stu-id="83e07-110">Index number of the group for which to retrieve the count.</span></span>

</dd> <dt>

<span data-ttu-id="83e07-111">*pVal*</span><span class="sxs-lookup"><span data-stu-id="83e07-111">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="83e07-112">Riceve il numero di oggetti del tipo specificato contenuti nel gruppo e in tutte le relative tracce virtuali, in modo ricorsivo.</span><span class="sxs-lookup"><span data-stu-id="83e07-112">Receives the number of objects of the specified type contained in the group and all of its virtual tracks, recursively.</span></span>

</dd> <dt>

<span data-ttu-id="83e07-113">*pValWithComps*</span><span class="sxs-lookup"><span data-stu-id="83e07-113">*pValWithComps*</span></span> 
</dt> <dd>

<span data-ttu-id="83e07-114">Riceve il conteggio restituito in *pval* più il numero di composizioni ricercate, incluso quello.</span><span class="sxs-lookup"><span data-stu-id="83e07-114">Receives the count returned in *pVal* plus the number of compositions searched, including this one.</span></span>

</dd> <dt>

<span data-ttu-id="83e07-115">*MajorType*</span><span class="sxs-lookup"><span data-stu-id="83e07-115">*MajorType*</span></span> 
</dt> <dd>

<span data-ttu-id="83e07-116">Membro del tipo enumerato della [**sequenza temporale \_ principale \_**](timeline-major-type.md) , che specifica il tipo di oggetto da contare.</span><span class="sxs-lookup"><span data-stu-id="83e07-116">Member of the [**TIMELINE\_MAJOR\_TYPE**](timeline-major-type.md) enumerated type, specifying the type of object to count.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83e07-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="83e07-117">Return value</span></span>

<span data-ttu-id="83e07-118">Restituisce uno dei seguenti valori **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="83e07-118">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="83e07-119">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="83e07-119">Return code</span></span>                                                                                  | <span data-ttu-id="83e07-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="83e07-120">Description</span></span>                           |
|----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="83e07-121"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="83e07-121"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="83e07-122">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="83e07-122">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="83e07-123"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="83e07-123"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="83e07-124">Numero di gruppo non valido.</span><span class="sxs-lookup"><span data-stu-id="83e07-124">Invalid group number.</span></span><br/>      |
| <dl> <span data-ttu-id="83e07-125"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="83e07-125"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="83e07-126">Argomento puntatore **null** .</span><span class="sxs-lookup"><span data-stu-id="83e07-126">**NULL** pointer argument.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="83e07-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="83e07-127">Remarks</span></span>

<span data-ttu-id="83e07-128">La chiamata a questo metodo equivale alla chiamata di [**IAMTimelineComp:: GetCountOfType**](iamtimelinecomp-getcountoftype.md) nel gruppo specificato.</span><span class="sxs-lookup"><span data-stu-id="83e07-128">Calling this method is equivalent to calling [**IAMTimelineComp::GetCountOfType**](iamtimelinecomp-getcountoftype.md) on the specified group.</span></span> <span data-ttu-id="83e07-129">Per ulteriori informazioni, vedere la sezione Osservazioni di tale metodo.</span><span class="sxs-lookup"><span data-stu-id="83e07-129">See the Remarks section of that method for more information.</span></span>

<span data-ttu-id="83e07-130">In genere, un'applicazione non chiamerà questo metodo.</span><span class="sxs-lookup"><span data-stu-id="83e07-130">Typically, an application will not call this method.</span></span> <span data-ttu-id="83e07-131">Viene chiamato internamente dal motore di rendering.</span><span class="sxs-lookup"><span data-stu-id="83e07-131">It is called internally by the render engine.</span></span>

> [!Note]  
> <span data-ttu-id="83e07-132">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="83e07-132">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="83e07-133">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="83e07-133">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="83e07-134">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="83e07-134">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="83e07-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="83e07-135">Requirements</span></span>



| <span data-ttu-id="83e07-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="83e07-136">Requirement</span></span> | <span data-ttu-id="83e07-137">Valore</span><span class="sxs-lookup"><span data-stu-id="83e07-137">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="83e07-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="83e07-138">Header</span></span><br/>  | <dl> <span data-ttu-id="83e07-139"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="83e07-139"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="83e07-140">Libreria</span><span class="sxs-lookup"><span data-stu-id="83e07-140">Library</span></span><br/> | <dl> <span data-ttu-id="83e07-141"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="83e07-141"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83e07-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="83e07-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83e07-143">**Interfaccia IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="83e07-143">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="83e07-144">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="83e07-144">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




