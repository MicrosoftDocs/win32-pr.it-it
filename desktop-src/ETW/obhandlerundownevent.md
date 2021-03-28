---
description: Rappresenta la classe del tipo di evento per gli eventi dell'handle di oggetto correlati all'inizio e alla fine della raccolta dei dati.
ms.assetid: 96231819-f4ca-4c5c-bc19-4a76add5d3cf
title: Classe ObHandleRundownEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObHandleRundownEvent
- ObHandleRundownEvent.Handle
- ObHandleRundownEvent.Object
- ObHandleRundownEvent.ObjectName
- ObHandleRundownEvent.ObjectType
- ObHandleRundownEvent.ProcessId
api_type:
- NA
api_location: ''
ms.openlocfilehash: 5477acc1851d9799fe2bf68f9b867ab3f4c032fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980119"
---
# <a name="obhandlerundownevent-class"></a><span data-ttu-id="f6bd5-103">Classe ObHandleRundownEvent</span><span class="sxs-lookup"><span data-stu-id="f6bd5-103">ObHandleRundownEvent class</span></span>

<span data-ttu-id="f6bd5-104">Rappresenta la classe del tipo di evento per gli eventi dell'handle di oggetto correlati all'inizio e alla fine della raccolta dei dati.</span><span class="sxs-lookup"><span data-stu-id="f6bd5-104">Represents the event type class for object handle events related to the beginning and end of data collection.</span></span> <span data-ttu-id="f6bd5-105">Questo evento comporta l'enumerazione di tutti gli handle quando viene eseguito il rundown.</span><span class="sxs-lookup"><span data-stu-id="f6bd5-105">This event involves the enumerating of all handles when rundown is performed.</span></span>

<span data-ttu-id="f6bd5-106">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="f6bd5-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6bd5-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f6bd5-107">Syntax</span></span>

``` syntax
[Dynamic, EventType{38,39}, EventTypeName{HandleDCStart,HandleDCEnd}]
class ObHandleRundownEvent : ObTrace
{
  uint32 Handle;
  uint32 Object;
  string ObjectName;
  uint16 ObjectType;
  uint32 ProcessId;
};
```

## <a name="members"></a><span data-ttu-id="f6bd5-108">Members</span><span class="sxs-lookup"><span data-stu-id="f6bd5-108">Members</span></span>

<span data-ttu-id="f6bd5-109">La classe **ObHandleRundownEvent** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="f6bd5-109">The **ObHandleRundownEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="f6bd5-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f6bd5-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f6bd5-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f6bd5-111">Properties</span></span>

<span data-ttu-id="f6bd5-112">La classe **ObHandleRundownEvent** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="f6bd5-112">The **ObHandleRundownEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f6bd5-113">**Handle**</span><span class="sxs-lookup"><span data-stu-id="f6bd5-113">**Handle**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6bd5-114">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f6bd5-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f6bd5-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f6bd5-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6bd5-116">Qualificatori: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (3)</span><span class="sxs-lookup"><span data-stu-id="f6bd5-116">Qualifiers: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (3)</span></span>
</dt> </dl>

<span data-ttu-id="f6bd5-117">Handle dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f6bd5-117">The object handle.</span></span>

</dd> <dt>

<span data-ttu-id="f6bd5-118">**Object**</span><span class="sxs-lookup"><span data-stu-id="f6bd5-118">**Object**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6bd5-119">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f6bd5-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f6bd5-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f6bd5-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6bd5-121">Qualificatori: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**pointer**](event-tracing-mof-qualifiers.md), [**WmiDataId**](event-tracing-mof-qualifiers.md) (1)</span><span class="sxs-lookup"><span data-stu-id="f6bd5-121">Qualifiers: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**Pointer**](event-tracing-mof-qualifiers.md), [**WmiDataId**](event-tracing-mof-qualifiers.md) (1)</span></span>
</dt> </dl>

<span data-ttu-id="f6bd5-122">Oggetto.</span><span class="sxs-lookup"><span data-stu-id="f6bd5-122">The object.</span></span>

</dd> <dt>

<span data-ttu-id="f6bd5-123">**ObjectName**</span><span class="sxs-lookup"><span data-stu-id="f6bd5-123">**ObjectName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6bd5-124">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f6bd5-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6bd5-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f6bd5-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6bd5-126">Qualificatori: [**Format**](event-tracing-mof-qualifiers.md) ("w"), [**StringTermination**](event-tracing-mof-qualifiers.md) ("NullTerminated"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (5)</span><span class="sxs-lookup"><span data-stu-id="f6bd5-126">Qualifiers: [**Format**](event-tracing-mof-qualifiers.md) ("w"), [**StringTermination**](event-tracing-mof-qualifiers.md) ("NullTerminated"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (5)</span></span>
</dt> </dl>

<span data-ttu-id="f6bd5-127">Nome dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f6bd5-127">The object name.</span></span>

</dd> <dt>

<span data-ttu-id="f6bd5-128">**ObjectType**</span><span class="sxs-lookup"><span data-stu-id="f6bd5-128">**ObjectType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6bd5-129">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f6bd5-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f6bd5-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f6bd5-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6bd5-131">Qualificatori: [**WmiDataId**](event-tracing-mof-qualifiers.md) (4)</span><span class="sxs-lookup"><span data-stu-id="f6bd5-131">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (4)</span></span>
</dt> </dl>

<span data-ttu-id="f6bd5-132">Tipo di oggetto.</span><span class="sxs-lookup"><span data-stu-id="f6bd5-132">The object type.</span></span>

</dd> <dt>

<span data-ttu-id="f6bd5-133">**ProcessId**</span><span class="sxs-lookup"><span data-stu-id="f6bd5-133">**ProcessId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6bd5-134">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f6bd5-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f6bd5-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f6bd5-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6bd5-136">Qualificatori: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (2)</span><span class="sxs-lookup"><span data-stu-id="f6bd5-136">Qualifiers: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (2)</span></span>
</dt> </dl>

<span data-ttu-id="f6bd5-137">Identificatore di processo.</span><span class="sxs-lookup"><span data-stu-id="f6bd5-137">The process identifier.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f6bd5-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f6bd5-138">Requirements</span></span>



| <span data-ttu-id="f6bd5-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6bd5-139">Requirement</span></span> | <span data-ttu-id="f6bd5-140">Valore</span><span class="sxs-lookup"><span data-stu-id="f6bd5-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f6bd5-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f6bd5-141">Minimum supported client</span></span><br/> | <span data-ttu-id="f6bd5-142">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="f6bd5-142">Windows 8 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="f6bd5-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f6bd5-143">Minimum supported server</span></span><br/> | <span data-ttu-id="f6bd5-144">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="f6bd5-144">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="f6bd5-145">MOF</span><span class="sxs-lookup"><span data-stu-id="f6bd5-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f6bd5-146"><dt>Wmicore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f6bd5-146"><dt>Wmicore.mof</dt></span></span> </dl> |



 

 




