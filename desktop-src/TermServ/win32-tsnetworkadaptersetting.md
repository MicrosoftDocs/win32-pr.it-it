---
title: Classe Win32_TSNetworkAdapterSetting
description: Definisce diverse impostazioni di configurazione per la \_ classe terminale Win32, incluse le proprietà correlate alla scheda di rete e il numero massimo di connessioni consentite.
ms.assetid: b8a757e6-801b-4349-902e-76596b06df1f
ms.tgt_platform: multiple
keywords:
- Classe Win32_TSNetworkAdapterSetting Servizi Desktop remoto
- Classe Win32_TSNetworkAdapterSetting Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_TSNetworkAdapterSetting
- Win32_TSNetworkAdapterSetting.Caption
- Win32_TSNetworkAdapterSetting.Description
- Win32_TSNetworkAdapterSetting.InstallDate
- Win32_TSNetworkAdapterSetting.Name
- Win32_TSNetworkAdapterSetting.Status
- Win32_TSNetworkAdapterSetting.TerminalName
- Win32_TSNetworkAdapterSetting.DeviceIDList
- Win32_TSNetworkAdapterSetting.MaximumConnections
- Win32_TSNetworkAdapterSetting.NetworkAdapterID
- Win32_TSNetworkAdapterSetting.NetworkAdapterLanaID
- Win32_TSNetworkAdapterSetting.NetworkAdapterList
- Win32_TSNetworkAdapterSetting.NetworkAdapterName
- Win32_TSNetworkAdapterSetting.PolicySourceMaximumConnections
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f2f2f1ac7d6bf4b1fd3fb5f5a92fc4fd5260a92
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477699"
---
# <a name="win32_tsnetworkadaptersetting-class"></a><span data-ttu-id="33752-105">Win32 \_ TSNetworkAdapterSetting (classe)</span><span class="sxs-lookup"><span data-stu-id="33752-105">Win32\_TSNetworkAdapterSetting class</span></span>

<span data-ttu-id="33752-106">La classe WMI **Win32 \_ TSNetworkAdapterSetting** definisce varie impostazioni di configurazione per la classe [**\_ terminale Win32**](win32-terminal.md) , incluse le proprietà correlate alla scheda di rete e il numero massimo di connessioni consentite.</span><span class="sxs-lookup"><span data-stu-id="33752-106">The **Win32\_TSNetworkAdapterSetting** WMI class defines various configuration settings for the [**Win32\_Terminal**](win32-terminal.md) class including properties related to the network adapter and the maximum number of connections allowed.</span></span>

<span data-ttu-id="33752-107">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà definite ed ereditate, in ordine alfabetico.</span><span class="sxs-lookup"><span data-stu-id="33752-107">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span> <span data-ttu-id="33752-108">Per informazioni di riferimento sui metodi, vedere la tabella dei metodi più avanti in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="33752-108">For reference information on methods, see the table of methods later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="33752-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="33752-109">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TSNETWORKADAPTERSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSNetworkAdapterSetting : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  string   DeviceIDList[];
  uint32   MaximumConnections;
  string   NetworkAdapterID;
  uint32   NetworkAdapterLanaID;
  string   NetworkAdapterList[];
  string   NetworkAdapterName;
  uint32   PolicySourceMaximumConnections;
};
```

## <a name="members"></a><span data-ttu-id="33752-110">Members</span><span class="sxs-lookup"><span data-stu-id="33752-110">Members</span></span>

<span data-ttu-id="33752-111">La classe **Win32 \_ TSNetworkAdapterSetting** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="33752-111">The **Win32\_TSNetworkAdapterSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="33752-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="33752-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="33752-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="33752-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="33752-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="33752-114">Methods</span></span>

<span data-ttu-id="33752-115">La classe **Win32 \_ TSNetworkAdapterSetting** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="33752-115">The **Win32\_TSNetworkAdapterSetting** class has these methods.</span></span>



| <span data-ttu-id="33752-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="33752-116">Method</span></span>                                                                                     | <span data-ttu-id="33752-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="33752-117">Description</span></span>                                                                                              |
|:-------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="33752-118">**SelectAllNetworkAdapters**</span><span class="sxs-lookup"><span data-stu-id="33752-118">**SelectAllNetworkAdapters**</span></span>](win32-tsnetworkadaptersetting-selectallnetworkadapters.md) | <span data-ttu-id="33752-119">Seleziona tutte le schede di rete.</span><span class="sxs-lookup"><span data-stu-id="33752-119">Selects all network adapters.</span></span><br/>                                                                 |
| [<span data-ttu-id="33752-120">**SelectNetworkAdapterIP**</span><span class="sxs-lookup"><span data-stu-id="33752-120">**SelectNetworkAdapterIP**</span></span>](win32-tsnetworkadaptersetting-selectnetworkadapterip.md)     | <span data-ttu-id="33752-121">Seleziona una scheda di rete in base all'indirizzo IP della scheda.</span><span class="sxs-lookup"><span data-stu-id="33752-121">Selects a network adapter based on the adapter's IP address.</span></span><br/>                                  |
| [<span data-ttu-id="33752-122">**SetNetworkAdapterLanaID**</span><span class="sxs-lookup"><span data-stu-id="33752-122">**SetNetworkAdapterLanaID**</span></span>](setnetworkadapterlanaid-win32-tsnetworkadaptersetting.md)   | <span data-ttu-id="33752-123">Specifica il numero di scheda di rete locale (LANA) NetBIOS della scheda di rete da impostare.</span><span class="sxs-lookup"><span data-stu-id="33752-123">Specifies the NetBIOS Local Area Network Adapter (LANA) number of the network adapter to set.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="33752-124">Proprietà</span><span class="sxs-lookup"><span data-stu-id="33752-124">Properties</span></span>

<span data-ttu-id="33752-125">La classe **Win32 \_ TSNetworkAdapterSetting** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="33752-125">The **Win32\_TSNetworkAdapterSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="33752-126">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="33752-126">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33752-127">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="33752-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33752-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="33752-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="33752-129">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="33752-129">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="33752-130">Breve descrizione (stringa a una riga) dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="33752-130">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="33752-131">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="33752-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="33752-132">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="33752-132">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33752-133">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="33752-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33752-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="33752-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="33752-135">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="33752-135">Description of the object.</span></span>

<span data-ttu-id="33752-136">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="33752-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="33752-137">**DeviceIDList**</span><span class="sxs-lookup"><span data-stu-id="33752-137">**DeviceIDList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33752-138">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="33752-138">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="33752-139">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="33752-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="33752-140">Matrice di stringhe di ID dispositivo disponibili restituiti nell'ordine delle schede di rete fisiche restituite nella matrice di proprietà **NetworkAdapterList** .</span><span class="sxs-lookup"><span data-stu-id="33752-140">String array of available device IDs returned in the order of physical network adapters returned in the **NetworkAdapterList** property array.</span></span> <span data-ttu-id="33752-141">Il valore ID dispositivo è la proprietà **DeviceID** in [**Win32 \_ NetworkAdapter**](/windows/desktop/CIMWin32Prov/win32-networkadapter)</span><span class="sxs-lookup"><span data-stu-id="33752-141">The device ID value is the **DeviceID** property in [**Win32\_NetworkAdapter**](/windows/desktop/CIMWin32Prov/win32-networkadapter)</span></span>

</dd> <dt>

<span data-ttu-id="33752-142">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="33752-142">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33752-143">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="33752-143">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="33752-144">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="33752-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="33752-145">Qualificatori: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="33752-145">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="33752-146">Data di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="33752-146">The date the object was installed.</span></span> <span data-ttu-id="33752-147">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="33752-147">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="33752-148">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="33752-148">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="33752-149">**MaximumConnections**</span><span class="sxs-lookup"><span data-stu-id="33752-149">**MaximumConnections**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33752-150">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="33752-150">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="33752-151">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="33752-151">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="33752-152">Numero massimo di connessioni consentite.</span><span class="sxs-lookup"><span data-stu-id="33752-152">The maximum number of connections allowed.</span></span> <span data-ttu-id="33752-153">Il valore **MaxInt** indica un numero illimitato di connessioni.</span><span class="sxs-lookup"><span data-stu-id="33752-153">The value **MAXINT** denotes an unlimited number of connections.</span></span>

</dd> <dt>

<span data-ttu-id="33752-154">**Nome**</span><span class="sxs-lookup"><span data-stu-id="33752-154">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33752-155">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="33752-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33752-156">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="33752-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="33752-157">Nome dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="33752-157">The name of the object.</span></span>

<span data-ttu-id="33752-158">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="33752-158">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="33752-159">**NetworkAdapterID**</span><span class="sxs-lookup"><span data-stu-id="33752-159">**NetworkAdapterID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33752-160">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="33752-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33752-161">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="33752-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="33752-162">GUID che rappresenta l'ID della scheda di rete da impostare.</span><span class="sxs-lookup"><span data-stu-id="33752-162">The GUID that represents the ID of the network adapter to set.</span></span> <span data-ttu-id="33752-163">Un **GUID** costituito da tutti gli zeri indica tutte le schede di rete.</span><span class="sxs-lookup"><span data-stu-id="33752-163">A **GUID** that consists of all zeros denotes all network adapters.</span></span>

</dd> <dt>

<span data-ttu-id="33752-164">**NetworkAdapterLanaID**</span><span class="sxs-lookup"><span data-stu-id="33752-164">**NetworkAdapterLanaID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33752-165">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="33752-165">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="33752-166">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="33752-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="33752-167">Numero di scheda di rete locale (LANA) NetBIOS della scheda di rete utilizzata per identificare la scheda di rete assegnata al terminale.</span><span class="sxs-lookup"><span data-stu-id="33752-167">NetBIOS Local Area Network Adapter (LANA) number of the network adapter that is used to identify the network adapter assigned to the terminal.</span></span>

</dd> <dt>

<span data-ttu-id="33752-168">**NetworkAdapterList**</span><span class="sxs-lookup"><span data-stu-id="33752-168">**NetworkAdapterList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33752-169">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="33752-169">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="33752-170">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="33752-170">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="33752-171">Matrice di stringhe di schede di rete fisiche disponibili e ID dispositivo corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="33752-171">String array of available physical network adapters and the corresponding device IDs.</span></span> <span data-ttu-id="33752-172">Gli ID dispositivo sono la proprietà **DeviceID** in [**Win32 \_ NetworkAdapter**](/windows/desktop/CIMWin32Prov/win32-networkadapter).</span><span class="sxs-lookup"><span data-stu-id="33752-172">The device IDs are the **DeviceID** property in [**Win32\_NetworkAdapter**](/windows/desktop/CIMWin32Prov/win32-networkadapter).</span></span>

</dd> <dt>

<span data-ttu-id="33752-173">**NetworkAdapterName**</span><span class="sxs-lookup"><span data-stu-id="33752-173">**NetworkAdapterName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33752-174">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="33752-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33752-175">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="33752-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="33752-176">Descrizione della scheda di rete da impostare.</span><span class="sxs-lookup"><span data-stu-id="33752-176">Description of the network adapter to set.</span></span> <span data-ttu-id="33752-177">Questo valore è in [**Win32 \_ NetworkAdapterConfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration).</span><span class="sxs-lookup"><span data-stu-id="33752-177">This value is in [**Win32\_NetworkAdapterConfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration).</span></span>

</dd> <dt>

<span data-ttu-id="33752-178">**PolicySourceMaximumConnections**</span><span class="sxs-lookup"><span data-stu-id="33752-178">**PolicySourceMaximumConnections**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33752-179">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="33752-179">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="33752-180">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="33752-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="33752-181">Indica se la proprietà **MaximumConnections** è configurata dal server, da criteri di gruppo o per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="33752-181">Indicates whether the **MaximumConnections** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="33752-182">0</span><span class="sxs-lookup"><span data-stu-id="33752-182">0</span></span>
</dt> <dd>

<span data-ttu-id="33752-183">Server</span><span class="sxs-lookup"><span data-stu-id="33752-183">Server</span></span>

</dd> <dt>

<span data-ttu-id="33752-184">1</span><span class="sxs-lookup"><span data-stu-id="33752-184">1</span></span>
</dt> <dd>

<span data-ttu-id="33752-185">Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="33752-185">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="33752-186">2</span><span class="sxs-lookup"><span data-stu-id="33752-186">2</span></span>
</dt> <dd>

<span data-ttu-id="33752-187">Predefinito</span><span class="sxs-lookup"><span data-stu-id="33752-187">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="33752-188">**Status**</span><span class="sxs-lookup"><span data-stu-id="33752-188">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33752-189">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="33752-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33752-190">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="33752-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="33752-191">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="33752-191">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="33752-192">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="33752-192">Current status of the object.</span></span> <span data-ttu-id="33752-193">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="33752-193">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="33752-194">Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro).</span><span class="sxs-lookup"><span data-stu-id="33752-194">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="33752-195">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="33752-195">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="33752-196">Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="33752-196">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="33752-197">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="33752-197">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="33752-198">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="33752-198">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="33752-199">("OK")</span><span class="sxs-lookup"><span data-stu-id="33752-199">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="33752-200">("Errore")</span><span class="sxs-lookup"><span data-stu-id="33752-200">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="33752-201">("Danneggiato")</span><span class="sxs-lookup"><span data-stu-id="33752-201">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="33752-202">("Sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="33752-202">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="33752-203">("Errore di predazione")</span><span class="sxs-lookup"><span data-stu-id="33752-203">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="33752-204">("Avvio")</span><span class="sxs-lookup"><span data-stu-id="33752-204">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="33752-205">("Arresto")</span><span class="sxs-lookup"><span data-stu-id="33752-205">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="33752-206">("Servizio")</span><span class="sxs-lookup"><span data-stu-id="33752-206">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="33752-207">**Terminale**</span><span class="sxs-lookup"><span data-stu-id="33752-207">**TerminalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33752-208">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="33752-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33752-209">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="33752-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="33752-210">Nome del terminale.</span><span class="sxs-lookup"><span data-stu-id="33752-210">The name of the terminal.</span></span>

<span data-ttu-id="33752-211">Questa proprietà viene ereditata da [**Win32 \_ TerminalSetting**](win32-terminalsetting.md).</span><span class="sxs-lookup"><span data-stu-id="33752-211">This property is inherited from [**Win32\_TerminalSetting**](win32-terminalsetting.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="33752-212">Commenti</span><span class="sxs-lookup"><span data-stu-id="33752-212">Remarks</span></span>

<span data-ttu-id="33752-213">Tenere presente che WinStations associato alla sessione della console non può accedere ai metodi e alle proprietà di questa classe.</span><span class="sxs-lookup"><span data-stu-id="33752-213">Be aware that Winstations associated with the console session cannot access the methods and properties of this class.</span></span> <span data-ttu-id="33752-214">Se viene effettuato un tentativo di eseguire questa operazione specificando "console" come valore della proprietà TerminalName, i metodi di questo oggetto restituiscono **WBEM \_ E \_ non \_ supportati**.</span><span class="sxs-lookup"><span data-stu-id="33752-214">If an attempt is made to do so by specifying "Console" as the value of the TerminalName property, methods of this object return **WBEM\_E\_NOT\_SUPPORTED**.</span></span> <span data-ttu-id="33752-215">Questo codice di errore viene restituito anche se una stazione della finestra tenta di chiamare i metodi di questo oggetto per aggiungere o modificare le proprietà di sicurezza degli account LocalSystem, LocalService o NetworkService.</span><span class="sxs-lookup"><span data-stu-id="33752-215">This error code is also returned if a window station attempts to call methods of this object to add or modify the security properties of the LocalSystem, LocalService, or NetworkService accounts.</span></span>

<span data-ttu-id="33752-216">Per connettersi allo \\ \\ spazio dei nomi "root cimv2 TerminalServices", il livello di autenticazione deve includere la riservatezza dei pacchetti.</span><span class="sxs-lookup"><span data-stu-id="33752-216">To connect to the "Root\\CIMV2\\TerminalServices" namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="33752-217">Per le chiamate C/C++, si tratta di un livello di autenticazione del livello di autenticazione **RPC \_ C \_ \_ \_ PKT \_ privacy**.</span><span class="sxs-lookup"><span data-stu-id="33752-217">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="33752-218">Per Visual Basic e le chiamate di scripting, si tratta di un livello di autenticazione di **WbemAuthenticationLevelPktPrivacy** o "su PktPrivacy", con un valore pari a 6.</span><span class="sxs-lookup"><span data-stu-id="33752-218">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="33752-219">Il seguente esempio di Visual Basic Scripting Edition (VBScript) illustra come connettersi a un computer remoto con la privacy dei pacchetti.</span><span class="sxs-lookup"><span data-stu-id="33752-219">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="33752-220">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="33752-220">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="33752-221">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="33752-221">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="33752-222">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="33752-222">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="33752-223">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="33752-223">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="33752-224">Requisiti</span><span class="sxs-lookup"><span data-stu-id="33752-224">Requirements</span></span>



| <span data-ttu-id="33752-225">Requisito</span><span class="sxs-lookup"><span data-stu-id="33752-225">Requirement</span></span> | <span data-ttu-id="33752-226">Valore</span><span class="sxs-lookup"><span data-stu-id="33752-226">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="33752-227">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="33752-227">Minimum supported client</span></span><br/> | <span data-ttu-id="33752-228">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="33752-228">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="33752-229">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="33752-229">Minimum supported server</span></span><br/> | <span data-ttu-id="33752-230">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="33752-230">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="33752-231">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="33752-231">Namespace</span></span><br/>                | <span data-ttu-id="33752-232">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="33752-232">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="33752-233">MOF</span><span class="sxs-lookup"><span data-stu-id="33752-233">MOF</span></span><br/>                      | <dl> <span data-ttu-id="33752-234"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="33752-234"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="33752-235">DLL</span><span class="sxs-lookup"><span data-stu-id="33752-235">DLL</span></span><br/>                      | <dl> <span data-ttu-id="33752-236"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="33752-236"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33752-237">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="33752-237">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33752-238">**\_NetworkAdapter Win32**</span><span class="sxs-lookup"><span data-stu-id="33752-238">**Win32\_NetworkAdapter**</span></span>](/windows/desktop/CIMWin32Prov/win32-networkadapter)
</dt> <dt>

[<span data-ttu-id="33752-239">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="33752-239">**Win32\_NetworkAdapterConfiguration**</span></span>](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration)
</dt> <dt>

[<span data-ttu-id="33752-240">**\_TerminalSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="33752-240">**Win32\_TerminalSetting**</span></span>](win32-terminalsetting.md)
</dt> <dt>

[<span data-ttu-id="33752-241">**\_TSNetworkAdapterListSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="33752-241">**Win32\_TSNetworkAdapterListSetting**</span></span>](win32-tsnetworkadapterlistsetting.md)
</dt> </dl>

 

