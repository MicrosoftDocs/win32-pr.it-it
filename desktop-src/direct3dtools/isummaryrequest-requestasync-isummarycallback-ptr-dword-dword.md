---
description: Richiesta asincrona per ottenere informazioni di riepilogo su un log di grafica.
MS-HAID: vspixengine.ISummaryRequest\_RequestAsync\_iSummaryCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo ISummaryRequest:: RequestAsync'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: A33798E3-7332-4582-A7B1-B0F9FB694872
api_name:
- ISummaryRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c716545de275250efcae56a6be39c8b620ed014a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304290"
---
# <a name="span-idvspixengineisummaryrequest_requestasync_isummarycallback_ptr_dword_dwordspanisummaryrequestrequestasync-method"></a><span data-ttu-id="88601-103"><span id="vspixengine.isummaryrequest_requestasync_isummarycallback_ptr_dword_dword"></span>Metodo ISummaryRequest:: RequestAsync</span><span class="sxs-lookup"><span data-stu-id="88601-103"><span id="vspixengine.isummaryrequest_requestasync_isummarycallback_ptr_dword_dword"></span>ISummaryRequest::RequestAsync method</span></span>

<span data-ttu-id="88601-104">Richiesta asincrona per ottenere informazioni di riepilogo su un log di grafica.</span><span class="sxs-lookup"><span data-stu-id="88601-104">An asynchronous request to get summary information about a graphics log.</span></span>

## <a name="syntax"></a><span data-ttu-id="88601-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="88601-105">Syntax</span></span>


```C++
HRESULT RequestAsync(
   iSummaryCallback * requestCallback,
   DWORD              requestCookie,
   DWORD              progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="88601-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="88601-106">Parameters</span></span>

<span data-ttu-id="88601-107">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="88601-107">*requestCallback* </span></span>  
<span data-ttu-id="88601-108">Indirizzo del callback utilizzato per notificare all'host i risultati.</span><span class="sxs-lookup"><span data-stu-id="88601-108">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="88601-109">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="88601-109">*requestCookie* </span></span>  
<span data-ttu-id="88601-110">Un cookie che identifica in modo univoco la richiesta e può essere usato per segnalare l'annullamento.</span><span class="sxs-lookup"><span data-stu-id="88601-110">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="88601-111">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="88601-111">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="88601-112">Non usato.</span><span class="sxs-lookup"><span data-stu-id="88601-112">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="88601-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="88601-113">Return value</span></span>

<span data-ttu-id="88601-114">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="88601-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="88601-115">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="88601-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="88601-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="88601-116">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="88601-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="88601-117">Header</span></span></p></td><td><span data-ttu-id="88601-118">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="88601-118">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="88601-119"><span id="see_also"></span>Vedere anche</span><span class="sxs-lookup"><span data-stu-id="88601-119"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="88601-120">**ISummaryRequest**</span><span class="sxs-lookup"><span data-stu-id="88601-120">**ISummaryRequest**</span></span>](/windows/desktop/direct3dtools/isummaryrequest)

 

 
