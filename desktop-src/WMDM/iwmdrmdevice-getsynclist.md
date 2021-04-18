---
title: IWMDRMDevice metodo getsyncs
description: Il metodo getsyncname recupera l'elenco di sincronizzazione delle licenze nel dispositivo. La sincronizzazione delle licenze consente al computer host di trasferire le licenze aggiornate a un dispositivo in base ai criteri specificati.
ms.assetid: 772ac03b-3339-4c5f-a8fc-1c216ec665b7
keywords:
- Metodo getsyncname Windows Media Gestione dispositivi
- Metodo getsyncname Windows Media Gestione dispositivi, interfaccia IWMDRMDevice
- Interfaccia IWMDRMDevice Windows Media Gestione dispositivi, metodo getsyncname
topic_type:
- apiref
api_name:
- IWMDRMDevice.GetSyncList
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 381d410bd938cb90855b182e62354d48e72f16d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327402"
---
# <a name="iwmdrmdevicegetsynclist-method"></a><span data-ttu-id="5bfcd-107">Metodo IWMDRMDevice:: getsyncname</span><span class="sxs-lookup"><span data-stu-id="5bfcd-107">IWMDRMDevice::GetSyncList method</span></span>

<span data-ttu-id="5bfcd-108">Il metodo **Getsyncname** recupera l'elenco di sincronizzazione delle licenze nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5bfcd-108">The **GetSyncList** method retrieves the license synchronization list on the device.</span></span> <span data-ttu-id="5bfcd-109">La sincronizzazione delle licenze consente al computer host di trasferire le licenze aggiornate a un dispositivo in base ai criteri specificati.</span><span class="sxs-lookup"><span data-stu-id="5bfcd-109">License synchronization allows the host computer to transfer updated licenses to a device according to the specified criteria.</span></span>

## <a name="syntax"></a><span data-ttu-id="5bfcd-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5bfcd-110">Syntax</span></span>


```C++
HRESULT GetSyncList(
  [in]  DWORD cMinCountThreshold,
  [in]  DWORD cMinHoursThreshold,
  [out] BYTE  **ppbSyncList,
  [out] DWORD *pcbSyncList
);
```



## <a name="parameters"></a><span data-ttu-id="5bfcd-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="5bfcd-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5bfcd-112">*cMinCountThreshold* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5bfcd-112">*cMinCountThreshold* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5bfcd-113">Soglia numero minimo.</span><span class="sxs-lookup"><span data-stu-id="5bfcd-113">Minimum count threshold.</span></span>

</dd> <dt>

<span data-ttu-id="5bfcd-114">*cMinHoursThreshold* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5bfcd-114">*cMinHoursThreshold* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5bfcd-115">Soglia ore minime.</span><span class="sxs-lookup"><span data-stu-id="5bfcd-115">Minimum hours threshold.</span></span>

</dd> <dt>

<span data-ttu-id="5bfcd-116">*ppbSyncList* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="5bfcd-116">*ppbSyncList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5bfcd-117">Elenco di sincronizzazione delle licenze recuperato.</span><span class="sxs-lookup"><span data-stu-id="5bfcd-117">Retrieved license synchronization list.</span></span>

</dd> <dt>

<span data-ttu-id="5bfcd-118">*pcbSyncList* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="5bfcd-118">*pcbSyncList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5bfcd-119">Dimensioni in byte dell'elenco di sincronizzazione delle licenze.</span><span class="sxs-lookup"><span data-stu-id="5bfcd-119">Size of the license synchronization list, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5bfcd-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5bfcd-120">Return value</span></span>

<span data-ttu-id="5bfcd-121">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="5bfcd-121">The method returns an **HRESULT**.</span></span> <span data-ttu-id="5bfcd-122">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="5bfcd-122">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="5bfcd-123">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="5bfcd-123">Return code</span></span>                                                                          | <span data-ttu-id="5bfcd-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5bfcd-124">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="5bfcd-125"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5bfcd-125"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="5bfcd-126">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="5bfcd-126">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="5bfcd-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5bfcd-127">Requirements</span></span>



| <span data-ttu-id="5bfcd-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="5bfcd-128">Requirement</span></span> | <span data-ttu-id="5bfcd-129">Valore</span><span class="sxs-lookup"><span data-stu-id="5bfcd-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5bfcd-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5bfcd-130">Header</span></span><br/>  | <dl> <span data-ttu-id="5bfcd-131"><dt>WMDDRMSP. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5bfcd-131"><dt>WMDDRMSP.idl</dt></span></span> </dl> |
| <span data-ttu-id="5bfcd-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="5bfcd-132">Library</span></span><br/> | <dl> <span data-ttu-id="5bfcd-133"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5bfcd-133"><dt>Mssachlp.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5bfcd-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5bfcd-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5bfcd-135">**Interfaccia IWMDRMDevice**</span><span class="sxs-lookup"><span data-stu-id="5bfcd-135">**IWMDRMDevice Interface**</span></span>](iwmdrmdevice.md)
</dt> </dl>

 

 





