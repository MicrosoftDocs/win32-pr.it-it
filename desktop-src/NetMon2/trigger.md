---
description: La struttura del TRIGGER indica un'azione che deve essere eseguita dal driver a un'ora specificata.
ms.assetid: 63541796-b0d8-456c-8544-697fedbe05f7
title: Struttura TRIGGER (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TRIGGER
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: d9b385557e3c34bdf75f2bf959d4e5e3e47e0750
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315886"
---
# <a name="trigger-structure"></a><span data-ttu-id="70a38-103">Struttura TRIGGER</span><span class="sxs-lookup"><span data-stu-id="70a38-103">TRIGGER structure</span></span>

<span data-ttu-id="70a38-104">La struttura del **trigger** indica un'azione che deve essere eseguita dal driver a un'ora specificata.</span><span class="sxs-lookup"><span data-stu-id="70a38-104">The **TRIGGER** structure indicates an action to be taken by the driver at a specified time.</span></span>

## <a name="syntax"></a><span data-ttu-id="70a38-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="70a38-105">Syntax</span></span>


```C++
typedef struct _TRIGGER {
  BOOL         TriggerActive;
  BYTE         TriggerType;
  BYTE         TriggerAction;
  DWORD        TriggerFlags;
  PATTERNMATCH TriggerPatternMatch;
  DWORD        TriggerBufferSize;
  DWORD        Reserved;
} TRIGGER, *LPTRIGGER;
```



## <a name="members"></a><span data-ttu-id="70a38-106">Members</span><span class="sxs-lookup"><span data-stu-id="70a38-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="70a38-107">**TriggerActive**</span><span class="sxs-lookup"><span data-stu-id="70a38-107">**TriggerActive**</span></span>
</dt> <dd>

<span data-ttu-id="70a38-108">Valore booleano che determina se il trigger deve prestare attenzione al driver.</span><span class="sxs-lookup"><span data-stu-id="70a38-108">A Boolean value that determines if the trigger should be paid attention to by the driver.</span></span>

</dd> <dt>

<span data-ttu-id="70a38-109">**TriggerType**</span><span class="sxs-lookup"><span data-stu-id="70a38-109">**TriggerType**</span></span>
</dt> <dd>

<span data-ttu-id="70a38-110">Codice op del trigger.</span><span class="sxs-lookup"><span data-stu-id="70a38-110">The op code of the trigger.</span></span>

</dd> <dt>

<span data-ttu-id="70a38-111">**TriggerAction**</span><span class="sxs-lookup"><span data-stu-id="70a38-111">**TriggerAction**</span></span>
</dt> <dd>

<span data-ttu-id="70a38-112">Azione che il trigger deve eseguire se viene attivato.</span><span class="sxs-lookup"><span data-stu-id="70a38-112">Action that the trigger is to take if it is fired.</span></span>

</dd> <dt>

<span data-ttu-id="70a38-113">**TriggerFlags**</span><span class="sxs-lookup"><span data-stu-id="70a38-113">**TriggerFlags**</span></span>
</dt> <dd>

<span data-ttu-id="70a38-114">Flag del trigger.</span><span class="sxs-lookup"><span data-stu-id="70a38-114">Trigger flags.</span></span>

</dd> <dt>

<span data-ttu-id="70a38-115">**TriggerPatternMatch**</span><span class="sxs-lookup"><span data-stu-id="70a38-115">**TriggerPatternMatch**</span></span>
</dt> <dd>

<span data-ttu-id="70a38-116">Modello di trigger corrispondente.</span><span class="sxs-lookup"><span data-stu-id="70a38-116">The trigger pattern match.</span></span>

</dd> <dt>

<span data-ttu-id="70a38-117">**TriggerBufferSize**</span><span class="sxs-lookup"><span data-stu-id="70a38-117">**TriggerBufferSize**</span></span>
</dt> <dd>

<span data-ttu-id="70a38-118">Dimensioni del buffer di trigger.</span><span class="sxs-lookup"><span data-stu-id="70a38-118">Trigger buffer size.</span></span>

</dd> <dt>

<span data-ttu-id="70a38-119">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="70a38-119">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="70a38-120">Riservato.</span><span class="sxs-lookup"><span data-stu-id="70a38-120">Reserved.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="70a38-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="70a38-121">Requirements</span></span>



| <span data-ttu-id="70a38-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="70a38-122">Requirement</span></span> | <span data-ttu-id="70a38-123">Valore</span><span class="sxs-lookup"><span data-stu-id="70a38-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="70a38-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="70a38-124">Minimum supported client</span></span><br/> | <span data-ttu-id="70a38-125">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="70a38-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="70a38-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="70a38-126">Minimum supported server</span></span><br/> | <span data-ttu-id="70a38-127">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="70a38-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="70a38-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="70a38-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="70a38-129"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="70a38-129"><dt>Netmon.h</dt></span></span> </dl> |



 

 




