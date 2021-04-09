---
description: Segnala un evento di modifica dello spazio dei nomi, ovvero un tipo di evento intrinseco che viene generato quando viene modificato uno spazio dei nomi.
ms.assetid: 168505d7-4677-4f41-935e-149f22de2cb5
ms.tgt_platform: multiple
title: Classe __NamespaceModificationEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __NamespaceModificationEvent
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 5af5783d3ebfbfb4b7842cb86b1919f8dbed1365
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759443"
---
# <a name="__namespacemodificationevent-class"></a><span data-ttu-id="33a38-103">\_\_Classe NamespaceModificationEvent</span><span class="sxs-lookup"><span data-stu-id="33a38-103">\_\_NamespaceModificationEvent class</span></span>

<span data-ttu-id="33a38-104">La classe di sistema **\_ \_ NamespaceModificationEvent** segnala un evento di modifica dello spazio dei nomi, ovvero un tipo di [evento intrinseco](determining-the-type-of-event-to-receive.md) che viene generato quando viene modificato uno spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="33a38-104">The **\_\_NamespaceModificationEvent** system class reports a namespace modification event, which is a type of [intrinsic event](determining-the-type-of-event-to-receive.md) that is generated when a namespace is modified.</span></span>

<span data-ttu-id="33a38-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="33a38-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="33a38-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="33a38-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="33a38-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="33a38-107">Syntax</span></span>

``` syntax
class __NamespaceModificationEvent : __NamespaceOperationEvent
{
  uint8       SECURITY_DESCRIPTOR[];
  __Namespace PreviousNamespace;
  uint8       SECURITY_DESCRIPTOR [];
  __Namespace TargetNamespace;
  uint64      TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="33a38-108">Members</span><span class="sxs-lookup"><span data-stu-id="33a38-108">Members</span></span>

<span data-ttu-id="33a38-109">La classe **\_ \_ NamespaceModificationEvent** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="33a38-109">The **\_\_NamespaceModificationEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="33a38-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="33a38-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="33a38-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="33a38-111">Properties</span></span>

<span data-ttu-id="33a38-112">La classe **\_ \_ NamespaceModificationEvent** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="33a38-112">The **\_\_NamespaceModificationEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="33a38-113">**PreviousNamespace**</span><span class="sxs-lookup"><span data-stu-id="33a38-113">**PreviousNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33a38-114">Tipo di dati: **\_ \_ namespace**</span><span class="sxs-lookup"><span data-stu-id="33a38-114">Data type: **\_\_Namespace**</span></span>
</dt> <dt>

<span data-ttu-id="33a38-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="33a38-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="33a38-116">Copia della versione originale di un'istanza [**\_ \_ dello spazio dei nomi**](--namespace.md) .</span><span class="sxs-lookup"><span data-stu-id="33a38-116">Copy of the original version of a [**\_\_Namespace**](--namespace.md) instance.</span></span> <span data-ttu-id="33a38-117">La proprietà **Name** di questa istanza identifica lo spazio dei nomi che viene modificato.</span><span class="sxs-lookup"><span data-stu-id="33a38-117">The **Name** property of this instance identifies the namespace that is modified.</span></span>

</dd> <dt>

<span data-ttu-id="33a38-118">**descrittore di sicurezza \_**</span><span class="sxs-lookup"><span data-stu-id="33a38-118">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33a38-119">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="33a38-119">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="33a38-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="33a38-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="33a38-121">Descrittore utilizzato dal provider di eventi per determinare gli utenti che possono ricevere l'evento.</span><span class="sxs-lookup"><span data-stu-id="33a38-121">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="33a38-122">Questa proprietà viene ereditata dall' [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="33a38-122">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="33a38-123">**descrittore di sicurezza \_**</span><span class="sxs-lookup"><span data-stu-id="33a38-123">**SECURITY\_DESCRIPTOR**</span></span> 
</dt> <dd> <dl> <dt>

<span data-ttu-id="33a38-124">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="33a38-124">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="33a38-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="33a38-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="33a38-126">Descrittore utilizzato dal provider di eventi per determinare gli utenti che possono ricevere un evento.</span><span class="sxs-lookup"><span data-stu-id="33a38-126">Descriptor that the event provider uses to determine the users that can receive an event.</span></span> <span data-ttu-id="33a38-127">Questa proprietà viene ereditata dall' [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="33a38-127">This property is inherited from [**\_\_Event**](--event.md).</span></span>

> [!Note]  
> <span data-ttu-id="33a38-128">Un  elenco di controllo di accesso (ACL) null [**nel \_ descrittore di sicurezza**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) concede un accesso illimitato a tutti i tempi.</span><span class="sxs-lookup"><span data-stu-id="33a38-128">A **NULL** access control list (ACL) in the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) grants unlimited access to everyone all the time.</span></span> <span data-ttu-id="33a38-129">Per ulteriori informazioni, vedere [creazione di un descrittore di sicurezza per un nuovo oggetto](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span><span class="sxs-lookup"><span data-stu-id="33a38-129">For more information, see [Creating a Security Descriptor for a New Object](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span></span>

 

</dd> <dt>

<span data-ttu-id="33a38-130">**TargetNamespace**</span><span class="sxs-lookup"><span data-stu-id="33a38-130">**TargetNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33a38-131">Tipo di dati: **\_ \_ namespace**</span><span class="sxs-lookup"><span data-stu-id="33a38-131">Data type: **\_\_Namespace**</span></span>
</dt> <dt>

<span data-ttu-id="33a38-132">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="33a38-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="33a38-133">Copia dell'istanza [**\_ \_ dello spazio dei nomi**](--namespace.md) modificata.</span><span class="sxs-lookup"><span data-stu-id="33a38-133">Copy of the [**\_\_Namespace**](--namespace.md) instance that is modified.</span></span> <span data-ttu-id="33a38-134">La proprietà **Name** dell'istanza **\_ \_ dello spazio dei nomi** indica lo spazio dei nomi modificato.</span><span class="sxs-lookup"><span data-stu-id="33a38-134">The **Name** property of the **\_\_Namespace** instance indicates the namespace that is modified.</span></span> <span data-ttu-id="33a38-135">Questa proprietà viene ereditata dalla classe [**\_ \_ NamespaceOperationEvent**](--namespaceoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="33a38-135">This property is inherited from class [**\_\_NamespaceOperationEvent**](--namespaceoperationevent.md).</span></span>

</dd> <dt>

<span data-ttu-id="33a38-136">**ORA di \_ creazione**</span><span class="sxs-lookup"><span data-stu-id="33a38-136">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33a38-137">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="33a38-137">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="33a38-138">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="33a38-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="33a38-139">Valore univoco che indica l'ora in cui viene generato un evento.</span><span class="sxs-lookup"><span data-stu-id="33a38-139">Unique value that indicates the time that an event is generated.</span></span> <span data-ttu-id="33a38-140">Si tratta di un valore a 64 bit che rappresenta il numero di intervalli di 100-nanosecondi dopo il 1 ° gennaio 1601.</span><span class="sxs-lookup"><span data-stu-id="33a38-140">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="33a38-141">Le informazioni sono nel formato UTC (Coordinated Universal Time).</span><span class="sxs-lookup"><span data-stu-id="33a38-141">The information is in the Coordinated Universal Time (UTC) format.</span></span> <span data-ttu-id="33a38-142">Questa proprietà viene ereditata dall' [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="33a38-142">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="33a38-143">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="33a38-143">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="33a38-144">Commenti</span><span class="sxs-lookup"><span data-stu-id="33a38-144">Remarks</span></span>

<span data-ttu-id="33a38-145">La classe **\_ \_ NamespaceModificationEvent** deriva da [**\_ \_ NamespaceOperationEvent**](--namespaceoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="33a38-145">The **\_\_NamespaceModificationEvent** class is derived from [**\_\_NamespaceOperationEvent**](--namespaceoperationevent.md).</span></span>

<span data-ttu-id="33a38-146">Le uniche differenze tra lo spazio dei nomi di destinazione e lo spazio dei nomi precedente sono i qualificatori e le proprietà eccetto [**Name**](--namespace.md).</span><span class="sxs-lookup"><span data-stu-id="33a38-146">The only differences between the target namespace and the previous namespace is the qualifiers and properties except [**Name**](--namespace.md).</span></span>

<span data-ttu-id="33a38-147">Si noti che la proprietà [**Name**](--namespace.md) di un'istanza **\_ \_ dello spazio dei nomi** non può essere modificata perché gli spazi dei nomi non possono essere rinominati.</span><span class="sxs-lookup"><span data-stu-id="33a38-147">Note that the [**Name**](--namespace.md) property of a **\_\_Namespace** instance cannot change because namespaces cannot be renamed.</span></span> <span data-ttu-id="33a38-148">Per modificare il nome di uno spazio dei nomi, l'istanza **\_ \_ dello spazio dei nomi** deve essere eliminata e ricreata con un nuovo nome.</span><span class="sxs-lookup"><span data-stu-id="33a38-148">To modify the name of a namespace, the **\_\_Namespace** instance must be deleted and re-created with a new name.</span></span> <span data-ttu-id="33a38-149">Gli eventi di modifica dello spazio dei nomi vengono pertanto generati quando si verifica una modifica a qualificatori e proprietà diverse dal **nome**.</span><span class="sxs-lookup"><span data-stu-id="33a38-149">Therefore, namespace modification events are generated when a change occurs to qualifiers and properties other than **Name**.</span></span> <span data-ttu-id="33a38-150">Un evento di modifica dello spazio dei nomi non viene generato quando si verifica un qualsiasi tipo di modifica nello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="33a38-150">A namespace modification event is not generated when any kind of change occurs within the namespace.</span></span> <span data-ttu-id="33a38-151">Un evento di modifica dello spazio dei nomi viene generato solo quando viene modificata un'istanza dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="33a38-151">A namespace modification event is generated only when a namespace instance is modified.</span></span>

## <a name="requirements"></a><span data-ttu-id="33a38-152">Requisiti</span><span class="sxs-lookup"><span data-stu-id="33a38-152">Requirements</span></span>



| <span data-ttu-id="33a38-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="33a38-153">Requirement</span></span> | <span data-ttu-id="33a38-154">Valore</span><span class="sxs-lookup"><span data-stu-id="33a38-154">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="33a38-155">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="33a38-155">Minimum supported client</span></span><br/> | <span data-ttu-id="33a38-156">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="33a38-156">Windows Vista</span></span><br/>       |
| <span data-ttu-id="33a38-157">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="33a38-157">Minimum supported server</span></span><br/> | <span data-ttu-id="33a38-158">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="33a38-158">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="33a38-159">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="33a38-159">Namespace</span></span><br/>                | <span data-ttu-id="33a38-160">Tutti gli spazi dei nomi WMI</span><span class="sxs-lookup"><span data-stu-id="33a38-160">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="33a38-161">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="33a38-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33a38-162">**\_\_NamespaceOperationEvent**</span><span class="sxs-lookup"><span data-stu-id="33a38-162">**\_\_NamespaceOperationEvent**</span></span>](/windows/desktop/WmiSdk/--namespaceoperationevent)
</dt> <dt>

[<span data-ttu-id="33a38-163">Classi di sistema WMI</span><span class="sxs-lookup"><span data-stu-id="33a38-163">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

