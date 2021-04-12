---
description: Ottiene un'icona di dispositivo personalizzata.
ms.assetid: ea768dd1-22fe-4a0f-8851-b152e28d65fb
title: 'Metodo IWiaUIExtension2:: GetDeviceIcon (Wiadevd. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension2.GetDeviceIcon
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: d071332a1947c4eb6398235d6941a6843a4fa54c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526443"
---
# <a name="iwiauiextension2getdeviceicon-method"></a><span data-ttu-id="35728-103">Metodo IWiaUIExtension2:: GetDeviceIcon</span><span class="sxs-lookup"><span data-stu-id="35728-103">IWiaUIExtension2::GetDeviceIcon method</span></span>

<span data-ttu-id="35728-104">Ottiene un'icona di dispositivo personalizzata.</span><span class="sxs-lookup"><span data-stu-id="35728-104">Gets a custom device icon.</span></span>

## <a name="syntax"></a><span data-ttu-id="35728-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="35728-105">Syntax</span></span>


```C++
HRESULT GetDeviceIcon(
  [in]  BSTR  bstrDeviceId,
  [out] HICON *phIcon,
  [in]  ULONG nSize
);
```



## <a name="parameters"></a><span data-ttu-id="35728-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="35728-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35728-107">*bstrDeviceId* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="35728-107">*bstrDeviceId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35728-108">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="35728-108">Type: **BSTR**</span></span>

<span data-ttu-id="35728-109">Specifica l'ID dispositivo del dispositivo WIA per il quale deve essere ottenuta l'icona.</span><span class="sxs-lookup"><span data-stu-id="35728-109">Specifies the device ID of the WIA device for which the icon is to be obtained.</span></span>

</dd> <dt>

<span data-ttu-id="35728-110">*phIcon* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="35728-110">*phIcon* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="35728-111">Tipo: \**HICON \** _</span><span class="sxs-lookup"><span data-stu-id="35728-111">Type: \**HICON\** _</span></span>

<span data-ttu-id="35728-112">Punta a una posizione di memoria che riceverà un handle per l'icona del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="35728-112">Points to a memory location that will receive a handle for the icon for the device.</span></span>

</dd> <dt>

<span data-ttu-id="35728-113">_nSize \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="35728-113">_nSize\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35728-114">Tipo: **ULONG**</span><span class="sxs-lookup"><span data-stu-id="35728-114">Type: **ULONG**</span></span>

<span data-ttu-id="35728-115">Specifica la dimensione dell'icona desiderata, in pixel.</span><span class="sxs-lookup"><span data-stu-id="35728-115">Specifies the desired icon size, in pixels.</span></span> <span data-ttu-id="35728-116">Si presuppone che l'icona sia quadrata, mentre nSize specifica sia la larghezza che l'altezza dell'icona richiesta.</span><span class="sxs-lookup"><span data-stu-id="35728-116">The icon is assumed to be square, and nSize specifies both the width and height of the requested icon.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35728-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="35728-117">Return value</span></span>

<span data-ttu-id="35728-118">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="35728-118">Type: **HRESULT**</span></span>

<span data-ttu-id="35728-119">Se il metodo ha esito positivo, restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="35728-119">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="35728-120">Se il metodo ha esito negativo, viene restituito un codice di errore appropriato.</span><span class="sxs-lookup"><span data-stu-id="35728-120">If the method fails, it returns an appropriate error code.</span></span> <span data-ttu-id="35728-121">Nella tabella seguente vengono illustrati alcuni dei possibili codici di stato restituiti.</span><span class="sxs-lookup"><span data-stu-id="35728-121">The following table shows some of the possible return status codes.</span></span>



| <span data-ttu-id="35728-122">Codice di errore</span><span class="sxs-lookup"><span data-stu-id="35728-122">Error code</span></span>    | <span data-ttu-id="35728-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="35728-123">Description</span></span>                                                                                                  |
|---------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35728-124">E \_ INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="35728-124">E\_INVALIDARG</span></span> | <span data-ttu-id="35728-125">Il parametro bstrDeviceId o phIcon è **null** oppure bstrDeviceId non punta a una stringa di ID del dispositivo WIA valida</span><span class="sxs-lookup"><span data-stu-id="35728-125">Parameter bstrDeviceId or phIcon is **NULL**, or bstrDeviceId does not point to a valid WIA device ID string</span></span> |
| <span data-ttu-id="35728-126">E \_ non riescono</span><span class="sxs-lookup"><span data-stu-id="35728-126">E\_FAIL</span></span>       | <span data-ttu-id="35728-127">Non sono disponibili risorse icona.</span><span class="sxs-lookup"><span data-stu-id="35728-127">No icon resource is available.</span></span>                                                                               |
| <span data-ttu-id="35728-128">E \_ NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="35728-128">E\_NOTIMPL</span></span>    | <span data-ttu-id="35728-129">Non è disponibile alcuna icona delle dimensioni richieste.</span><span class="sxs-lookup"><span data-stu-id="35728-129">No icon of the size requested is available.</span></span>                                                                  |



 

## <a name="requirements"></a><span data-ttu-id="35728-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="35728-130">Requirements</span></span>



| <span data-ttu-id="35728-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="35728-131">Requirement</span></span> | <span data-ttu-id="35728-132">Valore</span><span class="sxs-lookup"><span data-stu-id="35728-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="35728-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="35728-133">Minimum supported client</span></span><br/> | <span data-ttu-id="35728-134">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="35728-134">Windows XP \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="35728-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="35728-135">Minimum supported server</span></span><br/> | <span data-ttu-id="35728-136">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="35728-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="35728-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="35728-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="35728-138"><dt>Wiadevd. h</dt></span><span class="sxs-lookup"><span data-stu-id="35728-138"><dt>Wiadevd.h</dt></span></span> </dl> |



 

 




