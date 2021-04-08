---
title: Classe Win32_TSVirtualIP
description: Definisce le impostazioni di virtualizzazione IP (Internet Protocol) per un server Host sessione Desktop remoto (host sessione Desktop remoto).
ms.assetid: c37d572c-f6db-438b-8290-006a623c6593
ms.tgt_platform: multiple
keywords:
- Classe Win32_TSVirtualIP Servizi Desktop remoto
- Classe Win32_TSVirtualIP Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP
- Win32_TSVirtualIP.Caption
- Win32_TSVirtualIP.Description
- Win32_TSVirtualIP.InstallDate
- Win32_TSVirtualIP.Name
- Win32_TSVirtualIP.Status
- Win32_TSVirtualIP.VirtualIPActive
- Win32_TSVirtualIP.PolicySourceVirtualIPActive
- Win32_TSVirtualIP.VirtualIPMode
- Win32_TSVirtualIP.PolicySourceVirtualIPMode
- Win32_TSVirtualIP.ProgramList
- Win32_TSVirtualIP.PolicySourceProgramList
- Win32_TSVirtualIP.NetworkAdapterDescription
- Win32_TSVirtualIP.NetworkAdapterMacAddress
- Win32_TSVirtualIP.PolicySourceNetworkAdapter
- Win32_TSVirtualIP.NetworkAdapterDescriptionList
- Win32_TSVirtualIP.NetworkAdapterMacList
- Win32_TSVirtualIP.VirtualizeLoopbackAddressesEnabled
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f87db04d61dda0c6034b536544362ec09e0aaa66
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740183"
---
# <a name="win32_tsvirtualip-class"></a><span data-ttu-id="f7154-105">Win32 \_ TSVirtualIP (classe)</span><span class="sxs-lookup"><span data-stu-id="f7154-105">Win32\_TSVirtualIP class</span></span>

<span data-ttu-id="f7154-106">Definisce le impostazioni di virtualizzazione IP (Internet Protocol) per un server Host sessione Desktop remoto (host sessione Desktop remoto).</span><span class="sxs-lookup"><span data-stu-id="f7154-106">Defines Internet protocol (IP) virtualization settings for a Remote Desktop Session Host (RD Session Host) server.</span></span>

<span data-ttu-id="f7154-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="f7154-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7154-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f7154-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TSVIRTUALIP_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\TSAppSrv\\VirtualIP"), AMENDMENT]
class Win32_TSVirtualIP : CIM_Setting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  uint32   VirtualIPActive;
  uint32   PolicySourceVirtualIPActive;
  uint32   VirtualIPMode;
  uint32   PolicySourceVirtualIPMode;
  string   ProgramList[];
  uint32   PolicySourceProgramList;
  string   NetworkAdapterDescription;
  string   NetworkAdapterMacAddress;
  uint32   PolicySourceNetworkAdapter;
  string   NetworkAdapterDescriptionList[];
  string   NetworkAdapterMacList[];
  uint32   VirtualizeLoopbackAddressesEnabled;
};
```

## <a name="members"></a><span data-ttu-id="f7154-109">Members</span><span class="sxs-lookup"><span data-stu-id="f7154-109">Members</span></span>

<span data-ttu-id="f7154-110">La classe **Win32 \_ TSVirtualIP** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="f7154-110">The **Win32\_TSVirtualIP** class has these types of members:</span></span>

-   [<span data-ttu-id="f7154-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="f7154-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="f7154-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f7154-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="f7154-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="f7154-113">Methods</span></span>

<span data-ttu-id="f7154-114">La classe **Win32 \_ TSVirtualIP** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="f7154-114">The **Win32\_TSVirtualIP** class has these methods.</span></span>



| <span data-ttu-id="f7154-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="f7154-115">Method</span></span>                                                                                                   | <span data-ttu-id="f7154-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f7154-116">Description</span></span>                                                                                                                                                                  |
|:---------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f7154-117">**AddProgram**</span><span class="sxs-lookup"><span data-stu-id="f7154-117">**AddProgram**</span></span>](addprogram-win32-tsvirtualip.md)                                                       | <span data-ttu-id="f7154-118">Aggiunge un programma all'elenco di programmi che utilizzano la virtualizzazione IP.</span><span class="sxs-lookup"><span data-stu-id="f7154-118">Adds a program to the list of programs that use IP virtualization.</span></span><br/>                                                                                                |
| [<span data-ttu-id="f7154-119">**RemoveProgram**</span><span class="sxs-lookup"><span data-stu-id="f7154-119">**RemoveProgram**</span></span>](removeprogram-win32-tsvirtualip.md)                                                 | <span data-ttu-id="f7154-120">Rimuove un programma dall'elenco di programmi che utilizzano la virtualizzazione IP.</span><span class="sxs-lookup"><span data-stu-id="f7154-120">Removes a program from the list of programs that use IP virtualization.</span></span><br/>                                                                                           |
| [<span data-ttu-id="f7154-121">**SelectNetworkAdapter**</span><span class="sxs-lookup"><span data-stu-id="f7154-121">**SelectNetworkAdapter**</span></span>](selectnetworkadapter-win32-tsvirtualip.md)                                   | <span data-ttu-id="f7154-122">Imposta l'indirizzo MAC della scheda di rete da utilizzare per la virtualizzazione IP.</span><span class="sxs-lookup"><span data-stu-id="f7154-122">Sets the MAC address of the network adapter to use for IP virtualization.</span></span><br/>                                                                                         |
| [<span data-ttu-id="f7154-123">**Seprogrammatore**</span><span class="sxs-lookup"><span data-stu-id="f7154-123">**SetProgramList**</span></span>](setprogramlist-win32-tsvirtualip.md)                                               | <span data-ttu-id="f7154-124">Sovrascrive l'elenco di programmi che usano la virtualizzazione IP.</span><span class="sxs-lookup"><span data-stu-id="f7154-124">Overwrites the list of programs that use IP virtualization.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="f7154-125">**SetVirtualIPActive**</span><span class="sxs-lookup"><span data-stu-id="f7154-125">**SetVirtualIPActive**</span></span>](setvirtualipactive-win32-tsvirtualip.md)                                       | <span data-ttu-id="f7154-126">Imposta il valore della proprietà **VirtualIPActive** .</span><span class="sxs-lookup"><span data-stu-id="f7154-126">Sets the **VirtualIPActive** property value.</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="f7154-127">**SetVirtualIPMode**</span><span class="sxs-lookup"><span data-stu-id="f7154-127">**SetVirtualIPMode**</span></span>](setvirtualipmode-win32-tsvirtualip.md)                                           | <span data-ttu-id="f7154-128">Imposta il valore della proprietà **VirtualIPMode** .</span><span class="sxs-lookup"><span data-stu-id="f7154-128">Sets the **VirtualIPMode** property value.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="f7154-129">**SetVirtualizeLoopbackAddressesEnabled**</span><span class="sxs-lookup"><span data-stu-id="f7154-129">**SetVirtualizeLoopbackAddressesEnabled**</span></span>](setvirtualizeloopbackaddressesenabled-win32-tsvirtualip.md) | <span data-ttu-id="f7154-130">Imposta il valore della proprietà **VirtualizeLoopbackAddressesEnabled** .</span><span class="sxs-lookup"><span data-stu-id="f7154-130">Sets the **VirtualizeLoopbackAddressesEnabled** property value.</span></span><br/> <span data-ttu-id="f7154-131">**Windows Server 2008 R2:** Questo metodo non è disponibile prima di Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="f7154-131">**Windows Server 2008 R2:** This method is not available prior to Windows Server 2012.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="f7154-132">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f7154-132">Properties</span></span>

<span data-ttu-id="f7154-133">La classe **Win32 \_ TSVirtualIP** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="f7154-133">The **Win32\_TSVirtualIP** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f7154-134">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="f7154-134">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7154-135">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f7154-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7154-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f7154-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7154-137">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="f7154-137">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="f7154-138">Breve descrizione (stringa a una riga) dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f7154-138">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="f7154-139">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f7154-139">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f7154-140">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="f7154-140">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7154-141">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f7154-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7154-142">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f7154-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f7154-143">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f7154-143">Description of the object.</span></span>

<span data-ttu-id="f7154-144">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f7154-144">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f7154-145">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="f7154-145">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7154-146">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f7154-146">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f7154-147">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f7154-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7154-148">Qualificatori: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="f7154-148">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="f7154-149">Data di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f7154-149">The date the object was installed.</span></span> <span data-ttu-id="f7154-150">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="f7154-150">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="f7154-151">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f7154-151">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f7154-152">**Nome**</span><span class="sxs-lookup"><span data-stu-id="f7154-152">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7154-153">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f7154-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7154-154">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f7154-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f7154-155">Nome dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f7154-155">The name of the object.</span></span>

<span data-ttu-id="f7154-156">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f7154-156">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f7154-157">**NetworkAdapterDescription**</span><span class="sxs-lookup"><span data-stu-id="f7154-157">**NetworkAdapterDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7154-158">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f7154-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7154-159">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f7154-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f7154-160">Descrizione della scheda di rete.</span><span class="sxs-lookup"><span data-stu-id="f7154-160">The description for the network adapter.</span></span>

</dd> <dt>

<span data-ttu-id="f7154-161">**NetworkAdapterDescriptionList**</span><span class="sxs-lookup"><span data-stu-id="f7154-161">**NetworkAdapterDescriptionList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7154-162">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="f7154-162">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f7154-163">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f7154-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f7154-164">Elenco di descrizioni delle schede di rete fisiche disponibili.</span><span class="sxs-lookup"><span data-stu-id="f7154-164">The list of descriptions of the available physical network adapters.</span></span>

</dd> <dt>

<span data-ttu-id="f7154-165">**NetworkAdapterMacAddress**</span><span class="sxs-lookup"><span data-stu-id="f7154-165">**NetworkAdapterMacAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7154-166">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f7154-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7154-167">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f7154-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f7154-168">Indirizzo MAC della scheda di rete.</span><span class="sxs-lookup"><span data-stu-id="f7154-168">The MAC address of the network adapter.</span></span>

</dd> <dt>

<span data-ttu-id="f7154-169">**NetworkAdapterMacList**</span><span class="sxs-lookup"><span data-stu-id="f7154-169">**NetworkAdapterMacList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7154-170">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="f7154-170">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f7154-171">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f7154-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f7154-172">Elenco di indirizzi MAC delle schede di rete fisiche disponibili.</span><span class="sxs-lookup"><span data-stu-id="f7154-172">The list of MAC addresses of the available physical network adapters.</span></span>

</dd> <dt>

<span data-ttu-id="f7154-173">**PolicySourceNetworkAdapter**</span><span class="sxs-lookup"><span data-stu-id="f7154-173">**PolicySourceNetworkAdapter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7154-174">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f7154-174">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f7154-175">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f7154-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f7154-176">Indica se la scheda di rete è configurata dal server o da criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="f7154-176">Indicates whether the network adapter is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="f7154-177">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="f7154-177">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="f7154-178">Server</span><span class="sxs-lookup"><span data-stu-id="f7154-178">Server</span></span>

</dd> <dt>

<span data-ttu-id="f7154-179">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="f7154-179">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="f7154-180">Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="f7154-180">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f7154-181">**PolicySourceProgramList**</span><span class="sxs-lookup"><span data-stu-id="f7154-181">**PolicySourceProgramList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7154-182">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f7154-182">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f7154-183">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f7154-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f7154-184">Indica se la proprietà dell'oggetto **Programmi\Microsoft** è configurata dal server o da criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="f7154-184">Indicates whether the **ProgramList** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="f7154-185">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="f7154-185">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="f7154-186">Server</span><span class="sxs-lookup"><span data-stu-id="f7154-186">Server</span></span>

</dd> <dt>

<span data-ttu-id="f7154-187">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="f7154-187">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="f7154-188">Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="f7154-188">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f7154-189">**PolicySourceVirtualIPActive**</span><span class="sxs-lookup"><span data-stu-id="f7154-189">**PolicySourceVirtualIPActive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7154-190">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f7154-190">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f7154-191">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f7154-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f7154-192">Indica se la proprietà **VirtualIPActive** è configurata dal server o da criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="f7154-192">Indicates if the **VirtualIPActive** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="f7154-193">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="f7154-193">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="f7154-194">Server</span><span class="sxs-lookup"><span data-stu-id="f7154-194">Server</span></span>

</dd> <dt>

<span data-ttu-id="f7154-195">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="f7154-195">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="f7154-196">Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="f7154-196">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f7154-197">**PolicySourceVirtualIPMode**</span><span class="sxs-lookup"><span data-stu-id="f7154-197">**PolicySourceVirtualIPMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7154-198">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f7154-198">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f7154-199">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f7154-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f7154-200">Indica se la proprietà **VirtualIPMode** è configurata dal server o da criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="f7154-200">Indicates if the **VirtualIPMode** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="f7154-201">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="f7154-201">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="f7154-202">Server</span><span class="sxs-lookup"><span data-stu-id="f7154-202">Server</span></span>

</dd> <dt>

<span data-ttu-id="f7154-203">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="f7154-203">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="f7154-204">Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="f7154-204">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f7154-205">**Programmatore**</span><span class="sxs-lookup"><span data-stu-id="f7154-205">**ProgramList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7154-206">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="f7154-206">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f7154-207">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f7154-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f7154-208">Specifica i programmi configurati per l'utilizzo della virtualizzazione IP.</span><span class="sxs-lookup"><span data-stu-id="f7154-208">Specifies the programs that are configured to use IP virtualization.</span></span> <span data-ttu-id="f7154-209">Questo può essere il nome di un programma o il percorso completo.</span><span class="sxs-lookup"><span data-stu-id="f7154-209">This may a program name or the full path.</span></span>

</dd> <dt>

<span data-ttu-id="f7154-210">**Status**</span><span class="sxs-lookup"><span data-stu-id="f7154-210">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7154-211">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f7154-211">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7154-212">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f7154-212">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7154-213">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="f7154-213">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="f7154-214">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f7154-214">Current status of the object.</span></span> <span data-ttu-id="f7154-215">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="f7154-215">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="f7154-216">Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro).</span><span class="sxs-lookup"><span data-stu-id="f7154-216">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="f7154-217">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="f7154-217">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="f7154-218">Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="f7154-218">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="f7154-219">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="f7154-219">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="f7154-220">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f7154-220">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="f7154-221">("OK")</span><span class="sxs-lookup"><span data-stu-id="f7154-221">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f7154-222">("Errore")</span><span class="sxs-lookup"><span data-stu-id="f7154-222">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f7154-223">("Danneggiato")</span><span class="sxs-lookup"><span data-stu-id="f7154-223">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f7154-224">("Sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="f7154-224">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f7154-225">("Errore di predazione")</span><span class="sxs-lookup"><span data-stu-id="f7154-225">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f7154-226">("Avvio")</span><span class="sxs-lookup"><span data-stu-id="f7154-226">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f7154-227">("Arresto")</span><span class="sxs-lookup"><span data-stu-id="f7154-227">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f7154-228">("Servizio")</span><span class="sxs-lookup"><span data-stu-id="f7154-228">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f7154-229">**VirtualIPActive**</span><span class="sxs-lookup"><span data-stu-id="f7154-229">**VirtualIPActive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7154-230">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f7154-230">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f7154-231">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f7154-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7154-232">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f7154-232">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f7154-233">Specifica se la virtualizzazione IP è attiva sul server.</span><span class="sxs-lookup"><span data-stu-id="f7154-233">Specifies if IP virtualization is active on the server.</span></span> <span data-ttu-id="f7154-234">Può corrispondere a uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="f7154-234">This can be one of the following values.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="f7154-235"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="f7154-235"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="f7154-236">La virtualizzazione IP non è attiva.</span><span class="sxs-lookup"><span data-stu-id="f7154-236">IP virtualization is not active.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="f7154-237"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="f7154-237"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="f7154-238">La virtualizzazione IP è attiva.</span><span class="sxs-lookup"><span data-stu-id="f7154-238">IP virtualization is active.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f7154-239">**VirtualIPMode**</span><span class="sxs-lookup"><span data-stu-id="f7154-239">**VirtualIPMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7154-240">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f7154-240">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f7154-241">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f7154-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f7154-242">Specifica la modalità di virtualizzazione IP utilizzata nel server.</span><span class="sxs-lookup"><span data-stu-id="f7154-242">Specifies which IP virtualization mode is being used on the server.</span></span> <span data-ttu-id="f7154-243">Può corrispondere a uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="f7154-243">This can be one of the following values.</span></span>

<dt>

<span id="Per-Session"></span><span id="per-session"></span><span id="PER-SESSION"></span>

<span data-ttu-id="f7154-244"><span id="Per-Session"></span><span id="per-session"></span><span id="PER-SESSION"></span>**Per sessione** (0)</span><span class="sxs-lookup"><span data-stu-id="f7154-244"><span id="Per-Session"></span><span id="per-session"></span><span id="PER-SESSION"></span>**Per-Session** (0)</span></span>


</dt> <dd>

<span data-ttu-id="f7154-245">La modalità di virtualizzazione IP è per sessione.</span><span class="sxs-lookup"><span data-stu-id="f7154-245">The IP virtualization mode is per-session.</span></span>

</dd> <dt>

<span id="Per-Program"></span><span id="per-program"></span><span id="PER-PROGRAM"></span>

<span data-ttu-id="f7154-246"><span id="Per-Program"></span><span id="per-program"></span><span id="PER-PROGRAM"></span>**Per programma** (1)</span><span class="sxs-lookup"><span data-stu-id="f7154-246"><span id="Per-Program"></span><span id="per-program"></span><span id="PER-PROGRAM"></span>**Per-Program** (1)</span></span>


</dt> <dd>

<span data-ttu-id="f7154-247">La modalità di virtualizzazione IP è per utente.</span><span class="sxs-lookup"><span data-stu-id="f7154-247">The IP virtualization mode is per-user.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f7154-248">**VirtualizeLoopbackAddressesEnabled**</span><span class="sxs-lookup"><span data-stu-id="f7154-248">**VirtualizeLoopbackAddressesEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7154-249">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f7154-249">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f7154-250">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f7154-250">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f7154-251">Specifica se è abilitata la virtualizzazione degli indirizzi di loopback.</span><span class="sxs-lookup"><span data-stu-id="f7154-251">Specifies whether loopback address virtualization is enabled.</span></span>

<span data-ttu-id="f7154-252">**Windows Server 2008 R2:** Questa proprietà non è disponibile prima di Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="f7154-252">**Windows Server 2008 R2:** This property is not available prior to Windows Server 2012.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="f7154-253"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="f7154-253"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="f7154-254">Non abilitato</span><span class="sxs-lookup"><span data-stu-id="f7154-254">Not enabled</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="f7154-255"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="f7154-255"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="f7154-256">Abilitato</span><span class="sxs-lookup"><span data-stu-id="f7154-256">Enabled</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f7154-257">Commenti</span><span class="sxs-lookup"><span data-stu-id="f7154-257">Remarks</span></span>

<span data-ttu-id="f7154-258">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="f7154-258">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="f7154-259">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="f7154-259">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="f7154-260">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="f7154-260">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="f7154-261">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="f7154-261">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="f7154-262">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f7154-262">Requirements</span></span>



| <span data-ttu-id="f7154-263">Requisito</span><span class="sxs-lookup"><span data-stu-id="f7154-263">Requirement</span></span> | <span data-ttu-id="f7154-264">Valore</span><span class="sxs-lookup"><span data-stu-id="f7154-264">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f7154-265">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f7154-265">Minimum supported client</span></span><br/> | <span data-ttu-id="f7154-266">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="f7154-266">None supported</span></span><br/>                                                               |
| <span data-ttu-id="f7154-267">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f7154-267">Minimum supported server</span></span><br/> | <span data-ttu-id="f7154-268">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f7154-268">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="f7154-269">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f7154-269">Namespace</span></span><br/>                | <span data-ttu-id="f7154-270">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="f7154-270">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="f7154-271">MOF</span><span class="sxs-lookup"><span data-stu-id="f7154-271">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f7154-272"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f7154-272"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="f7154-273">DLL</span><span class="sxs-lookup"><span data-stu-id="f7154-273">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f7154-274"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f7154-274"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



 

