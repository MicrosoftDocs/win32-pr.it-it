---
title: Metodo IBasicDevice PhysicalAddresses
description: Restituisce un vettore di indirizzi fisici.
ms.assetid: 85F48EE3-14A1-46DA-A3C3-F94A8A43CF92
keywords:
- API di streaming multimediale del metodo PhysicalAddresses
- API di streaming multimediale del metodo PhysicalAddresses, interfaccia IBasicDevice
- API di streaming multimediale dell'interfaccia IBasicDevice, metodo PhysicalAddresses
topic_type:
- apiref
api_name:
- IBasicDevice.PhysicalAddresses
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2f1cd87435c78e1f6877d1bb6afd1b38981b05dc
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104333892"
---
# <a name="ibasicdevicephysicaladdresses-method"></a><span data-ttu-id="e18ce-106">IBasicDevice::P metodo hysicalAddresses</span><span class="sxs-lookup"><span data-stu-id="e18ce-106">IBasicDevice::PhysicalAddresses method</span></span>

<span data-ttu-id="e18ce-107">Restituisce un vettore di indirizzi fisici.</span><span class="sxs-lookup"><span data-stu-id="e18ce-107">Returns a vector of physical addresses.</span></span>

## <a name="syntax"></a><span data-ttu-id="e18ce-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e18ce-108">Syntax</span></span>


```C++
HRESULT PhysicalAddresses(
  [out] IVector< HSTRING > **value
);
```



## <a name="parameters"></a><span data-ttu-id="e18ce-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="e18ce-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e18ce-110">*valore* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="e18ce-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e18ce-111">Riceve una raccolta enumerabile di puntatori a indirizzi fisici.</span><span class="sxs-lookup"><span data-stu-id="e18ce-111">Receives an enumerable collection of pointers to physical addresses.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e18ce-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e18ce-112">Return value</span></span>

<span data-ttu-id="e18ce-113">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="e18ce-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="e18ce-114">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="e18ce-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="e18ce-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="e18ce-115">Return code</span></span>                                                                          | <span data-ttu-id="e18ce-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e18ce-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="e18ce-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e18ce-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="e18ce-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="e18ce-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="e18ce-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e18ce-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e18ce-120">**IBasicDevice**</span><span class="sxs-lookup"><span data-stu-id="e18ce-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





