---
description: Controlla l'accesso remoto alle versioni non supportate di Windows.
ms.assetid: eb326bba-a011-4b9c-b4ee-fc08ae364f6f
ms.tgt_platform: multiple
title: Classe __NTLMUser9X
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __NTLMUser9X
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 79aa5153869c7337b6849e8c465dbbf8b36a0f58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317582"
---
# <a name="__ntlmuser9x-class"></a><span data-ttu-id="8e4ed-103">\_\_Classe NTLMUser9X</span><span class="sxs-lookup"><span data-stu-id="8e4ed-103">\_\_NTLMUser9X class</span></span>

<span data-ttu-id="8e4ed-104">La classe di sistema **\_ \_ NTLMUser9X** controlla l'accesso remoto alle versioni non supportate di Windows.</span><span class="sxs-lookup"><span data-stu-id="8e4ed-104">The **\_\_NTLMUser9X** system class controls remote access to unsupported versions of Windows.</span></span> <span data-ttu-id="8e4ed-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="8e4ed-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="8e4ed-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="8e4ed-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e4ed-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8e4ed-107">Syntax</span></span>

``` syntax
class __NTLMUser9X : __SecurityRelatedClass
{
  string Authority;
  sint32 Flags;
  sint32 Mask;
  string Name;
  sint32 Type;
};
```

## <a name="members"></a><span data-ttu-id="8e4ed-108">Members</span><span class="sxs-lookup"><span data-stu-id="8e4ed-108">Members</span></span>

<span data-ttu-id="8e4ed-109">La classe **\_ \_ NTLMUser9X** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="8e4ed-109">The **\_\_NTLMUser9X** class has these types of members:</span></span>

-   [<span data-ttu-id="8e4ed-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8e4ed-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8e4ed-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8e4ed-111">Properties</span></span>

<span data-ttu-id="8e4ed-112">La classe **\_ \_ NTLMUser9X** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="8e4ed-112">The **\_\_NTLMUser9X** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8e4ed-113">**Authority**</span><span class="sxs-lookup"><span data-stu-id="8e4ed-113">**Authority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e4ed-114">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8e4ed-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e4ed-115">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="8e4ed-115">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="8e4ed-116">Dominio a cui si applica un nome utente.</span><span class="sxs-lookup"><span data-stu-id="8e4ed-116">Domain to which a user name applies.</span></span>

</dd> <dt>

<span data-ttu-id="8e4ed-117">**Flag**</span><span class="sxs-lookup"><span data-stu-id="8e4ed-117">**Flags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e4ed-118">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8e4ed-118">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8e4ed-119">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="8e4ed-119">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="8e4ed-120">Flag di ereditarietà.</span><span class="sxs-lookup"><span data-stu-id="8e4ed-120">Inheritance flags.</span></span>

<dt>

<span data-ttu-id="8e4ed-121">0</span><span class="sxs-lookup"><span data-stu-id="8e4ed-121">0</span></span>
</dt> <dd>

<span data-ttu-id="8e4ed-122">Nessuna ereditarietà.</span><span class="sxs-lookup"><span data-stu-id="8e4ed-122">No inheritance.</span></span>

</dd> <dt>

<span data-ttu-id="8e4ed-123">2</span><span class="sxs-lookup"><span data-stu-id="8e4ed-123">2</span></span>
</dt> <dd>

<span data-ttu-id="8e4ed-124">Si applicano agli spazi dei nomi figlio, oltre a quello corrente.</span><span class="sxs-lookup"><span data-stu-id="8e4ed-124">Apply to child namespaces, in addition to the current one.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8e4ed-125">**Mask**</span><span class="sxs-lookup"><span data-stu-id="8e4ed-125">**Mask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e4ed-126">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8e4ed-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8e4ed-127">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="8e4ed-127">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="8e4ed-128">Maschera di maschera che specifica i diritti di accesso allo spazio dei nomi nel repository di Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="8e4ed-128">Bitmask that specifies access rights to the namespace in the Windows Management Instrumentation (WMI) repository.</span></span> <span data-ttu-id="8e4ed-129">Per i valori di bit, vedere [**costanti di diritti di accesso allo spazio dei nomi**](namespace-access-rights-constants.md).</span><span class="sxs-lookup"><span data-stu-id="8e4ed-129">For bit values, see [**Namespace Access Rights Constants**](namespace-access-rights-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e4ed-130">**Nome**</span><span class="sxs-lookup"><span data-stu-id="8e4ed-130">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e4ed-131">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8e4ed-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e4ed-132">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="8e4ed-132">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="8e4ed-133">Nome utente.</span><span class="sxs-lookup"><span data-stu-id="8e4ed-133">User name.</span></span>

</dd> <dt>

<span data-ttu-id="8e4ed-134">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="8e4ed-134">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e4ed-135">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8e4ed-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8e4ed-136">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="8e4ed-136">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="8e4ed-137">Accesso consentito.</span><span class="sxs-lookup"><span data-stu-id="8e4ed-137">Access allowed.</span></span>

<dt>

<span data-ttu-id="8e4ed-138">0</span><span class="sxs-lookup"><span data-stu-id="8e4ed-138">0</span></span>
</dt> <dd>

<span data-ttu-id="8e4ed-139">Accesso consentito.</span><span class="sxs-lookup"><span data-stu-id="8e4ed-139">Access allowed.</span></span>

</dd> <dt>

<span data-ttu-id="8e4ed-140">2</span><span class="sxs-lookup"><span data-stu-id="8e4ed-140">2</span></span>
</dt> <dd>

<span data-ttu-id="8e4ed-141">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="8e4ed-141">Access denied.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8e4ed-142">Commenti</span><span class="sxs-lookup"><span data-stu-id="8e4ed-142">Remarks</span></span>

<span data-ttu-id="8e4ed-143">La classe **\_ \_ NTLMUser9X** viene usata come parametro di input per i metodi [**\_ \_ SystemSecurity:: Get9XUserList**](--systemsecurity-get9xuserlist.md) e [**\_ \_ SystemSecurity:: Set9XUserList**](--systemsecurity-set9xuserlist.md) .</span><span class="sxs-lookup"><span data-stu-id="8e4ed-143">The **\_\_NTLMUser9X** class is used as an input parameter for the [**\_\_SystemSecurity::Get9XUserList**](--systemsecurity-get9xuserlist.md) and [**\_\_SystemSecurity::Set9XUserList**](--systemsecurity-set9xuserlist.md) methods.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e4ed-144">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8e4ed-144">Requirements</span></span>



| <span data-ttu-id="8e4ed-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e4ed-145">Requirement</span></span> | <span data-ttu-id="8e4ed-146">Valore</span><span class="sxs-lookup"><span data-stu-id="8e4ed-146">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="8e4ed-147">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8e4ed-147">Minimum supported client</span></span><br/> | <span data-ttu-id="8e4ed-148">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8e4ed-148">Windows Vista</span></span><br/>       |
| <span data-ttu-id="8e4ed-149">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8e4ed-149">Minimum supported server</span></span><br/> | <span data-ttu-id="8e4ed-150">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8e4ed-150">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="8e4ed-151">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="8e4ed-151">Namespace</span></span><br/>                | <span data-ttu-id="8e4ed-152">Tutti gli spazi dei nomi WMI</span><span class="sxs-lookup"><span data-stu-id="8e4ed-152">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="8e4ed-153">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8e4ed-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e4ed-154">**\_\_SecurityRelatedClass**</span><span class="sxs-lookup"><span data-stu-id="8e4ed-154">**\_\_SecurityRelatedClass**</span></span>](/windows/desktop/WmiSdk/--securityrelatedclass)
</dt> <dt>

[<span data-ttu-id="8e4ed-155">Classi di sistema WMI</span><span class="sxs-lookup"><span data-stu-id="8e4ed-155">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="8e4ed-156">**\_\_SystemSecurity**</span><span class="sxs-lookup"><span data-stu-id="8e4ed-156">**\_\_SystemSecurity**</span></span>](--systemsecurity.md)
</dt> </dl>

 

