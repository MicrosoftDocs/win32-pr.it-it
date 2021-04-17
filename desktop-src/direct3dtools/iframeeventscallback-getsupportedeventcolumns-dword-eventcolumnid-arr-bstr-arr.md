---
description: Ottiene informazioni sulle colonne (tipi di dati dell'evento) supportate dall'elenco di eventi.
MS-HAID: vspixengine.IFrameEventsCallback\_GetSupportedEventColumns\_DWORD\_EventColumnID\_arr\_BSTR\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo IFrameEventsCallback:: GetSupportedEventColumns'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: F1BFF189-A22C-4058-A427-74653998DD27
api_name:
- IFrameEventsCallback.GetSupportedEventColumns
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e5b7bc9f74998a061ea63fca925263b7b4a0a4d8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481941"
---
# <a name="span-idvspixengineiframeeventscallback_getsupportedeventcolumns_dword_eventcolumnid_arr_bstr_arrspaniframeeventscallbackgetsupportedeventcolumns-method"></a><span data-ttu-id="a67d1-103"><span id="vspixengine.iframeeventscallback_getsupportedeventcolumns_dword_eventcolumnid_arr_bstr_arr"></span>Metodo IFrameEventsCallback:: GetSupportedEventColumns</span><span class="sxs-lookup"><span data-stu-id="a67d1-103"><span id="vspixengine.iframeeventscallback_getsupportedeventcolumns_dword_eventcolumnid_arr_bstr_arr"></span>IFrameEventsCallback::GetSupportedEventColumns method</span></span>

<span data-ttu-id="a67d1-104">Ottiene informazioni sulle colonne (tipi di dati dell'evento) supportate dall'elenco di eventi.</span><span class="sxs-lookup"><span data-stu-id="a67d1-104">Gets information about which columns (types of event data) are supported by the event list.</span></span>

## <a name="syntax"></a><span data-ttu-id="a67d1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a67d1-105">Syntax</span></span>


```C++
HRESULT GetSupportedEventColumns(
   DWORD            numColumns,
   EventColumnID [] count0_pIDs,
   BSTR []          count0_pBstrNames
);
```

## <a name="parameters"></a><span data-ttu-id="a67d1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a67d1-106">Parameters</span></span>

<span data-ttu-id="a67d1-107">*numColumns* </span><span class="sxs-lookup"><span data-stu-id="a67d1-107">*numColumns* </span></span>  
<span data-ttu-id="a67d1-108">Il numero di colonne supportate da</span><span class="sxs-lookup"><span data-stu-id="a67d1-108">The number of columns supported by</span></span>

<span data-ttu-id="a67d1-109">*count0 \_ PID* </span><span class="sxs-lookup"><span data-stu-id="a67d1-109">*count0\_pIDs* </span></span>  
<span data-ttu-id="a67d1-110">ID di ogni colonna supportata dall'elenco di eventi.</span><span class="sxs-lookup"><span data-stu-id="a67d1-110">The IDs of each column supported by the event list.</span></span>

<span data-ttu-id="a67d1-111">*\_pBstrNames count0* </span><span class="sxs-lookup"><span data-stu-id="a67d1-111">*count0\_pBstrNames* </span></span>  
<span data-ttu-id="a67d1-112">I nomi di ogni colonna, come stringa COM, supportati dall'elenco di eventi.</span><span class="sxs-lookup"><span data-stu-id="a67d1-112">The names of each column, as a COM string, supported by the event list.</span></span>

## <a name="return-value"></a><span data-ttu-id="a67d1-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a67d1-113">Return value</span></span>

<span data-ttu-id="a67d1-114">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="a67d1-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a67d1-115">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a67d1-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a67d1-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a67d1-116">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="a67d1-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a67d1-117">Header</span></span></p></td><td><span data-ttu-id="a67d1-118">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="a67d1-118">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="a67d1-119"><span id="see_also"></span>Vedere anche</span><span class="sxs-lookup"><span data-stu-id="a67d1-119"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="a67d1-120">**IFrameEventsCallback**</span><span class="sxs-lookup"><span data-stu-id="a67d1-120">**IFrameEventsCallback**</span></span>](/windows/desktop/direct3dtools/iframeeventscallback)

 

 
