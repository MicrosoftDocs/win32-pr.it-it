---
title: IBasicDevice ModelName (metodo)
description: Recupera il nome del modello del dispositivo.
ms.assetid: 8F871E89-97C1-4788-83AB-B7E0D8D6E0B5
keywords:
- API di streaming multimediale del metodo ModelName
- API di streaming multimediale del metodo ModelName, interfaccia IBasicDevice
- API di streaming multimediale dell'interfaccia IBasicDevice, metodo ModelName
topic_type:
- apiref
api_name:
- IBasicDevice.ModelName
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6e486b372b2108bc85153f416032ef6bfbe8a397
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "106299133"
---
# <a name="ibasicdevicemodelname-method"></a><span data-ttu-id="32252-106">Metodo IBasicDevice:: ModelName</span><span class="sxs-lookup"><span data-stu-id="32252-106">IBasicDevice::ModelName method</span></span>

<span data-ttu-id="32252-107">Recupera il nome del modello del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="32252-107">Retrieves the device s model name.</span></span>

## <a name="syntax"></a><span data-ttu-id="32252-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="32252-108">Syntax</span></span>


```C++
HRESULT ModelName(
  [out] HSTRING *value
);
```



## <a name="parameters"></a><span data-ttu-id="32252-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="32252-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32252-110">*valore* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="32252-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="32252-111">Riceve un puntatore al nome del modello del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="32252-111">Receives a pointer to the device s model name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32252-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="32252-112">Return value</span></span>

<span data-ttu-id="32252-113">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="32252-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="32252-114">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="32252-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="32252-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="32252-115">Return code</span></span>                                                                          | <span data-ttu-id="32252-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="32252-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="32252-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="32252-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="32252-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="32252-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="32252-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="32252-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32252-120">**IBasicDevice**</span><span class="sxs-lookup"><span data-stu-id="32252-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





