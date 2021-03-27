---
description: Rappresenta la classe del tipo di evento per gli eventi di duplicazione dell'handle.
ms.assetid: a933ffaa-8c99-4b87-ad00-4c40fa4d8d26
title: Classe ObHandleDuplicateEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObHandleDuplicateEvent
- ObHandleDuplicateEvent.Object
- ObHandleDuplicateEvent.ObjectType
- ObHandleDuplicateEvent.SourceHandle
- ObHandleDuplicateEvent.TargetHandle
- ObHandleDuplicateEvent.TargetProcessId
api_type:
- NA
api_location: ''
ms.openlocfilehash: 0f81ff9d85c0c5de8469f563db21e2054fa065f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980687"
---
# <a name="obhandleduplicateevent-class"></a><span data-ttu-id="00457-103">Classe ObHandleDuplicateEvent</span><span class="sxs-lookup"><span data-stu-id="00457-103">ObHandleDuplicateEvent class</span></span>

<span data-ttu-id="00457-104">Rappresenta la classe del tipo di evento per gli eventi di duplicazione dell'handle.</span><span class="sxs-lookup"><span data-stu-id="00457-104">Represents the event type class for handle duplication events.</span></span>

<span data-ttu-id="00457-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="00457-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="00457-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="00457-106">Syntax</span></span>

``` syntax
[Dynamic, EventType(34), EventTypeName("DuplicateHandle")]
class ObHandleDuplicateEvent : ObTrace
{
  uint32 Object;
  uint16 ObjectType;
  uint32 SourceHandle;
  uint32 TargetHandle;
  uint32 TargetProcessId;
};
```

## <a name="members"></a><span data-ttu-id="00457-107">Members</span><span class="sxs-lookup"><span data-stu-id="00457-107">Members</span></span>

<span data-ttu-id="00457-108">La classe **ObHandleDuplicateEvent** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="00457-108">The **ObHandleDuplicateEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="00457-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="00457-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="00457-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="00457-110">Properties</span></span>

<span data-ttu-id="00457-111">La classe **ObHandleDuplicateEvent** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="00457-111">The **ObHandleDuplicateEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="00457-112">**Object**</span><span class="sxs-lookup"><span data-stu-id="00457-112">**Object**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00457-113">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="00457-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="00457-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="00457-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="00457-115">Qualificatori: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**pointer**](event-tracing-mof-qualifiers.md), [**WmiDataId**](event-tracing-mof-qualifiers.md) (1)</span><span class="sxs-lookup"><span data-stu-id="00457-115">Qualifiers: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**Pointer**](event-tracing-mof-qualifiers.md), [**WmiDataId**](event-tracing-mof-qualifiers.md) (1)</span></span>
</dt> </dl>

<span data-ttu-id="00457-116">Oggetto.</span><span class="sxs-lookup"><span data-stu-id="00457-116">The object.</span></span>

</dd> <dt>

<span data-ttu-id="00457-117">**ObjectType**</span><span class="sxs-lookup"><span data-stu-id="00457-117">**ObjectType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00457-118">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="00457-118">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="00457-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="00457-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="00457-120">Qualificatori: [**WmiDataId**](event-tracing-mof-qualifiers.md) (5)</span><span class="sxs-lookup"><span data-stu-id="00457-120">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (5)</span></span>
</dt> </dl>

<span data-ttu-id="00457-121">Tipo di oggetto.</span><span class="sxs-lookup"><span data-stu-id="00457-121">The object type.</span></span>

</dd> <dt>

<span data-ttu-id="00457-122">**SourceHandle**</span><span class="sxs-lookup"><span data-stu-id="00457-122">**SourceHandle**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00457-123">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="00457-123">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="00457-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="00457-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="00457-125">Qualificatori: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (2)</span><span class="sxs-lookup"><span data-stu-id="00457-125">Qualifiers: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (2)</span></span>
</dt> </dl>

<span data-ttu-id="00457-126">Handle dell'oggetto di origine.</span><span class="sxs-lookup"><span data-stu-id="00457-126">The handle of the source object.</span></span>

</dd> <dt>

<span data-ttu-id="00457-127">**TargetHandle**</span><span class="sxs-lookup"><span data-stu-id="00457-127">**TargetHandle**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00457-128">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="00457-128">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="00457-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="00457-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="00457-130">Qualificatori: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (3)</span><span class="sxs-lookup"><span data-stu-id="00457-130">Qualifiers: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (3)</span></span>
</dt> </dl>

<span data-ttu-id="00457-131">Handle dell'oggetto di destinazione.</span><span class="sxs-lookup"><span data-stu-id="00457-131">The handle of the target object.</span></span>

</dd> <dt>

<span data-ttu-id="00457-132">**TargetProcessId**</span><span class="sxs-lookup"><span data-stu-id="00457-132">**TargetProcessId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00457-133">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="00457-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="00457-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="00457-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="00457-135">Qualificatori: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (4)</span><span class="sxs-lookup"><span data-stu-id="00457-135">Qualifiers: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (4)</span></span>
</dt> </dl>

<span data-ttu-id="00457-136">Identificatore del processo della destinazione.</span><span class="sxs-lookup"><span data-stu-id="00457-136">The process identifier of the target.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="00457-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="00457-137">Requirements</span></span>



| <span data-ttu-id="00457-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="00457-138">Requirement</span></span> | <span data-ttu-id="00457-139">Valore</span><span class="sxs-lookup"><span data-stu-id="00457-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="00457-140">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="00457-140">Minimum supported client</span></span><br/> | <span data-ttu-id="00457-141">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="00457-141">Windows 8 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="00457-142">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="00457-142">Minimum supported server</span></span><br/> | <span data-ttu-id="00457-143">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="00457-143">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="00457-144">MOF</span><span class="sxs-lookup"><span data-stu-id="00457-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="00457-145"><dt>Wmicore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="00457-145"><dt>Wmicore.mof</dt></span></span> </dl> |



 

 




