---
title: Metodo IWMDRMDeviceApp GenerateMeterChallenge (WMDRMDeviceApp. h)
description: Il metodo GenerateMeterChallenge acquisisce i dati di misurazione da un dispositivo.
ms.assetid: 2457cab7-bd45-49a7-ba69-74ae022207ce
keywords:
- Metodo GenerateMeterChallenge Windows Media Gestione dispositivi
- Metodo GenerateMeterChallenge Windows Media Gestione dispositivi, interfaccia IWMDRMDeviceApp
- Interfaccia IWMDRMDeviceApp Windows Media Gestione dispositivi, metodo GenerateMeterChallenge
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp.GenerateMeterChallenge
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06a71f04a5837f09575a2f4bccf4b17e34e30d63
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327879"
---
# <a name="iwmdrmdeviceappgeneratemeterchallenge-method"></a><span data-ttu-id="59542-106">Metodo IWMDRMDeviceApp:: GenerateMeterChallenge</span><span class="sxs-lookup"><span data-stu-id="59542-106">IWMDRMDeviceApp::GenerateMeterChallenge method</span></span>

<span data-ttu-id="59542-107">Il metodo **GenerateMeterChallenge** acquisisce i dati di misurazione da un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="59542-107">The **GenerateMeterChallenge** method acquires metering data from a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="59542-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="59542-108">Syntax</span></span>


```C++
HRESULT GenerateMeterChallenge(
  [in]  IWMDMDevice *pDevice,
  [in]  BSTR        bstrMeterCert,
  [out] BSTR        *pbstrMeterURL,
  [out] BSTR        *pbstrMeterData
);
```



## <a name="parameters"></a><span data-ttu-id="59542-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="59542-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59542-110">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="59542-110">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59542-111">Puntatore a un'interfaccia [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) .</span><span class="sxs-lookup"><span data-stu-id="59542-111">Pointer to an [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) interface.</span></span> <span data-ttu-id="59542-112">Se l'applicazione passa **null**, vengono usate le informazioni di misurazione archiviate nel computer anziché le informazioni di controllo da un dispositivo connesso.</span><span class="sxs-lookup"><span data-stu-id="59542-112">If the application passes in **NULL**, metering information stored on the computer is used instead of metering information from a connected device.</span></span>

</dd> <dt>

<span data-ttu-id="59542-113">*bstrMeterCert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="59542-113">*bstrMeterCert* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59542-114">Certificato di misurazione dell'applicazione, come **BSTR**.</span><span class="sxs-lookup"><span data-stu-id="59542-114">The application's metering certificate, as a **BSTR**.</span></span> <span data-ttu-id="59542-115">Si tratta di un certificato firmato ricevuto da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="59542-115">This is a signed certificate received from Microsoft.</span></span>

</dd> <dt>

<span data-ttu-id="59542-116">*pbstrMeterURL* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="59542-116">*pbstrMeterURL* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="59542-117">URL in cui devono essere inviati i dati di misurazione.</span><span class="sxs-lookup"><span data-stu-id="59542-117">The URL where metering data should be sent.</span></span> <span data-ttu-id="59542-118">Questa operazione viene allocata da Windows Media Gestione dispositivi e deve essere libera dal chiamante utilizzando **SysFreeString**.</span><span class="sxs-lookup"><span data-stu-id="59542-118">This is allocated by Windows Media Device Manager, and must be free by the caller using **SysFreeString**.</span></span>

</dd> <dt>

<span data-ttu-id="59542-119">*pbstrMeterData* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="59542-119">*pbstrMeterData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="59542-120">Misurazione dei dati da inviare al servizio di controllo.</span><span class="sxs-lookup"><span data-stu-id="59542-120">Metering data to send to the metering service.</span></span> <span data-ttu-id="59542-121">Questa operazione viene allocata da Windows Media Gestione dispositivi e deve essere libera dal chiamante utilizzando **SysFreeString**.</span><span class="sxs-lookup"><span data-stu-id="59542-121">This is allocated by Windows Media Device Manager, and must be free by the caller using **SysFreeString**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59542-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="59542-122">Return value</span></span>

<span data-ttu-id="59542-123">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="59542-123">The method returns an **HRESULT**.</span></span> <span data-ttu-id="59542-124">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="59542-124">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="59542-125">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="59542-125">Return code</span></span>                                                                                                      | <span data-ttu-id="59542-126">Descrizione</span><span class="sxs-lookup"><span data-stu-id="59542-126">Description</span></span>                                                                   |
|------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="59542-127"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="59542-127"><dt>**S\_OK**</dt></span></span> </dl>                             | <span data-ttu-id="59542-128">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="59542-128">The method succeeded.</span></span><br/>                                              |
| <dl> <span data-ttu-id="59542-129"><dt>**DRM \_ E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="59542-129"><dt>**DRM\_E\_INVALIDARG**</dt></span></span> </dl>                | <span data-ttu-id="59542-130">Uno o più argomenti non sono validi.</span><span class="sxs-lookup"><span data-stu-id="59542-130">One or more arguments are not valid.</span></span><br/>                               |
| <dl> <span data-ttu-id="59542-131"><dt>**DRM \_ E \_ INVALIDXMLTAG**</dt></span><span class="sxs-lookup"><span data-stu-id="59542-131"><dt>**DRM\_E\_INVALIDXMLTAG**</dt></span></span> </dl>             | <span data-ttu-id="59542-132">Il formato XML non è corretto.</span><span class="sxs-lookup"><span data-stu-id="59542-132">XML is improperly formed.</span></span><br/>                                          |
| <dl> <span data-ttu-id="59542-133"><dt>**DRM \_ E \_ NOXMLCLOSETAG**</dt></span><span class="sxs-lookup"><span data-stu-id="59542-133"><dt>**DRM\_E\_NOXMLCLOSETAG**</dt></span></span> </dl>             | <span data-ttu-id="59542-134">Il formato XML non è corretto.</span><span class="sxs-lookup"><span data-stu-id="59542-134">XML is improperly formed.</span></span><br/>                                          |
| <dl> <span data-ttu-id="59542-135"><dt>**DRM \_ E \_ NOXMLOPENTAG**</dt></span><span class="sxs-lookup"><span data-stu-id="59542-135"><dt>**DRM\_E\_NOXMLOPENTAG**</dt></span></span> </dl>              | <span data-ttu-id="59542-136">Il formato XML non è corretto.</span><span class="sxs-lookup"><span data-stu-id="59542-136">XML is improperly formed.</span></span><br/>                                          |
| <dl> <span data-ttu-id="59542-137"><dt>**DRM \_ E \_ XMLNOTFOUND**</dt></span><span class="sxs-lookup"><span data-stu-id="59542-137"><dt>**DRM\_E\_XMLNOTFOUND**</dt></span></span> </dl>               | <span data-ttu-id="59542-138">Impossibile trovare un tag XML obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="59542-138">Failed to find a required XML tag.</span></span><br/>                                 |
| <dl> <span data-ttu-id="59542-139"><dt>**Errori dal dispositivo**</dt></span><span class="sxs-lookup"><span data-stu-id="59542-139"><dt>**Errors from the device**</dt></span></span> </dl>            | <span data-ttu-id="59542-140">Qualsiasi numero di errori del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="59542-140">Any of a number of device errors.</span></span><br/>                                  |
| <dl> <span data-ttu-id="59542-141"><dt>**Errori dal client DRM**</dt></span><span class="sxs-lookup"><span data-stu-id="59542-141"><dt>**Errors from the DRM Client**</dt></span></span> </dl>        | <span data-ttu-id="59542-142">Uno qualsiasi dei numerosi errori interni del client DRM.</span><span class="sxs-lookup"><span data-stu-id="59542-142">Any of a number of internal DRM client errors.</span></span><br/>                     |
| <dl> <span data-ttu-id="59542-143"><dt>**dispositivo NS \_ E \_ dispositivo \_ non \_ WMDRM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="59542-143"><dt>**NS\_E\_DEVICE\_NOT\_WMDRM\_DEVICE**</dt></span></span> </dl> | <span data-ttu-id="59542-144">Il dispositivo specificato non è un dispositivo compatibile con Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="59542-144">The specified device is not a Windows Media DRM compatible device.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="59542-145">Commenti</span><span class="sxs-lookup"><span data-stu-id="59542-145">Remarks</span></span>

<span data-ttu-id="59542-146">Prima di chiamare questo metodo, l'applicazione deve chiamare [**IWMDRMDeviceApp:: QueryDeviceStatus**](iwmdrmdeviceapp-querydevicestatus.md) o [**IWMDRMDeviceApp2:: QueryDeviceStatus2**](iwmdrmdeviceapp2-querydevicestatus2.md) per verificare che tutti i componenti DRM del dispositivo siano aggiornati.</span><span class="sxs-lookup"><span data-stu-id="59542-146">Before calling this method, the application should call [**IWMDRMDeviceApp::QueryDeviceStatus**](iwmdrmdeviceapp-querydevicestatus.md) or [**IWMDRMDeviceApp2::QueryDeviceStatus2**](iwmdrmdeviceapp2-querydevicestatus2.md) to verify that all the device's DRM components are up to date.</span></span> <span data-ttu-id="59542-147">Questo metodo può essere chiamato solo su un dispositivo che supporta Windows Media DRM 10 per i dispositivi portatili.</span><span class="sxs-lookup"><span data-stu-id="59542-147">This method can only be called on a device that supports Windows Media DRM 10 for Portable Devices.</span></span>

<span data-ttu-id="59542-148">I dati recuperati *pbstrMeterData* devono essere inviati all'URL specificato da *pbstrMeterURL*.</span><span class="sxs-lookup"><span data-stu-id="59542-148">The retrieved data *pbstrMeterData* should be sent to the URL specified by *pbstrMeterURL*.</span></span> <span data-ttu-id="59542-149">Assicurarsi di codificare in URL i dati recuperati in modo che non vengano modificati durante il trasferimento.</span><span class="sxs-lookup"><span data-stu-id="59542-149">Be sure to URL-encode the retrieved data so that it does not get modified during transfer.</span></span>

<span data-ttu-id="59542-150">Per ulteriori informazioni, vedere [gestione del contenuto protetto nell'applicazione](handling-protected-content-in-the-application.md) .</span><span class="sxs-lookup"><span data-stu-id="59542-150">See [Handling Protected Content in the Application](handling-protected-content-in-the-application.md) for more information.</span></span>

## <a name="examples"></a><span data-ttu-id="59542-151">Esempio</span><span class="sxs-lookup"><span data-stu-id="59542-151">Examples</span></span>

<span data-ttu-id="59542-152">Nell'esempio di codice C++ riportato di seguito viene creato un oggetto **WMDRMDeviceApp** , verifica che il dispositivo sia un dispositivo Windows Media DRM 10, che l'orologio sia accurato e quindi richiede i dati di misurazione.</span><span class="sxs-lookup"><span data-stu-id="59542-152">The following C++ code example creates a **WMDRMDeviceApp** object, verifies that the device is a Windows Media DRM 10 device, that its clock is accurate, and then requests the metering data.</span></span>


```C++
HRESULT hr = S_OK;
// Create the WMDRMDeviceApp object.
CComPtr<IWMDRMDeviceApp> pDRM;
hr = pDRM.CoCreateInstance(CLSID_WMDRMDeviceApp, 0, CLSCTX_ALL);

// Find out first if the device is a WMDRM 10 device, and if it requires
// any clock updates.
DWORD status = 0;
hr = pDRM->QueryDeviceStatus(pDevice, &status);

if (!(WMDRM_DEVICE_ISWMDRM & status)) // Device is not WMDRM 10. Nothing can be updated,
    return E_FAIL;                   // and metering cannot be performed.
else if (status & WMDRM_DEVICE_REVOKED) // Device is revoked.
    return E_FAIL;
else if (status & WMDRM_DEVICE_NEEDCLOCK || 
    status & WMDRM_CLIENT_NEEDINDIV ||
    status & WMDRM_DEVICE_REFRESHCLOCK)
{
    // Need to update device clock. 
    // Using custom function, which is synchronous.
    hr = myAcquireDeviceData(pDRM, pDevice, this, status, &result);
    if (hr != S_OK || result != 0)    // Couldn't perform the updates.
        return E_FAIL;    
}

// Any updates have been performed. Now get the metering information from the device.
CComBSTR meterCert(METERCERT);
CComBSTR URL;
CComBSTR rawdata;
CComBSTR data;
hr = pDRM->GenerateMeterChallenge(pDevice, meterCert, &URL, &rawdata);
if (hr == S_OK)
    ..... Send to URL...
```



## <a name="requirements"></a><span data-ttu-id="59542-153">Requisiti</span><span class="sxs-lookup"><span data-stu-id="59542-153">Requirements</span></span>



| <span data-ttu-id="59542-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="59542-154">Requirement</span></span> | <span data-ttu-id="59542-155">Valore</span><span class="sxs-lookup"><span data-stu-id="59542-155">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59542-156">Intestazione</span><span class="sxs-lookup"><span data-stu-id="59542-156">Header</span></span><br/>  | <dl> <span data-ttu-id="59542-157"><dt>WMDRMDeviceApp. h (richiede anche Wmdrmdeviceapp \_ i. c, compilato da WMDRMDeviceApp. idl)</dt></span><span class="sxs-lookup"><span data-stu-id="59542-157"><dt>WMDRMDeviceApp.h (also requires Wmdrmdeviceapp\_i.c, built from WMDRMDeviceApp.idl)</dt></span></span> </dl> |
| <span data-ttu-id="59542-158">Libreria</span><span class="sxs-lookup"><span data-stu-id="59542-158">Library</span></span><br/> | <dl> <span data-ttu-id="59542-159"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="59542-159"><dt>Mssachlp.lib</dt></span></span> </dl>                                                                        |



## <a name="see-also"></a><span data-ttu-id="59542-160">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="59542-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59542-161">**Gestione del contenuto protetto nell'applicazione**</span><span class="sxs-lookup"><span data-stu-id="59542-161">**Handling Protected Content in the Application**</span></span>](handling-protected-content-in-the-application.md)
</dt> <dt>

[<span data-ttu-id="59542-162">**Interfaccia IWMDMDevice**</span><span class="sxs-lookup"><span data-stu-id="59542-162">**IWMDMDevice Interface**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice)
</dt> <dt>

[<span data-ttu-id="59542-163">**Interfaccia IWMDRMDeviceApp**</span><span class="sxs-lookup"><span data-stu-id="59542-163">**IWMDRMDeviceApp Interface**</span></span>](iwmdrmdeviceapp.md)
</dt> </dl>

 

 





