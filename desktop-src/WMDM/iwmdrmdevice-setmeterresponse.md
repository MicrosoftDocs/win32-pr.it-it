---
title: Metodo IWMDRMDevice SetMeterResponse
description: Il metodo SetMeterResponse imposta la risposta di misurazione.
ms.assetid: 3f2e7d7c-6470-4d53-96b0-d3eebdb08329
keywords:
- Metodo SetMeterResponse Windows Media Gestione dispositivi
- Metodo SetMeterResponse Windows Media Gestione dispositivi, interfaccia IWMDRMDevice
- Interfaccia IWMDRMDevice Windows Media Gestione dispositivi, metodo SetMeterResponse
topic_type:
- apiref
api_name:
- IWMDRMDevice.SetMeterResponse
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ed70b158215eb831296ad083af8cd2c001cb38f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327395"
---
# <a name="iwmdrmdevicesetmeterresponse-method"></a><span data-ttu-id="3dba9-106">Metodo IWMDRMDevice:: SetMeterResponse</span><span class="sxs-lookup"><span data-stu-id="3dba9-106">IWMDRMDevice::SetMeterResponse method</span></span>

<span data-ttu-id="3dba9-107">Il metodo **SetMeterResponse** imposta la risposta di misurazione.</span><span class="sxs-lookup"><span data-stu-id="3dba9-107">The **SetMeterResponse** method sets the metering response.</span></span>

## <a name="syntax"></a><span data-ttu-id="3dba9-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3dba9-108">Syntax</span></span>


```C++
HRESULT SetMeterResponse(
  [in]  BYTE  *pbMeterResponse,
  [in]  DWORD cbMeterResponse,
  [out] DWORD *pdwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="3dba9-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="3dba9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3dba9-110">*pbMeterResponse* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3dba9-110">*pbMeterResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3dba9-111">Risposta di misurazione da impostare.</span><span class="sxs-lookup"><span data-stu-id="3dba9-111">The metering response to be set.</span></span>

</dd> <dt>

<span data-ttu-id="3dba9-112">*cbMeterResponse* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3dba9-112">*cbMeterResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3dba9-113">Dimensioni in byte della risposta di misurazione.</span><span class="sxs-lookup"><span data-stu-id="3dba9-113">Size of the metering response, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="3dba9-114">*pdwFlags* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="3dba9-114">*pdwFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3dba9-115">Flag di risposta.</span><span class="sxs-lookup"><span data-stu-id="3dba9-115">Response flags.</span></span> <span data-ttu-id="3dba9-116">Questo valore deve essere uno dei flag seguenti.</span><span class="sxs-lookup"><span data-stu-id="3dba9-116">This value must be one of the following flags.</span></span>



| <span data-ttu-id="3dba9-117">Flag</span><span class="sxs-lookup"><span data-stu-id="3dba9-117">Flag</span></span>                            | <span data-ttu-id="3dba9-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3dba9-118">Description</span></span>              |
|---------------------------------|--------------------------|
| <span data-ttu-id="3dba9-119">\_risposta contatore \_ WMDRM \_ tutti</span><span class="sxs-lookup"><span data-stu-id="3dba9-119">WMDRM\_METER\_RESPONSE\_ALL</span></span>     | <span data-ttu-id="3dba9-120">Tutte le risposte del contatore.</span><span class="sxs-lookup"><span data-stu-id="3dba9-120">All meter responses.</span></span>     |
| <span data-ttu-id="3dba9-121">\_risposta contatore \_ WMDRM \_ parziale</span><span class="sxs-lookup"><span data-stu-id="3dba9-121">WMDRM\_METER\_RESPONSE\_PARTIAL</span></span> | <span data-ttu-id="3dba9-122">Risposte parziali del contatore.</span><span class="sxs-lookup"><span data-stu-id="3dba9-122">Partial meter responses.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3dba9-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3dba9-123">Return value</span></span>

<span data-ttu-id="3dba9-124">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="3dba9-124">The method returns an **HRESULT**.</span></span> <span data-ttu-id="3dba9-125">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="3dba9-125">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="3dba9-126">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="3dba9-126">Return code</span></span>                                                                          | <span data-ttu-id="3dba9-127">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3dba9-127">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="3dba9-128"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3dba9-128"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="3dba9-129">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="3dba9-129">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="3dba9-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3dba9-130">Requirements</span></span>



| <span data-ttu-id="3dba9-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="3dba9-131">Requirement</span></span> | <span data-ttu-id="3dba9-132">Valore</span><span class="sxs-lookup"><span data-stu-id="3dba9-132">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3dba9-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3dba9-133">Header</span></span><br/>  | <dl> <span data-ttu-id="3dba9-134"><dt>WMDDRMSP. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3dba9-134"><dt>WMDDRMSP.idl</dt></span></span> </dl> |
| <span data-ttu-id="3dba9-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="3dba9-135">Library</span></span><br/> | <dl> <span data-ttu-id="3dba9-136"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3dba9-136"><dt>Mssachlp.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3dba9-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3dba9-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3dba9-138">**Interfaccia IWMDRMDevice**</span><span class="sxs-lookup"><span data-stu-id="3dba9-138">**IWMDRMDevice Interface**</span></span>](iwmdrmdevice.md)
</dt> </dl>

 

 





