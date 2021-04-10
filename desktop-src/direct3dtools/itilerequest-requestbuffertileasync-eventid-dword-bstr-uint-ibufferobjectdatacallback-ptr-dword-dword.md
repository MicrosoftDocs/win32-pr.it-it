---
description: Richiede di ottenere il contenuto non elaborato di un riquadro.
MS-HAID: vspixengine.ITileRequest_RequestBufferTileAsync_EventID_DWORD_BSTR_UINT_IBufferObjectDataCallback_ptr_DWORD_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo ITileRequest:: RequestBufferTileAsync'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 2D68766F-1BED-439E-AC51-790471DA4F70
api_name:
- ITileRequest.RequestBufferTileAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 83f013b4bc3235ece2850c75324333e4b59d298f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104225489"
---
# <a name="span-idvspixengineitilerequest_requestbuffertileasync_eventid_dword_bstr_uint_ibufferobjectdatacallback_ptr_dword_dwordspanitilerequestrequestbuffertileasync-method"></a><span data-ttu-id="db7fe-103"><span id="vspixengine.itilerequest_requestbuffertileasync_eventid_dword_bstr_uint_ibufferobjectdatacallback_ptr_dword_dword"></span>Metodo ITileRequest:: RequestBufferTileAsync</span><span class="sxs-lookup"><span data-stu-id="db7fe-103"><span id="vspixengine.itilerequest_requestbuffertileasync_eventid_dword_bstr_uint_ibufferobjectdatacallback_ptr_dword_dword"></span>ITileRequest::RequestBufferTileAsync method</span></span>

<span data-ttu-id="db7fe-104">Richiede di ottenere il contenuto non elaborato di un riquadro.</span><span class="sxs-lookup"><span data-stu-id="db7fe-104">Requests to get the raw contents of a tile.</span></span>

## <a name="syntax"></a><span data-ttu-id="db7fe-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="db7fe-105">Syntax</span></span>


```C++
HRESULT RequestBufferTileAsync(
   EventID                     eventID,
   DWORD                       RequestedDataUID,
   BSTR                        File,
   UINT                        tileIndex,
   IBufferObjectDataCallback * requestCallback,
   DWORD                       requestCookie,
   DWORD                       progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="db7fe-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="db7fe-106">Parameters</span></span>

<span data-ttu-id="db7fe-107">*eventID* </span><span class="sxs-lookup"><span data-stu-id="db7fe-107">*eventID* </span></span>  
<span data-ttu-id="db7fe-108">Evento specificato a cui associare il contenuto del riquadro, ad esempio una destinazione di rendering può cambiare nel tempo.</span><span class="sxs-lookup"><span data-stu-id="db7fe-108">The specified event to match the tile's content to (for example, a render target could change over time).</span></span>

<span data-ttu-id="db7fe-109">*RequestedDataUID* </span><span class="sxs-lookup"><span data-stu-id="db7fe-109">*RequestedDataUID* </span></span>  
<span data-ttu-id="db7fe-110">Indirizzo del riquadro specificato.</span><span class="sxs-lookup"><span data-stu-id="db7fe-110">The address of the specified tile.</span></span>

<span data-ttu-id="db7fe-111">*File* </span><span class="sxs-lookup"><span data-stu-id="db7fe-111">*File* </span></span>  
<span data-ttu-id="db7fe-112">Stringa COM che contiene il percorso del file in cui vengono scritti i risultati.</span><span class="sxs-lookup"><span data-stu-id="db7fe-112">A COM string that contains the pathname of the file where results are written.</span></span>

<span data-ttu-id="db7fe-113">*tileIndex* </span><span class="sxs-lookup"><span data-stu-id="db7fe-113">*tileIndex* </span></span>  
<span data-ttu-id="db7fe-114">Indice del riquadro specificato.</span><span class="sxs-lookup"><span data-stu-id="db7fe-114">The index of the specified tile.</span></span>

<span data-ttu-id="db7fe-115">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="db7fe-115">*requestCallback* </span></span>  
<span data-ttu-id="db7fe-116">Indirizzo del callback utilizzato per notificare all'host i risultati.</span><span class="sxs-lookup"><span data-stu-id="db7fe-116">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="db7fe-117">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="db7fe-117">*requestCookie* </span></span>  
<span data-ttu-id="db7fe-118">Un cookie che identifica in modo univoco la richiesta e può essere usato per segnalare l'annullamento.</span><span class="sxs-lookup"><span data-stu-id="db7fe-118">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="db7fe-119">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="db7fe-119">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="db7fe-120">Non usato.</span><span class="sxs-lookup"><span data-stu-id="db7fe-120">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="db7fe-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="db7fe-121">Return value</span></span>

<span data-ttu-id="db7fe-122">Se questo metodo ha esito positivo, restituisce **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="db7fe-122">If this method succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="db7fe-123">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="db7fe-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="db7fe-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="db7fe-124">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="db7fe-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="db7fe-125">Header</span></span></p></td><td><span data-ttu-id="db7fe-126">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="db7fe-126">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="db7fe-127"><span id="see_also"></span>Vedere anche</span><span class="sxs-lookup"><span data-stu-id="db7fe-127"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="db7fe-128">**ITileRequest**</span><span class="sxs-lookup"><span data-stu-id="db7fe-128">**ITileRequest**</span></span>](/windows/desktop/direct3dtools/itilerequest)

 

 
