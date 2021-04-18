---
title: Metodo IWMDRMDeviceApp ProcessMeterResponse (WMDRMDeviceApp. h)
description: Il metodo ProcessMeterResponse Reimposta alcuni o tutti i conteggi di misurazione in un dispositivo, dopo che i dati del dispositivo sono stati inviati ed elaborati dal server.
ms.assetid: bafc4bb2-aa3c-4b2a-a818-1a78577cefc5
keywords:
- Metodo ProcessMeterResponse Windows Media Gestione dispositivi
- Metodo ProcessMeterResponse Windows Media Gestione dispositivi, interfaccia IWMDRMDeviceApp
- Interfaccia IWMDRMDeviceApp Windows Media Gestione dispositivi, metodo ProcessMeterResponse
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp.ProcessMeterResponse
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b57312dc2f401207e41f38f5bf75cddf69a13b1e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327878"
---
# <a name="iwmdrmdeviceappprocessmeterresponse-method"></a><span data-ttu-id="49f2b-106">IWMDRMDeviceApp::P metodo rocessMeterResponse</span><span class="sxs-lookup"><span data-stu-id="49f2b-106">IWMDRMDeviceApp::ProcessMeterResponse method</span></span>

<span data-ttu-id="49f2b-107">Il metodo **ProcessMeterResponse** Reimposta alcuni o tutti i conteggi di misurazione in un dispositivo, dopo che i dati del dispositivo sono stati inviati ed elaborati dal server.</span><span class="sxs-lookup"><span data-stu-id="49f2b-107">The **ProcessMeterResponse** method resets some or all of the metering counts on a device, after data from the device has been sent to and processed by the server.</span></span>

## <a name="syntax"></a><span data-ttu-id="49f2b-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="49f2b-108">Syntax</span></span>


```C++
HRESULT ProcessMeterResponse(
  [in]  IWMDMDevice *pDevice,
  [in]  BYTE        *pbResponse,
  [in]  DWORD       cbResponse,
  [out] DWORD       *pdwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="49f2b-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="49f2b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49f2b-110">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="49f2b-110">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49f2b-111">Puntatore a un oggetto [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) .</span><span class="sxs-lookup"><span data-stu-id="49f2b-111">Pointer to an [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) object.</span></span>

</dd> <dt>

<span data-ttu-id="49f2b-112">*pbResponse* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="49f2b-112">*pbResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49f2b-113">Risposta ricevuta da un server di controllo, dopo l'invio dei dati generati con [**GenerateMeterChallenge**](iwmdrmdeviceapp-generatemeterchallenge.md).</span><span class="sxs-lookup"><span data-stu-id="49f2b-113">Response received from a metering server, after sending data generated using [**GenerateMeterChallenge**](iwmdrmdeviceapp-generatemeterchallenge.md).</span></span>

</dd> <dt>

<span data-ttu-id="49f2b-114">*cbResponse* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="49f2b-114">*cbResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49f2b-115">Dimensioni di *pbResponse* in byte.</span><span class="sxs-lookup"><span data-stu-id="49f2b-115">Size of *pbResponse*, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="49f2b-116">*pdwFlags* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="49f2b-116">*pdwFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="49f2b-117">**Valore DWORD** della tabella seguente che indica se nel dispositivo sono presenti più dati di misurazione che devono essere elaborati.</span><span class="sxs-lookup"><span data-stu-id="49f2b-117">A **DWORD** from the following table indicating whether there is more metering data on the device that needs to be processed.</span></span>



| <span data-ttu-id="49f2b-118">Flag</span><span class="sxs-lookup"><span data-stu-id="49f2b-118">Flag</span></span>                            | <span data-ttu-id="49f2b-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="49f2b-119">Description</span></span>                                     |
|---------------------------------|-------------------------------------------------|
| <span data-ttu-id="49f2b-120">\_risposta contatore \_ WMDRM \_ tutti</span><span class="sxs-lookup"><span data-stu-id="49f2b-120">WMDRM\_METER\_RESPONSE\_ALL</span></span>     | <span data-ttu-id="49f2b-121">Tutti i dati di misurazione sono stati elaborati.</span><span class="sxs-lookup"><span data-stu-id="49f2b-121">All metering data has been processed.</span></span>           |
| <span data-ttu-id="49f2b-122">\_risposta contatore \_ WMDRM \_ parziale</span><span class="sxs-lookup"><span data-stu-id="49f2b-122">WMDRM\_METER\_RESPONSE\_PARTIAL</span></span> | <span data-ttu-id="49f2b-123">È necessario elaborare dati di misurazione aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="49f2b-123">Additional metering data needs to be processed.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49f2b-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="49f2b-124">Return value</span></span>

<span data-ttu-id="49f2b-125">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="49f2b-125">The method returns an **HRESULT**.</span></span> <span data-ttu-id="49f2b-126">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="49f2b-126">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="49f2b-127">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="49f2b-127">Return code</span></span>                                                                                                      | <span data-ttu-id="49f2b-128">Descrizione</span><span class="sxs-lookup"><span data-stu-id="49f2b-128">Description</span></span>                                                                   |
|------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="49f2b-129"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="49f2b-129"><dt>**S\_OK**</dt></span></span> </dl>                             | <span data-ttu-id="49f2b-130">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="49f2b-130">The method succeeded.</span></span><br/>                                              |
| <dl> <span data-ttu-id="49f2b-131"><dt>**DRM \_ E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="49f2b-131"><dt>**DRM\_E\_INVALIDARG**</dt></span></span> </dl>                | <span data-ttu-id="49f2b-132">Uno o più argomenti non sono validi.</span><span class="sxs-lookup"><span data-stu-id="49f2b-132">One or more arguments are not valid.</span></span><br/>                               |
| <dl> <span data-ttu-id="49f2b-133"><dt>**Errori dal dispositivo**</dt></span><span class="sxs-lookup"><span data-stu-id="49f2b-133"><dt>**Errors from the device**</dt></span></span> </dl>            | <span data-ttu-id="49f2b-134">Qualsiasi numero di errori del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="49f2b-134">Any of a number of device errors.</span></span><br/>                                  |
| <dl> <span data-ttu-id="49f2b-135"><dt>**Errori dal client DRM**</dt></span><span class="sxs-lookup"><span data-stu-id="49f2b-135"><dt>**Errors from the DRM Client**</dt></span></span> </dl>        | <span data-ttu-id="49f2b-136">Uno qualsiasi dei numerosi errori interni del client DRM.</span><span class="sxs-lookup"><span data-stu-id="49f2b-136">Any of a number of internal DRM client errors.</span></span><br/>                     |
| <dl> <span data-ttu-id="49f2b-137"><dt>**dispositivo NS \_ E \_ dispositivo \_ non \_ WMDRM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="49f2b-137"><dt>**NS\_E\_DEVICE\_NOT\_WMDRM\_DEVICE**</dt></span></span> </dl> | <span data-ttu-id="49f2b-138">Il dispositivo specificato non è un dispositivo compatibile con Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="49f2b-138">The specified device is not a Windows Media DRM compatible device.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="49f2b-139">Commenti</span><span class="sxs-lookup"><span data-stu-id="49f2b-139">Remarks</span></span>

<span data-ttu-id="49f2b-140">Altre informazioni sulla misurazione, inclusi esempi di codice, sono disponibili nel white paper relativo all' [uso di contenuti multimediali digitali con Windows Media DRM 10](/previous-versions//bb614723(v=vs.85)) sul sito Web MSDN.</span><span class="sxs-lookup"><span data-stu-id="49f2b-140">More information on metering, including code examples, can be found in the whitepaper [Metering the Use of Digital Media Content with Windows Media DRM 10](/previous-versions//bb614723(v=vs.85)) on the MSDN Web site.</span></span>

## <a name="requirements"></a><span data-ttu-id="49f2b-141">Requisiti</span><span class="sxs-lookup"><span data-stu-id="49f2b-141">Requirements</span></span>



| <span data-ttu-id="49f2b-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="49f2b-142">Requirement</span></span> | <span data-ttu-id="49f2b-143">Valore</span><span class="sxs-lookup"><span data-stu-id="49f2b-143">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49f2b-144">Intestazione</span><span class="sxs-lookup"><span data-stu-id="49f2b-144">Header</span></span><br/>  | <dl> <span data-ttu-id="49f2b-145"><dt>WMDRMDeviceApp. h (richiede anche Wmdrmdeviceapp \_ i. c, compilato da WMDRMDeviceApp. idl)</dt></span><span class="sxs-lookup"><span data-stu-id="49f2b-145"><dt>WMDRMDeviceApp.h (also requires Wmdrmdeviceapp\_i.c, built from WMDRMDeviceApp.idl)</dt></span></span> </dl> |
| <span data-ttu-id="49f2b-146">Libreria</span><span class="sxs-lookup"><span data-stu-id="49f2b-146">Library</span></span><br/> | <dl> <span data-ttu-id="49f2b-147"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="49f2b-147"><dt>Mssachlp.lib</dt></span></span> </dl>                                                                        |



## <a name="see-also"></a><span data-ttu-id="49f2b-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="49f2b-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49f2b-149">**Gestione del contenuto protetto nell'applicazione**</span><span class="sxs-lookup"><span data-stu-id="49f2b-149">**Handling Protected Content in the Application**</span></span>](handling-protected-content-in-the-application.md)
</dt> <dt>

[<span data-ttu-id="49f2b-150">**Interfaccia IWMDMDevice**</span><span class="sxs-lookup"><span data-stu-id="49f2b-150">**IWMDMDevice Interface**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice)
</dt> <dt>

[<span data-ttu-id="49f2b-151">**Interfaccia IWMDRMDeviceApp**</span><span class="sxs-lookup"><span data-stu-id="49f2b-151">**IWMDRMDeviceApp Interface**</span></span>](iwmdrmdeviceapp.md)
</dt> </dl>

 

