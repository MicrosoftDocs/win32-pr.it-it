---
title: Classe Win32_TSSessionSetting
description: Definisce le impostazioni di configurazione per la \_ classe terminale Win32, ad esempio i limiti di tempo e le azioni di disconnessione e riconnessione.
ms.assetid: e115f370-270c-404f-b6c6-7781c1ff376f
ms.tgt_platform: multiple
keywords:
- Classe Win32_TSSessionSetting Servizi Desktop remoto
- Classe Win32_TSSessionSetting Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_TSSessionSetting
- Win32_TSSessionSetting.Caption
- Win32_TSSessionSetting.Description
- Win32_TSSessionSetting.InstallDate
- Win32_TSSessionSetting.Name
- Win32_TSSessionSetting.Status
- Win32_TSSessionSetting.TerminalName
- Win32_TSSessionSetting.ActiveSessionLimit
- Win32_TSSessionSetting.BrokenConnectionAction
- Win32_TSSessionSetting.BrokenConnectionPolicy
- Win32_TSSessionSetting.DisconnectedSessionLimit
- Win32_TSSessionSetting.IdleSessionLimit
- Win32_TSSessionSetting.PolicySourceActiveSessionLimit
- Win32_TSSessionSetting.PolicySourceBrokenConnectionAction
- Win32_TSSessionSetting.PolicySourceDisconnectedSessionLimit
- Win32_TSSessionSetting.PolicySourceIdleSessionLimit
- Win32_TSSessionSetting.PolicySourceReconnectionPolicy
- Win32_TSSessionSetting.ReconnectionPolicy
- Win32_TSSessionSetting.TimeLimitPolicy
- Win32_TSSessionSetting.EnableTimeoutWarning
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e780cdedee0fe447499bed5013dadc2ba9b448b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518976"
---
# <a name="win32_tssessionsetting-class"></a><span data-ttu-id="85132-105">Win32 \_ TSSessionSetting (classe)</span><span class="sxs-lookup"><span data-stu-id="85132-105">Win32\_TSSessionSetting class</span></span>

<span data-ttu-id="85132-106">La classe WMI **Win32 \_ TSSessionSetting** definisce le impostazioni di configurazione per la classe [**\_ terminale Win32**](win32-terminal.md) , ad esempio i limiti di tempo e le azioni di disconnessione e riconnessione.</span><span class="sxs-lookup"><span data-stu-id="85132-106">The **Win32\_TSSessionSetting** WMI class defines configuration settings for the [**Win32\_Terminal**](win32-terminal.md) class such as time-limits, and disconnection and reconnection actions.</span></span>

<span data-ttu-id="85132-107">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà definite ed ereditate, in ordine alfabetico.</span><span class="sxs-lookup"><span data-stu-id="85132-107">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span> <span data-ttu-id="85132-108">Per informazioni di riferimento sui metodi, vedere la tabella dei metodi più avanti in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="85132-108">For reference information on methods, see the table of methods later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="85132-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="85132-109">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TSSESSIONSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSSessionSetting : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  uint32   ActiveSessionLimit;
  uint32   BrokenConnectionAction;
  uint32   BrokenConnectionPolicy;
  uint32   DisconnectedSessionLimit;
  uint32   IdleSessionLimit;
  uint32   PolicySourceActiveSessionLimit;
  uint32   PolicySourceBrokenConnectionAction;
  uint32   PolicySourceDisconnectedSessionLimit;
  uint32   PolicySourceIdleSessionLimit;
  uint32   PolicySourceReconnectionPolicy;
  uint32   ReconnectionPolicy;
  uint32   TimeLimitPolicy;
  uint32   EnableTimeoutWarning;
};
```

## <a name="members"></a><span data-ttu-id="85132-110">Members</span><span class="sxs-lookup"><span data-stu-id="85132-110">Members</span></span>

<span data-ttu-id="85132-111">La classe **Win32 \_ TSSessionSetting** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="85132-111">The **Win32\_TSSessionSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="85132-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="85132-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="85132-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="85132-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="85132-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="85132-114">Methods</span></span>

<span data-ttu-id="85132-115">La classe **Win32 \_ TSSessionSetting** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="85132-115">The **Win32\_TSSessionSetting** class has these methods.</span></span>



| <span data-ttu-id="85132-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="85132-116">Method</span></span>                                                              | <span data-ttu-id="85132-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="85132-117">Description</span></span>                                                              |
|:--------------------------------------------------------------------|:-------------------------------------------------------------------------|
| [<span data-ttu-id="85132-118">**BrokenConnection**</span><span class="sxs-lookup"><span data-stu-id="85132-118">**BrokenConnection**</span></span>](win32-tssessionsetting-brokenconnection.md) | <span data-ttu-id="85132-119">Imposta le proprietà di connessione interrotte incluse in questa classe.</span><span class="sxs-lookup"><span data-stu-id="85132-119">Sets the broken connection properties included in this class.</span></span><br/> |
| [<span data-ttu-id="85132-120">**Limite**</span><span class="sxs-lookup"><span data-stu-id="85132-120">**TimeLimit**</span></span>](win32-tssessionsetting-timelimit.md)               | <span data-ttu-id="85132-121">Imposta le proprietà del limite di tempo incluse in questa classe.</span><span class="sxs-lookup"><span data-stu-id="85132-121">Sets the time-limit properties included in this class.</span></span><br/>        |



 

### <a name="properties"></a><span data-ttu-id="85132-122">Proprietà</span><span class="sxs-lookup"><span data-stu-id="85132-122">Properties</span></span>

<span data-ttu-id="85132-123">La classe **Win32 \_ TSSessionSetting** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="85132-123">The **Win32\_TSSessionSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="85132-124">**ActiveSessionLimit**</span><span class="sxs-lookup"><span data-stu-id="85132-124">**ActiveSessionLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85132-125">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="85132-125">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="85132-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="85132-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85132-127">Quantità massima di tempo, in millisecondi, allocata a una sessione attiva.</span><span class="sxs-lookup"><span data-stu-id="85132-127">The maximum amount of time, in milliseconds, allocated to an active session.</span></span> <span data-ttu-id="85132-128">Il valore 0 specifica un periodo di tempo infinito.</span><span class="sxs-lookup"><span data-stu-id="85132-128">A value of 0 specifies an infinite amount of time.</span></span>

</dd> <dt>

<span data-ttu-id="85132-129">**BrokenConnectionAction**</span><span class="sxs-lookup"><span data-stu-id="85132-129">**BrokenConnectionAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85132-130">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="85132-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="85132-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="85132-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85132-132">Azione eseguita dal server in caso di interruzione di una connessione a causa della perdita di rete o del superamento dei limiti di tempo.</span><span class="sxs-lookup"><span data-stu-id="85132-132">The action the server takes on the session when a connection has been broken due to network loss or exceeded time-limits.</span></span>

<dt>

<span id="Disconnect"></span><span id="disconnect"></span><span id="DISCONNECT"></span>

<span data-ttu-id="85132-133"><span id="Disconnect"></span><span id="disconnect"></span><span id="DISCONNECT"></span>**Disconnetti** (0)</span><span class="sxs-lookup"><span data-stu-id="85132-133"><span id="Disconnect"></span><span id="disconnect"></span><span id="DISCONNECT"></span>**Disconnect** (0)</span></span>


</dt> <dd>

<span data-ttu-id="85132-134">L'utente è disconnesso dalla sessione.</span><span class="sxs-lookup"><span data-stu-id="85132-134">The user is disconnected from the session.</span></span>

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span data-ttu-id="85132-135"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Termina** (1)</span><span class="sxs-lookup"><span data-stu-id="85132-135"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminate** (1)</span></span>


</dt> <dd>

<span data-ttu-id="85132-136">La sessione viene eliminata definitivamente dal server.</span><span class="sxs-lookup"><span data-stu-id="85132-136">The session is permanently deleted from the server.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="85132-137">**BrokenConnectionPolicy**</span><span class="sxs-lookup"><span data-stu-id="85132-137">**BrokenConnectionPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85132-138">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="85132-138">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="85132-139">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="85132-139">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="85132-140">Il criterio utilizzato dal server per determinare quando interrompere una connessione a causa di una perdita di rete o di limiti di tempo superati.</span><span class="sxs-lookup"><span data-stu-id="85132-140">The policy the server uses to determine when to break a connection because of network loss or exceeded time-limits.</span></span>

<dt>

<span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>

<span data-ttu-id="85132-141"><span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>**Server-override** (1)</span><span class="sxs-lookup"><span data-stu-id="85132-141"><span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>**Server-Override** (1)</span></span>


</dt> <dd>

<span data-ttu-id="85132-142">Le impostazioni dei criteri di disconnessione dell'utente vengono sostituite dal server.</span><span class="sxs-lookup"><span data-stu-id="85132-142">The user's disconnection policy settings are overridden by the server.</span></span>

</dd> <dt>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>

<span data-ttu-id="85132-143"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Per utente** (0)</span><span class="sxs-lookup"><span data-stu-id="85132-143"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Per User** (0)</span></span>


</dt> <dd>

<span data-ttu-id="85132-144">Le impostazioni dei criteri di disconnessione dell'utente sono attive.</span><span class="sxs-lookup"><span data-stu-id="85132-144">The user's disconnection policy settings are in effect.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="85132-145">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="85132-145">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85132-146">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="85132-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85132-147">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="85132-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85132-148">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="85132-148">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="85132-149">Breve descrizione (stringa a una riga) dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="85132-149">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="85132-150">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="85132-150">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="85132-151">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="85132-151">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85132-152">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="85132-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85132-153">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="85132-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85132-154">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="85132-154">Description of the object.</span></span>

<span data-ttu-id="85132-155">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="85132-155">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="85132-156">**DisconnectedSessionLimit**</span><span class="sxs-lookup"><span data-stu-id="85132-156">**DisconnectedSessionLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85132-157">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="85132-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="85132-158">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="85132-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85132-159">Intervallo di tempo, in millisecondi, dopo il quale una sessione disconnessa viene terminata.</span><span class="sxs-lookup"><span data-stu-id="85132-159">The time interval, in milliseconds, after which a disconnected session is terminated.</span></span> <span data-ttu-id="85132-160">Il valore 0 specifica un periodo di tempo infinito.</span><span class="sxs-lookup"><span data-stu-id="85132-160">A value of 0 specifies an infinite amount of time.</span></span>

</dd> <dt>

<span data-ttu-id="85132-161">**EnableTimeoutWarning**</span><span class="sxs-lookup"><span data-stu-id="85132-161">**EnableTimeoutWarning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85132-162">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="85132-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="85132-163">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="85132-163">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="85132-164">Consente di abilitare l'avviso di timeout.</span><span class="sxs-lookup"><span data-stu-id="85132-164">Enables the timeout warning.</span></span>

<span data-ttu-id="85132-165">**Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:** Questa proprietà non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="85132-165">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="85132-166">**IdleSessionLimit**</span><span class="sxs-lookup"><span data-stu-id="85132-166">**IdleSessionLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85132-167">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="85132-167">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="85132-168">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="85132-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85132-169">Intervallo di tempo, in millisecondi, dopo il quale una sessione inattiva viene terminata.</span><span class="sxs-lookup"><span data-stu-id="85132-169">The time interval, in milliseconds, after which an idle session is terminated.</span></span> <span data-ttu-id="85132-170">Il valore 0 specifica un periodo di tempo infinito.</span><span class="sxs-lookup"><span data-stu-id="85132-170">A value of 0 specifies an infinite amount of time.</span></span>

</dd> <dt>

<span data-ttu-id="85132-171">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="85132-171">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85132-172">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="85132-172">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="85132-173">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="85132-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85132-174">Qualificatori: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="85132-174">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="85132-175">Data di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="85132-175">The date the object was installed.</span></span> <span data-ttu-id="85132-176">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="85132-176">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="85132-177">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="85132-177">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="85132-178">**Nome**</span><span class="sxs-lookup"><span data-stu-id="85132-178">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85132-179">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="85132-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85132-180">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="85132-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85132-181">Nome dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="85132-181">The name of the object.</span></span>

<span data-ttu-id="85132-182">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="85132-182">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="85132-183">**PolicySourceActiveSessionLimit**</span><span class="sxs-lookup"><span data-stu-id="85132-183">**PolicySourceActiveSessionLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85132-184">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="85132-184">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="85132-185">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="85132-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85132-186">Indica se la proprietà **ActiveSessionLimit** è configurata dal server, da criteri di gruppo o per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="85132-186">Indicates whether the **ActiveSessionLimit** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="85132-187">0</span><span class="sxs-lookup"><span data-stu-id="85132-187">0</span></span>
</dt> <dd>

<span data-ttu-id="85132-188">Server</span><span class="sxs-lookup"><span data-stu-id="85132-188">Server</span></span>

</dd> <dt>

<span data-ttu-id="85132-189">1</span><span class="sxs-lookup"><span data-stu-id="85132-189">1</span></span>
</dt> <dd>

<span data-ttu-id="85132-190">Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="85132-190">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="85132-191">2</span><span class="sxs-lookup"><span data-stu-id="85132-191">2</span></span>
</dt> <dd>

<span data-ttu-id="85132-192">Predefinito</span><span class="sxs-lookup"><span data-stu-id="85132-192">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="85132-193">**PolicySourceBrokenConnectionAction**</span><span class="sxs-lookup"><span data-stu-id="85132-193">**PolicySourceBrokenConnectionAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85132-194">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="85132-194">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="85132-195">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="85132-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85132-196">Indica se la proprietà **BrokenConnectionAction** è configurata dal server, da criteri di gruppo o per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="85132-196">Indicates whether the **BrokenConnectionAction** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="85132-197">0</span><span class="sxs-lookup"><span data-stu-id="85132-197">0</span></span>
</dt> <dd>

<span data-ttu-id="85132-198">Server</span><span class="sxs-lookup"><span data-stu-id="85132-198">Server</span></span>

</dd> <dt>

<span data-ttu-id="85132-199">1</span><span class="sxs-lookup"><span data-stu-id="85132-199">1</span></span>
</dt> <dd>

<span data-ttu-id="85132-200">Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="85132-200">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="85132-201">2</span><span class="sxs-lookup"><span data-stu-id="85132-201">2</span></span>
</dt> <dd>

<span data-ttu-id="85132-202">Predefinito</span><span class="sxs-lookup"><span data-stu-id="85132-202">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="85132-203">**PolicySourceDisconnectedSessionLimit**</span><span class="sxs-lookup"><span data-stu-id="85132-203">**PolicySourceDisconnectedSessionLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85132-204">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="85132-204">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="85132-205">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="85132-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85132-206">Indica se la proprietà **DisconnectedSessionLimit** è configurata dal server, da criteri di gruppo o per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="85132-206">Indicates whether the **DisconnectedSessionLimit** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="85132-207">0</span><span class="sxs-lookup"><span data-stu-id="85132-207">0</span></span>
</dt> <dd>

<span data-ttu-id="85132-208">Server</span><span class="sxs-lookup"><span data-stu-id="85132-208">Server</span></span>

</dd> <dt>

<span data-ttu-id="85132-209">1</span><span class="sxs-lookup"><span data-stu-id="85132-209">1</span></span>
</dt> <dd>

<span data-ttu-id="85132-210">Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="85132-210">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="85132-211">2</span><span class="sxs-lookup"><span data-stu-id="85132-211">2</span></span>
</dt> <dd>

<span data-ttu-id="85132-212">Predefinito</span><span class="sxs-lookup"><span data-stu-id="85132-212">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="85132-213">**PolicySourceIdleSessionLimit**</span><span class="sxs-lookup"><span data-stu-id="85132-213">**PolicySourceIdleSessionLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85132-214">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="85132-214">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="85132-215">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="85132-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85132-216">Indica se la proprietà **IdleSessionLimit** è configurata dal server, da criteri di gruppo o per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="85132-216">Indicates whether the **IdleSessionLimit** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="85132-217">0</span><span class="sxs-lookup"><span data-stu-id="85132-217">0</span></span>
</dt> <dd>

<span data-ttu-id="85132-218">Server</span><span class="sxs-lookup"><span data-stu-id="85132-218">Server</span></span>

</dd> <dt>

<span data-ttu-id="85132-219">1</span><span class="sxs-lookup"><span data-stu-id="85132-219">1</span></span>
</dt> <dd>

<span data-ttu-id="85132-220">Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="85132-220">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="85132-221">2</span><span class="sxs-lookup"><span data-stu-id="85132-221">2</span></span>
</dt> <dd>

<span data-ttu-id="85132-222">Predefinito</span><span class="sxs-lookup"><span data-stu-id="85132-222">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="85132-223">**PolicySourceReconnectionPolicy**</span><span class="sxs-lookup"><span data-stu-id="85132-223">**PolicySourceReconnectionPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85132-224">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="85132-224">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="85132-225">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="85132-225">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85132-226">Indica se la proprietà **ReconnectPolicy** è configurata dal server, da criteri di gruppo o per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="85132-226">Indicates whether the **ReconnectPolicy** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="85132-227">0</span><span class="sxs-lookup"><span data-stu-id="85132-227">0</span></span>
</dt> <dd>

<span data-ttu-id="85132-228">Server</span><span class="sxs-lookup"><span data-stu-id="85132-228">Server</span></span>

</dd> <dt>

<span data-ttu-id="85132-229">1</span><span class="sxs-lookup"><span data-stu-id="85132-229">1</span></span>
</dt> <dd>

<span data-ttu-id="85132-230">Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="85132-230">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="85132-231">2</span><span class="sxs-lookup"><span data-stu-id="85132-231">2</span></span>
</dt> <dd>

<span data-ttu-id="85132-232">Predefinito</span><span class="sxs-lookup"><span data-stu-id="85132-232">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="85132-233">**ReconnectionPolicy**</span><span class="sxs-lookup"><span data-stu-id="85132-233">**ReconnectionPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85132-234">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="85132-234">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="85132-235">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="85132-235">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="85132-236">Specifica se un utente deve utilizzare il client precedente per riconnettersi a una sessione disconnessa.</span><span class="sxs-lookup"><span data-stu-id="85132-236">Specifies whether a user must use the previous client to reconnect to a disconnected session.</span></span>

<dt>

<span id="Any_Client"></span><span id="any_client"></span><span id="ANY_CLIENT"></span>

<span data-ttu-id="85132-237"><span id="Any_Client"></span><span id="any_client"></span><span id="ANY_CLIENT"></span>**Qualsiasi client** (0)</span><span class="sxs-lookup"><span data-stu-id="85132-237"><span id="Any_Client"></span><span id="any_client"></span><span id="ANY_CLIENT"></span>**Any Client** (0)</span></span>


</dt> <dd>

<span data-ttu-id="85132-238">Qualsiasi client verrà usato per la riconnessione.</span><span class="sxs-lookup"><span data-stu-id="85132-238">Any client will be used to reconnect.</span></span>

</dd> <dt>

<span id="Previous_Client"></span><span id="previous_client"></span><span id="PREVIOUS_CLIENT"></span>

<span data-ttu-id="85132-239"><span id="Previous_Client"></span><span id="previous_client"></span><span id="PREVIOUS_CLIENT"></span>**Client precedente** (1)</span><span class="sxs-lookup"><span data-stu-id="85132-239"><span id="Previous_Client"></span><span id="previous_client"></span><span id="PREVIOUS_CLIENT"></span>**Previous Client** (1)</span></span>


</dt> <dd>

<span data-ttu-id="85132-240">Il client precedente utilizzato in una connessione verrà utilizzato per la riconnessione.</span><span class="sxs-lookup"><span data-stu-id="85132-240">The previous client used in a connection will be used to reconnect.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="85132-241">**Status**</span><span class="sxs-lookup"><span data-stu-id="85132-241">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85132-242">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="85132-242">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85132-243">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="85132-243">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85132-244">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="85132-244">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="85132-245">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="85132-245">Current status of the object.</span></span> <span data-ttu-id="85132-246">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="85132-246">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="85132-247">Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro).</span><span class="sxs-lookup"><span data-stu-id="85132-247">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="85132-248">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="85132-248">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="85132-249">Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="85132-249">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="85132-250">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="85132-250">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="85132-251">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="85132-251">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="85132-252">("OK")</span><span class="sxs-lookup"><span data-stu-id="85132-252">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="85132-253">("Errore")</span><span class="sxs-lookup"><span data-stu-id="85132-253">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="85132-254">("Danneggiato")</span><span class="sxs-lookup"><span data-stu-id="85132-254">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="85132-255">("Sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="85132-255">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="85132-256">("Errore di predazione")</span><span class="sxs-lookup"><span data-stu-id="85132-256">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="85132-257">("Avvio")</span><span class="sxs-lookup"><span data-stu-id="85132-257">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="85132-258">("Arresto")</span><span class="sxs-lookup"><span data-stu-id="85132-258">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="85132-259">("Servizio")</span><span class="sxs-lookup"><span data-stu-id="85132-259">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="85132-260">**Terminale**</span><span class="sxs-lookup"><span data-stu-id="85132-260">**TerminalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85132-261">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="85132-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85132-262">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="85132-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85132-263">Nome del terminale.</span><span class="sxs-lookup"><span data-stu-id="85132-263">The name of the terminal.</span></span>

<span data-ttu-id="85132-264">Questa proprietà viene ereditata da [**Win32 \_ TerminalSetting**](win32-terminalsetting.md).</span><span class="sxs-lookup"><span data-stu-id="85132-264">This property is inherited from [**Win32\_TerminalSetting**](win32-terminalsetting.md).</span></span>

</dd> <dt>

<span data-ttu-id="85132-265">**TimeLimitPolicy**</span><span class="sxs-lookup"><span data-stu-id="85132-265">**TimeLimitPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85132-266">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="85132-266">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="85132-267">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="85132-267">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="85132-268">Il criterio utilizzato dal server per determinare i limiti di tempo per le sessioni utente.</span><span class="sxs-lookup"><span data-stu-id="85132-268">The policy the server uses to determine time-limits for user sessions.</span></span>

<dt>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>

<span data-ttu-id="85132-269"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Per utente** (0)</span><span class="sxs-lookup"><span data-stu-id="85132-269"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Per User** (0)</span></span>


</dt> <dd>

<span data-ttu-id="85132-270">Sono attive le impostazioni dei criteri per i limiti di tempo dell'utente.</span><span class="sxs-lookup"><span data-stu-id="85132-270">The user's time-limits policy settings are in effect.</span></span>

</dd> <dt>

<span id="Server_Override"></span><span id="server_override"></span><span id="SERVER_OVERRIDE"></span>

<span data-ttu-id="85132-271"><span id="Server_Override"></span><span id="server_override"></span><span id="SERVER_OVERRIDE"></span>**Sostituzione server** (1)</span><span class="sxs-lookup"><span data-stu-id="85132-271"><span id="Server_Override"></span><span id="server_override"></span><span id="SERVER_OVERRIDE"></span>**Server Override** (1)</span></span>


</dt> <dd>

<span data-ttu-id="85132-272">Le impostazioni dei criteri per i limiti di tempo dell'utente vengono sostituite dal server.</span><span class="sxs-lookup"><span data-stu-id="85132-272">The user's time-limits policy settings are overridden by the server.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="85132-273">Commenti</span><span class="sxs-lookup"><span data-stu-id="85132-273">Remarks</span></span>

<span data-ttu-id="85132-274">Tenere presente che WinStations associato alla sessione della console non può accedere ai metodi e alle proprietà di questa classe.</span><span class="sxs-lookup"><span data-stu-id="85132-274">Be aware that Winstations associated with the console session cannot access the methods and properties of this class.</span></span> <span data-ttu-id="85132-275">Se viene effettuato un tentativo di eseguire questa operazione specificando "console" come valore della proprietà TerminalName, i metodi di questo oggetto restituiranno **WBEM \_ E \_ non \_ supportati**.</span><span class="sxs-lookup"><span data-stu-id="85132-275">If an attempt is made to do so by specifying "Console" as the value of the TerminalName property, methods of this object will return **WBEM\_E\_NOT\_SUPPORTED**.</span></span> <span data-ttu-id="85132-276">Questo codice di errore viene restituito anche se una stazione della finestra tenta di chiamare i metodi di questo oggetto allo scopo di aggiungere o modificare le proprietà di sicurezza degli account LocalSystem, LocalService o NetworkService.</span><span class="sxs-lookup"><span data-stu-id="85132-276">This error code will also be returned if a window station attempts to call methods of this object for the purpose of adding or modifying the security properties of the LocalSystem, LocalService, or NetworkService accounts.</span></span>

<span data-ttu-id="85132-277">Per connettersi allo \\ \\ spazio dei nomi "root cimv2 TerminalServices", il livello di autenticazione deve includere la riservatezza dei pacchetti.</span><span class="sxs-lookup"><span data-stu-id="85132-277">To connect to the "root\\CIMV2\\TerminalServices" namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="85132-278">Per le chiamate C/C++, si tratta di un livello di autenticazione del livello di autenticazione **RPC \_ C \_ \_ \_ PKT \_ privacy**.</span><span class="sxs-lookup"><span data-stu-id="85132-278">For C/C++ calls, this would be an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="85132-279">Per Visual Basic e le chiamate di scripting, si tratta di un livello di autenticazione di **WbemAuthenticationLevelPktPrivacy** o "su PktPrivacy", con un valore pari a 6.</span><span class="sxs-lookup"><span data-stu-id="85132-279">For Visual Basic and scripting calls, this would be an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="85132-280">Il seguente esempio di Visual Basic Scripting Edition (VBScript) illustra come connettersi a un computer remoto con la privacy dei pacchetti.</span><span class="sxs-lookup"><span data-stu-id="85132-280">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="85132-281">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="85132-281">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="85132-282">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="85132-282">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="85132-283">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="85132-283">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="85132-284">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="85132-284">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="85132-285">Requisiti</span><span class="sxs-lookup"><span data-stu-id="85132-285">Requirements</span></span>



| <span data-ttu-id="85132-286">Requisito</span><span class="sxs-lookup"><span data-stu-id="85132-286">Requirement</span></span> | <span data-ttu-id="85132-287">Valore</span><span class="sxs-lookup"><span data-stu-id="85132-287">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="85132-288">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="85132-288">Minimum supported client</span></span><br/> | <span data-ttu-id="85132-289">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="85132-289">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="85132-290">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="85132-290">Minimum supported server</span></span><br/> | <span data-ttu-id="85132-291">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="85132-291">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="85132-292">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="85132-292">Namespace</span></span><br/>                | <span data-ttu-id="85132-293">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="85132-293">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="85132-294">MOF</span><span class="sxs-lookup"><span data-stu-id="85132-294">MOF</span></span><br/>                      | <dl> <span data-ttu-id="85132-295"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="85132-295"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="85132-296">DLL</span><span class="sxs-lookup"><span data-stu-id="85132-296">DLL</span></span><br/>                      | <dl> <span data-ttu-id="85132-297"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="85132-297"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85132-298">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="85132-298">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85132-299">**\_TerminalSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="85132-299">**Win32\_TerminalSetting**</span></span>](win32-terminalsetting.md)
</dt> <dt>

[<span data-ttu-id="85132-300">**\_Impostazione CIM**</span><span class="sxs-lookup"><span data-stu-id="85132-300">**CIM\_Setting**</span></span>](/windows/desktop/CIMWin32Prov/cim-setting)
</dt> </dl>

 

