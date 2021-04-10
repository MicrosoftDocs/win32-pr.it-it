---
title: Classe Win32_Terminal
description: Rappresenta un terminale.
ms.assetid: d56cc605-6c5a-46ae-96fd-d0a4f5b6074a
ms.tgt_platform: multiple
keywords:
- Classe Win32_Terminal Servizi Desktop remoto
- Classe Win32_Terminal Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_Terminal
- Win32_Terminal.Caption
- Win32_Terminal.Description
- Win32_Terminal.InstallDate
- Win32_Terminal.Name
- Win32_Terminal.Status
- Win32_Terminal.fEnableTerminal
- Win32_Terminal.LoggedOnUsers
- Win32_Terminal.TerminalName
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7ae74003f798049fbdb34c955db3f64112bfcd2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119254"
---
# <a name="win32_terminal-class"></a><span data-ttu-id="a4086-105">\_Classe terminale Win32</span><span class="sxs-lookup"><span data-stu-id="a4086-105">Win32\_Terminal class</span></span>

<span data-ttu-id="a4086-106">La classe WMI del **\_ terminale Win32** rappresenta un terminale.</span><span class="sxs-lookup"><span data-stu-id="a4086-106">The **Win32\_Terminal** WMI class represents a terminal.</span></span>

<span data-ttu-id="a4086-107">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà definite ed ereditate, in ordine alfabetico.</span><span class="sxs-lookup"><span data-stu-id="a4086-107">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span> <span data-ttu-id="a4086-108">Per informazioni di riferimento sui metodi, vedere la tabella dei metodi più avanti in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="a4086-108">For reference information on methods, see the table of methods later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4086-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a4086-109">Syntax</span></span>

``` syntax
[dynamic, overwrite, provider("Win32_WIN32_TERMINAL_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_Terminal : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  uint32   fEnableTerminal;
  uint32   LoggedOnUsers;
  string   TerminalName;
};
```

## <a name="members"></a><span data-ttu-id="a4086-110">Members</span><span class="sxs-lookup"><span data-stu-id="a4086-110">Members</span></span>

<span data-ttu-id="a4086-111">La **classe \_ terminale Win32** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="a4086-111">The **Win32\_Terminal** class has these types of members:</span></span>

-   [<span data-ttu-id="a4086-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="a4086-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="a4086-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a4086-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a4086-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="a4086-114">Methods</span></span>

<span data-ttu-id="a4086-115">La **classe \_ terminale Win32** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="a4086-115">The **Win32\_Terminal** class has these methods.</span></span>



| <span data-ttu-id="a4086-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="a4086-116">Method</span></span>                                  | <span data-ttu-id="a4086-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a4086-117">Description</span></span>                                                                                                                                                                             |
|:----------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a4086-118">**Creare**</span><span class="sxs-lookup"><span data-stu-id="a4086-118">**Create**</span></span>](create-win32-terminal.md) | <span data-ttu-id="a4086-119">Crea un terminale con le impostazioni predefinite che possono essere personalizzate usando le proprietà e i metodi delle classi [**Win32 \_ TerminalSetting**](win32-terminalsetting.md) .</span><span class="sxs-lookup"><span data-stu-id="a4086-119">Creates a terminal with default settings which can be customized by using the properties and methods of the [**Win32\_TerminalSetting**](win32-terminalsetting.md) classes.</span></span><br/> |
| [<span data-ttu-id="a4086-120">**Delete**</span><span class="sxs-lookup"><span data-stu-id="a4086-120">**Delete**</span></span>](delete-win32-terminal.md) | <span data-ttu-id="a4086-121">Elimina il terminale specificato.</span><span class="sxs-lookup"><span data-stu-id="a4086-121">Deletes the specified terminal.</span></span><br/>                                                                                                                                              |
| [<span data-ttu-id="a4086-122">**Abilitare**</span><span class="sxs-lookup"><span data-stu-id="a4086-122">**Enable**</span></span>](win32-terminal-enable.md) | <span data-ttu-id="a4086-123">Disabilita o Abilita il terminale.</span><span class="sxs-lookup"><span data-stu-id="a4086-123">Disables or enables the terminal.</span></span><br/>                                                                                                                                            |
| [<span data-ttu-id="a4086-124">**Rinominare**</span><span class="sxs-lookup"><span data-stu-id="a4086-124">**Rename**</span></span>](win32-terminal-rename.md) | <span data-ttu-id="a4086-125">Rinomina il terminale.</span><span class="sxs-lookup"><span data-stu-id="a4086-125">Renames the terminal.</span></span><br/>                                                                                                                                                        |



 

### <a name="properties"></a><span data-ttu-id="a4086-126">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a4086-126">Properties</span></span>

<span data-ttu-id="a4086-127">La **classe \_ terminale Win32** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="a4086-127">The **Win32\_Terminal** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a4086-128">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="a4086-128">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4086-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a4086-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a4086-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a4086-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a4086-131">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="a4086-131">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="a4086-132">Breve descrizione (stringa a una riga) dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a4086-132">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="a4086-133">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a4086-133">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a4086-134">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="a4086-134">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4086-135">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a4086-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a4086-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a4086-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a4086-137">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a4086-137">Description of the object.</span></span>

<span data-ttu-id="a4086-138">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a4086-138">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a4086-139">**fEnableTerminal**</span><span class="sxs-lookup"><span data-stu-id="a4086-139">**fEnableTerminal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4086-140">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a4086-140">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a4086-141">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a4086-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a4086-142">Specifica se il terminale specificato è disabilitato o abilitato.</span><span class="sxs-lookup"><span data-stu-id="a4086-142">Specifies whether the specified terminal is disabled or enabled.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="a4086-143"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="a4086-143"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="a4086-144">Il terminale è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="a4086-144">The terminal is disabled.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="a4086-145"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="a4086-145"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="a4086-146">Il terminale è abilitato.</span><span class="sxs-lookup"><span data-stu-id="a4086-146">The terminal is enabled.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a4086-147">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="a4086-147">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4086-148">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a4086-148">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a4086-149">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a4086-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a4086-150">Qualificatori: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="a4086-150">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="a4086-151">Data di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a4086-151">The date the object was installed.</span></span> <span data-ttu-id="a4086-152">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="a4086-152">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="a4086-153">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a4086-153">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a4086-154">**LoggedOnUsers**</span><span class="sxs-lookup"><span data-stu-id="a4086-154">**LoggedOnUsers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4086-155">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a4086-155">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a4086-156">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a4086-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a4086-157">Numero di sessioni di accesso per il terminale.</span><span class="sxs-lookup"><span data-stu-id="a4086-157">Number of logged-on sessions for the terminal.</span></span>

</dd> <dt>

<span data-ttu-id="a4086-158">**Nome**</span><span class="sxs-lookup"><span data-stu-id="a4086-158">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4086-159">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a4086-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a4086-160">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a4086-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a4086-161">Nome dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a4086-161">The name of the object.</span></span>

<span data-ttu-id="a4086-162">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a4086-162">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a4086-163">**Status**</span><span class="sxs-lookup"><span data-stu-id="a4086-163">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4086-164">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a4086-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a4086-165">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a4086-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a4086-166">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="a4086-166">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="a4086-167">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a4086-167">Current status of the object.</span></span> <span data-ttu-id="a4086-168">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="a4086-168">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="a4086-169">Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro).</span><span class="sxs-lookup"><span data-stu-id="a4086-169">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="a4086-170">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="a4086-170">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="a4086-171">Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="a4086-171">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="a4086-172">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="a4086-172">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="a4086-173">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a4086-173">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="a4086-174">("OK")</span><span class="sxs-lookup"><span data-stu-id="a4086-174">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="a4086-175">("Errore")</span><span class="sxs-lookup"><span data-stu-id="a4086-175">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="a4086-176">("Danneggiato")</span><span class="sxs-lookup"><span data-stu-id="a4086-176">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="a4086-177">("Sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="a4086-177">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="a4086-178">("Errore di predazione")</span><span class="sxs-lookup"><span data-stu-id="a4086-178">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="a4086-179">("Avvio")</span><span class="sxs-lookup"><span data-stu-id="a4086-179">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="a4086-180">("Arresto")</span><span class="sxs-lookup"><span data-stu-id="a4086-180">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="a4086-181">("Servizio")</span><span class="sxs-lookup"><span data-stu-id="a4086-181">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a4086-182">**Terminale**</span><span class="sxs-lookup"><span data-stu-id="a4086-182">**TerminalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4086-183">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a4086-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a4086-184">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a4086-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a4086-185">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a4086-185">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a4086-186">Nome univoco che identifica l'istanza del terminale.</span><span class="sxs-lookup"><span data-stu-id="a4086-186">The unique name that identifies the instance of the terminal.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a4086-187">Commenti</span><span class="sxs-lookup"><span data-stu-id="a4086-187">Remarks</span></span>

<span data-ttu-id="a4086-188">**Win32 \_ Il terminale** è associato [**a Win32 \_ TerminalSetting**](win32-terminalsetting.md) come proprietà dell' **elemento** dell' [**associazione \_ TerminalTerminalSetting Win32**](win32-terminalterminalsetting.md) .</span><span class="sxs-lookup"><span data-stu-id="a4086-188">**Win32\_Terminal** is associated with [**Win32\_TerminalSetting**](win32-terminalsetting.md) as the **Element** property of the [**Win32\_TerminalTerminalSetting**](win32-terminalterminalsetting.md) association.</span></span>

<span data-ttu-id="a4086-189">Le classi seguenti sono sottoclassi della classe **\_ terminale Win32** : [**Win32 \_ TSGeneralSetting**](win32-tsgeneralsetting.md), Win32 [**\_ TSLogonSetting**](win32-tslogonsetting.md), [**Win32 \_ TSSessionSetting**](win32-tssessionsetting.md), Win32 [**\_ TSEnvironmentSetting**](win32-tsenvironmentsetting.md), Win32 [**\_ TSRemoteControlSetting**](win32-tsremotecontrolsetting.md), Win32 TSClientSetting [**, \_ Win32**](win32-tsclientsetting.md)TSNetworkAdapterSetting [**, \_**](win32-tsnetworkadaptersetting.md)Win32 TSNetworkAdapterListSetting, [**Win32 \_**](win32-tspermissionssetting.md)TSPermissionsSetting e [**Win32 \_ TSAccount**](win32-tsaccount.md). [**\_**](win32-tsnetworkadapterlistsetting.md)</span><span class="sxs-lookup"><span data-stu-id="a4086-189">The following classes are subclasses of the **Win32\_Terminal** class: [**Win32\_TSGeneralSetting**](win32-tsgeneralsetting.md), [**Win32\_TSLogonSetting**](win32-tslogonsetting.md), [**Win32\_TSSessionSetting**](win32-tssessionsetting.md), [**Win32\_TSEnvironmentSetting**](win32-tsenvironmentsetting.md), [**Win32\_TSRemoteControlSetting**](win32-tsremotecontrolsetting.md), [**Win32\_TSClientSetting**](win32-tsclientsetting.md), [**Win32\_TSNetworkAdapterSetting**](win32-tsnetworkadaptersetting.md), [**Win32\_TSNetworkAdapterListSetting**](win32-tsnetworkadapterlistsetting.md), [**Win32\_TSPermissionsSetting**](win32-tspermissionssetting.md), and [**Win32\_TSAccount**](win32-tsaccount.md).</span></span>

<span data-ttu-id="a4086-190">Si noti che WinStations associato alla sessione della console non può accedere ai metodi e alle proprietà di questa classe.</span><span class="sxs-lookup"><span data-stu-id="a4086-190">Note that Winstations associated with the console session cannot access the methods and properties of this class.</span></span> <span data-ttu-id="a4086-191">Se viene effettuato un tentativo di eseguire questa operazione specificando "console" come valore della proprietà **TerminalName** , i metodi di questo oggetto restituiscono **WBEM \_ E \_ non \_ supportati**.</span><span class="sxs-lookup"><span data-stu-id="a4086-191">If an attempt is made to do so by specifying "Console" as the value of the **TerminalName** property, methods of this object return **WBEM\_E\_NOT\_SUPPORTED**.</span></span> <span data-ttu-id="a4086-192">Questo codice di errore viene restituito anche se una stazione della finestra tenta di chiamare i metodi di questo oggetto per aggiungere o modificare le proprietà di sicurezza degli account LocalSystem, LocalService o NetworkService.</span><span class="sxs-lookup"><span data-stu-id="a4086-192">This error code is also returned if a window station attempts to call methods of this object to add or modify the security properties of the LocalSystem, LocalService, or NetworkService accounts.</span></span>

<span data-ttu-id="a4086-193">Per connettersi allo \\ \\ \\ spazio dei nomi CIMV2 TerminalServices radice, il livello di autenticazione deve includere la riservatezza dei pacchetti.</span><span class="sxs-lookup"><span data-stu-id="a4086-193">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="a4086-194">Per le chiamate C/C++, si tratta di un livello di autenticazione del livello di autenticazione **RPC \_ C \_ \_ \_ PKT \_ privacy**.</span><span class="sxs-lookup"><span data-stu-id="a4086-194">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="a4086-195">Per Visual Basic e le chiamate di scripting, si tratta di un livello di autenticazione di **WbemAuthenticationLevelPktPrivacy** o "su PktPrivacy", con un valore pari a 6.</span><span class="sxs-lookup"><span data-stu-id="a4086-195">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="a4086-196">Il seguente esempio di Visual Basic Scripting Edition (VBScript) illustra come connettersi a un computer remoto con la privacy dei pacchetti.</span><span class="sxs-lookup"><span data-stu-id="a4086-196">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="a4086-197">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="a4086-197">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="a4086-198">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="a4086-198">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="a4086-199">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="a4086-199">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="a4086-200">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="a4086-200">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="a4086-201">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a4086-201">Requirements</span></span>



| <span data-ttu-id="a4086-202">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4086-202">Requirement</span></span> | <span data-ttu-id="a4086-203">Valore</span><span class="sxs-lookup"><span data-stu-id="a4086-203">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a4086-204">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a4086-204">Minimum supported client</span></span><br/> | <span data-ttu-id="a4086-205">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a4086-205">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a4086-206">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a4086-206">Minimum supported server</span></span><br/> | <span data-ttu-id="a4086-207">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a4086-207">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a4086-208">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a4086-208">Namespace</span></span><br/>                | <span data-ttu-id="a4086-209">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="a4086-209">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="a4086-210">MOF</span><span class="sxs-lookup"><span data-stu-id="a4086-210">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a4086-211"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a4086-211"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="a4086-212">DLL</span><span class="sxs-lookup"><span data-stu-id="a4086-212">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a4086-213"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a4086-213"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4086-214">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a4086-214">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4086-215">**\_LogicalElement CIM**</span><span class="sxs-lookup"><span data-stu-id="a4086-215">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

[<span data-ttu-id="a4086-216">**\_TerminalServiceSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="a4086-216">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="a4086-217">**\_TerminalTerminalSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="a4086-217">**Win32\_TerminalTerminalSetting**</span></span>](win32-terminalterminalsetting.md)
</dt> </dl>

 

