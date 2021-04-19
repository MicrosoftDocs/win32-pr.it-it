---
title: Metodo IBasicDevice Manufacturer
description: Recupera il nome del produttore del dispositivo.
ms.assetid: F04400C9-02FC-4CB5-B355-A7E84BECD098
keywords:
- Metodo manufacturname API di streaming multimediale
- Manufacturname metodo API di streaming multimediale, interfaccia IBasicDevice
- API di streaming multimediale dell'interfaccia IBasicDevice, metodo Manufacturname
topic_type:
- apiref
api_name:
- IBasicDevice.ManufacturerName
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 698b4b6c202ed157737b20296976a282c7f97ba3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "106299155"
---
# <a name="ibasicdevicemanufacturername-method"></a><span data-ttu-id="4226b-106">Metodo IBasicDevice:: Manufacturname</span><span class="sxs-lookup"><span data-stu-id="4226b-106">IBasicDevice::ManufacturerName method</span></span>

<span data-ttu-id="4226b-107">Recupera il nome del produttore del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4226b-107">Retrieves the device s manufacturer name.</span></span>

## <a name="syntax"></a><span data-ttu-id="4226b-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4226b-108">Syntax</span></span>


```C++
HRESULT ManufacturerName(
  [out] HSTRING *value
);
```



## <a name="parameters"></a><span data-ttu-id="4226b-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="4226b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4226b-110">*valore* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="4226b-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4226b-111">Riceve un puntatore al nome del produttore del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4226b-111">Receives a pointer to the device s manufacturer name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4226b-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4226b-112">Return value</span></span>

<span data-ttu-id="4226b-113">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="4226b-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="4226b-114">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="4226b-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="4226b-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="4226b-115">Return code</span></span>                                                                          | <span data-ttu-id="4226b-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4226b-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="4226b-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4226b-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="4226b-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="4226b-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="4226b-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4226b-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4226b-120">**IBasicDevice**</span><span class="sxs-lookup"><span data-stu-id="4226b-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





