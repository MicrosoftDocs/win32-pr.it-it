---
description: Funzione di callback utilizzata per notificare all'host le informazioni di riepilogo del log di grafica.
MS-HAID: vspixengine.ISummaryCallback\_ResultCallback\_DWORD\_SummaryItem\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo ISummaryCallback:: ResultCallback'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 07569D26-45A6-41A5-868D-8038BAB9079B
api_name:
- ISummaryCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c4ea46550628ec9701ab6b0e6bb3af9ab71a2499
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304292"
---
# <a name="span-idvspixengineisummarycallback_resultcallback_dword_summaryitem_arrspanisummarycallbackresultcallback-method"></a><span data-ttu-id="12532-103"><span id="vspixengine.isummarycallback_resultcallback_dword_summaryitem_arr"></span>Metodo ISummaryCallback:: ResultCallback</span><span class="sxs-lookup"><span data-stu-id="12532-103"><span id="vspixengine.isummarycallback_resultcallback_dword_summaryitem_arr"></span>ISummaryCallback::ResultCallback method</span></span>

<span data-ttu-id="12532-104">Funzione di callback utilizzata per notificare all'host le informazioni di riepilogo del log di grafica.</span><span class="sxs-lookup"><span data-stu-id="12532-104">A callback function used to notify the host of graphics log summary information.</span></span>

## <a name="syntax"></a><span data-ttu-id="12532-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="12532-105">Syntax</span></span>


```C++
HRESULT ResultCallback(
   DWORD          count,
   SummaryItem [] count0_summaryItem
);
```

## <a name="parameters"></a><span data-ttu-id="12532-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="12532-106">Parameters</span></span>

<span data-ttu-id="12532-107">*conteggio* </span><span class="sxs-lookup"><span data-stu-id="12532-107">*count* </span></span>  
<span data-ttu-id="12532-108">Numero di elementi di informazioni di riepilogo restituiti.</span><span class="sxs-lookup"><span data-stu-id="12532-108">The number of summary information items returned.</span></span>

<span data-ttu-id="12532-109">*\_summaryItem count0* </span><span class="sxs-lookup"><span data-stu-id="12532-109">*count0\_summaryItem* </span></span>  
<span data-ttu-id="12532-110">Elementi di informazioni di riepilogo (coppie chiave-valore).</span><span class="sxs-lookup"><span data-stu-id="12532-110">The summary information items (key-value pairs).</span></span>

## <a name="return-value"></a><span data-ttu-id="12532-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="12532-111">Return value</span></span>

<span data-ttu-id="12532-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="12532-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="12532-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="12532-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="12532-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="12532-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="12532-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="12532-115">Header</span></span></p></td><td><span data-ttu-id="12532-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="12532-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="12532-117"><span id="see_also"></span>Vedere anche</span><span class="sxs-lookup"><span data-stu-id="12532-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="12532-118">**ISummaryCallback**</span><span class="sxs-lookup"><span data-stu-id="12532-118">**ISummaryCallback**</span></span>](/windows/desktop/direct3dtools/isummarycallback)

 

 
