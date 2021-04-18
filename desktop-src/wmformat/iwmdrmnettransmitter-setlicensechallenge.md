---
title: Metodo IWMDRMNetTransmitter SetLicenseChallenge (wmdrmsdk. h)
description: Il metodo SetLicenseChallenge elabora una richiesta di licenza inviata da un DRM di Windows Media per i dispositivi di rete Receiver.
ms.assetid: 3d4cd029-a8f5-49fc-ba8c-d8615ff94366
keywords:
- Metodo SetLicenseChallenge Windows Media Format
- Metodo SetLicenseChallenge Windows Media Format, interfaccia IWMDRMNetTransmitter
- Interfaccia IWMDRMNetTransmitter-formato Windows Media, metodo SetLicenseChallenge
topic_type:
- apiref
api_name:
- IWMDRMNetTransmitter.SetLicenseChallenge
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94b83ca615896039a592d147fe8c14d15493cec0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325551"
---
# <a name="iwmdrmnettransmittersetlicensechallenge-method"></a><span data-ttu-id="f0c72-106">Metodo IWMDRMNetTransmitter:: SetLicenseChallenge</span><span class="sxs-lookup"><span data-stu-id="f0c72-106">IWMDRMNetTransmitter::SetLicenseChallenge method</span></span>

<span data-ttu-id="f0c72-107">Il metodo **SetLicenseChallenge** elabora una richiesta di licenza inviata da un DRM di Windows Media per i dispositivi di rete Receiver.</span><span class="sxs-lookup"><span data-stu-id="f0c72-107">The **SetLicenseChallenge** method processes a license challenge sent by a Windows Media DRM for Network Devices receiver.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0c72-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f0c72-108">Syntax</span></span>


```C++
HRESULT SetLicenseChallenge(
  [in] BYTE  *pbLicenseChallenge,
  [in] DWORD cbLicenseChallenge
);
```



## <a name="parameters"></a><span data-ttu-id="f0c72-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="f0c72-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0c72-110">*pbLicenseChallenge* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f0c72-110">*pbLicenseChallenge* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0c72-111">Puntatore ai dati di richiesta della licenza inviati da un ricevitore.</span><span class="sxs-lookup"><span data-stu-id="f0c72-111">Pointer to the license challenge data that was sent by a receiver.</span></span>

</dd> <dt>

<span data-ttu-id="f0c72-112">*cbLicenseChallenge* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f0c72-112">*cbLicenseChallenge* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0c72-113">Dimensioni in byte della richiesta di verifica delle licenze.</span><span class="sxs-lookup"><span data-stu-id="f0c72-113">Size of license challenge in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0c72-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f0c72-114">Return value</span></span>

<span data-ttu-id="f0c72-115">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="f0c72-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="f0c72-116">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="f0c72-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="f0c72-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="f0c72-117">Return code</span></span>                                                                          | <span data-ttu-id="f0c72-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f0c72-118">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="f0c72-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f0c72-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="f0c72-120">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="f0c72-120">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f0c72-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="f0c72-121">Remarks</span></span>

<span data-ttu-id="f0c72-122">Se questo metodo ha esito positivo, le chiamate successive agli altri metodi di **IWMDRMNetTransmitter** utilizzeranno le informazioni nella richiesta elaborata.</span><span class="sxs-lookup"><span data-stu-id="f0c72-122">If this method succeeds, subsequent calls to the other methods of **IWMDRMNetTransmitter** will use the information in the processed challenge.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0c72-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f0c72-123">Requirements</span></span>



| <span data-ttu-id="f0c72-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0c72-124">Requirement</span></span> | <span data-ttu-id="f0c72-125">Valore</span><span class="sxs-lookup"><span data-stu-id="f0c72-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f0c72-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f0c72-126">Header</span></span><br/> | <dl> <span data-ttu-id="f0c72-127"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0c72-127"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0c72-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f0c72-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0c72-129">**Interfaccia IWMDRMNetTransmitter**</span><span class="sxs-lookup"><span data-stu-id="f0c72-129">**IWMDRMNetTransmitter Interface**</span></span>](iwmdrmnettransmitter.md)
</dt> </dl>

 

 





