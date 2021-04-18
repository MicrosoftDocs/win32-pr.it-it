---
description: Richieste di annullamento della generazione di istruzioni di traccia dello shader in una richiesta di debug.
MS-HAID: vspixengine.IDebugShaderCancel\_CancelGenerate\_DebugShaderRequestInfo\_ptr\_PixelHistoryOperation\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo IDebugShaderCancel:: CancelGenerate'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 10DA5080-3AA6-47AA-BFE7-774BC26C7F95
api_name:
- IDebugShaderCancel.CancelGenerate
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5c2754f0d390960775b11ac5da121d5e6a20705a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304036"
---
# <a name="span-idvspixengineidebugshadercancel_cancelgenerate_debugshaderrequestinfo_ptr_pixelhistoryoperation_ptrspanidebugshadercancelcancelgenerate-method"></a><span data-ttu-id="e198c-103"><span id="vspixengine.idebugshadercancel_cancelgenerate_debugshaderrequestinfo_ptr_pixelhistoryoperation_ptr"></span>Metodo IDebugShaderCancel:: CancelGenerate</span><span class="sxs-lookup"><span data-stu-id="e198c-103"><span id="vspixengine.idebugshadercancel_cancelgenerate_debugshaderrequestinfo_ptr_pixelhistoryoperation_ptr"></span>IDebugShaderCancel::CancelGenerate method</span></span>

<span data-ttu-id="e198c-104">Richieste di annullamento della generazione di istruzioni di traccia dello shader in una richiesta di debug.</span><span class="sxs-lookup"><span data-stu-id="e198c-104">Requests to cancel generation of shader trace instructions in a debug request.</span></span>

## <a name="syntax"></a><span data-ttu-id="e198c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e198c-105">Syntax</span></span>


```C++
HRESULT CancelGenerate(
   DebugShaderRequestInfo * requestInfo,
   PixelHistoryOperation *  pPixelHistory
);
```

## <a name="parameters"></a><span data-ttu-id="e198c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e198c-106">Parameters</span></span>

<span data-ttu-id="e198c-107">*requestInfo* </span><span class="sxs-lookup"><span data-stu-id="e198c-107">*requestInfo* </span></span>  
<span data-ttu-id="e198c-108">Indirizzo di una struttura DebugShaderRequestInfo che descrive l'evento/vertice/pixel richiesto.</span><span class="sxs-lookup"><span data-stu-id="e198c-108">The address of a DebugShaderRequestInfo structure that describes the requested event/vertex/pixel.</span></span>

<span data-ttu-id="e198c-109">*pPixelHistory* </span><span class="sxs-lookup"><span data-stu-id="e198c-109">*pPixelHistory* </span></span>  
<span data-ttu-id="e198c-110">Indirizzo dei risultati della Cronologia pixel utilizzati per trovare il pixel associato di cui eseguire il debug.</span><span class="sxs-lookup"><span data-stu-id="e198c-110">The address of pixel history results used for finding the associated pixel to debug.</span></span> <span data-ttu-id="e198c-111">Si applica solo quando si esegue il debug di un pixel shader.</span><span class="sxs-lookup"><span data-stu-id="e198c-111">Only applies when debugging a pixel shader.</span></span>

## <a name="return-value"></a><span data-ttu-id="e198c-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e198c-112">Return value</span></span>

<span data-ttu-id="e198c-113">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="e198c-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e198c-114">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e198c-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="e198c-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e198c-115">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="e198c-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e198c-116">Header</span></span></p></td><td><span data-ttu-id="e198c-117">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="e198c-117">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="e198c-118"><span id="see_also"></span>Vedere anche</span><span class="sxs-lookup"><span data-stu-id="e198c-118"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="e198c-119">**IDebugShaderCancel**</span><span class="sxs-lookup"><span data-stu-id="e198c-119">**IDebugShaderCancel**</span></span>](/windows/desktop/direct3dtools/idebugshadercancel)

 

 
