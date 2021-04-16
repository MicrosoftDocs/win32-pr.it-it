---
title: Metodo IBasicDevice RemoteStreamingUrls
description: Restituisce un vettore di URL di streaming remoto.
ms.assetid: 19B4475F-A7E4-4DC4-9C88-68D91D023AF4
keywords:
- API di streaming multimediale del metodo RemoteStreamingUrls
- API di streaming multimediale del metodo RemoteStreamingUrls, interfaccia IBasicDevice
- API di streaming multimediale dell'interfaccia IBasicDevice, metodo RemoteStreamingUrls
topic_type:
- apiref
api_name:
- IBasicDevice.RemoteStreamingUrls
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fdc4bd363096e7b808a51cfbddb764daabe03a55
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104397603"
---
# <a name="ibasicdeviceremotestreamingurls-method"></a><span data-ttu-id="4dac3-106">Metodo IBasicDevice:: RemoteStreamingUrls</span><span class="sxs-lookup"><span data-stu-id="4dac3-106">IBasicDevice::RemoteStreamingUrls method</span></span>

<span data-ttu-id="4dac3-107">Restituisce un vettore di URL di streaming remoto.</span><span class="sxs-lookup"><span data-stu-id="4dac3-107">Returns a vector of remote streaming URLs.</span></span>

## <a name="syntax"></a><span data-ttu-id="4dac3-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4dac3-108">Syntax</span></span>


```C++
HRESULT RemoteStreamingUrls(
  [out] IVector< HSTRING > **value
);
```



## <a name="parameters"></a><span data-ttu-id="4dac3-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="4dac3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4dac3-110">*valore* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="4dac3-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4dac3-111">Riceve una raccolta enumerabile di puntatori agli URL di streaming remoto.</span><span class="sxs-lookup"><span data-stu-id="4dac3-111">Receives an enumerable collection of pointers to remote streaming URLs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4dac3-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4dac3-112">Return value</span></span>

<span data-ttu-id="4dac3-113">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="4dac3-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="4dac3-114">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="4dac3-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="4dac3-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="4dac3-115">Return code</span></span>                                                                          | <span data-ttu-id="4dac3-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4dac3-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="4dac3-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4dac3-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="4dac3-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="4dac3-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="4dac3-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4dac3-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4dac3-120">**IBasicDevice**</span><span class="sxs-lookup"><span data-stu-id="4dac3-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





