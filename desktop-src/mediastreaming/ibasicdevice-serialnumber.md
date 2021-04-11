---
title: Metodo IBasicDevice SerialNumber
description: Recupera il numero di serie del dispositivo.
ms.assetid: 238A5999-0E8B-4462-AFCF-790DB58CFCB4
keywords:
- API di streaming multimediale del metodo SerialNumber
- API di streaming multimediale del metodo SerialNumber, interfaccia IBasicDevice
- API di streaming multimediale dell'interfaccia IBasicDevice, metodo SerialNumber
topic_type:
- apiref
api_name:
- IBasicDevice.SerialNumber
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f24fad2e74c3ec2a5b489d8f5dd57265ea6d21bf
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104333943"
---
# <a name="ibasicdeviceserialnumber-method"></a><span data-ttu-id="34eb1-106">Metodo IBasicDevice:: SerialNumber</span><span class="sxs-lookup"><span data-stu-id="34eb1-106">IBasicDevice::SerialNumber method</span></span>

<span data-ttu-id="34eb1-107">Recupera il numero di serie del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="34eb1-107">Retrieves the device s serial number.</span></span>

## <a name="syntax"></a><span data-ttu-id="34eb1-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="34eb1-108">Syntax</span></span>


```C++
HRESULT SerialNumber(
  [out] HSTRING *value
);
```



## <a name="parameters"></a><span data-ttu-id="34eb1-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="34eb1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34eb1-110">*valore* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="34eb1-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="34eb1-111">Riceve un puntatore al numero di serie del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="34eb1-111">Receives a pointer to the device s serial number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34eb1-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="34eb1-112">Return value</span></span>

<span data-ttu-id="34eb1-113">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="34eb1-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="34eb1-114">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="34eb1-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="34eb1-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="34eb1-115">Return code</span></span>                                                                          | <span data-ttu-id="34eb1-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="34eb1-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="34eb1-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="34eb1-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="34eb1-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="34eb1-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="34eb1-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="34eb1-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34eb1-120">**IBasicDevice**</span><span class="sxs-lookup"><span data-stu-id="34eb1-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





