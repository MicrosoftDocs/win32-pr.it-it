---
title: Metodo IWMDRMDevice viene chiamato SetLicenseResponse
description: Il metodo viene chiamato SetLicenseResponse imposta la risposta della licenza.
ms.assetid: 1ef3ba9d-d14c-4a20-92d6-0bcb604fd9e2
keywords:
- Metodo viene chiamato SetLicenseResponse Windows Media Gestione dispositivi
- Metodo viene chiamato SetLicenseResponse Windows Media Gestione dispositivi, interfaccia IWMDRMDevice
- Interfaccia IWMDRMDevice Windows Media Gestione dispositivi, metodo viene chiamato SetLicenseResponse
topic_type:
- apiref
api_name:
- IWMDRMDevice.SetLicenseResponse
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f32a2d27fabe45081b13d658e49171af035b8cc6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327398"
---
# <a name="iwmdrmdevicesetlicenseresponse-method"></a><span data-ttu-id="bd946-106">Metodo IWMDRMDevice:: viene chiamato SetLicenseResponse</span><span class="sxs-lookup"><span data-stu-id="bd946-106">IWMDRMDevice::SetLicenseResponse method</span></span>

<span data-ttu-id="bd946-107">Il metodo **viene chiamato SetLicenseResponse** imposta la risposta della licenza.</span><span class="sxs-lookup"><span data-stu-id="bd946-107">The **SetLicenseResponse** method sets the license response.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd946-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bd946-108">Syntax</span></span>


```C++
HRESULT SetLicenseResponse(
  [in] BYTE  *pbResponse,
  [in] DWORD cbResponse
);
```



## <a name="parameters"></a><span data-ttu-id="bd946-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="bd946-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd946-110">*pbResponse* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bd946-110">*pbResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd946-111">Specifica la risposta da impostare.</span><span class="sxs-lookup"><span data-stu-id="bd946-111">Specifies the response to be set.</span></span>

</dd> <dt>

<span data-ttu-id="bd946-112">*cbResponse* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bd946-112">*cbResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd946-113">Dimensione della risposta in byte.</span><span class="sxs-lookup"><span data-stu-id="bd946-113">Size of the response, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd946-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bd946-114">Return value</span></span>

<span data-ttu-id="bd946-115">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="bd946-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="bd946-116">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="bd946-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="bd946-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="bd946-117">Return code</span></span>                                                                          | <span data-ttu-id="bd946-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bd946-118">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="bd946-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="bd946-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="bd946-120">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="bd946-120">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="bd946-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bd946-121">Requirements</span></span>



| <span data-ttu-id="bd946-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd946-122">Requirement</span></span> | <span data-ttu-id="bd946-123">Valore</span><span class="sxs-lookup"><span data-stu-id="bd946-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bd946-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bd946-124">Header</span></span><br/>  | <dl> <span data-ttu-id="bd946-125"><dt>WMDDRMSP. idl</dt></span><span class="sxs-lookup"><span data-stu-id="bd946-125"><dt>WMDDRMSP.idl</dt></span></span> </dl> |
| <span data-ttu-id="bd946-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="bd946-126">Library</span></span><br/> | <dl> <span data-ttu-id="bd946-127"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bd946-127"><dt>Mssachlp.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd946-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bd946-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd946-129">**Interfaccia IWMDRMDevice**</span><span class="sxs-lookup"><span data-stu-id="bd946-129">**IWMDRMDevice Interface**</span></span>](iwmdrmdevice.md)
</dt> </dl>

 

 





