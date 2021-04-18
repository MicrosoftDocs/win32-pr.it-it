---
description: Richiede la restituzione di dati oggetto generici che descrivono un oggetto nel file con estensione vsglog per l'evento specificato e nel formato specificato.
MS-HAID: vspixengine.IGenericBufferDataRequest\_RequestAsync\_DumperType\_EventID\_DWORD\_IGenericBufferDataCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo IGenericBufferDataRequest:: RequestAsync'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 542E20F9-B91D-4A05-AEE8-9DD2E80B76DB
api_name:
- IGenericBufferDataRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 6d8860b2de7c3dce5c6f8b61467bfe147530ed76
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304353"
---
# <a name="span-idvspixengineigenericbufferdatarequest_requestasync_dumpertype_eventid_dword_igenericbufferdatacallback_ptr_dword_dwordspanigenericbufferdatarequestrequestasync-method"></a><span data-ttu-id="980a5-103"><span id="vspixengine.igenericbufferdatarequest_requestasync_dumpertype_eventid_dword_igenericbufferdatacallback_ptr_dword_dword"></span>Metodo IGenericBufferDataRequest:: RequestAsync</span><span class="sxs-lookup"><span data-stu-id="980a5-103"><span id="vspixengine.igenericbufferdatarequest_requestasync_dumpertype_eventid_dword_igenericbufferdatacallback_ptr_dword_dword"></span>IGenericBufferDataRequest::RequestAsync method</span></span>

<span data-ttu-id="980a5-104">Richiede la restituzione di dati oggetto generici che descrivono un oggetto nel file con estensione vsglog per l'evento specificato e nel formato specificato.</span><span class="sxs-lookup"><span data-stu-id="980a5-104">Requests to return generic object data that describes an object in the .vsglog file for the specified event and in the specified format.</span></span>

## <a name="syntax"></a><span data-ttu-id="980a5-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="980a5-105">Syntax</span></span>


```C++
HRESULT RequestAsync(
   DumperType                   dumperType,
   EventID                      eventID,
   DWORD                        RequestedDataUID,
   IGenericBufferDataCallback * requestCallback,
   DWORD                        requestCookie,
   DWORD                        progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="980a5-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="980a5-106">Parameters</span></span>

<span data-ttu-id="980a5-107">*dumperType* </span><span class="sxs-lookup"><span data-stu-id="980a5-107">*dumperType* </span></span>  
<span data-ttu-id="980a5-108">Formato specificato della rappresentazione testuale dell'oggetto (HTML, XML e così via)</span><span class="sxs-lookup"><span data-stu-id="980a5-108">The specified format of the textual representation of the object (HTML, XML, etc.)</span></span>

<span data-ttu-id="980a5-109">*eventID* </span><span class="sxs-lookup"><span data-stu-id="980a5-109">*eventID* </span></span>  
<span data-ttu-id="980a5-110">Evento specificato a cui associare il contenuto del buffer, ad esempio una destinazione di rendering può cambiare nel tempo.</span><span class="sxs-lookup"><span data-stu-id="980a5-110">The specified event to match the buffer's content to (for example, a render target could change over time).</span></span>

<span data-ttu-id="980a5-111">*RequestedDataUID* </span><span class="sxs-lookup"><span data-stu-id="980a5-111">*RequestedDataUID* </span></span>  
<span data-ttu-id="980a5-112">Indirizzo dell'oggetto specificato.</span><span class="sxs-lookup"><span data-stu-id="980a5-112">The address of the specified object.</span></span>

<span data-ttu-id="980a5-113">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="980a5-113">*requestCallback* </span></span>  
<span data-ttu-id="980a5-114">Indirizzo del callback utilizzato per notificare all'host i risultati.</span><span class="sxs-lookup"><span data-stu-id="980a5-114">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="980a5-115">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="980a5-115">*requestCookie* </span></span>  
<span data-ttu-id="980a5-116">Un cookie che identifica in modo univoco la richiesta e può essere usato per segnalare l'annullamento.</span><span class="sxs-lookup"><span data-stu-id="980a5-116">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="980a5-117">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="980a5-117">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="980a5-118">Non usato.</span><span class="sxs-lookup"><span data-stu-id="980a5-118">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="980a5-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="980a5-119">Return value</span></span>

<span data-ttu-id="980a5-120">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="980a5-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="980a5-121">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="980a5-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="980a5-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="980a5-122">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="980a5-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="980a5-123">Header</span></span></p></td><td><span data-ttu-id="980a5-124">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="980a5-124">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="980a5-125"><span id="see_also"></span>Vedere anche</span><span class="sxs-lookup"><span data-stu-id="980a5-125"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="980a5-126">**IGenericBufferDataRequest**</span><span class="sxs-lookup"><span data-stu-id="980a5-126">**IGenericBufferDataRequest**</span></span>](/windows/desktop/direct3dtools/igenericbufferdatarequest)

 

 
