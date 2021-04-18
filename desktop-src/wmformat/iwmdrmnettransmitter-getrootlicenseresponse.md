---
title: Metodo IWMDRMNetTransmitter GetRootLicenseResponse (wmdrmsdk. h)
description: Il metodo GetRootLicenseResponse genera un messaggio di risposta di licenza radice.
ms.assetid: c735ee52-f0e0-4404-881b-18ee9a7fa9f9
keywords:
- Metodo GetRootLicenseResponse Windows Media Format
- Metodo GetRootLicenseResponse Windows Media Format, interfaccia IWMDRMNetTransmitter
- Interfaccia IWMDRMNetTransmitter-formato Windows Media, metodo GetRootLicenseResponse
topic_type:
- apiref
api_name:
- IWMDRMNetTransmitter.GetRootLicenseResponse
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3497a3eaedb872b7d2c9eb5d7782d01f8b35462
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327463"
---
# <a name="iwmdrmnettransmittergetrootlicenseresponse-method"></a><span data-ttu-id="95175-106">Metodo IWMDRMNetTransmitter:: GetRootLicenseResponse</span><span class="sxs-lookup"><span data-stu-id="95175-106">IWMDRMNetTransmitter::GetRootLicenseResponse method</span></span>

<span data-ttu-id="95175-107">Il metodo **GetRootLicenseResponse** genera un messaggio di risposta di licenza radice.</span><span class="sxs-lookup"><span data-stu-id="95175-107">The **GetRootLicenseResponse** method generates a root license response message.</span></span>

## <a name="syntax"></a><span data-ttu-id="95175-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="95175-108">Syntax</span></span>


```C++
HRESULT GetRootLicenseResponse(
  [in]  BSTR  bstrKID,
  [out] BYTE  **ppbLicenseResponse,
  [out] DWORD *pcbLicenseResponse
);
```



## <a name="parameters"></a><span data-ttu-id="95175-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="95175-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95175-110">*bstrKID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="95175-110">*bstrKID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95175-111">Identificatore di chiave con codifica base64 da usare per la nuova licenza radice.</span><span class="sxs-lookup"><span data-stu-id="95175-111">Base64-encoded key identifier to be used for the new root license.</span></span> <span data-ttu-id="95175-112">L'identificatore di chiave deve essere un valore GUID generato in modo casuale.</span><span class="sxs-lookup"><span data-stu-id="95175-112">The key identifier should be a randomly generated GUID value.</span></span>

</dd> <dt>

<span data-ttu-id="95175-113">*ppbLicenseResponse* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="95175-113">*ppbLicenseResponse* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="95175-114">Indirizzo di una variabile che riceve l'indirizzo della risposta di licenza generata.</span><span class="sxs-lookup"><span data-stu-id="95175-114">Address of a variable that receives the address of the generated license response.</span></span> <span data-ttu-id="95175-115">Al termine di questi dati, è necessario rilasciare la memoria chiamando **CoTaskMemFree**.</span><span class="sxs-lookup"><span data-stu-id="95175-115">When finished with this data, you must release the memory by calling **CoTaskMemFree**.</span></span>

</dd> <dt>

<span data-ttu-id="95175-116">*pcbLicenseResponse* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="95175-116">*pcbLicenseResponse* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="95175-117">Indirizzo di una variabile che riceve le dimensioni della risposta di licenza, in byte.</span><span class="sxs-lookup"><span data-stu-id="95175-117">Address of a variable that receives the size of the license response, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95175-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="95175-118">Return value</span></span>

<span data-ttu-id="95175-119">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="95175-119">The method returns an **HRESULT**.</span></span> <span data-ttu-id="95175-120">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="95175-120">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="95175-121">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="95175-121">Return code</span></span>                                                                                                | <span data-ttu-id="95175-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="95175-122">Description</span></span>                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="95175-123"><dt>**NS \_ E \_ DRM di DRM \_ \_ troppo \_ piccoli**</dt></span><span class="sxs-lookup"><span data-stu-id="95175-123"><dt>**NS\_E\_DRM\_RIV\_TOO\_SMALL**</dt></span></span> </dl> | <span data-ttu-id="95175-124">È necessario un elenco di revoche di contenuti aggiornato.</span><span class="sxs-lookup"><span data-stu-id="95175-124">An updated content revocation list is needed.</span></span><br/> |
| <dl> <span data-ttu-id="95175-125"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="95175-125"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="95175-126">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="95175-126">The method succeeded.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="95175-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="95175-127">Remarks</span></span>

<span data-ttu-id="95175-128">La licenza radice generata viene creata usando le informazioni dei dati di richiesta della licenza, elaborati per l'interfaccia chiamando [**SetLicenseChallenge**](iwmdrmnettransmitter-setlicensechallenge.md).</span><span class="sxs-lookup"><span data-stu-id="95175-128">The generated root license is created using the information from the license challenge data, which is processed for the interface by calling [**SetLicenseChallenge**](iwmdrmnettransmitter-setlicensechallenge.md).</span></span>

<span data-ttu-id="95175-129">La licenza radice viene utilizzata per la generazione di licenze foglia, che viene eseguita chiamando il metodo [**GetLeafLicenseResponse**](iwmdrmnettransmitter-getleaflicenseresponse.md) .</span><span class="sxs-lookup"><span data-stu-id="95175-129">The root license is used in the generation of leaf licenses, which is accomplished by calling the [**GetLeafLicenseResponse**](iwmdrmnettransmitter-getleaflicenseresponse.md) method.</span></span> <span data-ttu-id="95175-130">L'interfaccia **IWMDRMNetTransmitter** gestisce una copia della licenza radice per tale uso.</span><span class="sxs-lookup"><span data-stu-id="95175-130">The **IWMDRMNetTransmitter** interface maintains a copy of the root license for that use.</span></span>

<span data-ttu-id="95175-131">La licenza radice creata chiamando questo metodo non dispone di alcun criterio ed è configurata in modo che non possa essere resa persistente nel dispositivo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="95175-131">The root license created by calling this method does not have any policies and is configured so that it cannot be persisted on the receiving device.</span></span>

## <a name="requirements"></a><span data-ttu-id="95175-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="95175-132">Requirements</span></span>



| <span data-ttu-id="95175-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="95175-133">Requirement</span></span> | <span data-ttu-id="95175-134">Valore</span><span class="sxs-lookup"><span data-stu-id="95175-134">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="95175-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="95175-135">Header</span></span><br/> | <dl> <span data-ttu-id="95175-136"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="95175-136"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95175-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="95175-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95175-138">**Interfaccia IWMDRMNetTransmitter**</span><span class="sxs-lookup"><span data-stu-id="95175-138">**IWMDRMNetTransmitter Interface**</span></span>](iwmdrmnettransmitter.md)
</dt> </dl>

 

 





