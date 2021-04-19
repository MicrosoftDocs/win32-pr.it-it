---
description: 'Il metodo GetCutPoint2 Recupera il punto di taglio. Questo metodo è equivalente a IAMTimelineTrans:: GetCutPoint, ma accetta un valore REFTIME.'
ms.assetid: bf2b7cac-6740-44d8-a889-8c745a23db19
title: 'Metodo IAMTimelineTrans:: GetCutPoint2 (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.GetCutPoint2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 68712da95da2f5c21d5e370c688002aa14a8a166
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333264"
---
# <a name="iamtimelinetransgetcutpoint2-method"></a><span data-ttu-id="a7dcd-104">Metodo IAMTimelineTrans:: GetCutPoint2</span><span class="sxs-lookup"><span data-stu-id="a7dcd-104">IAMTimelineTrans::GetCutPoint2 method</span></span>

> [!Note]  
> <span data-ttu-id="a7dcd-105">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="a7dcd-105">\[Deprecated.</span></span> <span data-ttu-id="a7dcd-106">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a7dcd-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="a7dcd-107">Il `GetCutPoint2` metodo recupera il punto di taglio.</span><span class="sxs-lookup"><span data-stu-id="a7dcd-107">The `GetCutPoint2` method retrieves the cut point.</span></span> <span data-ttu-id="a7dcd-108">Questo metodo è equivalente a [**IAMTimelineTrans:: GetCutPoint**](iamtimelinetrans-getcutpoint.md), ma accetta un valore [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="a7dcd-108">This method is equivalent to [**IAMTimelineTrans::GetCutPoint**](iamtimelinetrans-getcutpoint.md), but takes a [**REFTIME**](reftime.md) value.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7dcd-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a7dcd-109">Syntax</span></span>


```C++
HRESULT GetCutPoint2(
   REFTIME *pTLTime
);
```



## <a name="parameters"></a><span data-ttu-id="a7dcd-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="a7dcd-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7dcd-111">*pTLTime*</span><span class="sxs-lookup"><span data-stu-id="a7dcd-111">*pTLTime*</span></span> 
</dt> <dd>

<span data-ttu-id="a7dcd-112">Riceve il punto di taglio, in secondi, rispetto all'ora di inizio della transizione.</span><span class="sxs-lookup"><span data-stu-id="a7dcd-112">Receives the cut point, relative to the start time of the transition, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7dcd-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a7dcd-113">Return value</span></span>

<span data-ttu-id="a7dcd-114">Restituisce uno dei seguenti valori **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="a7dcd-114">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="a7dcd-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="a7dcd-115">Return code</span></span>                                                                               | <span data-ttu-id="a7dcd-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a7dcd-116">Description</span></span>                                                                    |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a7dcd-117"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="a7dcd-117"><dt>**S\_FALSE**</dt></span></span> </dl>   | <span data-ttu-id="a7dcd-118">Il punto di taglio non è stato impostato.</span><span class="sxs-lookup"><span data-stu-id="a7dcd-118">The cut point was not set.</span></span> <span data-ttu-id="a7dcd-119">Il valore restituito è il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="a7dcd-119">The value returned is the default value.</span></span><br/> |
| <dl> <span data-ttu-id="a7dcd-120"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a7dcd-120"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="a7dcd-121">Il punto di taglio è stato impostato su un valore diverso da quello predefinito.</span><span class="sxs-lookup"><span data-stu-id="a7dcd-121">The cut point was set to a value other than the default.</span></span><br/>            |
| <dl> <span data-ttu-id="a7dcd-122"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="a7dcd-122"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="a7dcd-123">Argomento puntatore **null** .</span><span class="sxs-lookup"><span data-stu-id="a7dcd-123">**NULL** pointer argument.</span></span><br/>                                          |



 

## <a name="remarks"></a><span data-ttu-id="a7dcd-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="a7dcd-124">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a7dcd-125">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="a7dcd-125">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="a7dcd-126">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="a7dcd-126">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="a7dcd-127">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="a7dcd-127">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a7dcd-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a7dcd-128">Requirements</span></span>



| <span data-ttu-id="a7dcd-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7dcd-129">Requirement</span></span> | <span data-ttu-id="a7dcd-130">Valore</span><span class="sxs-lookup"><span data-stu-id="a7dcd-130">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a7dcd-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a7dcd-131">Header</span></span><br/>  | <dl> <span data-ttu-id="a7dcd-132"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="a7dcd-132"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="a7dcd-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="a7dcd-133">Library</span></span><br/> | <dl> <span data-ttu-id="a7dcd-134"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a7dcd-134"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7dcd-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a7dcd-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7dcd-136">**Interfaccia IAMTimelineTrans**</span><span class="sxs-lookup"><span data-stu-id="a7dcd-136">**IAMTimelineTrans Interface**</span></span>](iamtimelinetrans.md)
</dt> <dt>

[<span data-ttu-id="a7dcd-137">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="a7dcd-137">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




