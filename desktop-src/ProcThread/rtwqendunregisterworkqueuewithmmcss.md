---
description: Completa una richiesta asincrona per annullare la registrazione di una coda di lavoro con un'attività di servizio Utilità di pianificazione classi multimediali (MMCSS).
ms.assetid: 0E8F9BF6-AC1E-4FC0-BFAE-F292C4859F1F
title: RtwqEndUnregisterWorkQueueWithMMCSS (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtwqEndUnregisterWorkQueueWithMMCSS
api_type:
- DllExport
api_location:
- RTWorkQ.dll
ms.openlocfilehash: b55386b2a018b0e311a1d4dbb2084b136d49c2f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882381"
---
# <a name="rtwqendunregisterworkqueuewithmmcss-function"></a><span data-ttu-id="2f650-103">RtwqEndUnregisterWorkQueueWithMMCSS (funzione)</span><span class="sxs-lookup"><span data-stu-id="2f650-103">RtwqEndUnregisterWorkQueueWithMMCSS function</span></span>

<span data-ttu-id="2f650-104">Completa una richiesta asincrona per annullare la registrazione di una coda di lavoro con un'attività di servizio Utilità di pianificazione classi multimediali (MMCSS).</span><span class="sxs-lookup"><span data-stu-id="2f650-104">Completes an asynchronous request to unregister a work queue with a Multimedia Class Scheduler Service (MMCSS) task.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f650-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2f650-105">Syntax</span></span>


```C++
HRESULT WINAPI RtwqEndUnregisterWorkQueueWithMMCSS(
    IMFAsyncResult  *pResult 
);
```



## <a name="parameters"></a><span data-ttu-id="2f650-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2f650-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f650-107">*pResult*</span><span class="sxs-lookup"><span data-stu-id="2f650-107">*pResult*</span></span> 
</dt> <dd>

<span data-ttu-id="2f650-108">Puntatore all'interfaccia [**IMFAsyncResult**](/windows/win32/api/mfobjects/nn-mfobjects-imfasyncresult) .</span><span class="sxs-lookup"><span data-stu-id="2f650-108">Pointer to the [**IMFAsyncResult**](/windows/win32/api/mfobjects/nn-mfobjects-imfasyncresult) interface.</span></span> <span data-ttu-id="2f650-109">Passare lo stesso puntatore ricevuto dall'oggetto callback nel metodo [**IRtwqAsyncCallback:: Invoke**](/windows/win32/api/rtworkq/nf-rtworkq-irtwqasynccallback-invoke) .</span><span class="sxs-lookup"><span data-stu-id="2f650-109">Pass in the same pointer that your callback object received in the [**IRtwqAsyncCallback::Invoke**](/windows/win32/api/rtworkq/nf-rtworkq-irtwqasynccallback-invoke) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f650-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2f650-110">Return value</span></span>

<span data-ttu-id="2f650-111">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="2f650-111">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2f650-112">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2f650-112">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f650-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2f650-113">Requirements</span></span>



| <span data-ttu-id="2f650-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f650-114">Requirement</span></span> | <span data-ttu-id="2f650-115">Valore</span><span class="sxs-lookup"><span data-stu-id="2f650-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2f650-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2f650-116">Minimum supported client</span></span><br/> | <span data-ttu-id="2f650-117">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2f650-117">Windows 8.1 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="2f650-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2f650-118">Minimum supported server</span></span><br/> | <span data-ttu-id="2f650-119">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="2f650-119">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="2f650-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2f650-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f650-121"><dt>Nessuno</dt></span><span class="sxs-lookup"><span data-stu-id="2f650-121"><dt>None</dt></span></span> </dl>        |
| <span data-ttu-id="2f650-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="2f650-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="2f650-123"><dt>Rtworkq. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2f650-123"><dt>Rtworkq.lib</dt></span></span> </dl> |
| <span data-ttu-id="2f650-124">DLL</span><span class="sxs-lookup"><span data-stu-id="2f650-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2f650-125"><dt>RTWorkQ.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2f650-125"><dt>RTWorkQ.dll</dt></span></span> </dl> |



 

 
