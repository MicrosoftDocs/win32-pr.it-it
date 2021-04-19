---
title: Metodo IWMDRMDevice CleanDataStore
description: Il metodo CleanDataStore avvia il processo di pulizia dell'archivio dati DRM sul dispositivo.
ms.assetid: aad99137-6d2b-4612-8014-9783035af929
keywords:
- Metodo CleanDataStore Windows Media Gestione dispositivi
- Metodo CleanDataStore Windows Media Gestione dispositivi, interfaccia IWMDRMDevice
- Interfaccia IWMDRMDevice Windows Media Gestione dispositivi, metodo CleanDataStore
topic_type:
- apiref
api_name:
- IWMDRMDevice.CleanDataStore
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5aed9608a7428245edd84602ea5e7252861d938
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324122"
---
# <a name="iwmdrmdevicecleandatastore-method"></a><span data-ttu-id="14a99-106">Metodo IWMDRMDevice:: CleanDataStore</span><span class="sxs-lookup"><span data-stu-id="14a99-106">IWMDRMDevice::CleanDataStore method</span></span>

<span data-ttu-id="14a99-107">Il metodo **CleanDataStore** avvia il processo di pulizia dell'archivio dati DRM sul dispositivo.</span><span class="sxs-lookup"><span data-stu-id="14a99-107">The **CleanDataStore** method starts the process of cleaning the DRM data store on the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="14a99-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="14a99-108">Syntax</span></span>


```C++
HRESULT CleanDataStore(
  [in] DWORD dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="14a99-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="14a99-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14a99-110">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="14a99-110">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14a99-111">Flag per i criteri di pulizia dell'archivio.</span><span class="sxs-lookup"><span data-stu-id="14a99-111">Flags for store cleaning criteria.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14a99-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="14a99-112">Return value</span></span>

<span data-ttu-id="14a99-113">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="14a99-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="14a99-114">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="14a99-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="14a99-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="14a99-115">Return code</span></span>                                                                          | <span data-ttu-id="14a99-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="14a99-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="14a99-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="14a99-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="14a99-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="14a99-118">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="14a99-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="14a99-119">Requirements</span></span>



| <span data-ttu-id="14a99-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="14a99-120">Requirement</span></span> | <span data-ttu-id="14a99-121">Valore</span><span class="sxs-lookup"><span data-stu-id="14a99-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="14a99-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="14a99-122">Header</span></span><br/>  | <dl> <span data-ttu-id="14a99-123"><dt>WMDDRMSP. idl</dt></span><span class="sxs-lookup"><span data-stu-id="14a99-123"><dt>WMDDRMSP.idl</dt></span></span> </dl> |
| <span data-ttu-id="14a99-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="14a99-124">Library</span></span><br/> | <dl> <span data-ttu-id="14a99-125"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="14a99-125"><dt>Mssachlp.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14a99-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="14a99-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14a99-127">**Interfaccia IWMDRMDevice**</span><span class="sxs-lookup"><span data-stu-id="14a99-127">**IWMDRMDevice Interface**</span></span>](iwmdrmdevice.md)
</dt> </dl>

 

 





