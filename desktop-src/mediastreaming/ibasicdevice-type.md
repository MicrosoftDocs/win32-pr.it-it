---
title: Metodo di tipo IBasicDevice
description: Recupera un valore di enumerazione che indica il tipo di dispositivo del dispositivo DLNA.
ms.assetid: D9FB3A02-7796-4ACB-B7D3-D171D1D9B77F
keywords:
- Metodo di tipo API di streaming multimediale
- Metodo di tipo API di streaming multimediale, interfaccia IBasicDevice
- API di streaming multimediale dell'interfaccia IBasicDevice, metodo Type
topic_type:
- apiref
api_name:
- IBasicDevice.Type
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a69f0671c82363ff61179c0120b3db8f6e755de9
ms.sourcegitcommit: 89f99926f946dc6c5ea600fb7c41f6b19ceac516
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/21/2020
ms.locfileid: "104399907"
---
# <a name="ibasicdevicetype-method"></a><span data-ttu-id="e7684-106">Metodo IBasicDevice:: Type</span><span class="sxs-lookup"><span data-stu-id="e7684-106">IBasicDevice::Type method</span></span>

<span data-ttu-id="e7684-107">Recupera un valore di enumerazione che indica il tipo di dispositivo del dispositivo DLNA.</span><span class="sxs-lookup"><span data-stu-id="e7684-107">Retrieves an enumeration value indicating the device type of the DLNA device.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7684-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e7684-108">Syntax</span></span>


```C++
HRESULT Type(
  [out] DeviceTypes *value
);
```



## <a name="parameters"></a><span data-ttu-id="e7684-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="e7684-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7684-110">*valore* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="e7684-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e7684-111">Riceve un puntatore a un valore [**DeviceTypes**](devicetypes.md) .</span><span class="sxs-lookup"><span data-stu-id="e7684-111">Receives a pointer to a [**DeviceTypes**](devicetypes.md) value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7684-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e7684-112">Return value</span></span>

<span data-ttu-id="e7684-113">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="e7684-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="e7684-114">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="e7684-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="e7684-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="e7684-115">Return code</span></span>                                                                          | <span data-ttu-id="e7684-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e7684-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="e7684-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e7684-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="e7684-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="e7684-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="e7684-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e7684-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7684-120">**IBasicDevice**</span><span class="sxs-lookup"><span data-stu-id="e7684-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





