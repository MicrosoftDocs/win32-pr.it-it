---
description: "Metodo IWiaUIExtension2::GetDeviceIcon: ottiene un'icona del dispositivo personalizzata."
ms.assetid: ea768dd1-22fe-4a0f-8851-b152e28d65fb
title: Metodo IWiaUIExtension2::GetDeviceIcon (Wiadevd.h)
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
ms.openlocfilehash: fe1498a804de5adeeea459464e95640b3b81ef06
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116619"
---
# <a name="iwiauiextension2getdeviceicon-method"></a><span data-ttu-id="3de17-103">Metodo IWiaUIExtension2::GetDeviceIcon</span><span class="sxs-lookup"><span data-stu-id="3de17-103">IWiaUIExtension2::GetDeviceIcon method</span></span>

<span data-ttu-id="3de17-104">Ottiene un'icona del dispositivo personalizzata.</span><span class="sxs-lookup"><span data-stu-id="3de17-104">Gets a custom device icon.</span></span>

## <a name="syntax"></a><span data-ttu-id="3de17-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3de17-105">Syntax</span></span>


```C++
HRESULT GetDeviceIcon(
  [in]  BSTR  bstrDeviceId,
  [out] HICON *phIcon,
  [in]  ULONG nSize
);
```



## <a name="parameters"></a><span data-ttu-id="3de17-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3de17-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3de17-107">*bstrDeviceId* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="3de17-107">*bstrDeviceId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3de17-108">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="3de17-108">Type: **BSTR**</span></span>

<span data-ttu-id="3de17-109">Specifica l'ID dispositivo del dispositivo WIA per il quale è necessario ottenere l'icona.</span><span class="sxs-lookup"><span data-stu-id="3de17-109">Specifies the device ID of the WIA device for which the icon is to be obtained.</span></span>

</dd> <dt>

<span data-ttu-id="3de17-110">*phIcon* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="3de17-110">*phIcon* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3de17-111">Tipo: **HICON \***</span><span class="sxs-lookup"><span data-stu-id="3de17-111">Type: **HICON\***</span></span>

<span data-ttu-id="3de17-112">Punta a una posizione di memoria che riceverà un handle per l'icona per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3de17-112">Points to a memory location that will receive a handle for the icon for the device.</span></span>

</dd> <dt>

<span data-ttu-id="3de17-113">*nSize* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="3de17-113">*nSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3de17-114">Tipo: **ULONG**</span><span class="sxs-lookup"><span data-stu-id="3de17-114">Type: **ULONG**</span></span>

<span data-ttu-id="3de17-115">Specifica le dimensioni dell'icona desiderate, in pixel.</span><span class="sxs-lookup"><span data-stu-id="3de17-115">Specifies the desired icon size, in pixels.</span></span> <span data-ttu-id="3de17-116">Si presuppone che l'icona sia quadrata e che nSize specifichi sia la larghezza che l'altezza dell'icona richiesta.</span><span class="sxs-lookup"><span data-stu-id="3de17-116">The icon is assumed to be square, and nSize specifies both the width and height of the requested icon.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3de17-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3de17-117">Return value</span></span>

<span data-ttu-id="3de17-118">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="3de17-118">Type: **HRESULT**</span></span>

<span data-ttu-id="3de17-119">Se il metodo ha esito positivo, restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3de17-119">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="3de17-120">Se il metodo ha esito negativo, restituisce un codice di errore appropriato.</span><span class="sxs-lookup"><span data-stu-id="3de17-120">If the method fails, it returns an appropriate error code.</span></span> <span data-ttu-id="3de17-121">La tabella seguente illustra alcuni dei possibili codici di stato restituiti.</span><span class="sxs-lookup"><span data-stu-id="3de17-121">The following table shows some of the possible return status codes.</span></span>



| <span data-ttu-id="3de17-122">Codice di errore</span><span class="sxs-lookup"><span data-stu-id="3de17-122">Error code</span></span>    | <span data-ttu-id="3de17-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3de17-123">Description</span></span>                                                                                                  |
|---------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3de17-124">E \_ INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="3de17-124">E\_INVALIDARG</span></span> | <span data-ttu-id="3de17-125">Il parametro bstrDeviceId o phIcon è **NULL** oppure bstrDeviceId non punta a una stringa ID dispositivo WIA valida</span><span class="sxs-lookup"><span data-stu-id="3de17-125">Parameter bstrDeviceId or phIcon is **NULL**, or bstrDeviceId does not point to a valid WIA device ID string</span></span> |
| <span data-ttu-id="3de17-126">E \_ FAIL</span><span class="sxs-lookup"><span data-stu-id="3de17-126">E\_FAIL</span></span>       | <span data-ttu-id="3de17-127">Nessuna risorsa icona disponibile.</span><span class="sxs-lookup"><span data-stu-id="3de17-127">No icon resource is available.</span></span>                                                                               |
| <span data-ttu-id="3de17-128">E \_ NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="3de17-128">E\_NOTIMPL</span></span>    | <span data-ttu-id="3de17-129">Non è disponibile alcuna icona delle dimensioni richieste.</span><span class="sxs-lookup"><span data-stu-id="3de17-129">No icon of the size requested is available.</span></span>                                                                  |



 

## <a name="requirements"></a><span data-ttu-id="3de17-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3de17-130">Requirements</span></span>



| <span data-ttu-id="3de17-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="3de17-131">Requirement</span></span> | <span data-ttu-id="3de17-132">Valore</span><span class="sxs-lookup"><span data-stu-id="3de17-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="3de17-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3de17-133">Minimum supported client</span></span><br/> | <span data-ttu-id="3de17-134">Solo app desktop di Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="3de17-134">Windows XP \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="3de17-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3de17-135">Minimum supported server</span></span><br/> | <span data-ttu-id="3de17-136">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="3de17-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="3de17-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3de17-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="3de17-138"><dt>Wiadevd.h</dt></span><span class="sxs-lookup"><span data-stu-id="3de17-138"><dt>Wiadevd.h</dt></span></span> </dl> |



 

 




