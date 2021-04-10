---
description: Callback utilizzato per notificare all'host che un oggetto è stato aggiornato.
MS-HAID: vspixengine.IUpdateObjectCallback\_UpdateComplete\_UINT\_HRESULT
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo IUpdateObjectCallback:: UpdateComplete'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 7F54DDEC-E595-4615-B9B7-B1213A58B362
api_name:
- IUpdateObjectCallback.UpdateComplete
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: b601d8ac785f65c4400821741b83e76bd6987481
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124695"
---
# <a name="span-idvspixengineiupdateobjectcallback_updatecomplete_uint_hresultspaniupdateobjectcallbackupdatecomplete-method"></a><span data-ttu-id="fb2c5-103"><span id="vspixengine.iupdateobjectcallback_updatecomplete_uint_hresult"></span>Metodo IUpdateObjectCallback:: UpdateComplete</span><span class="sxs-lookup"><span data-stu-id="fb2c5-103"><span id="vspixengine.iupdateobjectcallback_updatecomplete_uint_hresult"></span>IUpdateObjectCallback::UpdateComplete method</span></span>

<span data-ttu-id="fb2c5-104">Callback utilizzato per notificare all'host che un oggetto è stato aggiornato.</span><span class="sxs-lookup"><span data-stu-id="fb2c5-104">A callback used to notify the host that an object was updated.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb2c5-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fb2c5-105">Syntax</span></span>


```C++
HRESULT UpdateComplete(
   UINT    objectAddress,
   HRESULT result
);
```

## <a name="parameters"></a><span data-ttu-id="fb2c5-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="fb2c5-106">Parameters</span></span>

<span data-ttu-id="fb2c5-107">*objectAddress* </span><span class="sxs-lookup"><span data-stu-id="fb2c5-107">*objectAddress* </span></span>  
<span data-ttu-id="fb2c5-108">ID dell'oggetto che è stato aggiornato.</span><span class="sxs-lookup"><span data-stu-id="fb2c5-108">The ID of the object that was updated.</span></span>

<span data-ttu-id="fb2c5-109">*risultato* </span><span class="sxs-lookup"><span data-stu-id="fb2c5-109">*result* </span></span>  
<span data-ttu-id="fb2c5-110">Indica se l'aggiornamento è stato completato o meno.</span><span class="sxs-lookup"><span data-stu-id="fb2c5-110">Indicates whether or not the update succeeded.</span></span>

## <a name="return-value"></a><span data-ttu-id="fb2c5-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fb2c5-111">Return value</span></span>

<span data-ttu-id="fb2c5-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="fb2c5-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="fb2c5-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="fb2c5-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb2c5-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fb2c5-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="fb2c5-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fb2c5-115">Header</span></span></p></td><td><span data-ttu-id="fb2c5-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="fb2c5-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="fb2c5-117"><span id="see_also"></span>Vedere anche</span><span class="sxs-lookup"><span data-stu-id="fb2c5-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="fb2c5-118">**IUpdateObjectCallback**</span><span class="sxs-lookup"><span data-stu-id="fb2c5-118">**IUpdateObjectCallback**</span></span>](/windows/desktop/direct3dtools/iupdateobjectcallback)

 

 
