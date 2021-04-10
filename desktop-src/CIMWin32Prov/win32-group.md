---
description: Rappresenta i dati relativi a un account di gruppo.
ms.assetid: a53d1276-3dc9-419a-bbb8-5dd07794a971
ms.tgt_platform: multiple
title: Classe Win32_Group
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Group
- Win32_Group.Caption
- Win32_Group.Description
- Win32_Group.InstallDate
- Win32_Group.Status
- Win32_Group.LocalAccount
- Win32_Group.SID
- Win32_Group.SIDType
- Win32_Group.Domain
- Win32_Group.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a8849ba149e0de570150682d3afbad3a4ee33f36
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127330"
---
# <a name="win32_group-class"></a><span data-ttu-id="c901a-103">\_Classe gruppo Win32</span><span class="sxs-lookup"><span data-stu-id="c901a-103">Win32\_Group class</span></span>

<span data-ttu-id="c901a-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) del **\_ gruppo Win32** rappresenta i dati relativi a un account di gruppo.</span><span class="sxs-lookup"><span data-stu-id="c901a-104">The **Win32\_Group** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents data about a group account.</span></span> <span data-ttu-id="c901a-105">Un account di gruppo consente la modifica dei privilegi di accesso per un elenco di utenti.</span><span class="sxs-lookup"><span data-stu-id="c901a-105">A group account allows access privileges to be changed for a list of users.</span></span> <span data-ttu-id="c901a-106">Esempio: Marketing2.</span><span class="sxs-lookup"><span data-stu-id="c901a-106">Example: Marketing2.</span></span>

<span data-ttu-id="c901a-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="c901a-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="c901a-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="c901a-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c901a-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c901a-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4CB-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_Group : Win32_Account
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  boolean  LocalAccount;
  string   SID;
  uint8    SIDType;
  string   Domain;
  string   Name;
};
```

## <a name="members"></a><span data-ttu-id="c901a-110">Members</span><span class="sxs-lookup"><span data-stu-id="c901a-110">Members</span></span>

<span data-ttu-id="c901a-111">La classe del **\_ gruppo Win32** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="c901a-111">The **Win32\_Group** class has these types of members:</span></span>

-   [<span data-ttu-id="c901a-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="c901a-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="c901a-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c901a-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c901a-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="c901a-114">Methods</span></span>

<span data-ttu-id="c901a-115">La classe del **\_ gruppo Win32** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="c901a-115">The **Win32\_Group** class has these methods.</span></span>



| <span data-ttu-id="c901a-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="c901a-116">Method</span></span>                                               | <span data-ttu-id="c901a-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c901a-117">Description</span></span>                        |
|:-----------------------------------------------------|:-----------------------------------|
| [<span data-ttu-id="c901a-118">**Rinominare**</span><span class="sxs-lookup"><span data-stu-id="c901a-118">**Rename**</span></span>](rename-method-in-class-win32-group.md) | <span data-ttu-id="c901a-119">Modifica il nome del gruppo.</span><span class="sxs-lookup"><span data-stu-id="c901a-119">Changes the group name.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="c901a-120">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c901a-120">Properties</span></span>

<span data-ttu-id="c901a-121">La classe del **\_ gruppo Win32** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="c901a-121">The **Win32\_Group** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c901a-122">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="c901a-122">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c901a-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c901a-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c901a-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c901a-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c901a-125">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="c901a-125">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="c901a-126">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="c901a-126">A short textual description of the object.</span></span>

<span data-ttu-id="c901a-127">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c901a-127">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c901a-128">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="c901a-128">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c901a-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c901a-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c901a-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c901a-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c901a-131">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="c901a-131">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="c901a-132">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="c901a-132">A textual description of the object.</span></span>

<span data-ttu-id="c901a-133">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c901a-133">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c901a-134">**Dominio**</span><span class="sxs-lookup"><span data-stu-id="c901a-134">**Domain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c901a-135">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c901a-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c901a-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c901a-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c901a-137">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Domain"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Network Management Functions \| NomeDominio")</span><span class="sxs-lookup"><span data-stu-id="c901a-137">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Domain"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Network Management Functions\|domainname")</span></span>
</dt> </dl>

<span data-ttu-id="c901a-138">Nome del dominio Windows a cui appartiene l'account di gruppo.</span><span class="sxs-lookup"><span data-stu-id="c901a-138">Name of the Windows domain to which the group account belongs.</span></span>

<span data-ttu-id="c901a-139">Esempio: "NA-SALES"</span><span class="sxs-lookup"><span data-stu-id="c901a-139">Example: "NA-SALES"</span></span>

</dd> <dt>

<span data-ttu-id="c901a-140">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="c901a-140">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c901a-141">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c901a-141">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c901a-142">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c901a-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c901a-143">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="c901a-143">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="c901a-144">Indica quando l'oggetto è stato installato.</span><span class="sxs-lookup"><span data-stu-id="c901a-144">Indicates when the object was installed.</span></span> <span data-ttu-id="c901a-145">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="c901a-145">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="c901a-146">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c901a-146">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c901a-147">**LocalAccount**</span><span class="sxs-lookup"><span data-stu-id="c901a-147">**LocalAccount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c901a-148">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="c901a-148">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c901a-149">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c901a-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c901a-150">Qualificatori: [ **corretti**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c901a-150">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c901a-151">Se **true**, l'account viene definito nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="c901a-151">If **TRUE**, the account is defined on the local machine.</span></span> <span data-ttu-id="c901a-152">Per recuperare solo gli account definiti nel computer locale, progettare una query che includa la condizione "LocalAccount =**true**".</span><span class="sxs-lookup"><span data-stu-id="c901a-152">To retrieve only accounts defined on the local machine, design a query that includes the condition "LocalAccount=**TRUE**".</span></span>

<span data-ttu-id="c901a-153">Questa proprietà viene ereditata [**dall' \_ account Win32**](win32-account.md).</span><span class="sxs-lookup"><span data-stu-id="c901a-153">This property is inherited from [**Win32\_Account**](win32-account.md).</span></span>

</dd> <dt>

<span data-ttu-id="c901a-154">**Nome**</span><span class="sxs-lookup"><span data-stu-id="c901a-154">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c901a-155">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c901a-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c901a-156">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c901a-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c901a-157">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Network Management Structures \| Name")</span><span class="sxs-lookup"><span data-stu-id="c901a-157">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Network Management Structures\|name")</span></span>
</dt> </dl>

<span data-ttu-id="c901a-158">Nome dell'account di gruppo di Windows nel dominio specificato dalla proprietà del **dominio** di questa classe.</span><span class="sxs-lookup"><span data-stu-id="c901a-158">Name of the Windows group account on the domain specified by the **Domain** property of this class.</span></span>

</dd> <dt>

<span data-ttu-id="c901a-159">**SID**</span><span class="sxs-lookup"><span data-stu-id="c901a-159">**SID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c901a-160">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c901a-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c901a-161">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c901a-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c901a-162">Qualificatori: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Security Identifier (SID)")</span><span class="sxs-lookup"><span data-stu-id="c901a-162">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Security Identifiers (SIDs)")</span></span>
</dt> </dl>

<span data-ttu-id="c901a-163">ID di sicurezza (SID) per l'account.</span><span class="sxs-lookup"><span data-stu-id="c901a-163">Security identifier (SID) for this account.</span></span> <span data-ttu-id="c901a-164">Un SID è un valore stringa di lunghezza variabile usato per identificare un trustee.</span><span class="sxs-lookup"><span data-stu-id="c901a-164">A SID is a string value of variable length used to identify a trustee.</span></span> <span data-ttu-id="c901a-165">Ogni account dispone di un SID univoco emesso da un'autorità, ad esempio un dominio di Windows, archiviato in un database di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="c901a-165">Each account has a unique SID issued by an authority (such as a Windows domain), stored in a security database.</span></span> <span data-ttu-id="c901a-166">Quando un utente esegue l'accesso, il sistema Recupera il SID dell'utente dal database e lo inserisce nel token di accesso dell'utente.</span><span class="sxs-lookup"><span data-stu-id="c901a-166">When a user logs on, the system retrieves the user's SID from the database and places it in the user's access token.</span></span> <span data-ttu-id="c901a-167">Il sistema usa il SID nel token di accesso dell'utente per identificare l'utente in tutte le interazioni successive con la sicurezza di Windows.</span><span class="sxs-lookup"><span data-stu-id="c901a-167">The system uses the SID in the user's access token to identify the user in all subsequent interactions with Windows security.</span></span> <span data-ttu-id="c901a-168">Quando un SID è stato usato come identificatore univoco per un utente o un gruppo, non può essere usato di nuovo per identificare un altro utente o gruppo.</span><span class="sxs-lookup"><span data-stu-id="c901a-168">When a SID has been used as the unique identifier for a user or group, it cannot be used again to identify another user or group.</span></span>

<span data-ttu-id="c901a-169">Questa proprietà viene ereditata [**dall' \_ account Win32**](win32-account.md).</span><span class="sxs-lookup"><span data-stu-id="c901a-169">This property is inherited from [**Win32\_Account**](win32-account.md).</span></span>

</dd> <dt>

<span data-ttu-id="c901a-170">**SIDType**</span><span class="sxs-lookup"><span data-stu-id="c901a-170">**SIDType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c901a-171">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="c901a-171">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="c901a-172">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c901a-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c901a-173">Qualificatori: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API di \| controllo di accesso tipi di enumerazione \| SID \_ nome \_ utilizzo")</span><span class="sxs-lookup"><span data-stu-id="c901a-173">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Access Control Enumeration Types\|SID\_NAME\_USE")</span></span>
</dt> </dl>

<span data-ttu-id="c901a-174">Valori enumerati che specificano il tipo di ID di sicurezza (SID).</span><span class="sxs-lookup"><span data-stu-id="c901a-174">Enumerated values that specify the type of security identifier (SID).</span></span>

<span data-ttu-id="c901a-175">Questa proprietà viene ereditata [**dall' \_ account Win32**](win32-account.md).</span><span class="sxs-lookup"><span data-stu-id="c901a-175">This property is inherited from [**Win32\_Account**](win32-account.md).</span></span>

<dt>

<span id="SidTypeUser"></span><span id="sidtypeuser"></span><span id="SIDTYPEUSER"></span>

<span data-ttu-id="c901a-176">**SidTypeUser** (1)</span><span class="sxs-lookup"><span data-stu-id="c901a-176">**SidTypeUser** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeGroup"></span><span id="sidtypegroup"></span><span id="SIDTYPEGROUP"></span>

<span data-ttu-id="c901a-177">**SidTypeGroup** (2)</span><span class="sxs-lookup"><span data-stu-id="c901a-177">**SidTypeGroup** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeDomain"></span><span id="sidtypedomain"></span><span id="SIDTYPEDOMAIN"></span>

<span data-ttu-id="c901a-178">**SidTypeDomain** (3)</span><span class="sxs-lookup"><span data-stu-id="c901a-178">**SidTypeDomain** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeAlias"></span><span id="sidtypealias"></span><span id="SIDTYPEALIAS"></span>

<span data-ttu-id="c901a-179">**SidTypeAlias** (4)</span><span class="sxs-lookup"><span data-stu-id="c901a-179">**SidTypeAlias** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeWellKnownGroup"></span><span id="sidtypewellknowngroup"></span><span id="SIDTYPEWELLKNOWNGROUP"></span>

<span data-ttu-id="c901a-180">**SidTypeWellKnownGroup** (5)</span><span class="sxs-lookup"><span data-stu-id="c901a-180">**SidTypeWellKnownGroup** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeDeletedAccount"></span><span id="sidtypedeletedaccount"></span><span id="SIDTYPEDELETEDACCOUNT"></span>

<span data-ttu-id="c901a-181">**SidTypeDeletedAccount** (6)</span><span class="sxs-lookup"><span data-stu-id="c901a-181">**SidTypeDeletedAccount** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeInvalid"></span><span id="sidtypeinvalid"></span><span id="SIDTYPEINVALID"></span>

<span data-ttu-id="c901a-182">**SidTypeInvalid** (7)</span><span class="sxs-lookup"><span data-stu-id="c901a-182">**SidTypeInvalid** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeUnknown"></span><span id="sidtypeunknown"></span><span id="SIDTYPEUNKNOWN"></span>

<span data-ttu-id="c901a-183">**SidTypeUnknown** (8)</span><span class="sxs-lookup"><span data-stu-id="c901a-183">**SidTypeUnknown** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeComputer"></span><span id="sidtypecomputer"></span><span id="SIDTYPECOMPUTER"></span>

<span data-ttu-id="c901a-184">**SidTypeComputer** (9)</span><span class="sxs-lookup"><span data-stu-id="c901a-184">**SidTypeComputer** (9)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c901a-185">**Status**</span><span class="sxs-lookup"><span data-stu-id="c901a-185">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c901a-186">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c901a-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c901a-187">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c901a-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c901a-188">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="c901a-188">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="c901a-189">Stringa che indica lo stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="c901a-189">String that indicates the current status of the object.</span></span> <span data-ttu-id="c901a-190">È possibile definire lo stato operativo e non operativo.</span><span class="sxs-lookup"><span data-stu-id="c901a-190">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="c901a-191">Lo stato operativo può includere "OK", "danneggiato" e "errore predazione".</span><span class="sxs-lookup"><span data-stu-id="c901a-191">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="c901a-192">"Predator fail" indica che un elemento funziona correttamente, ma sta stimando un errore, ad esempio un'unità disco rigido abilitata per SMART.</span><span class="sxs-lookup"><span data-stu-id="c901a-192">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="c901a-193">Lo stato non operativo può includere "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="c901a-193">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="c901a-194">Il "servizio" può essere applicato durante il mirroring del disco, ovvero la riattivazione, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="c901a-194">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="c901a-195">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="c901a-195">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="c901a-196">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c901a-196">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="c901a-197">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="c901a-197">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="c901a-198">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="c901a-198">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="c901a-199">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="c901a-199">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="c901a-200">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="c901a-200">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c901a-201">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="c901a-201">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="c901a-202">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="c901a-202">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="c901a-203">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="c901a-203">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="c901a-204">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="c901a-204">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="c901a-205">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="c901a-205">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="c901a-206">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="c901a-206">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="c901a-207">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="c901a-207">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="c901a-208">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="c901a-208">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="c901a-209">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="c901a-209">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="c901a-210"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="c901a-210"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="c901a-211">Commenti</span><span class="sxs-lookup"><span data-stu-id="c901a-211">Remarks</span></span>

<span data-ttu-id="c901a-212">La classe del **\_ gruppo Win32** è derivata [**dall' \_ account Win32**](win32-account.md).</span><span class="sxs-lookup"><span data-stu-id="c901a-212">The **Win32\_Group** class is derived from [**Win32\_Account**](win32-account.md).</span></span>

## <a name="examples"></a><span data-ttu-id="c901a-213">Esempio</span><span class="sxs-lookup"><span data-stu-id="c901a-213">Examples</span></span>

<span data-ttu-id="c901a-214">Il codice seguente, tratto dall' [elenco dei gruppi locali utilizzando](https://Gallery.TechNet.Microsoft.Com/4474e390-776d-428e-906d-20668ce5933f) l'esempio di codice VBScript WMI nella raccolta TechNet, utilizza il **\_ gruppo Win32** per restituire informazioni sui gruppi locali presenti in un computer.</span><span class="sxs-lookup"><span data-stu-id="c901a-214">The following code, taken from the [List Local Groups Using WMI](https://Gallery.TechNet.Microsoft.Com/4474e390-776d-428e-906d-20668ce5933f) VBScript code example on TechNet Gallery, uses **Win32\_Group** to return information about the local groups found on a computer.</span></span>


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
Set colItems = objWMIService.ExecQuery _ 
    ("Select * from Win32_Group  Where LocalAccount = True") 
 
For Each objItem in colItems 
    Wscript.Echo "Caption: " & objItem.Caption 
    Wscript.Echo "Description: " & objItem.Description 
    Wscript.Echo "Domain: " & objItem.Domain 
    Wscript.Echo "Local Account: " & objItem.LocalAccount 
    Wscript.Echo "Name: " & objItem.Name 
    Wscript.Echo "SID: " & objItem.SID 
    Wscript.Echo "SID Type: " & objItem.SIDType 
    Wscript.Echo "Status: " & objItem.Status 
    Wscript.Echo 
Next 
```



## <a name="requirements"></a><span data-ttu-id="c901a-215">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c901a-215">Requirements</span></span>



| <span data-ttu-id="c901a-216">Requisito</span><span class="sxs-lookup"><span data-stu-id="c901a-216">Requirement</span></span> | <span data-ttu-id="c901a-217">Valore</span><span class="sxs-lookup"><span data-stu-id="c901a-217">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c901a-218">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c901a-218">Minimum supported client</span></span><br/> | <span data-ttu-id="c901a-219">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c901a-219">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c901a-220">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c901a-220">Minimum supported server</span></span><br/> | <span data-ttu-id="c901a-221">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c901a-221">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c901a-222">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c901a-222">Namespace</span></span><br/>                | <span data-ttu-id="c901a-223">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="c901a-223">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c901a-224">MOF</span><span class="sxs-lookup"><span data-stu-id="c901a-224">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c901a-225"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c901a-225"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c901a-226">DLL</span><span class="sxs-lookup"><span data-stu-id="c901a-226">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c901a-227"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c901a-227"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c901a-228">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c901a-228">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c901a-229">**\_Account Win32**</span><span class="sxs-lookup"><span data-stu-id="c901a-229">**Win32\_Account**</span></span>](win32-account.md)
</dt> <dt>

<span data-ttu-id="c901a-230">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c901a-230">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

