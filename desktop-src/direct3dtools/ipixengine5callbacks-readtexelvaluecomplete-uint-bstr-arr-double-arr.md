---
description: Funzione di callback utilizzata per notificare all'host quando un valore di Texel letto è stato completato.
MS-HAID: vspixengine.IPixEngine5Callbacks\_ReadTexelValueComplete\_UINT\_BSTR\_arr\_double\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo IPixEngine5Callbacks:: ReadTexelValueComplete'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 3CAC08D8-0E4F-40B5-B91C-5C9159665C96
api_name:
- IPixEngine5Callbacks.ReadTexelValueComplete
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 7069d286cf65d87ba7bf4c576de3692b2a51d1a0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521898"
---
# <a name="span-idvspixengineipixengine5callbacks_readtexelvaluecomplete_uint_bstr_arr_double_arrspanipixengine5callbacksreadtexelvaluecomplete-method"></a><span data-ttu-id="728a0-103"><span id="vspixengine.ipixengine5callbacks_readtexelvaluecomplete_uint_bstr_arr_double_arr"></span>Metodo IPixEngine5Callbacks:: ReadTexelValueComplete</span><span class="sxs-lookup"><span data-stu-id="728a0-103"><span id="vspixengine.ipixengine5callbacks_readtexelvaluecomplete_uint_bstr_arr_double_arr"></span>IPixEngine5Callbacks::ReadTexelValueComplete method</span></span>

<span data-ttu-id="728a0-104">Funzione di callback utilizzata per notificare all'host quando un valore di Texel letto è stato completato.</span><span class="sxs-lookup"><span data-stu-id="728a0-104">A callback function used to notify the host when a texel value read has been completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="728a0-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="728a0-105">Syntax</span></span>


```C++
HRESULT ReadTexelValueComplete(
   UINT      numChannels,
   BSTR []   count0_channelNames,
   double [] count0_channelValues
);
```

## <a name="parameters"></a><span data-ttu-id="728a0-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="728a0-106">Parameters</span></span>

<span data-ttu-id="728a0-107">*numChannels* </span><span class="sxs-lookup"><span data-stu-id="728a0-107">*numChannels* </span></span>  
<span data-ttu-id="728a0-108">Il numero di canali del Texel.</span><span class="sxs-lookup"><span data-stu-id="728a0-108">The number of channels the texel has.</span></span>

<span data-ttu-id="728a0-109">*\_channelNames count0* </span><span class="sxs-lookup"><span data-stu-id="728a0-109">*count0\_channelNames* </span></span>  
<span data-ttu-id="728a0-110">Stringhe COM contenenti i nomi dei canali.</span><span class="sxs-lookup"><span data-stu-id="728a0-110">COM strings containing the names of the channels.</span></span>

<span data-ttu-id="728a0-111">*\_channelValues count0* </span><span class="sxs-lookup"><span data-stu-id="728a0-111">*count0\_channelValues* </span></span>  
<span data-ttu-id="728a0-112">Valori dei canali.</span><span class="sxs-lookup"><span data-stu-id="728a0-112">The values of the channels.</span></span>

## <a name="return-value"></a><span data-ttu-id="728a0-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="728a0-113">Return value</span></span>

<span data-ttu-id="728a0-114">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="728a0-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="728a0-115">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="728a0-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="728a0-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="728a0-116">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="728a0-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="728a0-117">Header</span></span></p></td><td><span data-ttu-id="728a0-118">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="728a0-118">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="728a0-119"><span id="see_also"></span>Vedere anche</span><span class="sxs-lookup"><span data-stu-id="728a0-119"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="728a0-120">**IPixEngine5Callbacks**</span><span class="sxs-lookup"><span data-stu-id="728a0-120">**IPixEngine5Callbacks**</span></span>](/windows/desktop/direct3dtools/ipixengine5callbacks)

 

 
