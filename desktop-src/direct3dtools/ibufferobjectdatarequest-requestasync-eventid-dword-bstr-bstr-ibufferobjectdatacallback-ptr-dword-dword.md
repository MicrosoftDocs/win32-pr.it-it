---
description: Richieste per ottenere il contenuto non elaborato di un oggetto (buffer, trama, visualizzazione della destinazione di rendering e così via).
MS-HAID: vspixengine.IBufferObjectDataRequest\_RequestAsync\_EventID\_DWORD\_BSTR\_BSTR\_IBufferObjectDataCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo IBufferObjectDataRequest:: RequestAsync'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 899954DC-6196-4F79-AFB4-5E692DAA03EC
api_name:
- IBufferObjectDataRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 97d35f656f373f2f0040d49a78a2c0d376bc4266
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124170"
---
# <a name="span-idvspixengineibufferobjectdatarequest_requestasync_eventid_dword_bstr_bstr_ibufferobjectdatacallback_ptr_dword_dwordspanibufferobjectdatarequestrequestasync-method"></a><span data-ttu-id="1cf1a-103"><span id="vspixengine.ibufferobjectdatarequest_requestasync_eventid_dword_bstr_bstr_ibufferobjectdatacallback_ptr_dword_dword"></span>Metodo IBufferObjectDataRequest:: RequestAsync</span><span class="sxs-lookup"><span data-stu-id="1cf1a-103"><span id="vspixengine.ibufferobjectdatarequest_requestasync_eventid_dword_bstr_bstr_ibufferobjectdatacallback_ptr_dword_dword"></span>IBufferObjectDataRequest::RequestAsync method</span></span>

<span data-ttu-id="1cf1a-104">Richieste per ottenere il contenuto non elaborato di un oggetto (buffer, trama, visualizzazione della destinazione di rendering e così via)</span><span class="sxs-lookup"><span data-stu-id="1cf1a-104">Requests to get the raw contents of an object (buffer, texture, render target view, etc.)</span></span>

## <a name="syntax"></a><span data-ttu-id="1cf1a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1cf1a-105">Syntax</span></span>


```C++
HRESULT RequestAsync(
   EventID                     eventID,
   DWORD                       RequestedDataUID,
   BSTR                        File,
   BSTR                        Format,
   IBufferObjectDataCallback * requestCallback,
   DWORD                       requestCookie,
   DWORD                       progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="1cf1a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1cf1a-106">Parameters</span></span>

<span data-ttu-id="1cf1a-107">*eventID* </span><span class="sxs-lookup"><span data-stu-id="1cf1a-107">*eventID* </span></span>  
<span data-ttu-id="1cf1a-108">Evento specificato a cui associare il contenuto del buffer, ad esempio una destinazione di rendering può cambiare nel tempo.</span><span class="sxs-lookup"><span data-stu-id="1cf1a-108">The specified event to match the buffer's content to (for example, a render target could change over time).</span></span>

<span data-ttu-id="1cf1a-109">*RequestedDataUID* </span><span class="sxs-lookup"><span data-stu-id="1cf1a-109">*RequestedDataUID* </span></span>  
<span data-ttu-id="1cf1a-110">Indirizzo dell'oggetto specificato.</span><span class="sxs-lookup"><span data-stu-id="1cf1a-110">The address of the specified object.</span></span>

<span data-ttu-id="1cf1a-111">*File* </span><span class="sxs-lookup"><span data-stu-id="1cf1a-111">*File* </span></span>  
<span data-ttu-id="1cf1a-112">Stringa COM che contiene il percorso del file in cui vengono scritti i risultati.</span><span class="sxs-lookup"><span data-stu-id="1cf1a-112">A COM string that contains the pathname of the file where results are written.</span></span>

<span data-ttu-id="1cf1a-113">*Formato* </span><span class="sxs-lookup"><span data-stu-id="1cf1a-113">*Format* </span></span>  
<span data-ttu-id="1cf1a-114">Attualmente non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="1cf1a-114">Not currently used.</span></span> <span data-ttu-id="1cf1a-115">Stringa COM che specifica il formato di output.</span><span class="sxs-lookup"><span data-stu-id="1cf1a-115">A COM string that specifies the output format.</span></span>

<span data-ttu-id="1cf1a-116">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="1cf1a-116">*requestCallback* </span></span>  
<span data-ttu-id="1cf1a-117">Indirizzo del callback utilizzato per notificare all'host i risultati.</span><span class="sxs-lookup"><span data-stu-id="1cf1a-117">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="1cf1a-118">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="1cf1a-118">*requestCookie* </span></span>  
<span data-ttu-id="1cf1a-119">Un cookie che identifica in modo univoco la richiesta e può essere usato per segnalare l'annullamento.</span><span class="sxs-lookup"><span data-stu-id="1cf1a-119">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="1cf1a-120">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="1cf1a-120">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="1cf1a-121">Non usato.</span><span class="sxs-lookup"><span data-stu-id="1cf1a-121">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="1cf1a-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1cf1a-122">Return value</span></span>

<span data-ttu-id="1cf1a-123">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="1cf1a-123">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1cf1a-124">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1cf1a-124">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="1cf1a-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1cf1a-125">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="1cf1a-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1cf1a-126">Header</span></span></p></td><td><span data-ttu-id="1cf1a-127">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="1cf1a-127">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="1cf1a-128"><span id="see_also"></span>Vedere anche</span><span class="sxs-lookup"><span data-stu-id="1cf1a-128"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="1cf1a-129">**IBufferObjectDataRequest**</span><span class="sxs-lookup"><span data-stu-id="1cf1a-129">**IBufferObjectDataRequest**</span></span>](/windows/desktop/direct3dtools/ibufferobjectdatarequest)

 

 
