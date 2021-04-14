---
description: Callback che notifica all'host il numero di thread e gruppi del compute shader nella richiesta associata.
MS-HAID: vspixengine.IPipeLineStagesCallback2\_ThreadDataDimensionCallback\_ThreadData3D\_ThreadData3D
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo IPipeLineStagesCallback2:: ThreadDataDimensionCallback'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: E8765C14-0A55-468D-BCA8-3E28E5476DFB
api_name:
- IPipeLineStagesCallback2.ThreadDataDimensionCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 93a8ee64c863128513563f3ce50dd2bfcdd77714
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401309"
---
# <a name="span-idvspixengineipipelinestagescallback2_threaddatadimensioncallback_threaddata3d_threaddata3dspanipipelinestagescallback2threaddatadimensioncallback-method"></a><span data-ttu-id="403ff-103"><span id="vspixengine.ipipelinestagescallback2_threaddatadimensioncallback_threaddata3d_threaddata3d"></span>Metodo IPipeLineStagesCallback2:: ThreadDataDimensionCallback</span><span class="sxs-lookup"><span data-stu-id="403ff-103"><span id="vspixengine.ipipelinestagescallback2_threaddatadimensioncallback_threaddata3d_threaddata3d"></span>IPipeLineStagesCallback2::ThreadDataDimensionCallback method</span></span>

<span data-ttu-id="403ff-104">Callback che notifica all'host il numero di thread e gruppi del compute shader nella richiesta associata.</span><span class="sxs-lookup"><span data-stu-id="403ff-104">A callback that notifies the host of the number of threads and groups of the compute shader in the associated request.</span></span>

## <a name="syntax"></a><span data-ttu-id="403ff-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="403ff-105">Syntax</span></span>


```C++
HRESULT ThreadDataDimensionCallback(
   ThreadData3D threadGroupCount,
   ThreadData3D threadGroupSize
);
```

## <a name="parameters"></a><span data-ttu-id="403ff-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="403ff-106">Parameters</span></span>

<span data-ttu-id="403ff-107">*threadGroupCount* </span><span class="sxs-lookup"><span data-stu-id="403ff-107">*threadGroupCount* </span></span>  
<span data-ttu-id="403ff-108">Conteggio multidimensionali dei gruppi di thread.</span><span class="sxs-lookup"><span data-stu-id="403ff-108">The multi-dimensional count of thread groups.</span></span>

<span data-ttu-id="403ff-109">*threadGroupSize* </span><span class="sxs-lookup"><span data-stu-id="403ff-109">*threadGroupSize* </span></span>  
<span data-ttu-id="403ff-110">Dimensioni multidimensionali di ogni gruppo di thread.</span><span class="sxs-lookup"><span data-stu-id="403ff-110">The multi-dimensional size of each thread group.</span></span>

## <a name="return-value"></a><span data-ttu-id="403ff-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="403ff-111">Return value</span></span>

<span data-ttu-id="403ff-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="403ff-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="403ff-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="403ff-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="403ff-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="403ff-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="403ff-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="403ff-115">Header</span></span></p></td><td><span data-ttu-id="403ff-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="403ff-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="403ff-117"><span id="see_also"></span>Vedere anche</span><span class="sxs-lookup"><span data-stu-id="403ff-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="403ff-118">**IPipeLineStagesCallback2**</span><span class="sxs-lookup"><span data-stu-id="403ff-118">**IPipeLineStagesCallback2**</span></span>](/windows/desktop/direct3dtools/ipipelinestagescallback2)

 

 
