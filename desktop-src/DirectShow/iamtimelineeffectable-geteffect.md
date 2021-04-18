---
description: Il metodo GetEffect recupera l'effetto al livello di priorità specificato.
ms.assetid: 8606c457-1c4d-4a20-b674-aaf82abeb451
title: 'Metodo IAMTimelineEffectable:: GetEffect (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineEffectable.GetEffect
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: b7a769fca28ea1f8f698b23de7df6b7c15f05234
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333694"
---
# <a name="iamtimelineeffectablegeteffect-method"></a><span data-ttu-id="4a80e-103">Metodo IAMTimelineEffectable:: GetEffect</span><span class="sxs-lookup"><span data-stu-id="4a80e-103">IAMTimelineEffectable::GetEffect method</span></span>

> [!Note]  
> <span data-ttu-id="4a80e-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="4a80e-104">\[Deprecated.</span></span> <span data-ttu-id="4a80e-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4a80e-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="4a80e-106">Il metodo **GetEffect** recupera l'effetto al livello di priorità specificato.</span><span class="sxs-lookup"><span data-stu-id="4a80e-106">The **GetEffect** method retrieves the effect at the specified priority level.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a80e-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4a80e-107">Syntax</span></span>


```C++
HRESULT GetEffect(
  [out] IAMTimelineObj **ppFX,
        long           Which
);
```



## <a name="parameters"></a><span data-ttu-id="4a80e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="4a80e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a80e-109">*ppFX* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="4a80e-109">*ppFX* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4a80e-110">Riceve l'interfaccia [**IAMTimelineObj**](iamtimelineobj.md) dell'effetto.</span><span class="sxs-lookup"><span data-stu-id="4a80e-110">Receives the effect's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="4a80e-111">*Che*</span><span class="sxs-lookup"><span data-stu-id="4a80e-111">*Which*</span></span> 
</dt> <dd>

<span data-ttu-id="4a80e-112">Livello di priorità dell'effetto da recuperare.</span><span class="sxs-lookup"><span data-stu-id="4a80e-112">Priority level of the effect to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a80e-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4a80e-113">Return value</span></span>

<span data-ttu-id="4a80e-114">Restituisce un valore HRESULT.</span><span class="sxs-lookup"><span data-stu-id="4a80e-114">Returns an HRESULT value.</span></span> <span data-ttu-id="4a80e-115">I possibili valori sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="4a80e-115">Possible values include the following:</span></span>



| <span data-ttu-id="4a80e-116">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="4a80e-116">Return code</span></span>                                                                               | <span data-ttu-id="4a80e-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4a80e-117">Description</span></span>                                     |
|-------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="4a80e-118"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="4a80e-118"><dt>**S\_FALSE**</dt></span></span> </dl>   | <span data-ttu-id="4a80e-119">Nessun effetto alla priorità specificata,</span><span class="sxs-lookup"><span data-stu-id="4a80e-119">No effect at the specified priority,</span></span><br/> |
| <dl> <span data-ttu-id="4a80e-120"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4a80e-120"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="4a80e-121">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="4a80e-121">Success.</span></span><br/>                             |
| <dl> <span data-ttu-id="4a80e-122"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="4a80e-122"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="4a80e-123">Argomento puntatore **null** .</span><span class="sxs-lookup"><span data-stu-id="4a80e-123">**NULL** pointer argument.</span></span><br/>           |



 

## <a name="remarks"></a><span data-ttu-id="4a80e-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="4a80e-124">Remarks</span></span>

<span data-ttu-id="4a80e-125">Se il metodo restituisce S \_ OK, l'interfaccia **IAMTimelineObj** restituita presenta un conteggio dei riferimenti in attesa.</span><span class="sxs-lookup"><span data-stu-id="4a80e-125">If the method returns S\_OK, the **IAMTimelineObj** interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="4a80e-126">Assicurarsi di rilasciare l'interfaccia al termine dell'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="4a80e-126">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="4a80e-127">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="4a80e-127">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="4a80e-128">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="4a80e-128">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="4a80e-129">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="4a80e-129">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4a80e-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4a80e-130">Requirements</span></span>



| <span data-ttu-id="4a80e-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a80e-131">Requirement</span></span> | <span data-ttu-id="4a80e-132">Valore</span><span class="sxs-lookup"><span data-stu-id="4a80e-132">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4a80e-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4a80e-133">Header</span></span><br/>  | <dl> <span data-ttu-id="4a80e-134"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a80e-134"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="4a80e-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="4a80e-135">Library</span></span><br/> | <dl> <span data-ttu-id="4a80e-136"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4a80e-136"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a80e-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4a80e-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a80e-138">**Interfaccia IAMTimelineEffectable**</span><span class="sxs-lookup"><span data-stu-id="4a80e-138">**IAMTimelineEffectable Interface**</span></span>](iamtimelineeffectable.md)
</dt> <dt>

[<span data-ttu-id="4a80e-139">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="4a80e-139">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




