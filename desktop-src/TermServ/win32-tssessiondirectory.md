---
title: Classe Win32_TSSessionDirectory
description: Definisce le impostazioni di configurazione di Connessione Desktop remoto broker (gestore connessione Desktop remoto) per la \_ classe Win32 TSSessionDirectorySetting.
ms.assetid: ef9042c2-4a35-49e9-b195-fb37c0919068
ms.tgt_platform: multiple
keywords:
- Classe Win32_TSSessionDirectory Servizi Desktop remoto
- Classe Win32_TSSessionDirectory Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory
- Win32_TSSessionDirectory.Caption
- Win32_TSSessionDirectory.Description
- Win32_TSSessionDirectory.InstallDate
- Win32_TSSessionDirectory.Name
- Win32_TSSessionDirectory.Status
- Win32_TSSessionDirectory.SessionDirectoryLocation
- Win32_TSSessionDirectory.PolicySourceSessionDirectoryLocation
- Win32_TSSessionDirectory.SessionDirectoryActive
- Win32_TSSessionDirectory.PolicySourceSessionDirectoryActive
- Win32_TSSessionDirectory.SessionDirectoryExposeServerIP
- Win32_TSSessionDirectory.PolicySourceSessionDirectoryExposeServerIP
- Win32_TSSessionDirectory.SessionDirectoryClusterName
- Win32_TSSessionDirectory.PolicySourceLoadBalancing
- Win32_TSSessionDirectory.GetLoadBalancingState
- Win32_TSSessionDirectory.GetServerWeight
- Win32_TSSessionDirectory.PolicySourceSessionDirectoryClusterName
- Win32_TSSessionDirectory.SessionDirectoryIPAddress
- Win32_TSSessionDirectory.GetTSRedirectorMode
- Win32_TSSessionDirectory.PolicySourceTSRedirectorMode
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb50ed77b99f415ae551dfcf69655af5c1d77501
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964072"
---
# <a name="win32_tssessiondirectory-class"></a><span data-ttu-id="0a89b-105">Win32 \_ TSSessionDirectory (classe)</span><span class="sxs-lookup"><span data-stu-id="0a89b-105">Win32\_TSSessionDirectory class</span></span>

<span data-ttu-id="0a89b-106">Definisce le impostazioni di configurazione di Connessione Desktop remoto broker (gestore connessione Desktop remoto) per la classe [**Win32 \_ TSSessionDirectorySetting**](win32-tssessiondirectorysetting.md) .</span><span class="sxs-lookup"><span data-stu-id="0a89b-106">Defines the Remote Desktop Connection Broker (RD Connection Broker) configuration settings for the [**Win32\_TSSessionDirectorySetting**](win32-tssessiondirectorysetting.md) class.</span></span>

> [!Note]  
> <span data-ttu-id="0a89b-107">In Windows Server 2008 R2 il nome di gestore sessioni Servizi terminal è stato modificato in Gestore connessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="0a89b-107">In Windows Server 2008 R2, the name of Terminal Services Session Broker (TS Session Broker) was changed to RD Connection Broker.</span></span> <span data-ttu-id="0a89b-108">Queste proprietà si applicano a tutti i sistemi operativi supportati se non diversamente specificato.</span><span class="sxs-lookup"><span data-stu-id="0a89b-108">These properties apply to all supported operating systems unless otherwise noted.</span></span>

 

<span data-ttu-id="0a89b-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà definite ed ereditate, in ordine alfabetico.</span><span class="sxs-lookup"><span data-stu-id="0a89b-109">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span> <span data-ttu-id="0a89b-110">Per informazioni di riferimento sui metodi, vedere la tabella dei metodi più avanti in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="0a89b-110">For reference information about methods, see the table of methods later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a89b-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0a89b-111">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TSSESSIONDIRECTORY_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer"), AMENDMENT]
class Win32_TSSessionDirectory : CIM_Setting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   SessionDirectoryLocation;
  uint32   PolicySourceSessionDirectoryLocation;
  uint32   SessionDirectoryActive;
  uint32   PolicySourceSessionDirectoryActive;
  uint32   SessionDirectoryExposeServerIP;
  uint32   PolicySourceSessionDirectoryExposeServerIP;
  string   SessionDirectoryClusterName;
  uint32   PolicySourceLoadBalancing;
  uint32   GetLoadBalancingState;
  uint32   GetServerWeight;
  uint32   PolicySourceSessionDirectoryClusterName;
  string   SessionDirectoryIPAddress;
  uint32   GetTSRedirectorMode;
  uint32   PolicySourceTSRedirectorMode;
};
```

## <a name="members"></a><span data-ttu-id="0a89b-112">Members</span><span class="sxs-lookup"><span data-stu-id="0a89b-112">Members</span></span>

<span data-ttu-id="0a89b-113">La classe **Win32 \_ TSSessionDirectory** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="0a89b-113">The **Win32\_TSSessionDirectory** class has these types of members:</span></span>

-   [<span data-ttu-id="0a89b-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="0a89b-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="0a89b-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0a89b-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="0a89b-116">Metodi</span><span class="sxs-lookup"><span data-stu-id="0a89b-116">Methods</span></span>

<span data-ttu-id="0a89b-117">La classe **Win32 \_ TSSessionDirectory** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="0a89b-117">The **Win32\_TSSessionDirectory** class has these methods.</span></span>



| <span data-ttu-id="0a89b-118">Metodo</span><span class="sxs-lookup"><span data-stu-id="0a89b-118">Method</span></span>                                                                                                  | <span data-ttu-id="0a89b-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0a89b-119">Description</span></span>                                                                                                  |
|:--------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0a89b-120">**CreateUserDiskTemplate**</span><span class="sxs-lookup"><span data-stu-id="0a89b-120">**CreateUserDiskTemplate**</span></span>](createuserdisktemplate-win32-tssessiondirectory.md)                       | <span data-ttu-id="0a89b-121">Crea un modello di disco utente.</span><span class="sxs-lookup"><span data-stu-id="0a89b-121">Creates a user disk template.</span></span><br/>                                                                     |
| [<span data-ttu-id="0a89b-122">**DisableUserVhd**</span><span class="sxs-lookup"><span data-stu-id="0a89b-122">**DisableUserVhd**</span></span>](disableuservhd-win32-tssessiondirectory.md)                                       | <span data-ttu-id="0a89b-123">Disabilita un disco rigido virtuale del profilo utente.</span><span class="sxs-lookup"><span data-stu-id="0a89b-123">Disables a user profile VHD.</span></span><br/>                                                                      |
| [<span data-ttu-id="0a89b-124">**EnableUserVhd**</span><span class="sxs-lookup"><span data-stu-id="0a89b-124">**EnableUserVhd**</span></span>](enableuservhd-win32-tssessiondirectory.md)                                         | <span data-ttu-id="0a89b-125">Abilita un VHD del profilo utente in un server RDSH.</span><span class="sxs-lookup"><span data-stu-id="0a89b-125">Enables a user profile VHD on an RDSH server.</span></span><br/>                                                     |
| [<span data-ttu-id="0a89b-126">**GetCurrentRedirectableAddresses**</span><span class="sxs-lookup"><span data-stu-id="0a89b-126">**GetCurrentRedirectableAddresses**</span></span>](getcurrentredirectableaddresses-win32-tssessiondirectory.md)     | <span data-ttu-id="0a89b-127">Ottiene l'elenco attualmente configurato di indirizzi DNS idonei e il tipo di reindirizzamento.</span><span class="sxs-lookup"><span data-stu-id="0a89b-127">Obtains the currently configured list of DNS eligible addresses, and the redirection type.</span></span><br/>        |
| [<span data-ttu-id="0a89b-128">**GetRedirectableAddresses**</span><span class="sxs-lookup"><span data-stu-id="0a89b-128">**GetRedirectableAddresses**</span></span>](getredirectableaddresses-win32-tssessiondirectory.md)                   | <span data-ttu-id="0a89b-129">Ottiene l'intero elenco di indirizzi DNS idonei.</span><span class="sxs-lookup"><span data-stu-id="0a89b-129">Obtains the entire list of DNS eligible addresses.</span></span><br/>                                                |
| [<span data-ttu-id="0a89b-130">**PingSessionDirectory**</span><span class="sxs-lookup"><span data-stu-id="0a89b-130">**PingSessionDirectory**</span></span>](pingsessiondirectory-win32-tssessiondirectory.md)                           | <span data-ttu-id="0a89b-131">Verifica se il server Gestore connessione Desktop remoto è disponibile.</span><span class="sxs-lookup"><span data-stu-id="0a89b-131">Checks whether the RD Connection Broker server is available.</span></span><br/>                                      |
| [<span data-ttu-id="0a89b-132">**SetCurrentRedirectableAddresses**</span><span class="sxs-lookup"><span data-stu-id="0a89b-132">**SetCurrentRedirectableAddresses**</span></span>](setcurrentredirectableaddresses-win32-tssessiondirectory.md)     | <span data-ttu-id="0a89b-133">Imposta l'elenco configurato di indirizzi DNS idonei e il tipo di reindirizzamento.</span><span class="sxs-lookup"><span data-stu-id="0a89b-133">Sets the configured list of DNS eligible addresses, and the redirection type.</span></span><br/>                     |
| [<span data-ttu-id="0a89b-134">**SetLoadBalancingState**</span><span class="sxs-lookup"><span data-stu-id="0a89b-134">**SetLoadBalancingState**</span></span>](setloadbalancingstate-win32-tssessiondirectory.md)                         | <span data-ttu-id="0a89b-135">Imposta il valore per indicare se il server parteciperà al bilanciamento del carico di gestore connessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="0a89b-135">Sets the value to indicate if the server will participate in RD Connection Broker load balancing.</span></span><br/> |
| [<span data-ttu-id="0a89b-136">**SetServerWeight**</span><span class="sxs-lookup"><span data-stu-id="0a89b-136">**SetServerWeight**</span></span>](setserverweight-win32-tssessiondirectory.md)                                     | <span data-ttu-id="0a89b-137">Imposta il valore del peso del server per il bilanciamento del carico di gestore connessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="0a89b-137">Sets the server weight value for RD Connection Broker load balancing.</span></span><br/>                             |
| [<span data-ttu-id="0a89b-138">**SetSessionDirectoryActive**</span><span class="sxs-lookup"><span data-stu-id="0a89b-138">**SetSessionDirectoryActive**</span></span>](win32-tssessiondirectory-setsessiondirectoryactive.md)                 | <span data-ttu-id="0a89b-139">Disabilita e Abilita il gestore connessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="0a89b-139">Disables and enables the RD Connection Broker.</span></span><br/>                                                    |
| [<span data-ttu-id="0a89b-140">**SetSessionDirectoryExposeServerIP**</span><span class="sxs-lookup"><span data-stu-id="0a89b-140">**SetSessionDirectoryExposeServerIP**</span></span>](win32-tssessiondirectory-setsessiondirectoryexposeserverip.md) | <span data-ttu-id="0a89b-141">Imposta la proprietà **SessionDirectoryExposeServerIP** .</span><span class="sxs-lookup"><span data-stu-id="0a89b-141">Sets the **SessionDirectoryExposeServerIP** property.</span></span><br/>                                             |
| [<span data-ttu-id="0a89b-142">**SetSessionDirectoryProperty**</span><span class="sxs-lookup"><span data-stu-id="0a89b-142">**SetSessionDirectoryProperty**</span></span>](win32-tssessiondirectory-setsessiondirectoryproperty.md)             | <span data-ttu-id="0a89b-143">Imposta la proprietà **SessionDirectoryLocation** o la proprietà **SessionDirectoryClusterName** .</span><span class="sxs-lookup"><span data-stu-id="0a89b-143">Sets the **SessionDirectoryLocation** property or the **SessionDirectoryClusterName** property.</span></span><br/>   |
| [<span data-ttu-id="0a89b-144">**SetTSRedirectorMode**</span><span class="sxs-lookup"><span data-stu-id="0a89b-144">**SetTSRedirectorMode**</span></span>](settsredirectormode-win32-tssessiondirectory.md)                             | <span data-ttu-id="0a89b-145">Questo metodo non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="0a89b-145">This method is not available.</span></span><br/>                                                                     |



 

### <a name="properties"></a><span data-ttu-id="0a89b-146">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0a89b-146">Properties</span></span>

<span data-ttu-id="0a89b-147">La classe **Win32 \_ TSSessionDirectory** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="0a89b-147">The **Win32\_TSSessionDirectory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0a89b-148">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="0a89b-148">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a89b-149">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0a89b-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0a89b-150">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0a89b-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0a89b-151">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="0a89b-151">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="0a89b-152">Breve descrizione (stringa a una riga) dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="0a89b-152">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="0a89b-153">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0a89b-153">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0a89b-154">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="0a89b-154">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a89b-155">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0a89b-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0a89b-156">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0a89b-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0a89b-157">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="0a89b-157">Description of the object.</span></span>

<span data-ttu-id="0a89b-158">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0a89b-158">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0a89b-159">**GetLoadBalancingState**</span><span class="sxs-lookup"><span data-stu-id="0a89b-159">**GetLoadBalancingState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a89b-160">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0a89b-160">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0a89b-161">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0a89b-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0a89b-162">Indica se il server è configurato per partecipare al bilanciamento del carico di gestore connessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="0a89b-162">Indicates if the server is configured to participate in RD Connection Broker load balancing.</span></span>

<dt>

<span data-ttu-id="0a89b-163">0</span><span class="sxs-lookup"><span data-stu-id="0a89b-163">0</span></span>
</dt> <dd>

<span data-ttu-id="0a89b-164">Il server non è configurato per partecipare al bilanciamento del carico di gestore connessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="0a89b-164">The server is not configured to participate in RD Connection Broker load balancing.</span></span>

</dd> <dt>

<span data-ttu-id="0a89b-165">1</span><span class="sxs-lookup"><span data-stu-id="0a89b-165">1</span></span>
</dt> <dd>

<span data-ttu-id="0a89b-166">Il server è configurato per partecipare al bilanciamento del carico di gestore connessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="0a89b-166">The server is configured to participate in RD Connection Broker load balancing.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0a89b-167">**GetServerWeight**</span><span class="sxs-lookup"><span data-stu-id="0a89b-167">**GetServerWeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a89b-168">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0a89b-168">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0a89b-169">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0a89b-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0a89b-170">Recupera il valore del peso del server utilizzato nel bilanciamento del carico di gestore connessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="0a89b-170">Retrieves the server weight value that is used in RD Connection Broker load balancing.</span></span>

</dd> <dt>

<span data-ttu-id="0a89b-171">**GetTSRedirectorMode**</span><span class="sxs-lookup"><span data-stu-id="0a89b-171">**GetTSRedirectorMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a89b-172">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0a89b-172">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0a89b-173">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0a89b-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0a89b-174">Indica se il server è configurato per fungere da redirector Servizi Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="0a89b-174">Indicates if the server is configured to act as a Remote Desktop Services redirector.</span></span>

<dt>

<span data-ttu-id="0a89b-175">0</span><span class="sxs-lookup"><span data-stu-id="0a89b-175">0</span></span>
</dt> <dd>

<span data-ttu-id="0a89b-176">Il server è configurato per fungere da redirector Servizi Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="0a89b-176">The server is configured to act as a Remote Desktop Services redirector.</span></span>

</dd> <dt>

<span data-ttu-id="0a89b-177">1</span><span class="sxs-lookup"><span data-stu-id="0a89b-177">1</span></span>
</dt> <dd>

<span data-ttu-id="0a89b-178">Il server non è configurato per fungere da redirector Servizi Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="0a89b-178">The server is not configured to act as a Remote Desktop Services redirector.</span></span>

</dd> </dl>

<span data-ttu-id="0a89b-179">**Windows Server 2008:** Questa proprietà non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="0a89b-179">**Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="0a89b-180">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="0a89b-180">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a89b-181">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="0a89b-181">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0a89b-182">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0a89b-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0a89b-183">Qualificatori: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="0a89b-183">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="0a89b-184">Data di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="0a89b-184">The date the object was installed.</span></span> <span data-ttu-id="0a89b-185">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="0a89b-185">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="0a89b-186">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0a89b-186">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0a89b-187">**Nome**</span><span class="sxs-lookup"><span data-stu-id="0a89b-187">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a89b-188">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0a89b-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0a89b-189">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0a89b-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0a89b-190">Nome dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="0a89b-190">The name of the object.</span></span>

<span data-ttu-id="0a89b-191">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0a89b-191">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0a89b-192">**PolicySourceLoadBalancing**</span><span class="sxs-lookup"><span data-stu-id="0a89b-192">**PolicySourceLoadBalancing**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a89b-193">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0a89b-193">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0a89b-194">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0a89b-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0a89b-195">Indica se la proprietà **GetLoadBalancingState** è configurata dal server o da criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="0a89b-195">Indicates if the **GetLoadBalancingState** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="0a89b-196">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="0a89b-196">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="0a89b-197">Server</span><span class="sxs-lookup"><span data-stu-id="0a89b-197">Server</span></span>

</dd> <dt>

<span data-ttu-id="0a89b-198">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="0a89b-198">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="0a89b-199">Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="0a89b-199">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0a89b-200">**PolicySourceSessionDirectoryActive**</span><span class="sxs-lookup"><span data-stu-id="0a89b-200">**PolicySourceSessionDirectoryActive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a89b-201">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0a89b-201">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0a89b-202">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0a89b-202">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0a89b-203">Indica se la proprietà **SessionDirectoryActive** è configurata dal server o da criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="0a89b-203">Indicates if the **SessionDirectoryActive** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="0a89b-204">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="0a89b-204">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="0a89b-205">Server</span><span class="sxs-lookup"><span data-stu-id="0a89b-205">Server</span></span>

</dd> <dt>

<span data-ttu-id="0a89b-206">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="0a89b-206">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="0a89b-207">Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="0a89b-207">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0a89b-208">**PolicySourceSessionDirectoryClusterName**</span><span class="sxs-lookup"><span data-stu-id="0a89b-208">**PolicySourceSessionDirectoryClusterName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a89b-209">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0a89b-209">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0a89b-210">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0a89b-210">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0a89b-211">Indica se la proprietà **SessionDirectoryClusterName** è configurata dal server o da criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="0a89b-211">Indicates if the **SessionDirectoryClusterName** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="0a89b-212">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="0a89b-212">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="0a89b-213">Server</span><span class="sxs-lookup"><span data-stu-id="0a89b-213">Server</span></span>

</dd> <dt>

<span data-ttu-id="0a89b-214">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="0a89b-214">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="0a89b-215">Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="0a89b-215">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0a89b-216">**PolicySourceSessionDirectoryExposeServerIP**</span><span class="sxs-lookup"><span data-stu-id="0a89b-216">**PolicySourceSessionDirectoryExposeServerIP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a89b-217">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0a89b-217">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0a89b-218">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0a89b-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0a89b-219">Indica se la proprietà **SessionDirectoryExposeServerIP** è configurata dal server o da criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="0a89b-219">Indicates if the **SessionDirectoryExposeServerIP** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="0a89b-220">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="0a89b-220">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="0a89b-221">Server</span><span class="sxs-lookup"><span data-stu-id="0a89b-221">Server</span></span>

</dd> <dt>

<span data-ttu-id="0a89b-222">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="0a89b-222">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="0a89b-223">Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="0a89b-223">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0a89b-224">**PolicySourceSessionDirectoryLocation**</span><span class="sxs-lookup"><span data-stu-id="0a89b-224">**PolicySourceSessionDirectoryLocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a89b-225">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0a89b-225">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0a89b-226">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0a89b-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0a89b-227">Indica se la proprietà **SessionDirectoryLocation** è configurata dal server o da criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="0a89b-227">Indicates if the **SessionDirectoryLocation** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="0a89b-228">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="0a89b-228">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="0a89b-229">Server</span><span class="sxs-lookup"><span data-stu-id="0a89b-229">Server</span></span>

</dd> <dt>

<span data-ttu-id="0a89b-230">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="0a89b-230">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="0a89b-231">Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="0a89b-231">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0a89b-232">**PolicySourceTSRedirectorMode**</span><span class="sxs-lookup"><span data-stu-id="0a89b-232">**PolicySourceTSRedirectorMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a89b-233">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0a89b-233">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0a89b-234">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0a89b-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0a89b-235">Questa proprietà non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="0a89b-235">This property is not available.</span></span>

<span data-ttu-id="0a89b-236">**Windows Server 2008 R2:** Indica se la proprietà **GetTSRedirectorMode** è configurata dal server o da criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="0a89b-236">**Windows Server 2008 R2:** Indicates if the **GetTSRedirectorMode** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="0a89b-237">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="0a89b-237">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="0a89b-238">Server</span><span class="sxs-lookup"><span data-stu-id="0a89b-238">Server</span></span>

</dd> <dt>

<span data-ttu-id="0a89b-239">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="0a89b-239">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="0a89b-240">Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="0a89b-240">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0a89b-241">**SessionDirectoryActive**</span><span class="sxs-lookup"><span data-stu-id="0a89b-241">**SessionDirectoryActive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a89b-242">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0a89b-242">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0a89b-243">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0a89b-243">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0a89b-244">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0a89b-244">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="0a89b-245">Specifica se Servizi Desktop remoto partecipa al gestore connessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="0a89b-245">Specifies if Remote Desktop Services participates in the RD Connection Broker.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="0a89b-246"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="0a89b-246"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="0a89b-247">Servizi Desktop remoto partecipazione al gestore connessione Desktop remoto è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="0a89b-247">Remote Desktop Services participation in the RD Connection Broker is disabled.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="0a89b-248"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="0a89b-248"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="0a89b-249">Servizi Desktop remoto la partecipazione al gestore connessione Desktop remoto è abilitata.</span><span class="sxs-lookup"><span data-stu-id="0a89b-249">Remote Desktop Services participation in the RD Connection Broker is enabled.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0a89b-250">**SessionDirectoryClusterName**</span><span class="sxs-lookup"><span data-stu-id="0a89b-250">**SessionDirectoryClusterName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a89b-251">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0a89b-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0a89b-252">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0a89b-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0a89b-253">Indirizzo IP virtuale del cluster a cui appartiene il server Host sessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="0a89b-253">The virtual IP address of the cluster to which the RD Session Host server belongs.</span></span>

</dd> <dt>

<span data-ttu-id="0a89b-254">**SessionDirectoryExposeServerIP**</span><span class="sxs-lookup"><span data-stu-id="0a89b-254">**SessionDirectoryExposeServerIP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a89b-255">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0a89b-255">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0a89b-256">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0a89b-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0a89b-257">Specifica se è consentito il recupero dell'indirizzo IP del gestore connessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="0a89b-257">Specifies if retrieval of the IP address of the RD Connection Broker is allowed.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="0a89b-258"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="0a89b-258"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="0a89b-259">Recupero negato.</span><span class="sxs-lookup"><span data-stu-id="0a89b-259">Retrieval is denied.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="0a89b-260"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="0a89b-260"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="0a89b-261">Il recupero è consentito.</span><span class="sxs-lookup"><span data-stu-id="0a89b-261">Retrieval is allowed.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0a89b-262">**SessionDirectoryIPAddress**</span><span class="sxs-lookup"><span data-stu-id="0a89b-262">**SessionDirectoryIPAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a89b-263">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0a89b-263">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0a89b-264">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="0a89b-264">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0a89b-265">Indirizzo IP della scheda LAN utilizzata dalla directory di sessione.</span><span class="sxs-lookup"><span data-stu-id="0a89b-265">The IP address of the LAN adapter used by the session directory.</span></span>

</dd> <dt>

<span data-ttu-id="0a89b-266">**SessionDirectoryLocation**</span><span class="sxs-lookup"><span data-stu-id="0a89b-266">**SessionDirectoryLocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a89b-267">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0a89b-267">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0a89b-268">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0a89b-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0a89b-269">Nome DNS di rete o indirizzo IP del server in cui è in esecuzione il servizio Gestore connessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="0a89b-269">The network DNS name or IP address of the server where the RD Connection Broker service is running.</span></span>

</dd> <dt>

<span data-ttu-id="0a89b-270">**Status**</span><span class="sxs-lookup"><span data-stu-id="0a89b-270">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a89b-271">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0a89b-271">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0a89b-272">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0a89b-272">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0a89b-273">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="0a89b-273">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="0a89b-274">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="0a89b-274">Current status of the object.</span></span> <span data-ttu-id="0a89b-275">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="0a89b-275">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="0a89b-276">Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro).</span><span class="sxs-lookup"><span data-stu-id="0a89b-276">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="0a89b-277">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="0a89b-277">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="0a89b-278">Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="0a89b-278">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="0a89b-279">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="0a89b-279">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="0a89b-280">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0a89b-280">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="0a89b-281">("OK")</span><span class="sxs-lookup"><span data-stu-id="0a89b-281">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0a89b-282">("Errore")</span><span class="sxs-lookup"><span data-stu-id="0a89b-282">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0a89b-283">("Danneggiato")</span><span class="sxs-lookup"><span data-stu-id="0a89b-283">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0a89b-284">("Sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="0a89b-284">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0a89b-285">("Errore di predazione")</span><span class="sxs-lookup"><span data-stu-id="0a89b-285">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0a89b-286">("Avvio")</span><span class="sxs-lookup"><span data-stu-id="0a89b-286">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0a89b-287">("Arresto")</span><span class="sxs-lookup"><span data-stu-id="0a89b-287">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0a89b-288">("Servizio")</span><span class="sxs-lookup"><span data-stu-id="0a89b-288">("Service")</span></span>


<span data-ttu-id="0a89b-289"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="0a89b-289"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="0a89b-290">Commenti</span><span class="sxs-lookup"><span data-stu-id="0a89b-290">Remarks</span></span>

<span data-ttu-id="0a89b-291">Per connettersi allo \\ \\ \\ \\ spazio dei nomi CIMV2 TerminalServices radice, il livello di autenticazione deve includere la riservatezza dei pacchetti.</span><span class="sxs-lookup"><span data-stu-id="0a89b-291">To connect to the \\\\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="0a89b-292">Per le chiamate C/C++, si tratta di un livello di autenticazione del livello di autenticazione **RPC \_ C \_ \_ \_ PKT \_ privacy**.</span><span class="sxs-lookup"><span data-stu-id="0a89b-292">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="0a89b-293">Per Visual Basic e le chiamate di scripting, si tratta di un livello di autenticazione di **WbemAuthenticationLevelPktPrivacy** o "su PktPrivacy", con un valore di sei.</span><span class="sxs-lookup"><span data-stu-id="0a89b-293">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of six.</span></span>

<span data-ttu-id="0a89b-294">Il seguente esempio di Visual Basic Scripting Edition (VBScript) illustra come connettersi a un computer remoto con la privacy dei pacchetti.</span><span class="sxs-lookup"><span data-stu-id="0a89b-294">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="0a89b-295">In Windows Server 2008, il nome della funzionalità directory di sessione di Servizi terminal è stato modificato in Gestore sessioni Servizi terminal.</span><span class="sxs-lookup"><span data-stu-id="0a89b-295">In Windows Server 2008, the name of the Terminal Services Session Directory feature was changed to Terminal Services Session Broker.</span></span>

<span data-ttu-id="0a89b-296">In Windows Server 2008 R2 il nome della funzionalità gestore sessioni Servizi terminal è stato modificato in Connessione Desktop remoto broker.</span><span class="sxs-lookup"><span data-stu-id="0a89b-296">In Windows Server 2008 R2, the name of the Terminal Services Session Broker feature was changed to Remote Desktop Connection Broker.</span></span>

<span data-ttu-id="0a89b-297">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="0a89b-297">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="0a89b-298">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="0a89b-298">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="0a89b-299">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="0a89b-299">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="0a89b-300">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="0a89b-300">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="0a89b-301">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0a89b-301">Requirements</span></span>



| <span data-ttu-id="0a89b-302">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a89b-302">Requirement</span></span> | <span data-ttu-id="0a89b-303">Valore</span><span class="sxs-lookup"><span data-stu-id="0a89b-303">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0a89b-304">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0a89b-304">Minimum supported client</span></span><br/> | <span data-ttu-id="0a89b-305">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="0a89b-305">None supported</span></span><br/>                                                               |
| <span data-ttu-id="0a89b-306">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0a89b-306">Minimum supported server</span></span><br/> | <span data-ttu-id="0a89b-307">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0a89b-307">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0a89b-308">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="0a89b-308">Namespace</span></span><br/>                | <span data-ttu-id="0a89b-309">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="0a89b-309">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="0a89b-310">MOF</span><span class="sxs-lookup"><span data-stu-id="0a89b-310">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0a89b-311"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0a89b-311"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="0a89b-312">DLL</span><span class="sxs-lookup"><span data-stu-id="0a89b-312">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0a89b-313"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0a89b-313"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a89b-314">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0a89b-314">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a89b-315">**\_Impostazione CIM**</span><span class="sxs-lookup"><span data-stu-id="0a89b-315">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

[<span data-ttu-id="0a89b-316">**\_TSSessionDirectorySetting Win32**</span><span class="sxs-lookup"><span data-stu-id="0a89b-316">**Win32\_TSSessionDirectorySetting**</span></span>](win32-tssessiondirectorysetting.md)
</dt> </dl>

 

