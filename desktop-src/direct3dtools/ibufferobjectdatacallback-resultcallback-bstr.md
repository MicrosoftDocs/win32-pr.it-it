---
description: Callback che notifica all'host le informazioni del buffer scritte in un file dalla richiesta associata.
MS-HAID: vspixengine.IBufferObjectDataCallback\_ResultCallback\_BSTR
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo IBufferObjectDataCallback:: ResultCallback'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: C8083FDF-0A56-4777-8EFD-66F77AD195EA
api_name:
- IBufferObjectDataCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 41a5017171fee8476033e3c38d050bc38b1642a5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401336"
---
# <a name="span-idvspixengineibufferobjectdatacallback_resultcallback_bstrspanibufferobjectdatacallbackresultcallback-method"></a><span data-ttu-id="a70b1-103"><span id="vspixengine.ibufferobjectdatacallback_resultcallback_bstr"></span>Metodo IBufferObjectDataCallback:: ResultCallback</span><span class="sxs-lookup"><span data-stu-id="a70b1-103"><span id="vspixengine.ibufferobjectdatacallback_resultcallback_bstr"></span>IBufferObjectDataCallback::ResultCallback method</span></span>

<span data-ttu-id="a70b1-104">Callback che notifica all'host le informazioni del buffer scritte in un file dalla richiesta associata.</span><span class="sxs-lookup"><span data-stu-id="a70b1-104">A callback that notifies the host of buffer information written to a file by the assocaited request.</span></span>

## <a name="syntax"></a><span data-ttu-id="a70b1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a70b1-105">Syntax</span></span>

```C++
HRESULT ResultCallback(
   BSTR File
);
```

## <a name="parameters"></a><span data-ttu-id="a70b1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a70b1-106">Parameters</span></span>

<span data-ttu-id="a70b1-107">*File* Stringa COM che contiene il percorso del file in cui vengono scritti i risultati.</span><span class="sxs-lookup"><span data-stu-id="a70b1-107">*File* A COM string that contains the pathname of the file where results are written.</span></span>

## <a name="return-value"></a><span data-ttu-id="a70b1-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a70b1-108">Return value</span></span>

<span data-ttu-id="a70b1-109">Se questo metodo ha esito positivo, restituisce **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="a70b1-109">If this method succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="a70b1-110">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a70b1-110">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a70b1-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a70b1-111">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="a70b1-112">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a70b1-112">Header</span></span></p></td><td><span data-ttu-id="a70b1-113">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="a70b1-113">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="a70b1-114"><span id="see_also"></span>Vedere anche</span><span class="sxs-lookup"><span data-stu-id="a70b1-114"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="a70b1-115">**IBufferObjectDataCallback**</span><span class="sxs-lookup"><span data-stu-id="a70b1-115">**IBufferObjectDataCallback**</span></span>](/windows/desktop/direct3dtools/ibufferobjectdatacallback)

 

 
