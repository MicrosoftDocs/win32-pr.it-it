---
title: Metodo IBasicDevice CanWakeDevices
description: Recupera un valore che indica se il dispositivo può essere riattivato.
ms.assetid: AAD0597C-AD33-40EE-A5DA-27AC66375D38
keywords:
- API di streaming multimediale del metodo CanWakeDevices
- API di streaming multimediale del metodo CanWakeDevices, interfaccia IBasicDevice
- API di streaming multimediale dell'interfaccia IBasicDevice, metodo CanWakeDevices
topic_type:
- apiref
api_name:
- IBasicDevice.CanWakeDevices
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 08a893ac880a426f604f2dc1c73173585e507cc0
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104045808"
---
# <a name="ibasicdevicecanwakedevices-method"></a><span data-ttu-id="33ef9-106">Metodo IBasicDevice:: CanWakeDevices</span><span class="sxs-lookup"><span data-stu-id="33ef9-106">IBasicDevice::CanWakeDevices method</span></span>

<span data-ttu-id="33ef9-107">Recupera un valore che indica se il dispositivo può essere riattivato.</span><span class="sxs-lookup"><span data-stu-id="33ef9-107">Retrieves a value that indicates if the device can wake.</span></span>

## <a name="syntax"></a><span data-ttu-id="33ef9-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="33ef9-108">Syntax</span></span>


```C++
HRESULT CanWakeDevices(
  [out] boolean *value
);
```



## <a name="parameters"></a><span data-ttu-id="33ef9-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="33ef9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33ef9-110">*valore* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="33ef9-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="33ef9-111">Riceve un puntatore a un valore booleano che è **true** se il dispositivo può essere riattivato.</span><span class="sxs-lookup"><span data-stu-id="33ef9-111">Receives a pointer to a boolean value that is **True** if the device can wake.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33ef9-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="33ef9-112">Return value</span></span>

<span data-ttu-id="33ef9-113">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="33ef9-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="33ef9-114">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="33ef9-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="33ef9-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="33ef9-115">Return code</span></span>                                                                          | <span data-ttu-id="33ef9-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="33ef9-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="33ef9-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="33ef9-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="33ef9-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="33ef9-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="33ef9-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="33ef9-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33ef9-120">**IBasicDevice**</span><span class="sxs-lookup"><span data-stu-id="33ef9-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





