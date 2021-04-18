---
title: Metodo IWMDRMDevice2 GetPartialSyncList
description: Il metodo GetPartialSyncList ottiene un elenco di sincronizzazione parziale.
ms.assetid: 4ee8e9d7-d5d1-4614-b7a1-1dcb7f07b161
keywords:
- Metodo GetPartialSyncList Windows Media Gestione dispositivi
- Metodo GetPartialSyncList Windows Media Gestione dispositivi, interfaccia IWMDRMDevice2
- Interfaccia IWMDRMDevice2 Windows Media Gestione dispositivi, metodo GetPartialSyncList
topic_type:
- apiref
api_name:
- IWMDRMDevice2.GetPartialSyncList
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c68c9c9a0bc47dcbea25158bb1f25db6cd084075
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332153"
---
# <a name="iwmdrmdevice2getpartialsynclist-method"></a><span data-ttu-id="6c028-106">Metodo IWMDRMDevice2:: GetPartialSyncList</span><span class="sxs-lookup"><span data-stu-id="6c028-106">IWMDRMDevice2::GetPartialSyncList method</span></span>

<span data-ttu-id="6c028-107">Il metodo **GetPartialSyncList** ottiene un elenco di sincronizzazione parziale.</span><span class="sxs-lookup"><span data-stu-id="6c028-107">The **GetPartialSyncList** method gets a partial synchronization list.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c028-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6c028-108">Syntax</span></span>


```C++
HRESULT GetPartialSyncList(
  [in]  DWORD cMinCountThreshold,
  [in]  DWORD cMinHoursThreshold,
  [in]  DWORD dwStartingIndex,
  [in]  DWORD cItems,
  [out] BYTE  **ppbSyncList,
  [out] DWORD *pcbSyncList,
  [out] DWORD *pdwNextStartingIndex,
  [out] DWORD *pcItemsProcessed
);
```



## <a name="parameters"></a><span data-ttu-id="6c028-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="6c028-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c028-110">*cMinCountThreshold* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6c028-110">*cMinCountThreshold* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c028-111">Soglia numero minimo.</span><span class="sxs-lookup"><span data-stu-id="6c028-111">Minimum count threshold.</span></span>

</dd> <dt>

<span data-ttu-id="6c028-112">*cMinHoursThreshold* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6c028-112">*cMinHoursThreshold* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c028-113">Soglia ore minime.</span><span class="sxs-lookup"><span data-stu-id="6c028-113">Minimum hours threshold.</span></span>

</dd> <dt>

<span data-ttu-id="6c028-114">*dwStartingIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6c028-114">*dwStartingIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c028-115">Posizione iniziale per l'indicizzazione.</span><span class="sxs-lookup"><span data-stu-id="6c028-115">Start position for indexing.</span></span>

</dd> <dt>

<span data-ttu-id="6c028-116">*cItems* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6c028-116">*cItems* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c028-117">Numero di elementi da indicizzare.</span><span class="sxs-lookup"><span data-stu-id="6c028-117">Count of items to be indexed.</span></span>

</dd> <dt>

<span data-ttu-id="6c028-118">*ppbSyncList* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="6c028-118">*ppbSyncList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6c028-119">Elenco di sincronizzazione delle licenze recuperato.</span><span class="sxs-lookup"><span data-stu-id="6c028-119">Retrieved license synchronization list.</span></span>

</dd> <dt>

<span data-ttu-id="6c028-120">*pcbSyncList* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="6c028-120">*pcbSyncList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6c028-121">Dimensioni in byte dell'elenco di sincronizzazione delle licenze.</span><span class="sxs-lookup"><span data-stu-id="6c028-121">Size of the license synchronization list, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="6c028-122">*pdwNextStartingIndex* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="6c028-122">*pdwNextStartingIndex* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6c028-123">Posizione iniziale successiva per l'indicizzazione.</span><span class="sxs-lookup"><span data-stu-id="6c028-123">Next start position for indexing.</span></span>

</dd> <dt>

<span data-ttu-id="6c028-124">*pcItemsProcessed* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="6c028-124">*pcItemsProcessed* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6c028-125">Numero di elementi in fase di elaborazione.</span><span class="sxs-lookup"><span data-stu-id="6c028-125">Count of items being processed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c028-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6c028-126">Return value</span></span>

<span data-ttu-id="6c028-127">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="6c028-127">The method returns an **HRESULT**.</span></span> <span data-ttu-id="6c028-128">Tutti i metodi di interfaccia in Windows Media Gestione dispositivi possono restituire una delle classi di codici di errore seguenti:</span><span class="sxs-lookup"><span data-stu-id="6c028-128">All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:</span></span>

-   <span data-ttu-id="6c028-129">Codici di errore COM standard</span><span class="sxs-lookup"><span data-stu-id="6c028-129">Standard COM error codes</span></span>
-   <span data-ttu-id="6c028-130">Codici di errore di Windows convertiti in valori HRESULT</span><span class="sxs-lookup"><span data-stu-id="6c028-130">Windows error codes converted to HRESULT values</span></span>
-   <span data-ttu-id="6c028-131">Codici di errore di Windows Media Gestione dispositivi</span><span class="sxs-lookup"><span data-stu-id="6c028-131">Windows Media Device Manager error codes</span></span>

<span data-ttu-id="6c028-132">Per un elenco completo dei codici di errore possibili, vedere [codici di errore](error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="6c028-132">For an extensive list of possible error codes, see [Error Codes](error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6c028-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6c028-133">Requirements</span></span>



| <span data-ttu-id="6c028-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c028-134">Requirement</span></span> | <span data-ttu-id="6c028-135">Valore</span><span class="sxs-lookup"><span data-stu-id="6c028-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6c028-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6c028-136">Header</span></span><br/>  | <dl> <span data-ttu-id="6c028-137"><dt>WMDDRMSP. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6c028-137"><dt>WMDDRMSP.idl</dt></span></span> </dl> |
| <span data-ttu-id="6c028-138">Libreria</span><span class="sxs-lookup"><span data-stu-id="6c028-138">Library</span></span><br/> | <dl> <span data-ttu-id="6c028-139"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6c028-139"><dt>Mssachlp.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c028-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6c028-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c028-141">**IWMDRMDevice:: getsyncs**</span><span class="sxs-lookup"><span data-stu-id="6c028-141">**IWMDRMDevice::GetSyncList**</span></span>](iwmdrmdevice-getsynclist.md)
</dt> <dt>

[<span data-ttu-id="6c028-142">**Interfaccia IWMDRMDevice2**</span><span class="sxs-lookup"><span data-stu-id="6c028-142">**IWMDRMDevice2 Interface**</span></span>](iwmdrmdevice2.md)
</dt> </dl>

 

 





