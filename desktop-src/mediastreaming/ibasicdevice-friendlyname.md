---
title: Metodo IBasicDevice FriendlyName
description: Recupera il nome descrittivo del dispositivo.
ms.assetid: 693806E1-CA66-457D-A25B-D79064776965
keywords:
- API di streaming multimediale del metodo FriendlyName
- API di streaming multimediale del metodo FriendlyName, interfaccia IBasicDevice
- API di streaming multimediale dell'interfaccia IBasicDevice, metodo FriendlyName
topic_type:
- apiref
api_name:
- IBasicDevice.FriendlyName
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ec2b2edfa3a98dfdbbdd1d236acb6e1f1433f141
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718565"
---
# <a name="ibasicdevicefriendlyname-method"></a><span data-ttu-id="755b4-106">Metodo IBasicDevice:: FriendlyName</span><span class="sxs-lookup"><span data-stu-id="755b4-106">IBasicDevice::FriendlyName method</span></span>

<span data-ttu-id="755b4-107">Recupera il nome descrittivo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="755b4-107">Retrieves the device s friendly name.</span></span>

## <a name="syntax"></a><span data-ttu-id="755b4-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="755b4-108">Syntax</span></span>


```C++
HRESULT FriendlyName(
  [out] HSTRING *value
);
```



## <a name="parameters"></a><span data-ttu-id="755b4-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="755b4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="755b4-110">*valore* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="755b4-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="755b4-111">Riceve un puntatore al nome descrittivo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="755b4-111">Receives a pointer to the device s friendly name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="755b4-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="755b4-112">Return value</span></span>

<span data-ttu-id="755b4-113">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="755b4-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="755b4-114">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="755b4-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="755b4-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="755b4-115">Return code</span></span>                                                                          | <span data-ttu-id="755b4-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="755b4-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="755b4-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="755b4-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="755b4-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="755b4-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="755b4-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="755b4-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="755b4-120">**IBasicDevice**</span><span class="sxs-lookup"><span data-stu-id="755b4-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





