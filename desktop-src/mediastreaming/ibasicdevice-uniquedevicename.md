---
title: Metodo IBasicDevice UniqueDeviceName
description: Recupera il nome del dispositivo univoco del dispositivo (UDN).
ms.assetid: 393EFF96-69E1-4081-905D-D8CC47B5FC4A
keywords:
- API di streaming multimediale del metodo UniqueDeviceName
- API di streaming multimediale del metodo UniqueDeviceName, interfaccia IBasicDevice
- API di streaming multimediale dell'interfaccia IBasicDevice, metodo UniqueDeviceName
topic_type:
- apiref
api_name:
- IBasicDevice.UniqueDeviceName
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4b3103640fd49880dc5ae5ca881618ac1091de62
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104397578"
---
# <a name="ibasicdeviceuniquedevicename-method"></a><span data-ttu-id="ebbfd-106">Metodo IBasicDevice:: UniqueDeviceName</span><span class="sxs-lookup"><span data-stu-id="ebbfd-106">IBasicDevice::UniqueDeviceName method</span></span>

<span data-ttu-id="ebbfd-107">Recupera il nome del dispositivo univoco del dispositivo (UDN).</span><span class="sxs-lookup"><span data-stu-id="ebbfd-107">Retrieves the device s unique device name (UDN).</span></span>

## <a name="syntax"></a><span data-ttu-id="ebbfd-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ebbfd-108">Syntax</span></span>


```C++
HRESULT UniqueDeviceName(
  [out] HSTRING *value
);
```



## <a name="parameters"></a><span data-ttu-id="ebbfd-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="ebbfd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ebbfd-110">*valore* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="ebbfd-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ebbfd-111">Riceve un puntatore al modello del dispositivo UDN.</span><span class="sxs-lookup"><span data-stu-id="ebbfd-111">Receives a pointer to the device s model UDN.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ebbfd-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ebbfd-112">Return value</span></span>

<span data-ttu-id="ebbfd-113">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="ebbfd-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="ebbfd-114">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="ebbfd-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="ebbfd-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="ebbfd-115">Return code</span></span>                                                                          | <span data-ttu-id="ebbfd-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ebbfd-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="ebbfd-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ebbfd-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="ebbfd-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="ebbfd-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="ebbfd-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ebbfd-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebbfd-120">**IBasicDevice**</span><span class="sxs-lookup"><span data-stu-id="ebbfd-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





