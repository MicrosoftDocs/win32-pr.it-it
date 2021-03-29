---
description: Questa classe è la classe del tipo di evento per gli eventi del thread. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: cc668fef-48fe-4948-8fe5-4351f7a033d1
title: Classe Thread_V0_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Thread_V0_TypeGroup1
- Thread_V0_TypeGroup1.TThreadId
- Thread_V0_TypeGroup1.ProcessId
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2f6fa7ae1f50e005fe8f66e918a4a8360a0e8f86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978223"
---
# <a name="thread_v0_typegroup1-class"></a><span data-ttu-id="b84a8-104">\_ \_ Classe TypeGroup1 di thread V0</span><span class="sxs-lookup"><span data-stu-id="b84a8-104">Thread\_V0\_TypeGroup1 class</span></span>

<span data-ttu-id="b84a8-105">Questa classe è la classe del tipo di evento per gli eventi del thread.</span><span class="sxs-lookup"><span data-stu-id="b84a8-105">This class is the event type class for thread events.</span></span>

<span data-ttu-id="b84a8-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="b84a8-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="b84a8-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b84a8-107">Syntax</span></span>

``` syntax
[EventType{1, 2, 3, 4}, EventTypeName{"Start", "End", "DCStart", "DCEnd"}]
class Thread_V0_TypeGroup1 : Thread_V0
{
  uint32 TThreadId;
  uint32 ProcessId;
};
```

## <a name="members"></a><span data-ttu-id="b84a8-108">Members</span><span class="sxs-lookup"><span data-stu-id="b84a8-108">Members</span></span>

<span data-ttu-id="b84a8-109">La classe **thread \_ V0 \_ TypeGroup1** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="b84a8-109">The **Thread\_V0\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="b84a8-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b84a8-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b84a8-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b84a8-111">Properties</span></span>

<span data-ttu-id="b84a8-112">La **classe \_ \_ TypeGroup1 del thread V0** presenta queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="b84a8-112">The **Thread\_V0\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b84a8-113">ProcessId</span><span class="sxs-lookup"><span data-stu-id="b84a8-113">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b84a8-114">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b84a8-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b84a8-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b84a8-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b84a8-116">Qualificatori: WmiDataId (2), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="b84a8-116">Qualifiers: WmiDataId(2), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="b84a8-117">Identificatore del processo del thread che interessano l'evento.</span><span class="sxs-lookup"><span data-stu-id="b84a8-117">Process identifier of the thread involved in the event.</span></span>

</dd> <dt>

<span data-ttu-id="b84a8-118">TThreadId</span><span class="sxs-lookup"><span data-stu-id="b84a8-118">TThreadId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b84a8-119">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b84a8-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b84a8-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b84a8-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b84a8-121">Qualificatori: WmiDataId (1), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="b84a8-121">Qualifiers: WmiDataId(1), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="b84a8-122">Identificatore del thread associato all'evento.</span><span class="sxs-lookup"><span data-stu-id="b84a8-122">Thread identifier of the thread involved in the event.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b84a8-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b84a8-123">Requirements</span></span>



| <span data-ttu-id="b84a8-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="b84a8-124">Requirement</span></span> | <span data-ttu-id="b84a8-125">Valore</span><span class="sxs-lookup"><span data-stu-id="b84a8-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="b84a8-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b84a8-126">Minimum supported client</span></span><br/> | <span data-ttu-id="b84a8-127">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b84a8-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="b84a8-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b84a8-128">Minimum supported server</span></span><br/> | <span data-ttu-id="b84a8-129">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b84a8-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="b84a8-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b84a8-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b84a8-131">**Thread \_ V0**</span><span class="sxs-lookup"><span data-stu-id="b84a8-131">**Thread\_V0**</span></span>](thread-v0.md)
</dt> </dl>

 

 




