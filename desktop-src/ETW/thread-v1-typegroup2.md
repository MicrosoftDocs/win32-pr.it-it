---
description: Questa classe è la classe del tipo di evento per gli eventi di fine thread. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: c495bf22-04ce-4285-8e7e-152e4ab65823
title: Classe Thread_V1_TypeGroup2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Thread_V1_TypeGroup2
- Thread_V1_TypeGroup2.ProcessId
- Thread_V1_TypeGroup2.TThreadId
api_type:
- NA
api_location: ''
ms.openlocfilehash: 3e56590127b2317813d7431a1cc646fbe76e35a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527289"
---
# <a name="thread_v1_typegroup2-class"></a><span data-ttu-id="4bce4-104">\_Classe thread V1 \_ TypeGroup2</span><span class="sxs-lookup"><span data-stu-id="4bce4-104">Thread\_V1\_TypeGroup2 class</span></span>

<span data-ttu-id="4bce4-105">Questa classe è la classe del tipo di evento per gli eventi di fine thread.</span><span class="sxs-lookup"><span data-stu-id="4bce4-105">This class is the event type class for thread end events.</span></span>

<span data-ttu-id="4bce4-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="4bce4-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="4bce4-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4bce4-107">Syntax</span></span>

``` syntax
[EventType{2, 4}, EventTypeName{"End", "DCEnd"}]
class Thread_V1_TypeGroup2 : Thread_V1
{
  uint32 ProcessId;
  uint32 TThreadId;
};
```

## <a name="members"></a><span data-ttu-id="4bce4-108">Members</span><span class="sxs-lookup"><span data-stu-id="4bce4-108">Members</span></span>

<span data-ttu-id="4bce4-109">I tipi di membri della classe **thread \_ V1 \_ TypeGroup2** sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="4bce4-109">The **Thread\_V1\_TypeGroup2** class has these types of members:</span></span>

-   [<span data-ttu-id="4bce4-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4bce4-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4bce4-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4bce4-111">Properties</span></span>

<span data-ttu-id="4bce4-112">La classe **thread \_ V1 \_ TypeGroup2** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="4bce4-112">The **Thread\_V1\_TypeGroup2** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4bce4-113">ProcessId</span><span class="sxs-lookup"><span data-stu-id="4bce4-113">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4bce4-114">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4bce4-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4bce4-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4bce4-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4bce4-116">Qualificatori: WmiDataId (1)</span><span class="sxs-lookup"><span data-stu-id="4bce4-116">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="4bce4-117">Identificatore del processo del thread che interessano l'evento.</span><span class="sxs-lookup"><span data-stu-id="4bce4-117">Process identifier of the thread involved in the event.</span></span>

<span data-ttu-id="4bce4-118">**Windows Server 2003:** Contiene il qualificatore di formato ("x").</span><span class="sxs-lookup"><span data-stu-id="4bce4-118">**Windows Server 2003:** Contains the Format("x") qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="4bce4-119">TThreadId</span><span class="sxs-lookup"><span data-stu-id="4bce4-119">TThreadId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4bce4-120">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4bce4-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4bce4-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4bce4-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4bce4-122">Qualificatori: WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="4bce4-122">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="4bce4-123">Identificatore del thread associato all'evento.</span><span class="sxs-lookup"><span data-stu-id="4bce4-123">Thread identifier of the thread involved in the event.</span></span>

<span data-ttu-id="4bce4-124">**Windows Server 2003:** Contiene il qualificatore di formato ("x").</span><span class="sxs-lookup"><span data-stu-id="4bce4-124">**Windows Server 2003:** Contains the Format("x") qualifier.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4bce4-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4bce4-125">Requirements</span></span>



| <span data-ttu-id="4bce4-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="4bce4-126">Requirement</span></span> | <span data-ttu-id="4bce4-127">Valore</span><span class="sxs-lookup"><span data-stu-id="4bce4-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4bce4-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4bce4-128">Minimum supported client</span></span><br/> | <span data-ttu-id="4bce4-129">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="4bce4-129">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="4bce4-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4bce4-130">Minimum supported server</span></span><br/> | <span data-ttu-id="4bce4-131">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4bce4-131">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4bce4-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4bce4-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bce4-133">**Thread \_ V1**</span><span class="sxs-lookup"><span data-stu-id="4bce4-133">**Thread\_V1**</span></span>](thread-v1.md)
</dt> </dl>

 

 




