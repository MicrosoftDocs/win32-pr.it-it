---
description: Rappresenta il Trusted Platform Module (TPM), un chip di sicurezza hardware che fornisce una radice di attendibilità per un sistema di computer.
ms.assetid: da4ba366-49af-420e-a2ad-80bba34b3b00
title: Classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm
- Win32_Tpm.IsActivated_InitialValue
- Win32_Tpm.IsEnabled_InitialValue
- Win32_Tpm.IsOwned_InitialValue
- Win32_Tpm.SpecVersion
- Win32_Tpm.ManufacturerVersion
- Win32_Tpm.ManufacturerVersionInfo
- Win32_Tpm.ManufacturerId
- Win32_Tpm.PhysicalPresenceVersionInfo
api_type:
- DllExport
api_location:
- Win32_tpm.dll
ms.openlocfilehash: d8d6eac9fba875484ba2f08e149608c9994a1087
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316630"
---
# <a name="win32_tpm-class"></a><span data-ttu-id="7dc34-103">\_Classe TPM Win32</span><span class="sxs-lookup"><span data-stu-id="7dc34-103">Win32\_Tpm class</span></span>

<span data-ttu-id="7dc34-104">La **classe \_ TPM Win32** rappresenta il Trusted Platform Module (TPM), un chip di sicurezza hardware che fornisce una radice di attendibilità per un sistema di computer.</span><span class="sxs-lookup"><span data-stu-id="7dc34-104">The **Win32\_Tpm** class represents the Trusted Platform Module (TPM), a hardware security chip that provides a root of trust for a computer system.</span></span>

## <a name="syntax"></a><span data-ttu-id="7dc34-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7dc34-105">Syntax</span></span>

``` syntax
class Win32_Tpm
{
  boolean IsActivated_InitialValue;
  boolean IsEnabled_InitialValue;
  boolean IsOwned_InitialValue;
  string  SpecVersion;
  string  ManufacturerVersion;
  string  ManufacturerVersionInfo;
  uint32  ManufacturerId;
  string  PhysicalPresenceVersionInfo;
};
```

## <a name="members"></a><span data-ttu-id="7dc34-106">Members</span><span class="sxs-lookup"><span data-stu-id="7dc34-106">Members</span></span>

<span data-ttu-id="7dc34-107">La **classe \_ TPM Win32** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="7dc34-107">The **Win32\_Tpm** class has these types of members:</span></span>

-   [<span data-ttu-id="7dc34-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="7dc34-108">Methods</span></span>](#methods)
-   [<span data-ttu-id="7dc34-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7dc34-109">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="7dc34-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="7dc34-110">Methods</span></span>

<span data-ttu-id="7dc34-111">La **classe \_ TPM Win32** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="7dc34-111">The **Win32\_Tpm** class has these methods.</span></span>



| <span data-ttu-id="7dc34-112">Metodo</span><span class="sxs-lookup"><span data-stu-id="7dc34-112">Method</span></span>                                                                                   | <span data-ttu-id="7dc34-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7dc34-113">Description</span></span>                                                                                                                                                                                 |
|:-----------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7dc34-114">**AddBlockedCommand**</span><span class="sxs-lookup"><span data-stu-id="7dc34-114">**AddBlockedCommand**</span></span>](addblockedcommand-win32-tpm.md)                                 | <span data-ttu-id="7dc34-115">Aggiunge un comando TPM all'elenco locale dei comandi bloccati in Windows.</span><span class="sxs-lookup"><span data-stu-id="7dc34-115">Adds a TPM command to the local list of commands blocked on Windows.</span></span><br/>                                                                                                             |
| [<span data-ttu-id="7dc34-116">**ChangeOwnerAuth**</span><span class="sxs-lookup"><span data-stu-id="7dc34-116">**ChangeOwnerAuth**</span></span>](changeownerauth-win32-tpm.md)                                     | <span data-ttu-id="7dc34-117">Modifica il valore di autorizzazione del proprietario del TPM.</span><span class="sxs-lookup"><span data-stu-id="7dc34-117">Changes the TPM owner authorization value.</span></span><br/>                                                                                                                                       |
| [<span data-ttu-id="7dc34-118">**Deselezionare**</span><span class="sxs-lookup"><span data-stu-id="7dc34-118">**Clear**</span></span>](clear-win32-tpm.md)                                                         | <span data-ttu-id="7dc34-119">Reimposta il TPM sullo stato predefinito della factory.</span><span class="sxs-lookup"><span data-stu-id="7dc34-119">Resets the TPM to its factory-default state.</span></span><br/>                                                                                                                                     |
| [<span data-ttu-id="7dc34-120">**ConvertToOwnerAuth**</span><span class="sxs-lookup"><span data-stu-id="7dc34-120">**ConvertToOwnerAuth**</span></span>](converttoownerauth-win32-tpm.md)                               | <span data-ttu-id="7dc34-121">Converte una passphrase fornita dall'utente in un valore di autorizzazione proprietario di 20 byte che può essere utilizzato per interagire con il TPM.</span><span class="sxs-lookup"><span data-stu-id="7dc34-121">Converts a user-provided passphrase to a 20-byte owner authorization value that can be used to interact with the TPM.</span></span><br/>                                                            |
| [<span data-ttu-id="7dc34-122">**CreateEndorsementKeyPair**</span><span class="sxs-lookup"><span data-stu-id="7dc34-122">**CreateEndorsementKeyPair**</span></span>](createendorsementkeypair-win32-tpm.md)                   | <span data-ttu-id="7dc34-123">Crea una coppia di chiavi di approvazione a 2048 bit nel TPM.</span><span class="sxs-lookup"><span data-stu-id="7dc34-123">Creates a 2048-bit endorsement key pair on the TPM.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="7dc34-124">**Disabilita**</span><span class="sxs-lookup"><span data-stu-id="7dc34-124">**Disable**</span></span>](disable-win32-tpm.md)                                                     | <span data-ttu-id="7dc34-125">Consente al proprietario del TPM di disabilitare il TPM.</span><span class="sxs-lookup"><span data-stu-id="7dc34-125">Allows the TPM owner to disable the TPM.</span></span><br/>                                                                                                                                         |
| [<span data-ttu-id="7dc34-126">**Abilitare**</span><span class="sxs-lookup"><span data-stu-id="7dc34-126">**Enable**</span></span>](enable-win32-tpm.md)                                                       | <span data-ttu-id="7dc34-127">Consente al proprietario del TPM di abilitare il TPM.</span><span class="sxs-lookup"><span data-stu-id="7dc34-127">Allows the TPM owner to enable the TPM.</span></span><br/>                                                                                                                                          |
| [<span data-ttu-id="7dc34-128">**GetPhysicalPresenceRequest**</span><span class="sxs-lookup"><span data-stu-id="7dc34-128">**GetPhysicalPresenceRequest**</span></span>](getphysicalpresencerequest-win32-tpm.md)               | <span data-ttu-id="7dc34-129">Ottiene e restituisce l'operazione di presenza fisica del TPM in sospeso.</span><span class="sxs-lookup"><span data-stu-id="7dc34-129">Gets and returns the pending TPM physical presence operation.</span></span> <span data-ttu-id="7dc34-130">Usare il metodo [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) per richiedere un'operazione.</span><span class="sxs-lookup"><span data-stu-id="7dc34-130">Use the [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) method to request an operation.</span></span><br/> |
| [<span data-ttu-id="7dc34-131">**GetPhysicalPresenceResponse**</span><span class="sxs-lookup"><span data-stu-id="7dc34-131">**GetPhysicalPresenceResponse**</span></span>](getphysicalpresenceresponse-win32-tpm.md)             | <span data-ttu-id="7dc34-132">Ottiene e restituisce i risultati di un'operazione di presenza fisica TPM eseguita.</span><span class="sxs-lookup"><span data-stu-id="7dc34-132">Gets and returns the results from a TPM physical presence operation that was performed.</span></span><br/>                                                                                          |
| [<span data-ttu-id="7dc34-133">**GetPhysicalPresenceTransition**</span><span class="sxs-lookup"><span data-stu-id="7dc34-133">**GetPhysicalPresenceTransition**</span></span>](getphysicalpresencetransition-win32-tpm.md)         | <span data-ttu-id="7dc34-134">Indica l'azione dell'utente necessaria per eseguire un'operazione di presenza fisica del TPM.</span><span class="sxs-lookup"><span data-stu-id="7dc34-134">Indicates the user action that is needed to perform a TPM physical presence operation.</span></span><br/>                                                                                           |
| [<span data-ttu-id="7dc34-135">**IsActivated**</span><span class="sxs-lookup"><span data-stu-id="7dc34-135">**IsActivated**</span></span>](isactivated-win32-tpm.md)                                             | <span data-ttu-id="7dc34-136">Indica se il TPM è attivato.</span><span class="sxs-lookup"><span data-stu-id="7dc34-136">Indicates whether the TPM is activated.</span></span><br/>                                                                                                                                          |
| [<span data-ttu-id="7dc34-137">**IsCommandBlocked**</span><span class="sxs-lookup"><span data-stu-id="7dc34-137">**IsCommandBlocked**</span></span>](iscommandblocked-win32-tpm.md)                                   | <span data-ttu-id="7dc34-138">Indica se il comando TPM può essere eseguito in questo sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="7dc34-138">Indicates whether the TPM command can run on this operating system.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="7dc34-139">**IsCommandPresent**</span><span class="sxs-lookup"><span data-stu-id="7dc34-139">**IsCommandPresent**</span></span>](iscommandpresent-win32-tpm.md)                                   | <span data-ttu-id="7dc34-140">Indica se un comando TPM è supportato da questo computer.</span><span class="sxs-lookup"><span data-stu-id="7dc34-140">Indicates whether a TPM command is supported by this computer.</span></span><br/>                                                                                                                   |
| [<span data-ttu-id="7dc34-141">**IsEnabled**</span><span class="sxs-lookup"><span data-stu-id="7dc34-141">**IsEnabled**</span></span>](isenabled-win32-tpm.md)                                                 | <span data-ttu-id="7dc34-142">Indica se il TPM è abilitato.</span><span class="sxs-lookup"><span data-stu-id="7dc34-142">Indicates whether the TPM is enabled.</span></span><br/>                                                                                                                                            |
| [<span data-ttu-id="7dc34-143">**IsEndorsementKeyPairPresent**</span><span class="sxs-lookup"><span data-stu-id="7dc34-143">**IsEndorsementKeyPairPresent**</span></span>](isendorsementkeypairpresent-win32-tpm.md)             | <span data-ttu-id="7dc34-144">Indica se il TPM ha una coppia di chiavi di verifica dell'autenticità.</span><span class="sxs-lookup"><span data-stu-id="7dc34-144">Indicates whether the TPM has an endorsement key pair.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="7dc34-145">**Proprietario**</span><span class="sxs-lookup"><span data-stu-id="7dc34-145">**IsOwned**</span></span>](isowned-win32-tpm.md)                                                     | <span data-ttu-id="7dc34-146">Indica se il TPM ha un proprietario.</span><span class="sxs-lookup"><span data-stu-id="7dc34-146">Indicates whether the TPM has an owner.</span></span><br/>                                                                                                                                          |
| [<span data-ttu-id="7dc34-147">**IsOwnerClearDisabled**</span><span class="sxs-lookup"><span data-stu-id="7dc34-147">**IsOwnerClearDisabled**</span></span>](isownercleardisabled-win32-tpm.md)                           | <span data-ttu-id="7dc34-148">Indica se il proprietario del TPM può cancellare il TPM.</span><span class="sxs-lookup"><span data-stu-id="7dc34-148">Indicates whether the TPM owner can clear the TPM.</span></span><br/>                                                                                                                               |
| [<span data-ttu-id="7dc34-149">**IsOwnershipAllowed**</span><span class="sxs-lookup"><span data-stu-id="7dc34-149">**IsOwnershipAllowed**</span></span>](isownershipallowed-win32-tpm.md)                               | <span data-ttu-id="7dc34-150">Indica se è possibile installare un proprietario del TPM.</span><span class="sxs-lookup"><span data-stu-id="7dc34-150">Indicates whether a TPM owner can be installed.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="7dc34-151">**IsPhysicalClearDisabled**</span><span class="sxs-lookup"><span data-stu-id="7dc34-151">**IsPhysicalClearDisabled**</span></span>](isphysicalcleardisabled-win32-tpm.md)                     | <span data-ttu-id="7dc34-152">Indica se un'operazione di presenza fisica TPM può cancellare il TPM.</span><span class="sxs-lookup"><span data-stu-id="7dc34-152">Indicates whether a TPM physical presence operation can clear the TPM.</span></span><br/>                                                                                                           |
| [<span data-ttu-id="7dc34-153">**IsPhysicalPresenceHardwareEnabled**</span><span class="sxs-lookup"><span data-stu-id="7dc34-153">**IsPhysicalPresenceHardwareEnabled**</span></span>](isphysicalpresencehardwareenabled-win32-tpm.md) | <span data-ttu-id="7dc34-154">Indica se il computer supporta un percorso hardware dedicato per segnalare la presenza fisica.</span><span class="sxs-lookup"><span data-stu-id="7dc34-154">Indicates whether this computer supports a dedicated hardware path to signal physical presence.</span></span><br/>                                                                                  |
| [<span data-ttu-id="7dc34-155">**IsSrkAuthCompatible**</span><span class="sxs-lookup"><span data-stu-id="7dc34-155">**IsSrkAuthCompatible**</span></span>](issrkauthcompatible-win32-tpm.md)                             | <span data-ttu-id="7dc34-156">Indica se l'autorizzazione della chiave radice di archiviazione (SRK) è compatibile con Windows.</span><span class="sxs-lookup"><span data-stu-id="7dc34-156">Indicates whether the Storage Root Key (SRK) authorization is compatible with Windows.</span></span><br/>                                                                                           |
| [<span data-ttu-id="7dc34-157">**RemoveBlockedCommand**</span><span class="sxs-lookup"><span data-stu-id="7dc34-157">**RemoveBlockedCommand**</span></span>](removeblockedcommand-win32-tpm.md)                           | <span data-ttu-id="7dc34-158">Rimuove un comando TPM dall'elenco locale di comandi bloccati da Windows.</span><span class="sxs-lookup"><span data-stu-id="7dc34-158">Removes a TPM command from the local list of commands blocked by Windows.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="7dc34-159">**ResetAuthLockOut**</span><span class="sxs-lookup"><span data-stu-id="7dc34-159">**ResetAuthLockOut**</span></span>](resetauthlockout-win32-tpm.md)                                   | <span data-ttu-id="7dc34-160">Reimposta il periodo di timeout o un altro meccanismo che i produttori di TPM implementano per proteggersi dagli attacchi del dizionario sul TPM.</span><span class="sxs-lookup"><span data-stu-id="7dc34-160">Resets the time-out period or other mechanism that TPM manufacturers implement to protect against dictionary attacks on the TPM.</span></span><br/>                                                 |
| [<span data-ttu-id="7dc34-161">**ResetSrkAuth**</span><span class="sxs-lookup"><span data-stu-id="7dc34-161">**ResetSrkAuth**</span></span>](resetsrkauth-win32-tpm.md)                                           | <span data-ttu-id="7dc34-162">Reimposta il valore di autorizzazione della chiave radice di archiviazione (SRK) in modo che sia compatibile con Windows.</span><span class="sxs-lookup"><span data-stu-id="7dc34-162">Resets the Storage Root Key (SRK) authorization value to be compatible with Windows.</span></span><br/>                                                                                             |
| [<span data-ttu-id="7dc34-163">**SelfTest**</span><span class="sxs-lookup"><span data-stu-id="7dc34-163">**SelfTest**</span></span>](selftest-win32-tpm.md)                                                   | <span data-ttu-id="7dc34-164">Esegue un test automatico del TPM e restituisce il risultato.</span><span class="sxs-lookup"><span data-stu-id="7dc34-164">Performs a self-test of the TPM and returns the result.</span></span><br/>                                                                                                                          |
| [<span data-ttu-id="7dc34-165">**SetPhysicalPresenceRequest**</span><span class="sxs-lookup"><span data-stu-id="7dc34-165">**SetPhysicalPresenceRequest**</span></span>](setphysicalpresencerequest-win32-tpm.md)               | <span data-ttu-id="7dc34-166">Richiede l'esecuzione di un'operazione di presenza fisica TPM.</span><span class="sxs-lookup"><span data-stu-id="7dc34-166">Requests a TPM physical presence operation to run.</span></span><br/>                                                                                                                               |
| [<span data-ttu-id="7dc34-167">**TakeOwnership**</span><span class="sxs-lookup"><span data-stu-id="7dc34-167">**TakeOwnership**</span></span>](takeownership-win32-tpm.md)                                         | <span data-ttu-id="7dc34-168">Installa un proprietario per il TPM.</span><span class="sxs-lookup"><span data-stu-id="7dc34-168">Installs an owner for the TPM.</span></span><br/>                                                                                                                                                   |



 

### <a name="properties"></a><span data-ttu-id="7dc34-169">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7dc34-169">Properties</span></span>

<span data-ttu-id="7dc34-170">La **classe \_ TPM Win32** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="7dc34-170">The **Win32\_Tpm** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7dc34-171">**\_InitialValue disattivato**</span><span class="sxs-lookup"><span data-stu-id="7dc34-171">**IsActivated\_InitialValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7dc34-172">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="7dc34-172">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7dc34-173">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7dc34-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7dc34-174">Indica se il TPM è attivato.</span><span class="sxs-lookup"><span data-stu-id="7dc34-174">Indicates whether the TPM is activated.</span></span>

<span data-ttu-id="7dc34-175">**true** se il dispositivo è attivato (ovvero se **\_ InitialValue** è true); in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="7dc34-175">**true** if the device is activated (that is, if **IsActivated\_InitialValue** is true); otherwise, **false**.</span></span>

<span data-ttu-id="7dc34-176">Questo valore viene archiviato quando viene creata un'istanza della classe.</span><span class="sxs-lookup"><span data-stu-id="7dc34-176">This value is stored when the class is instantiated.</span></span> <span data-ttu-id="7dc34-177">È possibile che il TPM modifichi lo stato tra la creazione dell'istanza e quando si seleziona questo valore.</span><span class="sxs-lookup"><span data-stu-id="7dc34-177">It is possible for the TPM to change state between the instantiation and when you check this value.</span></span> <span data-ttu-id="7dc34-178">Per verificare se il TPM è attivato in tempo reale, usare il metodo [**disattivato**](isactivated-win32-tpm.md) .</span><span class="sxs-lookup"><span data-stu-id="7dc34-178">To check whether the TPM is activated in real time, use the [**IsActivated**](isactivated-win32-tpm.md) method.</span></span>

<span data-ttu-id="7dc34-179">**Windows Server 2008 e Windows Vista:** Questa proprietà non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="7dc34-179">**Windows Server 2008 and Windows Vista:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="7dc34-180">**IsEnabled \_ InitialValue**</span><span class="sxs-lookup"><span data-stu-id="7dc34-180">**IsEnabled\_InitialValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7dc34-181">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="7dc34-181">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7dc34-182">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7dc34-182">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7dc34-183">Indica se il TPM è abilitato.</span><span class="sxs-lookup"><span data-stu-id="7dc34-183">Indicates whether the TPM is enabled.</span></span>

<span data-ttu-id="7dc34-184">**true** se il dispositivo è abilitato (ovvero se **IsEnabled \_ InitialValue** è true); in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="7dc34-184">**true** if the device is enabled (that is, if **IsEnabled\_InitialValue** is true); otherwise, **false**.</span></span>

<span data-ttu-id="7dc34-185">Questo valore viene archiviato quando viene creata un'istanza della classe.</span><span class="sxs-lookup"><span data-stu-id="7dc34-185">This value is stored when the class is instantiated.</span></span> <span data-ttu-id="7dc34-186">È possibile che il TPM modifichi lo stato tra la creazione dell'istanza e quando si seleziona questo valore.</span><span class="sxs-lookup"><span data-stu-id="7dc34-186">It is possible for the TPM to change state between the instantiation and when you check this value.</span></span> <span data-ttu-id="7dc34-187">Per verificare se il TPM è abilitato in tempo reale, usare il metodo [**IsEnabled**](isenabled-win32-tpm.md) .</span><span class="sxs-lookup"><span data-stu-id="7dc34-187">To check whether the TPM is enabled in real time, use the [**IsEnabled**](isenabled-win32-tpm.md) method.</span></span>

<span data-ttu-id="7dc34-188">**Windows Server 2008 e Windows Vista:** Questa proprietà non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="7dc34-188">**Windows Server 2008 and Windows Vista:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="7dc34-189">**InitialValue di proprietà \_**</span><span class="sxs-lookup"><span data-stu-id="7dc34-189">**IsOwned\_InitialValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7dc34-190">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="7dc34-190">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7dc34-191">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7dc34-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7dc34-192">Indica se il TPM ha un proprietario.</span><span class="sxs-lookup"><span data-stu-id="7dc34-192">Indicates whether the TPM has an owner.</span></span>

<span data-ttu-id="7dc34-193">**true** se il dispositivo ha un proprietario (ovvero se **\_ InitialValue** è true); in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="7dc34-193">**true** if the device has an owner (that is, if **IsOwned\_InitialValue** is true); otherwise, **false**.</span></span>

<span data-ttu-id="7dc34-194">Questo valore viene archiviato quando viene creata un'istanza della classe.</span><span class="sxs-lookup"><span data-stu-id="7dc34-194">This value is stored when the class is instantiated.</span></span> <span data-ttu-id="7dc34-195">È possibile che il TPM modifichi lo stato tra la creazione dell'istanza e quando si seleziona questo valore.</span><span class="sxs-lookup"><span data-stu-id="7dc34-195">It is possible for the TPM to change state between the instantiation and when you check this value.</span></span> <span data-ttu-id="7dc34-196">Per verificare se il TPM è di proprietà in tempo reale, utilizzare il metodo di [**Proprietà**](isowned-win32-tpm.md) .</span><span class="sxs-lookup"><span data-stu-id="7dc34-196">To check whether the TPM is owned in real time, use the [**IsOwned**](isowned-win32-tpm.md) method.</span></span>

<span data-ttu-id="7dc34-197">**Windows Server 2008 e Windows Vista:** Questa proprietà non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="7dc34-197">**Windows Server 2008 and Windows Vista:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="7dc34-198">**ManufacturerId**</span><span class="sxs-lookup"><span data-stu-id="7dc34-198">**ManufacturerId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7dc34-199">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7dc34-199">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7dc34-200">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7dc34-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7dc34-201">Informazioni di identificazione che denominano in modo univoco il produttore del TPM.</span><span class="sxs-lookup"><span data-stu-id="7dc34-201">The identifying information that uniquely names the TPM manufacturer.</span></span>

<span data-ttu-id="7dc34-202">Quando i dati non sono disponibili, viene restituito zero.</span><span class="sxs-lookup"><span data-stu-id="7dc34-202">When the data is unavailable, zero is returned.</span></span>

<span data-ttu-id="7dc34-203">Questo valore integer può essere convertito in un valore stringa interpretando ogni byte come carattere ASCII.</span><span class="sxs-lookup"><span data-stu-id="7dc34-203">This integer value can be translated to a string value by interpreting each byte as an ASCII character.</span></span> <span data-ttu-id="7dc34-204">Ad esempio, un valore intero di 1414548736 può essere suddiviso in questi 4 byte: 0x54, 0x50, irreversibile 0x4D e 0x00.</span><span class="sxs-lookup"><span data-stu-id="7dc34-204">For example, an integer value of 1414548736 can be divided into these 4 bytes: 0x54, 0x50, 0x4D, and 0x00.</span></span> <span data-ttu-id="7dc34-205">Supponendo che la stringa venga interpretata da sinistra a destra, questo valore intero viene convertito in un valore stringa di "TPM".</span><span class="sxs-lookup"><span data-stu-id="7dc34-205">Assuming the string is interpreted from left to right, this integer value translated to a string value of "TPM".</span></span>

</dd> <dt>

<span data-ttu-id="7dc34-206">**ManufacturerVersion**</span><span class="sxs-lookup"><span data-stu-id="7dc34-206">**ManufacturerVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7dc34-207">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7dc34-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7dc34-208">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7dc34-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7dc34-209">Versione del TPM, come specificato dal produttore.</span><span class="sxs-lookup"><span data-stu-id="7dc34-209">The version of the TPM, as specified by the manufacturer.</span></span>

<span data-ttu-id="7dc34-210">Quando i dati non sono disponibili, viene restituito "non supportato".</span><span class="sxs-lookup"><span data-stu-id="7dc34-210">When the data is unavailable, "Not Supported" is returned.</span></span>

</dd> <dt>

<span data-ttu-id="7dc34-211">**ManufacturerVersionInfo**</span><span class="sxs-lookup"><span data-stu-id="7dc34-211">**ManufacturerVersionInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7dc34-212">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7dc34-212">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7dc34-213">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7dc34-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7dc34-214">Altre informazioni sulla versione specifiche del produttore per il TPM.</span><span class="sxs-lookup"><span data-stu-id="7dc34-214">Other manufacturer-specific version information for the TPM.</span></span>

<span data-ttu-id="7dc34-215">Quando i dati non sono disponibili, viene restituito "non supportato".</span><span class="sxs-lookup"><span data-stu-id="7dc34-215">When the data is unavailable, "Not Supported" is returned.</span></span>

</dd> <dt>

<span data-ttu-id="7dc34-216">**PhysicalPresenceVersionInfo**</span><span class="sxs-lookup"><span data-stu-id="7dc34-216">**PhysicalPresenceVersionInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7dc34-217">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7dc34-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7dc34-218">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7dc34-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7dc34-219">La versione dell'interfaccia di presenza fisica, un meccanismo di comunicazione utilizzato per eseguire le operazioni del dispositivo che richiedono la presenza fisica, supportata dal computer.</span><span class="sxs-lookup"><span data-stu-id="7dc34-219">The version of the Physical Presence Interface, a communication mechanism used to run device operations that require physical presence, that the computer supports.</span></span>

<span data-ttu-id="7dc34-220">Questa interfaccia deve essere disponibile per l'esecuzione di operazioni di presenza fisica TPM.</span><span class="sxs-lookup"><span data-stu-id="7dc34-220">This interface must be available to run TPM physical presence operations.</span></span> <span data-ttu-id="7dc34-221">I **metodi \_ TPM Win32** [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md), [**GetPhysicalPresenceRequest**](getphysicalpresencerequest-win32-tpm.md), [**GetPhysicalPresenceTransition**](getphysicalpresencetransition-win32-tpm.md)e [**GetPhysicalPresenceResponse**](getphysicalpresenceresponse-win32-tpm.md) espongono le funzionalità dell'interfaccia di presenza fisica.</span><span class="sxs-lookup"><span data-stu-id="7dc34-221">The **Win32\_Tpm** methods [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md), [**GetPhysicalPresenceRequest**](getphysicalpresencerequest-win32-tpm.md), [**GetPhysicalPresenceTransition**](getphysicalpresencetransition-win32-tpm.md), and [**GetPhysicalPresenceResponse**](getphysicalpresenceresponse-win32-tpm.md) expose the capabilities of the Physical Presence Interface.</span></span>

<span data-ttu-id="7dc34-222">Quando i dati non sono disponibili, viene restituito "non supportato".</span><span class="sxs-lookup"><span data-stu-id="7dc34-222">When the data is unavailable, "Not Supported" is returned.</span></span>

</dd> <dt>

<span data-ttu-id="7dc34-223">**Versione specifica**</span><span class="sxs-lookup"><span data-stu-id="7dc34-223">**SpecVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7dc34-224">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7dc34-224">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7dc34-225">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7dc34-225">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7dc34-226">Versione della specifica del Trusted Computing Group (TCG) supportata dal TPM.</span><span class="sxs-lookup"><span data-stu-id="7dc34-226">The version of the Trusted Computing Group (TCG) specification that the TPM supports.</span></span> <span data-ttu-id="7dc34-227">Questo valore include la versione delle specifiche TCG principale e secondaria, il livello di revisione della specifica e il livello di revisione degli errori.</span><span class="sxs-lookup"><span data-stu-id="7dc34-227">This value includes the major and minor TCG specification version, the specification revision level, and the errata revision level.</span></span> <span data-ttu-id="7dc34-228">Tutti i valori sono in formato esadecimale.</span><span class="sxs-lookup"><span data-stu-id="7dc34-228">All values are in hexadecimal.</span></span> <span data-ttu-id="7dc34-229">Ad esempio, le informazioni sulla versione "1,2, 2, 0" indicano che il dispositivo è stato implementato nella specifica TCG versione 1,2, livello Revisione 2 e senza errori.</span><span class="sxs-lookup"><span data-stu-id="7dc34-229">For example, a version information of "1.2, 2, 0" indicates that the device was implemented to TCG specification version 1.2, revision level 2, and with no errata.</span></span>

<span data-ttu-id="7dc34-230">Quando i dati non sono disponibili, viene restituito "non supportato".</span><span class="sxs-lookup"><span data-stu-id="7dc34-230">When the data is unavailable, "Not Supported" is returned.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7dc34-231">Commenti</span><span class="sxs-lookup"><span data-stu-id="7dc34-231">Remarks</span></span>

<span data-ttu-id="7dc34-232">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="7dc34-232">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="7dc34-233">I file MOF non sono installati come parte del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="7dc34-233">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="7dc34-234">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="7dc34-234">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="7dc34-235">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="7dc34-235">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7dc34-236">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7dc34-236">Requirements</span></span>



| <span data-ttu-id="7dc34-237">Requisito</span><span class="sxs-lookup"><span data-stu-id="7dc34-237">Requirement</span></span> | <span data-ttu-id="7dc34-238">Valore</span><span class="sxs-lookup"><span data-stu-id="7dc34-238">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="7dc34-239">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7dc34-239">Minimum supported client</span></span><br/> | <span data-ttu-id="7dc34-240">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7dc34-240">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="7dc34-241">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7dc34-241">Minimum supported server</span></span><br/> | <span data-ttu-id="7dc34-242">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7dc34-242">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="7dc34-243">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="7dc34-243">Namespace</span></span><br/>                | <span data-ttu-id="7dc34-244">Radice \\ CIMV2 \\ sicurezza \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="7dc34-244">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="7dc34-245">MOF</span><span class="sxs-lookup"><span data-stu-id="7dc34-245">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7dc34-246"><dt>\_TPM Win32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7dc34-246"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="7dc34-247">DLL</span><span class="sxs-lookup"><span data-stu-id="7dc34-247">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7dc34-248"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="7dc34-248"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



 

 
