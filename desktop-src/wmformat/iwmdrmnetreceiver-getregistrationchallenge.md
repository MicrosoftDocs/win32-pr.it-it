---
title: Metodo IWMDRMNetReceiver GetRegistrationChallenge (wmdrmsdk. h)
description: Il metodo GetRegistrationChallenge genera un messaggio di verifica della registrazione per i dispositivi di rete DRM di Windows Media.
ms.assetid: 7b3641a1-ccc5-4e29-b0e9-808b111f8841
keywords:
- Metodo GetRegistrationChallenge Windows Media Format
- Metodo GetRegistrationChallenge Windows Media Format, interfaccia IWMDRMNetReceiver
- Interfaccia IWMDRMNetReceiver-formato Windows Media, metodo GetRegistrationChallenge
topic_type:
- apiref
api_name:
- IWMDRMNetReceiver.GetRegistrationChallenge
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a292749e95ca6ba2dabc8f3829eae827dbdd8325
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331563"
---
# <a name="iwmdrmnetreceivergetregistrationchallenge-method"></a><span data-ttu-id="d08d9-106">Metodo IWMDRMNetReceiver:: GetRegistrationChallenge</span><span class="sxs-lookup"><span data-stu-id="d08d9-106">IWMDRMNetReceiver::GetRegistrationChallenge method</span></span>

<span data-ttu-id="d08d9-107">Il metodo **GetRegistrationChallenge** genera un messaggio di verifica della registrazione per i dispositivi di rete DRM di Windows Media.</span><span class="sxs-lookup"><span data-stu-id="d08d9-107">The **GetRegistrationChallenge** method generates a Windows Media DRM for Network Devices registration challenge message.</span></span>

## <a name="syntax"></a><span data-ttu-id="d08d9-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d08d9-108">Syntax</span></span>


```C++
HRESULT GetRegistrationChallenge(
  [out] BYTE  **ppbRegistrationChallenge,
  [out] DWORD *pcbRegistrationChallenge
);
```



## <a name="parameters"></a><span data-ttu-id="d08d9-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="d08d9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d08d9-110">*ppbRegistrationChallenge* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d08d9-110">*ppbRegistrationChallenge* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d08d9-111">Indirizzo di un puntatore che riceve l'indirizzo della richiesta generata.</span><span class="sxs-lookup"><span data-stu-id="d08d9-111">Address of a pointer that receives the address of the generated challenge.</span></span> <span data-ttu-id="d08d9-112">Al termine di questi dati, è necessario rilasciare la memoria chiamando **CoTaskMemFree**.</span><span class="sxs-lookup"><span data-stu-id="d08d9-112">When finished with this data, you must release the memory by calling **CoTaskMemFree**.</span></span>

</dd> <dt>

<span data-ttu-id="d08d9-113">*pcbRegistrationChallenge* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d08d9-113">*pcbRegistrationChallenge* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d08d9-114">Indirizzo di una variabile che riceve le dimensioni in byte della richiesta di registrazione.</span><span class="sxs-lookup"><span data-stu-id="d08d9-114">Address of a variable that receives the size of the registration challenge in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d08d9-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d08d9-115">Return value</span></span>

<span data-ttu-id="d08d9-116">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="d08d9-116">The method returns an **HRESULT**.</span></span> <span data-ttu-id="d08d9-117">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="d08d9-117">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="d08d9-118">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="d08d9-118">Return code</span></span>                                                                          | <span data-ttu-id="d08d9-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d08d9-119">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="d08d9-120"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d08d9-120"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="d08d9-121">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="d08d9-121">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d08d9-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="d08d9-122">Remarks</span></span>

<span data-ttu-id="d08d9-123">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="d08d9-123">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="d08d9-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d08d9-124">Requirements</span></span>



| <span data-ttu-id="d08d9-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="d08d9-125">Requirement</span></span> | <span data-ttu-id="d08d9-126">Valore</span><span class="sxs-lookup"><span data-stu-id="d08d9-126">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d08d9-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d08d9-127">Header</span></span><br/> | <dl> <span data-ttu-id="d08d9-128"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="d08d9-128"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d08d9-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d08d9-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d08d9-130">**Interfaccia IWMDRMNetReceiver**</span><span class="sxs-lookup"><span data-stu-id="d08d9-130">**IWMDRMNetReceiver Interface**</span></span>](iwmdrmnetreceiver.md)
</dt> <dt>

[<span data-ttu-id="d08d9-131">**IWMDRMNetReceiver::P rocessRegistrationResponse**</span><span class="sxs-lookup"><span data-stu-id="d08d9-131">**IWMDRMNetReceiver::ProcessRegistrationResponse**</span></span>](iwmdrmnetreceiver-processregistrationresponse.md)
</dt> </dl>

 

 





