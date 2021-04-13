---
title: IBasicDevice (metodo IpAddresses)
description: Restituisce un vettore di indirizzi IP.
ms.assetid: F48B91DC-3AE2-462F-835B-292BF86904B3
keywords:
- API di streaming multimediale del metodo IpAddresses
- API di streaming multimediale del metodo IpAddresses, interfaccia IBasicDevice
- API di streaming multimediale dell'interfaccia IBasicDevice, metodo IpAddresses
topic_type:
- apiref
api_name:
- IBasicDevice.IpAddresses
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0623b6e2e5d96cb0a400ab1e820424b7eecf46c9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104397626"
---
# <a name="ibasicdeviceipaddresses-method"></a><span data-ttu-id="9bec8-106">Metodo IBasicDevice:: IpAddresses</span><span class="sxs-lookup"><span data-stu-id="9bec8-106">IBasicDevice::IpAddresses method</span></span>

<span data-ttu-id="9bec8-107">Restituisce un vettore di indirizzi IP.</span><span class="sxs-lookup"><span data-stu-id="9bec8-107">Returns a vector of IP addresses.</span></span>

## <a name="syntax"></a><span data-ttu-id="9bec8-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9bec8-108">Syntax</span></span>


```C++
HRESULT IpAddresses(
  [out] IVector< HSTRING > **value
);
```



## <a name="parameters"></a><span data-ttu-id="9bec8-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="9bec8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9bec8-110">*valore* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="9bec8-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9bec8-111">Riceve una raccolta enumerabile di puntatori a indirizzi IP.</span><span class="sxs-lookup"><span data-stu-id="9bec8-111">Receives an enumerable collection of pointers to IP addresses.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9bec8-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9bec8-112">Return value</span></span>

<span data-ttu-id="9bec8-113">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="9bec8-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="9bec8-114">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="9bec8-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="9bec8-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="9bec8-115">Return code</span></span>                                                                          | <span data-ttu-id="9bec8-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9bec8-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="9bec8-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9bec8-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="9bec8-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="9bec8-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="9bec8-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9bec8-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9bec8-120">**IBasicDevice**</span><span class="sxs-lookup"><span data-stu-id="9bec8-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





