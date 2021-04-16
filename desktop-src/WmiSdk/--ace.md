---
description: Rappresenta una voce di controllo di accesso (ACE, Access Control Entry).
ms.assetid: 47daffd0-b9db-4367-b0b8-654a2da30fed
ms.tgt_platform: multiple
title: Classe __ACE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ACE
- All
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
ms.openlocfilehash: ea2a765225145ce3d44e0aff89aeaca0a7563e0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485756"
---
# <a name="__ace-class"></a><span data-ttu-id="00a5b-103">\_\_ACE (classe)</span><span class="sxs-lookup"><span data-stu-id="00a5b-103">\_\_ACE class</span></span>

<span data-ttu-id="00a5b-104">La classe di sistema **\_ \_ ACE** abstract rappresenta una voce di controllo di accesso ([*ACE*](/windows/desktop/SecGloss/a-gly)).</span><span class="sxs-lookup"><span data-stu-id="00a5b-104">The **\_\_ACE** abstract system class represents an access control entry ([*ACE*](/windows/desktop/SecGloss/a-gly)).</span></span>

<span data-ttu-id="00a5b-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="00a5b-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="00a5b-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="00a5b-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="00a5b-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="00a5b-107">Syntax</span></span>

``` syntax
class  __ACE : __SecurityRelatedClass
{
            AceFlags;
            AccessMask;
            AceType;
            GuidInheritedObjectType;
            GuidObjectType;
  uint64    TIME_CREATED;
  __Trustee Trustee;
};
```

## <a name="members"></a><span data-ttu-id="00a5b-108">Members</span><span class="sxs-lookup"><span data-stu-id="00a5b-108">Members</span></span>

<span data-ttu-id="00a5b-109">La classe **\_ \_ ACE** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="00a5b-109">The **\_\_ACE** class has these types of members:</span></span>

-   [<span data-ttu-id="00a5b-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="00a5b-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="00a5b-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="00a5b-111">Properties</span></span>

<span data-ttu-id="00a5b-112">La classe **\_ \_ ACE** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="00a5b-112">The **\_\_ACE** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="00a5b-113">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="00a5b-113">**AccessMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00a5b-114">Tipo di dati:</span><span class="sxs-lookup"><span data-stu-id="00a5b-114">Data type:</span></span> 
</dt> <dt>

<span data-ttu-id="00a5b-115">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="00a5b-115">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="00a5b-116">Flag di bit che rappresentano i diritti concessi o negati al trustee.</span><span class="sxs-lookup"><span data-stu-id="00a5b-116">Bit flags representing rights that are granted or denied to the trustee.</span></span> <span data-ttu-id="00a5b-117">Per ulteriori informazioni e una descrizione dei flag, vedere la proprietà **accessMask** nella classe [**\_ ACE Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) .</span><span class="sxs-lookup"><span data-stu-id="00a5b-117">For more information and a description of the flags, see **AccessMask** property in the [**Win32\_ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) class.</span></span>

</dd> <dt>

<span data-ttu-id="00a5b-118">**AceFlags**</span><span class="sxs-lookup"><span data-stu-id="00a5b-118">**AceFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00a5b-119">Tipo di dati:</span><span class="sxs-lookup"><span data-stu-id="00a5b-119">Data type:</span></span> 
</dt> <dt>

<span data-ttu-id="00a5b-120">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="00a5b-120">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="00a5b-121">Flag di bit che specificano l'ereditarietà della voce ACE.</span><span class="sxs-lookup"><span data-stu-id="00a5b-121">Bit flags specifying the inheritance of the ACE.</span></span> <span data-ttu-id="00a5b-122">Per ulteriori informazioni e una descrizione dei flag, vedere la proprietà **AceFlags** nella classe [**\_ ACE Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) .</span><span class="sxs-lookup"><span data-stu-id="00a5b-122">For more information and a description of the flags, see **AceFlags** property in the [**Win32\_ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) class.</span></span>

</dd> <dt>

<span data-ttu-id="00a5b-123">**AceType**</span><span class="sxs-lookup"><span data-stu-id="00a5b-123">**AceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00a5b-124">Tipo di dati:</span><span class="sxs-lookup"><span data-stu-id="00a5b-124">Data type:</span></span> 
</dt> <dt>

<span data-ttu-id="00a5b-125">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="00a5b-125">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="00a5b-126">Tipo di voce ACE rappresentata da questa istanza.</span><span class="sxs-lookup"><span data-stu-id="00a5b-126">The type of ACE entry that this instance represents.</span></span>

</dd> <dt>

<span data-ttu-id="00a5b-127">**GuidInheritedObjectType**</span><span class="sxs-lookup"><span data-stu-id="00a5b-127">**GuidInheritedObjectType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00a5b-128">Tipo di dati:</span><span class="sxs-lookup"><span data-stu-id="00a5b-128">Data type:</span></span> 
</dt> <dt>

<span data-ttu-id="00a5b-129">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="00a5b-129">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="00a5b-130">GUID dell'elemento padre dell'oggetto a cui si applicano i diritti di accesso nella proprietà **accessMask** .</span><span class="sxs-lookup"><span data-stu-id="00a5b-130">The GUID of the parent of the object to which the access rights in the **AccessMask** property apply.</span></span>

</dd> <dt>

<span data-ttu-id="00a5b-131">**GuidObjectType**</span><span class="sxs-lookup"><span data-stu-id="00a5b-131">**GuidObjectType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00a5b-132">Tipo di dati:</span><span class="sxs-lookup"><span data-stu-id="00a5b-132">Data type:</span></span> 
</dt> <dt>

<span data-ttu-id="00a5b-133">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="00a5b-133">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="00a5b-134">GUID che indica il tipo di oggetto a cui si applicano i diritti nella proprietà **accessMask** .</span><span class="sxs-lookup"><span data-stu-id="00a5b-134">The GUID that indicates the type of object to which the rights in the **AccessMask** property apply.</span></span>

</dd> <dt>

<span data-ttu-id="00a5b-135">**ORA di \_ creazione**</span><span class="sxs-lookup"><span data-stu-id="00a5b-135">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00a5b-136">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="00a5b-136">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="00a5b-137">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="00a5b-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00a5b-138">Ora, nel formato [ \_ DateTime CIM](cim-datetime.md) , in cui è stato creato il descrittore di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="00a5b-138">The time, in the [CIM\_DATETIME](cim-datetime.md) format, when the security descriptor was created.</span></span>

</dd> <dt>

<span data-ttu-id="00a5b-139">**Fiduciario**</span><span class="sxs-lookup"><span data-stu-id="00a5b-139">**Trustee**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00a5b-140">Tipo di dati: **[ **\_ \_ trustee**](--trustee.md)**</span><span class="sxs-lookup"><span data-stu-id="00a5b-140">Data type: **[**\_\_Trustee**](--trustee.md)**</span></span>
</dt> <dt>

<span data-ttu-id="00a5b-141">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="00a5b-141">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="00a5b-142">Il trustee della voce ACE rappresentata da questa istanza della classe **\_ \_ ACE** .</span><span class="sxs-lookup"><span data-stu-id="00a5b-142">The trustee of the ACE entry represented by this instance of the **\_\_ACE** class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="00a5b-143">Commenti</span><span class="sxs-lookup"><span data-stu-id="00a5b-143">Remarks</span></span>

<span data-ttu-id="00a5b-144">Questa classe fornisce le proprietà ereditate dalla classe [**\_ ACE Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) , che è un membro della classe [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) .</span><span class="sxs-lookup"><span data-stu-id="00a5b-144">This class provides the properties that are inherited by the [**Win32\_ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) class, which is a member of the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) class.</span></span> <span data-ttu-id="00a5b-145">Per ulteriori informazioni, vedere [oggetti del descrittore di sicurezza WMI](wmi-security-descriptor-objects.md) e [modifica della sicurezza di accesso per gli oggetti a protezione diretta](changing-access-security-on-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="00a5b-145">For more information, see [WMI Security Descriptor Objects](wmi-security-descriptor-objects.md) and [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span> <span data-ttu-id="00a5b-146">Per ulteriori informazioni sulle voci ACE, vedere [Access Control Components](/windows/desktop/SecAuthZ/access-control-components).</span><span class="sxs-lookup"><span data-stu-id="00a5b-146">For more information about ACEs, see [Access Control Components](/windows/desktop/SecAuthZ/access-control-components).</span></span>

## <a name="requirements"></a><span data-ttu-id="00a5b-147">Requisiti</span><span class="sxs-lookup"><span data-stu-id="00a5b-147">Requirements</span></span>



| <span data-ttu-id="00a5b-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="00a5b-148">Requirement</span></span> | <span data-ttu-id="00a5b-149">Valore</span><span class="sxs-lookup"><span data-stu-id="00a5b-149">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="00a5b-150">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="00a5b-150">Minimum supported client</span></span><br/> | <span data-ttu-id="00a5b-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="00a5b-151">Windows Vista</span></span><br/>       |
| <span data-ttu-id="00a5b-152">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="00a5b-152">Minimum supported server</span></span><br/> | <span data-ttu-id="00a5b-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="00a5b-153">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="00a5b-154">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="00a5b-154">Namespace</span></span><br/>                | <span data-ttu-id="00a5b-155">Tutti gli spazi dei nomi WMI</span><span class="sxs-lookup"><span data-stu-id="00a5b-155">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="00a5b-156">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="00a5b-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00a5b-157">**\_\_SecurityRelatedClass**</span><span class="sxs-lookup"><span data-stu-id="00a5b-157">**\_\_SecurityRelatedClass**</span></span>](--securityrelatedclass.md)
</dt> <dt>

[<span data-ttu-id="00a5b-158">Classi di sistema WMI</span><span class="sxs-lookup"><span data-stu-id="00a5b-158">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="00a5b-159">**\_ACE Win32**</span><span class="sxs-lookup"><span data-stu-id="00a5b-159">**Win32\_ACE**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
</dt> <dt>

[<span data-ttu-id="00a5b-160">Gestione della sicurezza WMI</span><span class="sxs-lookup"><span data-stu-id="00a5b-160">Maintaining WMI Security</span></span>](maintaining-wmi-security.md)
</dt> </dl>

 

