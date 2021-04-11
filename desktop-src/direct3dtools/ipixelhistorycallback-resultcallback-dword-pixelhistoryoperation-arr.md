---
description: Callback che notifica all'host i risultati della richiesta di Cronologia pixel.
MS-HAID: vspixengine.IPixelHistoryCallback\_ResultCallback\_DWORD\_PixelHistoryOperation\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo IPixelHistoryCallback:: ResultCallback'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 1F7D0EA5-402A-49C4-A83E-91596AE9536B
api_name:
- IPixelHistoryCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c43947148e2eb8139f3ad46157f19b1621a6c91e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104341976"
---
# <a name="span-idvspixengineipixelhistorycallback_resultcallback_dword_pixelhistoryoperation_arrspanipixelhistorycallbackresultcallback-method"></a><span data-ttu-id="007ae-103"><span id="vspixengine.ipixelhistorycallback_resultcallback_dword_pixelhistoryoperation_arr"></span>Metodo IPixelHistoryCallback:: ResultCallback</span><span class="sxs-lookup"><span data-stu-id="007ae-103"><span id="vspixengine.ipixelhistorycallback_resultcallback_dword_pixelhistoryoperation_arr"></span>IPixelHistoryCallback::ResultCallback method</span></span>

<span data-ttu-id="007ae-104">Callback che notifica all'host i risultati della richiesta di Cronologia pixel.</span><span class="sxs-lookup"><span data-stu-id="007ae-104">A callback that notifies the host of pixel history request results.</span></span>

## <a name="syntax"></a><span data-ttu-id="007ae-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="007ae-105">Syntax</span></span>


```C++
HRESULT ResultCallback(
   DWORD                    count,
   PixelHistoryOperation [] count0_pixelHistoryOperation
);
```

## <a name="parameters"></a><span data-ttu-id="007ae-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="007ae-106">Parameters</span></span>

<span data-ttu-id="007ae-107">*conteggio* </span><span class="sxs-lookup"><span data-stu-id="007ae-107">*count* </span></span>  
<span data-ttu-id="007ae-108">Numero di risultati.</span><span class="sxs-lookup"><span data-stu-id="007ae-108">The number of results.</span></span>

<span data-ttu-id="007ae-109">*\_pixelHistoryOperation count0* </span><span class="sxs-lookup"><span data-stu-id="007ae-109">*count0\_pixelHistoryOperation* </span></span>  
<span data-ttu-id="007ae-110">Risultati.</span><span class="sxs-lookup"><span data-stu-id="007ae-110">The results.</span></span>

## <a name="return-value"></a><span data-ttu-id="007ae-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="007ae-111">Return value</span></span>

<span data-ttu-id="007ae-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="007ae-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="007ae-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="007ae-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="007ae-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="007ae-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="007ae-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="007ae-115">Header</span></span></p></td><td><span data-ttu-id="007ae-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="007ae-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="007ae-117"><span id="see_also"></span>Vedere anche</span><span class="sxs-lookup"><span data-stu-id="007ae-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="007ae-118">**IPixelHistoryCallback**</span><span class="sxs-lookup"><span data-stu-id="007ae-118">**IPixelHistoryCallback**</span></span>](/windows/desktop/direct3dtools/ipixelhistorycallback)

 

 
