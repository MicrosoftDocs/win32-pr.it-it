---
description: Segnala un evento di eliminazione dello spazio dei nomi, ovvero un tipo di evento intrinseco generato quando uno spazio dei nomi secondario viene rimosso dallo spazio dei nomi corrente.
ms.assetid: f7160a90-562d-40d9-9189-32aaabcd81d0
ms.tgt_platform: multiple
title: Classe __NamespaceDeletionEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __NamespaceDeletionEvent
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 6e23f909718167760c02bbdb38e2a075d04bc516
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317588"
---
# <a name="__namespacedeletionevent-class"></a><span data-ttu-id="73604-103">\_\_Classe NamespaceDeletionEvent</span><span class="sxs-lookup"><span data-stu-id="73604-103">\_\_NamespaceDeletionEvent class</span></span>

<span data-ttu-id="73604-104">La classe di sistema **\_ \_ NamespaceDeletionEvent** segnala un evento di eliminazione dello spazio dei nomi, ovvero un tipo di [evento intrinseco](determining-the-type-of-event-to-receive.md) generato quando uno spazio dei nomi secondario viene rimosso dallo spazio dei nomi corrente.</span><span class="sxs-lookup"><span data-stu-id="73604-104">The **\_\_NamespaceDeletionEvent** system class reports a namespace deletion event, which is a type of [intrinsic event](determining-the-type-of-event-to-receive.md) that is generated when a sub-namespace is removed from the current namespace.</span></span>

<span data-ttu-id="73604-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="73604-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="73604-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="73604-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="73604-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="73604-107">Syntax</span></span>

``` syntax
class __NamespaceDeletionEvent : __NamespaceOperationEvent
{
  uint8       SECURITY_DESCRIPTOR[];
  __Namespace TargetNamespace;
  uint64      TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="73604-108">Members</span><span class="sxs-lookup"><span data-stu-id="73604-108">Members</span></span>

<span data-ttu-id="73604-109">La classe **\_ \_ NamespaceDeletionEvent** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="73604-109">The **\_\_NamespaceDeletionEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="73604-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="73604-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="73604-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="73604-111">Properties</span></span>

<span data-ttu-id="73604-112">La classe **\_ \_ NamespaceDeletionEvent** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="73604-112">The **\_\_NamespaceDeletionEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="73604-113">**descrittore di sicurezza \_**</span><span class="sxs-lookup"><span data-stu-id="73604-113">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73604-114">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="73604-114">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="73604-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="73604-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73604-116">Descrittore utilizzato dal provider di eventi per determinare gli utenti che possono ricevere un evento.</span><span class="sxs-lookup"><span data-stu-id="73604-116">Descriptor that the event provider uses to determine the users that can receive an event.</span></span> <span data-ttu-id="73604-117">Questa proprietà viene ereditata dall' [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="73604-117">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="73604-118">**TargetNamespace**</span><span class="sxs-lookup"><span data-stu-id="73604-118">**TargetNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73604-119">Tipo di dati: **\_ \_ namespace**</span><span class="sxs-lookup"><span data-stu-id="73604-119">Data type: **\_\_Namespace**</span></span>
</dt> <dt>

<span data-ttu-id="73604-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="73604-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73604-121">Copia dell'istanza [**\_ \_ dello spazio dei nomi**](--namespace.md) eliminata.</span><span class="sxs-lookup"><span data-stu-id="73604-121">Copy of the [**\_\_Namespace**](--namespace.md) instance that is deleted.</span></span> <span data-ttu-id="73604-122">La proprietà **Name** dell'istanza **\_ \_ dello spazio dei nomi** identifica lo spazio dei nomi che viene eliminato.</span><span class="sxs-lookup"><span data-stu-id="73604-122">The **Name** property of the **\_\_Namespace** instance identifies the namespace that is deleted.</span></span> <span data-ttu-id="73604-123">Questa proprietà viene ereditata da [**\_ \_ NamespaceOperationEvent**](--namespaceoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="73604-123">This property is inherited from [**\_\_NamespaceOperationEvent**](--namespaceoperationevent.md).</span></span>

</dd> <dt>

<span data-ttu-id="73604-124">**ORA di \_ creazione**</span><span class="sxs-lookup"><span data-stu-id="73604-124">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73604-125">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="73604-125">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="73604-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="73604-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73604-127">Valore univoco che indica l'ora in cui viene generato un evento.</span><span class="sxs-lookup"><span data-stu-id="73604-127">Unique value that indicates the time an event is generated.</span></span> <span data-ttu-id="73604-128">Si tratta di un valore a 64 bit che rappresenta il numero di intervalli di 100-nanosecondi dopo il 1 ° gennaio 1601.</span><span class="sxs-lookup"><span data-stu-id="73604-128">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="73604-129">Le informazioni sono nel formato UTC (Coordinated Universal Time).</span><span class="sxs-lookup"><span data-stu-id="73604-129">The information is in the Coordinated Universal Time (UTC) format.</span></span> <span data-ttu-id="73604-130">Questa proprietà viene ereditata dall' [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="73604-130">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="73604-131">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="73604-131">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="73604-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="73604-132">Remarks</span></span>

<span data-ttu-id="73604-133">La classe **\_ \_ NamespaceDeletionEvent** deriva da [**\_ \_ NamespaceOperationEvent**](--namespaceoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="73604-133">The **\_\_NamespaceDeletionEvent** class is derived from [**\_\_NamespaceOperationEvent**](--namespaceoperationevent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="73604-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="73604-134">Requirements</span></span>



| <span data-ttu-id="73604-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="73604-135">Requirement</span></span> | <span data-ttu-id="73604-136">Valore</span><span class="sxs-lookup"><span data-stu-id="73604-136">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="73604-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="73604-137">Minimum supported client</span></span><br/> | <span data-ttu-id="73604-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="73604-138">Windows Vista</span></span><br/>       |
| <span data-ttu-id="73604-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="73604-139">Minimum supported server</span></span><br/> | <span data-ttu-id="73604-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="73604-140">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="73604-141">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="73604-141">Namespace</span></span><br/>                | <span data-ttu-id="73604-142">Tutti gli spazi dei nomi WMI</span><span class="sxs-lookup"><span data-stu-id="73604-142">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="73604-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="73604-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73604-144">**\_\_NamespaceOperationEvent**</span><span class="sxs-lookup"><span data-stu-id="73604-144">**\_\_NamespaceOperationEvent**</span></span>](/windows/desktop/WmiSdk/--namespaceoperationevent)
</dt> <dt>

[<span data-ttu-id="73604-145">Classi di sistema WMI</span><span class="sxs-lookup"><span data-stu-id="73604-145">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

