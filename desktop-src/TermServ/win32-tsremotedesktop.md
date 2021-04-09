---
title: Classe Win32_TSRemoteDesktop
description: Descrive una connessione Desktop remoto disponibile tramite Desktop remoto Accesso Web (Accesso Web Desktop remoto).
ms.assetid: 40c7d8f1-cc45-4f0a-8c07-8215342ca02e
ms.tgt_platform: multiple
keywords:
- Classe Win32_TSRemoteDesktop Servizi Desktop remoto
- Classe Win32_TSRemoteDesktop Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_TSRemoteDesktop
- Win32_TSRemoteDesktop.Caption
- Win32_TSRemoteDesktop.Description
- Win32_TSRemoteDesktop.InstallDate
- Win32_TSRemoteDesktop.Name
- Win32_TSRemoteDesktop.Status
- Win32_TSRemoteDesktop.Alias
- Win32_TSRemoteDesktop.SecurityDescriptor
- Win32_TSRemoteDesktop.IconPath
- Win32_TSRemoteDesktop.IconIndex
- Win32_TSRemoteDesktop.IconContents
- Win32_TSRemoteDesktop.ShowInPortal
- Win32_TSRemoteDesktop.RDPFileContents
- Win32_TSRemoteDesktop.IsVmFarm
- Win32_TSRemoteDesktop.VmFarmSettings
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b3a23e63d5c79313933b7ce6951265a85740bc8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119111"
---
# <a name="win32_tsremotedesktop-class"></a><span data-ttu-id="61265-105">Win32 \_ TSRemoteDesktop (classe)</span><span class="sxs-lookup"><span data-stu-id="61265-105">Win32\_TSRemoteDesktop class</span></span>

<span data-ttu-id="61265-106">Descrive una connessione Desktop remoto disponibile tramite Desktop remoto Accesso Web (Accesso Web Desktop remoto).</span><span class="sxs-lookup"><span data-stu-id="61265-106">Describes a remote desktop connection that is available through Remote Desktop Web Access (RD Web Access).</span></span>

## <a name="syntax"></a><span data-ttu-id="61265-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="61265-107">Syntax</span></span>

``` syntax
class Win32_TSRemoteDesktop : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   Alias;
  string   SecurityDescriptor;
  string   IconPath;
  sint32   IconIndex;
  uint8    IconContents[];
  boolean  ShowInPortal;
  string   RDPFileContents;
  boolean  IsVmFarm;
  string   VmFarmSettings;
};
```

## <a name="members"></a><span data-ttu-id="61265-108">Members</span><span class="sxs-lookup"><span data-stu-id="61265-108">Members</span></span>

<span data-ttu-id="61265-109">La classe **Win32 \_ TSRemoteDesktop** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="61265-109">The **Win32\_TSRemoteDesktop** class has these types of members:</span></span>

-   [<span data-ttu-id="61265-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="61265-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="61265-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="61265-111">Properties</span></span>

<span data-ttu-id="61265-112">La classe **Win32 \_ TSRemoteDesktop** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="61265-112">The **Win32\_TSRemoteDesktop** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="61265-113">**Alias**</span><span class="sxs-lookup"><span data-stu-id="61265-113">**Alias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61265-114">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="61265-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="61265-115">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="61265-115">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="61265-116">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="61265-116">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="61265-117">Alias della connessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="61265-117">The alias of the remote desktop connection.</span></span>

</dd> <dt>

<span data-ttu-id="61265-118">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="61265-118">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61265-119">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="61265-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="61265-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="61265-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="61265-121">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="61265-121">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="61265-122">Breve descrizione (stringa a una riga) dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="61265-122">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="61265-123">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="61265-123">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="61265-124">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="61265-124">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61265-125">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="61265-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="61265-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="61265-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61265-127">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="61265-127">Description of the object.</span></span>

<span data-ttu-id="61265-128">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="61265-128">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="61265-129">**IconContents**</span><span class="sxs-lookup"><span data-stu-id="61265-129">**IconContents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61265-130">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="61265-130">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="61265-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="61265-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61265-132">Contenuto byte dell'icona che corrisponde alla connessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="61265-132">The byte contents of the icon that corresponds to the remote desktop connection.</span></span>

</dd> <dt>

<span data-ttu-id="61265-133">**IconIndex**</span><span class="sxs-lookup"><span data-stu-id="61265-133">**IconIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61265-134">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="61265-134">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="61265-135">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="61265-135">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="61265-136">Indice o ID dell'icona per la connessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="61265-136">The index or ID of the icon for the remote desktop connection.</span></span>

</dd> <dt>

<span data-ttu-id="61265-137">**IconPath**</span><span class="sxs-lookup"><span data-stu-id="61265-137">**IconPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61265-138">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="61265-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="61265-139">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="61265-139">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="61265-140">Percorso dell'icona per la connessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="61265-140">Path of the icon for the remote desktop connection.</span></span>

</dd> <dt>

<span data-ttu-id="61265-141">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="61265-141">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61265-142">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="61265-142">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="61265-143">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="61265-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="61265-144">Qualificatori: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="61265-144">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="61265-145">Data di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="61265-145">The date the object was installed.</span></span> <span data-ttu-id="61265-146">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="61265-146">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="61265-147">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="61265-147">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="61265-148">**IsVmFarm**</span><span class="sxs-lookup"><span data-stu-id="61265-148">**IsVmFarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61265-149">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="61265-149">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="61265-150">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="61265-150">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="61265-151">Indica se questa connessione Desktop remoto fa parte di una farm di macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="61265-151">Indicates if this remote desktop connection is part of a virtual machine farm.</span></span>

</dd> <dt>

<span data-ttu-id="61265-152">**Nome**</span><span class="sxs-lookup"><span data-stu-id="61265-152">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61265-153">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="61265-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="61265-154">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="61265-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61265-155">Nome dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="61265-155">The name of the object.</span></span>

<span data-ttu-id="61265-156">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="61265-156">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="61265-157">**RDPFileContents**</span><span class="sxs-lookup"><span data-stu-id="61265-157">**RDPFileContents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61265-158">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="61265-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="61265-159">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="61265-159">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="61265-160">Contenuto del file RDP che corrisponde alla connessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="61265-160">Contents of the RDP file that correspond to the remote desktop connection.</span></span>

</dd> <dt>

<span data-ttu-id="61265-161">**SecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="61265-161">**SecurityDescriptor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61265-162">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="61265-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="61265-163">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="61265-163">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="61265-164">Descrittore di sicurezza che controlla l'accesso alla connessione Desktop remoto, in formato SDDL.</span><span class="sxs-lookup"><span data-stu-id="61265-164">A security descriptor that controls access to the remote desktop connection, in SDDL format.</span></span> <span data-ttu-id="61265-165">Una stringa vuota implica l'autorizzazione All Access.</span><span class="sxs-lookup"><span data-stu-id="61265-165">An empty string implies allow all access.</span></span> <span data-ttu-id="61265-166">Questo descrittore di sicurezza non supporta Ace DENY o ACE che fanno riferimento a utenti o gruppi non di dominio.</span><span class="sxs-lookup"><span data-stu-id="61265-166">This security descriptor does not support DENY ACEs, or ACEs that refer to nondomain users or groups.</span></span>

</dd> <dt>

<span data-ttu-id="61265-167">**ShowInPortal**</span><span class="sxs-lookup"><span data-stu-id="61265-167">**ShowInPortal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61265-168">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="61265-168">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="61265-169">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="61265-169">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="61265-170">Indica se la connessione Desktop remoto deve essere visualizzata in Accesso Web Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="61265-170">Indicates whether the remote desktop connection should be shown in RD Web Access.</span></span>

</dd> <dt>

<span data-ttu-id="61265-171">**Status**</span><span class="sxs-lookup"><span data-stu-id="61265-171">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61265-172">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="61265-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="61265-173">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="61265-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="61265-174">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="61265-174">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="61265-175">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="61265-175">Current status of the object.</span></span> <span data-ttu-id="61265-176">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="61265-176">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="61265-177">Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro).</span><span class="sxs-lookup"><span data-stu-id="61265-177">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="61265-178">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="61265-178">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="61265-179">Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="61265-179">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="61265-180">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="61265-180">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="61265-181">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="61265-181">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="61265-182">("OK")</span><span class="sxs-lookup"><span data-stu-id="61265-182">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="61265-183">("Errore")</span><span class="sxs-lookup"><span data-stu-id="61265-183">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="61265-184">("Danneggiato")</span><span class="sxs-lookup"><span data-stu-id="61265-184">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="61265-185">("Sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="61265-185">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="61265-186">("Errore di predazione")</span><span class="sxs-lookup"><span data-stu-id="61265-186">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="61265-187">("Avvio")</span><span class="sxs-lookup"><span data-stu-id="61265-187">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="61265-188">("Arresto")</span><span class="sxs-lookup"><span data-stu-id="61265-188">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="61265-189">("Servizio")</span><span class="sxs-lookup"><span data-stu-id="61265-189">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="61265-190">**VmFarmSettings**</span><span class="sxs-lookup"><span data-stu-id="61265-190">**VmFarmSettings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61265-191">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="61265-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="61265-192">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="61265-192">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="61265-193">Impostazioni della farm della macchina virtuale per la connessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="61265-193">Virtual machine farm settings for the remote desktop connection.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="61265-194">Commenti</span><span class="sxs-lookup"><span data-stu-id="61265-194">Remarks</span></span>

<span data-ttu-id="61265-195">Per impostare le proprietà tramite questa classe, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="61265-195">You must be a member of the Administrators group to set properties by using this class.</span></span>

<span data-ttu-id="61265-196">Per connettersi allo \\ \\ \\ spazio dei nomi CIMV2 TerminalServices radice, il livello di autenticazione deve includere la riservatezza dei pacchetti.</span><span class="sxs-lookup"><span data-stu-id="61265-196">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="61265-197">Per le chiamate C/C++, si tratta di un livello di autenticazione del livello di autenticazione **RPC \_ C \_ \_ \_ PKT \_**, che può essere impostato tramite la funzione com [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) .</span><span class="sxs-lookup"><span data-stu-id="61265-197">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**, which can be set by using the [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) COM function.</span></span> <span data-ttu-id="61265-198">Per Visual Basic e le chiamate di scripting, si tratta di un livello di autenticazione di **WbemAuthenticationLevelPktPrivacy** o "su PktPrivacy", con un valore pari a 6.</span><span class="sxs-lookup"><span data-stu-id="61265-198">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="61265-199">Il seguente esempio di Visual Basic Scripting Edition (VBScript) illustra come connettersi a un computer remoto con la privacy dei pacchetti.</span><span class="sxs-lookup"><span data-stu-id="61265-199">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="61265-200">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="61265-200">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="61265-201">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="61265-201">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="61265-202">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="61265-202">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="61265-203">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="61265-203">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="61265-204">Requisiti</span><span class="sxs-lookup"><span data-stu-id="61265-204">Requirements</span></span>



| <span data-ttu-id="61265-205">Requisito</span><span class="sxs-lookup"><span data-stu-id="61265-205">Requirement</span></span> | <span data-ttu-id="61265-206">Valore</span><span class="sxs-lookup"><span data-stu-id="61265-206">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="61265-207">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="61265-207">Minimum supported client</span></span><br/> | <span data-ttu-id="61265-208">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="61265-208">None supported</span></span><br/>                                                               |
| <span data-ttu-id="61265-209">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="61265-209">Minimum supported server</span></span><br/> | <span data-ttu-id="61265-210">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="61265-210">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="61265-211">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="61265-211">Namespace</span></span><br/>                | <span data-ttu-id="61265-212">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="61265-212">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="61265-213">MOF</span><span class="sxs-lookup"><span data-stu-id="61265-213">MOF</span></span><br/>                      | <dl> <span data-ttu-id="61265-214"><dt>Tsallow. mof</dt></span><span class="sxs-lookup"><span data-stu-id="61265-214"><dt>Tsallow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="61265-215">DLL</span><span class="sxs-lookup"><span data-stu-id="61265-215">DLL</span></span><br/>                      | <dl> <span data-ttu-id="61265-216"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="61265-216"><dt>TsPubWmi.dll</dt></span></span> </dl> |



 

