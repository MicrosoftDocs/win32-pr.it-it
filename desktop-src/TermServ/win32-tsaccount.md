---
title: Classe Win32_TSAccount
description: Consente l'eliminazione di un account esistente nel terminale Win32 \_ e la modifica delle autorizzazioni esistenti.
ms.assetid: fd4d8a0f-685b-4619-84f1-faefbabd04ba
ms.tgt_platform: multiple
keywords:
- Classe Win32_TSAccount Servizi Desktop remoto
- Classe Win32_TSAccount Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_TSAccount
- Win32_TSAccount.Caption
- Win32_TSAccount.Description
- Win32_TSAccount.InstallDate
- Win32_TSAccount.Name
- Win32_TSAccount.Status
- Win32_TSAccount.TerminalName
- Win32_TSAccount.AccountName
- Win32_TSAccount.AuditFail
- Win32_TSAccount.AuditSuccess
- Win32_TSAccount.PermissionsAllowed
- Win32_TSAccount.PermissionsDenied
- Win32_TSAccount.SID
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10fed32943cf89728081e2443dfffe2e3762298d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302432"
---
# <a name="win32_tsaccount-class"></a><span data-ttu-id="51665-105">Win32 \_ TSAccount (classe)</span><span class="sxs-lookup"><span data-stu-id="51665-105">Win32\_TSAccount class</span></span>

<span data-ttu-id="51665-106">La classe WMI **Win32 \_ TSAccount** consente l'eliminazione di un account esistente nel [**\_ terminale Win32**](win32-terminal.md) e la modifica delle autorizzazioni esistenti.</span><span class="sxs-lookup"><span data-stu-id="51665-106">The **Win32\_TSAccount** WMI class allows deletion of an account that exists on the [**Win32\_Terminal**](win32-terminal.md) and modification of existing permissions.</span></span>

<span data-ttu-id="51665-107">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà definite ed ereditate, in ordine alfabetico.</span><span class="sxs-lookup"><span data-stu-id="51665-107">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span> <span data-ttu-id="51665-108">Per informazioni di riferimento sui metodi, vedere la tabella dei metodi più avanti in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="51665-108">For reference information on methods, see the table of methods later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="51665-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="51665-109">Syntax</span></span>

``` syntax
[dynamic, overwrite, provider("Win32_WIN32_TSACCOUNT_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSAccount : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  string   AccountName;
  uint32   AuditFail;
  uint32   AuditSuccess;
  uint32   PermissionsAllowed;
  uint32   PermissionsDenied;
  string   SID;
};
```

## <a name="members"></a><span data-ttu-id="51665-110">Members</span><span class="sxs-lookup"><span data-stu-id="51665-110">Members</span></span>

<span data-ttu-id="51665-111">La classe **Win32 \_ TSAccount** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="51665-111">The **Win32\_TSAccount** class has these types of members:</span></span>

-   [<span data-ttu-id="51665-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="51665-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="51665-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="51665-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="51665-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="51665-114">Methods</span></span>

<span data-ttu-id="51665-115">La classe **Win32 \_ TSAccount** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="51665-115">The **Win32\_TSAccount** class has these methods.</span></span>



| <span data-ttu-id="51665-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="51665-116">Method</span></span>                                                                   | <span data-ttu-id="51665-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="51665-117">Description</span></span>                                                                                  |
|:-------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="51665-118">**Eliminare**</span><span class="sxs-lookup"><span data-stu-id="51665-118">**Delete**</span></span>](win32-tsaccount-delete.md)                                 | <span data-ttu-id="51665-119">Elimina l'account utente, gruppo o computer specificato.</span><span class="sxs-lookup"><span data-stu-id="51665-119">Deletes the specified user, group, or computer account.</span></span><br/>                           |
| [<span data-ttu-id="51665-120">**ModifyAuditPermissions**</span><span class="sxs-lookup"><span data-stu-id="51665-120">**ModifyAuditPermissions**</span></span>](win32-tsaccount-modifyauditpermissions.md) | <span data-ttu-id="51665-121">Modifica la granularità del set di autorizzazioni di controllo dell'account specificato.</span><span class="sxs-lookup"><span data-stu-id="51665-121">Changes the granularity of the set of audit permissions of the specified account.</span></span><br/> |
| [<span data-ttu-id="51665-122">**ModifyPermissions**</span><span class="sxs-lookup"><span data-stu-id="51665-122">**ModifyPermissions**</span></span>](win32-tsaccount-modifypermissions.md)           | <span data-ttu-id="51665-123">Imposta un set di autorizzazioni più granulare per l'account specificato.</span><span class="sxs-lookup"><span data-stu-id="51665-123">Sets a more granular permission set to the specified account.</span></span><br/>                     |



 

### <a name="properties"></a><span data-ttu-id="51665-124">Proprietà</span><span class="sxs-lookup"><span data-stu-id="51665-124">Properties</span></span>

<span data-ttu-id="51665-125">La classe **Win32 \_ TSAccount** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="51665-125">The **Win32\_TSAccount** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="51665-126">**AccountName**</span><span class="sxs-lookup"><span data-stu-id="51665-126">**AccountName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51665-127">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="51665-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="51665-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="51665-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51665-129">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="51665-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="51665-130">Nome corrente dell'account.</span><span class="sxs-lookup"><span data-stu-id="51665-130">The current name of the account.</span></span> <span data-ttu-id="51665-131">Il nome di dominio è incluso.</span><span class="sxs-lookup"><span data-stu-id="51665-131">The domain name is included.</span></span>

</dd> <dt>

<span data-ttu-id="51665-132">**AuditFail**</span><span class="sxs-lookup"><span data-stu-id="51665-132">**AuditFail**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51665-133">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="51665-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="51665-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="51665-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51665-135">Specifica le [autorizzazioni di host sessione Desktop remoto Services](terminal-services-permissions.md) controllate per una condizione di errore.</span><span class="sxs-lookup"><span data-stu-id="51665-135">Specifies the [Remote Desktop Session Host Services Permissions](terminal-services-permissions.md) that are audited for a failure condition.</span></span> <span data-ttu-id="51665-136">Il valore di questa proprietà è una maschera di maschera, che può essere impostata su uno o più valori della proprietà **PermissionsAllowed** .</span><span class="sxs-lookup"><span data-stu-id="51665-136">The value of this property is a bitmask, which can be set to one or more of the values of the **PermissionsAllowed** property.</span></span>

<dt>

<span id="WINSTATION_QUERY_0x1"></span><span id="winstation_query_0x1"></span><span id="WINSTATION_QUERY_0X1"></span>

<span data-ttu-id="51665-137">**WINSTATION \_ QUERY = 0x1** (0)</span><span class="sxs-lookup"><span data-stu-id="51665-137">**WINSTATION\_QUERY=0x1** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_SET_0x2"></span><span id="winstation_set_0x2"></span><span id="WINSTATION_SET_0X2"></span>

<span data-ttu-id="51665-138">**WINSTATION \_ SET = 0x2** (1)</span><span class="sxs-lookup"><span data-stu-id="51665-138">**WINSTATION\_SET=0x2** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_LOGOFF_0x4"></span><span id="winstation_logoff_0x4"></span><span id="WINSTATION_LOGOFF_0X4"></span>

<span data-ttu-id="51665-139">**WINSTATION \_ Disconnessione = 0x4** (2)</span><span class="sxs-lookup"><span data-stu-id="51665-139">**WINSTATION\_LOGOFF=0x4** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED___0xF008"></span><span id="winstation_virtual___standard_rights_required___0xf008"></span><span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED___0XF008"></span>

<span data-ttu-id="51665-140">**WINSTATION \_ \| Diritti standard \_ virtuali \_ richiesti = 0xF008** (3)</span><span class="sxs-lookup"><span data-stu-id="51665-140">**WINSTATION\_VIRTUAL \| STANDARD\_RIGHTS\_REQUIRED = 0xF008** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_SHADOW_0x10"></span><span id="winstation_shadow_0x10"></span><span id="WINSTATION_SHADOW_0X10"></span>

<span data-ttu-id="51665-141">**WINSTATION \_ SHADOW = 0x10** (4)</span><span class="sxs-lookup"><span data-stu-id="51665-141">**WINSTATION\_SHADOW=0x10** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_LOGON_0x20"></span><span id="winstation_logon_0x20"></span><span id="WINSTATION_LOGON_0X20"></span>

<span data-ttu-id="51665-142">**WINSTATION \_ LOGON = 0x20** (5)</span><span class="sxs-lookup"><span data-stu-id="51665-142">**WINSTATION\_LOGON=0x20** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_MSG_0x80"></span><span id="winstation_msg_0x80"></span><span id="WINSTATION_MSG_0X80"></span>

<span data-ttu-id="51665-143">**WINSTATION \_ MESSAGGIO = 0x80** (6)</span><span class="sxs-lookup"><span data-stu-id="51665-143">**WINSTATION\_MSG=0x80** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_CONNECT_0x100"></span><span id="winstation_connect_0x100"></span><span id="WINSTATION_CONNECT_0X100"></span>

<span data-ttu-id="51665-144">**WINSTATION \_ Connetti = 0x100** (7)</span><span class="sxs-lookup"><span data-stu-id="51665-144">**WINSTATION\_CONNECT=0x100** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_DISCONNECT_0x200"></span><span id="winstation_disconnect_0x200"></span><span id="WINSTATION_DISCONNECT_0X200"></span>

<span data-ttu-id="51665-145">**WINSTATION \_ Disconnect = 0x200** (8)</span><span class="sxs-lookup"><span data-stu-id="51665-145">**WINSTATION\_DISCONNECT=0x200** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="51665-146">**AuditSuccess**</span><span class="sxs-lookup"><span data-stu-id="51665-146">**AuditSuccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51665-147">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="51665-147">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="51665-148">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="51665-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51665-149">Specifica le autorizzazioni specifiche per il server Host sessione Desktop remoto controllate per una condizione di esito positivo.</span><span class="sxs-lookup"><span data-stu-id="51665-149">Specifies the RD Session Host server-specific permissions that are audited for a success condition.</span></span> <span data-ttu-id="51665-150">Il valore di questa proprietà è una maschera di maschera, che può essere impostata su uno o più valori della proprietà **PermissionsAllowed** .</span><span class="sxs-lookup"><span data-stu-id="51665-150">The value of this property is a bitmask, which can be set to one or more of the values of the **PermissionsAllowed** property.</span></span>

<dt>

<span id="WINSTATION_QUERY_0x1"></span><span id="winstation_query_0x1"></span><span id="WINSTATION_QUERY_0X1"></span>

<span data-ttu-id="51665-151">**WINSTATION \_ QUERY = 0x1** (0)</span><span class="sxs-lookup"><span data-stu-id="51665-151">**WINSTATION\_QUERY=0x1** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_SET_0x2"></span><span id="winstation_set_0x2"></span><span id="WINSTATION_SET_0X2"></span>

<span data-ttu-id="51665-152">**WINSTATION \_ SET = 0x2** (1)</span><span class="sxs-lookup"><span data-stu-id="51665-152">**WINSTATION\_SET=0x2** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_LOGOFF_0x4WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED___0xF008"></span><span id="winstation_logoff_0x4winstation_virtual___standard_rights_required___0xf008"></span><span id="WINSTATION_LOGOFF_0X4WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED___0XF008"></span>

<span data-ttu-id="51665-153">**WINSTATION \_ Disconnessione = 0x4WINSTATION \_ virtual \| standard \_ Rights \_ required = 0xF008** (2)</span><span class="sxs-lookup"><span data-stu-id="51665-153">**WINSTATION\_LOGOFF=0x4WINSTATION\_VIRTUAL \| STANDARD\_RIGHTS\_REQUIRED = 0xF008** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_SHADOW_0x10"></span><span id="winstation_shadow_0x10"></span><span id="WINSTATION_SHADOW_0X10"></span>

<span data-ttu-id="51665-154">**WINSTATION \_ SHADOW = 0x10** (3)</span><span class="sxs-lookup"><span data-stu-id="51665-154">**WINSTATION\_SHADOW=0x10** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_LOGON_0x20"></span><span id="winstation_logon_0x20"></span><span id="WINSTATION_LOGON_0X20"></span>

<span data-ttu-id="51665-155">**WINSTATION \_ LOGON = 0x20** (4)</span><span class="sxs-lookup"><span data-stu-id="51665-155">**WINSTATION\_LOGON=0x20** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_MSG_0x80"></span><span id="winstation_msg_0x80"></span><span id="WINSTATION_MSG_0X80"></span>

<span data-ttu-id="51665-156">**WINSTATION \_ MESSAGGIO = 0x80** (5)</span><span class="sxs-lookup"><span data-stu-id="51665-156">**WINSTATION\_MSG=0x80** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_CONNECT_0x100"></span><span id="winstation_connect_0x100"></span><span id="WINSTATION_CONNECT_0X100"></span>

<span data-ttu-id="51665-157">**WINSTATION \_ Connetti = 0x100** (6)</span><span class="sxs-lookup"><span data-stu-id="51665-157">**WINSTATION\_CONNECT=0x100** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_DISCONNECT_0x200"></span><span id="winstation_disconnect_0x200"></span><span id="WINSTATION_DISCONNECT_0X200"></span>

<span data-ttu-id="51665-158">**WINSTATION \_ Disconnect = 0x200** (7)</span><span class="sxs-lookup"><span data-stu-id="51665-158">**WINSTATION\_DISCONNECT=0x200** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="51665-159">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="51665-159">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51665-160">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="51665-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="51665-161">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="51665-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51665-162">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="51665-162">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="51665-163">Breve descrizione (stringa a una riga) dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="51665-163">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="51665-164">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="51665-164">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="51665-165">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="51665-165">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51665-166">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="51665-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="51665-167">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="51665-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51665-168">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="51665-168">Description of the object.</span></span>

<span data-ttu-id="51665-169">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="51665-169">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="51665-170">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="51665-170">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51665-171">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="51665-171">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="51665-172">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="51665-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51665-173">Qualificatori: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="51665-173">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="51665-174">Data di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="51665-174">The date the object was installed.</span></span> <span data-ttu-id="51665-175">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="51665-175">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="51665-176">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="51665-176">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="51665-177">**Nome**</span><span class="sxs-lookup"><span data-stu-id="51665-177">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51665-178">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="51665-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="51665-179">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="51665-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51665-180">Nome dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="51665-180">The name of the object.</span></span>

<span data-ttu-id="51665-181">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="51665-181">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="51665-182">**PermissionsAllowed**</span><span class="sxs-lookup"><span data-stu-id="51665-182">**PermissionsAllowed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51665-183">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="51665-183">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="51665-184">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="51665-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51665-185">Specifica le [autorizzazioni servizi desktop remoto](terminal-services-permissions.md) consentite per l'account.</span><span class="sxs-lookup"><span data-stu-id="51665-185">Specifies the [Remote Desktop Services Permissions](terminal-services-permissions.md) allowed for the account.</span></span> <span data-ttu-id="51665-186">Il valore di questa proprietà è una maschera di maschera, che può essere impostata su uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="51665-186">The value of this property is a bitmask, which can be set to one or more of the following values.</span></span>

<dt>

<span id="WINSTATION_QUERY_0x1"></span><span id="winstation_query_0x1"></span><span id="WINSTATION_QUERY_0X1"></span>

<span data-ttu-id="51665-187"><span id="WINSTATION_QUERY_0x1"></span><span id="winstation_query_0x1"></span><span id="WINSTATION_QUERY_0X1"></span>**WINSTATION \_ QUERY = 0x1** (1)</span><span class="sxs-lookup"><span data-stu-id="51665-187"><span id="WINSTATION_QUERY_0x1"></span><span id="winstation_query_0x1"></span><span id="WINSTATION_QUERY_0X1"></span>**WINSTATION\_QUERY=0x1** (1)</span></span>


</dt> <dd>

<span data-ttu-id="51665-188">Autorizzazione per eseguire query sulle informazioni relative a una sessione.</span><span class="sxs-lookup"><span data-stu-id="51665-188">Permission to query information about a session.</span></span>

</dd> <dt>

<span id="WINSTATION_SET"></span><span id="winstation_set"></span>

<span data-ttu-id="51665-189"><span id="WINSTATION_SET"></span><span id="winstation_set"></span>**WINSTATION \_ IMPOSTA** (2)</span><span class="sxs-lookup"><span data-stu-id="51665-189"><span id="WINSTATION_SET"></span><span id="winstation_set"></span>**WINSTATION\_SET** (2)</span></span>


</dt> <dd>

<span data-ttu-id="51665-190">Autorizzazione per la modifica dei parametri di connessione.</span><span class="sxs-lookup"><span data-stu-id="51665-190">Permission to modify connection parameters.</span></span>

</dd> <dt>

<span id="WINSTATION_RESET"></span><span id="winstation_reset"></span>

<span data-ttu-id="51665-191"><span id="WINSTATION_RESET"></span><span id="winstation_reset"></span>**WINSTATION \_ Reimposta** (64)</span><span class="sxs-lookup"><span data-stu-id="51665-191"><span id="WINSTATION_RESET"></span><span id="winstation_reset"></span>**WINSTATION\_RESET** (64)</span></span>


</dt> <dd>

<span data-ttu-id="51665-192">Autorizzazione per reimpostare o terminare una sessione o una connessione.</span><span class="sxs-lookup"><span data-stu-id="51665-192">Permission to reset or end a session or connection.</span></span>

</dd> <dt>

<span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED"></span><span id="winstation_virtual___standard_rights_required"></span>

<span data-ttu-id="51665-193"><span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED"></span><span id="winstation_virtual___standard_rights_required"></span>**WINSTATION \_ \| Diritti standard \_ virtuali \_ richiesti** (983048)</span><span class="sxs-lookup"><span data-stu-id="51665-193"><span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED"></span><span id="winstation_virtual___standard_rights_required"></span>**WINSTATION\_VIRTUAL \| STANDARD\_RIGHTS\_REQUIRED** (983048)</span></span>


</dt> <dd>

<span data-ttu-id="51665-194">Autorizzazione per l'utilizzo di canali virtuali.</span><span class="sxs-lookup"><span data-stu-id="51665-194">Permission to use virtual channels.</span></span> <span data-ttu-id="51665-195">I canali virtuali forniscono l'accesso da un programma server ai dispositivi client.</span><span class="sxs-lookup"><span data-stu-id="51665-195">Virtual channels provide access from a server program to client devices.</span></span>

</dd> <dt>

<span id="WINSTATION_SHADOW"></span><span id="winstation_shadow"></span>

<span data-ttu-id="51665-196"><span id="WINSTATION_SHADOW"></span><span id="winstation_shadow"></span>**WINSTATION \_ OMBREGGIAtura** (16)</span><span class="sxs-lookup"><span data-stu-id="51665-196"><span id="WINSTATION_SHADOW"></span><span id="winstation_shadow"></span>**WINSTATION\_SHADOW** (16)</span></span>


</dt> <dd>

<span data-ttu-id="51665-197">Autorizzazione per nascondere o controllare in modalità remota la sessione di un altro utente.</span><span class="sxs-lookup"><span data-stu-id="51665-197">Permission to shadow or remotely control another user's session.</span></span>

</dd> <dt>

<span id="WINSTATION_LOGON"></span><span id="winstation_logon"></span>

<span data-ttu-id="51665-198"><span id="WINSTATION_LOGON"></span><span id="winstation_logon"></span>**WINSTATION \_ ACCESSO** (32)</span><span class="sxs-lookup"><span data-stu-id="51665-198"><span id="WINSTATION_LOGON"></span><span id="winstation_logon"></span>**WINSTATION\_LOGON** (32)</span></span>


</dt> <dd>

<span data-ttu-id="51665-199">Autorizzazione per accedere a una sessione nel server.</span><span class="sxs-lookup"><span data-stu-id="51665-199">Permission to log on to a session on the server.</span></span>

</dd> <dt>

<span id="WINSTATION_LOGOFF"></span><span id="winstation_logoff"></span>

<span data-ttu-id="51665-200"><span id="WINSTATION_LOGOFF"></span><span id="winstation_logoff"></span>**WINSTATION \_ Disconnessione** (4)</span><span class="sxs-lookup"><span data-stu-id="51665-200"><span id="WINSTATION_LOGOFF"></span><span id="winstation_logoff"></span>**WINSTATION\_LOGOFF** (4)</span></span>


</dt> <dd>

<span data-ttu-id="51665-201">Autorizzazione per disconnettere un utente da una sessione.</span><span class="sxs-lookup"><span data-stu-id="51665-201">Permission to log off a user from a session.</span></span>

</dd> <dt>

<span id="WINSTATION_MSG"></span><span id="winstation_msg"></span>

<span data-ttu-id="51665-202"><span id="WINSTATION_MSG"></span><span id="winstation_msg"></span>**WINSTATION \_ MESSAGGIO** (128)</span><span class="sxs-lookup"><span data-stu-id="51665-202"><span id="WINSTATION_MSG"></span><span id="winstation_msg"></span>**WINSTATION\_MSG** (128)</span></span>


</dt> <dd>

<span data-ttu-id="51665-203">Autorizzazione per l'invio di un messaggio alla sessione di un altro utente.</span><span class="sxs-lookup"><span data-stu-id="51665-203">Permission to send a message to another user's session.</span></span>

</dd> <dt>

<span id="WINSTATION_CONNECT"></span><span id="winstation_connect"></span>

<span data-ttu-id="51665-204"><span id="WINSTATION_CONNECT"></span><span id="winstation_connect"></span>**WINSTATION \_ Connetti** (256)</span><span class="sxs-lookup"><span data-stu-id="51665-204"><span id="WINSTATION_CONNECT"></span><span id="winstation_connect"></span>**WINSTATION\_CONNECT** (256)</span></span>


</dt> <dd>

<span data-ttu-id="51665-205">Autorizzazione per la connessione a un'altra sessione.</span><span class="sxs-lookup"><span data-stu-id="51665-205">Permission to connect to another session.</span></span>

</dd> <dt>

<span id="WINSTATION_DISCONNECT"></span><span id="winstation_disconnect"></span>

<span data-ttu-id="51665-206"><span id="WINSTATION_DISCONNECT"></span><span id="winstation_disconnect"></span>**WINSTATION \_ Disconnetti** (512)</span><span class="sxs-lookup"><span data-stu-id="51665-206"><span id="WINSTATION_DISCONNECT"></span><span id="winstation_disconnect"></span>**WINSTATION\_DISCONNECT** (512)</span></span>


</dt> <dd>

<span data-ttu-id="51665-207">Autorizzazione per disconnettere una sessione.</span><span class="sxs-lookup"><span data-stu-id="51665-207">Permission to disconnect a session.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="51665-208">**PermissionsDenied**</span><span class="sxs-lookup"><span data-stu-id="51665-208">**PermissionsDenied**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51665-209">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="51665-209">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="51665-210">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="51665-210">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51665-211">Specifica le autorizzazioni specifiche per il server Host sessione Desktop remoto non consentite per l'account.</span><span class="sxs-lookup"><span data-stu-id="51665-211">Specifies the RD Session Host server-specific permissions disallowed for the account.</span></span> <span data-ttu-id="51665-212">Il valore di questa proprietà è una maschera di maschera, che può essere impostata su uno o più valori della proprietà **PermissionsAllowed** .</span><span class="sxs-lookup"><span data-stu-id="51665-212">The value of this property is a bitmask, which can be set to one or more of the values of the **PermissionsAllowed** property.</span></span>

<dt>

<span id="WINSTATION_QUERY_0x1"></span><span id="winstation_query_0x1"></span><span id="WINSTATION_QUERY_0X1"></span>

<span data-ttu-id="51665-213">**WINSTATION \_ QUERY = 0x1** (0)</span><span class="sxs-lookup"><span data-stu-id="51665-213">**WINSTATION\_QUERY=0x1** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_SET_0x2"></span><span id="winstation_set_0x2"></span><span id="WINSTATION_SET_0X2"></span>

<span data-ttu-id="51665-214">**WINSTATION \_ SET = 0x2** (1)</span><span class="sxs-lookup"><span data-stu-id="51665-214">**WINSTATION\_SET=0x2** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_LOGOFF_0x4"></span><span id="winstation_logoff_0x4"></span><span id="WINSTATION_LOGOFF_0X4"></span>

<span data-ttu-id="51665-215">**WINSTATION \_ Disconnessione = 0x4** (2)</span><span class="sxs-lookup"><span data-stu-id="51665-215">**WINSTATION\_LOGOFF=0x4** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED___0xF008"></span><span id="winstation_virtual___standard_rights_required___0xf008"></span><span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED___0XF008"></span>

<span data-ttu-id="51665-216">**WINSTATION \_ \| Diritti standard \_ virtuali \_ richiesti = 0xF008** (3)</span><span class="sxs-lookup"><span data-stu-id="51665-216">**WINSTATION\_VIRTUAL \| STANDARD\_RIGHTS\_REQUIRED = 0xF008** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_SHADOW_0x10"></span><span id="winstation_shadow_0x10"></span><span id="WINSTATION_SHADOW_0X10"></span>

<span data-ttu-id="51665-217">**WINSTATION \_ SHADOW = 0x10** (4)</span><span class="sxs-lookup"><span data-stu-id="51665-217">**WINSTATION\_SHADOW=0x10** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_LOGON_0x20"></span><span id="winstation_logon_0x20"></span><span id="WINSTATION_LOGON_0X20"></span>

<span data-ttu-id="51665-218">**WINSTATION \_ LOGON = 0x20** (5)</span><span class="sxs-lookup"><span data-stu-id="51665-218">**WINSTATION\_LOGON=0x20** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_MSG_0x80"></span><span id="winstation_msg_0x80"></span><span id="WINSTATION_MSG_0X80"></span>

<span data-ttu-id="51665-219">**WINSTATION \_ MESSAGGIO = 0x80** (6)</span><span class="sxs-lookup"><span data-stu-id="51665-219">**WINSTATION\_MSG=0x80** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_CONNECT_0x100"></span><span id="winstation_connect_0x100"></span><span id="WINSTATION_CONNECT_0X100"></span>

<span data-ttu-id="51665-220">**WINSTATION \_ Connetti = 0x100** (7)</span><span class="sxs-lookup"><span data-stu-id="51665-220">**WINSTATION\_CONNECT=0x100** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_DISCONNECT_0x200"></span><span id="winstation_disconnect_0x200"></span><span id="WINSTATION_DISCONNECT_0X200"></span>

<span data-ttu-id="51665-221">**WINSTATION \_ Disconnect = 0x200** (8)</span><span class="sxs-lookup"><span data-stu-id="51665-221">**WINSTATION\_DISCONNECT=0x200** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="51665-222">**SID**</span><span class="sxs-lookup"><span data-stu-id="51665-222">**SID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51665-223">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="51665-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="51665-224">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="51665-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51665-225">Specifica gli [ID di sicurezza](/windows/desktop/SecAuthZ/security-identifiers) dell'account.</span><span class="sxs-lookup"><span data-stu-id="51665-225">Specifies the [Security Identifiers](/windows/desktop/SecAuthZ/security-identifiers) of the account.</span></span>

</dd> <dt>

<span data-ttu-id="51665-226">**Status**</span><span class="sxs-lookup"><span data-stu-id="51665-226">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51665-227">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="51665-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="51665-228">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="51665-228">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51665-229">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="51665-229">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="51665-230">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="51665-230">Current status of the object.</span></span> <span data-ttu-id="51665-231">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="51665-231">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="51665-232">Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro).</span><span class="sxs-lookup"><span data-stu-id="51665-232">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="51665-233">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="51665-233">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="51665-234">Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="51665-234">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="51665-235">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="51665-235">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="51665-236">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="51665-236">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="51665-237">("OK")</span><span class="sxs-lookup"><span data-stu-id="51665-237">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="51665-238">("Errore")</span><span class="sxs-lookup"><span data-stu-id="51665-238">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="51665-239">("Danneggiato")</span><span class="sxs-lookup"><span data-stu-id="51665-239">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="51665-240">("Sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="51665-240">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="51665-241">("Errore di predazione")</span><span class="sxs-lookup"><span data-stu-id="51665-241">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="51665-242">("Avvio")</span><span class="sxs-lookup"><span data-stu-id="51665-242">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="51665-243">("Arresto")</span><span class="sxs-lookup"><span data-stu-id="51665-243">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="51665-244">("Servizio")</span><span class="sxs-lookup"><span data-stu-id="51665-244">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="51665-245">**Terminale**</span><span class="sxs-lookup"><span data-stu-id="51665-245">**TerminalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51665-246">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="51665-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="51665-247">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="51665-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51665-248">Nome del terminale.</span><span class="sxs-lookup"><span data-stu-id="51665-248">The name of the terminal.</span></span>

<span data-ttu-id="51665-249">Questa proprietà viene ereditata da [**Win32 \_ TerminalSetting**](win32-terminalsetting.md).</span><span class="sxs-lookup"><span data-stu-id="51665-249">This property is inherited from [**Win32\_TerminalSetting**](win32-terminalsetting.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="51665-250">Commenti</span><span class="sxs-lookup"><span data-stu-id="51665-250">Remarks</span></span>

<span data-ttu-id="51665-251">Per connettersi allo \\ \\ \\ spazio dei nomi CIMV2 TerminalServices radice, il livello di autenticazione deve includere la riservatezza dei pacchetti.</span><span class="sxs-lookup"><span data-stu-id="51665-251">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="51665-252">Per le chiamate C/C++, si tratta di un livello di autenticazione del livello di autenticazione **RPC \_ C \_ \_ \_ PKT \_ privacy**.</span><span class="sxs-lookup"><span data-stu-id="51665-252">For C/C++ calls, this would be an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="51665-253">Per Visual Basic e le chiamate di scripting, si tratta di un livello di autenticazione di **WbemAuthenticationLevelPktPrivacy** o "su PktPrivacy", con un valore pari a 6.</span><span class="sxs-lookup"><span data-stu-id="51665-253">For Visual Basic and scripting calls, this would be an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="51665-254">Il seguente esempio di Visual Basic Scripting Edition (VBScript) illustra come connettersi a un computer remoto con la privacy dei pacchetti.</span><span class="sxs-lookup"><span data-stu-id="51665-254">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="51665-255">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="51665-255">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="51665-256">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="51665-256">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="51665-257">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="51665-257">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="51665-258">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="51665-258">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="51665-259">Requisiti</span><span class="sxs-lookup"><span data-stu-id="51665-259">Requirements</span></span>



| <span data-ttu-id="51665-260">Requisito</span><span class="sxs-lookup"><span data-stu-id="51665-260">Requirement</span></span> | <span data-ttu-id="51665-261">Valore</span><span class="sxs-lookup"><span data-stu-id="51665-261">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="51665-262">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="51665-262">Minimum supported client</span></span><br/> | <span data-ttu-id="51665-263">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="51665-263">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="51665-264">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="51665-264">Minimum supported server</span></span><br/> | <span data-ttu-id="51665-265">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="51665-265">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="51665-266">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="51665-266">Namespace</span></span><br/>                | <span data-ttu-id="51665-267">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="51665-267">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="51665-268">MOF</span><span class="sxs-lookup"><span data-stu-id="51665-268">MOF</span></span><br/>                      | <dl> <span data-ttu-id="51665-269"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="51665-269"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="51665-270">DLL</span><span class="sxs-lookup"><span data-stu-id="51665-270">DLL</span></span><br/>                      | <dl> <span data-ttu-id="51665-271"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="51665-271"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51665-272">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="51665-272">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51665-273">**\_TerminalSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="51665-273">**Win32\_TerminalSetting**</span></span>](win32-terminalsetting.md)
</dt> </dl>

 

