---
description: Contiene informazioni sugli account utente e gli account di gruppo noti al sistema del computer in cui è in esecuzione Windows.
ms.assetid: c0916f20-05be-4282-9642-28cec606bfd7
ms.tgt_platform: multiple
title: Classe Win32_Account
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Account
- Win32_Account.Caption
- Win32_Account.Description
- Win32_Account.Domain
- Win32_Account.InstallDate
- Win32_Account.LocalAccount
- Win32_Account.Name
- Win32_Account.SID
- Win32_Account.SIDType
- Win32_Account.Status
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2af601799095192d7af4ffedce0c8e0cd28bff21
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127494"
---
# <a name="win32_account-class"></a><span data-ttu-id="039ff-103">\_Classe account Win32</span><span class="sxs-lookup"><span data-stu-id="039ff-103">Win32\_Account class</span></span>

<span data-ttu-id="039ff-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) astratta dell' **\_ account Win32** contiene informazioni sugli account utente e gli account di gruppo noti al sistema del computer in cui è in esecuzione Windows.</span><span class="sxs-lookup"><span data-stu-id="039ff-104">The **Win32\_Account** abstract [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) contains information about user accounts and group accounts known to the computer system running Windows.</span></span> <span data-ttu-id="039ff-105">I nomi degli utenti o dei gruppi riconosciuti da un dominio di Windows sono discendenti (o membri) di questa classe.</span><span class="sxs-lookup"><span data-stu-id="039ff-105">User or group names recognized by a Windows domain are descendants (or members) of this class.</span></span>

<span data-ttu-id="039ff-106">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="039ff-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="039ff-107">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="039ff-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="039ff-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="039ff-108">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C4C9-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_Account : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  string   Domain;
  datetime InstallDate;
  boolean  LocalAccount;
  string   Name;
  string   SID;
  uint8    SIDType;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="039ff-109">Members</span><span class="sxs-lookup"><span data-stu-id="039ff-109">Members</span></span>

<span data-ttu-id="039ff-110">La classe dell' **\_ account Win32** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="039ff-110">The **Win32\_Account** class has these types of members:</span></span>

-   [<span data-ttu-id="039ff-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="039ff-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="039ff-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="039ff-112">Properties</span></span>

<span data-ttu-id="039ff-113">La classe dell' **\_ account Win32** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="039ff-113">The **Win32\_Account** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="039ff-114">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="039ff-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="039ff-115">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="039ff-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="039ff-116">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="039ff-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="039ff-117">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="039ff-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="039ff-118">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="039ff-118">Short description of the object.</span></span>

<span data-ttu-id="039ff-119">Questa proprietà viene ereditata dalla classe [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md) .</span><span class="sxs-lookup"><span data-stu-id="039ff-119">This property is inherited from the [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="039ff-120">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="039ff-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="039ff-121">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="039ff-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="039ff-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="039ff-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="039ff-123">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="039ff-123">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="039ff-124">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="039ff-124">Description of the object.</span></span>

<span data-ttu-id="039ff-125">Questa proprietà viene ereditata dalla classe [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md) .</span><span class="sxs-lookup"><span data-stu-id="039ff-125">This property is inherited from the [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="039ff-126">**Dominio**</span><span class="sxs-lookup"><span data-stu-id="039ff-126">**Domain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="039ff-127">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="039ff-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="039ff-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="039ff-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="039ff-129">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Network Management Functions \| Domain")</span><span class="sxs-lookup"><span data-stu-id="039ff-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Network Management Functions\|Domain")</span></span>
</dt> </dl>

<span data-ttu-id="039ff-130">Nome del dominio Windows a cui appartiene un gruppo o un utente.</span><span class="sxs-lookup"><span data-stu-id="039ff-130">Name of the Windows domain to which a group or user belongs.</span></span>

<span data-ttu-id="039ff-131">Esempio: "NA-SALES"</span><span class="sxs-lookup"><span data-stu-id="039ff-131">Example: "NA-SALES"</span></span>

</dd> <dt>

<span data-ttu-id="039ff-132">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="039ff-132">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="039ff-133">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="039ff-133">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="039ff-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="039ff-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="039ff-135">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="039ff-135">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="039ff-136">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="039ff-136">Date and time that the object was installed.</span></span> <span data-ttu-id="039ff-137">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="039ff-137">This property does not require a value to indicate that the object is installed.</span></span>

<span data-ttu-id="039ff-138">Questa proprietà viene ereditata dalla classe [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md) .</span><span class="sxs-lookup"><span data-stu-id="039ff-138">This property is inherited from the [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="039ff-139">**LocalAccount**</span><span class="sxs-lookup"><span data-stu-id="039ff-139">**LocalAccount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="039ff-140">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="039ff-140">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="039ff-141">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="039ff-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="039ff-142">Qualificatori: [ **corretti**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="039ff-142">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="039ff-143">Se **true**, l'account viene definito nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="039ff-143">If **TRUE**, the account is defined on the local machine.</span></span> <span data-ttu-id="039ff-144">Per recuperare solo gli account definiti nel computer locale, progettare una query che includa la condizione "LocalAccount =**true**".</span><span class="sxs-lookup"><span data-stu-id="039ff-144">To retrieve only accounts defined on the local machine, design a query that includes the condition "LocalAccount=**TRUE**".</span></span>

</dd> <dt>

<span data-ttu-id="039ff-145">**Nome**</span><span class="sxs-lookup"><span data-stu-id="039ff-145">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="039ff-146">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="039ff-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="039ff-147">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="039ff-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="039ff-148">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Network Management Structures \| Name")</span><span class="sxs-lookup"><span data-stu-id="039ff-148">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Network Management Structures\|name")</span></span>
</dt> </dl>

<span data-ttu-id="039ff-149">Nome dell'account di sistema di Windows nel dominio specificato dalla proprietà del **dominio** di questa classe.</span><span class="sxs-lookup"><span data-stu-id="039ff-149">Name of the Windows system account on the domain specified by the **Domain** property of this class.</span></span> <span data-ttu-id="039ff-150">Questa proprietà esegue l'override della proprietà **Name** ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="039ff-150">This property overrides the **Name** property inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="039ff-151">**SID**</span><span class="sxs-lookup"><span data-stu-id="039ff-151">**SID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="039ff-152">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="039ff-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="039ff-153">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="039ff-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="039ff-154">Qualificatori: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Security Identifier (SID)")</span><span class="sxs-lookup"><span data-stu-id="039ff-154">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Security Identifiers (SIDs)")</span></span>
</dt> </dl>

<span data-ttu-id="039ff-155">ID di sicurezza (SID) per l'account.</span><span class="sxs-lookup"><span data-stu-id="039ff-155">Security identifier (SID) for this account.</span></span> <span data-ttu-id="039ff-156">Un SID è un valore stringa di lunghezza variabile usato per identificare un trustee.</span><span class="sxs-lookup"><span data-stu-id="039ff-156">A SID is a string value of variable length used to identify a trustee.</span></span> <span data-ttu-id="039ff-157">Ogni account dispone di un SID univoco emesso da un'autorità, ad esempio un dominio di Windows, archiviato in un database di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="039ff-157">Each account has a unique SID issued by an authority (such as a Windows domain), stored in a security database.</span></span> <span data-ttu-id="039ff-158">Quando un utente esegue l'accesso, il sistema Recupera il SID dell'utente dal database e lo inserisce nel token di accesso dell'utente.</span><span class="sxs-lookup"><span data-stu-id="039ff-158">When a user logs on, the system retrieves the user's SID from the database and places it in the user's access token.</span></span> <span data-ttu-id="039ff-159">Il sistema usa il SID nel token di accesso dell'utente per identificare l'utente in tutte le interazioni successive con la sicurezza di Windows.</span><span class="sxs-lookup"><span data-stu-id="039ff-159">The system uses the SID in the user's access token to identify the user in all subsequent interactions with Windows security.</span></span> <span data-ttu-id="039ff-160">Quando un SID è stato usato come identificatore univoco per un utente o un gruppo, non può essere usato di nuovo per identificare un altro utente o gruppo.</span><span class="sxs-lookup"><span data-stu-id="039ff-160">When a SID has been used as the unique identifier for a user or group, it cannot be used again to identify another user or group.</span></span>

</dd> <dt>

<span data-ttu-id="039ff-161">**SIDType**</span><span class="sxs-lookup"><span data-stu-id="039ff-161">**SIDType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="039ff-162">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="039ff-162">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="039ff-163">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="039ff-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="039ff-164">Qualificatori: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API di \| controllo di accesso tipi di enumerazione \| SID \_ nome \_ utilizzo")</span><span class="sxs-lookup"><span data-stu-id="039ff-164">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Access Control Enumeration Types\|SID\_NAME\_USE")</span></span>
</dt> </dl>

<span data-ttu-id="039ff-165">Valori enumerati che specificano il tipo di ID di sicurezza (SID).</span><span class="sxs-lookup"><span data-stu-id="039ff-165">Enumerated values that specify the type of security identifier (SID).</span></span>

<dt>

<span id="SidTypeUser"></span><span id="sidtypeuser"></span><span id="SIDTYPEUSER"></span>

<span data-ttu-id="039ff-166">**SidTypeUser** (1)</span><span class="sxs-lookup"><span data-stu-id="039ff-166">**SidTypeUser** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeGroup"></span><span id="sidtypegroup"></span><span id="SIDTYPEGROUP"></span>

<span data-ttu-id="039ff-167">**SidTypeGroup** (2)</span><span class="sxs-lookup"><span data-stu-id="039ff-167">**SidTypeGroup** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeDomain"></span><span id="sidtypedomain"></span><span id="SIDTYPEDOMAIN"></span>

<span data-ttu-id="039ff-168">**SidTypeDomain** (3)</span><span class="sxs-lookup"><span data-stu-id="039ff-168">**SidTypeDomain** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeAlias"></span><span id="sidtypealias"></span><span id="SIDTYPEALIAS"></span>

<span data-ttu-id="039ff-169">**SidTypeAlias** (4)</span><span class="sxs-lookup"><span data-stu-id="039ff-169">**SidTypeAlias** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeWellKnownGroup"></span><span id="sidtypewellknowngroup"></span><span id="SIDTYPEWELLKNOWNGROUP"></span>

<span data-ttu-id="039ff-170">**SidTypeWellKnownGroup** (5)</span><span class="sxs-lookup"><span data-stu-id="039ff-170">**SidTypeWellKnownGroup** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeDeletedAccount"></span><span id="sidtypedeletedaccount"></span><span id="SIDTYPEDELETEDACCOUNT"></span>

<span data-ttu-id="039ff-171">**SidTypeDeletedAccount** (6)</span><span class="sxs-lookup"><span data-stu-id="039ff-171">**SidTypeDeletedAccount** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeInvalid"></span><span id="sidtypeinvalid"></span><span id="SIDTYPEINVALID"></span>

<span data-ttu-id="039ff-172">**SidTypeInvalid** (7)</span><span class="sxs-lookup"><span data-stu-id="039ff-172">**SidTypeInvalid** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeUnknown"></span><span id="sidtypeunknown"></span><span id="SIDTYPEUNKNOWN"></span>

<span data-ttu-id="039ff-173">**SidTypeUnknown** (8)</span><span class="sxs-lookup"><span data-stu-id="039ff-173">**SidTypeUnknown** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeComputer"></span><span id="sidtypecomputer"></span><span id="SIDTYPECOMPUTER"></span>

<span data-ttu-id="039ff-174">**SidTypeComputer** (9)</span><span class="sxs-lookup"><span data-stu-id="039ff-174">**SidTypeComputer** (9)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="039ff-175">**Status**</span><span class="sxs-lookup"><span data-stu-id="039ff-175">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="039ff-176">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="039ff-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="039ff-177">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="039ff-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="039ff-178">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="039ff-178">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="039ff-179">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="039ff-179">Current status of the object.</span></span> <span data-ttu-id="039ff-180">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="039ff-180">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="039ff-181">Gli stati operativi includono: "OK", "degradato" e "errore predazione" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, può funzionare correttamente, ma prevede un errore nel prossimo futuro).</span><span class="sxs-lookup"><span data-stu-id="039ff-181">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicts a failure in the near future).</span></span> <span data-ttu-id="039ff-182">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="039ff-182">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="039ff-183">Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="039ff-183">The latter, "Service", can apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="039ff-184">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="039ff-184">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="039ff-185">Questa proprietà viene ereditata dalla classe [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md) .</span><span class="sxs-lookup"><span data-stu-id="039ff-185">This property is inherited from the [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) class.</span></span>

<span data-ttu-id="039ff-186">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="039ff-186">The values are:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="039ff-187">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="039ff-187">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="039ff-188">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="039ff-188">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="039ff-189">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="039ff-189">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="039ff-190">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="039ff-190">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="039ff-191">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="039ff-191">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="039ff-192">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="039ff-192">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="039ff-193">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="039ff-193">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="039ff-194">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="039ff-194">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="039ff-195">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="039ff-195">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="039ff-196">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="039ff-196">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="039ff-197">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="039ff-197">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="039ff-198">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="039ff-198">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="039ff-199"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="039ff-199"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="039ff-200">Commenti</span><span class="sxs-lookup"><span data-stu-id="039ff-200">Remarks</span></span>

<span data-ttu-id="039ff-201">La classe dell' **\_ account Win32** è derivata da [**CIM \_ LogicalElement**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="039ff-201">The **Win32\_Account** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

## <a name="examples"></a><span data-ttu-id="039ff-202">Esempio</span><span class="sxs-lookup"><span data-stu-id="039ff-202">Examples</span></span>

<span data-ttu-id="039ff-203">Il codice di PowerShell seguente recupera gli account locali.</span><span class="sxs-lookup"><span data-stu-id="039ff-203">The following PowerShell code retrieves the local accounts.</span></span>


```PowerShell
Get-WmiObject Win32_Account -Filter "Domain='$Env:ComputerName'"
```



<span data-ttu-id="039ff-204">Il codice di PowerShell seguente recupera gli account di dominio.</span><span class="sxs-lookup"><span data-stu-id="039ff-204">The following PowerShell code retrieves the domain accounts.</span></span>


```PowerShell
 Get-WmiObject Win32_Account -Filter "Domain='$Env:UserDomain'" 
```



## <a name="requirements"></a><span data-ttu-id="039ff-205">Requisiti</span><span class="sxs-lookup"><span data-stu-id="039ff-205">Requirements</span></span>



| <span data-ttu-id="039ff-206">Requisito</span><span class="sxs-lookup"><span data-stu-id="039ff-206">Requirement</span></span> | <span data-ttu-id="039ff-207">Valore</span><span class="sxs-lookup"><span data-stu-id="039ff-207">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="039ff-208">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="039ff-208">Minimum supported client</span></span><br/> | <span data-ttu-id="039ff-209">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="039ff-209">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="039ff-210">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="039ff-210">Minimum supported server</span></span><br/> | <span data-ttu-id="039ff-211">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="039ff-211">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="039ff-212">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="039ff-212">Namespace</span></span><br/>                | <span data-ttu-id="039ff-213">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="039ff-213">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="039ff-214">MOF</span><span class="sxs-lookup"><span data-stu-id="039ff-214">MOF</span></span><br/>                      | <dl> <span data-ttu-id="039ff-215"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="039ff-215"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="039ff-216">DLL</span><span class="sxs-lookup"><span data-stu-id="039ff-216">DLL</span></span><br/>                      | <dl> <span data-ttu-id="039ff-217"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="039ff-217"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="039ff-218">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="039ff-218">See also</span></span>

<dl> <dt>

[<span data-ttu-id="039ff-219">**\_LogicalElement CIM**</span><span class="sxs-lookup"><span data-stu-id="039ff-219">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

<span data-ttu-id="039ff-220">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="039ff-220">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

