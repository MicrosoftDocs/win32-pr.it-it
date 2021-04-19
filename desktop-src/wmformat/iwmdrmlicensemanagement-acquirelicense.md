---
title: Metodo IWMDRMLicenseManagement AcquireLicense (wmdrmsdk. h)
description: Il metodo AcquireLicense acquisisce in modo asincrono una licenza da un URL specificato.
ms.assetid: 2e134f39-1f45-4d3a-b7c7-460aa0a250d0
keywords:
- Metodo AcquireLicense Windows Media Format
- Metodo AcquireLicense Windows Media Format, interfaccia IWMDRMLicenseManagement
- Interfaccia IWMDRMLicenseManagement-formato Windows Media, metodo AcquireLicense
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.AcquireLicense
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 279a3d4d84617c4a4fa5454d1f39f6f78f0cf3fd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327468"
---
# <a name="iwmdrmlicensemanagementacquirelicense-method"></a><span data-ttu-id="a1f6e-106">Metodo IWMDRMLicenseManagement:: AcquireLicense</span><span class="sxs-lookup"><span data-stu-id="a1f6e-106">IWMDRMLicenseManagement::AcquireLicense method</span></span>

<span data-ttu-id="a1f6e-107">Il metodo **AcquireLicense** acquisisce in modo asincrono una licenza da un URL specificato.</span><span class="sxs-lookup"><span data-stu-id="a1f6e-107">The **AcquireLicense** method asynchronously acquires a license from a specified URL.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1f6e-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a1f6e-108">Syntax</span></span>


```C++
HRESULT AcquireLicense(
  [in]  BSTR     bstrURL,
  [in]  BSTR     bstrHeaderData,
  [in]  BSTR     bstrActions,
  [in]  DWORD    dwFlags,
  [out] IUnknown **ppunkCancelationCookie
);
```



## <a name="parameters"></a><span data-ttu-id="a1f6e-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="a1f6e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1f6e-110">*bstrURL* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a1f6e-110">*bstrURL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1f6e-111">URL del server licenze da cui acquisire la licenza.</span><span class="sxs-lookup"><span data-stu-id="a1f6e-111">URL of the license server from which to acquire the license.</span></span> <span data-ttu-id="a1f6e-112">Passare **null** per fare in modo che il metodo analizzi l'URL dall'intestazione del contenuto.</span><span class="sxs-lookup"><span data-stu-id="a1f6e-112">Pass **NULL** to have the method parse the URL from the content header.</span></span>

</dd> <dt>

<span data-ttu-id="a1f6e-113">*bstrHeaderData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a1f6e-113">*bstrHeaderData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1f6e-114">Intestazione del contenuto da passare al server licenze.</span><span class="sxs-lookup"><span data-stu-id="a1f6e-114">Content header to be passed to the license server.</span></span> <span data-ttu-id="a1f6e-115">Se *bstrURL* è **null**, il metodo analizzerà l'URL da questa intestazione.</span><span class="sxs-lookup"><span data-stu-id="a1f6e-115">If *bstrURL* is **NULL**, the method will parse the URL from this header.</span></span> <span data-ttu-id="a1f6e-116">Se *dwFlags* è impostato su WMDRM \_ acquisisce \_ License \_ legacy \_ Unsilent, impostare questo valore sull'ID chiave anziché sull'intera intestazione Content.</span><span class="sxs-lookup"><span data-stu-id="a1f6e-116">If *dwFlags* is set to WMDRM\_ACQUIRE\_LICENSE\_LEGACY\_NONSILENT, set this value to the key ID instead of the entire content header.</span></span>

</dd> <dt>

<span data-ttu-id="a1f6e-117">*bstrActions* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a1f6e-117">*bstrActions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1f6e-118">Stringa contenente zero o più azioni per le quali richiedere l'autorizzazione per la licenza.</span><span class="sxs-lookup"><span data-stu-id="a1f6e-118">String containing zero or more actions for which to request permission in the license.</span></span> <span data-ttu-id="a1f6e-119">La stringa deve essere formattata come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="a1f6e-119">The string must be formatted as follows:</span></span>

-   <span data-ttu-id="a1f6e-120">Ogni azione deve essere definita all'interno di un elemento ACTION.</span><span class="sxs-lookup"><span data-stu-id="a1f6e-120">Each action must be defined within an ACTION element.</span></span> <span data-ttu-id="a1f6e-121">I dati dell'elemento sono la stringa dell'azione.</span><span class="sxs-lookup"><span data-stu-id="a1f6e-121">The data of the element is the action string.</span></span>
-   <span data-ttu-id="a1f6e-122">Tutti gli elementi ACTION devono essere contenuti all'interno di un elemento ACTION.</span><span class="sxs-lookup"><span data-stu-id="a1f6e-122">All ACTION elements must be contained within an ACTIONLIST element.</span></span>

    <span data-ttu-id="a1f6e-123">Ad esempio, la stringa per richiedere una licenza per riprodurre il contenuto è formattata come la seguente:</span><span class="sxs-lookup"><span data-stu-id="a1f6e-123">For example, the string to request a license to play content is formatted like this:</span></span>

    ```C++
    <ACTIONLIST><ACTION></ACTION></ACTIONLIST>
    ```

    

</dd> <dt>

<span data-ttu-id="a1f6e-124">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a1f6e-124">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1f6e-125">Flag dell'opzione di acquisizione delle licenze.</span><span class="sxs-lookup"><span data-stu-id="a1f6e-125">License acquisition option flags.</span></span> <span data-ttu-id="a1f6e-126">Impostare su una delle costanti nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="a1f6e-126">Set to one of the constants in the following table.</span></span>



| <span data-ttu-id="a1f6e-127">Costante</span><span class="sxs-lookup"><span data-stu-id="a1f6e-127">Constant</span></span>                                   | <span data-ttu-id="a1f6e-128">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a1f6e-128">Description</span></span>                                                                                                              |
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1f6e-129">WMDRM \_ acquisire la \_ licenza \_ invisibile all'utente</span><span class="sxs-lookup"><span data-stu-id="a1f6e-129">WMDRM\_ACQUIRE\_LICENSE\_SILENT</span></span>            | <span data-ttu-id="a1f6e-130">La licenza verrà emessa direttamente tramite Internet senza alcuna conferma da parte dell'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="a1f6e-130">The license will be issued directly over the Internet without any confirmation from the client application.</span></span>              |
| <span data-ttu-id="a1f6e-131">WMDRM \_ Acquisisci \_ licenza non \_ invisibile</span><span class="sxs-lookup"><span data-stu-id="a1f6e-131">WMDRM\_ACQUIRE\_LICENSE\_NONSILENT</span></span>         | <span data-ttu-id="a1f6e-132">Il sottosistema DRM creerà una richiesta di licenza che verrà restituita in modo asincrono per la pubblicazione nel server licenze.</span><span class="sxs-lookup"><span data-stu-id="a1f6e-132">The DRM subsystem will create a license request which will be returned asynchronously for posting to the license server.</span></span> |
| <span data-ttu-id="a1f6e-133">WMDRM \_ acquisire la \_ licenza \_ legacy non invisibile all' \_ utente</span><span class="sxs-lookup"><span data-stu-id="a1f6e-133">WMDRM\_ACQUIRE\_LICENSE\_LEGACY\_NONSILENT</span></span> | <span data-ttu-id="a1f6e-134">Analogamente a WMDRM \_ , Acquisisci \_ licenza \_ non invisibile ad eccezione del fatto che verrà creata una richiesta di licenza di DRM versione 1.</span><span class="sxs-lookup"><span data-stu-id="a1f6e-134">The same as WMDRM\_ACQUIRE\_LICENSE\_NONSILENT, except that a DRM version 1 license challenge will be created.</span></span>           |



 

</dd> <dt>

<span data-ttu-id="a1f6e-135">*ppunkCancelationCookie* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a1f6e-135">*ppunkCancelationCookie* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a1f6e-136">Puntatore che riceve un puntatore all'interfaccia **IUnknown** di un oggetto che identifica la chiamata asincrona.</span><span class="sxs-lookup"><span data-stu-id="a1f6e-136">Pointer that receives a pointer to the **IUnknown** interface of an object that identifies this asynchronous call.</span></span> <span data-ttu-id="a1f6e-137">Questo puntatore di interfaccia può essere utilizzato per annullare la chiamata asincrona chiamando il metodo [**IWMDRMEventGenerator:: CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) .</span><span class="sxs-lookup"><span data-stu-id="a1f6e-137">This interface pointer can be used to cancel the asynchronous call by calling the [**IWMDRMEventGenerator::CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1f6e-138">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a1f6e-138">Return value</span></span>

<span data-ttu-id="a1f6e-139">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="a1f6e-139">The method returns an **HRESULT**.</span></span> <span data-ttu-id="a1f6e-140">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="a1f6e-140">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="a1f6e-141">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="a1f6e-141">Return code</span></span>                                                                          | <span data-ttu-id="a1f6e-142">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a1f6e-142">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="a1f6e-143"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a1f6e-143"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="a1f6e-144">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="a1f6e-144">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a1f6e-145">Commenti</span><span class="sxs-lookup"><span data-stu-id="a1f6e-145">Remarks</span></span>

<span data-ttu-id="a1f6e-146">Questo metodo viene eseguito in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="a1f6e-146">This method executes asynchronously.</span></span> <span data-ttu-id="a1f6e-147">Viene restituito immediatamente dopo la chiamata di e quindi genera un evento **MEWMDRMLicenseAcquisitionCompleted** al termine dell'elaborazione.</span><span class="sxs-lookup"><span data-stu-id="a1f6e-147">It returns immediately after being called and then generates an **MEWMDRMLicenseAcquisitionCompleted** event when processing is complete.</span></span> <span data-ttu-id="a1f6e-148">Per le operazioni di acquisizione di licenze non Silent, il valore dell'evento ottenuto chiamando **IMFMediaEvent:: GetValue** è un puntatore **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="a1f6e-148">For non-silent license acquisition operations, the value of the event obtained by calling **IMFMediaEvent::GetValue** is an **IUnknown** pointer.</span></span> <span data-ttu-id="a1f6e-149">È possibile chiamare il metodo **QueryInterface** dell'interfaccia **IUnknown** recuperata per ottenere un'istanza dell'interfaccia [**IWMDRMNonSilentLicenseAquisition**](iwmdrmnonsilentlicenseaquisition.md) .</span><span class="sxs-lookup"><span data-stu-id="a1f6e-149">You can call the **QueryInterface** method of the retrieved **IUnknown** interface to get an instance of the [**IWMDRMNonSilentLicenseAquisition**](iwmdrmnonsilentlicenseaquisition.md) interface.</span></span>

<span data-ttu-id="a1f6e-150">Per ulteriori informazioni sull'utilizzo dei metodi asincroni delle API estese del client Windows Media DRM, vedere [utilizzo del modello di eventi Media Foundation](using-the-media-foundation-model.md).</span><span class="sxs-lookup"><span data-stu-id="a1f6e-150">For more information about using the asynchronous methods of the Windows Media DRM Client Extended APIs, see [Using the Media Foundation Event Model](using-the-media-foundation-model.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a1f6e-151">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a1f6e-151">Requirements</span></span>



| <span data-ttu-id="a1f6e-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1f6e-152">Requirement</span></span> | <span data-ttu-id="a1f6e-153">Valore</span><span class="sxs-lookup"><span data-stu-id="a1f6e-153">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a1f6e-154">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a1f6e-154">Header</span></span><br/>  | <dl> <span data-ttu-id="a1f6e-155"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="a1f6e-155"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="a1f6e-156">Libreria</span><span class="sxs-lookup"><span data-stu-id="a1f6e-156">Library</span></span><br/> | <dl> <span data-ttu-id="a1f6e-157"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a1f6e-157"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1f6e-158">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a1f6e-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1f6e-159">**Interfaccia IWMDRMLicenseManagement**</span><span class="sxs-lookup"><span data-stu-id="a1f6e-159">**IWMDRMLicenseManagement Interface**</span></span>](iwmdrmlicensemanagement.md)
</dt> <dt>

[<span data-ttu-id="a1f6e-160">**Acquisizione di una licenza invisibile all'utente**</span><span class="sxs-lookup"><span data-stu-id="a1f6e-160">**Silent License Acquisition**</span></span>](silent-license-acquisition.md)
</dt> </dl>

 

 





