---
title: Metodo IWMDRMDevice IsWMDRMDevice
description: Il metodo IsWMDRMDevice determina se il dispositivo supporta Windows Media DRM 10 per i dispositivi portatili.
ms.assetid: 247e7a77-e805-4848-893f-f5522c161232
keywords:
- Metodo IsWMDRMDevice Windows Media Gestione dispositivi
- Metodo IsWMDRMDevice Windows Media Gestione dispositivi, interfaccia IWMDRMDevice
- Interfaccia IWMDRMDevice Windows Media Gestione dispositivi, metodo IsWMDRMDevice
topic_type:
- apiref
api_name:
- IWMDRMDevice.IsWMDRMDevice
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca9cb79598ea41a996748e383c8fdfc63364dd6c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327401"
---
# <a name="iwmdrmdeviceiswmdrmdevice-method"></a><span data-ttu-id="0fc3a-106">Metodo IWMDRMDevice:: IsWMDRMDevice</span><span class="sxs-lookup"><span data-stu-id="0fc3a-106">IWMDRMDevice::IsWMDRMDevice method</span></span>

<span data-ttu-id="0fc3a-107">Il metodo **IsWMDRMDevice** determina se il dispositivo supporta Windows Media DRM 10 per i dispositivi portatili.</span><span class="sxs-lookup"><span data-stu-id="0fc3a-107">The **IsWMDRMDevice** method determines whether the device supports Windows Media DRM 10 for Portable Devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="0fc3a-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0fc3a-108">Syntax</span></span>


```C++
HRESULT IsWMDRMDevice(
  [out] DWORD *pdwVersion
);
```



## <a name="parameters"></a><span data-ttu-id="0fc3a-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="0fc3a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0fc3a-110">*pdwVersion* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0fc3a-110">*pdwVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0fc3a-111">Versione di Windows Media DRM 10 per dispositivi portatili, il cui valore è 0x00010000.</span><span class="sxs-lookup"><span data-stu-id="0fc3a-111">Version of Windows Media DRM 10 for Portable Devices, which has value of 0x00010000.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0fc3a-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0fc3a-112">Return value</span></span>

<span data-ttu-id="0fc3a-113">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="0fc3a-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="0fc3a-114">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="0fc3a-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="0fc3a-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="0fc3a-115">Return code</span></span>                                                                          | <span data-ttu-id="0fc3a-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0fc3a-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="0fc3a-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0fc3a-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="0fc3a-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="0fc3a-118">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="0fc3a-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0fc3a-119">Requirements</span></span>



| <span data-ttu-id="0fc3a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="0fc3a-120">Requirement</span></span> | <span data-ttu-id="0fc3a-121">Valore</span><span class="sxs-lookup"><span data-stu-id="0fc3a-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0fc3a-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0fc3a-122">Header</span></span><br/>  | <dl> <span data-ttu-id="0fc3a-123"><dt>WMDDRMSP. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0fc3a-123"><dt>WMDDRMSP.idl</dt></span></span> </dl> |
| <span data-ttu-id="0fc3a-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="0fc3a-124">Library</span></span><br/> | <dl> <span data-ttu-id="0fc3a-125"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0fc3a-125"><dt>Mssachlp.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0fc3a-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0fc3a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fc3a-127">**Interfaccia IWMDRMDevice**</span><span class="sxs-lookup"><span data-stu-id="0fc3a-127">**IWMDRMDevice Interface**</span></span>](iwmdrmdevice.md)
</dt> </dl>

 

 





