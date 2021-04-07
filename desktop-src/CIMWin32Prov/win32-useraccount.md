---
description: Win32 \_ accountutente&\# 32; La classe WMI contiene informazioni su un account utente in un sistema di computer che esegue Windows.
ms.assetid: 747b2ce2-ae38-47de-bf3a-97058df56a7a
ms.tgt_platform: multiple
title: Classe Win32_UserAccount
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_UserAccount
- Win32_UserAccount.AccountType
- Win32_UserAccount.Caption
- Win32_UserAccount.Description
- Win32_UserAccount.Disabled
- Win32_UserAccount.Domain
- Win32_UserAccount.FullName
- Win32_UserAccount.InstallDate
- Win32_UserAccount.LocalAccount
- Win32_UserAccount.Lockout
- Win32_UserAccount.Name
- Win32_UserAccount.PasswordChangeable
- Win32_UserAccount.PasswordExpires
- Win32_UserAccount.PasswordRequired
- Win32_UserAccount.SID
- Win32_UserAccount.SIDType
- Win32_UserAccount.Status
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b5af83f7a52e9f3db9dbaa4a959bfe01ae740746
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049129"
---
# <a name="win32_useraccount-class"></a><span data-ttu-id="dc99a-103">Win32 \_ AccountUtente (classe)</span><span class="sxs-lookup"><span data-stu-id="dc99a-103">Win32\_UserAccount class</span></span>

<span data-ttu-id="dc99a-104">La [classe WMI](../wmisdk/retrieving-a-class.md) **\_ AccountUtente Win32** contiene informazioni su un account utente in un sistema di computer che esegue Windows.</span><span class="sxs-lookup"><span data-stu-id="dc99a-104">The **Win32\_UserAccount** [WMI class](../wmisdk/retrieving-a-class.md) contains information about a user account on a computer system running Windows.</span></span>

> [!Note]  
> <span data-ttu-id="dc99a-105">Poiché sia il **nome** che il **dominio** sono proprietà chiave, l'enumerazione di **Win32 \_ AccountUtente** in una rete di grandi dimensioni può influire negativamente sulle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="dc99a-105">Because both the **Name** and **Domain** are key properties, enumerating **Win32\_UserAccount** on a large network can negatively affect performance.</span></span> <span data-ttu-id="dc99a-106">La chiamata di **GetObject** o di query per un'istanza specifica ha un minore effetto.</span><span class="sxs-lookup"><span data-stu-id="dc99a-106">Calling **GetObject** or querying for a specific instance has less impact.</span></span>

 

<span data-ttu-id="dc99a-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="dc99a-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="dc99a-108">Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="dc99a-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc99a-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dc99a-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4CC-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_UserAccount : Win32_Account
{
  uint32   AccountType;
  string   Caption;
  string   Description;
  boolean  Disabled;
  string   Domain;
  string   FullName;
  datetime InstallDate;
  boolean  LocalAccount;
  boolean  Lockout;
  string   Name;
  boolean  PasswordChangeable;
  boolean  PasswordExpires;
  boolean  PasswordRequired;
  string   SID;
  uint8    SIDType;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="dc99a-110">Members</span><span class="sxs-lookup"><span data-stu-id="dc99a-110">Members</span></span>

<span data-ttu-id="dc99a-111">La classe **Win32 \_ AccountUtente** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="dc99a-111">The **Win32\_UserAccount** class has these types of members:</span></span>

-   [<span data-ttu-id="dc99a-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="dc99a-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="dc99a-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="dc99a-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="dc99a-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="dc99a-114">Methods</span></span>

<span data-ttu-id="dc99a-115">La classe **Win32 \_ AccountUtente** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="dc99a-115">The **Win32\_UserAccount** class has these methods.</span></span>



| <span data-ttu-id="dc99a-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="dc99a-116">Method</span></span>                                                     | <span data-ttu-id="dc99a-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dc99a-117">Description</span></span>                                             |
|:-----------------------------------------------------------|:--------------------------------------------------------|
| [<span data-ttu-id="dc99a-118">**Rinominare**</span><span class="sxs-lookup"><span data-stu-id="dc99a-118">**Rename**</span></span>](rename-method-in-class-win32-useraccount.md) | <span data-ttu-id="dc99a-119">Consente la ridenominazione dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="dc99a-119">Allows for the renaming of the user account.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="dc99a-120">Proprietà</span><span class="sxs-lookup"><span data-stu-id="dc99a-120">Properties</span></span>

<span data-ttu-id="dc99a-121">La classe **Win32 \_ AccountUtente** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="dc99a-121">The **Win32\_UserAccount** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dc99a-122">**AccountType**</span><span class="sxs-lookup"><span data-stu-id="dc99a-122">**AccountType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc99a-123">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dc99a-123">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dc99a-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dc99a-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc99a-125">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ info \_ 2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2) \| usri2 \_ Flags")</span><span class="sxs-lookup"><span data-stu-id="dc99a-125">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2)\|usri2\_flags")</span></span>
</dt> </dl>

<span data-ttu-id="dc99a-126">Flag che descrivono le caratteristiche di un account utente di Windows.</span><span class="sxs-lookup"><span data-stu-id="dc99a-126">Flags that describe the characteristics of a Windows user account.</span></span>

<dt>

<span id="Temporary_duplicate_account"></span><span id="temporary_duplicate_account"></span><span id="TEMPORARY_DUPLICATE_ACCOUNT"></span>

<span data-ttu-id="dc99a-127"><span id="Temporary_duplicate_account"></span><span id="temporary_duplicate_account"></span><span id="TEMPORARY_DUPLICATE_ACCOUNT"></span>**Account duplicato temporaneo** (256)</span><span class="sxs-lookup"><span data-stu-id="dc99a-127"><span id="Temporary_duplicate_account"></span><span id="temporary_duplicate_account"></span><span id="TEMPORARY_DUPLICATE_ACCOUNT"></span>**Temporary duplicate account** (256)</span></span>


</dt> <dd>

<span data-ttu-id="dc99a-128">**\_account con \_ duplicazione temporanea UF \_**</span><span class="sxs-lookup"><span data-stu-id="dc99a-128">**UF\_TEMP\_DUPLICATE\_ACCOUNT**</span></span>

<span data-ttu-id="dc99a-129">Account utente locale per gli utenti che dispongono di un account primario in un altro dominio.</span><span class="sxs-lookup"><span data-stu-id="dc99a-129">Local user account for users who have a primary account in another domain.</span></span> <span data-ttu-id="dc99a-130">Questo account fornisce l'accesso utente solo a questo dominio, non a un dominio che considera attendibile il dominio.</span><span class="sxs-lookup"><span data-stu-id="dc99a-130">This account provides user access to this domain only—not to any domain that trusts this domain.</span></span>

</dd> <dt>

<span id="Normal_account"></span><span id="normal_account"></span><span id="NORMAL_ACCOUNT"></span>

<span data-ttu-id="dc99a-131"><span id="Normal_account"></span><span id="normal_account"></span><span id="NORMAL_ACCOUNT"></span>**Normale account** (512)</span><span class="sxs-lookup"><span data-stu-id="dc99a-131"><span id="Normal_account"></span><span id="normal_account"></span><span id="NORMAL_ACCOUNT"></span>**Normal account** (512)</span></span>


</dt> <dd>

<span data-ttu-id="dc99a-132">**\_account UF Normal \_**</span><span class="sxs-lookup"><span data-stu-id="dc99a-132">**UF\_NORMAL\_ACCOUNT**</span></span>

<span data-ttu-id="dc99a-133">Tipo di account predefinito che rappresenta un utente tipico.</span><span class="sxs-lookup"><span data-stu-id="dc99a-133">Default account type that represents a typical user.</span></span>

</dd> <dt>

<span id="Interdomain_trust_account"></span><span id="interdomain_trust_account"></span><span id="INTERDOMAIN_TRUST_ACCOUNT"></span>

<span data-ttu-id="dc99a-134"><span id="Interdomain_trust_account"></span><span id="interdomain_trust_account"></span><span id="INTERDOMAIN_TRUST_ACCOUNT"></span>**Account trust tra domini** (2048)</span><span class="sxs-lookup"><span data-stu-id="dc99a-134"><span id="Interdomain_trust_account"></span><span id="interdomain_trust_account"></span><span id="INTERDOMAIN_TRUST_ACCOUNT"></span>**Interdomain trust account** (2048)</span></span>


</dt> <dd>

<span data-ttu-id="dc99a-135">**\_ \_ account trust tra domini \_ UF**</span><span class="sxs-lookup"><span data-stu-id="dc99a-135">**UF\_INTERDOMAIN\_TRUST\_ACCOUNT**</span></span>

<span data-ttu-id="dc99a-136">Account per un dominio di sistema che considera attendibili altri domini.</span><span class="sxs-lookup"><span data-stu-id="dc99a-136">Account for a system domain that trusts other domains.</span></span>

</dd> <dt>

<span id="Workstation_trust_account"></span><span id="workstation_trust_account"></span><span id="WORKSTATION_TRUST_ACCOUNT"></span>

<span data-ttu-id="dc99a-137"><span id="Workstation_trust_account"></span><span id="workstation_trust_account"></span><span id="WORKSTATION_TRUST_ACCOUNT"></span>**Account attendibilità workstation** (4096)</span><span class="sxs-lookup"><span data-stu-id="dc99a-137"><span id="Workstation_trust_account"></span><span id="workstation_trust_account"></span><span id="WORKSTATION_TRUST_ACCOUNT"></span>**Workstation trust account** (4096)</span></span>


</dt> <dd>

<span data-ttu-id="dc99a-138">**\_ \_ account attendibilità UF workstation \_**</span><span class="sxs-lookup"><span data-stu-id="dc99a-138">**UF\_WORKSTATION\_TRUST\_ACCOUNT**</span></span>

<span data-ttu-id="dc99a-139">Account computer per un computer che esegue Windows che è membro di questo dominio.</span><span class="sxs-lookup"><span data-stu-id="dc99a-139">Computer account for a computer system running Windows that is a member of this domain.</span></span>

</dd> <dt>

<span id="Server_trust_account"></span><span id="server_trust_account"></span><span id="SERVER_TRUST_ACCOUNT"></span>

<span data-ttu-id="dc99a-140"><span id="Server_trust_account"></span><span id="server_trust_account"></span><span id="SERVER_TRUST_ACCOUNT"></span>**Account trust server** (8192)</span><span class="sxs-lookup"><span data-stu-id="dc99a-140"><span id="Server_trust_account"></span><span id="server_trust_account"></span><span id="SERVER_TRUST_ACCOUNT"></span>**Server trust account** (8192)</span></span>


</dt> <dd>

<span data-ttu-id="dc99a-141">**\_ \_ account trust server \_ UF**</span><span class="sxs-lookup"><span data-stu-id="dc99a-141">**UF\_SERVER\_TRUST\_ACCOUNT**</span></span>

<span data-ttu-id="dc99a-142">Account per un controller di dominio di backup del sistema membro di questo dominio.</span><span class="sxs-lookup"><span data-stu-id="dc99a-142">Account for a system backup domain controller that is a member of this domain.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="dc99a-143">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="dc99a-143">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc99a-144">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="dc99a-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc99a-145">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dc99a-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc99a-146">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="dc99a-146">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="dc99a-147">Dominio e nome utente dell'account.</span><span class="sxs-lookup"><span data-stu-id="dc99a-147">Domain and username of the account.</span></span>

<span data-ttu-id="dc99a-148">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="dc99a-148">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc99a-149">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="dc99a-149">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc99a-150">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="dc99a-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc99a-151">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dc99a-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc99a-152">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="dc99a-152">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="dc99a-153">Descrizione dell'account.</span><span class="sxs-lookup"><span data-stu-id="dc99a-153">Description of the account.</span></span>

<span data-ttu-id="dc99a-154">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="dc99a-154">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc99a-155">**Disabilitato**</span><span class="sxs-lookup"><span data-stu-id="dc99a-155">**Disabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc99a-156">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="dc99a-156">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dc99a-157">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="dc99a-157">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="dc99a-158">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| \_ informazioni utente \| UF \_ ACCOUNTDISABLE")</span><span class="sxs-lookup"><span data-stu-id="dc99a-158">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|USER\_INFO\|UF\_ACCOUNTDISABLE")</span></span>
</dt> </dl>

<span data-ttu-id="dc99a-159">Account utente di Windows disabilitato.</span><span class="sxs-lookup"><span data-stu-id="dc99a-159">Windows user account is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="dc99a-160">**Dominio**</span><span class="sxs-lookup"><span data-stu-id="dc99a-160">**Domain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc99a-161">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="dc99a-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc99a-162">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dc99a-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc99a-163">Qualificatori: [**override**](../wmisdk/standard-qualifiers.md) ("Domain"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Functions \| NomeDominio")</span><span class="sxs-lookup"><span data-stu-id="dc99a-163">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Domain"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Functions\|domainname")</span></span>
</dt> </dl>

<span data-ttu-id="dc99a-164">Nome del dominio Windows a cui appartiene un account utente, ad esempio: "NA-SALES".</span><span class="sxs-lookup"><span data-stu-id="dc99a-164">Name of the Windows domain to which a user account belongs, for example: "NA-SALES".</span></span>

</dd> <dt>

<span data-ttu-id="dc99a-165">**FullName**</span><span class="sxs-lookup"><span data-stu-id="dc99a-165">**FullName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc99a-166">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="dc99a-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc99a-167">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="dc99a-167">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="dc99a-168">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**\_ Info utente \_ 2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2) \| **usri2 \_ \_ nome completo**")</span><span class="sxs-lookup"><span data-stu-id="dc99a-168">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2)\|**usri2\_full\_name**")</span></span>
</dt> </dl>

<span data-ttu-id="dc99a-169">Nome completo di un utente locale, ad esempio: "Dan Wilson".</span><span class="sxs-lookup"><span data-stu-id="dc99a-169">Full name of a local user, for example: "Dan Wilson".</span></span>

</dd> <dt>

<span data-ttu-id="dc99a-170">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="dc99a-170">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc99a-171">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="dc99a-171">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="dc99a-172">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dc99a-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc99a-173">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="dc99a-173">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="dc99a-174">Data di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="dc99a-174">Date the object is installed.</span></span> <span data-ttu-id="dc99a-175">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="dc99a-175">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="dc99a-176">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="dc99a-176">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc99a-177">**LocalAccount**</span><span class="sxs-lookup"><span data-stu-id="dc99a-177">**LocalAccount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc99a-178">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="dc99a-178">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dc99a-179">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dc99a-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc99a-180">Qualificatori: [ **corretti**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="dc99a-180">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="dc99a-181">Se **true**, l'account viene definito nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="dc99a-181">If **true**, the account is defined on the local computer.</span></span>

<span data-ttu-id="dc99a-182">Questa proprietà viene ereditata [**dall' \_ account Win32**](win32-account.md).</span><span class="sxs-lookup"><span data-stu-id="dc99a-182">This property is inherited from [**Win32\_Account**](win32-account.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc99a-183">**Blocco**</span><span class="sxs-lookup"><span data-stu-id="dc99a-183">**Lockout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc99a-184">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="dc99a-184">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dc99a-185">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="dc99a-185">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="dc99a-186">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**\_ informazioni utente \_ 2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2) \| **\_ blocco UF**")</span><span class="sxs-lookup"><span data-stu-id="dc99a-186">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2)\|**UF\_LOCKOUT**")</span></span>
</dt> </dl>

<span data-ttu-id="dc99a-187">Se **true**, l'account utente viene bloccato dal sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="dc99a-187">If **true**, the user account is locked out of the Windows operating system.</span></span>

</dd> <dt>

<span data-ttu-id="dc99a-188">**Nome**</span><span class="sxs-lookup"><span data-stu-id="dc99a-188">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc99a-189">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="dc99a-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc99a-190">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dc99a-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc99a-191">Qualificatori: [**override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| Name")</span><span class="sxs-lookup"><span data-stu-id="dc99a-191">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|name")</span></span>
</dt> </dl>

<span data-ttu-id="dc99a-192">Nome dell'account utente di Windows nel dominio specificato dalla proprietà **Domain** di questa classe.</span><span class="sxs-lookup"><span data-stu-id="dc99a-192">Name of the Windows user account on the domain that the **Domain** property of this class specifies.</span></span>

<span data-ttu-id="dc99a-193">Esempio: "danwilson".</span><span class="sxs-lookup"><span data-stu-id="dc99a-193">Example: "danwilson".</span></span>

<span data-ttu-id="dc99a-194">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="dc99a-194">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc99a-195">**PasswordChangeable**</span><span class="sxs-lookup"><span data-stu-id="dc99a-195">**PasswordChangeable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc99a-196">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="dc99a-196">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dc99a-197">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="dc99a-197">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="dc99a-198">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ info \_ 2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2) \| **UF \_ passwd \_ cant \_ Change**")</span><span class="sxs-lookup"><span data-stu-id="dc99a-198">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2)\|**UF\_PASSWD\_CANT\_CHANGE**")</span></span>
</dt> </dl>

<span data-ttu-id="dc99a-199">Se **true**, è possibile modificare la password di questo account utente.</span><span class="sxs-lookup"><span data-stu-id="dc99a-199">If **true**, the password on this user account can be changed.</span></span>

</dd> <dt>

<span data-ttu-id="dc99a-200">**PasswordExpires**</span><span class="sxs-lookup"><span data-stu-id="dc99a-200">**PasswordExpires**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc99a-201">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="dc99a-201">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dc99a-202">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="dc99a-202">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="dc99a-203">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ info \_ 2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2) \| **UF \_ dont \_ expire \_ passwd**")</span><span class="sxs-lookup"><span data-stu-id="dc99a-203">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2)\|**UF\_DONT\_EXPIRE\_PASSWD**")</span></span>
</dt> </dl>

<span data-ttu-id="dc99a-204">Se **true**, la password dell'account utente scade.</span><span class="sxs-lookup"><span data-stu-id="dc99a-204">If **true**, the password on this user account expires.</span></span>

</dd> <dt>

<span data-ttu-id="dc99a-205">**PasswordRequired**</span><span class="sxs-lookup"><span data-stu-id="dc99a-205">**PasswordRequired**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc99a-206">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="dc99a-206">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dc99a-207">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="dc99a-207">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="dc99a-208">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**utente \_ info \_ 2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2) \| **UF \_ passwd \_ NOTREQD**")</span><span class="sxs-lookup"><span data-stu-id="dc99a-208">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2)\|**UF\_PASSWD\_NOTREQD**")</span></span>
</dt> </dl>

<span data-ttu-id="dc99a-209">Se **true**, è necessaria una password per un account utente di Windows.</span><span class="sxs-lookup"><span data-stu-id="dc99a-209">If **true**, a password is required on a Windows user account.</span></span> <span data-ttu-id="dc99a-210">Se **false**, l'account non richiede una password.</span><span class="sxs-lookup"><span data-stu-id="dc99a-210">If **false**, this account does not require a password.</span></span>

</dd> <dt>

<span data-ttu-id="dc99a-211">**SID**</span><span class="sxs-lookup"><span data-stu-id="dc99a-211">**SID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc99a-212">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="dc99a-212">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc99a-213">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dc99a-213">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc99a-214">Qualificatori: [**fixed**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Security Identifier (SID)")</span><span class="sxs-lookup"><span data-stu-id="dc99a-214">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Security Identifiers (SIDs)")</span></span>
</dt> </dl>

<span data-ttu-id="dc99a-215">ID di sicurezza (SID) per l'account.</span><span class="sxs-lookup"><span data-stu-id="dc99a-215">Security identifier (SID) for this account.</span></span> <span data-ttu-id="dc99a-216">Un SID è un valore stringa di lunghezza variabile che viene usato per identificare un trustee.</span><span class="sxs-lookup"><span data-stu-id="dc99a-216">A SID is a string value of variable length that is used to identify a trustee.</span></span> <span data-ttu-id="dc99a-217">Ogni account dispone di un SID univoco che un'autorità, ad esempio un dominio di Windows, ha problemi.</span><span class="sxs-lookup"><span data-stu-id="dc99a-217">Each account has a unique SID that an authority, such as a Windows domain, issues.</span></span> <span data-ttu-id="dc99a-218">Il SID viene archiviato nel database di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="dc99a-218">The SID is stored in the security database.</span></span> <span data-ttu-id="dc99a-219">Quando un utente accede, il sistema Recupera il SID dell'utente dal database, inserisce il SID nel token di accesso utente e quindi usa il SID nel token di accesso utente per identificare l'utente in tutte le interazioni successive con la sicurezza di Windows.</span><span class="sxs-lookup"><span data-stu-id="dc99a-219">When a user logs on, the system retrieves the user SID from the database, places the SID in the user access token, and then uses the SID in the user access token to identify the user in all subsequent interactions with Windows security.</span></span> <span data-ttu-id="dc99a-220">Ogni SID è un identificatore univoco per un utente o un gruppo e un utente o un gruppo diverso non può avere lo stesso SID.</span><span class="sxs-lookup"><span data-stu-id="dc99a-220">Each SID is a unique identifier for a user or group, and a different user or group cannot have the same SID.</span></span>

<span data-ttu-id="dc99a-221">Questa proprietà viene ereditata [**dall' \_ account Win32**](win32-account.md).</span><span class="sxs-lookup"><span data-stu-id="dc99a-221">This property is inherited from [**Win32\_Account**](win32-account.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc99a-222">**SIDType**</span><span class="sxs-lookup"><span data-stu-id="dc99a-222">**SIDType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc99a-223">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="dc99a-223">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="dc99a-224">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dc99a-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc99a-225">Qualificatori: [**fixed**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API di \| controllo di accesso tipi di enumerazione \| [**SID \_ nome \_ utilizzo**](/windows/win32/api/winnt/ne-winnt-sid_name_use)")</span><span class="sxs-lookup"><span data-stu-id="dc99a-225">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Access Control Enumeration Types\|[**SID\_NAME\_USE**](/windows/win32/api/winnt/ne-winnt-sid_name_use)")</span></span>
</dt> </dl>

<span data-ttu-id="dc99a-226">Valore enumerato che specifica il tipo di SID.</span><span class="sxs-lookup"><span data-stu-id="dc99a-226">Enumerated value that specifies the type of SID.</span></span>

<span data-ttu-id="dc99a-227">Questa proprietà viene ereditata [**dall' \_ account Win32**](win32-account.md).</span><span class="sxs-lookup"><span data-stu-id="dc99a-227">This property is inherited from [**Win32\_Account**](win32-account.md).</span></span>

<dt>

<span id="SidTypeUser"></span><span id="sidtypeuser"></span><span id="SIDTYPEUSER"></span>

<span data-ttu-id="dc99a-228">**SidTypeUser** (1)</span><span class="sxs-lookup"><span data-stu-id="dc99a-228">**SidTypeUser** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeGroup"></span><span id="sidtypegroup"></span><span id="SIDTYPEGROUP"></span>

<span data-ttu-id="dc99a-229">**SidTypeGroup** (2)</span><span class="sxs-lookup"><span data-stu-id="dc99a-229">**SidTypeGroup** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeDomain"></span><span id="sidtypedomain"></span><span id="SIDTYPEDOMAIN"></span>

<span data-ttu-id="dc99a-230">**SidTypeDomain** (3)</span><span class="sxs-lookup"><span data-stu-id="dc99a-230">**SidTypeDomain** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeAlias"></span><span id="sidtypealias"></span><span id="SIDTYPEALIAS"></span>

<span data-ttu-id="dc99a-231">**SidTypeAlias** (4)</span><span class="sxs-lookup"><span data-stu-id="dc99a-231">**SidTypeAlias** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeWellKnownGroup"></span><span id="sidtypewellknowngroup"></span><span id="SIDTYPEWELLKNOWNGROUP"></span>

<span data-ttu-id="dc99a-232">**SidTypeWellKnownGroup** (5)</span><span class="sxs-lookup"><span data-stu-id="dc99a-232">**SidTypeWellKnownGroup** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeDeletedAccount"></span><span id="sidtypedeletedaccount"></span><span id="SIDTYPEDELETEDACCOUNT"></span>

<span data-ttu-id="dc99a-233">**SidTypeDeletedAccount** (6)</span><span class="sxs-lookup"><span data-stu-id="dc99a-233">**SidTypeDeletedAccount** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeInvalid"></span><span id="sidtypeinvalid"></span><span id="SIDTYPEINVALID"></span>

<span data-ttu-id="dc99a-234">**SidTypeInvalid** (7)</span><span class="sxs-lookup"><span data-stu-id="dc99a-234">**SidTypeInvalid** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeUnknown"></span><span id="sidtypeunknown"></span><span id="SIDTYPEUNKNOWN"></span>

<span data-ttu-id="dc99a-235">**SidTypeUnknown** (8)</span><span class="sxs-lookup"><span data-stu-id="dc99a-235">**SidTypeUnknown** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeComputer"></span><span id="sidtypecomputer"></span><span id="SIDTYPECOMPUTER"></span>

<span data-ttu-id="dc99a-236">**SidTypeComputer** (9)</span><span class="sxs-lookup"><span data-stu-id="dc99a-236">**SidTypeComputer** (9)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dc99a-237">**Status**</span><span class="sxs-lookup"><span data-stu-id="dc99a-237">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc99a-238">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="dc99a-238">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc99a-239">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dc99a-239">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc99a-240">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="dc99a-240">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="dc99a-241">Stato corrente di un oggetto.</span><span class="sxs-lookup"><span data-stu-id="dc99a-241">Current status of an object.</span></span> <span data-ttu-id="dc99a-242">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="dc99a-242">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="dc99a-243">Gli stati operativi includono: "OK", "degradato" e "errore di predazione", che è un elemento, ad esempio un'unità disco rigido abilitata per SMART, che può funzionare correttamente, ma che prevede un errore nel prossimo futuro.</span><span class="sxs-lookup"><span data-stu-id="dc99a-243">Operational statuses include: "OK", "Degraded", and "Pred Fail", which is an element such as a SMART-enabled hard disk drive that may be functioning properly, but predicts a failure in the near future.</span></span> <span data-ttu-id="dc99a-244">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service", che possono essere applicati durante la riesecuzione del mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="dc99a-244">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service", which can apply during mirror resilvering of a disk, reloading a user permissions list, or other administrative work.</span></span>

<span data-ttu-id="dc99a-245">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="dc99a-245">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="dc99a-246">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="dc99a-246">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="dc99a-247">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="dc99a-247">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="dc99a-248">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="dc99a-248">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="dc99a-249">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="dc99a-249">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dc99a-250">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="dc99a-250">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="dc99a-251">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="dc99a-251">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="dc99a-252">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="dc99a-252">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="dc99a-253">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="dc99a-253">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="dc99a-254">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="dc99a-254">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="dc99a-255">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="dc99a-255">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="dc99a-256">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="dc99a-256">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="dc99a-257">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="dc99a-257">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="dc99a-258">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="dc99a-258">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="dc99a-259"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="dc99a-259"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="dc99a-260">Commenti</span><span class="sxs-lookup"><span data-stu-id="dc99a-260">Remarks</span></span>

<span data-ttu-id="dc99a-261">La classe **Win32 \_ AccountUtente** è derivata dall' [**\_ account Win32**](win32-account.md).</span><span class="sxs-lookup"><span data-stu-id="dc99a-261">The **Win32\_UserAccount** class is derived from [**Win32\_Account**](win32-account.md).</span></span>

> [!Note]  
> <span data-ttu-id="dc99a-262">Un errore non viene restituito per un tentativo di scrittura in una proprietà di sola lettura e il valore della proprietà rimane invariato.</span><span class="sxs-lookup"><span data-stu-id="dc99a-262">An error is not returned for an attempt to write to a read-only property, and the value of the property remains unchanged.</span></span>

 

## <a name="examples"></a><span data-ttu-id="dc99a-263">Esempio</span><span class="sxs-lookup"><span data-stu-id="dc99a-263">Examples</span></span>

<span data-ttu-id="dc99a-264">L'esempio di codice dell' [elenco degli account utente locale utilizzando WMI](https://Gallery.TechNet.Microsoft.Com/827623f5-eb55-4035-8f57-25c4afb444cd) VBScript nella raccolta TechNet utilizza **Win32 \_ AccountUtente** per restituire informazioni sugli account utente locali trovati in un computer.</span><span class="sxs-lookup"><span data-stu-id="dc99a-264">The [List Local User Accounts Using WMI](https://Gallery.TechNet.Microsoft.Com/827623f5-eb55-4035-8f57-25c4afb444cd) VBScript code sample on TechNet Gallery uses **Win32\_UserAccount** to Returns information about the local user accounts found on a computer.</span></span>

<span data-ttu-id="dc99a-265">[Convertire SID in account utente e account utente in SID](https://Gallery.TechNet.Microsoft.Com/f1c83aed-fe60-48d5-90ab-22388fcbd54f) Esempio di codice PowerShell nella raccolta TechNet USA **Win32 \_ AccountUtente** per convertire un SID in un account utente e/o un account utente in SID.</span><span class="sxs-lookup"><span data-stu-id="dc99a-265">[The Translate SID to User Account and User Account to SID](https://Gallery.TechNet.Microsoft.Com/f1c83aed-fe60-48d5-90ab-22388fcbd54f) PowerShell code sample on TechNet Gallery uses **Win32\_UserAccount** to translate a SID to User Account and/or a User Account to SID.</span></span>

<span data-ttu-id="dc99a-266">Nell'esempio di codice VBScript riportato di seguito viene illustrato come ottenere il nome completo di un utente in un computer locale.</span><span class="sxs-lookup"><span data-stu-id="dc99a-266">The following VBScript code example shows you how to get the full name of a user on a local computer.</span></span> <span data-ttu-id="dc99a-267">Il nome completo è il nome della lingua umana. ad esempio, una persona potrebbe avere il nome utente "kensanchez" e il nome completo può essere "Ken Sanchez", quindi sostituire il nome di dominio reale e il nome utente per "NomeDominio" e "nome utente".</span><span class="sxs-lookup"><span data-stu-id="dc99a-267">The full name is the human language name, for example, a person may have the user name of "kensanchez" and the full name may be "Ken Sanchez", so you substitute the real domain name and user name for "MyDomainName" and "MyUserName".</span></span> <span data-ttu-id="dc99a-268">Per una query efficiente, è necessario specificare le proprietà di dominio e nome utente.</span><span class="sxs-lookup"><span data-stu-id="dc99a-268">For an efficient query, you must specify both the domain and user name properties.</span></span>

<span data-ttu-id="dc99a-269">Se si è un amministratore di un computer remoto, è possibile assegnare il nome del computer remoto per strComputer (anziché "."), quindi utilizzare il tipo di script seguente per ottenere il nome completo di un account utente in un computer locale, da un computer remoto.</span><span class="sxs-lookup"><span data-stu-id="dc99a-269">If you are an administrator on a remote computer, you can assign the name of the remote computer for strComputer (instead of "."), and then use the following type of script to get the full name of a user account on a local computer—from a remote computer.</span></span>


```VB
On Error Resume Next
strComputer = "."

Set objUserAccount = GetObject("winmgmts{impersonationLevel=impersonate}!\\" & strComputer _
    & "\root\cimv2:Win32_UserAccount.Domain='MyDomainName',Name='MyUserName' ")

If Err = 0 Then
    WScript.Echo objUserAccount.FullName
Else
    WScript.Echo "No object found" & Err.Number
End If
```




```CSharp
using System.Management;

{
     ManagementScope mgmtScope = new ManagementScope("\\\\.\\Root\\CIMv2");
     ObjectQuery oQuery = new ObjectQuery("SELECT * FROM Win32_UserAccount Where Name=\"myUserName\"");
     ManagementObjectSearcher mgmtSearch = new ManagementObjectSearcher(mgmtScope, oQuery);
     ManagementObjectCollection objCollection = mgmtSearch.Get();
     foreach (ManagementObject mgmtObject in objCollection)
     {
          Console.WriteLine("Full Name : {0}", mgmtObject["FullName"]);
     }
}
```



## <a name="requirements"></a><span data-ttu-id="dc99a-270">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dc99a-270">Requirements</span></span>



| <span data-ttu-id="dc99a-271">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc99a-271">Requirement</span></span> | <span data-ttu-id="dc99a-272">Valore</span><span class="sxs-lookup"><span data-stu-id="dc99a-272">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dc99a-273">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dc99a-273">Minimum supported client</span></span><br/> | <span data-ttu-id="dc99a-274">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dc99a-274">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="dc99a-275">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dc99a-275">Minimum supported server</span></span><br/> | <span data-ttu-id="dc99a-276">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dc99a-276">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="dc99a-277">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="dc99a-277">Namespace</span></span><br/>                | <span data-ttu-id="dc99a-278">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="dc99a-278">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="dc99a-279">MOF</span><span class="sxs-lookup"><span data-stu-id="dc99a-279">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dc99a-280"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dc99a-280"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="dc99a-281">DLL</span><span class="sxs-lookup"><span data-stu-id="dc99a-281">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dc99a-282"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dc99a-282"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc99a-283">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dc99a-283">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc99a-284">**\_Account Win32**</span><span class="sxs-lookup"><span data-stu-id="dc99a-284">**Win32\_Account**</span></span>](win32-account.md)
</dt> <dt>

[<span data-ttu-id="dc99a-285">Classi del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="dc99a-285">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
