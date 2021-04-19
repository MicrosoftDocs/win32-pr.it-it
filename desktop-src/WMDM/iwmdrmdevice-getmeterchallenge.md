---
title: Metodo IWMDRMDevice GetMeterChallenge
description: Il metodo GetMeterChallenge recupera la richiesta di misurazione.
ms.assetid: 4c122886-46bd-4e63-8e7d-5e6132363662
keywords:
- Metodo GetMeterChallenge Windows Media Gestione dispositivi
- Metodo GetMeterChallenge Windows Media Gestione dispositivi, interfaccia IWMDRMDevice
- Interfaccia IWMDRMDevice Windows Media Gestione dispositivi, metodo GetMeterChallenge
topic_type:
- apiref
api_name:
- IWMDRMDevice.GetMeterChallenge
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a916afa90d1db310041f9b92be94d3af9154df4b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324120"
---
# <a name="iwmdrmdevicegetmeterchallenge-method"></a><span data-ttu-id="54337-106">Metodo IWMDRMDevice:: GetMeterChallenge</span><span class="sxs-lookup"><span data-stu-id="54337-106">IWMDRMDevice::GetMeterChallenge method</span></span>

<span data-ttu-id="54337-107">Il metodo **GetMeterChallenge** recupera la richiesta di misurazione.</span><span class="sxs-lookup"><span data-stu-id="54337-107">The **GetMeterChallenge** method retrieves the metering challenge.</span></span>

## <a name="syntax"></a><span data-ttu-id="54337-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="54337-108">Syntax</span></span>


```C++
HRESULT GetMeterChallenge(
  [in]  BSTR  bstrMeterCert,
  [out] BYTE  **ppbMeterChallenge,
  [out] DWORD *pcbMeterChallenge
);
```



## <a name="parameters"></a><span data-ttu-id="54337-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="54337-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54337-110">*bstrMeterCert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="54337-110">*bstrMeterCert* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54337-111">Certificato di misurazione inviato dal proprietario del contenuto al computer host per la raccolta dei dati di misurazione associati nel dispositivo</span><span class="sxs-lookup"><span data-stu-id="54337-111">Metering certificate that the content owner sends to the host computer for collecting the associated metering data on the device</span></span>

</dd> <dt>

<span data-ttu-id="54337-112">*ppbMeterChallenge* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="54337-112">*ppbMeterChallenge* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="54337-113">Risultato della richiesta di misurazione recuperato.</span><span class="sxs-lookup"><span data-stu-id="54337-113">Retrieved metering challenge result.</span></span>

</dd> <dt>

<span data-ttu-id="54337-114">*pcbMeterChallenge* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="54337-114">*pcbMeterChallenge* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="54337-115">Dimensioni in byte della richiesta di misurazione.</span><span class="sxs-lookup"><span data-stu-id="54337-115">The size of the metering challenge, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54337-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="54337-116">Return value</span></span>

<span data-ttu-id="54337-117">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="54337-117">The method returns an **HRESULT**.</span></span> <span data-ttu-id="54337-118">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="54337-118">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="54337-119">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="54337-119">Return code</span></span>                                                                          | <span data-ttu-id="54337-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="54337-120">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="54337-121"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="54337-121"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="54337-122">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="54337-122">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="54337-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="54337-123">Remarks</span></span>

<span data-ttu-id="54337-124">I dati di misurazione vengono raccolti e archiviati nell'archivio dati DRM sul dispositivo per il contenuto con misurazione abilitata.</span><span class="sxs-lookup"><span data-stu-id="54337-124">Metering data is collected and stored in the DRM data store on the device for content with metering enabled.</span></span> <span data-ttu-id="54337-125">Verranno registrate azioni come Play.</span><span class="sxs-lookup"><span data-stu-id="54337-125">Actions such as play will be recorded.</span></span> <span data-ttu-id="54337-126">Quando questa funzione viene chiamata, il dispositivo raccoglie i dati di misurazione nell'archivio dati DRM sotto forma di documento XML e lo invia a Hostcomputer.</span><span class="sxs-lookup"><span data-stu-id="54337-126">When this function is called, the device collects the metering data in the DRM data store in the form of an XML document and sends it to the hostcomputer.</span></span> <span data-ttu-id="54337-127">Se la quantità di dati è eccessiva, viene inviata in fasi.</span><span class="sxs-lookup"><span data-stu-id="54337-127">If there is too much data, it is sent in phases.</span></span>

<span data-ttu-id="54337-128">Quando il computer host riceve i dati di controllo, invia i dati tramite Internet all'URL specificato nel certificato di misurazione.</span><span class="sxs-lookup"><span data-stu-id="54337-128">When the host computer receives the metering data, it sends the data over the Internet to the URL specified in the metering certificate.</span></span>

## <a name="requirements"></a><span data-ttu-id="54337-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="54337-129">Requirements</span></span>



| <span data-ttu-id="54337-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="54337-130">Requirement</span></span> | <span data-ttu-id="54337-131">Valore</span><span class="sxs-lookup"><span data-stu-id="54337-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="54337-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="54337-132">Header</span></span><br/>  | <dl> <span data-ttu-id="54337-133"><dt>WMDDRMSP. idl</dt></span><span class="sxs-lookup"><span data-stu-id="54337-133"><dt>WMDDRMSP.idl</dt></span></span> </dl> |
| <span data-ttu-id="54337-134">Libreria</span><span class="sxs-lookup"><span data-stu-id="54337-134">Library</span></span><br/> | <dl> <span data-ttu-id="54337-135"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="54337-135"><dt>Mssachlp.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54337-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="54337-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54337-137">**Interfaccia IWMDRMDevice**</span><span class="sxs-lookup"><span data-stu-id="54337-137">**IWMDRMDevice Interface**</span></span>](iwmdrmdevice.md)
</dt> </dl>

 

 





