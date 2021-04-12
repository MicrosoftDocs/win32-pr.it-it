---
description: Funzione di callback utilizzata per notificare all'host lo stato di avanzamento dell'analisi offline.
MS-HAID: vspixengine.IOfflineAnalysisCallback\_OfflineAnalysisProgress\_DWORD\_DOUBLE
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo IOfflineAnalysisCallback:: OfflineAnalysisProgress'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 17847FD7-A10A-4E52-90AD-ADE446D87E73
api_name:
- IOfflineAnalysisCallback.OfflineAnalysisProgress
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 4184be5d8d40b0ef46fe5e0029e9e4b1f38cf120
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401329"
---
# <a name="span-idvspixengineiofflineanalysiscallback_offlineanalysisprogress_dword_doublespaniofflineanalysiscallbackofflineanalysisprogress-method"></a><span data-ttu-id="23afa-103"><span id="vspixengine.iofflineanalysiscallback_offlineanalysisprogress_dword_double"></span>Metodo IOfflineAnalysisCallback:: OfflineAnalysisProgress</span><span class="sxs-lookup"><span data-stu-id="23afa-103"><span id="vspixengine.iofflineanalysiscallback_offlineanalysisprogress_dword_double"></span>IOfflineAnalysisCallback::OfflineAnalysisProgress method</span></span>

<span data-ttu-id="23afa-104">Funzione di callback utilizzata per notificare all'host lo stato di avanzamento dell'analisi offline.</span><span class="sxs-lookup"><span data-stu-id="23afa-104">A callback function used to notify the host of offline analysis progress.</span></span>

## <a name="syntax"></a><span data-ttu-id="23afa-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="23afa-105">Syntax</span></span>


```C++
HRESULT OfflineAnalysisComplete(
   DWORD   cookie,
   HRESULT result,
   BSTR    outputFullFileName
);
```

## <a name="parameters"></a><span data-ttu-id="23afa-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="23afa-106">Parameters</span></span>

<span data-ttu-id="23afa-107">*cookie* </span><span class="sxs-lookup"><span data-stu-id="23afa-107">*cookie* </span></span>  
<span data-ttu-id="23afa-108">Un cookie che identifica in modo univoco la richiesta e può essere usato per segnalare l'annullamento.</span><span class="sxs-lookup"><span data-stu-id="23afa-108">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="23afa-109">*corso* </span><span class="sxs-lookup"><span data-stu-id="23afa-109">*progress* </span></span>  
<span data-ttu-id="23afa-110">Percentuale di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="23afa-110">The progress percentage.</span></span>

## <a name="return-value"></a><span data-ttu-id="23afa-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="23afa-111">Return value</span></span>

<span data-ttu-id="23afa-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="23afa-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="23afa-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="23afa-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="23afa-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="23afa-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="23afa-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="23afa-115">Header</span></span></p></td><td><span data-ttu-id="23afa-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="23afa-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="23afa-117"><span id="see_also"></span>Vedere anche</span><span class="sxs-lookup"><span data-stu-id="23afa-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="23afa-118">**IOfflineAnalysisCallback**</span><span class="sxs-lookup"><span data-stu-id="23afa-118">**IOfflineAnalysisCallback**</span></span>](/windows/desktop/direct3dtools/iofflineanalysiscallback)

 

 
