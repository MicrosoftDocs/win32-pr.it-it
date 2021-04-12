---
description: Rappresenta un descrittore di sicurezza.
ms.assetid: 1ade1751-52a2-4ada-8255-323321111663
ms.tgt_platform: multiple
title: Classe __SecurityDescriptor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SecurityDescriptor
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
ms.openlocfilehash: 5f305387a29d1d1569addafd127f53c98246e1a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231826"
---
# <a name="__securitydescriptor-class"></a><span data-ttu-id="a7d7a-103">\_\_Classe SecurityDescriptor</span><span class="sxs-lookup"><span data-stu-id="a7d7a-103">\_\_SecurityDescriptor class</span></span>

<span data-ttu-id="a7d7a-104">La classe di sistema astratta **\_ \_ securityDescriptor** rappresenta un [*descrittore di sicurezza*](/windows/desktop/SecGloss/s-gly).</span><span class="sxs-lookup"><span data-stu-id="a7d7a-104">The **\_\_SecurityDescriptor** abstract system class represents a [*security descriptor*](/windows/desktop/SecGloss/s-gly).</span></span>

<span data-ttu-id="a7d7a-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="a7d7a-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="a7d7a-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="a7d7a-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7d7a-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a7d7a-107">Syntax</span></span>

``` syntax
class __SecurityDescriptor
{
  uint32 ControlFlags;
  __ACE  DACL[];
  __ACE  Group;
  __ACE  Owner;
  __ACE  SACL;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="a7d7a-108">Members</span><span class="sxs-lookup"><span data-stu-id="a7d7a-108">Members</span></span>

<span data-ttu-id="a7d7a-109">La classe **\_ \_ securityDescriptor** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="a7d7a-109">The **\_\_SecurityDescriptor** class has these types of members:</span></span>

-   [<span data-ttu-id="a7d7a-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a7d7a-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a7d7a-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a7d7a-111">Properties</span></span>

<span data-ttu-id="a7d7a-112">La classe **\_ \_ securityDescriptor** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="a7d7a-112">The **\_\_SecurityDescriptor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a7d7a-113">**ControlFlags**</span><span class="sxs-lookup"><span data-stu-id="a7d7a-113">**ControlFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7d7a-114">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a7d7a-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a7d7a-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a7d7a-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a7d7a-116">Flag di bit che forniscono informazioni sul contenuto e sul formato del descrittore.</span><span class="sxs-lookup"><span data-stu-id="a7d7a-116">Bit flags that provide information about the descriptor's contents and format.</span></span> <span data-ttu-id="a7d7a-117">Per una descrizione dei flag, vedere la proprietà **ControlFlags** nella classe [**\_ securityDescriptor Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) .</span><span class="sxs-lookup"><span data-stu-id="a7d7a-117">See the **ControlFlags** property in the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) class for a description of the flags.</span></span>

</dd> <dt>

<span data-ttu-id="a7d7a-118">**DACL**</span><span class="sxs-lookup"><span data-stu-id="a7d7a-118">**DACL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7d7a-119">Tipo di dati: matrice **[**\_ \_ ACE**](--ace.md)**</span><span class="sxs-lookup"><span data-stu-id="a7d7a-119">Data type: **[**\_\_ACE**](--ace.md)** array</span></span>
</dt> <dt>

<span data-ttu-id="a7d7a-120">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="a7d7a-120">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a7d7a-121">Matrice di voci [**\_ \_ ACE**](--ace.md) che specificano l'accesso all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a7d7a-121">An array of [**\_\_ACE**](--ace.md) entries that specify access to the object.</span></span>

</dd> <dt>

<span data-ttu-id="a7d7a-122">**Gruppo**</span><span class="sxs-lookup"><span data-stu-id="a7d7a-122">**Group**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7d7a-123">Tipo di dati: **[ **\_ \_ ACE**](--ace.md)**</span><span class="sxs-lookup"><span data-stu-id="a7d7a-123">Data type: **[**\_\_ACE**](--ace.md)**</span></span>
</dt> <dt>

<span data-ttu-id="a7d7a-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a7d7a-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a7d7a-125">ACE che identifica il trustee che rappresenta il gruppo dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a7d7a-125">ACE that identifies the trustee representing the group of the object.</span></span>

</dd> <dt>

<span data-ttu-id="a7d7a-126">**Proprietario**</span><span class="sxs-lookup"><span data-stu-id="a7d7a-126">**Owner**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7d7a-127">Tipo di dati: **[ **\_ \_ ACE**](--ace.md)**</span><span class="sxs-lookup"><span data-stu-id="a7d7a-127">Data type: **[**\_\_ACE**](--ace.md)**</span></span>
</dt> <dt>

<span data-ttu-id="a7d7a-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a7d7a-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a7d7a-129">ACE che identifica il trustee che rappresenta il proprietario dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a7d7a-129">ACE that identifies the trustee representing the owner of the object.</span></span>

</dd> <dt>

<span data-ttu-id="a7d7a-130">**SACL**</span><span class="sxs-lookup"><span data-stu-id="a7d7a-130">**SACL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7d7a-131">Tipo di dati: **[ **\_ \_ ACE**](--ace.md)**</span><span class="sxs-lookup"><span data-stu-id="a7d7a-131">Data type: **[**\_\_ACE**](--ace.md)**</span></span>
</dt> <dt>

<span data-ttu-id="a7d7a-132">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a7d7a-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a7d7a-133">Matrice di voci [**\_ \_ ACE**](--ace.md) che identifica gli utenti e i gruppi per i quali vengono raccolte le informazioni di controllo.</span><span class="sxs-lookup"><span data-stu-id="a7d7a-133">An array of [**\_\_ACE**](--ace.md) entries that identifies users and groups for which auditing information is gathered.</span></span>

</dd> <dt>

<span data-ttu-id="a7d7a-134">**ORA di \_ creazione**</span><span class="sxs-lookup"><span data-stu-id="a7d7a-134">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7d7a-135">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a7d7a-135">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a7d7a-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a7d7a-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a7d7a-137">Ora nel formato [CIM \_ DateTime](cim-datetime.md) quando è stato creato il descrittore di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="a7d7a-137">Time in the [CIM\_DATETIME](cim-datetime.md) format when the security descriptor was created.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a7d7a-138">Commenti</span><span class="sxs-lookup"><span data-stu-id="a7d7a-138">Remarks</span></span>

<span data-ttu-id="a7d7a-139">Questa classe fornisce le proprietà ereditate da [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span><span class="sxs-lookup"><span data-stu-id="a7d7a-139">This class provides properties inherited by [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span> <span data-ttu-id="a7d7a-140">Per ulteriori informazioni, vedere [oggetti del descrittore di sicurezza WMI](wmi-security-descriptor-objects.md) e [modifica della sicurezza di accesso per gli oggetti a protezione diretta](changing-access-security-on-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="a7d7a-140">For more information, see [WMI Security Descriptor Objects](wmi-security-descriptor-objects.md) and [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span> <span data-ttu-id="a7d7a-141">Per ulteriori informazioni sulle voci ACE, vedere [Access Control Components](/windows/desktop/SecAuthZ/access-control-components).</span><span class="sxs-lookup"><span data-stu-id="a7d7a-141">For more information about ACEs, see [Access Control Components](/windows/desktop/SecAuthZ/access-control-components).</span></span>

## <a name="requirements"></a><span data-ttu-id="a7d7a-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a7d7a-142">Requirements</span></span>



| <span data-ttu-id="a7d7a-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7d7a-143">Requirement</span></span> | <span data-ttu-id="a7d7a-144">Valore</span><span class="sxs-lookup"><span data-stu-id="a7d7a-144">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="a7d7a-145">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a7d7a-145">Minimum supported client</span></span><br/> | <span data-ttu-id="a7d7a-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a7d7a-146">Windows Vista</span></span><br/>       |
| <span data-ttu-id="a7d7a-147">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a7d7a-147">Minimum supported server</span></span><br/> | <span data-ttu-id="a7d7a-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a7d7a-148">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="a7d7a-149">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a7d7a-149">Namespace</span></span><br/>                | <span data-ttu-id="a7d7a-150">Tutti gli spazi dei nomi WMI</span><span class="sxs-lookup"><span data-stu-id="a7d7a-150">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="a7d7a-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a7d7a-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7d7a-152">Classi di sistema WMI</span><span class="sxs-lookup"><span data-stu-id="a7d7a-152">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="a7d7a-153">**\_SecurityDescriptor Win32**</span><span class="sxs-lookup"><span data-stu-id="a7d7a-153">**Win32\_SecurityDescriptor**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
</dt> <dt>

[<span data-ttu-id="a7d7a-154">Gestione della sicurezza WMI</span><span class="sxs-lookup"><span data-stu-id="a7d7a-154">Maintaining WMI Security</span></span>](maintaining-wmi-security.md)
</dt> </dl>

 

