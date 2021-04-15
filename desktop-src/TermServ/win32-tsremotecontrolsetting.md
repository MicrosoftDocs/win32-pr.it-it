---
title: Classe Win32_TSRemoteControlSetting
description: Definisce le impostazioni di configurazione del controllo remoto per la \_ classe terminale Win32.
ms.assetid: 2e23915e-ee1c-4e53-8d0d-4d3fc2fefce6
ms.tgt_platform: multiple
keywords:
- Classe Win32_TSRemoteControlSetting Servizi Desktop remoto
- Classe Win32_TSRemoteControlSetting Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_TSRemoteControlSetting
- Win32_TSRemoteControlSetting.Caption
- Win32_TSRemoteControlSetting.Description
- Win32_TSRemoteControlSetting.InstallDate
- Win32_TSRemoteControlSetting.Name
- Win32_TSRemoteControlSetting.Status
- Win32_TSRemoteControlSetting.TerminalName
- Win32_TSRemoteControlSetting.LevelOfControl
- Win32_TSRemoteControlSetting.PolicySourceLevelOfControl
- Win32_TSRemoteControlSetting.RemoteControlPolicy
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96e327744ad864e14e1f2580b3b71116e448f36e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477074"
---
# <a name="win32_tsremotecontrolsetting-class"></a><span data-ttu-id="56522-105">Win32 \_ TSRemoteControlSetting (classe)</span><span class="sxs-lookup"><span data-stu-id="56522-105">Win32\_TSRemoteControlSetting class</span></span>

<span data-ttu-id="56522-106">La classe WMI **Win32 \_ TSRemoteControlSetting** definisce le impostazioni di configurazione del controllo remoto per la classe [**\_ terminale Win32**](win32-terminal.md) .</span><span class="sxs-lookup"><span data-stu-id="56522-106">The **Win32\_TSRemoteControlSetting** WMI class defines the remote control configuration settings for the [**Win32\_Terminal**](win32-terminal.md) class.</span></span>

<span data-ttu-id="56522-107">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà definite ed ereditate, in ordine alfabetico.</span><span class="sxs-lookup"><span data-stu-id="56522-107">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span> <span data-ttu-id="56522-108">Per informazioni di riferimento sui metodi, vedere la tabella dei metodi più avanti in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="56522-108">For reference information on methods, see the table of methods later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="56522-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="56522-109">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TSREMOTECONTROLSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSRemoteControlSetting : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  uint32   LevelOfControl;
  uint32   PolicySourceLevelOfControl;
  uint32   RemoteControlPolicy;
};
```

## <a name="members"></a><span data-ttu-id="56522-110">Members</span><span class="sxs-lookup"><span data-stu-id="56522-110">Members</span></span>

<span data-ttu-id="56522-111">La classe **Win32 \_ TSRemoteControlSetting** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="56522-111">The **Win32\_TSRemoteControlSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="56522-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="56522-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="56522-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="56522-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="56522-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="56522-114">Methods</span></span>

<span data-ttu-id="56522-115">La classe **Win32 \_ TSRemoteControlSetting** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="56522-115">The **Win32\_TSRemoteControlSetting** class has these methods.</span></span>



| <span data-ttu-id="56522-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="56522-116">Method</span></span>                                                              | <span data-ttu-id="56522-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="56522-117">Description</span></span>                                                    |
|:--------------------------------------------------------------------|:---------------------------------------------------------------|
| [<span data-ttu-id="56522-118">**RemoteControl**</span><span class="sxs-lookup"><span data-stu-id="56522-118">**RemoteControl**</span></span>](win32-tsremotecontrolsetting-remotecontrol.md) | <span data-ttu-id="56522-119">Imposta la proprietà **LevelOfControl** di questa classe.</span><span class="sxs-lookup"><span data-stu-id="56522-119">Sets the **LevelOfControl** property of this class.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="56522-120">Proprietà</span><span class="sxs-lookup"><span data-stu-id="56522-120">Properties</span></span>

<span data-ttu-id="56522-121">La classe **Win32 \_ TSRemoteControlSetting** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="56522-121">The **Win32\_TSRemoteControlSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="56522-122">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="56522-122">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56522-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="56522-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56522-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="56522-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="56522-125">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="56522-125">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="56522-126">Breve descrizione (stringa a una riga) dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="56522-126">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="56522-127">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="56522-127">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="56522-128">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="56522-128">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56522-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="56522-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56522-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="56522-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56522-131">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="56522-131">Description of the object.</span></span>

<span data-ttu-id="56522-132">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="56522-132">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="56522-133">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="56522-133">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56522-134">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="56522-134">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="56522-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="56522-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="56522-136">Qualificatori: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="56522-136">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="56522-137">Data di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="56522-137">The date the object was installed.</span></span> <span data-ttu-id="56522-138">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="56522-138">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="56522-139">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="56522-139">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="56522-140">**LevelOfControl**</span><span class="sxs-lookup"><span data-stu-id="56522-140">**LevelOfControl**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56522-141">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="56522-141">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="56522-142">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="56522-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56522-143">Livello di controllo per la sessione, che specifica se la sessione verrà visualizzata solo dall'utente remoto oppure visualizzata e controllata tramite una tastiera e un mouse.</span><span class="sxs-lookup"><span data-stu-id="56522-143">Level of control for the session, which specifies whether the session will only be viewed by the remote user, or viewed and controlled through a keyboard and mouse.</span></span> <span data-ttu-id="56522-144">Per ulteriori informazioni, vedere la sezione Osservazioni del metodo [**RemoteControl**](win32-tsremotecontrolsetting-remotecontrol.md) .</span><span class="sxs-lookup"><span data-stu-id="56522-144">For more information, see the Remarks section of the [**RemoteControl**](win32-tsremotecontrolsetting-remotecontrol.md) method.</span></span> <span data-ttu-id="56522-145">Sono supportati i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="56522-145">The following values are supported.</span></span>

<dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span data-ttu-id="56522-146"><span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**Disabilita** (0)</span><span class="sxs-lookup"><span data-stu-id="56522-146"><span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**Disable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="56522-147">Il controllo remoto è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="56522-147">Remote control is disabled.</span></span>

</dd> <dt>

<span id="EnableInputNotify"></span><span id="enableinputnotify"></span><span id="ENABLEINPUTNOTIFY"></span>

<span data-ttu-id="56522-148"><span id="EnableInputNotify"></span><span id="enableinputnotify"></span><span id="ENABLEINPUTNOTIFY"></span>**EnableInputNotify** (1)</span><span class="sxs-lookup"><span data-stu-id="56522-148"><span id="EnableInputNotify"></span><span id="enableinputnotify"></span><span id="ENABLEINPUTNOTIFY"></span>**EnableInputNotify** (1)</span></span>


</dt> <dd>

<span data-ttu-id="56522-149">L'utente del controllo remoto dispone del controllo completo della sessione dell'utente, con l'autorizzazione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="56522-149">The user of remote control has full control of the user's session, with the user's permission.</span></span>

</dd> <dt>

<span id="EnableInputNoNotify"></span><span id="enableinputnonotify"></span><span id="ENABLEINPUTNONOTIFY"></span>

<span data-ttu-id="56522-150"><span id="EnableInputNoNotify"></span><span id="enableinputnonotify"></span><span id="ENABLEINPUTNONOTIFY"></span>**EnableInputNoNotify** (2)</span><span class="sxs-lookup"><span data-stu-id="56522-150"><span id="EnableInputNoNotify"></span><span id="enableinputnonotify"></span><span id="ENABLEINPUTNONOTIFY"></span>**EnableInputNoNotify** (2)</span></span>


</dt> <dd>

<span data-ttu-id="56522-151">L'utente del controllo remoto ha il controllo completo della sessione dell'utente. l'autorizzazione dell'utente non è obbligatoria.</span><span class="sxs-lookup"><span data-stu-id="56522-151">The user of remote control has full control of the user's session; the user's permission is not required.</span></span>

</dd> <dt>

<span id="EnableNoInputNotify"></span><span id="enablenoinputnotify"></span><span id="ENABLENOINPUTNOTIFY"></span>

<span data-ttu-id="56522-152"><span id="EnableNoInputNotify"></span><span id="enablenoinputnotify"></span><span id="ENABLENOINPUTNOTIFY"></span>**EnableNoInputNotify** (3)</span><span class="sxs-lookup"><span data-stu-id="56522-152"><span id="EnableNoInputNotify"></span><span id="enablenoinputnotify"></span><span id="ENABLENOINPUTNOTIFY"></span>**EnableNoInputNotify** (3)</span></span>


</dt> <dd>

<span data-ttu-id="56522-153">L'utente del controllo remoto può visualizzare la sessione in modalità remota con l'autorizzazione dell'utente. l'utente remoto non è in grado di controllare attivamente la sessione.</span><span class="sxs-lookup"><span data-stu-id="56522-153">The user of remote control can view the session remotely, with the user's permission; the remote user cannot actively control the session.</span></span>

</dd> <dt>

<span id="EnableNoInputNoNotify"></span><span id="enablenoinputnonotify"></span><span id="ENABLENOINPUTNONOTIFY"></span>

<span data-ttu-id="56522-154"><span id="EnableNoInputNoNotify"></span><span id="enablenoinputnonotify"></span><span id="ENABLENOINPUTNONOTIFY"></span>**EnableNoInputNoNotify** (4)</span><span class="sxs-lookup"><span data-stu-id="56522-154"><span id="EnableNoInputNoNotify"></span><span id="enablenoinputnonotify"></span><span id="ENABLENOINPUTNONOTIFY"></span>**EnableNoInputNoNotify** (4)</span></span>


</dt> <dd>

<span data-ttu-id="56522-155">L'utente del controllo remoto può visualizzare la sessione in modalità remota, ma non controlla attivamente la sessione. l'autorizzazione dell'utente non è obbligatoria.</span><span class="sxs-lookup"><span data-stu-id="56522-155">The user of remote control can view the session remotely, but not actively control the session; the user's permission is not required.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="56522-156">**Nome**</span><span class="sxs-lookup"><span data-stu-id="56522-156">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56522-157">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="56522-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56522-158">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="56522-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56522-159">Nome dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="56522-159">The name of the object.</span></span>

<span data-ttu-id="56522-160">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="56522-160">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="56522-161">**PolicySourceLevelOfControl**</span><span class="sxs-lookup"><span data-stu-id="56522-161">**PolicySourceLevelOfControl**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56522-162">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="56522-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="56522-163">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="56522-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56522-164">Indica se la proprietà **LevelOfControl** è configurata dal server, da criteri di gruppo o per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="56522-164">Indicates whether the **LevelOfControl** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="56522-165">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="56522-165">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="56522-166">Server</span><span class="sxs-lookup"><span data-stu-id="56522-166">Server</span></span>

</dd> <dt>

<span data-ttu-id="56522-167">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="56522-167">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="56522-168">Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="56522-168">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="56522-169">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="56522-169">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="56522-170">Predefinito</span><span class="sxs-lookup"><span data-stu-id="56522-170">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="56522-171">**RemoteControlPolicy**</span><span class="sxs-lookup"><span data-stu-id="56522-171">**RemoteControlPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56522-172">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="56522-172">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="56522-173">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="56522-173">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="56522-174">Il criterio utilizzato dal server per recuperare le impostazioni di controllo remoto.</span><span class="sxs-lookup"><span data-stu-id="56522-174">The policy the server uses to retrieve the remote control settings.</span></span>

<dt>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>

<span data-ttu-id="56522-175"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Per utente** (0)</span><span class="sxs-lookup"><span data-stu-id="56522-175"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Per User** (0)</span></span>


</dt> <dd>

<span data-ttu-id="56522-176">Le impostazioni di controllo remoto dell'utente sono attive.</span><span class="sxs-lookup"><span data-stu-id="56522-176">The user's remote control settings are in effect.</span></span>

</dd> <dt>

<span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>

<span data-ttu-id="56522-177"><span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>**Server-override** (1)</span><span class="sxs-lookup"><span data-stu-id="56522-177"><span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>**Server-Override** (1)</span></span>


</dt> <dd>

<span data-ttu-id="56522-178">Le impostazioni di controllo remoto dell'utente vengono sostituite dal server.</span><span class="sxs-lookup"><span data-stu-id="56522-178">The user's remote control settings are overridden by the server.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="56522-179">**Status**</span><span class="sxs-lookup"><span data-stu-id="56522-179">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56522-180">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="56522-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56522-181">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="56522-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="56522-182">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="56522-182">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="56522-183">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="56522-183">Current status of the object.</span></span> <span data-ttu-id="56522-184">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="56522-184">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="56522-185">Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro).</span><span class="sxs-lookup"><span data-stu-id="56522-185">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="56522-186">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="56522-186">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="56522-187">Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="56522-187">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="56522-188">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="56522-188">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="56522-189">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="56522-189">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="56522-190">("OK")</span><span class="sxs-lookup"><span data-stu-id="56522-190">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="56522-191">("Errore")</span><span class="sxs-lookup"><span data-stu-id="56522-191">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="56522-192">("Danneggiato")</span><span class="sxs-lookup"><span data-stu-id="56522-192">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="56522-193">("Sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="56522-193">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="56522-194">("Errore di predazione")</span><span class="sxs-lookup"><span data-stu-id="56522-194">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="56522-195">("Avvio")</span><span class="sxs-lookup"><span data-stu-id="56522-195">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="56522-196">("Arresto")</span><span class="sxs-lookup"><span data-stu-id="56522-196">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="56522-197">("Servizio")</span><span class="sxs-lookup"><span data-stu-id="56522-197">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="56522-198">**Terminale**</span><span class="sxs-lookup"><span data-stu-id="56522-198">**TerminalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56522-199">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="56522-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56522-200">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="56522-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56522-201">Nome del terminale.</span><span class="sxs-lookup"><span data-stu-id="56522-201">The name of the terminal.</span></span>

<span data-ttu-id="56522-202">Questa proprietà viene ereditata da [**Win32 \_ TerminalSetting**](win32-terminalsetting.md).</span><span class="sxs-lookup"><span data-stu-id="56522-202">This property is inherited from [**Win32\_TerminalSetting**](win32-terminalsetting.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="56522-203">Commenti</span><span class="sxs-lookup"><span data-stu-id="56522-203">Remarks</span></span>

<span data-ttu-id="56522-204">Per connettersi allo \\ \\ \\ spazio dei nomi CIMV2 TerminalServices radice, il livello di autenticazione deve includere la riservatezza dei pacchetti.</span><span class="sxs-lookup"><span data-stu-id="56522-204">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="56522-205">Per le chiamate C/C++, si tratta di un livello di autenticazione del livello di autenticazione **RPC \_ C \_ \_ \_ PKT \_ privacy**.</span><span class="sxs-lookup"><span data-stu-id="56522-205">For C/C++ calls, this would be an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="56522-206">Per Visual Basic e le chiamate di scripting, si tratta di un livello di autenticazione di **WbemAuthenticationLevelPktPrivacy** o "su PktPrivacy", con un valore pari a 6.</span><span class="sxs-lookup"><span data-stu-id="56522-206">For Visual Basic and scripting calls, this would be an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="56522-207">Il seguente esempio di Visual Basic Scripting Edition (VBScript) illustra come connettersi a un computer remoto con la privacy dei pacchetti.</span><span class="sxs-lookup"><span data-stu-id="56522-207">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="56522-208">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="56522-208">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="56522-209">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="56522-209">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="56522-210">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="56522-210">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="56522-211">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="56522-211">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="56522-212">Requisiti</span><span class="sxs-lookup"><span data-stu-id="56522-212">Requirements</span></span>



| <span data-ttu-id="56522-213">Requisito</span><span class="sxs-lookup"><span data-stu-id="56522-213">Requirement</span></span> | <span data-ttu-id="56522-214">Valore</span><span class="sxs-lookup"><span data-stu-id="56522-214">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="56522-215">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="56522-215">Minimum supported client</span></span><br/> | <span data-ttu-id="56522-216">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="56522-216">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="56522-217">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="56522-217">Minimum supported server</span></span><br/> | <span data-ttu-id="56522-218">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="56522-218">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="56522-219">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="56522-219">Namespace</span></span><br/>                | <span data-ttu-id="56522-220">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="56522-220">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="56522-221">MOF</span><span class="sxs-lookup"><span data-stu-id="56522-221">MOF</span></span><br/>                      | <dl> <span data-ttu-id="56522-222"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="56522-222"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="56522-223">DLL</span><span class="sxs-lookup"><span data-stu-id="56522-223">DLL</span></span><br/>                      | <dl> <span data-ttu-id="56522-224"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="56522-224"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56522-225">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="56522-225">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56522-226">**\_Terminale Win32**</span><span class="sxs-lookup"><span data-stu-id="56522-226">**Win32\_Terminal**</span></span>](win32-terminal.md)
</dt> <dt>

[<span data-ttu-id="56522-227">**\_TerminalSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="56522-227">**Win32\_TerminalSetting**</span></span>](win32-terminalsetting.md)
</dt> </dl>

 

