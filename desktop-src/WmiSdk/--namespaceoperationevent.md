---
description: Classe di base per tutti gli eventi intrinseci correlati a uno spazio dei nomi.
ms.assetid: 168637b1-217e-4b6d-bd07-25127b9e9f6c
ms.tgt_platform: multiple
title: Classe __NamespaceOperationEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __NamespaceOperationEvent
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: d263af0eab5fc3899b45659bc8409a5e68776fe4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317584"
---
# <a name="__namespaceoperationevent-class"></a><span data-ttu-id="947cf-103">\_\_Classe NamespaceOperationEvent</span><span class="sxs-lookup"><span data-stu-id="947cf-103">\_\_NamespaceOperationEvent class</span></span>

<span data-ttu-id="947cf-104">La classe di sistema **\_ \_ NamespaceOperationEvent** è una classe di base per tutti gli eventi intrinseci correlati a uno spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="947cf-104">The **\_\_NamespaceOperationEvent** system class is a base class for all intrinsic events that relate to a namespace.</span></span>

<span data-ttu-id="947cf-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="947cf-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="947cf-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="947cf-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="947cf-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="947cf-107">Syntax</span></span>

``` syntax
class __NamespaceOperationEvent : __Event
{
  uint8       SECURITY_DESCRIPTOR[];
  __Namespace TargetNamespace;
  uint64      TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="947cf-108">Members</span><span class="sxs-lookup"><span data-stu-id="947cf-108">Members</span></span>

<span data-ttu-id="947cf-109">La classe **\_ \_ NamespaceOperationEvent** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="947cf-109">The **\_\_NamespaceOperationEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="947cf-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="947cf-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="947cf-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="947cf-111">Properties</span></span>

<span data-ttu-id="947cf-112">La classe **\_ \_ NamespaceOperationEvent** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="947cf-112">The **\_\_NamespaceOperationEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="947cf-113">**descrittore di sicurezza \_**</span><span class="sxs-lookup"><span data-stu-id="947cf-113">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="947cf-114">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="947cf-114">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="947cf-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="947cf-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="947cf-116">Descrittore utilizzato dal provider di eventi per determinare gli utenti che possono ricevere l'evento.</span><span class="sxs-lookup"><span data-stu-id="947cf-116">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="947cf-117">Questa proprietà viene ereditata dall' [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="947cf-117">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="947cf-118">**TargetNamespace**</span><span class="sxs-lookup"><span data-stu-id="947cf-118">**TargetNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="947cf-119">Tipo di dati: **\_ \_ namespace**</span><span class="sxs-lookup"><span data-stu-id="947cf-119">Data type: **\_\_Namespace**</span></span>
</dt> <dt>

<span data-ttu-id="947cf-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="947cf-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="947cf-121">Spazio dei nomi interessato dall'evento.</span><span class="sxs-lookup"><span data-stu-id="947cf-121">Namespace affected by the event.</span></span> <span data-ttu-id="947cf-122">Per gli eventi di creazione, si tratta dello spazio dei nomi appena creato.</span><span class="sxs-lookup"><span data-stu-id="947cf-122">For creation events, this is the newly created namespace.</span></span> <span data-ttu-id="947cf-123">Per gli eventi di modifica, si tratta dello spazio dei nomi modificato.</span><span class="sxs-lookup"><span data-stu-id="947cf-123">For modification events, this is the changed namespace.</span></span> <span data-ttu-id="947cf-124">Per gli eventi di eliminazione, si tratta dello spazio dei nomi eliminato.</span><span class="sxs-lookup"><span data-stu-id="947cf-124">For deletion events, this is the deleted namespace.</span></span>

</dd> <dt>

<span data-ttu-id="947cf-125">**ORA di \_ creazione**</span><span class="sxs-lookup"><span data-stu-id="947cf-125">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="947cf-126">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="947cf-126">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="947cf-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="947cf-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="947cf-128">Valore univoco che indica l'ora in cui è stato generato l'evento.</span><span class="sxs-lookup"><span data-stu-id="947cf-128">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="947cf-129">Si tratta di un valore a 64 bit che rappresenta il numero di intervalli di 100-nanosecondi dopo il 1 ° gennaio 1601.</span><span class="sxs-lookup"><span data-stu-id="947cf-129">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="947cf-130">Le informazioni sono nel formato UTC (Coordinated Universal Time).</span><span class="sxs-lookup"><span data-stu-id="947cf-130">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="947cf-131">Questa proprietà viene ereditata dall' [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="947cf-131">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="947cf-132">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="947cf-132">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="947cf-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="947cf-133">Remarks</span></span>

<span data-ttu-id="947cf-134">La classe **\_ \_ NamespaceOperationEvent** è derivata dall' [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="947cf-134">The **\_\_NamespaceOperationEvent** class is derived from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="947cf-135">Le istanze di questa classe non vengono create.</span><span class="sxs-lookup"><span data-stu-id="947cf-135">Instances of this class are not created.</span></span> <span data-ttu-id="947cf-136">WMI crea istanze di una delle classi seguenti derivate da questa classe:</span><span class="sxs-lookup"><span data-stu-id="947cf-136">WMI creates instances of one of the following classes derived from this class:</span></span>

[<span data-ttu-id="947cf-137">**\_\_NamespaceCreationEvent**</span><span class="sxs-lookup"><span data-stu-id="947cf-137">**\_\_NamespaceCreationEvent**</span></span>](--namespacecreationevent.md)

[<span data-ttu-id="947cf-138">**\_\_NamespaceModificationEvent**</span><span class="sxs-lookup"><span data-stu-id="947cf-138">**\_\_NamespaceModificationEvent**</span></span>](--namespacemodificationevent.md)

[<span data-ttu-id="947cf-139">**\_\_NamespaceDeletionEvent**</span><span class="sxs-lookup"><span data-stu-id="947cf-139">**\_\_NamespaceDeletionEvent**</span></span>](--namespacedeletionevent.md)

## <a name="requirements"></a><span data-ttu-id="947cf-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="947cf-140">Requirements</span></span>



| <span data-ttu-id="947cf-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="947cf-141">Requirement</span></span> | <span data-ttu-id="947cf-142">Valore</span><span class="sxs-lookup"><span data-stu-id="947cf-142">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="947cf-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="947cf-143">Minimum supported client</span></span><br/> | <span data-ttu-id="947cf-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="947cf-144">Windows Vista</span></span><br/>       |
| <span data-ttu-id="947cf-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="947cf-145">Minimum supported server</span></span><br/> | <span data-ttu-id="947cf-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="947cf-146">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="947cf-147">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="947cf-147">Namespace</span></span><br/>                | <span data-ttu-id="947cf-148">Tutti gli spazi dei nomi WMI</span><span class="sxs-lookup"><span data-stu-id="947cf-148">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="947cf-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="947cf-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="947cf-150">**\_\_Evento**</span><span class="sxs-lookup"><span data-stu-id="947cf-150">**\_\_Event**</span></span>](/windows/desktop/WmiSdk/--event)
</dt> <dt>

[<span data-ttu-id="947cf-151">Classi di sistema WMI</span><span class="sxs-lookup"><span data-stu-id="947cf-151">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="947cf-152">Determinazione del tipo di evento da ricevere</span><span class="sxs-lookup"><span data-stu-id="947cf-152">Determining the Type of Event to Receive</span></span>](determining-the-type-of-event-to-receive.md)
</dt> </dl>

 

