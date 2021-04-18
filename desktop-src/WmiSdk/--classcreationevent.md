---
description: Rappresenta un evento di creazione della classe, ovvero un tipo di evento intrinseco generato quando una nuova classe viene aggiunta allo spazio dei nomi.
ms.assetid: a946a8eb-498c-4104-b80f-e520b0e62e36
ms.tgt_platform: multiple
title: Classe __ClassCreationEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ClassCreationEvent
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 18994ee7067e44a9199de9b62f7ff278a8bece00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313222"
---
# <a name="__classcreationevent-class"></a><span data-ttu-id="d5fb9-103">\_\_Classe ClassCreationEvent</span><span class="sxs-lookup"><span data-stu-id="d5fb9-103">\_\_ClassCreationEvent class</span></span>

<span data-ttu-id="d5fb9-104">La classe di sistema **\_ \_ ClassCreationEvent** rappresenta un evento di creazione della classe, ovvero un tipo di [evento intrinseco](determining-the-type-of-event-to-receive.md) generato quando una nuova classe viene aggiunta allo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="d5fb9-104">The **\_\_ClassCreationEvent** system class represents a class creation event, which is a type of [intrinsic event](determining-the-type-of-event-to-receive.md) generated when a new class is added to the namespace.</span></span>

<span data-ttu-id="d5fb9-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="d5fb9-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="d5fb9-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="d5fb9-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5fb9-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d5fb9-107">Syntax</span></span>

``` syntax
class __ClassCreationEvent : __ClassOperationEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  object TargetClass;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="d5fb9-108">Members</span><span class="sxs-lookup"><span data-stu-id="d5fb9-108">Members</span></span>

<span data-ttu-id="d5fb9-109">La classe **\_ \_ ClassCreationEvent** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="d5fb9-109">The **\_\_ClassCreationEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="d5fb9-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d5fb9-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d5fb9-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d5fb9-111">Properties</span></span>

<span data-ttu-id="d5fb9-112">La classe **\_ \_ ClassCreationEvent** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="d5fb9-112">The **\_\_ClassCreationEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d5fb9-113">**descrittore di sicurezza \_**</span><span class="sxs-lookup"><span data-stu-id="d5fb9-113">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5fb9-114">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="d5fb9-114">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="d5fb9-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d5fb9-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d5fb9-116">Descrittore utilizzato dal provider di eventi per determinare gli utenti che possono ricevere l'evento.</span><span class="sxs-lookup"><span data-stu-id="d5fb9-116">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="d5fb9-117">Questa proprietà viene ereditata dall' [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="d5fb9-117">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="d5fb9-118">**TargetClass**</span><span class="sxs-lookup"><span data-stu-id="d5fb9-118">**TargetClass**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5fb9-119">Tipo di dati: **Object**</span><span class="sxs-lookup"><span data-stu-id="d5fb9-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="d5fb9-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d5fb9-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d5fb9-121">Copia della classe appena creata segnalata dall'evento di creazione della classe.</span><span class="sxs-lookup"><span data-stu-id="d5fb9-121">Copy of the newly created class reported by the class creation event.</span></span> <span data-ttu-id="d5fb9-122">Questa proprietà viene ereditata da [**\_ \_ ClassOperationEvent**](--classoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="d5fb9-122">This property is inherited from [**\_\_ClassOperationEvent**](--classoperationevent.md).</span></span>

</dd> <dt>

<span data-ttu-id="d5fb9-123">**ORA di \_ creazione**</span><span class="sxs-lookup"><span data-stu-id="d5fb9-123">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5fb9-124">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d5fb9-124">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d5fb9-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d5fb9-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d5fb9-126">Valore univoco che indica l'ora in cui è stato generato l'evento.</span><span class="sxs-lookup"><span data-stu-id="d5fb9-126">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="d5fb9-127">Si tratta di un valore a 64 bit che rappresenta il numero di intervalli di 100-nanosecondi dopo il 1 ° gennaio 1601.</span><span class="sxs-lookup"><span data-stu-id="d5fb9-127">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="d5fb9-128">Le informazioni sono nel formato UTC (Universal Time Coordinates).</span><span class="sxs-lookup"><span data-stu-id="d5fb9-128">The information is in the Universal Time Coordinates (UTC) format.</span></span> <span data-ttu-id="d5fb9-129">Questa proprietà viene ereditata dall' [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="d5fb9-129">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="d5fb9-130">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="d5fb9-130">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d5fb9-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="d5fb9-131">Remarks</span></span>

<span data-ttu-id="d5fb9-132">La classe **\_ \_ ClassCreationEvent** deriva da [**\_ \_ ClassOperationEvent**](--classoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="d5fb9-132">The **\_\_ClassCreationEvent** class is derived from [**\_\_ClassOperationEvent**](--classoperationevent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d5fb9-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d5fb9-133">Requirements</span></span>



| <span data-ttu-id="d5fb9-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5fb9-134">Requirement</span></span> | <span data-ttu-id="d5fb9-135">Valore</span><span class="sxs-lookup"><span data-stu-id="d5fb9-135">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="d5fb9-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d5fb9-136">Minimum supported client</span></span><br/> | <span data-ttu-id="d5fb9-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d5fb9-137">Windows Vista</span></span><br/>       |
| <span data-ttu-id="d5fb9-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d5fb9-138">Minimum supported server</span></span><br/> | <span data-ttu-id="d5fb9-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d5fb9-139">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="d5fb9-140">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d5fb9-140">Namespace</span></span><br/>                | <span data-ttu-id="d5fb9-141">Tutti gli spazi dei nomi WMI</span><span class="sxs-lookup"><span data-stu-id="d5fb9-141">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="d5fb9-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d5fb9-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5fb9-143">**\_\_ClassOperationEvent**</span><span class="sxs-lookup"><span data-stu-id="d5fb9-143">**\_\_ClassOperationEvent**</span></span>](/windows/desktop/WmiSdk/--classoperationevent)
</dt> <dt>

[<span data-ttu-id="d5fb9-144">Classi di sistema WMI</span><span class="sxs-lookup"><span data-stu-id="d5fb9-144">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

