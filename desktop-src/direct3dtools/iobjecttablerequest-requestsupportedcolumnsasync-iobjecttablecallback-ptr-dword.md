---
description: Richieste per ottenere informazioni sulle colonne (campi) supportate dal tipo di richiesta della tabella di oggetti.
MS-HAID: vspixengine.IObjectTableRequest\_RequestSupportedColumnsAsync\_IObjectTableCallback\_ptr\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo IObjectTableRequest:: RequestSupportedColumnsAsync'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 0931C81A-65D5-493E-9F54-C7E98FA2FA6F
api_name:
- IObjectTableRequest.RequestSupportedColumnsAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 6773a69061e7a17d2271e1a53f89f6f2def1a6c2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522746"
---
# <a name="span-idvspixengineiobjecttablerequest_requestsupportedcolumnsasync_iobjecttablecallback_ptr_dwordspaniobjecttablerequestrequestsupportedcolumnsasync-method"></a><span data-ttu-id="4db06-103"><span id="vspixengine.iobjecttablerequest_requestsupportedcolumnsasync_iobjecttablecallback_ptr_dword"></span>Metodo IObjectTableRequest:: RequestSupportedColumnsAsync</span><span class="sxs-lookup"><span data-stu-id="4db06-103"><span id="vspixengine.iobjecttablerequest_requestsupportedcolumnsasync_iobjecttablecallback_ptr_dword"></span>IObjectTableRequest::RequestSupportedColumnsAsync method</span></span>

<span data-ttu-id="4db06-104">Richieste per ottenere informazioni sulle colonne (campi) supportate dal tipo di richiesta della tabella di oggetti.</span><span class="sxs-lookup"><span data-stu-id="4db06-104">Requests to get information about what columns (fields) this object table request type supports.</span></span>

## <a name="syntax"></a><span data-ttu-id="4db06-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4db06-105">Syntax</span></span>


```C++
HRESULT RequestSupportedColumnsAsync(
   IObjectTableCallback * requestCallback,
   DWORD                  progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="4db06-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4db06-106">Parameters</span></span>

<span data-ttu-id="4db06-107">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="4db06-107">*requestCallback* </span></span>  
<span data-ttu-id="4db06-108">Indirizzo del callback utilizzato per notificare all'host i risultati.</span><span class="sxs-lookup"><span data-stu-id="4db06-108">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="4db06-109">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="4db06-109">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="4db06-110">Non usato.</span><span class="sxs-lookup"><span data-stu-id="4db06-110">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="4db06-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4db06-111">Return value</span></span>

<span data-ttu-id="4db06-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="4db06-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4db06-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4db06-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="4db06-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4db06-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="4db06-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4db06-115">Header</span></span></p></td><td><span data-ttu-id="4db06-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="4db06-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="4db06-117"><span id="see_also"></span>Vedere anche</span><span class="sxs-lookup"><span data-stu-id="4db06-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="4db06-118">**IObjectTableRequest**</span><span class="sxs-lookup"><span data-stu-id="4db06-118">**IObjectTableRequest**</span></span>](/windows/desktop/direct3dtools/iobjecttablerequest)

 

 
