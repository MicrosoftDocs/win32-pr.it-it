---
title: Metodo IWMDRMDeviceApp AcquireDeviceData (WMDRMDeviceApp. h)
description: Il metodo AcquireDeviceData Inizializza o reimposta un clock sicuro del dispositivo.
ms.assetid: 2f1cfdb9-0f07-4bee-94aa-b33b039453d0
keywords:
- Metodo AcquireDeviceData Windows Media Gestione dispositivi
- Metodo AcquireDeviceData Windows Media Gestione dispositivi, interfaccia IWMDRMDeviceApp
- Interfaccia IWMDRMDeviceApp Windows Media Gestione dispositivi, metodo AcquireDeviceData
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp.AcquireDeviceData
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 268572e5dad3dffd0fe15956a0ff145f277fb6db
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327880"
---
# <a name="iwmdrmdeviceappacquiredevicedata-method"></a><span data-ttu-id="8b74b-106">Metodo IWMDRMDeviceApp:: AcquireDeviceData</span><span class="sxs-lookup"><span data-stu-id="8b74b-106">IWMDRMDeviceApp::AcquireDeviceData method</span></span>

<span data-ttu-id="8b74b-107">Il metodo **AcquireDeviceData** Inizializza o reimposta un clock sicuro del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8b74b-107">The **AcquireDeviceData** method initializes or resets a device secure clock.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b74b-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8b74b-108">Syntax</span></span>


```C++
HRESULT AcquireDeviceData(
  [in]  IWMDMDevice    *pDevice,
  [in]  IWMDMProgress3 *pProgressCallback,
  [in]  DWORD          dwFlags,
  [out] DWORD          *pdwStatus
);
```



## <a name="parameters"></a><span data-ttu-id="8b74b-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="8b74b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b74b-110">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8b74b-110">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b74b-111">Puntatore a un'interfaccia [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) per il dispositivo che segnalerà i dati di misurazione.</span><span class="sxs-lookup"><span data-stu-id="8b74b-111">Pointer to an [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) interface for the device that will report metering data.</span></span>

</dd> <dt>

<span data-ttu-id="8b74b-112">*pProgressCallback* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8b74b-112">*pProgressCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b74b-113">Callback di stato tramite il quale l'applicazione può tenere traccia dello stato di avanzamento dell'evento o annullare l'evento.</span><span class="sxs-lookup"><span data-stu-id="8b74b-113">Progress callback through which the application can track the progress of the event, or cancel the event.</span></span> <span data-ttu-id="8b74b-114">Lo stato di avanzamento è identificato dal parametro *eventId* dei metodi [**IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3) .</span><span class="sxs-lookup"><span data-stu-id="8b74b-114">The progress is identified by the *EventId* parameter of [**IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3) methods.</span></span>

</dd> <dt>

<span data-ttu-id="8b74b-115">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8b74b-115">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b74b-116">Un **or** logico di uno o entrambi i flag seguenti, che specifica l'azione da eseguire.</span><span class="sxs-lookup"><span data-stu-id="8b74b-116">A logical **OR** of one or both of the following flags, specifying what action to perform.</span></span> <span data-ttu-id="8b74b-117">Questo valore viene recuperato dal parametro *pdwStatus* di [**IWMDRMDeviceApp:: QueryDeviceStatus**](iwmdrmdeviceapp-querydevicestatus.md) o [**IWMDRMDeviceApp2:: QueryDeviceStatus2**](iwmdrmdeviceapp2-querydevicestatus2.md).</span><span class="sxs-lookup"><span data-stu-id="8b74b-117">This value is retrieved from the *pdwStatus* parameter of [**IWMDRMDeviceApp::QueryDeviceStatus**](iwmdrmdeviceapp-querydevicestatus.md) or [**IWMDRMDeviceApp2::QueryDeviceStatus2**](iwmdrmdeviceapp2-querydevicestatus2.md).</span></span> <span data-ttu-id="8b74b-118">È possibile utilizzare direttamente il flag *pdwStatus* .</span><span class="sxs-lookup"><span data-stu-id="8b74b-118">You can use the *pdwStatus* flag directly.</span></span>



| <span data-ttu-id="8b74b-119">Flag</span><span class="sxs-lookup"><span data-stu-id="8b74b-119">Flag</span></span>                        | <span data-ttu-id="8b74b-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8b74b-120">Description</span></span>                                   |
|-----------------------------|-----------------------------------------------|
| <span data-ttu-id="8b74b-121">\_NEEDCLOCK del dispositivo WMDRM \_</span><span class="sxs-lookup"><span data-stu-id="8b74b-121">WMDRM\_DEVICE\_NEEDCLOCK</span></span>    | <span data-ttu-id="8b74b-122">Acquisire un clock da un server di clock protetto.</span><span class="sxs-lookup"><span data-stu-id="8b74b-122">Acquire a clock from a secure clock server.</span></span>   |
| <span data-ttu-id="8b74b-123">\_REFRESHCLOCK del dispositivo WMDRM \_</span><span class="sxs-lookup"><span data-stu-id="8b74b-123">WMDRM\_DEVICE\_REFRESHCLOCK</span></span> | <span data-ttu-id="8b74b-124">Aggiornare l'orologio da un server di clock protetto.</span><span class="sxs-lookup"><span data-stu-id="8b74b-124">Refresh the clock from a secure clock server.</span></span> |



 

</dd> <dt>

<span data-ttu-id="8b74b-125">*pdwStatus* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="8b74b-125">*pdwStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8b74b-126">Uno dei seguenti valori **DWORD** che specifica lo stato restituito dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8b74b-126">One of the following **DWORD** values specifying the status returned by the device.</span></span>



| <span data-ttu-id="8b74b-127">Stato</span><span class="sxs-lookup"><span data-stu-id="8b74b-127">Status</span></span> | <span data-ttu-id="8b74b-128">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8b74b-128">Description</span></span>                                                     |
|--------|-----------------------------------------------------------------|
| <span data-ttu-id="8b74b-129">0</span><span class="sxs-lookup"><span data-stu-id="8b74b-129">0</span></span>      | <span data-ttu-id="8b74b-130">L'azione non è supportata.</span><span class="sxs-lookup"><span data-stu-id="8b74b-130">The action is not supported.</span></span>                                    |
| <span data-ttu-id="8b74b-131">1</span><span class="sxs-lookup"><span data-stu-id="8b74b-131">1</span></span>      | <span data-ttu-id="8b74b-132">Non è stato possibile acquisire il clock sicuro del dispositivo dal servizio.</span><span class="sxs-lookup"><span data-stu-id="8b74b-132">The device secure clock could not be acquired from the service.</span></span> |
| <span data-ttu-id="8b74b-133">2</span><span class="sxs-lookup"><span data-stu-id="8b74b-133">2</span></span>      | <span data-ttu-id="8b74b-134">Non è stato possibile impostare il clock sicuro del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8b74b-134">The device's secure clock could not be set.</span></span>                     |
| <span data-ttu-id="8b74b-135">3</span><span class="sxs-lookup"><span data-stu-id="8b74b-135">3</span></span>      | <span data-ttu-id="8b74b-136">È stato impostato il clock sicuro del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8b74b-136">The device's secure clock was set.</span></span>                              |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b74b-137">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8b74b-137">Return value</span></span>

<span data-ttu-id="8b74b-138">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="8b74b-138">The method returns an **HRESULT**.</span></span> <span data-ttu-id="8b74b-139">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="8b74b-139">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="8b74b-140">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="8b74b-140">Return code</span></span>                                                                                                                             | <span data-ttu-id="8b74b-141">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8b74b-141">Description</span></span>                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8b74b-142"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8b74b-142"><dt>**S\_OK**</dt></span></span> </dl>                                                    | <span data-ttu-id="8b74b-143">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="8b74b-143">The method succeeded.</span></span><br/>                                                                                                    |
| <dl> <span data-ttu-id="8b74b-144"><dt>**DRM \_ E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="8b74b-144"><dt>**DRM\_E\_INVALIDARG**</dt></span></span> </dl>                                       | <span data-ttu-id="8b74b-145">Uno o più argomenti non sono validi.</span><span class="sxs-lookup"><span data-stu-id="8b74b-145">One or more arguments are not valid.</span></span><br/>                                                                                     |
| <dl> <span data-ttu-id="8b74b-146"><dt>**dispositivo NS \_ E \_ dispositivo \_ non \_ WMDRM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8b74b-146"><dt>**NS\_E\_DEVICE\_NOT\_WMDRM\_DEVICE**</dt></span></span> </dl>                        | <span data-ttu-id="8b74b-147">Il dispositivo specificato non è un dispositivo compatibile con Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="8b74b-147">The specified device is not a Windows Media DRM compatible device.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="8b74b-148"><dt>**NS \_ E \_ DRM \_ non riescono \_ a \_ ottenere il \_ \_ Clock sicuro**</dt></span><span class="sxs-lookup"><span data-stu-id="8b74b-148"><dt>**NS\_E\_DRM\_UNABLE\_TO\_GET\_SECURE\_CLOCK**</dt></span></span> </dl>               | <span data-ttu-id="8b74b-149">Non è stato possibile recuperare la richiesta del clock protetto dal dispositivo o non è possibile recuperare l'URL del clock protetto dalla richiesta di verifica.</span><span class="sxs-lookup"><span data-stu-id="8b74b-149">Failed to retrieve secure clock challenge from the device or unable to retrieve the secure clock URL from the challenge.</span></span><br/> |
| <dl> <span data-ttu-id="8b74b-150"><dt>**NS \_ E \_ DRM \_ non riescono \_ a \_ ottenere il \_ \_ Clock protetto \_ dal \_ Server**</dt></span><span class="sxs-lookup"><span data-stu-id="8b74b-150"><dt>**NS\_E\_DRM\_UNABLE\_TO\_GET\_SECURE\_CLOCK\_FROM\_SERVER**</dt></span></span> </dl> | <span data-ttu-id="8b74b-151">Non è stato possibile recuperare la risposta del clock protetto dal server di clock protetto.</span><span class="sxs-lookup"><span data-stu-id="8b74b-151">Failed to retrieve the secure clock response from the secure clock server.</span></span><br/>                                               |
| <dl> <span data-ttu-id="8b74b-152"><dt>**NS \_ E \_ DRM \_ non \_ possono \_ impostare \_ il \_ Clock sicuro**</dt></span><span class="sxs-lookup"><span data-stu-id="8b74b-152"><dt>**NS\_E\_DRM\_UNABLE\_TO\_SET\_SECURE\_CLOCK**</dt></span></span> </dl>               | <span data-ttu-id="8b74b-153">Non è stato possibile inviare la richiesta di clock sicura al dispositivo o il dispositivo non è riuscito a impostare l'orologio.</span><span class="sxs-lookup"><span data-stu-id="8b74b-153">Failed to send the secure clock challenge to the device, or the device failed to set the clock.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="8b74b-154">Commenti</span><span class="sxs-lookup"><span data-stu-id="8b74b-154">Remarks</span></span>

<span data-ttu-id="8b74b-155">Si tratta di un metodo asincrono. il dispositivo deve attendere il callback [**IWMDMProgress:: end**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmprogress-end) per questa operazione prima di provare a riprodurre eventuali contenuti con licenza.</span><span class="sxs-lookup"><span data-stu-id="8b74b-155">This is an asynchronous method; the device must await the [**IWMDMProgress::End**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmprogress-end) callback for this operation before attempting to play any licensed content.</span></span>

<span data-ttu-id="8b74b-156">Un'applicazione può apprendere se il dispositivo deve essere reimpostato o aggiornato chiamando [**IWMDRMDeviceApp:: QueryDeviceStatus**](iwmdrmdeviceapp-querydevicestatus.md) o [**IWMDRMDeviceApp2:: QueryDeviceStatus2**](iwmdrmdeviceapp2-querydevicestatus2.md).</span><span class="sxs-lookup"><span data-stu-id="8b74b-156">An application can learn if the device must have its clock reset or updated by calling [**IWMDRMDeviceApp::QueryDeviceStatus**](iwmdrmdeviceapp-querydevicestatus.md) or [**IWMDRMDeviceApp2::QueryDeviceStatus2**](iwmdrmdeviceapp2-querydevicestatus2.md).</span></span>

<span data-ttu-id="8b74b-157">L'applicazione deve disporre di una connessione Internet per consentire all'utente di acquisire o reimpostare un clock protetto.</span><span class="sxs-lookup"><span data-stu-id="8b74b-157">Your application must have an Internet connection to enable it to acquire or reset a secure clock.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b74b-158">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8b74b-158">Requirements</span></span>



| <span data-ttu-id="8b74b-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b74b-159">Requirement</span></span> | <span data-ttu-id="8b74b-160">Valore</span><span class="sxs-lookup"><span data-stu-id="8b74b-160">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b74b-161">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8b74b-161">Header</span></span><br/>  | <dl> <span data-ttu-id="8b74b-162"><dt>WMDRMDeviceApp. h (richiede anche Wmdrmdeviceapp \_ i. c, compilato da WMDRMDeviceApp. idl)</dt></span><span class="sxs-lookup"><span data-stu-id="8b74b-162"><dt>WMDRMDeviceApp.h (also requires Wmdrmdeviceapp\_i.c, built from WMDRMDeviceApp.idl)</dt></span></span> </dl> |
| <span data-ttu-id="8b74b-163">Libreria</span><span class="sxs-lookup"><span data-stu-id="8b74b-163">Library</span></span><br/> | <dl> <span data-ttu-id="8b74b-164"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8b74b-164"><dt>Mssachlp.lib</dt></span></span> </dl>                                                                        |



## <a name="see-also"></a><span data-ttu-id="8b74b-165">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8b74b-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b74b-166">**Gestione del contenuto protetto nell'applicazione**</span><span class="sxs-lookup"><span data-stu-id="8b74b-166">**Handling Protected Content in the Application**</span></span>](handling-protected-content-in-the-application.md)
</dt> <dt>

[<span data-ttu-id="8b74b-167">**Interfaccia IWMDMDevice**</span><span class="sxs-lookup"><span data-stu-id="8b74b-167">**IWMDMDevice Interface**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice)
</dt> <dt>

[<span data-ttu-id="8b74b-168">**Interfaccia IWMDMProgress3**</span><span class="sxs-lookup"><span data-stu-id="8b74b-168">**IWMDMProgress3 Interface**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3)
</dt> <dt>

[<span data-ttu-id="8b74b-169">**Interfaccia IWMDRMDeviceApp**</span><span class="sxs-lookup"><span data-stu-id="8b74b-169">**IWMDRMDeviceApp Interface**</span></span>](iwmdrmdeviceapp.md)
</dt> </dl>

 

 





