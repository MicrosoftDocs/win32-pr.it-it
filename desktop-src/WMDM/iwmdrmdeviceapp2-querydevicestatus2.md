---
title: Metodo IWMDRMDeviceApp2 QueryDeviceStatus2 (WMDRMDeviceApp. h)
description: Il metodo QueryDeviceStatus2 esegue una query su un dispositivo per uno stato o una funzionalità DRM specifica.
ms.assetid: f7e95fb7-5929-4a70-8580-a443e152e6d1
keywords:
- Metodo QueryDeviceStatus2 Windows Media Gestione dispositivi
- Metodo QueryDeviceStatus2 Windows Media Gestione dispositivi, interfaccia IWMDRMDeviceApp2
- Interfaccia IWMDRMDeviceApp2 Windows Media Gestione dispositivi, metodo QueryDeviceStatus2
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp2.QueryDeviceStatus2
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 338d1f03f8d1e63086bb260c9854c7dcf3e88514
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329207"
---
# <a name="iwmdrmdeviceapp2querydevicestatus2-method"></a><span data-ttu-id="7a268-106">Metodo IWMDRMDeviceApp2:: QueryDeviceStatus2</span><span class="sxs-lookup"><span data-stu-id="7a268-106">IWMDRMDeviceApp2::QueryDeviceStatus2 method</span></span>

<span data-ttu-id="7a268-107">Il metodo **QueryDeviceStatus2** esegue una query su un dispositivo per uno stato o una funzionalità DRM specifica.</span><span class="sxs-lookup"><span data-stu-id="7a268-107">The **QueryDeviceStatus2** method queries a device for a specific DRM status or capability.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a268-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7a268-108">Syntax</span></span>


```C++
HRESULT QueryDeviceStatus2(
  [in]  IWMDMDevice *pDevice,
  [in]  DWORD       dwFlags,
  [out] DWORD       *pdwStatus
);
```



## <a name="parameters"></a><span data-ttu-id="7a268-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="7a268-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a268-110">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7a268-110">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a268-111">Puntatore a un oggetto [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) .</span><span class="sxs-lookup"><span data-stu-id="7a268-111">Pointer to an [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) object.</span></span>

</dd> <dt>

<span data-ttu-id="7a268-112">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7a268-112">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a268-113">Uno o più dei seguenti valori **DWORD** che specificano le funzionalità da richiedere, combinati con un **or** bit per bit.</span><span class="sxs-lookup"><span data-stu-id="7a268-113">One or more of the following **DWORD** values specifying which capabilities to request, combined with a bitwise **OR**.</span></span>



| <span data-ttu-id="7a268-114">Flag</span><span class="sxs-lookup"><span data-stu-id="7a268-114">Flag</span></span>                              | <span data-ttu-id="7a268-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7a268-115">Description</span></span>                                                                  |
|-----------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="7a268-116">\_ \_ INDIVSTATUS client query \_ WMDRM</span><span class="sxs-lookup"><span data-stu-id="7a268-116">WMDRM\_QUERY\_CLIENT\_INDIVSTATUS</span></span> | <span data-ttu-id="7a268-117">Eseguire una query per verificare se i componenti DRM del computer devono essere personalizzati.</span><span class="sxs-lookup"><span data-stu-id="7a268-117">Query whether the computer's DRM components need to be individualized.</span></span>       |
| <span data-ttu-id="7a268-118">\_CLOCKSTATUS del \_ dispositivo di query WMDRM \_</span><span class="sxs-lookup"><span data-stu-id="7a268-118">WMDRM\_QUERY\_DEVICE\_CLOCKSTATUS</span></span> | <span data-ttu-id="7a268-119">Eseguire una query per verificare se è necessario aggiungere o aggiornare il clock sicuro del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7a268-119">Query whether the device's secure clock needs to be added or updated.</span></span>        |
| <span data-ttu-id="7a268-120">il dispositivo di query WMDRM è stato \_ \_ \_ revocato</span><span class="sxs-lookup"><span data-stu-id="7a268-120">WMDRM\_QUERY\_DEVICE\_ISREVOKED</span></span>   | <span data-ttu-id="7a268-121">Eseguire una query sull'eventuale revoca del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7a268-121">Query whether the device is revoked.</span></span>                                         |
| <span data-ttu-id="7a268-122">\_ISWMDRM del \_ dispositivo di query WMDRM \_</span><span class="sxs-lookup"><span data-stu-id="7a268-122">WMDRM\_QUERY\_DEVICE\_ISWMDRM</span></span>     | <span data-ttu-id="7a268-123">Eseguire una query per verificare se il dispositivo supporta Windows Media DRM 10 per i dispositivi portatili.</span><span class="sxs-lookup"><span data-stu-id="7a268-123">Query whether the device supports Windows Media DRM 10 for Portable Devices.</span></span> |



 

</dd> <dt>

<span data-ttu-id="7a268-124">*pdwStatus* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="7a268-124">*pdwStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7a268-125">Zero o più dei seguenti valori **DWORD** che specificano lo stato del dispositivo richiesto, combinati con un **or** bit per bit.</span><span class="sxs-lookup"><span data-stu-id="7a268-125">Zero or more of the following **DWORD** values specifying the requested device status, combined with a bitwise **OR**.</span></span>



| <span data-ttu-id="7a268-126">Stato</span><span class="sxs-lookup"><span data-stu-id="7a268-126">Status</span></span>                      | <span data-ttu-id="7a268-127">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7a268-127">Description</span></span>                                              |
|-----------------------------|----------------------------------------------------------|
| <span data-ttu-id="7a268-128">\_ISWMDRM del dispositivo WMDRM \_</span><span class="sxs-lookup"><span data-stu-id="7a268-128">WMDRM\_DEVICE\_ISWMDRM</span></span>      | <span data-ttu-id="7a268-129">Il dispositivo supporta Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="7a268-129">The device supports Windows Media DRM.</span></span>                   |
| <span data-ttu-id="7a268-130">\_NEEDCLOCK del dispositivo WMDRM \_</span><span class="sxs-lookup"><span data-stu-id="7a268-130">WMDRM\_DEVICE\_NEEDCLOCK</span></span>    | <span data-ttu-id="7a268-131">Il dispositivo non ha un clock protetto.</span><span class="sxs-lookup"><span data-stu-id="7a268-131">The device does not have a secure clock.</span></span>                 |
| <span data-ttu-id="7a268-132">il dispositivo WMDRM è stato \_ \_ revocato</span><span class="sxs-lookup"><span data-stu-id="7a268-132">WMDRM\_DEVICE\_REVOKED</span></span>      | <span data-ttu-id="7a268-133">Il dispositivo è stato revocato.</span><span class="sxs-lookup"><span data-stu-id="7a268-133">The device has been revoked.</span></span>                             |
| <span data-ttu-id="7a268-134">\_NEEDINDIV client \_ WMDRM</span><span class="sxs-lookup"><span data-stu-id="7a268-134">WMDRM\_CLIENT\_NEEDINDIV</span></span>    | <span data-ttu-id="7a268-135">I componenti DRM del computer devono essere personalizzati.</span><span class="sxs-lookup"><span data-stu-id="7a268-135">The computer's DRM components need to be individualized.</span></span> |
| <span data-ttu-id="7a268-136">\_REFRESHCLOCK del dispositivo WMDRM \_</span><span class="sxs-lookup"><span data-stu-id="7a268-136">WMDRM\_DEVICE\_REFRESHCLOCK</span></span> | <span data-ttu-id="7a268-137">È necessario aggiornare il clock.</span><span class="sxs-lookup"><span data-stu-id="7a268-137">The clock needs to be refreshed.</span></span>                         |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a268-138">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7a268-138">Return value</span></span>

<span data-ttu-id="7a268-139">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="7a268-139">The method returns an **HRESULT**.</span></span> <span data-ttu-id="7a268-140">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="7a268-140">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="7a268-141">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="7a268-141">Return code</span></span>                                                                                                              | <span data-ttu-id="7a268-142">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7a268-142">Description</span></span>                                                               |
|--------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7a268-143"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7a268-143"><dt>**S\_OK**</dt></span></span> </dl>                                     | <span data-ttu-id="7a268-144">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="7a268-144">The method succeeded.</span></span><br/>                                          |
| <dl> <span data-ttu-id="7a268-145"><dt>**DRM \_ E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="7a268-145"><dt>**DRM\_E\_INVALIDARG**</dt></span></span> </dl>                        | <span data-ttu-id="7a268-146">Uno o più argomenti non sono validi.</span><span class="sxs-lookup"><span data-stu-id="7a268-146">One or more arguments are not valid.</span></span><br/>                           |
| <dl> <span data-ttu-id="7a268-147"><dt>**\_ \_ \_ certificato non valido per NS E DRM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7a268-147"><dt>**NS\_E\_DRM\_INVALID\_CERTIFICATE**</dt></span></span> </dl>          | <span data-ttu-id="7a268-148">Il certificato del dispositivo recuperato dal dispositivo non è valido.</span><span class="sxs-lookup"><span data-stu-id="7a268-148">The device certificate retrieved from the device is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="7a268-149"><dt>**NS \_ E \_ DRM \_ non riescono \_ a \_ ottenere il \_ certificato del dispositivo \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7a268-149"><dt>**NS\_E\_DRM\_UNABLE\_TO\_GET\_DEVICE\_CERT**</dt></span></span> </dl> | <span data-ttu-id="7a268-150">Non è stato possibile recuperare il certificato del dispositivo dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7a268-150">Failed to retrieve the device certificate from the device.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="7a268-151">Commenti</span><span class="sxs-lookup"><span data-stu-id="7a268-151">Remarks</span></span>

<span data-ttu-id="7a268-152">Questo metodo deve essere chiamato prima di eseguire qualsiasi azione limitata sul contenuto DRM, ad esempio il trasferimento di contenuto DRM al dispositivo o l'acquisizione di informazioni di misurazione.</span><span class="sxs-lookup"><span data-stu-id="7a268-152">This method should be called before performing any restricted actions on DRM content, such as transferring DRM content to the device, or acquiring metering information.</span></span> <span data-ttu-id="7a268-153">Se i valori recuperati *da pdwStatus* indicano che è necessario eseguire un'azione, ad esempio l'individualizzazione per il desktop o l'acquisizione di un clock per il dispositivo, l'applicazione deve [**chiamare IWMDRMDeviceApp:: AcquireDeviceData**](iwmdrmdeviceapp-acquiredevicedata.md) e passare il valore *pdwStatus* recuperato da questa funzione al parametro *dwFlags* in **AcquireDeviceData**.</span><span class="sxs-lookup"><span data-stu-id="7a268-153">If the values retrieved by *pdwStatus* indicate that some action needs to be performed (such as individualization for the desktop or acquiring a clock for the device), the application should call [**IWMDRMDeviceApp::AcquireDeviceData**](iwmdrmdeviceapp-acquiredevicedata.md) and pass in the retrieved *pdwStatus* value from this function to the *dwFlags* parameter in **AcquireDeviceData**.</span></span> <span data-ttu-id="7a268-154">Se viene restituito zero, il dispositivo non supporta Windows Media DRM 10 per i dispositivi portatili e non è necessario eseguire alcuna azione.</span><span class="sxs-lookup"><span data-stu-id="7a268-154">If zero is returned, the device does not support Windows Media DRM 10 for Portable Devices, and no actions need be taken.</span></span> <span data-ttu-id="7a268-155">Per ulteriori informazioni, vedere [gestione del contenuto protetto nell'applicazione](handling-protected-content-in-the-application.md) .</span><span class="sxs-lookup"><span data-stu-id="7a268-155">See [Handling Protected Content in the Application](handling-protected-content-in-the-application.md) for more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a268-156">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7a268-156">Requirements</span></span>



| <span data-ttu-id="7a268-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a268-157">Requirement</span></span> | <span data-ttu-id="7a268-158">Valore</span><span class="sxs-lookup"><span data-stu-id="7a268-158">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a268-159">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7a268-159">Header</span></span><br/>  | <dl> <span data-ttu-id="7a268-160"><dt>WMDRMDeviceApp. h (richiede anche Wmdrmdeviceapp \_ i. c, compilato da WMDRMDeviceApp. idl)</dt></span><span class="sxs-lookup"><span data-stu-id="7a268-160"><dt>WMDRMDeviceApp.h (also requires Wmdrmdeviceapp\_i.c, built from WMDRMDeviceApp.idl)</dt></span></span> </dl> |
| <span data-ttu-id="7a268-161">Libreria</span><span class="sxs-lookup"><span data-stu-id="7a268-161">Library</span></span><br/> | <dl> <span data-ttu-id="7a268-162"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7a268-162"><dt>Mssachlp.lib</dt></span></span> </dl>                                                                        |



## <a name="see-also"></a><span data-ttu-id="7a268-163">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7a268-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a268-164">**Gestione del contenuto protetto nell'applicazione**</span><span class="sxs-lookup"><span data-stu-id="7a268-164">**Handling Protected Content in the Application**</span></span>](handling-protected-content-in-the-application.md)
</dt> <dt>

[<span data-ttu-id="7a268-165">**IWMDRMDeviceApp::QueryDeviceStatus**</span><span class="sxs-lookup"><span data-stu-id="7a268-165">**IWMDRMDeviceApp::QueryDeviceStatus**</span></span>](iwmdrmdeviceapp-querydevicestatus.md)
</dt> <dt>

[<span data-ttu-id="7a268-166">**Interfaccia IWMDRMDeviceApp2**</span><span class="sxs-lookup"><span data-stu-id="7a268-166">**IWMDRMDeviceApp2 Interface**</span></span>](iwmdrmdeviceapp2.md)
</dt> </dl>

 

 





