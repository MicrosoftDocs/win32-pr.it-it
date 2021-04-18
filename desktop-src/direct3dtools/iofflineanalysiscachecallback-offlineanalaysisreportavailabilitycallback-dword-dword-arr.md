---
description: Funzione di callback utilizzata per notificare all'host i frame con report di analisi offline disponibili.
MS-HAID: vspixengine.IOfflineAnalysisCacheCallback\_OfflineAnalaysisReportAvailabilityCallback\_DWORD\_DWORD\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo IOfflineAnalysisCacheCallback:: OfflineAnalaysisReportAvailabilityCallback'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 2061EB62-4CBD-4668-BFCD-6E43014BB406
api_name:
- IOfflineAnalysisCacheCallback.OfflineAnalaysisReportAvailabilityCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: adbffbeb79aaf648c3319cf572dcbc905e9fd307
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304346"
---
# <a name="span-idvspixengineiofflineanalysiscachecallback_offlineanalaysisreportavailabilitycallback_dword_dword_arrspaniofflineanalysiscachecallbackofflineanalaysisreportavailabilitycallback-method"></a><span data-ttu-id="03b56-103"><span id="vspixengine.iofflineanalysiscachecallback_offlineanalaysisreportavailabilitycallback_dword_dword_arr"></span>Metodo IOfflineAnalysisCacheCallback:: OfflineAnalaysisReportAvailabilityCallback</span><span class="sxs-lookup"><span data-stu-id="03b56-103"><span id="vspixengine.iofflineanalysiscachecallback_offlineanalaysisreportavailabilitycallback_dword_dword_arr"></span>IOfflineAnalysisCacheCallback::OfflineAnalaysisReportAvailabilityCallback method</span></span>

<span data-ttu-id="03b56-104">Funzione di callback utilizzata per notificare all'host i frame con report di analisi offline disponibili.</span><span class="sxs-lookup"><span data-stu-id="03b56-104">A callback function used to notify the host about which frames have offline analysis reports available.</span></span>

## <a name="syntax"></a><span data-ttu-id="03b56-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="03b56-105">Syntax</span></span>


```C++
HRESULT OfflineAnalaysisReportAvailabilityCallback(
   DWORD    numFramesWithReports,
   DWORD [] count0_framesWithReports
);
```

## <a name="parameters"></a><span data-ttu-id="03b56-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="03b56-106">Parameters</span></span>

<span data-ttu-id="03b56-107">*numFramesWithReports* </span><span class="sxs-lookup"><span data-stu-id="03b56-107">*numFramesWithReports* </span></span>  
<span data-ttu-id="03b56-108">Numero di frame in count0 \_ framesWithReports.</span><span class="sxs-lookup"><span data-stu-id="03b56-108">The number of frames in count0\_framesWithReports.</span></span>

<span data-ttu-id="03b56-109">*\_framesWithReports count0* </span><span class="sxs-lookup"><span data-stu-id="03b56-109">*count0\_framesWithReports* </span></span>  
<span data-ttu-id="03b56-110">Matrice contenente i numeri di frame dei frame con report di analisi offline disponibili.</span><span class="sxs-lookup"><span data-stu-id="03b56-110">An array containing the frame numbers of the frames that have offline analysis reports available.</span></span>

## <a name="return-value"></a><span data-ttu-id="03b56-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="03b56-111">Return value</span></span>

<span data-ttu-id="03b56-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="03b56-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="03b56-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="03b56-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="03b56-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="03b56-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="03b56-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="03b56-115">Header</span></span></p></td><td><span data-ttu-id="03b56-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="03b56-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="03b56-117"><span id="see_also"></span>Vedere anche</span><span class="sxs-lookup"><span data-stu-id="03b56-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="03b56-118">**IOfflineAnalysisCacheCallback**</span><span class="sxs-lookup"><span data-stu-id="03b56-118">**IOfflineAnalysisCacheCallback**</span></span>](/windows/desktop/direct3dtools/iofflineanalysiscachecallback)

 

 
