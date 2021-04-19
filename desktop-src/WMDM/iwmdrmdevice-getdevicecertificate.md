---
title: Metodo IWMDRMDevice GetDeviceCertificate
description: Il metodo GetDeviceCertificate Recupera il certificato del dispositivo.
ms.assetid: 9e345bf9-a158-4c0e-a9f1-e4ce3ec16b58
keywords:
- Metodo GetDeviceCertificate Windows Media Gestione dispositivi
- Metodo GetDeviceCertificate Windows Media Gestione dispositivi, interfaccia IWMDRMDevice
- Interfaccia IWMDRMDevice Windows Media Gestione dispositivi, metodo GetDeviceCertificate
topic_type:
- apiref
api_name:
- IWMDRMDevice.GetDeviceCertificate
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9ceecca32f2455d73ca1dce76a4f8a17613a1ee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324121"
---
# <a name="iwmdrmdevicegetdevicecertificate-method"></a><span data-ttu-id="0dbed-106">Metodo IWMDRMDevice:: GetDeviceCertificate</span><span class="sxs-lookup"><span data-stu-id="0dbed-106">IWMDRMDevice::GetDeviceCertificate method</span></span>

<span data-ttu-id="0dbed-107">Il metodo **GetDeviceCertificate** Recupera il certificato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0dbed-107">The **GetDeviceCertificate** method retrieves the device certificate.</span></span>

## <a name="syntax"></a><span data-ttu-id="0dbed-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0dbed-108">Syntax</span></span>


```C++
HRESULT GetDeviceCertificate(
  [out] BSTR *pbstrDevCert
);
```



## <a name="parameters"></a><span data-ttu-id="0dbed-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="0dbed-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0dbed-110">*pbstrDevCert* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0dbed-110">*pbstrDevCert* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0dbed-111">Puntatore a un **BSTR** che contiene il certificato del dispositivo recuperato.</span><span class="sxs-lookup"><span data-stu-id="0dbed-111">Pointer to a **BSTR** containing the retrieved device certificate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0dbed-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0dbed-112">Return value</span></span>

<span data-ttu-id="0dbed-113">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="0dbed-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="0dbed-114">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="0dbed-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="0dbed-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="0dbed-115">Return code</span></span>                                                                          | <span data-ttu-id="0dbed-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0dbed-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="0dbed-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0dbed-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="0dbed-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="0dbed-118">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="0dbed-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0dbed-119">Requirements</span></span>



| <span data-ttu-id="0dbed-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="0dbed-120">Requirement</span></span> | <span data-ttu-id="0dbed-121">Valore</span><span class="sxs-lookup"><span data-stu-id="0dbed-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0dbed-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0dbed-122">Header</span></span><br/>  | <dl> <span data-ttu-id="0dbed-123"><dt>WMDDRMSP. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0dbed-123"><dt>WMDDRMSP.idl</dt></span></span> </dl> |
| <span data-ttu-id="0dbed-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="0dbed-124">Library</span></span><br/> | <dl> <span data-ttu-id="0dbed-125"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0dbed-125"><dt>Mssachlp.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0dbed-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0dbed-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0dbed-127">**Interfaccia IWMDRMDevice**</span><span class="sxs-lookup"><span data-stu-id="0dbed-127">**IWMDRMDevice Interface**</span></span>](iwmdrmdevice.md)
</dt> </dl>

 

 





