---
title: Metodo IBasicDevice DiscoveredOnCurrentNetwork
description: Recupera un valore che indica se il dispositivo si trova nella rete corrente.
ms.assetid: E64D4E49-9790-4647-9A01-2C28C407F238
keywords:
- API di streaming multimediale del metodo DiscoveredOnCurrentNetwork
- API di streaming multimediale del metodo DiscoveredOnCurrentNetwork, interfaccia IBasicDevice
- API di streaming multimediale dell'interfaccia IBasicDevice, metodo DiscoveredOnCurrentNetwork
topic_type:
- apiref
api_name:
- IBasicDevice.DiscoveredOnCurrentNetwork
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6e79a012413b3b3d78a9c4617f01ca6cc01cf7e1
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104397458"
---
# <a name="ibasicdevicediscoveredoncurrentnetwork-method"></a><span data-ttu-id="ca285-106">IBasicDevice::D Metodo iscoveredOnCurrentNetwork</span><span class="sxs-lookup"><span data-stu-id="ca285-106">IBasicDevice::DiscoveredOnCurrentNetwork method</span></span>

<span data-ttu-id="ca285-107">Recupera un valore che indica se il dispositivo si trova nella rete corrente.</span><span class="sxs-lookup"><span data-stu-id="ca285-107">Retrieves a value that indicates if the device is on the current network.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca285-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ca285-108">Syntax</span></span>


```C++
HRESULT DiscoveredOnCurrentNetwork(
  [out] boolean *value
);
```



## <a name="parameters"></a><span data-ttu-id="ca285-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="ca285-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca285-110">*valore* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="ca285-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ca285-111">Riceve un puntatore a un valore booleano che è **true** se il dispositivo si trova nella rete corrente.</span><span class="sxs-lookup"><span data-stu-id="ca285-111">Receives a pointer to a boolean value that is **True** if the device is on the current network.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca285-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ca285-112">Return value</span></span>

<span data-ttu-id="ca285-113">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="ca285-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="ca285-114">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="ca285-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="ca285-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="ca285-115">Return code</span></span>                                                                          | <span data-ttu-id="ca285-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ca285-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="ca285-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ca285-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="ca285-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="ca285-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="ca285-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ca285-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca285-120">**IBasicDevice**</span><span class="sxs-lookup"><span data-stu-id="ca285-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





