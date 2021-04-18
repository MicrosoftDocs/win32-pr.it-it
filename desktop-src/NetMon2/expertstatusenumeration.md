---
description: L'enumerazione EXPERTSTATUSENUMERATION contiene valori di stato. Viene usato dal membro di stato della struttura EXPERTSTATUS e dal parametro status in ExpertIndicateStatus.
ms.assetid: 217dce5a-3698-45a9-bb13-8379bcbdd762
title: Enumerazione EXPERTSTATUSENUMERATION (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPERT_STATUS_ENUMERATION
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: b634d4dad2e024c3c995216b5af7de23b14b7da0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305942"
---
# <a name="expertstatusenumeration-enumeration"></a><span data-ttu-id="26bf5-104">Enumerazione EXPERTSTATUSENUMERATION</span><span class="sxs-lookup"><span data-stu-id="26bf5-104">EXPERTSTATUSENUMERATION enumeration</span></span>

<span data-ttu-id="26bf5-105">L'enumerazione **EXPERTSTATUSENUMERATION** contiene valori di stato.</span><span class="sxs-lookup"><span data-stu-id="26bf5-105">The **EXPERTSTATUSENUMERATION** enumeration contains status values.</span></span> <span data-ttu-id="26bf5-106">Viene usato dal membro di **stato** della struttura [EXPERTSTATUS](expertstatus.md) e dal parametro *status* in [ExpertIndicateStatus](expertindicatestatus.md).</span><span class="sxs-lookup"><span data-stu-id="26bf5-106">It is used by the **Status** member of [EXPERTSTATUS](expertstatus.md) structure and the *Status* parameter in [ExpertIndicateStatus](expertindicatestatus.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="26bf5-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="26bf5-107">Syntax</span></span>


```C++
typedef enum  { 
  EXPERTSTATUS_INACTIVE  = 0,
  EXPERTSTATUS_STARTING,
  EXPERTSTATUS_RUNNING,
  EXPERTSTATUS_PROBLEM,
  EXPERTSTATUS_ABORTED,
  EXPERTSTATUS_DONE
} EXPERT_STATUS_ENUMERATION;
```



## <a name="constants"></a><span data-ttu-id="26bf5-108">Costanti</span><span class="sxs-lookup"><span data-stu-id="26bf5-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="26bf5-109"><span id="EXPERTSTATUS_INACTIVE"></span><span id="expertstatus_inactive"></span>**EXPERTSTATUS \_ INattivo**</span><span class="sxs-lookup"><span data-stu-id="26bf5-109"><span id="EXPERTSTATUS_INACTIVE"></span><span id="expertstatus_inactive"></span>**EXPERTSTATUS\_INACTIVE**</span></span>
</dt> <dd>

<span data-ttu-id="26bf5-110">L'esperto non è mai stato avviato.</span><span class="sxs-lookup"><span data-stu-id="26bf5-110">The expert never started.</span></span>

</dd> <dt>

<span data-ttu-id="26bf5-111"><span id="EXPERTSTATUS_STARTING"></span><span id="expertstatus_starting"></span>**avvio di EXPERTSTATUS \_**</span><span class="sxs-lookup"><span data-stu-id="26bf5-111"><span id="EXPERTSTATUS_STARTING"></span><span id="expertstatus_starting"></span>**EXPERTSTATUS\_STARTING**</span></span>
</dt> <dd>

<span data-ttu-id="26bf5-112">L'esperto si sta avviando.</span><span class="sxs-lookup"><span data-stu-id="26bf5-112">The expert is starting.</span></span>

</dd> <dt>

<span data-ttu-id="26bf5-113"><span id="EXPERTSTATUS_RUNNING"></span><span id="expertstatus_running"></span>**EXPERTSTATUS \_ in esecuzione**</span><span class="sxs-lookup"><span data-stu-id="26bf5-113"><span id="EXPERTSTATUS_RUNNING"></span><span id="expertstatus_running"></span>**EXPERTSTATUS\_RUNNING**</span></span>
</dt> <dd>

<span data-ttu-id="26bf5-114">L'esperto viene eseguito normalmente.</span><span class="sxs-lookup"><span data-stu-id="26bf5-114">The expert is running normally.</span></span>

</dd> <dt>

<span data-ttu-id="26bf5-115"><span id="EXPERTSTATUS_PROBLEM"></span><span id="expertstatus_problem"></span>**\_problema EXPERTSTATUS**</span><span class="sxs-lookup"><span data-stu-id="26bf5-115"><span id="EXPERTSTATUS_PROBLEM"></span><span id="expertstatus_problem"></span>**EXPERTSTATUS\_PROBLEM**</span></span>
</dt> <dd>

<span data-ttu-id="26bf5-116">Un problema specificato nello *stato secondario* ha interrotto l'esperto.</span><span class="sxs-lookup"><span data-stu-id="26bf5-116">A problem specified in *SubStatus* stopped the expert.</span></span>

</dd> <dt>

<span data-ttu-id="26bf5-117"><span id="EXPERTSTATUS_ABORTED"></span><span id="expertstatus_aborted"></span>**EXPERTSTATUS \_ interrotto**</span><span class="sxs-lookup"><span data-stu-id="26bf5-117"><span id="EXPERTSTATUS_ABORTED"></span><span id="expertstatus_aborted"></span>**EXPERTSTATUS\_ABORTED**</span></span>
</dt> <dd>

<span data-ttu-id="26bf5-118">Network Monitor arrestato l'esperto.</span><span class="sxs-lookup"><span data-stu-id="26bf5-118">Network Monitor stopped the expert.</span></span>

</dd> <dt>

<span data-ttu-id="26bf5-119"><span id="EXPERTSTATUS_DONE"></span><span id="expertstatus_done"></span>**EXPERTSTATUS \_ completato**</span><span class="sxs-lookup"><span data-stu-id="26bf5-119"><span id="EXPERTSTATUS_DONE"></span><span id="expertstatus_done"></span>**EXPERTSTATUS\_DONE**</span></span>
</dt> <dd>

<span data-ttu-id="26bf5-120">L'esperto è stato completato correttamente.</span><span class="sxs-lookup"><span data-stu-id="26bf5-120">The expert finished successfully.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="26bf5-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="26bf5-121">Requirements</span></span>



| <span data-ttu-id="26bf5-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="26bf5-122">Requirement</span></span> | <span data-ttu-id="26bf5-123">Valore</span><span class="sxs-lookup"><span data-stu-id="26bf5-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="26bf5-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="26bf5-124">Minimum supported client</span></span><br/> | <span data-ttu-id="26bf5-125">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="26bf5-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="26bf5-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="26bf5-126">Minimum supported server</span></span><br/> | <span data-ttu-id="26bf5-127">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="26bf5-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="26bf5-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="26bf5-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="26bf5-129"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="26bf5-129"><dt>Netmon.h</dt></span></span> </dl> |



 

 




