---
description: Rappresenta la classe del tipo di evento per gli eventi di creazione o chiusura dell'handle.
ms.assetid: 39d27cdf-fa51-4fb1-8998-7150ca627eff
title: Classe ObHandleEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObHandleEvent
- ObHandleEvent.Handle
- ObHandleEvent.Object
- ObHandleEvent.ObjectName
- ObHandleEvent.ObjectType
api_type:
- NA
api_location: ''
ms.openlocfilehash: ae293684bd09322c7193035d374e5e2bad21447f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980114"
---
# <a name="obhandleevent-class"></a><span data-ttu-id="68f4c-103">Classe ObHandleEvent</span><span class="sxs-lookup"><span data-stu-id="68f4c-103">ObHandleEvent class</span></span>

<span data-ttu-id="68f4c-104">Rappresenta la classe del tipo di evento per gli eventi di creazione o chiusura dell'handle.</span><span class="sxs-lookup"><span data-stu-id="68f4c-104">Represents the event type class for handle creation or closure events.</span></span>

<span data-ttu-id="68f4c-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="68f4c-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="68f4c-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="68f4c-106">Syntax</span></span>

``` syntax
[Dynamic, EventType{32,33}, EventTypeName{CreateHandle,CloseHandle}]
class ObHandleEvent : ObTrace
{
  uint32 Handle;
  uint32 Object;
  string ObjectName;
  uint16 ObjectType;
};
```

## <a name="members"></a><span data-ttu-id="68f4c-107">Members</span><span class="sxs-lookup"><span data-stu-id="68f4c-107">Members</span></span>

<span data-ttu-id="68f4c-108">La classe **ObHandleEvent** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="68f4c-108">The **ObHandleEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="68f4c-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="68f4c-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="68f4c-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="68f4c-110">Properties</span></span>

<span data-ttu-id="68f4c-111">La classe **ObHandleEvent** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="68f4c-111">The **ObHandleEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="68f4c-112">**Handle**</span><span class="sxs-lookup"><span data-stu-id="68f4c-112">**Handle**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68f4c-113">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="68f4c-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="68f4c-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="68f4c-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68f4c-115">Qualificatori: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (2)</span><span class="sxs-lookup"><span data-stu-id="68f4c-115">Qualifiers: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (2)</span></span>
</dt> </dl>

<span data-ttu-id="68f4c-116">Handle dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="68f4c-116">The object handle.</span></span>

</dd> <dt>

<span data-ttu-id="68f4c-117">**Object**</span><span class="sxs-lookup"><span data-stu-id="68f4c-117">**Object**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68f4c-118">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="68f4c-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="68f4c-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="68f4c-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68f4c-120">Qualificatori: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**pointer**](event-tracing-mof-qualifiers.md), [**WmiDataId**](event-tracing-mof-qualifiers.md) (1)</span><span class="sxs-lookup"><span data-stu-id="68f4c-120">Qualifiers: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**Pointer**](event-tracing-mof-qualifiers.md), [**WmiDataId**](event-tracing-mof-qualifiers.md) (1)</span></span>
</dt> </dl>

<span data-ttu-id="68f4c-121">Oggetto.</span><span class="sxs-lookup"><span data-stu-id="68f4c-121">The object.</span></span>

</dd> <dt>

<span data-ttu-id="68f4c-122">**ObjectName**</span><span class="sxs-lookup"><span data-stu-id="68f4c-122">**ObjectName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68f4c-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="68f4c-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68f4c-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="68f4c-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68f4c-125">Qualificatori: [**Format**](event-tracing-mof-qualifiers.md) ("w"), [**StringTermination**](event-tracing-mof-qualifiers.md) ("NullTerminated"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (4)</span><span class="sxs-lookup"><span data-stu-id="68f4c-125">Qualifiers: [**Format**](event-tracing-mof-qualifiers.md) ("w"), [**StringTermination**](event-tracing-mof-qualifiers.md) ("NullTerminated"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (4)</span></span>
</dt> </dl>

<span data-ttu-id="68f4c-126">Nome dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="68f4c-126">The object name.</span></span>

</dd> <dt>

<span data-ttu-id="68f4c-127">**ObjectType**</span><span class="sxs-lookup"><span data-stu-id="68f4c-127">**ObjectType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68f4c-128">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="68f4c-128">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="68f4c-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="68f4c-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68f4c-130">Qualificatori: [**WmiDataId**](event-tracing-mof-qualifiers.md) (3)</span><span class="sxs-lookup"><span data-stu-id="68f4c-130">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (3)</span></span>
</dt> </dl>

<span data-ttu-id="68f4c-131">Tipo di oggetto.</span><span class="sxs-lookup"><span data-stu-id="68f4c-131">The object type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="68f4c-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="68f4c-132">Requirements</span></span>



| <span data-ttu-id="68f4c-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="68f4c-133">Requirement</span></span> | <span data-ttu-id="68f4c-134">Valore</span><span class="sxs-lookup"><span data-stu-id="68f4c-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="68f4c-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="68f4c-135">Minimum supported client</span></span><br/> | <span data-ttu-id="68f4c-136">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="68f4c-136">Windows 8 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="68f4c-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="68f4c-137">Minimum supported server</span></span><br/> | <span data-ttu-id="68f4c-138">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="68f4c-138">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="68f4c-139">MOF</span><span class="sxs-lookup"><span data-stu-id="68f4c-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="68f4c-140"><dt>Wmicore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="68f4c-140"><dt>Wmicore.mof</dt></span></span> </dl> |



 

 




