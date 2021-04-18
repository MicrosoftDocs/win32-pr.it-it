---
title: Metodo IWMDRMDevice SetSecureClockResponse
description: Il metodo SetSecureClockResponse imposta la risposta di clock protetto.
ms.assetid: 3f0a1487-d8c4-478d-bfb0-8d09931fd4b6
keywords:
- Metodo SetSecureClockResponse Windows Media Gestione dispositivi
- Metodo SetSecureClockResponse Windows Media Gestione dispositivi, interfaccia IWMDRMDevice
- Interfaccia IWMDRMDevice Windows Media Gestione dispositivi, metodo SetSecureClockResponse
topic_type:
- apiref
api_name:
- IWMDRMDevice.SetSecureClockResponse
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 821aceda734aceb7a80774db05465f31213eec47
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324878"
---
# <a name="iwmdrmdevicesetsecureclockresponse-method"></a><span data-ttu-id="82bde-106">Metodo IWMDRMDevice:: SetSecureClockResponse</span><span class="sxs-lookup"><span data-stu-id="82bde-106">IWMDRMDevice::SetSecureClockResponse method</span></span>

<span data-ttu-id="82bde-107">Il metodo **SetSecureClockResponse** imposta la risposta di clock protetto.</span><span class="sxs-lookup"><span data-stu-id="82bde-107">The **SetSecureClockResponse** method sets the secure clock response.</span></span>

## <a name="syntax"></a><span data-ttu-id="82bde-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="82bde-108">Syntax</span></span>


```C++
HRESULT SetSecureClockResponse(
  [in] BYTE  *pbResponse,
  [in] DWORD cbResponse
);
```



## <a name="parameters"></a><span data-ttu-id="82bde-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="82bde-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82bde-110">*pbResponse* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="82bde-110">*pbResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82bde-111">Risposta di clock sicuro da impostare.</span><span class="sxs-lookup"><span data-stu-id="82bde-111">The secure clock response to be set.</span></span>

</dd> <dt>

<span data-ttu-id="82bde-112">*cbResponse* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="82bde-112">*cbResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82bde-113">Dimensione specificata, in byte, della risposta del clock protetto.</span><span class="sxs-lookup"><span data-stu-id="82bde-113">The specified size of the secure clock response, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82bde-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="82bde-114">Return value</span></span>

<span data-ttu-id="82bde-115">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="82bde-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="82bde-116">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="82bde-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="82bde-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="82bde-117">Return code</span></span>                                                                          | <span data-ttu-id="82bde-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="82bde-118">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="82bde-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="82bde-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="82bde-120">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="82bde-120">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="82bde-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="82bde-121">Requirements</span></span>



| <span data-ttu-id="82bde-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="82bde-122">Requirement</span></span> | <span data-ttu-id="82bde-123">Valore</span><span class="sxs-lookup"><span data-stu-id="82bde-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="82bde-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="82bde-124">Header</span></span><br/>  | <dl> <span data-ttu-id="82bde-125"><dt>WMDDRMSP. idl</dt></span><span class="sxs-lookup"><span data-stu-id="82bde-125"><dt>WMDDRMSP.idl</dt></span></span> </dl> |
| <span data-ttu-id="82bde-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="82bde-126">Library</span></span><br/> | <dl> <span data-ttu-id="82bde-127"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="82bde-127"><dt>Mssachlp.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82bde-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="82bde-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82bde-129">**GetSecureClock**</span><span class="sxs-lookup"><span data-stu-id="82bde-129">**GetSecureClock**</span></span>](iwmdrmdevice-getsecureclock.md)
</dt> <dt>

[<span data-ttu-id="82bde-130">**Interfaccia IWMDRMDevice**</span><span class="sxs-lookup"><span data-stu-id="82bde-130">**IWMDRMDevice Interface**</span></span>](iwmdrmdevice.md)
</dt> </dl>

 

 





