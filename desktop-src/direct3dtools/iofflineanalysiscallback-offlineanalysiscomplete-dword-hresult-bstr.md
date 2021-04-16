---
description: Funzione di callback utilizzata per notificare all'host che l'analisi offline è stata completata.
MS-HAID: vspixengine.IOfflineAnalysisCallback\_OfflineAnalysisComplete\_DWORD\_HRESULT\_BSTR
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo IOfflineAnalysisCallback:: OfflineAnalysisComplete'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 36E10709-51DC-4657-B184-F1F807ABBBB4
api_name:
- IOfflineAnalysisCallback.OfflineAnalysisComplete
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: a1ece7106bee1c49f97238bf06348b049d3f7167
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522737"
---
# <a name="span-idvspixengineiofflineanalysiscallback_offlineanalysiscomplete_dword_hresult_bstrspaniofflineanalysiscallbackofflineanalysiscomplete-method"></a><span data-ttu-id="3d083-103"><span id="vspixengine.iofflineanalysiscallback_offlineanalysiscomplete_dword_hresult_bstr"></span>Metodo IOfflineAnalysisCallback:: OfflineAnalysisComplete</span><span class="sxs-lookup"><span data-stu-id="3d083-103"><span id="vspixengine.iofflineanalysiscallback_offlineanalysiscomplete_dword_hresult_bstr"></span>IOfflineAnalysisCallback::OfflineAnalysisComplete method</span></span>

<span data-ttu-id="3d083-104">Funzione di callback utilizzata per notificare all'host che l'analisi offline è stata completata.</span><span class="sxs-lookup"><span data-stu-id="3d083-104">A callback function used to notify the host that offline analysis has completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d083-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3d083-105">Syntax</span></span>


```C++
HRESULT OfflineAnalysisComplete(
   DWORD   cookie,
   HRESULT result,
   BSTR    outputFullFileName
);
```

## <a name="parameters"></a><span data-ttu-id="3d083-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3d083-106">Parameters</span></span>

<span data-ttu-id="3d083-107">*cookie* </span><span class="sxs-lookup"><span data-stu-id="3d083-107">*cookie* </span></span>  
<span data-ttu-id="3d083-108">Cookie che identifica in modo univoco la richiesta che ha avviato l'analisi offline.</span><span class="sxs-lookup"><span data-stu-id="3d083-108">A cookie that uniquely identifies the request which initiated offline analysis.</span></span>

<span data-ttu-id="3d083-109">*risultato* </span><span class="sxs-lookup"><span data-stu-id="3d083-109">*result* </span></span>  
<span data-ttu-id="3d083-110">Indica se l'analisi offline ha avuto esito positivo o negativo.</span><span class="sxs-lookup"><span data-stu-id="3d083-110">Indicates whether offline analysis succeeded or failed.</span></span> <span data-ttu-id="3d083-111">In caso di esito positivo, i risultati sono stati scritti in un file.</span><span class="sxs-lookup"><span data-stu-id="3d083-111">If it succeeded, results were written to a file.</span></span>

<span data-ttu-id="3d083-112">*outputFullFileName* </span><span class="sxs-lookup"><span data-stu-id="3d083-112">*outputFullFileName* </span></span>  
<span data-ttu-id="3d083-113">Stringa COM che rappresenta il nome del file in cui sono stati scritti i risultati dell'analisi offline.</span><span class="sxs-lookup"><span data-stu-id="3d083-113">A COM string contianing the name of the file where offline analysis results were written.</span></span>

## <a name="return-value"></a><span data-ttu-id="3d083-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3d083-114">Return value</span></span>

<span data-ttu-id="3d083-115">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="3d083-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3d083-116">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3d083-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d083-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3d083-117">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="3d083-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3d083-118">Header</span></span></p></td><td><span data-ttu-id="3d083-119">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="3d083-119">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="3d083-120"><span id="see_also"></span>Vedere anche</span><span class="sxs-lookup"><span data-stu-id="3d083-120"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="3d083-121">**IOfflineAnalysisCallback**</span><span class="sxs-lookup"><span data-stu-id="3d083-121">**IOfflineAnalysisCallback**</span></span>](/windows/desktop/direct3dtools/iofflineanalysiscallback)

 

 
