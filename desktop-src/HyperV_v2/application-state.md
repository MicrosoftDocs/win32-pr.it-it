---
description: Specifica lo stato di integrità di un'applicazione.
ms.assetid: CA06AA34-A549-4CFC-9B52-D2E0B200C3E9
title: Enumerazione APPLICATION_STATE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- APPLICATION_STATE
api_type:
- IDLDef
api_location:
- VmApplicationHealthMonitor.idl
ms.openlocfilehash: 4b7e288f41c863dc3f0365db3c6aae867605e5c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312339"
---
# <a name="application_state-enumeration"></a><span data-ttu-id="d7161-103">\_Enumerazione dello stato dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="d7161-103">APPLICATION\_STATE enumeration</span></span>

<span data-ttu-id="d7161-104">Specifica lo stato di integrità di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d7161-104">Specifies the health state of an application.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7161-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d7161-105">Syntax</span></span>


```C++
typedef enum _APPLICATION_STATE { 
  ApplicationStateHealthy   = 0,
  ApplicationStateCritical
} APPLICATION_STATE, *PAPPLICATION_STATE;
```



## <a name="constants"></a><span data-ttu-id="d7161-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="d7161-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="d7161-107"><span id="ApplicationStateHealthy"></span><span id="applicationstatehealthy"></span><span id="APPLICATIONSTATEHEALTHY"></span>**ApplicationStateHealthy**</span><span class="sxs-lookup"><span data-stu-id="d7161-107"><span id="ApplicationStateHealthy"></span><span id="applicationstatehealthy"></span><span id="APPLICATIONSTATEHEALTHY"></span>**ApplicationStateHealthy**</span></span>
</dt> <dd>

<span data-ttu-id="d7161-108">Lo stato dell'applicazione è integro.</span><span class="sxs-lookup"><span data-stu-id="d7161-108">The application state is healthy.</span></span>

</dd> <dt>

<span data-ttu-id="d7161-109"><span id="ApplicationStateCritical"></span><span id="applicationstatecritical"></span><span id="APPLICATIONSTATECRITICAL"></span>**ApplicationStateCritical**</span><span class="sxs-lookup"><span data-stu-id="d7161-109"><span id="ApplicationStateCritical"></span><span id="applicationstatecritical"></span><span id="APPLICATIONSTATECRITICAL"></span>**ApplicationStateCritical**</span></span>
</dt> <dd>

<span data-ttu-id="d7161-110">Lo stato dell'applicazione è critico.</span><span class="sxs-lookup"><span data-stu-id="d7161-110">The application state is critical.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d7161-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="d7161-111">Remarks</span></span>

<span data-ttu-id="d7161-112">Per utilizzare questo elemento di programmazione, è necessario installare i componenti di integrazione di Windows 8 nella macchina virtuale in cui è in esecuzione l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d7161-112">To use this programming element, the Windows 8 integration components must be installed on the virtual machine that the application is running in.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7161-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d7161-113">Requirements</span></span>



| <span data-ttu-id="d7161-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7161-114">Requirement</span></span> | <span data-ttu-id="d7161-115">Valore</span><span class="sxs-lookup"><span data-stu-id="d7161-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7161-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d7161-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d7161-117">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="d7161-117">Windows 8 \[desktop apps only\]</span></span><br/>                                                                |
| <span data-ttu-id="d7161-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d7161-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d7161-119">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="d7161-119">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="d7161-120">Versione</span><span class="sxs-lookup"><span data-stu-id="d7161-120">Version</span></span><br/>                  | <span data-ttu-id="d7161-121">Componenti di integrazione per Windows 8</span><span class="sxs-lookup"><span data-stu-id="d7161-121">Integration components for Windows 8</span></span><br/>                                                           |
| <span data-ttu-id="d7161-122">IDL</span><span class="sxs-lookup"><span data-stu-id="d7161-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d7161-123"><dt>VmApplicationHealthMonitor. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d7161-123"><dt>VmApplicationHealthMonitor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7161-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d7161-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7161-125">**SetApplicationState**</span><span class="sxs-lookup"><span data-stu-id="d7161-125">**SetApplicationState**</span></span>](ivmapplicationhealthmonitor-setapplicationstate.md)
</dt> </dl>

 

 




