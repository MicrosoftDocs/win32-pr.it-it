---
description: Callback che notifica all'host lo stato di avanzamento di una richiesta associata.
MS-HAID: vspixengine.IPixProgressCallback\_Progress\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPixProgressCallback::P metodo rogress
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: BE74599B-C98F-4BDB-ACDF-641F77A35EEB
api_name:
- IPixProgressCallback.Progress
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 0379ad6fcb5f97825469c97af38453e55585d005
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401229"
---
# <a name="span-idvspixengineipixprogresscallback_progress_dword_dwordspanipixprogresscallbackprogress-method"></a><span data-ttu-id="ec715-103"><span id="vspixengine.ipixprogresscallback_progress_dword_dword"></span>IPixProgressCallback::P metodo rogress</span><span class="sxs-lookup"><span data-stu-id="ec715-103"><span id="vspixengine.ipixprogresscallback_progress_dword_dword"></span>IPixProgressCallback::Progress method</span></span>

<span data-ttu-id="ec715-104">Callback che notifica all'host lo stato di avanzamento di una richiesta associata.</span><span class="sxs-lookup"><span data-stu-id="ec715-104">A callback that notifies the host of the progress of an associated request.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec715-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ec715-105">Syntax</span></span>


```C++
HRESULT Progress(
   DWORD current,
   DWORD maxSize
);
```

## <a name="parameters"></a><span data-ttu-id="ec715-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ec715-106">Parameters</span></span>

<span data-ttu-id="ec715-107">*corrente* </span><span class="sxs-lookup"><span data-stu-id="ec715-107">*current* </span></span>  
<span data-ttu-id="ec715-108">Parte di una richiesta completata, come conteggio del numero di passaggi completati.</span><span class="sxs-lookup"><span data-stu-id="ec715-108">The portion of a request completed, as a count of the number of steps completed.</span></span>

<span data-ttu-id="ec715-109">*maxSize* </span><span class="sxs-lookup"><span data-stu-id="ec715-109">*maxSize* </span></span>  
<span data-ttu-id="ec715-110">Il numero totale di passaggi per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="ec715-110">The total number of steps to complete the request.</span></span>

## <a name="return-value"></a><span data-ttu-id="ec715-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ec715-111">Return value</span></span>

<span data-ttu-id="ec715-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="ec715-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ec715-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ec715-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec715-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ec715-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="ec715-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ec715-115">Header</span></span></p></td><td><span data-ttu-id="ec715-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="ec715-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="ec715-117"><span id="see_also"></span>Vedere anche</span><span class="sxs-lookup"><span data-stu-id="ec715-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="ec715-118">**IPixProgressCallback**</span><span class="sxs-lookup"><span data-stu-id="ec715-118">**IPixProgressCallback**</span></span>](/windows/desktop/direct3dtools/ipixprogresscallback)

 

 
