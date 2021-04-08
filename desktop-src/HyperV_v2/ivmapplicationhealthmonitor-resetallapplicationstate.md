---
description: Reimposta lo stato di integrità di tutte le applicazioni in una macchina virtuale.
ms.assetid: DB0B2FB3-87EB-44B2-9C4E-849BCE594E89
title: 'Metodo IVmApplicationHealthMonitor:: ResetAllApplicationState'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVmApplicationHealthMonitor.ResetAllApplicationState
api_type:
- COM
api_location:
- VmApplicationHealthMonitor.idl
ms.openlocfilehash: b13781d26c256e41ea6685b19a3097236ebbdb91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880210"
---
# <a name="ivmapplicationhealthmonitorresetallapplicationstate-method"></a><span data-ttu-id="e247b-103">Metodo IVmApplicationHealthMonitor:: ResetAllApplicationState</span><span class="sxs-lookup"><span data-stu-id="e247b-103">IVmApplicationHealthMonitor::ResetAllApplicationState method</span></span>

<span data-ttu-id="e247b-104">Reimposta lo stato di integrità di tutte le applicazioni in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e247b-104">Resets the health state for all applications in a virtual machine.</span></span> <span data-ttu-id="e247b-105">In caso di esito positivo, lo stato di integrità di tutte le applicazioni monitorate verrà impostato su **ApplicationStateHealthy**.</span><span class="sxs-lookup"><span data-stu-id="e247b-105">If successful, the health state for all monitored applications will be set to **ApplicationStateHealthy**.</span></span>

## <a name="syntax"></a><span data-ttu-id="e247b-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e247b-106">Syntax</span></span>


```C++
HRESULT ResetAllApplicationState();
```



## <a name="parameters"></a><span data-ttu-id="e247b-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="e247b-107">Parameters</span></span>

<span data-ttu-id="e247b-108">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="e247b-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e247b-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e247b-109">Return value</span></span>

<span data-ttu-id="e247b-110">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="e247b-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e247b-111">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e247b-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e247b-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="e247b-112">Remarks</span></span>

<span data-ttu-id="e247b-113">Per utilizzare questo elemento di programmazione, è necessario installare i componenti di integrazione di Windows 8 nella macchina virtuale in cui è in esecuzione l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e247b-113">To use this programming element, the Windows 8 integration components must be installed on the virtual machine that the application is running in.</span></span>

## <a name="requirements"></a><span data-ttu-id="e247b-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e247b-114">Requirements</span></span>



| <span data-ttu-id="e247b-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e247b-115">Requirement</span></span> | <span data-ttu-id="e247b-116">Valore</span><span class="sxs-lookup"><span data-stu-id="e247b-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e247b-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e247b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e247b-118">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="e247b-118">Windows 8 \[desktop apps only\]</span></span><br/>                                                                |
| <span data-ttu-id="e247b-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e247b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e247b-120">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="e247b-120">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e247b-121">Versione</span><span class="sxs-lookup"><span data-stu-id="e247b-121">Version</span></span><br/>                  | <span data-ttu-id="e247b-122">Componenti di integrazione per Windows 8</span><span class="sxs-lookup"><span data-stu-id="e247b-122">Integration components for Windows 8</span></span><br/>                                                           |
| <span data-ttu-id="e247b-123">IDL</span><span class="sxs-lookup"><span data-stu-id="e247b-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e247b-124"><dt>VmApplicationHealthMonitor. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e247b-124"><dt>VmApplicationHealthMonitor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e247b-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e247b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e247b-126">**IVmApplicationHealthMonitor**</span><span class="sxs-lookup"><span data-stu-id="e247b-126">**IVmApplicationHealthMonitor**</span></span>](ivmapplicationhealthmonitor.md)
</dt> </dl>

 

 




