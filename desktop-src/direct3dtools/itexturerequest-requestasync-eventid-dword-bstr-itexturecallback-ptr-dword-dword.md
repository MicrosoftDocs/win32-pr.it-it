---
description: Richiede di ottenere il contenuto di una trama come. File DDS (superficie DirectDraw).
MS-HAID: vspixengine.ITextureRequest\_RequestAsync\_EventID\_DWORD\_BSTR\_ITextureCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo ITextureRequest:: RequestAsync'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 89A9F230-D296-43CD-A2A6-747057750EED
api_name:
- ITextureRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e5abfee1b26fd2145aef8e01239cc0b874ee54e2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482565"
---
# <a name="span-idvspixengineitexturerequest_requestasync_eventid_dword_bstr_itexturecallback_ptr_dword_dwordspanitexturerequestrequestasync-method"></a><span data-ttu-id="9aa15-103"><span id="vspixengine.itexturerequest_requestasync_eventid_dword_bstr_itexturecallback_ptr_dword_dword"></span>Metodo ITextureRequest:: RequestAsync</span><span class="sxs-lookup"><span data-stu-id="9aa15-103"><span id="vspixengine.itexturerequest_requestasync_eventid_dword_bstr_itexturecallback_ptr_dword_dword"></span>ITextureRequest::RequestAsync method</span></span>

<span data-ttu-id="9aa15-104">Richiede di ottenere il contenuto di una trama come. File DDS (superficie DirectDraw).</span><span class="sxs-lookup"><span data-stu-id="9aa15-104">Requests to get the contents of a texture as a .DDS (DirectDraw Surface) file.</span></span>

## <a name="syntax"></a><span data-ttu-id="9aa15-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9aa15-105">Syntax</span></span>


```C++
HRESULT RequestAsync(
   EventID            eventID,
   DWORD              textureFileptr,
   BSTR               ddsFilename,
   ITextureCallback * pRequestCallback,
   DWORD              requestCookie,
   DWORD              progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="9aa15-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9aa15-106">Parameters</span></span>

<span data-ttu-id="9aa15-107">*eventID* </span><span class="sxs-lookup"><span data-stu-id="9aa15-107">*eventID* </span></span>  
<span data-ttu-id="9aa15-108">Evento specificato a cui associare il contenuto del buffer, ad esempio una destinazione di rendering può cambiare nel tempo.</span><span class="sxs-lookup"><span data-stu-id="9aa15-108">The specified event to match the buffer's content to (for example, a render target could change over time).</span></span>

<span data-ttu-id="9aa15-109">*textureFileptr* </span><span class="sxs-lookup"><span data-stu-id="9aa15-109">*textureFileptr* </span></span>  
<span data-ttu-id="9aa15-110">Indirizzo dell'oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="9aa15-110">The address of the texture object.</span></span>

<span data-ttu-id="9aa15-111">*ddsFilename* </span><span class="sxs-lookup"><span data-stu-id="9aa15-111">*ddsFilename* </span></span>  
<span data-ttu-id="9aa15-112">Stringa COM che contiene il percorso del file con estensione DDS in cui vengono scritti i risultati.</span><span class="sxs-lookup"><span data-stu-id="9aa15-112">A COM string that contains the pathname of the .dds file where results are written.</span></span>

<span data-ttu-id="9aa15-113">*pRequestCallback* </span><span class="sxs-lookup"><span data-stu-id="9aa15-113">*pRequestCallback* </span></span>  
<span data-ttu-id="9aa15-114">Indirizzo del callback utilizzato per notificare all'host i risultati.</span><span class="sxs-lookup"><span data-stu-id="9aa15-114">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="9aa15-115">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="9aa15-115">*requestCookie* </span></span>  
<span data-ttu-id="9aa15-116">Un cookie che identifica in modo univoco la richiesta e può essere usato per segnalare l'annullamento.</span><span class="sxs-lookup"><span data-stu-id="9aa15-116">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="9aa15-117">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="9aa15-117">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="9aa15-118">Non usato.</span><span class="sxs-lookup"><span data-stu-id="9aa15-118">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="9aa15-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9aa15-119">Return value</span></span>

<span data-ttu-id="9aa15-120">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="9aa15-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9aa15-121">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9aa15-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="9aa15-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9aa15-122">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="9aa15-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9aa15-123">Header</span></span></p></td><td><span data-ttu-id="9aa15-124">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="9aa15-124">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="9aa15-125"><span id="see_also"></span>Vedere anche</span><span class="sxs-lookup"><span data-stu-id="9aa15-125"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="9aa15-126">**ITextureRequest**</span><span class="sxs-lookup"><span data-stu-id="9aa15-126">**ITextureRequest**</span></span>](/windows/desktop/direct3dtools/itexturerequest)

 

 
