---
title: Metodo IBasicDevice ModelNumber
description: Recupera il numero di modello del dispositivo.
ms.assetid: C4199135-0C6C-4427-8152-224D7D29C270
keywords:
- API di streaming multimediale del metodo ModelNumber
- API di streaming multimediale del metodo ModelNumber, interfaccia IBasicDevice
- API di streaming multimediale dell'interfaccia IBasicDevice, metodo ModelNumber
topic_type:
- apiref
api_name:
- IBasicDevice.ModelNumber
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8034e67e5f3c552f0af83678d75e33881f1318f4
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103857334"
---
# <a name="ibasicdevicemodelnumber-method"></a><span data-ttu-id="8a29b-106">Metodo IBasicDevice:: ModelNumber</span><span class="sxs-lookup"><span data-stu-id="8a29b-106">IBasicDevice::ModelNumber method</span></span>

<span data-ttu-id="8a29b-107">Recupera il numero di modello del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8a29b-107">Retrieves the device s model number.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a29b-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8a29b-108">Syntax</span></span>


```C++
HRESULT ModelNumber(
  [out] HSTRING *value
);
```



## <a name="parameters"></a><span data-ttu-id="8a29b-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="8a29b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a29b-110">*valore* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="8a29b-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8a29b-111">Riceve un puntatore al numero di modello del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8a29b-111">Receives a pointer to the device s model number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a29b-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8a29b-112">Return value</span></span>

<span data-ttu-id="8a29b-113">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="8a29b-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="8a29b-114">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="8a29b-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="8a29b-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="8a29b-115">Return code</span></span>                                                                          | <span data-ttu-id="8a29b-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8a29b-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="8a29b-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8a29b-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="8a29b-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="8a29b-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="8a29b-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8a29b-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a29b-120">**IBasicDevice**</span><span class="sxs-lookup"><span data-stu-id="8a29b-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





