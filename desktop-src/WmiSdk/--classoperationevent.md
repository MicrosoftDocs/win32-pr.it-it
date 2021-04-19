---
description: È una classe di base per tutti gli eventi intrinseci correlati a una classe.
ms.assetid: 554bbabd-2639-40f5-8786-6df2188db0ec
ms.tgt_platform: multiple
title: Classe __ClassOperationEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ClassOperationEvent
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 0c7a78219cec5c014e289dad4bf1cc29f0466a06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319809"
---
# <a name="__classoperationevent-class"></a><span data-ttu-id="a71d9-103">\_\_Classe ClassOperationEvent</span><span class="sxs-lookup"><span data-stu-id="a71d9-103">\_\_ClassOperationEvent class</span></span>

<span data-ttu-id="a71d9-104">La classe di sistema **\_ \_ ClassOperationEvent** è una classe di base per tutti gli eventi intrinseci correlati a una classe.</span><span class="sxs-lookup"><span data-stu-id="a71d9-104">The **\_\_ClassOperationEvent** system class is a base class for all intrinsic events that relate to a class.</span></span>

<span data-ttu-id="a71d9-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="a71d9-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="a71d9-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="a71d9-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a71d9-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a71d9-107">Syntax</span></span>

``` syntax
class __ClassOperationEvent : __Event
{
  uint8  SECURITY_DESCRIPTOR[];
  object TargetClass;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="a71d9-108">Members</span><span class="sxs-lookup"><span data-stu-id="a71d9-108">Members</span></span>

<span data-ttu-id="a71d9-109">La classe **\_ \_ ClassOperationEvent** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="a71d9-109">The **\_\_ClassOperationEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="a71d9-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a71d9-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a71d9-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a71d9-111">Properties</span></span>

<span data-ttu-id="a71d9-112">La classe **\_ \_ ClassOperationEvent** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="a71d9-112">The **\_\_ClassOperationEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a71d9-113">**descrittore di sicurezza \_**</span><span class="sxs-lookup"><span data-stu-id="a71d9-113">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a71d9-114">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="a71d9-114">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="a71d9-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a71d9-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a71d9-116">Descrittore utilizzato dal provider di eventi per determinare gli utenti che possono ricevere l'evento.</span><span class="sxs-lookup"><span data-stu-id="a71d9-116">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="a71d9-117">Questa proprietà viene ereditata dall' [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="a71d9-117">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="a71d9-118">**TargetClass**</span><span class="sxs-lookup"><span data-stu-id="a71d9-118">**TargetClass**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a71d9-119">Tipo di dati: **Object**</span><span class="sxs-lookup"><span data-stu-id="a71d9-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="a71d9-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a71d9-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a71d9-121">Classe interessata dall'evento.</span><span class="sxs-lookup"><span data-stu-id="a71d9-121">Class affected by the event.</span></span> <span data-ttu-id="a71d9-122">Per gli eventi di creazione è la classe appena creata.</span><span class="sxs-lookup"><span data-stu-id="a71d9-122">For creation events, this is the newly created class.</span></span> <span data-ttu-id="a71d9-123">Per gli eventi di modifica, si tratta della nuova versione della classe modificata.</span><span class="sxs-lookup"><span data-stu-id="a71d9-123">For modification events, this is the new version of the changed class.</span></span> <span data-ttu-id="a71d9-124">Per gli eventi di eliminazione, si tratta della classe eliminata.</span><span class="sxs-lookup"><span data-stu-id="a71d9-124">For deletion events, this is the deleted class.</span></span>

</dd> <dt>

<span data-ttu-id="a71d9-125">**ORA di \_ creazione**</span><span class="sxs-lookup"><span data-stu-id="a71d9-125">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a71d9-126">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a71d9-126">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a71d9-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a71d9-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a71d9-128">Valore univoco che indica l'ora in cui è stato generato l'evento.</span><span class="sxs-lookup"><span data-stu-id="a71d9-128">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="a71d9-129">Si tratta di un valore a 64 bit che rappresenta il numero di intervalli di 100-nanosecondi dopo il 1 ° gennaio 1601.</span><span class="sxs-lookup"><span data-stu-id="a71d9-129">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="a71d9-130">Le informazioni sono nel formato UTC (Coordinated Universal Time).</span><span class="sxs-lookup"><span data-stu-id="a71d9-130">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="a71d9-131">Questa proprietà viene ereditata dall' [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="a71d9-131">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="a71d9-132">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="a71d9-132">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a71d9-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="a71d9-133">Remarks</span></span>

<span data-ttu-id="a71d9-134">La classe **\_ \_ ClassOperationEvent** è derivata dall' [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="a71d9-134">The **\_\_ClassOperationEvent** class is derived from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="a71d9-135">Le istanze di **\_ \_ ClassOperationEvent** non vengono create. vengono create solo le istanze delle relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="a71d9-135">Instances of **\_\_ClassOperationEvent** are not created; only instances of its subclasses are created.</span></span> <span data-ttu-id="a71d9-136">Le classi seguenti derivano da **\_ \_ ClassOperationEvent**:</span><span class="sxs-lookup"><span data-stu-id="a71d9-136">The following classes derive from **\_\_ClassOperationEvent**:</span></span>

[<span data-ttu-id="a71d9-137">**\_\_ClassCreationEvent**</span><span class="sxs-lookup"><span data-stu-id="a71d9-137">**\_\_ClassCreationEvent**</span></span>](--classcreationevent.md)

[<span data-ttu-id="a71d9-138">**\_\_ClassModificationEvent**</span><span class="sxs-lookup"><span data-stu-id="a71d9-138">**\_\_ClassModificationEvent**</span></span>](--classmodificationevent.md)

[<span data-ttu-id="a71d9-139">**\_\_ClassDeletionEvent**</span><span class="sxs-lookup"><span data-stu-id="a71d9-139">**\_\_ClassDeletionEvent**</span></span>](--classdeletionevent.md)

## <a name="requirements"></a><span data-ttu-id="a71d9-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a71d9-140">Requirements</span></span>



| <span data-ttu-id="a71d9-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="a71d9-141">Requirement</span></span> | <span data-ttu-id="a71d9-142">Valore</span><span class="sxs-lookup"><span data-stu-id="a71d9-142">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="a71d9-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a71d9-143">Minimum supported client</span></span><br/> | <span data-ttu-id="a71d9-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a71d9-144">Windows Vista</span></span><br/>       |
| <span data-ttu-id="a71d9-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a71d9-145">Minimum supported server</span></span><br/> | <span data-ttu-id="a71d9-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a71d9-146">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="a71d9-147">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a71d9-147">Namespace</span></span><br/>                | <span data-ttu-id="a71d9-148">Tutti gli spazi dei nomi WMI</span><span class="sxs-lookup"><span data-stu-id="a71d9-148">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="a71d9-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a71d9-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a71d9-150">**\_\_Evento**</span><span class="sxs-lookup"><span data-stu-id="a71d9-150">**\_\_Event**</span></span>](/windows/desktop/WmiSdk/--event)
</dt> <dt>

[<span data-ttu-id="a71d9-151">Classi di sistema WMI</span><span class="sxs-lookup"><span data-stu-id="a71d9-151">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="a71d9-152">Determinazione del tipo di evento da ricevere</span><span class="sxs-lookup"><span data-stu-id="a71d9-152">Determining the Type of Event to Receive</span></span>](determining-the-type-of-event-to-receive.md)
</dt> </dl>

 

