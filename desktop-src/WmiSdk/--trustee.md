---
description: La \_ \_ classe di sistema astratta trustee rappresenta un trustee. È possibile utilizzare un nome o un SID (matrice di byte).
ms.assetid: 92d17c7c-ebca-4dd0-80d8-6edd999ca394
ms.tgt_platform: multiple
title: Classe __Trustee
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __Trustee
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
ms.openlocfilehash: 5c6ba04760e924ffe9d86916cffdb82ea2488219
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530367"
---
# <a name="__trustee-class"></a><span data-ttu-id="2c35d-104">\_\_Classe Trustee</span><span class="sxs-lookup"><span data-stu-id="2c35d-104">\_\_Trustee class</span></span>

<span data-ttu-id="2c35d-105">La classe di sistema astratta [**\_ \_ trustee**](--securitydescriptor.md) rappresenta un [*trustee*](/windows/desktop/SecGloss/t-gly).</span><span class="sxs-lookup"><span data-stu-id="2c35d-105">The [**\_\_Trustee**](--securitydescriptor.md) abstract system class represents a [*trustee*](/windows/desktop/SecGloss/t-gly).</span></span> <span data-ttu-id="2c35d-106">È possibile utilizzare un nome o un SID (matrice di byte).</span><span class="sxs-lookup"><span data-stu-id="2c35d-106">Either a name or an SID (byte array) can be used.</span></span>

<span data-ttu-id="2c35d-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="2c35d-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="2c35d-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="2c35d-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c35d-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2c35d-109">Syntax</span></span>

``` syntax
class __Trustee
{
  string Domain;
  string Name;
  uint8  SID[];
  uint32 SidLength;
  string SidString;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="2c35d-110">Members</span><span class="sxs-lookup"><span data-stu-id="2c35d-110">Members</span></span>

<span data-ttu-id="2c35d-111">La classe **\_ \_ trustee** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="2c35d-111">The **\_\_Trustee** class has these types of members:</span></span>

-   [<span data-ttu-id="2c35d-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2c35d-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2c35d-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2c35d-113">Properties</span></span>

<span data-ttu-id="2c35d-114">La classe **\_ \_ trustee** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="2c35d-114">The **\_\_Trustee** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2c35d-115">**Dominio**</span><span class="sxs-lookup"><span data-stu-id="2c35d-115">**Domain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c35d-116">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2c35d-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c35d-117">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="2c35d-117">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2c35d-118">Parte di dominio dell'account.</span><span class="sxs-lookup"><span data-stu-id="2c35d-118">Domain portion of the account.</span></span>

</dd> <dt>

<span data-ttu-id="2c35d-119">**Nome**</span><span class="sxs-lookup"><span data-stu-id="2c35d-119">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c35d-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2c35d-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c35d-121">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="2c35d-121">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2c35d-122">Parte relativa al nome dell'account.</span><span class="sxs-lookup"><span data-stu-id="2c35d-122">Name portion of the account.</span></span>

</dd> <dt>

<span data-ttu-id="2c35d-123">**SID**</span><span class="sxs-lookup"><span data-stu-id="2c35d-123">**SID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c35d-124">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="2c35d-124">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="2c35d-125">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="2c35d-125">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2c35d-126">SID del trustee nel formato della matrice di byte binari.</span><span class="sxs-lookup"><span data-stu-id="2c35d-126">The SID of the trustee in the binary byte array form.</span></span>

</dd> <dt>

<span data-ttu-id="2c35d-127">**SidLength**</span><span class="sxs-lookup"><span data-stu-id="2c35d-127">**SidLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c35d-128">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2c35d-128">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2c35d-129">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="2c35d-129">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2c35d-130">Lunghezza in byte del SID.</span><span class="sxs-lookup"><span data-stu-id="2c35d-130">The length of the SID in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="2c35d-131">**SidString**</span><span class="sxs-lookup"><span data-stu-id="2c35d-131">**SidString**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c35d-132">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2c35d-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c35d-133">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="2c35d-133">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2c35d-134">SID del trustee nel formato stringa, ad esempio "S-1-1-0".</span><span class="sxs-lookup"><span data-stu-id="2c35d-134">The SID of the trustee in the string format, for example, "S-1-1-0".</span></span>

</dd> <dt>

<span data-ttu-id="2c35d-135">**ORA di \_ creazione**</span><span class="sxs-lookup"><span data-stu-id="2c35d-135">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c35d-136">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2c35d-136">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2c35d-137">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2c35d-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2c35d-138">Ora nel formato [CIM \_ DateTime](cim-datetime.md) quando è stato creato il descrittore di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="2c35d-138">Time in the [CIM\_DATETIME](cim-datetime.md) format when the security descriptor was created.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2c35d-139">Commenti</span><span class="sxs-lookup"><span data-stu-id="2c35d-139">Remarks</span></span>

<span data-ttu-id="2c35d-140">Questa classe fornisce le proprietà ereditate dalla classe [**\_ trustee Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) , che è un membro della classe [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) .</span><span class="sxs-lookup"><span data-stu-id="2c35d-140">This class provides properties that are inherited by the [**Win32\_Trustee**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) class, which is a member of the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) class.</span></span> <span data-ttu-id="2c35d-141">Per ulteriori informazioni, vedere [oggetti del descrittore di sicurezza WMI](wmi-security-descriptor-objects.md) e [modifica della sicurezza di accesso per gli oggetti a protezione diretta](changing-access-security-on-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="2c35d-141">For more information, see [WMI Security Descriptor Objects](wmi-security-descriptor-objects.md) and [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span> <span data-ttu-id="2c35d-142">Per ulteriori informazioni sulle voci ACE, vedere [Access Control Components](/windows/desktop/SecAuthZ/access-control-components).</span><span class="sxs-lookup"><span data-stu-id="2c35d-142">For more information about ACEs, see [Access Control Components](/windows/desktop/SecAuthZ/access-control-components).</span></span>

## <a name="requirements"></a><span data-ttu-id="2c35d-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2c35d-143">Requirements</span></span>



| <span data-ttu-id="2c35d-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c35d-144">Requirement</span></span> | <span data-ttu-id="2c35d-145">Valore</span><span class="sxs-lookup"><span data-stu-id="2c35d-145">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="2c35d-146">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2c35d-146">Minimum supported client</span></span><br/> | <span data-ttu-id="2c35d-147">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2c35d-147">Windows Vista</span></span><br/>       |
| <span data-ttu-id="2c35d-148">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2c35d-148">Minimum supported server</span></span><br/> | <span data-ttu-id="2c35d-149">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2c35d-149">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="2c35d-150">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="2c35d-150">Namespace</span></span><br/>                | <span data-ttu-id="2c35d-151">Tutti gli spazi dei nomi WMI</span><span class="sxs-lookup"><span data-stu-id="2c35d-151">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="2c35d-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2c35d-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c35d-153">Classi di sistema WMI</span><span class="sxs-lookup"><span data-stu-id="2c35d-153">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="2c35d-154">**\_Trustee Win32**</span><span class="sxs-lookup"><span data-stu-id="2c35d-154">**Win32\_Trustee**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-trustee)
</dt> <dt>

[<span data-ttu-id="2c35d-155">Gestione della sicurezza WMI</span><span class="sxs-lookup"><span data-stu-id="2c35d-155">Maintaining WMI Security</span></span>](maintaining-wmi-security.md)
</dt> </dl>

 

