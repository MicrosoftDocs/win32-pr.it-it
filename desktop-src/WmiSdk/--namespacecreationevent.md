---
description: Segnala un evento di creazione dello spazio dei nomi, ovvero un tipo di evento intrinseco generato quando un nuovo spazio dei nomi viene aggiunto allo spazio dei nomi corrente.
ms.assetid: 50b9860a-d6e8-4dab-a7d0-09da9dd37b6b
ms.tgt_platform: multiple
title: Classe __NamespaceCreationEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __NamespaceCreationEvent
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 8432bcfb2c96c70b91a7f0d187297217082e2d28
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314095"
---
# <a name="__namespacecreationevent-class"></a><span data-ttu-id="5cc38-103">\_\_Classe NamespaceCreationEvent</span><span class="sxs-lookup"><span data-stu-id="5cc38-103">\_\_NamespaceCreationEvent class</span></span>

<span data-ttu-id="5cc38-104">La classe di sistema **\_ \_ NamespaceCreationEvent** segnala un evento di creazione dello spazio dei nomi, ovvero un tipo di [evento intrinseco](determining-the-type-of-event-to-receive.md) generato quando un nuovo spazio dei nomi viene aggiunto allo spazio dei nomi corrente.</span><span class="sxs-lookup"><span data-stu-id="5cc38-104">The **\_\_NamespaceCreationEvent** system class reports a namespace creation event, which is a type of [intrinsic event](determining-the-type-of-event-to-receive.md) generated when a new namespace is added to the current namespace.</span></span>

<span data-ttu-id="5cc38-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="5cc38-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="5cc38-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="5cc38-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5cc38-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5cc38-107">Syntax</span></span>

``` syntax
class __NamespaceCreationEvent : __NamespaceOperationEvent
{
  uint8       SECURITY_DESCRIPTOR[];
  __Namespace TargetNamespace;
  uint64      TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="5cc38-108">Members</span><span class="sxs-lookup"><span data-stu-id="5cc38-108">Members</span></span>

<span data-ttu-id="5cc38-109">La classe **\_ \_ NamespaceCreationEvent** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="5cc38-109">The **\_\_NamespaceCreationEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="5cc38-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5cc38-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5cc38-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5cc38-111">Properties</span></span>

<span data-ttu-id="5cc38-112">La classe **\_ \_ NamespaceCreationEvent** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="5cc38-112">The **\_\_NamespaceCreationEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5cc38-113">**descrittore di sicurezza \_**</span><span class="sxs-lookup"><span data-stu-id="5cc38-113">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cc38-114">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="5cc38-114">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="5cc38-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5cc38-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5cc38-116">Descrittore utilizzato dal provider di eventi per determinare gli utenti che possono ricevere l'evento.</span><span class="sxs-lookup"><span data-stu-id="5cc38-116">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="5cc38-117">Questa proprietà viene ereditata dall' [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="5cc38-117">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="5cc38-118">**TargetNamespace**</span><span class="sxs-lookup"><span data-stu-id="5cc38-118">**TargetNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cc38-119">Tipo di dati: **\_ \_ namespace**</span><span class="sxs-lookup"><span data-stu-id="5cc38-119">Data type: **\_\_Namespace**</span></span>
</dt> <dt>

<span data-ttu-id="5cc38-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5cc38-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5cc38-121">Copia dell'istanza [**\_ \_ dello spazio dei nomi**](--namespace.md) creata.</span><span class="sxs-lookup"><span data-stu-id="5cc38-121">Copy of the [**\_\_Namespace**](--namespace.md) instance that was created.</span></span> <span data-ttu-id="5cc38-122">La proprietà **Name** dell'istanza **\_ \_ dello spazio dei nomi** indica quale spazio dei nomi è stato creato.</span><span class="sxs-lookup"><span data-stu-id="5cc38-122">The **Name** property of the **\_\_Namespace** instance indicates which namespace was created.</span></span> <span data-ttu-id="5cc38-123">Questa proprietà viene ereditata da [**\_ \_ NamespaceOperationEvent**](--namespaceoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="5cc38-123">This property is inherited from [**\_\_NamespaceOperationEvent**](--namespaceoperationevent.md).</span></span>

</dd> <dt>

<span data-ttu-id="5cc38-124">**ORA di \_ creazione**</span><span class="sxs-lookup"><span data-stu-id="5cc38-124">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cc38-125">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5cc38-125">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5cc38-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5cc38-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5cc38-127">Valore univoco che indica l'ora in cui è stato generato l'evento.</span><span class="sxs-lookup"><span data-stu-id="5cc38-127">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="5cc38-128">Si tratta di un valore a 64 bit che rappresenta il numero di intervalli di 100-nanosecondi dopo il 1 ° gennaio 1601.</span><span class="sxs-lookup"><span data-stu-id="5cc38-128">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="5cc38-129">Le informazioni sono nel formato UTC (Coordinated Universal Time).</span><span class="sxs-lookup"><span data-stu-id="5cc38-129">The information is in the Coordinated Universal Time (UTC) format.</span></span> <span data-ttu-id="5cc38-130">Questa proprietà viene ereditata dall' [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="5cc38-130">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="5cc38-131">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="5cc38-131">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5cc38-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="5cc38-132">Remarks</span></span>

<span data-ttu-id="5cc38-133">La classe **\_ \_ NamespaceCreationEvent** deriva da [**\_ \_ NamespaceOperationEvent**](--namespaceoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="5cc38-133">The **\_\_NamespaceCreationEvent** class is derived from [**\_\_NamespaceOperationEvent**](--namespaceoperationevent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5cc38-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5cc38-134">Requirements</span></span>



| <span data-ttu-id="5cc38-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="5cc38-135">Requirement</span></span> | <span data-ttu-id="5cc38-136">Valore</span><span class="sxs-lookup"><span data-stu-id="5cc38-136">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="5cc38-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5cc38-137">Minimum supported client</span></span><br/> | <span data-ttu-id="5cc38-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5cc38-138">Windows Vista</span></span><br/>       |
| <span data-ttu-id="5cc38-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5cc38-139">Minimum supported server</span></span><br/> | <span data-ttu-id="5cc38-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5cc38-140">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="5cc38-141">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5cc38-141">Namespace</span></span><br/>                | <span data-ttu-id="5cc38-142">Tutti gli spazi dei nomi WMI</span><span class="sxs-lookup"><span data-stu-id="5cc38-142">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="5cc38-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5cc38-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5cc38-144">**\_\_NamespaceOperationEvent**</span><span class="sxs-lookup"><span data-stu-id="5cc38-144">**\_\_NamespaceOperationEvent**</span></span>](/windows/desktop/WmiSdk/--namespaceoperationevent)
</dt> <dt>

[<span data-ttu-id="5cc38-145">Classi di sistema WMI</span><span class="sxs-lookup"><span data-stu-id="5cc38-145">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

