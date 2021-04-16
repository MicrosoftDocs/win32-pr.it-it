---
description: Passa in modo asincrono le risorse al motore, ad esempio le stringhe per i messaggi di errore.
MS-HAID: vspixengine.IPixEngine7\_InitEngineAsync\_ResourcePair\_arr\_UINT\_IVersionCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo IPixEngine7:: InitEngineAsync'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 10138B39-88D2-4586-BD51-C618722EFFA0
api_name:
- IPixEngine7.InitEngineAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 21d98a207b0194f281abc2800cd63f9be7de5073
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482629"
---
# <a name="span-idvspixengineipixengine7_initengineasync_resourcepair_arr_uint_iversioncallback_ptr_dword_dwordspanipixengine7initengineasync-method"></a><span data-ttu-id="ebca7-103"><span id="vspixengine.ipixengine7_initengineasync_resourcepair_arr_uint_iversioncallback_ptr_dword_dword"></span>Metodo IPixEngine7:: InitEngineAsync</span><span class="sxs-lookup"><span data-stu-id="ebca7-103"><span id="vspixengine.ipixengine7_initengineasync_resourcepair_arr_uint_iversioncallback_ptr_dword_dword"></span>IPixEngine7::InitEngineAsync method</span></span>

<span data-ttu-id="ebca7-104">Passa in modo asincrono le risorse al motore, ad esempio le stringhe per i messaggi di errore.</span><span class="sxs-lookup"><span data-stu-id="ebca7-104">Asynchronously passes resources to the engine, such as strings for error messages.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebca7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ebca7-105">Syntax</span></span>


```C++
HRESULT InitEngineAsync(
   ResourcePair []   count1_resources,
   UINT              count,
   IVersionCallback* versionCallback,
   DWORD             requestCookie,
   DWORD             progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="ebca7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ebca7-106">Parameters</span></span>

<span data-ttu-id="ebca7-107">*risorse di count1 \_* </span><span class="sxs-lookup"><span data-stu-id="ebca7-107">*count1\_resources* </span></span>  
<span data-ttu-id="ebca7-108">Matrice di risorse.</span><span class="sxs-lookup"><span data-stu-id="ebca7-108">An array of resources.</span></span>

<span data-ttu-id="ebca7-109">*conteggio* </span><span class="sxs-lookup"><span data-stu-id="ebca7-109">*count* </span></span>  
<span data-ttu-id="ebca7-110">Il numero di risorse nelle \_ risorse count1</span><span class="sxs-lookup"><span data-stu-id="ebca7-110">The number of resources in count1\_resources</span></span>

<span data-ttu-id="ebca7-111">*versionCallback* </span><span class="sxs-lookup"><span data-stu-id="ebca7-111">*versionCallback* </span></span>  
<span data-ttu-id="ebca7-112">Indirizzo del callback utilizzato per notificare all'host i risultati.</span><span class="sxs-lookup"><span data-stu-id="ebca7-112">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="ebca7-113">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="ebca7-113">*requestCookie* </span></span>  
<span data-ttu-id="ebca7-114">Un cookie che identifica in modo univoco la richiesta e può essere usato per segnalare l'annullamento.</span><span class="sxs-lookup"><span data-stu-id="ebca7-114">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="ebca7-115">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="ebca7-115">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="ebca7-116">Non usato.</span><span class="sxs-lookup"><span data-stu-id="ebca7-116">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="ebca7-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ebca7-117">Return value</span></span>

<span data-ttu-id="ebca7-118">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="ebca7-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ebca7-119">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ebca7-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="ebca7-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ebca7-120">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="ebca7-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ebca7-121">Header</span></span></p></td><td><span data-ttu-id="ebca7-122">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="ebca7-122">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="ebca7-123"><span id="see_also"></span>Vedere anche</span><span class="sxs-lookup"><span data-stu-id="ebca7-123"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="ebca7-124">**IPixEngine7**</span><span class="sxs-lookup"><span data-stu-id="ebca7-124">**IPixEngine7**</span></span>](/windows/desktop/direct3dtools/ipixengine7)

 

 
