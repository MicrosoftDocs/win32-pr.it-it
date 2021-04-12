---
description: Funzione di callback utilizzata per notificare all'host le informazioni sugli eventi nell'elenco degli eventi.
MS-HAID: vspixengine.IFrameEventsCallback\_ResultCallback\_DWORD\_DWORD\_DWORD\_DWORD\_VARIANT\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo IFrameEventsCallback:: ResultCallback'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5AB67A11-00C1-47AF-8C8C-8B2FDD095BCF
api_name:
- IFrameEventsCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e746c54f2a82adb5042cd479e4ca04299c1b7402
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104225413"
---
# <a name="span-idvspixengineiframeeventscallback_resultcallback_dword_dword_dword_dword_variant_arrspaniframeeventscallbackresultcallback-method"></a><span data-ttu-id="da308-103"><span id="vspixengine.iframeeventscallback_resultcallback_dword_dword_dword_dword_variant_arr"></span>Metodo IFrameEventsCallback:: ResultCallback</span><span class="sxs-lookup"><span data-stu-id="da308-103"><span id="vspixengine.iframeeventscallback_resultcallback_dword_dword_dword_dword_variant_arr"></span>IFrameEventsCallback::ResultCallback method</span></span>

<span data-ttu-id="da308-104">Funzione di callback utilizzata per notificare all'host le informazioni sugli eventi nell'elenco degli eventi.</span><span class="sxs-lookup"><span data-stu-id="da308-104">A callback function used to notify the host of information about events in the event list.</span></span>

## <a name="syntax"></a><span data-ttu-id="da308-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="da308-105">Syntax</span></span>


```C++
HRESULT ResultCallback(
   DWORD      frameNumber,
   DWORD      numElements,
   DWORD      numRows,
   DWORD      numColumns,
   VARIANT [] count1_pRowData
);
```

## <a name="parameters"></a><span data-ttu-id="da308-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="da308-106">Parameters</span></span>

<span data-ttu-id="da308-107">*NumeroFrame* </span><span class="sxs-lookup"><span data-stu-id="da308-107">*frameNumber* </span></span>  
<span data-ttu-id="da308-108">Numero di frame associato agli eventi.</span><span class="sxs-lookup"><span data-stu-id="da308-108">The frame number associated with the events.</span></span>

<span data-ttu-id="da308-109">*numElements* </span><span class="sxs-lookup"><span data-stu-id="da308-109">*numElements* </span></span>  
<span data-ttu-id="da308-110">Numero totale di campi in tutte le colonne di tutti gli eventi.</span><span class="sxs-lookup"><span data-stu-id="da308-110">The total number of fields in all columns of all events.</span></span>

<span data-ttu-id="da308-111">*numRows* </span><span class="sxs-lookup"><span data-stu-id="da308-111">*numRows* </span></span>  
<span data-ttu-id="da308-112">Il numero di eventi nel risultato.</span><span class="sxs-lookup"><span data-stu-id="da308-112">The number of events in the result.</span></span>

<span data-ttu-id="da308-113">*numColumns* </span><span class="sxs-lookup"><span data-stu-id="da308-113">*numColumns* </span></span>  
<span data-ttu-id="da308-114">Numero di colonne (campi) in ogni riga.</span><span class="sxs-lookup"><span data-stu-id="da308-114">The number of columns (fields) in each row.</span></span>

<span data-ttu-id="da308-115">*\_pRowData count1* </span><span class="sxs-lookup"><span data-stu-id="da308-115">*count1\_pRowData* </span></span>  
<span data-ttu-id="da308-116">Informazioni sugli eventi; un elemento per ogni campo di ogni evento.</span><span class="sxs-lookup"><span data-stu-id="da308-116">Information about the events; one item for each field of each event.</span></span>

## <a name="return-value"></a><span data-ttu-id="da308-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="da308-117">Return value</span></span>

<span data-ttu-id="da308-118">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="da308-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="da308-119">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="da308-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="da308-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="da308-120">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="da308-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="da308-121">Header</span></span></p></td><td><span data-ttu-id="da308-122">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="da308-122">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="da308-123"><span id="see_also"></span>Vedere anche</span><span class="sxs-lookup"><span data-stu-id="da308-123"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="da308-124">**IFrameEventsCallback**</span><span class="sxs-lookup"><span data-stu-id="da308-124">**IFrameEventsCallback**</span></span>](/windows/desktop/direct3dtools/iframeeventscallback)

 

 
