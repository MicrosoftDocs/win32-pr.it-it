---
description: Richieste di annullamento dell'analisi offline in una richiesta di analisi offline.
MS-HAID: vspixengine.IOfflineAnalysisRequest\_CancelOfflineAnalysisAsync\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo IOfflineAnalysisRequest:: CancelOfflineAnalysisAsync'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 20107890-DF7B-4483-9D2C-1D9164366504
api_name:
- IOfflineAnalysisRequest.CancelOfflineAnalysisAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 79329d27aff74efb7d08c7cc182ddb6e21f96cba
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481500"
---
# <a name="span-idvspixengineiofflineanalysisrequest_cancelofflineanalysisasync_dwordspaniofflineanalysisrequestcancelofflineanalysisasync-method"></a><span data-ttu-id="3674c-103"><span id="vspixengine.iofflineanalysisrequest_cancelofflineanalysisasync_dword"></span>Metodo IOfflineAnalysisRequest:: CancelOfflineAnalysisAsync</span><span class="sxs-lookup"><span data-stu-id="3674c-103"><span id="vspixengine.iofflineanalysisrequest_cancelofflineanalysisasync_dword"></span>IOfflineAnalysisRequest::CancelOfflineAnalysisAsync method</span></span>

<span data-ttu-id="3674c-104">Richieste di annullamento dell'analisi offline in una richiesta di analisi offline.</span><span class="sxs-lookup"><span data-stu-id="3674c-104">Requests to cancel offline analysis in an offline analysis request.</span></span>

## <a name="syntax"></a><span data-ttu-id="3674c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3674c-105">Syntax</span></span>


```C++
HRESULT CancelOfflineAnalysisAsync(
   DWORD cookie
);
```

## <a name="parameters"></a><span data-ttu-id="3674c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3674c-106">Parameters</span></span>

<span data-ttu-id="3674c-107">*cookie* </span><span class="sxs-lookup"><span data-stu-id="3674c-107">*cookie* </span></span>  
<span data-ttu-id="3674c-108">Un cookie che identifica in modo univoco la richiesta e può essere usato per segnalare l'annullamento.</span><span class="sxs-lookup"><span data-stu-id="3674c-108">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

## <a name="return-value"></a><span data-ttu-id="3674c-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3674c-109">Return value</span></span>

<span data-ttu-id="3674c-110">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="3674c-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3674c-111">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3674c-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="3674c-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3674c-112">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="3674c-113">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3674c-113">Header</span></span></p></td><td><span data-ttu-id="3674c-114">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="3674c-114">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="3674c-115"><span id="see_also"></span>Vedere anche</span><span class="sxs-lookup"><span data-stu-id="3674c-115"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="3674c-116">**IOfflineAnalysisRequest**</span><span class="sxs-lookup"><span data-stu-id="3674c-116">**IOfflineAnalysisRequest**</span></span>](/windows/desktop/direct3dtools/iofflineanalysisrequest)

 

 
