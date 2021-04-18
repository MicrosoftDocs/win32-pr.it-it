---
title: Metodo IWMDRMDeviceApp SynchronizeLicenses (WMDRMDeviceApp. h)
description: Il metodo SynchronizeLicenses aggiorna le licenze in un dispositivo quando sono vicine alla scadenza.
ms.assetid: 352378c1-7432-476c-98e9-d811165c020e
keywords:
- Metodo SynchronizeLicenses Windows Media Gestione dispositivi
- Metodo SynchronizeLicenses Windows Media Gestione dispositivi, interfaccia IWMDRMDeviceApp
- Interfaccia IWMDRMDeviceApp Windows Media Gestione dispositivi, metodo SynchronizeLicenses
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp.SynchronizeLicenses
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b08f3457fec55a0eb519419feddf4594a2cbfac0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329208"
---
# <a name="iwmdrmdeviceappsynchronizelicenses-method"></a><span data-ttu-id="0b1a4-106">Metodo IWMDRMDeviceApp:: SynchronizeLicenses</span><span class="sxs-lookup"><span data-stu-id="0b1a4-106">IWMDRMDeviceApp::SynchronizeLicenses method</span></span>

<span data-ttu-id="0b1a4-107">Il metodo **SynchronizeLicenses** aggiorna le licenze in un dispositivo quando sono vicine alla scadenza.</span><span class="sxs-lookup"><span data-stu-id="0b1a4-107">The **SynchronizeLicenses** method updates licenses on a device when they are close to expiring.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b1a4-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0b1a4-108">Syntax</span></span>


```C++
HRESULT SynchronizeLicenses(
  [in] IWMDMDevice    *pDevice,
  [in] IWMDMProgress3 *pProgressCallback,
  [in] DWORD          cMinCountThreshold,
  [in] DWORD          cMinHoursThreshold
);
```



## <a name="parameters"></a><span data-ttu-id="0b1a4-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="0b1a4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b1a4-110">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0b1a4-110">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b1a4-111">Puntatore a un oggetto [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) .</span><span class="sxs-lookup"><span data-stu-id="0b1a4-111">Pointer to an [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) object.</span></span>

</dd> <dt>

<span data-ttu-id="0b1a4-112">*pProgressCallback* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0b1a4-112">*pProgressCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b1a4-113">Callback di stato che riceverà lo stato di tutti i passaggi che potrebbero essere necessari per eseguire. Il passaggio viene identificato dal parametro *eventId* del metodo [**IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3) chiamato.</span><span class="sxs-lookup"><span data-stu-id="0b1a4-113">Progress callback that will receive progress of any steps that it might need to carry out. The step is identified by the *EventId* parameter of the [**IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3) method called.</span></span>

</dd> <dt>

<span data-ttu-id="0b1a4-114">*cMinCountThreshold* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0b1a4-114">*cMinCountThreshold* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b1a4-115">Numero minimo di Play rimanenti facoltativo in una licenza del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0b1a4-115">Optional minimum remaining play count on a device license.</span></span>

</dd> <dt>

<span data-ttu-id="0b1a4-116">*cMinHoursThreshold* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0b1a4-116">*cMinHoursThreshold* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b1a4-117">Numero minimo di ore rimanenti facoltative per una licenza del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0b1a4-117">Optional minimum remaining hours on a device license.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b1a4-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0b1a4-118">Return value</span></span>

<span data-ttu-id="0b1a4-119">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="0b1a4-119">The method returns an **HRESULT**.</span></span> <span data-ttu-id="0b1a4-120">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="0b1a4-120">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="0b1a4-121">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="0b1a4-121">Return code</span></span>                                                                                                         | <span data-ttu-id="0b1a4-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0b1a4-122">Description</span></span>                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0b1a4-123"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0b1a4-123"><dt>**S\_OK**</dt></span></span> </dl>                                | <span data-ttu-id="0b1a4-124">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="0b1a4-124">The method succeeded.</span></span><br/>                                                                                                                            |
| <dl> <span data-ttu-id="0b1a4-125"><dt>**DRM \_ E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="0b1a4-125"><dt>**DRM\_E\_INVALIDARG**</dt></span></span> </dl>                   | <span data-ttu-id="0b1a4-126">Uno o più argomenti non sono validi.</span><span class="sxs-lookup"><span data-stu-id="0b1a4-126">One or more arguments are not valid.</span></span><br/>                                                                                                             |
| <dl> <span data-ttu-id="0b1a4-127"><dt>**DRM \_ E \_ INVALIDXMLTAG**</dt></span><span class="sxs-lookup"><span data-stu-id="0b1a4-127"><dt>**DRM\_E\_INVALIDXMLTAG**</dt></span></span> </dl>                | <span data-ttu-id="0b1a4-128">Il formato XML non è corretto.</span><span class="sxs-lookup"><span data-stu-id="0b1a4-128">XML is improperly formed.</span></span><br/>                                                                                                                        |
| <dl> <span data-ttu-id="0b1a4-129"><dt>**DRM \_ E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="0b1a4-129"><dt>**DRM\_E\_NOTIMPL**</dt></span></span> </dl>                      | <span data-ttu-id="0b1a4-130">Questa funzionalità non è attualmente implementata.</span><span class="sxs-lookup"><span data-stu-id="0b1a4-130">This functionality is not currently implemented.</span></span> <span data-ttu-id="0b1a4-131">(SyncLicenses w/ *PDEVICE* = null)</span><span class="sxs-lookup"><span data-stu-id="0b1a4-131">(SyncLicenses w/ *pDevice* =NULL)</span></span><br/>                                                               |
| <dl> <span data-ttu-id="0b1a4-132"><dt>**DRM \_ E \_ NOXMLCLOSETAG**</dt></span><span class="sxs-lookup"><span data-stu-id="0b1a4-132"><dt>**DRM\_E\_NOXMLCLOSETAG**</dt></span></span> </dl>                | <span data-ttu-id="0b1a4-133">Il formato dell'XML di licenza non è corretto.</span><span class="sxs-lookup"><span data-stu-id="0b1a4-133">The license XML was improperly formed.</span></span><br/>                                                                                                           |
| <dl> <span data-ttu-id="0b1a4-134"><dt>**DRM \_ E \_ NOXMLOPENTAG**</dt></span><span class="sxs-lookup"><span data-stu-id="0b1a4-134"><dt>**DRM\_E\_NOXMLOPENTAG**</dt></span></span> </dl>                 | <span data-ttu-id="0b1a4-135">Il formato dell'XML di licenza non è corretto.</span><span class="sxs-lookup"><span data-stu-id="0b1a4-135">The license XML was improperly formed.</span></span><br/>                                                                                                           |
| <dl> <span data-ttu-id="0b1a4-136"><dt>**DRM \_ E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="0b1a4-136"><dt>**DRM\_E\_OUTOFMEMORY**</dt></span></span> </dl>                  | <span data-ttu-id="0b1a4-137">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="0b1a4-137">Out of memory.</span></span><br/>                                                                                                                                   |
| <dl> <span data-ttu-id="0b1a4-138"><dt>**DRM \_ E \_ XMLNOTFOUND**</dt></span><span class="sxs-lookup"><span data-stu-id="0b1a4-138"><dt>**DRM\_E\_XMLNOTFOUND**</dt></span></span> </dl>                  | <span data-ttu-id="0b1a4-139">Impossibile trovare un tag XML necessario nella licenza.</span><span class="sxs-lookup"><span data-stu-id="0b1a4-139">Failed to find a required XML tag in the license.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="0b1a4-140"><dt>**dispositivo NS \_ E \_ dispositivo \_ non \_ WMDRM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0b1a4-140"><dt>**NS\_E\_DEVICE\_NOT\_WMDRM\_DEVICE**</dt></span></span> </dl>    | <span data-ttu-id="0b1a4-141">Il dispositivo specificato non è un dispositivo compatibile con DRM di Windows Media.</span><span class="sxs-lookup"><span data-stu-id="0b1a4-141">The specified device is not a Windows Media DRM-compatible device.</span></span><br/>                                                                               |
| <dl> <span data-ttu-id="0b1a4-142"><dt>**NS \_ E \_ DRM \_ necessitano di un' \_ individualizzazione**</dt></span><span class="sxs-lookup"><span data-stu-id="0b1a4-142"><dt>**NS\_E\_DRM\_NEEDS\_INDIVIDUALIZATION**</dt></span></span> </dl> | <span data-ttu-id="0b1a4-143">Per eseguire questa funzione, il DRM richiede un black box individualizzato.</span><span class="sxs-lookup"><span data-stu-id="0b1a4-143">The DRM requires an individualized black box to perform this function.</span></span> <span data-ttu-id="0b1a4-144">In altre parole, Windows Media Format SDK richiede un aggiornamento della sicurezza.</span><span class="sxs-lookup"><span data-stu-id="0b1a4-144">In other words, the Windows Media Format SDK requires a security upgrade.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0b1a4-145">Commenti</span><span class="sxs-lookup"><span data-stu-id="0b1a4-145">Remarks</span></span>

<span data-ttu-id="0b1a4-146">Questa chiamata può essere eseguita solo su un dispositivo che supporta Windows Media DRM 10 per i dispositivi portatili.</span><span class="sxs-lookup"><span data-stu-id="0b1a4-146">This call can only be made on a device that supports Windows Media DRM 10 for Portable Devices.</span></span> <span data-ttu-id="0b1a4-147">È necessario specificare almeno un parametro di soglia.</span><span class="sxs-lookup"><span data-stu-id="0b1a4-147">You must specify at least one threshold parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b1a4-148">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0b1a4-148">Requirements</span></span>



| <span data-ttu-id="0b1a4-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b1a4-149">Requirement</span></span> | <span data-ttu-id="0b1a4-150">Valore</span><span class="sxs-lookup"><span data-stu-id="0b1a4-150">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b1a4-151">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0b1a4-151">Header</span></span><br/>  | <dl> <span data-ttu-id="0b1a4-152"><dt>WMDRMDeviceApp. h (richiede anche Wmdrmdeviceapp \_ i. c, compilato da WMDRMDeviceApp. idl)</dt></span><span class="sxs-lookup"><span data-stu-id="0b1a4-152"><dt>WMDRMDeviceApp.h (also requires Wmdrmdeviceapp\_i.c, built from WMDRMDeviceApp.idl)</dt></span></span> </dl> |
| <span data-ttu-id="0b1a4-153">Libreria</span><span class="sxs-lookup"><span data-stu-id="0b1a4-153">Library</span></span><br/> | <dl> <span data-ttu-id="0b1a4-154"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0b1a4-154"><dt>Mssachlp.lib</dt></span></span> </dl>                                                                        |



## <a name="see-also"></a><span data-ttu-id="0b1a4-155">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0b1a4-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b1a4-156">**Gestione del contenuto protetto nell'applicazione**</span><span class="sxs-lookup"><span data-stu-id="0b1a4-156">**Handling Protected Content in the Application**</span></span>](handling-protected-content-in-the-application.md)
</dt> <dt>

[<span data-ttu-id="0b1a4-157">**Interfaccia IWMDMProgress3**</span><span class="sxs-lookup"><span data-stu-id="0b1a4-157">**IWMDMProgress3 Interface**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3)
</dt> <dt>

[<span data-ttu-id="0b1a4-158">**Interfaccia IWMDRMDeviceApp**</span><span class="sxs-lookup"><span data-stu-id="0b1a4-158">**IWMDRMDeviceApp Interface**</span></span>](iwmdrmdeviceapp.md)
</dt> </dl>

 

 





