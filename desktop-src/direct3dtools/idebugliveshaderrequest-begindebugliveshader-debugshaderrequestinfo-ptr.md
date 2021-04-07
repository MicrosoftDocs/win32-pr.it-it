---
description: Richieste di eseguire il debug di uno shader sulla GPU (debug in tempo reale) rispetto alla CPU (debug basato su traccia).
MS-HAID: vspixengine.IDebugLiveShaderRequest\_BeginDebugLiveShader\_DebugShaderRequestInfo\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo IDebugLiveShaderRequest:: BeginDebugLiveShader'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 805B2B68-C251-4192-85A3-F857B3F204C7
api_name:
- IDebugLiveShaderRequest.BeginDebugLiveShader
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2b09bff6a414df620e06263e13d94c2f39e36903
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746751"
---
# <a name="span-idvspixengineidebugliveshaderrequest_begindebugliveshader_debugshaderrequestinfo_ptrspanidebugliveshaderrequestbegindebugliveshader-method"></a><span data-ttu-id="380fa-103"><span id="vspixengine.idebugliveshaderrequest_begindebugliveshader_debugshaderrequestinfo_ptr"></span>Metodo IDebugLiveShaderRequest:: BeginDebugLiveShader</span><span class="sxs-lookup"><span data-stu-id="380fa-103"><span id="vspixengine.idebugliveshaderrequest_begindebugliveshader_debugshaderrequestinfo_ptr"></span>IDebugLiveShaderRequest::BeginDebugLiveShader method</span></span>

<span data-ttu-id="380fa-104">Richieste di eseguire il debug di uno shader sulla GPU (debug in tempo reale) rispetto alla CPU (debug basato su traccia).</span><span class="sxs-lookup"><span data-stu-id="380fa-104">Requests to debug a shader on the GPU (live debugging) vs CPU (trace-based debugging).</span></span>

## <a name="syntax"></a><span data-ttu-id="380fa-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="380fa-105">Syntax</span></span>


```C++
HRESULT BeginDebugLiveShader(
   DebugShaderRequestInfo * requestInfo
);
```

## <a name="parameters"></a><span data-ttu-id="380fa-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="380fa-106">Parameters</span></span>

<span data-ttu-id="380fa-107">*requestInfo* </span><span class="sxs-lookup"><span data-stu-id="380fa-107">*requestInfo* </span></span>  
<span data-ttu-id="380fa-108">Indirizzo di una struttura DebugShaderRequestInfo che descrive l'evento/vertice/pixel richiesto.</span><span class="sxs-lookup"><span data-stu-id="380fa-108">The address of a DebugShaderRequestInfo structure that describes the requested event/vertex/pixel.</span></span>

## <a name="return-value"></a><span data-ttu-id="380fa-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="380fa-109">Return value</span></span>

<span data-ttu-id="380fa-110">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="380fa-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="380fa-111">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="380fa-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="380fa-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="380fa-112">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="380fa-113">Intestazione</span><span class="sxs-lookup"><span data-stu-id="380fa-113">Header</span></span></p></td><td><span data-ttu-id="380fa-114">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="380fa-114">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="380fa-115"><span id="see_also"></span>Vedere anche</span><span class="sxs-lookup"><span data-stu-id="380fa-115"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="380fa-116">**IDebugLiveShaderRequest**</span><span class="sxs-lookup"><span data-stu-id="380fa-116">**IDebugLiveShaderRequest**</span></span>](/windows/desktop/direct3dtools/idebugliveshaderrequest)

 

 
