---
description: Rappresenta un evento di modifica della classe, ovvero un tipo di evento intrinseco generato quando una classe viene modificata nello spazio dei nomi.
ms.assetid: 77e8e025-d584-495d-98f8-71e7fb2c9698
ms.tgt_platform: multiple
title: Classe __ClassModificationEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ClassModificationEvent
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 3634b632fa9ab66f0da3e48bf77fab5875daf12c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313219"
---
# <a name="__classmodificationevent-class"></a><span data-ttu-id="30f12-103">\_\_Classe ClassModificationEvent</span><span class="sxs-lookup"><span data-stu-id="30f12-103">\_\_ClassModificationEvent class</span></span>

<span data-ttu-id="30f12-104">La classe di sistema **\_ \_ ClassModificationEvent** rappresenta un evento di modifica della classe, ovvero un tipo di [evento intrinseco](determining-the-type-of-event-to-receive.md) generato quando una classe viene modificata nello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="30f12-104">The **\_\_ClassModificationEvent** system class represents a class modification event, which is a type of [intrinsic event](determining-the-type-of-event-to-receive.md) generated when a class is changed in the namespace.</span></span>

<span data-ttu-id="30f12-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="30f12-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="30f12-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="30f12-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="30f12-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="30f12-107">Syntax</span></span>

``` syntax
class __ClassModificationEvent : __ClassOperationEvent
{
  object PreviousClass;
  uint8  SECURITY_DESCRIPTOR[];
  object TargetClass;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="30f12-108">Members</span><span class="sxs-lookup"><span data-stu-id="30f12-108">Members</span></span>

<span data-ttu-id="30f12-109">La classe **\_ \_ ClassModificationEvent** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="30f12-109">The **\_\_ClassModificationEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="30f12-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="30f12-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="30f12-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="30f12-111">Properties</span></span>

<span data-ttu-id="30f12-112">La classe **\_ \_ ClassModificationEvent** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="30f12-112">The **\_\_ClassModificationEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="30f12-113">**PreviousClass**</span><span class="sxs-lookup"><span data-stu-id="30f12-113">**PreviousClass**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30f12-114">Tipo di dati: **Object**</span><span class="sxs-lookup"><span data-stu-id="30f12-114">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="30f12-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="30f12-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="30f12-116">Copia della versione originale della classe.</span><span class="sxs-lookup"><span data-stu-id="30f12-116">Copy of the original version of the class.</span></span>

</dd> <dt>

<span data-ttu-id="30f12-117">**descrittore di sicurezza \_**</span><span class="sxs-lookup"><span data-stu-id="30f12-117">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30f12-118">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="30f12-118">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="30f12-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="30f12-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="30f12-120">Descrittore utilizzato dal provider di eventi per determinare gli utenti che possono ricevere l'evento.</span><span class="sxs-lookup"><span data-stu-id="30f12-120">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="30f12-121">Questa proprietà viene ereditata dall' [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="30f12-121">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="30f12-122">**TargetClass**</span><span class="sxs-lookup"><span data-stu-id="30f12-122">**TargetClass**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30f12-123">Tipo di dati: **Object**</span><span class="sxs-lookup"><span data-stu-id="30f12-123">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="30f12-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="30f12-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="30f12-125">Copia della classe appena modificata segnalata dall'evento di modifica della classe.</span><span class="sxs-lookup"><span data-stu-id="30f12-125">Copy of the newly modified class reported by the class modification event.</span></span> <span data-ttu-id="30f12-126">Questa proprietà viene ereditata da [**\_ \_ ClassOperationEvent**](--classoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="30f12-126">This property is inherited from [**\_\_ClassOperationEvent**](--classoperationevent.md).</span></span>

</dd> <dt>

<span data-ttu-id="30f12-127">**ORA di \_ creazione**</span><span class="sxs-lookup"><span data-stu-id="30f12-127">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30f12-128">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="30f12-128">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="30f12-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="30f12-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="30f12-130">Valore univoco che indica l'ora in cui è stato generato l'evento.</span><span class="sxs-lookup"><span data-stu-id="30f12-130">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="30f12-131">Si tratta di un valore a 64 bit che rappresenta il numero di intervalli di 100-nanosecondi dopo il 1 ° gennaio 1601.</span><span class="sxs-lookup"><span data-stu-id="30f12-131">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="30f12-132">Le informazioni sono nel formato UTC (Coordinated Universal Time).</span><span class="sxs-lookup"><span data-stu-id="30f12-132">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="30f12-133">Questa proprietà viene ereditata dall' [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="30f12-133">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="30f12-134">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="30f12-134">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="30f12-135">Commenti</span><span class="sxs-lookup"><span data-stu-id="30f12-135">Remarks</span></span>

<span data-ttu-id="30f12-136">La classe **\_ \_ ClassModificationEvent** deriva da [**\_ \_ ClassOperationEvent**](--classoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="30f12-136">The **\_\_ClassModificationEvent** class is derived from [**\_\_ClassOperationEvent**](--classoperationevent.md).</span></span>

<span data-ttu-id="30f12-137">L'evento indica le versioni nuove e precedenti della definizione della classe.</span><span class="sxs-lookup"><span data-stu-id="30f12-137">The event reports both the new and old versions of the class definition.</span></span>

## <a name="requirements"></a><span data-ttu-id="30f12-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="30f12-138">Requirements</span></span>



| <span data-ttu-id="30f12-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="30f12-139">Requirement</span></span> | <span data-ttu-id="30f12-140">Valore</span><span class="sxs-lookup"><span data-stu-id="30f12-140">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="30f12-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="30f12-141">Minimum supported client</span></span><br/> | <span data-ttu-id="30f12-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="30f12-142">Windows Vista</span></span><br/>       |
| <span data-ttu-id="30f12-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="30f12-143">Minimum supported server</span></span><br/> | <span data-ttu-id="30f12-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="30f12-144">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="30f12-145">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="30f12-145">Namespace</span></span><br/>                | <span data-ttu-id="30f12-146">Tutti gli spazi dei nomi WMI</span><span class="sxs-lookup"><span data-stu-id="30f12-146">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="30f12-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="30f12-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30f12-148">**\_\_ClassOperationEvent**</span><span class="sxs-lookup"><span data-stu-id="30f12-148">**\_\_ClassOperationEvent**</span></span>](/windows/desktop/WmiSdk/--classoperationevent)
</dt> <dt>

[<span data-ttu-id="30f12-149">Classi di sistema WMI</span><span class="sxs-lookup"><span data-stu-id="30f12-149">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

