---
description: Callback che notifica all'host gli errori restituiti dalla richiesta associata.
MS-HAID: vspixengine.IPixErrorCallback\_ErrorListCallback\_DWORD\_Issue\_arr\_DWORD\_Issue\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo IPixErrorCallback:: ErrorListCallback'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: B345846D-4853-4F6B-AB79-42265720451D
api_name:
- IPixErrorCallback.ErrorListCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 91754cd7db13165efcb66e9bc87b8e4661842fce
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304300"
---
# <a name="span-idvspixengineipixerrorcallback_errorlistcallback_dword_issue_arr_dword_issue_arrspanipixerrorcallbackerrorlistcallback-method"></a><span data-ttu-id="34091-103"><span id="vspixengine.ipixerrorcallback_errorlistcallback_dword_issue_arr_dword_issue_arr"></span>Metodo IPixErrorCallback:: ErrorListCallback</span><span class="sxs-lookup"><span data-stu-id="34091-103"><span id="vspixengine.ipixerrorcallback_errorlistcallback_dword_issue_arr_dword_issue_arr"></span>IPixErrorCallback::ErrorListCallback method</span></span>

<span data-ttu-id="34091-104">Callback che notifica all'host gli errori restituiti dalla richiesta associata.</span><span class="sxs-lookup"><span data-stu-id="34091-104">A callback that notifies the host of errors returned by the associated request.</span></span>

## <a name="syntax"></a><span data-ttu-id="34091-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="34091-105">Syntax</span></span>


```C++
HRESULT ErrorListCallback(
   DWORD    count,
   Issue [] count0_errorList,
   DWORD    count,
   Issue [] count0_warningList
);
```

## <a name="parameters"></a><span data-ttu-id="34091-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="34091-106">Parameters</span></span>

<span data-ttu-id="34091-107">*conteggio* </span><span class="sxs-lookup"><span data-stu-id="34091-107">*count* </span></span>  
<span data-ttu-id="34091-108">Numero di errori.</span><span class="sxs-lookup"><span data-stu-id="34091-108">The number of errors.</span></span>

<span data-ttu-id="34091-109">*\_errore count0* </span><span class="sxs-lookup"><span data-stu-id="34091-109">*count0\_errorList* </span></span>  
<span data-ttu-id="34091-110">Errori.</span><span class="sxs-lookup"><span data-stu-id="34091-110">The errors.</span></span>

<span data-ttu-id="34091-111">*conteggio* </span><span class="sxs-lookup"><span data-stu-id="34091-111">*count* </span></span>  
<span data-ttu-id="34091-112">Numero di avvisi.</span><span class="sxs-lookup"><span data-stu-id="34091-112">The number of warningns.</span></span>

<span data-ttu-id="34091-113">*\_avviso count0* </span><span class="sxs-lookup"><span data-stu-id="34091-113">*count0\_warningList* </span></span>  
<span data-ttu-id="34091-114">Avvisi.</span><span class="sxs-lookup"><span data-stu-id="34091-114">The warnings.</span></span>

## <a name="return-value"></a><span data-ttu-id="34091-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="34091-115">Return value</span></span>

<span data-ttu-id="34091-116">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="34091-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="34091-117">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="34091-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="34091-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="34091-118">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="34091-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="34091-119">Header</span></span></p></td><td><span data-ttu-id="34091-120">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="34091-120">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="34091-121"><span id="see_also"></span>Vedere anche</span><span class="sxs-lookup"><span data-stu-id="34091-121"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="34091-122">**IPixErrorCallback**</span><span class="sxs-lookup"><span data-stu-id="34091-122">**IPixErrorCallback**</span></span>](/windows/desktop/direct3dtools/ipixerrorcallback)

 

 
