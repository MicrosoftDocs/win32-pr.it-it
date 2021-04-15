---
description: Termina il experiement e completa il log di grafica.
MS-HAID: vspixengine.IPixEngine2\_EndExperiment\_BSTR\_IFileIOCallback\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo IPixEngine2:: EndExperiment'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 0260F337-B279-4FE6-92F3-FCF70C2B8980
api_name:
- IPixEngine2.EndExperiment
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2638c75269f93e50fd1f9e4b6938b123cbd01e60
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521538"
---
# <a name="span-idvspixengineipixengine2_endexperiment_bstr_ifileiocallback_ptrspanipixengine2endexperiment-method"></a><span data-ttu-id="e082f-103"><span id="vspixengine.ipixengine2_endexperiment_bstr_ifileiocallback_ptr"></span>Metodo IPixEngine2:: EndExperiment</span><span class="sxs-lookup"><span data-stu-id="e082f-103"><span id="vspixengine.ipixengine2_endexperiment_bstr_ifileiocallback_ptr"></span>IPixEngine2::EndExperiment method</span></span>

<span data-ttu-id="e082f-104">Termina il experiement e completa il log di grafica.</span><span class="sxs-lookup"><span data-stu-id="e082f-104">Ends the experiement and completes the graphics log.</span></span>

## <a name="syntax"></a><span data-ttu-id="e082f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e082f-105">Syntax</span></span>


```C++
HRESULT EndExperiment(
   BSTR              logFile,
   IFileIOCallback * pCallback
);
```

## <a name="parameters"></a><span data-ttu-id="e082f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e082f-106">Parameters</span></span>

<span data-ttu-id="e082f-107">*logFile* </span><span class="sxs-lookup"><span data-stu-id="e082f-107">*logFile* </span></span>  
<span data-ttu-id="e082f-108">Stringa COM contenente il nome del log di grafica.</span><span class="sxs-lookup"><span data-stu-id="e082f-108">A COM string containing the name of the graphics log.</span></span>

<span data-ttu-id="e082f-109">*pCallback* </span><span class="sxs-lookup"><span data-stu-id="e082f-109">*pCallback* </span></span>  
<span data-ttu-id="e082f-110">Indirizzo di un callback utilizzato per indicare che il experiement è terminato.</span><span class="sxs-lookup"><span data-stu-id="e082f-110">The address of a callback used to indicate that the experiement is ended.</span></span>

## <a name="return-value"></a><span data-ttu-id="e082f-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e082f-111">Return value</span></span>

<span data-ttu-id="e082f-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="e082f-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e082f-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e082f-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="e082f-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e082f-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="e082f-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e082f-115">Header</span></span></p></td><td><span data-ttu-id="e082f-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="e082f-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="e082f-117"><span id="see_also"></span>Vedere anche</span><span class="sxs-lookup"><span data-stu-id="e082f-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="e082f-118">**IPixEngine2**</span><span class="sxs-lookup"><span data-stu-id="e082f-118">**IPixEngine2**</span></span>](/windows/desktop/direct3dtools/ipixengine2)

 

 
