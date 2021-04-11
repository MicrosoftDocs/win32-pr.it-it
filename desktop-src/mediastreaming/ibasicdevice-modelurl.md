---
title: Metodo IBasicDevice ModelUrl
description: Recupera l'URL del modello del dispositivo.
ms.assetid: 093D306B-5DFC-4A68-803D-3DDE195A8B85
keywords:
- API di streaming multimediale del metodo ModelUrl
- API di streaming multimediale del metodo ModelUrl, interfaccia IBasicDevice
- API di streaming multimediale dell'interfaccia IBasicDevice, metodo ModelUrl
topic_type:
- apiref
api_name:
- IBasicDevice.ModelUrl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4f616d1a122f5fe6025c80742df61eb86d41514a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104333895"
---
# <a name="ibasicdevicemodelurl-method"></a><span data-ttu-id="9c0b8-106">Metodo IBasicDevice:: ModelUrl</span><span class="sxs-lookup"><span data-stu-id="9c0b8-106">IBasicDevice::ModelUrl method</span></span>

<span data-ttu-id="9c0b8-107">Recupera l'URL del modello del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9c0b8-107">Retrieves the device s model URL.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c0b8-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9c0b8-108">Syntax</span></span>


```C++
HRESULT ModelUrl(
  [out] HSTRING *value
);
```



## <a name="parameters"></a><span data-ttu-id="9c0b8-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="9c0b8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c0b8-110">*valore* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="9c0b8-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9c0b8-111">Riceve un puntatore all'URL del modello del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9c0b8-111">Receives a pointer to the device s model URL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c0b8-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9c0b8-112">Return value</span></span>

<span data-ttu-id="9c0b8-113">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="9c0b8-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="9c0b8-114">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="9c0b8-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="9c0b8-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="9c0b8-115">Return code</span></span>                                                                          | <span data-ttu-id="9c0b8-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9c0b8-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="9c0b8-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9c0b8-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="9c0b8-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="9c0b8-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="9c0b8-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9c0b8-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c0b8-120">**IBasicDevice**</span><span class="sxs-lookup"><span data-stu-id="9c0b8-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





