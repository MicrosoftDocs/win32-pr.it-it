---
title: Metodo IWMDRMNetReceiver ProcessRegistrationResponse (wmdrmsdk. h)
description: Il metodo ProcessRegistrationResponse elabora una risposta di registrazione inviata dal trasmettitore in risposta a una richiesta di registrazione.
ms.assetid: d0260e93-0a5e-494b-a723-bb62206ed55b
keywords:
- Metodo ProcessRegistrationResponse Windows Media Format
- Metodo ProcessRegistrationResponse Windows Media Format, interfaccia IWMDRMNetReceiver
- Interfaccia IWMDRMNetReceiver-formato Windows Media, metodo ProcessRegistrationResponse
topic_type:
- apiref
api_name:
- IWMDRMNetReceiver.ProcessRegistrationResponse
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a77b01f443d57825d82b7cf9556d7585745bb99e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325554"
---
# <a name="iwmdrmnetreceiverprocessregistrationresponse-method"></a><span data-ttu-id="e1ccc-106">IWMDRMNetReceiver::P metodo rocessRegistrationResponse</span><span class="sxs-lookup"><span data-stu-id="e1ccc-106">IWMDRMNetReceiver::ProcessRegistrationResponse method</span></span>

<span data-ttu-id="e1ccc-107">Il metodo **ProcessRegistrationResponse** elabora una risposta di registrazione inviata dal trasmettitore in risposta a una richiesta di registrazione.</span><span class="sxs-lookup"><span data-stu-id="e1ccc-107">The **ProcessRegistrationResponse** method processes a registration response sent by the transmitter in reply to a registration challenge.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1ccc-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e1ccc-108">Syntax</span></span>


```C++
HRESULT ProcessRegistrationResponse(
  [in]  BYTE     *pbRegistrationResponse,
  [in]  DWORD    cbRegistrationResponse,
  [out] IUnknown **ppunkCancellationCookie
);
```



## <a name="parameters"></a><span data-ttu-id="e1ccc-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="e1ccc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1ccc-110">*pbRegistrationResponse* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e1ccc-110">*pbRegistrationResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1ccc-111">Risposta di registrazione ricevuta dal trasmettitore.</span><span class="sxs-lookup"><span data-stu-id="e1ccc-111">Registration response received from the transmitter.</span></span>

</dd> <dt>

<span data-ttu-id="e1ccc-112">*cbRegistrationResponse* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e1ccc-112">*cbRegistrationResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1ccc-113">Dimensioni in byte della risposta di registrazione.</span><span class="sxs-lookup"><span data-stu-id="e1ccc-113">Size of the registration response in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="e1ccc-114">*ppunkCancellationCookie* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="e1ccc-114">*ppunkCancellationCookie* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e1ccc-115">Puntatore che riceve un puntatore all'interfaccia **IUnknown** di un oggetto che identifica la chiamata asincrona.</span><span class="sxs-lookup"><span data-stu-id="e1ccc-115">Pointer that receives a pointer to the **IUnknown** interface of an object that identifies this asynchronous call.</span></span> <span data-ttu-id="e1ccc-116">Questo puntatore di interfaccia può essere utilizzato per annullare la chiamata asincrona chiamando il metodo [**IWMDRMEventGenerator:: CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) .</span><span class="sxs-lookup"><span data-stu-id="e1ccc-116">This interface pointer can be used to cancel the asynchronous call by calling the [**IWMDRMEventGenerator::CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1ccc-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e1ccc-117">Return value</span></span>

<span data-ttu-id="e1ccc-118">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="e1ccc-118">The method returns an **HRESULT**.</span></span> <span data-ttu-id="e1ccc-119">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="e1ccc-119">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="e1ccc-120">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="e1ccc-120">Return code</span></span>                                                                          | <span data-ttu-id="e1ccc-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e1ccc-121">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="e1ccc-122"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e1ccc-122"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="e1ccc-123">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="e1ccc-123">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e1ccc-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="e1ccc-124">Remarks</span></span>

<span data-ttu-id="e1ccc-125">Questo metodo viene eseguito in modo asincrono. al termine dell'elaborazione, l'evento MEProximityCompleted viene inviato all'interfaccia **IMFMediaEventGenerator** .</span><span class="sxs-lookup"><span data-stu-id="e1ccc-125">This method executes asynchronously; when processing is complete, the MEProximityCompleted event is sent to the **IMFMediaEventGenerator** interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1ccc-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e1ccc-126">Requirements</span></span>



| <span data-ttu-id="e1ccc-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1ccc-127">Requirement</span></span> | <span data-ttu-id="e1ccc-128">Valore</span><span class="sxs-lookup"><span data-stu-id="e1ccc-128">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e1ccc-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e1ccc-129">Header</span></span><br/> | <dl> <span data-ttu-id="e1ccc-130"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="e1ccc-130"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1ccc-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e1ccc-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1ccc-132">**Interfaccia IWMDRMNetReceiver**</span><span class="sxs-lookup"><span data-stu-id="e1ccc-132">**IWMDRMNetReceiver Interface**</span></span>](iwmdrmnetreceiver.md)
</dt> <dt>

[<span data-ttu-id="e1ccc-133">**IWMDRMNetReceiver::GetRegistrationChallenge**</span><span class="sxs-lookup"><span data-stu-id="e1ccc-133">**IWMDRMNetReceiver::GetRegistrationChallenge**</span></span>](iwmdrmnetreceiver-getregistrationchallenge.md)
</dt> </dl>

 

 





