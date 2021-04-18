---
title: Metodo IWMDRMLicenseManagement CleanLicenseStore (wmdrmsdk. h)
description: Il metodo CleanLicenseStore rimuove le licenze inutilizzabili dall'archivio licenze temporaneo e deframmenta l'archivio licenze locale per migliorare le prestazioni.
ms.assetid: 07ddd6f8-a091-4c18-81d3-c4d0c6026b6b
keywords:
- Metodo CleanLicenseStore Windows Media Format
- Metodo CleanLicenseStore Windows Media Format, interfaccia IWMDRMLicenseManagement
- Interfaccia IWMDRMLicenseManagement-formato Windows Media, metodo CleanLicenseStore
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.CleanLicenseStore
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9327fd836cf742f5495c29767be93d914c0f187
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325564"
---
# <a name="iwmdrmlicensemanagementcleanlicensestore-method"></a><span data-ttu-id="11da0-106">Metodo IWMDRMLicenseManagement:: CleanLicenseStore</span><span class="sxs-lookup"><span data-stu-id="11da0-106">IWMDRMLicenseManagement::CleanLicenseStore method</span></span>

<span data-ttu-id="11da0-107">Il metodo **CleanLicenseStore** rimuove le licenze inutilizzabili dall'archivio licenze temporaneo e deframmenta l'archivio licenze locale per migliorare le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="11da0-107">The **CleanLicenseStore** method removes unusable licenses from the temporary license store and defragments the local license store to improve performance.</span></span>

## <a name="syntax"></a><span data-ttu-id="11da0-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="11da0-108">Syntax</span></span>


```C++
HRESULT CleanLicenseStore(
  [in]  DWORD    dwFlags,
  [out] IUnknown **ppunkCancelationCookie
);
```



## <a name="parameters"></a><span data-ttu-id="11da0-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="11da0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11da0-110">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="11da0-110">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11da0-111">Flag che specificano le opzioni di pulizia dell'archivio licenze da usare.</span><span class="sxs-lookup"><span data-stu-id="11da0-111">Flags specifying the license store cleaning options to use.</span></span> <span data-ttu-id="11da0-112">Impostare su una delle costanti nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="11da0-112">Set to one of the constants in the following table.</span></span>



| <span data-ttu-id="11da0-113">Costante</span><span class="sxs-lookup"><span data-stu-id="11da0-113">Constant</span></span>                            | <span data-ttu-id="11da0-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="11da0-114">Description</span></span>                                                                                                                                                                    |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11da0-115">\_sincronizzazione dell' \_ \_ archivio licenze clean WMDRM \_</span><span class="sxs-lookup"><span data-stu-id="11da0-115">WMDRM\_CLEAN\_LICENSE\_STORE\_SYNC</span></span>  | <span data-ttu-id="11da0-116">L'operazione di pulizia verrà eseguita in modo sincrono.</span><span class="sxs-lookup"><span data-stu-id="11da0-116">The clean operation will be performed synchronously.</span></span> <span data-ttu-id="11da0-117">Questo metodo non verrà restituito fino al completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="11da0-117">This method will not return until the operation is complete.</span></span>                                                              |
| <span data-ttu-id="11da0-118">WMDRM \_ Clean \_ License \_ Store \_ asincrono</span><span class="sxs-lookup"><span data-stu-id="11da0-118">WMDRM\_CLEAN\_LICENSE\_STORE\_ASYNC</span></span> | <span data-ttu-id="11da0-119">L'operazione di pulizia verrà eseguita in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="11da0-119">The clean operation will be performed asynchronously.</span></span> <span data-ttu-id="11da0-120">Questo metodo restituirà immediatamente.</span><span class="sxs-lookup"><span data-stu-id="11da0-120">This method will return immediately.</span></span> <span data-ttu-id="11da0-121">Al termine dell'operazione, verrà inviato l'evento multimediale MELicenseStoreCleaned.</span><span class="sxs-lookup"><span data-stu-id="11da0-121">When the operation is complete, the media event MELicenseStoreCleaned will be sent.</span></span> |



 

</dd> <dt>

<span data-ttu-id="11da0-122">*ppunkCancelationCookie* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="11da0-122">*ppunkCancelationCookie* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="11da0-123">Puntatore che riceve un puntatore all'interfaccia **IUnknown** di un oggetto che identifica la chiamata asincrona.</span><span class="sxs-lookup"><span data-stu-id="11da0-123">Pointer that receives a pointer to the **IUnknown** interface of an object that identifies this asynchronous call.</span></span> <span data-ttu-id="11da0-124">Questo puntatore di interfaccia può essere utilizzato per annullare la chiamata asincrona chiamando il metodo [**IWMDRMEventGenerator:: CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) .</span><span class="sxs-lookup"><span data-stu-id="11da0-124">This interface pointer can be used to cancel the asynchronous call by calling the [**IWMDRMEventGenerator::CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11da0-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="11da0-125">Return value</span></span>

<span data-ttu-id="11da0-126">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="11da0-126">The method returns an **HRESULT**.</span></span> <span data-ttu-id="11da0-127">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="11da0-127">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="11da0-128">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="11da0-128">Return code</span></span>                                                                                            | <span data-ttu-id="11da0-129">Descrizione</span><span class="sxs-lookup"><span data-stu-id="11da0-129">Description</span></span>                                                            |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="11da0-130"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="11da0-130"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="11da0-131">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="11da0-131">The method succeeded.</span></span><br/>                                       |
| <dl> <span data-ttu-id="11da0-132"><dt>**DRM \_ E \_ LICENSENOTFOUND**</dt></span><span class="sxs-lookup"><span data-stu-id="11da0-132"><dt>**DRM\_E\_LICENSENOTFOUND**</dt></span></span> </dl> | <span data-ttu-id="11da0-133">Nessun archivio licenze temporaneo nel computer client.</span><span class="sxs-lookup"><span data-stu-id="11da0-133">There is no temporary license store on the client computer.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="11da0-134">Commenti</span><span class="sxs-lookup"><span data-stu-id="11da0-134">Remarks</span></span>

<span data-ttu-id="11da0-135">Questo metodo viene eseguito in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="11da0-135">This method executes asynchronously.</span></span> <span data-ttu-id="11da0-136">Viene restituito immediatamente dopo la chiamata di e quindi genera un evento **MEWMDRMLicenseStoreCleaned** al termine dell'elaborazione.</span><span class="sxs-lookup"><span data-stu-id="11da0-136">It returns immediately after being called and then generates an **MEWMDRMLicenseStoreCleaned** event when processing is complete.</span></span>

<span data-ttu-id="11da0-137">Per ulteriori informazioni sull'utilizzo dei metodi asincroni delle API estese del client Windows Media DRM, vedere [utilizzo del modello di eventi Media Foundation](using-the-media-foundation-model.md).</span><span class="sxs-lookup"><span data-stu-id="11da0-137">For more information about using the asynchronous methods of the Windows Media DRM Client Extended APIs, see [Using the Media Foundation Event Model](using-the-media-foundation-model.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="11da0-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="11da0-138">Requirements</span></span>



| <span data-ttu-id="11da0-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="11da0-139">Requirement</span></span> | <span data-ttu-id="11da0-140">Valore</span><span class="sxs-lookup"><span data-stu-id="11da0-140">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="11da0-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="11da0-141">Header</span></span><br/>  | <dl> <span data-ttu-id="11da0-142"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="11da0-142"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="11da0-143">Libreria</span><span class="sxs-lookup"><span data-stu-id="11da0-143">Library</span></span><br/> | <dl> <span data-ttu-id="11da0-144"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="11da0-144"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11da0-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="11da0-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11da0-146">**Interfaccia IWMDRMLicenseManagement**</span><span class="sxs-lookup"><span data-stu-id="11da0-146">**IWMDRMLicenseManagement Interface**</span></span>](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





