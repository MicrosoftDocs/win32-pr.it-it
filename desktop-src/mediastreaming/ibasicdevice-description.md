---
title: Metodo di descrizione IBasicDevice
description: Recupera una descrizione del dispositivo.
ms.assetid: 9973AC46-E6BA-4931-BDEB-E64B147AB291
keywords:
- Descrizione metodo API di streaming multimediale
- Descrizione metodo API di streaming multimediale, interfaccia IBasicDevice
- API di streaming multimediale dell'interfaccia IBasicDevice, metodo Description
topic_type:
- apiref
api_name:
- IBasicDevice.Description
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f094246d1424c458e624d4a49358b63a84b9b7d2
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104045614"
---
# <a name="ibasicdevicedescription-method"></a><span data-ttu-id="87c29-106">IBasicDevice::D Metodo Descrizione</span><span class="sxs-lookup"><span data-stu-id="87c29-106">IBasicDevice::Description method</span></span>

<span data-ttu-id="87c29-107">Recupera una descrizione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="87c29-107">Retrieves a description of the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="87c29-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="87c29-108">Syntax</span></span>


```C++
HRESULT Description(
  [out] HSTRING *value
);
```



## <a name="parameters"></a><span data-ttu-id="87c29-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="87c29-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87c29-110">*valore* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="87c29-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="87c29-111">Riceve un puntatore alla descrizione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="87c29-111">Receives a pointer to the description of the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87c29-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="87c29-112">Return value</span></span>

<span data-ttu-id="87c29-113">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="87c29-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="87c29-114">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="87c29-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="87c29-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="87c29-115">Return code</span></span>                                                                          | <span data-ttu-id="87c29-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="87c29-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="87c29-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="87c29-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="87c29-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="87c29-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="87c29-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="87c29-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87c29-120">**IBasicDevice**</span><span class="sxs-lookup"><span data-stu-id="87c29-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





