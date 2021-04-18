---
description: Il metodo OnStop deve essere implementato dal monitoraggio. MSCVC chiama questo metodo per notificare al monitoraggio che l'acquisizione verrà arrestata.
ms.assetid: 5988bfb8-2068-42a1-a774-6f6be9828568
title: 'Metodo IMonitor:: OnStop (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor.OnStop
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: a737aa5bede443b63f2074239eec17ea8a205cc8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305871"
---
# <a name="imonitoronstop-method"></a><span data-ttu-id="6d697-104">Metodo IMonitor:: OnStop</span><span class="sxs-lookup"><span data-stu-id="6d697-104">IMonitor::OnStop method</span></span>

<span data-ttu-id="6d697-105">Il metodo **OnStop** deve essere implementato dal monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="6d697-105">The **OnStop** method must be implemented by the monitor.</span></span> <span data-ttu-id="6d697-106">MSCVC chiama questo metodo per notificare al monitoraggio che l'acquisizione verrà arrestata.</span><span class="sxs-lookup"><span data-stu-id="6d697-106">The MSCVC calls this method to notify the monitor that the capture will be stopped.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d697-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6d697-107">Syntax</span></span>


```C++
HRESULT OnStop();
```



## <a name="parameters"></a><span data-ttu-id="6d697-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="6d697-108">Parameters</span></span>

<span data-ttu-id="6d697-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="6d697-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6d697-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6d697-110">Return value</span></span>

<span data-ttu-id="6d697-111">Se il metodo ha esito positivo, il valore restituito è \_ OK (che corrisponde a NOERROR).</span><span class="sxs-lookup"><span data-stu-id="6d697-111">If the method is successful, the return value is S\_OK (which is the same as NOERROR).</span></span>

<span data-ttu-id="6d697-112">Se il metodo ha esito negativo, il valore restituito è un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="6d697-112">If the method is unsuccessful, the return value is an error code.</span></span> <span data-ttu-id="6d697-113">Quando viene restituito un codice di errore, il monitoraggio non può essere riavviato.</span><span class="sxs-lookup"><span data-stu-id="6d697-113">When an error code is returned, the monitor cannot be restarted.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d697-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="6d697-114">Remarks</span></span>

<span data-ttu-id="6d697-115">MCSVC chiama questo metodo dopo la chiamata a [IRTC:: Stop](irtc-stop.md) .</span><span class="sxs-lookup"><span data-stu-id="6d697-115">The MCSVC calls this method after [IRTC::Stop](irtc-stop.md) is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d697-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6d697-116">Requirements</span></span>



| <span data-ttu-id="6d697-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d697-117">Requirement</span></span> | <span data-ttu-id="6d697-118">Valore</span><span class="sxs-lookup"><span data-stu-id="6d697-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6d697-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6d697-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6d697-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6d697-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="6d697-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6d697-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6d697-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6d697-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="6d697-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6d697-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d697-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d697-124"><dt>Netmon.h</dt></span></span> </dl> |



 

 




