---
title: Metodo IWMDRMDeviceApp QueryDeviceStatus (WMDRMDeviceApp. h)
description: Il metodo QueryDeviceStatus esegue una query su un dispositivo per lo stato e le funzionalità DRM correnti.
ms.assetid: cd5a75d5-d7f8-4077-a9fc-6e7ddd7c796b
keywords:
- Metodo QueryDeviceStatus Windows Media Gestione dispositivi
- Metodo QueryDeviceStatus Windows Media Gestione dispositivi, interfaccia IWMDRMDeviceApp
- Interfaccia IWMDRMDeviceApp Windows Media Gestione dispositivi, metodo QueryDeviceStatus
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp.QueryDeviceStatus
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8e0f4fad5ff9026ce70fc21712506eb4796d76b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327877"
---
# <a name="iwmdrmdeviceappquerydevicestatus-method"></a><span data-ttu-id="a47fe-106">Metodo IWMDRMDeviceApp:: QueryDeviceStatus</span><span class="sxs-lookup"><span data-stu-id="a47fe-106">IWMDRMDeviceApp::QueryDeviceStatus method</span></span>

<span data-ttu-id="a47fe-107">Il metodo **QueryDeviceStatus** esegue una query su un dispositivo per lo stato e le funzionalità DRM correnti.</span><span class="sxs-lookup"><span data-stu-id="a47fe-107">The **QueryDeviceStatus** method queries a device for its current DRM status and capabilities.</span></span>

## <a name="syntax"></a><span data-ttu-id="a47fe-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a47fe-108">Syntax</span></span>


```C++
HRESULT QueryDeviceStatus(
  [in]  IWMDMDevice *pDevice,
  [out] DWORD       *pdwStatus
);
```



## <a name="parameters"></a><span data-ttu-id="a47fe-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="a47fe-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a47fe-110">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a47fe-110">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a47fe-111">Puntatore a un oggetto [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) .</span><span class="sxs-lookup"><span data-stu-id="a47fe-111">Pointer to an [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) object.</span></span>

</dd> <dt>

<span data-ttu-id="a47fe-112">*pdwStatus* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a47fe-112">*pdwStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a47fe-113">Zero o più dei seguenti valori **DWORD** che descrivono gli aspetti DRM del dispositivo, combinati con un **or** bit per bit.</span><span class="sxs-lookup"><span data-stu-id="a47fe-113">Zero or more of the following **DWORD** values describing the DRM aspects of the device, combined with a bitwise **OR**.</span></span> <span data-ttu-id="a47fe-114">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="a47fe-114">See Remarks.</span></span>



| <span data-ttu-id="a47fe-115">Stato</span><span class="sxs-lookup"><span data-stu-id="a47fe-115">Status</span></span>                      | <span data-ttu-id="a47fe-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a47fe-116">Description</span></span>                                  |
|-----------------------------|----------------------------------------------|
| <span data-ttu-id="a47fe-117">\_ISWMDRM del dispositivo WMDRM \_</span><span class="sxs-lookup"><span data-stu-id="a47fe-117">WMDRM\_DEVICE\_ISWMDRM</span></span>      | <span data-ttu-id="a47fe-118">Il dispositivo supporta Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="a47fe-118">The device supports Windows Media DRM.</span></span>       |
| <span data-ttu-id="a47fe-119">\_NEEDCLOCK del dispositivo WMDRM \_</span><span class="sxs-lookup"><span data-stu-id="a47fe-119">WMDRM\_DEVICE\_NEEDCLOCK</span></span>    | <span data-ttu-id="a47fe-120">Il dispositivo non ha un clock protetto.</span><span class="sxs-lookup"><span data-stu-id="a47fe-120">The device does not have a secure clock.</span></span>     |
| <span data-ttu-id="a47fe-121">il dispositivo WMDRM è stato \_ \_ revocato</span><span class="sxs-lookup"><span data-stu-id="a47fe-121">WMDRM\_DEVICE\_REVOKED</span></span>      | <span data-ttu-id="a47fe-122">Il dispositivo è stato revocato.</span><span class="sxs-lookup"><span data-stu-id="a47fe-122">The device has been revoked.</span></span>                 |
| <span data-ttu-id="a47fe-123">\_NEEDINDIV client \_ WMDRM</span><span class="sxs-lookup"><span data-stu-id="a47fe-123">WMDRM\_CLIENT\_NEEDINDIV</span></span>    | <span data-ttu-id="a47fe-124">La protezione DRM deve essere individualizzata.</span><span class="sxs-lookup"><span data-stu-id="a47fe-124">The DRM security needs to be individualized.</span></span> |
| <span data-ttu-id="a47fe-125">\_REFRESHCLOCK del dispositivo WMDRM \_</span><span class="sxs-lookup"><span data-stu-id="a47fe-125">WMDRM\_DEVICE\_REFRESHCLOCK</span></span> | <span data-ttu-id="a47fe-126">È necessario aggiornare il clock.</span><span class="sxs-lookup"><span data-stu-id="a47fe-126">The clock needs to be refreshed.</span></span>             |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a47fe-127">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a47fe-127">Return value</span></span>

<span data-ttu-id="a47fe-128">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="a47fe-128">The method returns an **HRESULT**.</span></span> <span data-ttu-id="a47fe-129">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="a47fe-129">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="a47fe-130">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="a47fe-130">Return code</span></span>                                                                                                              | <span data-ttu-id="a47fe-131">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a47fe-131">Description</span></span>                                                               |
|--------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a47fe-132"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a47fe-132"><dt>**S\_OK**</dt></span></span> </dl>                                     | <span data-ttu-id="a47fe-133">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="a47fe-133">The method succeeded.</span></span><br/>                                          |
| <dl> <span data-ttu-id="a47fe-134"><dt>**DRM \_ E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="a47fe-134"><dt>**DRM\_E\_INVALIDARG**</dt></span></span> </dl>                        | <span data-ttu-id="a47fe-135">L'argomento di input non è valido.</span><span class="sxs-lookup"><span data-stu-id="a47fe-135">The input argument is not valid.</span></span><br/>                               |
| <dl> <span data-ttu-id="a47fe-136"><dt>**\_ \_ \_ certificato non valido per NS E DRM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a47fe-136"><dt>**NS\_E\_DRM\_INVALID\_CERTIFICATE**</dt></span></span> </dl>          | <span data-ttu-id="a47fe-137">Il certificato del dispositivo recuperato dal dispositivo non è valido.</span><span class="sxs-lookup"><span data-stu-id="a47fe-137">The device certificate retrieved from the device is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="a47fe-138"><dt>**NS \_ E \_ DRM \_ non riescono \_ a \_ ottenere il \_ certificato del dispositivo \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a47fe-138"><dt>**NS\_E\_DRM\_UNABLE\_TO\_GET\_DEVICE\_CERT**</dt></span></span> </dl> | <span data-ttu-id="a47fe-139">Non è stato possibile recuperare il certificato del dispositivo dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a47fe-139">Failed to retrieve the device certificate from the device.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="a47fe-140">Commenti</span><span class="sxs-lookup"><span data-stu-id="a47fe-140">Remarks</span></span>

<span data-ttu-id="a47fe-141">Questo metodo deve essere chiamato prima di eseguire qualsiasi azione limitata sul contenuto DRM, ad esempio il trasferimento di contenuto DRM al dispositivo o l'acquisizione di informazioni di misurazione.</span><span class="sxs-lookup"><span data-stu-id="a47fe-141">This method should be called before performing any restricted actions on DRM content, such as transferring DRM content to the device, or acquiring metering information.</span></span> <span data-ttu-id="a47fe-142">Se i valori recuperati da *pdwStatus* indicano che è necessario eseguire un'azione, ad esempio l'individualizzazione per il desktop o l'acquisizione di un clock per il dispositivo, l'applicazione deve chiamare [**AcquireDeviceData**](iwmdrmdeviceapp-acquiredevicedata.md) e passare il valore *pdwStatus* recuperato da questa funzione al parametro *dwFlags* in **AcquireDeviceData**.</span><span class="sxs-lookup"><span data-stu-id="a47fe-142">If the values retrieved by *pdwStatus* indicate that some action needs to be performed (such as individualization for the desktop or acquiring a clock for the device), the application should call [**AcquireDeviceData**](iwmdrmdeviceapp-acquiredevicedata.md) and pass the retrieved *pdwStatus* value from this function to the *dwFlags* parameter in **AcquireDeviceData**.</span></span> <span data-ttu-id="a47fe-143">Se viene restituito zero, il dispositivo non supporta Windows Media DRM 10 per i dispositivi portatili e non è necessario eseguire alcuna azione.</span><span class="sxs-lookup"><span data-stu-id="a47fe-143">If zero is returned, the device does not support Windows Media DRM 10 for Portable Devices, and no actions need be taken.</span></span> <span data-ttu-id="a47fe-144">Per ulteriori informazioni, vedere [gestione del contenuto protetto nell'applicazione](handling-protected-content-in-the-application.md) .</span><span class="sxs-lookup"><span data-stu-id="a47fe-144">See [Handling Protected Content in the Application](handling-protected-content-in-the-application.md) for more information.</span></span>

## <a name="examples"></a><span data-ttu-id="a47fe-145">Esempio</span><span class="sxs-lookup"><span data-stu-id="a47fe-145">Examples</span></span>

<span data-ttu-id="a47fe-146">Nell'esempio di codice C++ riportato di seguito viene creato un oggetto **WMDRMDeviceApp** , verifica che il dispositivo sia un dispositivo Windows Media DRM 10, che l'orologio sia accurato e quindi richiede i dati di misurazione.</span><span class="sxs-lookup"><span data-stu-id="a47fe-146">The following C++ code example creates a **WMDRMDeviceApp** object, verifies that the device is a Windows Media DRM 10 device, that its clock is accurate, and then requests the metering data.</span></span>


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
```



## <a name="requirements"></a><span data-ttu-id="a47fe-147">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a47fe-147">Requirements</span></span>



| <span data-ttu-id="a47fe-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="a47fe-148">Requirement</span></span> | <span data-ttu-id="a47fe-149">Valore</span><span class="sxs-lookup"><span data-stu-id="a47fe-149">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a47fe-150">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a47fe-150">Header</span></span><br/>  | <dl> <span data-ttu-id="a47fe-151"><dt>WMDRMDeviceApp. h (richiede anche Wmdrmdeviceapp \_ i. c, compilato da WMDRMDeviceApp. idl)</dt></span><span class="sxs-lookup"><span data-stu-id="a47fe-151"><dt>WMDRMDeviceApp.h (also requires Wmdrmdeviceapp\_i.c, built from WMDRMDeviceApp.idl)</dt></span></span> </dl> |
| <span data-ttu-id="a47fe-152">Libreria</span><span class="sxs-lookup"><span data-stu-id="a47fe-152">Library</span></span><br/> | <dl> <span data-ttu-id="a47fe-153"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a47fe-153"><dt>Mssachlp.lib</dt></span></span> </dl>                                                                        |



## <a name="see-also"></a><span data-ttu-id="a47fe-154">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a47fe-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a47fe-155">**Gestione del contenuto protetto nell'applicazione**</span><span class="sxs-lookup"><span data-stu-id="a47fe-155">**Handling Protected Content in the Application**</span></span>](handling-protected-content-in-the-application.md)
</dt> <dt>

[<span data-ttu-id="a47fe-156">**Interfaccia IWMDRMDeviceApp**</span><span class="sxs-lookup"><span data-stu-id="a47fe-156">**IWMDRMDeviceApp Interface**</span></span>](iwmdrmdeviceapp.md)
</dt> <dt>

[<span data-ttu-id="a47fe-157">**IWMDRMDeviceApp2::QueryDeviceStatus2**</span><span class="sxs-lookup"><span data-stu-id="a47fe-157">**IWMDRMDeviceApp2::QueryDeviceStatus2**</span></span>](iwmdrmdeviceapp2-querydevicestatus2.md)
</dt> </dl>

 

 





