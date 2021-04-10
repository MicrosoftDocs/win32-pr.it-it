---
description: Restituisce un valore che rappresenta le funzionalità dell'hardware del tablet.
ms.assetid: 68936dab-3df4-42c4-9945-bcd525c996f3
title: 'Metodo ITablet:: GetHardwareCaps'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet.GetHardwareCaps
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 5ada3ad58699952bac5458ddd079abaf84f63bf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884366"
---
# <a name="itabletgethardwarecaps-method"></a><span data-ttu-id="a3866-103">Metodo ITablet:: GetHardwareCaps</span><span class="sxs-lookup"><span data-stu-id="a3866-103">ITablet::GetHardwareCaps method</span></span>

<span data-ttu-id="a3866-104">Restituisce un valore che rappresenta le funzionalità dell'hardware del tablet.</span><span class="sxs-lookup"><span data-stu-id="a3866-104">Returns a value that represents the capabilities of the tablet hardware.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3866-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a3866-105">Syntax</span></span>


```C++
HRESULT GetHardwareCaps(
  [out] DWORD *pdwCaps
);
```



## <a name="parameters"></a><span data-ttu-id="a3866-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a3866-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3866-107">*pdwCaps* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a3866-107">*pdwCaps* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a3866-108">Flag di bit che rappresentano le funzionalità dell'hardware del tablet.</span><span class="sxs-lookup"><span data-stu-id="a3866-108">Bit flags that represent the capabilities of the tablet hardware.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3866-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a3866-109">Return value</span></span>

<span data-ttu-id="a3866-110">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="a3866-110">This method can return one of these values.</span></span>



| <span data-ttu-id="a3866-111">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="a3866-111">Return code</span></span>                                                                            | <span data-ttu-id="a3866-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a3866-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="a3866-113"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a3866-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="a3866-114">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="a3866-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="a3866-115"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="a3866-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="a3866-116">Si è verificato un errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="a3866-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a3866-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="a3866-117">Remarks</span></span>

<span data-ttu-id="a3866-118">Il parametro *pdwCaps* è un set di flag di bit che descrivono le funzionalità hardware del tablet.</span><span class="sxs-lookup"><span data-stu-id="a3866-118">The *pdwCaps* parameter is a set of bit flags that describe tablet hardware capabilities.</span></span> <span data-ttu-id="a3866-119">Nella tabella seguente vengono descritti questi flag.</span><span class="sxs-lookup"><span data-stu-id="a3866-119">The following table describes these flags.</span></span>



| <span data-ttu-id="a3866-120">Nome del flag</span><span class="sxs-lookup"><span data-stu-id="a3866-120">Flag Name</span></span>                         | <span data-ttu-id="a3866-121">Valore</span><span class="sxs-lookup"><span data-stu-id="a3866-121">Value</span></span>                 | <span data-ttu-id="a3866-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a3866-122">Description</span></span>                                                                                                                    |
|-----------------------------------|-----------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3866-123">THWC \_ integrato</span><span class="sxs-lookup"><span data-stu-id="a3866-123">THWC\_INTEGRATED</span></span><br/>       | <span data-ttu-id="a3866-124">0x00000001</span><span class="sxs-lookup"><span data-stu-id="a3866-124">0x00000001</span></span><br/> | <span data-ttu-id="a3866-125">Indica che la visualizzazione e il digitalizzatore condividono la stessa superficie.</span><span class="sxs-lookup"><span data-stu-id="a3866-125">Indicates that the display and digitizer share the same surface.</span></span><br/>                                                    |
| <span data-ttu-id="a3866-126">THWC \_ CSR \_ deve \_ toccare</span><span class="sxs-lookup"><span data-stu-id="a3866-126">THWC\_CSR\_MUST\_TOUCH</span></span><br/> | <span data-ttu-id="a3866-127">0x00000002</span><span class="sxs-lookup"><span data-stu-id="a3866-127">0x00000002</span></span><br/> | <span data-ttu-id="a3866-128">Indica che il cursore deve essere in contatto fisico con il dispositivo per segnalare la posizione.</span><span class="sxs-lookup"><span data-stu-id="a3866-128">Indicates that the cursor must be in physical contact with the device to report position.</span></span><br/>                           |
| <span data-ttu-id="a3866-129">\_prossimità THWC \_</span><span class="sxs-lookup"><span data-stu-id="a3866-129">THWC\_HARD\_PROXIMITY</span></span><br/>  | <span data-ttu-id="a3866-130">0x00000004</span><span class="sxs-lookup"><span data-stu-id="a3866-130">0x00000004</span></span><br/> | <span data-ttu-id="a3866-131">Indica che il dispositivo può generare eventi quando il cursore entra e lascia l'intervallo di rilevamento fisico.</span><span class="sxs-lookup"><span data-stu-id="a3866-131">Indicates that the device can generate events when the cursor is entering and leaving the physical detection range.</span></span><br/> |
| <span data-ttu-id="a3866-132">THWC \_ PHYSID \_ i CSR</span><span class="sxs-lookup"><span data-stu-id="a3866-132">THWC\_PHYSID\_CSRS</span></span><br/>     | <span data-ttu-id="a3866-133">0x00000008</span><span class="sxs-lookup"><span data-stu-id="a3866-133">0x00000008</span></span><br/> | <span data-ttu-id="a3866-134">Indica che il dispositivo può identificare in modo univoco il cursore attivo nell'hardware.</span><span class="sxs-lookup"><span data-stu-id="a3866-134">Indicates that the device can uniquely identify the active cursor in hardware.</span></span><br/>                                      |



 

## <a name="requirements"></a><span data-ttu-id="a3866-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a3866-135">Requirements</span></span>



| <span data-ttu-id="a3866-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3866-136">Requirement</span></span> | <span data-ttu-id="a3866-137">Valore</span><span class="sxs-lookup"><span data-stu-id="a3866-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a3866-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a3866-138">Minimum supported client</span></span><br/> | <span data-ttu-id="a3866-139">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="a3866-139">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="a3866-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a3866-140">Minimum supported server</span></span><br/> | <span data-ttu-id="a3866-141">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="a3866-141">None supported</span></span><br/>                                                              |
| <span data-ttu-id="a3866-142">Libreria</span><span class="sxs-lookup"><span data-stu-id="a3866-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="a3866-143"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a3866-143"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3866-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a3866-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3866-145">**Interfaccia ITablet**</span><span class="sxs-lookup"><span data-stu-id="a3866-145">**ITablet Interface**</span></span>](itablet.md)
</dt> </dl>

 

 




