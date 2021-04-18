---
title: Metodo IWMDRMNetReceiver GetLicenseChallenge (wmdrmsdk. h)
description: Il metodo GetLicenseChallenge genera una richiesta di licenza di Windows Media DRM per i dispositivi di rete che può essere inviata a un trasmettitore quando richiede contenuto protetto.
ms.assetid: c13b9e9e-b076-411b-a106-b602544faaba
keywords:
- Metodo GetLicenseChallenge Windows Media Format
- Metodo GetLicenseChallenge Windows Media Format, interfaccia IWMDRMNetReceiver
- Interfaccia IWMDRMNetReceiver-formato Windows Media, metodo GetLicenseChallenge
topic_type:
- apiref
api_name:
- IWMDRMNetReceiver.GetLicenseChallenge
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61f58b85b8dc5edd6c23e809dda8c18bf30137f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325556"
---
# <a name="iwmdrmnetreceivergetlicensechallenge-method"></a><span data-ttu-id="d090f-106">Metodo IWMDRMNetReceiver:: GetLicenseChallenge</span><span class="sxs-lookup"><span data-stu-id="d090f-106">IWMDRMNetReceiver::GetLicenseChallenge method</span></span>

<span data-ttu-id="d090f-107">Il metodo **GetLicenseChallenge** genera una richiesta di licenza di Windows Media DRM per i dispositivi di rete che può essere inviata a un trasmettitore quando richiede contenuto protetto.</span><span class="sxs-lookup"><span data-stu-id="d090f-107">The **GetLicenseChallenge** method generates a Windows Media DRM for Network Devices license challenge that can be sent to a transmitter when requesting protected content.</span></span>

## <a name="syntax"></a><span data-ttu-id="d090f-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d090f-108">Syntax</span></span>


```C++
HRESULT GetLicenseChallenge(
  [in]  BSTR  bstrAction,
  [out] BYTE  **ppbLicenseChallenge,
  [out] DWORD *pcbLicenseChallenge
);
```



## <a name="parameters"></a><span data-ttu-id="d090f-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="d090f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d090f-110">*bstrAction* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d090f-110">*bstrAction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d090f-111">Azione per la quale generare la richiesta di verifica.</span><span class="sxs-lookup"><span data-stu-id="d090f-111">Action for which to generate the challenge.</span></span>

</dd> <dt>

<span data-ttu-id="d090f-112">*ppbLicenseChallenge* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d090f-112">*ppbLicenseChallenge* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d090f-113">Indirizzo di un puntatore impostato sull'indirizzo della richiesta generata.</span><span class="sxs-lookup"><span data-stu-id="d090f-113">Address of a pointer that is set to the address of the generated challenge.</span></span> <span data-ttu-id="d090f-114">Al termine di questi dati, è necessario rilasciare la memoria chiamando **CoTaskMemFree**.</span><span class="sxs-lookup"><span data-stu-id="d090f-114">When finished with this data, you must release the memory by calling **CoTaskMemFree**.</span></span>

</dd> <dt>

<span data-ttu-id="d090f-115">*pcbLicenseChallenge* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d090f-115">*pcbLicenseChallenge* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d090f-116">Indirizzo di una variabile che riceve le dimensioni della richiesta di licenza in byte.</span><span class="sxs-lookup"><span data-stu-id="d090f-116">Address of a variable that receives the size of the license challenge in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d090f-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d090f-117">Return value</span></span>

<span data-ttu-id="d090f-118">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="d090f-118">The method returns an **HRESULT**.</span></span> <span data-ttu-id="d090f-119">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="d090f-119">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="d090f-120">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="d090f-120">Return code</span></span>                                                                          | <span data-ttu-id="d090f-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d090f-121">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="d090f-122"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d090f-122"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="d090f-123">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="d090f-123">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d090f-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="d090f-124">Remarks</span></span>

<span data-ttu-id="d090f-125">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="d090f-125">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="d090f-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d090f-126">Requirements</span></span>



| <span data-ttu-id="d090f-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="d090f-127">Requirement</span></span> | <span data-ttu-id="d090f-128">Valore</span><span class="sxs-lookup"><span data-stu-id="d090f-128">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d090f-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d090f-129">Header</span></span><br/> | <dl> <span data-ttu-id="d090f-130"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="d090f-130"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d090f-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d090f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d090f-132">**Interfaccia IWMDRMNetReceiver**</span><span class="sxs-lookup"><span data-stu-id="d090f-132">**IWMDRMNetReceiver Interface**</span></span>](iwmdrmnetreceiver.md)
</dt> <dt>

[<span data-ttu-id="d090f-133">**IWMDRMNetReceiver::P rocessLicenseResponse**</span><span class="sxs-lookup"><span data-stu-id="d090f-133">**IWMDRMNetReceiver::ProcessLicenseResponse**</span></span>](iwmdrmnetreceiver-processlicenseresponse.md)
</dt> </dl>

 

 





