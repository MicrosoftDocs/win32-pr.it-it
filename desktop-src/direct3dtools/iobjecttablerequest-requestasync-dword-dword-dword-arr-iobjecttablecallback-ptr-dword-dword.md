---
description: Richiede di ottenere le informazioni specificate dalla tabella degli oggetti per l'evento specificato.
MS-HAID: vspixengine.IObjectTableRequest\_RequestAsync\_DWORD\_DWORD\_DWORD\_arr\_IObjectTableCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo IObjectTableRequest:: RequestAsync'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: EE40F584-CDDE-465D-B4CB-A98B917DD0EE
api_name:
- IObjectTableRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2c9108708475b27a7a1882051c7f0177e14470f9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746727"
---
# <a name="span-idvspixengineiobjecttablerequest_requestasync_dword_dword_dword_arr_iobjecttablecallback_ptr_dword_dwordspaniobjecttablerequestrequestasync-method"></a><span data-ttu-id="b9ed9-103"><span id="vspixengine.iobjecttablerequest_requestasync_dword_dword_dword_arr_iobjecttablecallback_ptr_dword_dword"></span>Metodo IObjectTableRequest:: RequestAsync</span><span class="sxs-lookup"><span data-stu-id="b9ed9-103"><span id="vspixengine.iobjecttablerequest_requestasync_dword_dword_dword_arr_iobjecttablecallback_ptr_dword_dword"></span>IObjectTableRequest::RequestAsync method</span></span>

<span data-ttu-id="b9ed9-104">Richiede di ottenere le informazioni specificate dalla tabella degli oggetti per l'evento specificato.</span><span class="sxs-lookup"><span data-stu-id="b9ed9-104">Requests to get specified information from the object table for the specified event.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9ed9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b9ed9-105">Syntax</span></span>


```C++
HRESULT RequestAsync(
   DWORD                  eventID,
   DWORD                  numColumns,
   DWORD []               count1_columns,
   IObjectTableCallback * requestCallback,
   DWORD                  requestCookie,
   DWORD                  progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="b9ed9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b9ed9-106">Parameters</span></span>

<span data-ttu-id="b9ed9-107">*eventID* </span><span class="sxs-lookup"><span data-stu-id="b9ed9-107">*eventID* </span></span>  
<span data-ttu-id="b9ed9-108">Evento specificato.</span><span class="sxs-lookup"><span data-stu-id="b9ed9-108">The specified event.</span></span>

<span data-ttu-id="b9ed9-109">*numColumns* </span><span class="sxs-lookup"><span data-stu-id="b9ed9-109">*numColumns* </span></span>  
<span data-ttu-id="b9ed9-110">Numero di colonne (campi) di informazioni da ottenere.</span><span class="sxs-lookup"><span data-stu-id="b9ed9-110">The number of columns (fields) of information to get.</span></span>

<span data-ttu-id="b9ed9-111">*\_colonne count1* </span><span class="sxs-lookup"><span data-stu-id="b9ed9-111">*count1\_columns* </span></span>  
<span data-ttu-id="b9ed9-112">Colonne specificate (campi).</span><span class="sxs-lookup"><span data-stu-id="b9ed9-112">The specified columns (fields).</span></span>

<span data-ttu-id="b9ed9-113">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="b9ed9-113">*requestCallback* </span></span>  
<span data-ttu-id="b9ed9-114">Indirizzo del callback utilizzato per notificare all'host i risultati.</span><span class="sxs-lookup"><span data-stu-id="b9ed9-114">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="b9ed9-115">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="b9ed9-115">*requestCookie* </span></span>  
<span data-ttu-id="b9ed9-116">Un cookie che identifica in modo univoco la richiesta e può essere usato per segnalare l'annullamento.</span><span class="sxs-lookup"><span data-stu-id="b9ed9-116">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="b9ed9-117">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="b9ed9-117">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="b9ed9-118">Non usato.</span><span class="sxs-lookup"><span data-stu-id="b9ed9-118">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="b9ed9-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b9ed9-119">Return value</span></span>

<span data-ttu-id="b9ed9-120">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b9ed9-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b9ed9-121">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b9ed9-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9ed9-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b9ed9-122">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="b9ed9-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b9ed9-123">Header</span></span></p></td><td><span data-ttu-id="b9ed9-124">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="b9ed9-124">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="b9ed9-125"><span id="see_also"></span>Vedere anche</span><span class="sxs-lookup"><span data-stu-id="b9ed9-125"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="b9ed9-126">**IObjectTableRequest**</span><span class="sxs-lookup"><span data-stu-id="b9ed9-126">**IObjectTableRequest**</span></span>](/windows/desktop/direct3dtools/iobjecttablerequest)

 

 
