---
title: Metodo IBasicDevice ManufacturerUrl
description: Recupera l'URL del produttore del dispositivo.
ms.assetid: E8372D15-D8B5-49E4-950A-96B4A88B0450
keywords:
- API di streaming multimediale del metodo ManufacturerUrl
- API di streaming multimediale del metodo ManufacturerUrl, interfaccia IBasicDevice
- API di streaming multimediale dell'interfaccia IBasicDevice, metodo ManufacturerUrl
topic_type:
- apiref
api_name:
- IBasicDevice.ManufacturerUrl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7e41ca83c98507c65ead8d1faf2922ee84b45649
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104045680"
---
# <a name="ibasicdevicemanufacturerurl-method"></a><span data-ttu-id="31183-106">Metodo IBasicDevice:: ManufacturerUrl</span><span class="sxs-lookup"><span data-stu-id="31183-106">IBasicDevice::ManufacturerUrl method</span></span>

<span data-ttu-id="31183-107">Recupera l'URL del produttore del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="31183-107">Retrieves the device s manufacturer URL.</span></span>

## <a name="syntax"></a><span data-ttu-id="31183-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="31183-108">Syntax</span></span>


```C++
HRESULT ManufacturerUrl(
  [out] HSTRING *value
);
```



## <a name="parameters"></a><span data-ttu-id="31183-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="31183-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31183-110">*valore* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="31183-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="31183-111">Riceve un puntatore all'URL del produttore del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="31183-111">Receives a pointer to the device s manufacturer URL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31183-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="31183-112">Return value</span></span>

<span data-ttu-id="31183-113">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="31183-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="31183-114">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="31183-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="31183-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="31183-115">Return code</span></span>                                                                          | <span data-ttu-id="31183-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="31183-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="31183-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="31183-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="31183-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="31183-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="31183-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="31183-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31183-120">**IBasicDevice**</span><span class="sxs-lookup"><span data-stu-id="31183-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





