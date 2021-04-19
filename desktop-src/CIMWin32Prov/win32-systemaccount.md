---
description: Win32 \_ SystemAccount&\# 8194; Classe WMI che rappresenta un account di sistema.
ms.assetid: 0f745d93-cbac-428e-bf27-56f6e97d529f
ms.tgt_platform: multiple
title: Classe Win32_SystemAccount
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemAccount
- Win32_SystemAccount.Caption
- Win32_SystemAccount.Description
- Win32_SystemAccount.InstallDate
- Win32_SystemAccount.Status
- Win32_SystemAccount.LocalAccount
- Win32_SystemAccount.SID
- Win32_SystemAccount.SIDType
- Win32_SystemAccount.Domain
- Win32_SystemAccount.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1ef246a0ee372c5755aeb30980095e7f2f6ca1dc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305151"
---
# <a name="win32_systemaccount-class"></a><span data-ttu-id="b592d-103">Win32 \_ SystemAccount (classe)</span><span class="sxs-lookup"><span data-stu-id="b592d-103">Win32\_SystemAccount class</span></span>

<span data-ttu-id="b592d-104">La  [classe WMI](../wmisdk/retrieving-a-class.md) **\_ SystemAccount Win32** rappresenta un account di sistema.</span><span class="sxs-lookup"><span data-stu-id="b592d-104">The **Win32\_SystemAccount** [WMI class](../wmisdk/retrieving-a-class.md) represents a system account.</span></span> <span data-ttu-id="b592d-105">L'account di sistema viene utilizzato dal sistema operativo e dai servizi.</span><span class="sxs-lookup"><span data-stu-id="b592d-105">The system account is used by the operating system and services.</span></span> <span data-ttu-id="b592d-106">All'interno di Windows sono disponibili molti servizi e processi che richiedono la possibilità di accedere internamente, ad esempio durante un'installazione di Windows.</span><span class="sxs-lookup"><span data-stu-id="b592d-106">There are many services and processes within Windows that need the capability to logon internally, for example, during a Windows installation.</span></span> <span data-ttu-id="b592d-107">L'account di sistema è stato progettato a tale scopo.</span><span class="sxs-lookup"><span data-stu-id="b592d-107">The system account was designed for that purpose.</span></span>

<span data-ttu-id="b592d-108">L'account di sistema è un account interno che non viene visualizzato in gestione utenti, non può essere aggiunto a gruppi e non può avere diritti utente assegnati.</span><span class="sxs-lookup"><span data-stu-id="b592d-108">The system account is an internal account that does not show up in User Manager, cannot be added to any groups, and cannot have user rights assigned to it.</span></span> <span data-ttu-id="b592d-109">Tuttavia, l'account di sistema viene visualizzato in un volume file system NTFS in gestione file, che si trova nella sezione autorizzazioni del menu sicurezza.</span><span class="sxs-lookup"><span data-stu-id="b592d-109">However, the system account does show up on an NTFS file system volume in file manager, which is located in the Permissions section of the Security menu.</span></span> <span data-ttu-id="b592d-110">Per impostazione predefinita, all'account di sistema viene concesso il controllo completo su tutti i file in un volume file system NTFS, il che significa che l'account di sistema ha gli stessi privilegi funzionali dell'account amministratore.</span><span class="sxs-lookup"><span data-stu-id="b592d-110">By default, the system account is granted full control to all files on an NTFS file system volume, which means that the system account has the same functional privileges as the administrator account.</span></span>

<span data-ttu-id="b592d-111">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="b592d-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="b592d-112">Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="b592d-112">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b592d-113">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b592d-113">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4CA-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemAccount : Win32_Account
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

## <a name="members"></a><span data-ttu-id="b592d-114">Members</span><span class="sxs-lookup"><span data-stu-id="b592d-114">Members</span></span>

<span data-ttu-id="b592d-115">La classe **Win32 \_ SystemAccount** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="b592d-115">The **Win32\_SystemAccount** class has these types of members:</span></span>

-   [<span data-ttu-id="b592d-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b592d-116">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b592d-117">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b592d-117">Properties</span></span>

<span data-ttu-id="b592d-118">La classe **Win32 \_ SystemAccount** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="b592d-118">The **Win32\_SystemAccount** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b592d-119">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="b592d-119">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b592d-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b592d-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b592d-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b592d-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b592d-122">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="b592d-122">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="b592d-123">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b592d-123">A short textual description of the object.</span></span>

<span data-ttu-id="b592d-124">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b592d-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b592d-125">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="b592d-125">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b592d-126">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b592d-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b592d-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b592d-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b592d-128">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="b592d-128">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="b592d-129">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b592d-129">A textual description of the object.</span></span>

<span data-ttu-id="b592d-130">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b592d-130">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b592d-131">**Dominio**</span><span class="sxs-lookup"><span data-stu-id="b592d-131">**Domain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b592d-132">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b592d-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b592d-133">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b592d-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b592d-134">Qualificatori: [**override**](../wmisdk/standard-qualifiers.md) ("Domain"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Functions \| NomeDominio")</span><span class="sxs-lookup"><span data-stu-id="b592d-134">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Domain"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Functions\|domainname")</span></span>
</dt> </dl>

<span data-ttu-id="b592d-135">Nome del dominio Windows a cui appartiene l'account di sistema.</span><span class="sxs-lookup"><span data-stu-id="b592d-135">Name of the Windows domain to which the system account belongs.</span></span>

<span data-ttu-id="b592d-136">Esempio: "NA-SALES"</span><span class="sxs-lookup"><span data-stu-id="b592d-136">Example: "NA-SALES"</span></span>

</dd> <dt>

<span data-ttu-id="b592d-137">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="b592d-137">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b592d-138">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b592d-138">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b592d-139">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b592d-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b592d-140">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="b592d-140">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="b592d-141">Indica quando l'oggetto è stato installato.</span><span class="sxs-lookup"><span data-stu-id="b592d-141">Indicates when the object was installed.</span></span> <span data-ttu-id="b592d-142">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="b592d-142">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="b592d-143">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b592d-143">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b592d-144">**LocalAccount**</span><span class="sxs-lookup"><span data-stu-id="b592d-144">**LocalAccount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b592d-145">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="b592d-145">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b592d-146">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b592d-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b592d-147">Qualificatori: [ **corretti**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="b592d-147">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="b592d-148">Se **true**, l'account viene definito nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="b592d-148">If **TRUE**, the account is defined on the local machine.</span></span> <span data-ttu-id="b592d-149">Per recuperare solo gli account definiti nel computer locale, progettare una query che includa la condizione "LocalAccount =**true**".</span><span class="sxs-lookup"><span data-stu-id="b592d-149">To retrieve only accounts defined on the local machine, design a query that includes the condition "LocalAccount=**TRUE**".</span></span>

<span data-ttu-id="b592d-150">Questa proprietà viene ereditata [**dall' \_ account Win32**](win32-account.md).</span><span class="sxs-lookup"><span data-stu-id="b592d-150">This property is inherited from [**Win32\_Account**](win32-account.md).</span></span>

</dd> <dt>

<span data-ttu-id="b592d-151">**Nome**</span><span class="sxs-lookup"><span data-stu-id="b592d-151">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b592d-152">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b592d-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b592d-153">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b592d-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b592d-154">Qualificatori: [**override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| Name")</span><span class="sxs-lookup"><span data-stu-id="b592d-154">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|name")</span></span>
</dt> </dl>

<span data-ttu-id="b592d-155">Nome dell'account di sistema di Windows nel dominio specificato dalla proprietà del **dominio** di questa classe.</span><span class="sxs-lookup"><span data-stu-id="b592d-155">Name of the Windows system account on the domain specified by the **Domain** property of this class.</span></span>

</dd> <dt>

<span data-ttu-id="b592d-156">**SID**</span><span class="sxs-lookup"><span data-stu-id="b592d-156">**SID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b592d-157">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b592d-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b592d-158">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b592d-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b592d-159">Qualificatori: [**fixed**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Security Identifier (SID)")</span><span class="sxs-lookup"><span data-stu-id="b592d-159">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Security Identifiers (SIDs)")</span></span>
</dt> </dl>

<span data-ttu-id="b592d-160">ID di sicurezza (SID) per l'account.</span><span class="sxs-lookup"><span data-stu-id="b592d-160">Security identifier (SID) for this account.</span></span> <span data-ttu-id="b592d-161">Un SID è un valore stringa di lunghezza variabile usato per identificare un trustee.</span><span class="sxs-lookup"><span data-stu-id="b592d-161">A SID is a string value of variable length used to identify a trustee.</span></span> <span data-ttu-id="b592d-162">Ogni account dispone di un SID univoco emesso da un'autorità, ad esempio un dominio di Windows, archiviato in un database di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="b592d-162">Each account has a unique SID issued by an authority (such as a Windows domain), stored in a security database.</span></span> <span data-ttu-id="b592d-163">Quando un utente esegue l'accesso, il sistema Recupera il SID dell'utente dal database e lo inserisce nel token di accesso dell'utente.</span><span class="sxs-lookup"><span data-stu-id="b592d-163">When a user logs on, the system retrieves the user's SID from the database and places it in the user's access token.</span></span> <span data-ttu-id="b592d-164">Il sistema usa il SID nel token di accesso dell'utente per identificare l'utente in tutte le interazioni successive con la sicurezza di Windows.</span><span class="sxs-lookup"><span data-stu-id="b592d-164">The system uses the SID in the user's access token to identify the user in all subsequent interactions with Windows security.</span></span> <span data-ttu-id="b592d-165">Quando un SID è stato usato come identificatore univoco per un utente o un gruppo, non può essere usato di nuovo per identificare un altro utente o gruppo.</span><span class="sxs-lookup"><span data-stu-id="b592d-165">When a SID has been used as the unique identifier for a user or group, it cannot be used again to identify another user or group.</span></span>

<span data-ttu-id="b592d-166">Questa proprietà viene ereditata [**dall' \_ account Win32**](win32-account.md).</span><span class="sxs-lookup"><span data-stu-id="b592d-166">This property is inherited from [**Win32\_Account**](win32-account.md).</span></span>

</dd> <dt>

<span data-ttu-id="b592d-167">**SIDType**</span><span class="sxs-lookup"><span data-stu-id="b592d-167">**SIDType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b592d-168">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="b592d-168">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="b592d-169">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b592d-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b592d-170">Qualificatori: [**fixed**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API di \| controllo di accesso tipi di enumerazione \| SID \_ nome \_ utilizzo")</span><span class="sxs-lookup"><span data-stu-id="b592d-170">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Access Control Enumeration Types\|SID\_NAME\_USE")</span></span>
</dt> </dl>

<span data-ttu-id="b592d-171">Valori enumerati che specificano il tipo di ID di sicurezza (SID).</span><span class="sxs-lookup"><span data-stu-id="b592d-171">Enumerated values that specify the type of security identifier (SID).</span></span>

<span data-ttu-id="b592d-172">Questa proprietà viene ereditata [**dall' \_ account Win32**](win32-account.md).</span><span class="sxs-lookup"><span data-stu-id="b592d-172">This property is inherited from [**Win32\_Account**](win32-account.md).</span></span>

<dt>

<span id="SidTypeUser"></span><span id="sidtypeuser"></span><span id="SIDTYPEUSER"></span>

<span data-ttu-id="b592d-173">**SidTypeUser** (1)</span><span class="sxs-lookup"><span data-stu-id="b592d-173">**SidTypeUser** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeGroup"></span><span id="sidtypegroup"></span><span id="SIDTYPEGROUP"></span>

<span data-ttu-id="b592d-174">**SidTypeGroup** (2)</span><span class="sxs-lookup"><span data-stu-id="b592d-174">**SidTypeGroup** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeDomain"></span><span id="sidtypedomain"></span><span id="SIDTYPEDOMAIN"></span>

<span data-ttu-id="b592d-175">**SidTypeDomain** (3)</span><span class="sxs-lookup"><span data-stu-id="b592d-175">**SidTypeDomain** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeAlias"></span><span id="sidtypealias"></span><span id="SIDTYPEALIAS"></span>

<span data-ttu-id="b592d-176">**SidTypeAlias** (4)</span><span class="sxs-lookup"><span data-stu-id="b592d-176">**SidTypeAlias** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeWellKnownGroup"></span><span id="sidtypewellknowngroup"></span><span id="SIDTYPEWELLKNOWNGROUP"></span>

<span data-ttu-id="b592d-177">**SidTypeWellKnownGroup** (5)</span><span class="sxs-lookup"><span data-stu-id="b592d-177">**SidTypeWellKnownGroup** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeDeletedAccount"></span><span id="sidtypedeletedaccount"></span><span id="SIDTYPEDELETEDACCOUNT"></span>

<span data-ttu-id="b592d-178">**SidTypeDeletedAccount** (6)</span><span class="sxs-lookup"><span data-stu-id="b592d-178">**SidTypeDeletedAccount** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeInvalid"></span><span id="sidtypeinvalid"></span><span id="SIDTYPEINVALID"></span>

<span data-ttu-id="b592d-179">**SidTypeInvalid** (7)</span><span class="sxs-lookup"><span data-stu-id="b592d-179">**SidTypeInvalid** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeUnknown"></span><span id="sidtypeunknown"></span><span id="SIDTYPEUNKNOWN"></span>

<span data-ttu-id="b592d-180">**SidTypeUnknown** (8)</span><span class="sxs-lookup"><span data-stu-id="b592d-180">**SidTypeUnknown** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeComputer"></span><span id="sidtypecomputer"></span><span id="SIDTYPECOMPUTER"></span>

<span data-ttu-id="b592d-181">**SidTypeComputer** (9)</span><span class="sxs-lookup"><span data-stu-id="b592d-181">**SidTypeComputer** (9)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b592d-182">**Status**</span><span class="sxs-lookup"><span data-stu-id="b592d-182">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b592d-183">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b592d-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b592d-184">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b592d-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b592d-185">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="b592d-185">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="b592d-186">Stringa che indica lo stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b592d-186">String that indicates the current status of the object.</span></span> <span data-ttu-id="b592d-187">È possibile definire lo stato operativo e non operativo.</span><span class="sxs-lookup"><span data-stu-id="b592d-187">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="b592d-188">Lo stato operativo può includere "OK", "danneggiato" e "errore predazione".</span><span class="sxs-lookup"><span data-stu-id="b592d-188">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="b592d-189">"Predator fail" indica che un elemento funziona correttamente, ma sta stimando un errore, ad esempio un'unità disco rigido abilitata per SMART.</span><span class="sxs-lookup"><span data-stu-id="b592d-189">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="b592d-190">Lo stato non operativo può includere "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="b592d-190">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="b592d-191">Il "servizio" può essere applicato durante il mirroring del disco, ovvero la riattivazione, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="b592d-191">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="b592d-192">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="b592d-192">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="b592d-193">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b592d-193">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="b592d-194">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="b592d-194">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="b592d-195">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="b592d-195">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="b592d-196">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="b592d-196">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="b592d-197">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="b592d-197">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b592d-198">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="b592d-198">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="b592d-199">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="b592d-199">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="b592d-200">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="b592d-200">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="b592d-201">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="b592d-201">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="b592d-202">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="b592d-202">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="b592d-203">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="b592d-203">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="b592d-204">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="b592d-204">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="b592d-205">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="b592d-205">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="b592d-206">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="b592d-206">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="b592d-207"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="b592d-207"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="b592d-208">Commenti</span><span class="sxs-lookup"><span data-stu-id="b592d-208">Remarks</span></span>

<span data-ttu-id="b592d-209">La classe **Win32 \_ SystemAccount** è derivata dall' [**\_ account Win32**](win32-account.md).</span><span class="sxs-lookup"><span data-stu-id="b592d-209">The **Win32\_SystemAccount** class is derived from [**Win32\_Account**](win32-account.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b592d-210">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b592d-210">Requirements</span></span>



| <span data-ttu-id="b592d-211">Requisito</span><span class="sxs-lookup"><span data-stu-id="b592d-211">Requirement</span></span> | <span data-ttu-id="b592d-212">Valore</span><span class="sxs-lookup"><span data-stu-id="b592d-212">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b592d-213">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b592d-213">Minimum supported client</span></span><br/> | <span data-ttu-id="b592d-214">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b592d-214">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b592d-215">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b592d-215">Minimum supported server</span></span><br/> | <span data-ttu-id="b592d-216">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b592d-216">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b592d-217">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b592d-217">Namespace</span></span><br/>                | <span data-ttu-id="b592d-218">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="b592d-218">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b592d-219">MOF</span><span class="sxs-lookup"><span data-stu-id="b592d-219">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b592d-220"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b592d-220"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b592d-221">DLL</span><span class="sxs-lookup"><span data-stu-id="b592d-221">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b592d-222"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b592d-222"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b592d-223">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b592d-223">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b592d-224">**\_Account Win32**</span><span class="sxs-lookup"><span data-stu-id="b592d-224">**Win32\_Account**</span></span>](win32-account.md)
</dt> <dt>

[<span data-ttu-id="b592d-225">Classi del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="b592d-225">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
