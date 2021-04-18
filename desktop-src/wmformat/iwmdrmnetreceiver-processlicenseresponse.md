---
title: Metodo IWMDRMNetReceiver ProcessLicenseResponse (wmdrmsdk. h)
description: Il metodo ProcessLicenseResponse elabora la risposta di licenza inviata dal trasmettitore in risposta a una richiesta di licenza.
ms.assetid: b6d04651-746b-474e-8a02-6b7cbee9db46
keywords:
- Metodo ProcessLicenseResponse Windows Media Format
- Metodo ProcessLicenseResponse Windows Media Format, interfaccia IWMDRMNetReceiver
- Interfaccia IWMDRMNetReceiver-formato Windows Media, metodo ProcessLicenseResponse
topic_type:
- apiref
api_name:
- IWMDRMNetReceiver.ProcessLicenseResponse
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45a09ebab81b71e21b9ef922423a7bbe67b20596
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325555"
---
# <a name="iwmdrmnetreceiverprocesslicenseresponse-method"></a><span data-ttu-id="1801f-106">IWMDRMNetReceiver::P metodo rocessLicenseResponse</span><span class="sxs-lookup"><span data-stu-id="1801f-106">IWMDRMNetReceiver::ProcessLicenseResponse method</span></span>

<span data-ttu-id="1801f-107">Il metodo **ProcessLicenseResponse** elabora la risposta di licenza inviata dal trasmettitore in risposta a una richiesta di licenza.</span><span class="sxs-lookup"><span data-stu-id="1801f-107">The **ProcessLicenseResponse** method processes the license response that is sent by the transmitter in reply to a license challenge.</span></span>

## <a name="syntax"></a><span data-ttu-id="1801f-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1801f-108">Syntax</span></span>


```C++
HRESULT ProcessLicenseResponse(
  [in]  BYTE  *pbLicenseResponse,
  [in]  DWORD cbLicenseResponse,
  [out] BYTE  **ppbWMDRMNetLicenseRepresentation,
  [out] DWORD *pcbWMDRMNetLicenseRepresentation
);
```



## <a name="parameters"></a><span data-ttu-id="1801f-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="1801f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1801f-110">*pbLicenseResponse* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1801f-110">*pbLicenseResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1801f-111">Risposta di licenza ricevuta dal trasmettitore.</span><span class="sxs-lookup"><span data-stu-id="1801f-111">License response received from the transmitter.</span></span>

</dd> <dt>

<span data-ttu-id="1801f-112">*cbLicenseResponse* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1801f-112">*cbLicenseResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1801f-113">Dimensione della risposta in byte.</span><span class="sxs-lookup"><span data-stu-id="1801f-113">Size of the response in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="1801f-114">*ppbWMDRMNetLicenseRepresentation* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="1801f-114">*ppbWMDRMNetLicenseRepresentation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1801f-115">Indirizzo di una variabile che riceve l'indirizzo della rappresentazione di licenza interna per la licenza contenuta nel messaggio di risposta della licenza.</span><span class="sxs-lookup"><span data-stu-id="1801f-115">Address of a variable that receives the address of the internal license representation for the license contained in the license response message.</span></span> <span data-ttu-id="1801f-116">Al termine di questi dati, è necessario rilasciare la memoria chiamando **CoTaskMemFree**.</span><span class="sxs-lookup"><span data-stu-id="1801f-116">When finished with this data, you must release the memory by calling **CoTaskMemFree**.</span></span> <span data-ttu-id="1801f-117">Questo parametro può essere impostato su **null** se la rappresentazione della licenza non è necessaria.</span><span class="sxs-lookup"><span data-stu-id="1801f-117">This parameter may be set to **NULL** if the license representation is not needed.</span></span>

</dd> <dt>

<span data-ttu-id="1801f-118">*pcbWMDRMNetLicenseRepresentation* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="1801f-118">*pcbWMDRMNetLicenseRepresentation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1801f-119">Indirizzo di una variabile che riceve le dimensioni della rappresentazione di licenza.</span><span class="sxs-lookup"><span data-stu-id="1801f-119">Address of a variable that receives the size of the license representation.</span></span> <span data-ttu-id="1801f-120">Deve essere impostato su **null** se *ppbWMDRMNetLicenseRepresentation* è **null**.</span><span class="sxs-lookup"><span data-stu-id="1801f-120">Must be set to **NULL** if *ppbWMDRMNetLicenseRepresentation* is **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1801f-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1801f-121">Return value</span></span>

<span data-ttu-id="1801f-122">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="1801f-122">The method returns an **HRESULT**.</span></span> <span data-ttu-id="1801f-123">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="1801f-123">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="1801f-124">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="1801f-124">Return code</span></span>                                                                                                | <span data-ttu-id="1801f-125">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1801f-125">Description</span></span>                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="1801f-126"><dt>**NS \_ E \_ DRM di DRM \_ \_ troppo \_ piccoli**</dt></span><span class="sxs-lookup"><span data-stu-id="1801f-126"><dt>**NS\_E\_DRM\_RIV\_TOO\_SMALL**</dt></span></span> </dl> | <span data-ttu-id="1801f-127">È necessario un elenco di revoche di contenuti aggiornato.</span><span class="sxs-lookup"><span data-stu-id="1801f-127">An updated content revocation list is needed.</span></span><br/> |
| <dl> <span data-ttu-id="1801f-128"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1801f-128"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="1801f-129">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="1801f-129">The method succeeded.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="1801f-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="1801f-130">Remarks</span></span>

<span data-ttu-id="1801f-131">La risposta di licenza elaborata utilizzando questo metodo deve corrispondere all'ultima richiesta di licenza generata sul computer client.</span><span class="sxs-lookup"><span data-stu-id="1801f-131">The license response processed by using this method must correspond to the last license challenge generated on the client computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="1801f-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1801f-132">Requirements</span></span>



| <span data-ttu-id="1801f-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="1801f-133">Requirement</span></span> | <span data-ttu-id="1801f-134">Valore</span><span class="sxs-lookup"><span data-stu-id="1801f-134">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1801f-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1801f-135">Header</span></span><br/> | <dl> <span data-ttu-id="1801f-136"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="1801f-136"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1801f-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1801f-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1801f-138">**Interfaccia IWMDRMNetReceiver**</span><span class="sxs-lookup"><span data-stu-id="1801f-138">**IWMDRMNetReceiver Interface**</span></span>](iwmdrmnetreceiver.md)
</dt> <dt>

[<span data-ttu-id="1801f-139">**IWMDRMNetReceiver::GetLicenseChallenge**</span><span class="sxs-lookup"><span data-stu-id="1801f-139">**IWMDRMNetReceiver::GetLicenseChallenge**</span></span>](iwmdrmnetreceiver-getlicensechallenge.md)
</dt> </dl>

 

 





