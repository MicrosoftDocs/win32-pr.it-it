---
description: Richiede di ottenere il contenuto di una trama affiancata come. File DDS (superficie DirectDraw).
MS-HAID: vspixengine.ITileRequest\_RequestTextureTileAsync\_EventID\_DWORD\_UINT\_UINT\_UINT\_UINT\_BSTR\_ITextureCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo ITileRequest:: RequestTextureTileAsync'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: E3F4FAC2-E7D9-4FDF-BE64-73D3EA175A8F
api_name:
- ITileRequest.RequestTextureTileAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e22c3b54c1e04242805d698c37a1d4dd2709fa0b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124710"
---
# <a name="span-idvspixengineitilerequest_requesttexturetileasync_eventid_dword_uint_uint_uint_uint_bstr_itexturecallback_ptr_dword_dwordspanitilerequestrequesttexturetileasync-method"></a><span data-ttu-id="1cb6f-103"><span id="vspixengine.itilerequest_requesttexturetileasync_eventid_dword_uint_uint_uint_uint_bstr_itexturecallback_ptr_dword_dword"></span>Metodo ITileRequest:: RequestTextureTileAsync</span><span class="sxs-lookup"><span data-stu-id="1cb6f-103"><span id="vspixengine.itilerequest_requesttexturetileasync_eventid_dword_uint_uint_uint_uint_bstr_itexturecallback_ptr_dword_dword"></span>ITileRequest::RequestTextureTileAsync method</span></span>

<span data-ttu-id="1cb6f-104">Richiede di ottenere il contenuto di una trama affiancata come. File DDS (superficie DirectDraw).</span><span class="sxs-lookup"><span data-stu-id="1cb6f-104">Requests to get the contents of a tiled texture as a .DDS (DirectDraw Surface) file.</span></span>

## <a name="syntax"></a><span data-ttu-id="1cb6f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1cb6f-105">Syntax</span></span>


```C++
HRESULT RequestTextureTileAsync(
   EventID            eventID,
   DWORD              textureFileptr,
   UINT               tileSubresource,
   UINT               tileX,
   UINT               tileY,
   UINT               tileZ,
   BSTR               ddsFilename,
   ITextureCallback * pRequestCallback,
   DWORD              requestCookie,
   DWORD              progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="1cb6f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1cb6f-106">Parameters</span></span>

<span data-ttu-id="1cb6f-107">*eventID* </span><span class="sxs-lookup"><span data-stu-id="1cb6f-107">*eventID* </span></span>  
<span data-ttu-id="1cb6f-108">Evento specificato a cui associare il contenuto del buffer, ad esempio una destinazione di rendering può cambiare nel tempo.</span><span class="sxs-lookup"><span data-stu-id="1cb6f-108">The specified event to match the buffer's content to (for example, a render target could change over time).</span></span>

<span data-ttu-id="1cb6f-109">*textureFileptr* </span><span class="sxs-lookup"><span data-stu-id="1cb6f-109">*textureFileptr* </span></span>  
<span data-ttu-id="1cb6f-110">Indirizzo dell'oggetto texture specificato.</span><span class="sxs-lookup"><span data-stu-id="1cb6f-110">The address of the specified texture object.</span></span>

<span data-ttu-id="1cb6f-111">*tileSubresource* </span><span class="sxs-lookup"><span data-stu-id="1cb6f-111">*tileSubresource* </span></span>  
<span data-ttu-id="1cb6f-112">Sottorisorsa specificata della sezione.</span><span class="sxs-lookup"><span data-stu-id="1cb6f-112">The specified subresource of the tile.</span></span>

<span data-ttu-id="1cb6f-113">*tileX* </span><span class="sxs-lookup"><span data-stu-id="1cb6f-113">*tileX* </span></span>  
<span data-ttu-id="1cb6f-114">Posizione X del riquadro specificata.</span><span class="sxs-lookup"><span data-stu-id="1cb6f-114">The specified tile X position.</span></span>

<span data-ttu-id="1cb6f-115">*affiancato* </span><span class="sxs-lookup"><span data-stu-id="1cb6f-115">*tileY* </span></span>  
<span data-ttu-id="1cb6f-116">Posizione Y del riquadro specificato.</span><span class="sxs-lookup"><span data-stu-id="1cb6f-116">The specified tile Y position.</span></span>

<span data-ttu-id="1cb6f-117">*tileZ* </span><span class="sxs-lookup"><span data-stu-id="1cb6f-117">*tileZ* </span></span>  
<span data-ttu-id="1cb6f-118">Posizione del riquadro Z specificata.</span><span class="sxs-lookup"><span data-stu-id="1cb6f-118">The specified tile Z position.</span></span>

<span data-ttu-id="1cb6f-119">*ddsFilename* </span><span class="sxs-lookup"><span data-stu-id="1cb6f-119">*ddsFilename* </span></span>  
<span data-ttu-id="1cb6f-120">Stringa COM che contiene il percorso del file con estensione DDS in cui vengono scritti i risultati.</span><span class="sxs-lookup"><span data-stu-id="1cb6f-120">A COM string that contains the pathname of the .dds file where results are written.</span></span>

<span data-ttu-id="1cb6f-121">*pRequestCallback* </span><span class="sxs-lookup"><span data-stu-id="1cb6f-121">*pRequestCallback* </span></span>  
<span data-ttu-id="1cb6f-122">Indirizzo del callback utilizzato per notificare all'host i risultati.</span><span class="sxs-lookup"><span data-stu-id="1cb6f-122">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="1cb6f-123">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="1cb6f-123">*requestCookie* </span></span>  
<span data-ttu-id="1cb6f-124">Un cookie che identifica in modo univoco la richiesta e può essere usato per segnalare l'annullamento.</span><span class="sxs-lookup"><span data-stu-id="1cb6f-124">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="1cb6f-125">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="1cb6f-125">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="1cb6f-126">Non usato.</span><span class="sxs-lookup"><span data-stu-id="1cb6f-126">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="1cb6f-127">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1cb6f-127">Return value</span></span>

<span data-ttu-id="1cb6f-128">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="1cb6f-128">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1cb6f-129">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1cb6f-129">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="1cb6f-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1cb6f-130">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="1cb6f-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1cb6f-131">Header</span></span></p></td><td><span data-ttu-id="1cb6f-132">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="1cb6f-132">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="1cb6f-133"><span id="see_also"></span>Vedere anche</span><span class="sxs-lookup"><span data-stu-id="1cb6f-133"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="1cb6f-134">**ITileRequest**</span><span class="sxs-lookup"><span data-stu-id="1cb6f-134">**ITileRequest**</span></span>](/windows/desktop/direct3dtools/itilerequest)

 

 
