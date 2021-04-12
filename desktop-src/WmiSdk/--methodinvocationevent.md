---
description: La \_ \_ classe di sistema MethodInvocationEvent è definita, ma non è implementata.
ms.assetid: ea736e44-a6bc-41e5-abc5-9e21a5504f44
ms.tgt_platform: multiple
title: Classe __MethodInvocationEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __MethodInvocationEvent
- All
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: bc7e8d70d027caf31a90d49abc490c2de2d52fb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232640"
---
# <a name="__methodinvocationevent-class"></a><span data-ttu-id="39964-103">\_\_Classe MethodInvocationEvent</span><span class="sxs-lookup"><span data-stu-id="39964-103">\_\_MethodInvocationEvent class</span></span>

<span data-ttu-id="39964-104">La classe di sistema **\_ \_ MethodInvocationEvent** è definita, ma non è implementata.</span><span class="sxs-lookup"><span data-stu-id="39964-104">The **\_\_MethodInvocationEvent** system class is defined but is not implemented.</span></span>

<span data-ttu-id="39964-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="39964-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="39964-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="39964-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="39964-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="39964-107">Syntax</span></span>

``` syntax
class __MethodInvocationEvent : __InstanceOperationEvent
{
  string       Method;
  __Parameters Parameters;
  boolean      PreCall;
  uint8        SECURITY_DESCRIPTOR[];
  object       TargetInstance;
  uint64       TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="39964-108">Members</span><span class="sxs-lookup"><span data-stu-id="39964-108">Members</span></span>

<span data-ttu-id="39964-109">La classe **\_ \_ MethodInvocationEvent** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="39964-109">The **\_\_MethodInvocationEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="39964-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="39964-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="39964-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="39964-111">Properties</span></span>

<span data-ttu-id="39964-112">La classe **\_ \_ MethodInvocationEvent** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="39964-112">The **\_\_MethodInvocationEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="39964-113">**Metodo**</span><span class="sxs-lookup"><span data-stu-id="39964-113">**Method**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39964-114">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="39964-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39964-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="39964-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39964-116">Metodo richiamato per attivare l'evento.</span><span class="sxs-lookup"><span data-stu-id="39964-116">Method invoked to trigger the event.</span></span>

</dd> <dt>

<span data-ttu-id="39964-117">**Parametri**</span><span class="sxs-lookup"><span data-stu-id="39964-117">**Parameters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39964-118">Tipo di dati: **\_ \_ parametri**</span><span class="sxs-lookup"><span data-stu-id="39964-118">Data type: **\_\_Parameters**</span></span>
</dt> <dt>

<span data-ttu-id="39964-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="39964-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39964-120">Riferimento a un'istanza di che rappresenta i parametri di input e di output della chiamata al metodo.</span><span class="sxs-lookup"><span data-stu-id="39964-120">Reference to an instance that represents the input and output parameters of the method call.</span></span>

</dd> <dt>

<span data-ttu-id="39964-121">**Prechiamata**</span><span class="sxs-lookup"><span data-stu-id="39964-121">**PreCall**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39964-122">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="39964-122">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="39964-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="39964-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39964-124">Se **true**, l'evento viene generato prima che venga chiamato il metodo.</span><span class="sxs-lookup"><span data-stu-id="39964-124">If **TRUE**, the event is raised before the method is called.</span></span>

</dd> <dt>

<span data-ttu-id="39964-125">**descrittore di sicurezza \_**</span><span class="sxs-lookup"><span data-stu-id="39964-125">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39964-126">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="39964-126">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="39964-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="39964-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39964-128">Descrittore utilizzato dal provider di eventi per determinare gli utenti che possono ricevere l'evento.</span><span class="sxs-lookup"><span data-stu-id="39964-128">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="39964-129">Questa proprietà viene ereditata dall' [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="39964-129">This property is inherited from [**\_\_Event**](--event.md).</span></span> <span data-ttu-id="39964-130">Per ulteriori informazioni, vedere [descrittori di sicurezza](/windows/desktop/SecAuthZ/security-descriptors).</span><span class="sxs-lookup"><span data-stu-id="39964-130">For more information, see [Security Descriptors](/windows/desktop/SecAuthZ/security-descriptors).</span></span>

</dd> <dt>

<span data-ttu-id="39964-131">**TargetInstance**</span><span class="sxs-lookup"><span data-stu-id="39964-131">**TargetInstance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39964-132">Tipo di dati: **Object**</span><span class="sxs-lookup"><span data-stu-id="39964-132">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="39964-133">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="39964-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39964-134">Istanza su cui viene richiamato il metodo.</span><span class="sxs-lookup"><span data-stu-id="39964-134">Instance the method is invoked on.</span></span> <span data-ttu-id="39964-135">Questa proprietà viene ereditata da [**\_ \_ InstanceOperationEvent**](--instanceoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="39964-135">This property is inherited from [**\_\_InstanceOperationEvent**](--instanceoperationevent.md).</span></span>

</dd> <dt>

<span data-ttu-id="39964-136">**ORA di \_ creazione**</span><span class="sxs-lookup"><span data-stu-id="39964-136">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39964-137">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="39964-137">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="39964-138">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="39964-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39964-139">Valore univoco che indica l'ora in cui viene generato un evento.</span><span class="sxs-lookup"><span data-stu-id="39964-139">Unique value that indicates the time an event is generated.</span></span> <span data-ttu-id="39964-140">Si tratta di un valore a 64 bit che rappresenta il numero di intervalli di 100-nanosecondi dopo il 1 ° gennaio 1601.</span><span class="sxs-lookup"><span data-stu-id="39964-140">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="39964-141">Le informazioni sono nel formato UTC (Coordinated Universal Time).</span><span class="sxs-lookup"><span data-stu-id="39964-141">The information is in the Coordinated Universal Time (UTC) format.</span></span> <span data-ttu-id="39964-142">Questa proprietà viene ereditata dall' [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="39964-142">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="39964-143">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="39964-143">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="39964-144">Commenti</span><span class="sxs-lookup"><span data-stu-id="39964-144">Remarks</span></span>

<span data-ttu-id="39964-145">La classe **\_ \_ MethodInvocationEvent** deriva da [**\_ \_ InstanceOperationEvent**](--instanceoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="39964-145">The **\_\_MethodInvocationEvent** class is derived from [**\_\_InstanceOperationEvent**](--instanceoperationevent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="39964-146">Requisiti</span><span class="sxs-lookup"><span data-stu-id="39964-146">Requirements</span></span>



| <span data-ttu-id="39964-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="39964-147">Requirement</span></span> | <span data-ttu-id="39964-148">Valore</span><span class="sxs-lookup"><span data-stu-id="39964-148">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="39964-149">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="39964-149">Minimum supported client</span></span><br/> | <span data-ttu-id="39964-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="39964-150">Windows Vista</span></span><br/>       |
| <span data-ttu-id="39964-151">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="39964-151">Minimum supported server</span></span><br/> | <span data-ttu-id="39964-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="39964-152">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="39964-153">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="39964-153">Namespace</span></span><br/>                | <span data-ttu-id="39964-154">Tutti gli spazi dei nomi WMI</span><span class="sxs-lookup"><span data-stu-id="39964-154">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="39964-155">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="39964-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39964-156">**\_\_InstanceOperationEvent**</span><span class="sxs-lookup"><span data-stu-id="39964-156">**\_\_InstanceOperationEvent**</span></span>](/windows/desktop/WmiSdk/--instanceoperationevent)
</dt> <dt>

[<span data-ttu-id="39964-157">Classi di sistema WMI</span><span class="sxs-lookup"><span data-stu-id="39964-157">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

