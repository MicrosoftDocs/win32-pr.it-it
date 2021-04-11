---
description: Indica un errore BIOS del sistema MCA (computer Check Architecture). Questa classe è disponibile solo nei sistemi Windows a 64 bit.
ms.assetid: b451ca45-6208-4445-b9f1-b4e3174837a4
title: Classe MSMCAEvent_SMBIOSError
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_SMBIOSError
- MSMCAEvent_SMBIOSError.Active
- MSMCAEvent_SMBIOSError.AdditionalErrors
- MSMCAEvent_SMBIOSError.Cpu
- MSMCAEvent_SMBIOSError.ErrorSeverity
- MSMCAEvent_SMBIOSError.InstanceName
- MSMCAEvent_SMBIOSError.RawRecord
- MSMCAEvent_SMBIOSError.RecordId
- MSMCAEvent_SMBIOSError.Size
- MSMCAEvent_SMBIOSError.SMBIOS_EVENT_TYPE
- MSMCAEvent_SMBIOSError.Type
- MSMCAEvent_SMBIOSError.VALIDATION_BITS
- MSMCAEvent_SMBIOSError.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 709d480e8865c5d5bde2a9f5e8de45f138e66548
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233115"
---
# <a name="msmcaevent_smbioserror-class"></a><span data-ttu-id="b2b1a-104">\_Classe MSMCAEvent SMBIOSError</span><span class="sxs-lookup"><span data-stu-id="b2b1a-104">MSMCAEvent\_SMBIOSError class</span></span>

<span data-ttu-id="b2b1a-105">La classe **MSMCAEvent \_ SMBIOSError** indica un errore BIOS del sistema MCA (Machine Check Architecture).</span><span class="sxs-lookup"><span data-stu-id="b2b1a-105">The **MSMCAEvent\_SMBIOSError** class indicates a Machine Check Architecture (MCA) system BIOS error.</span></span> <span data-ttu-id="b2b1a-106">Questa classe è disponibile solo nei sistemi Windows a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="b2b1a-106">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="b2b1a-107">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="b2b1a-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="b2b1a-108">Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="b2b1a-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2b1a-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b2b1a-109">Syntax</span></span>

``` syntax
class MSMCAEvent_SMBIOSError : WMIEvent
{
  boolean Active;
  uint32  AdditionalErrors;
  uint32  Cpu;
  uint8   ErrorSeverity;
  string  InstanceName;
  uint8   RawRecord[];
  uint64  RecordId;
  uint32  Size;
  uint8   SMBIOS_EVENT_TYPE;
  uint32  Type;
  uint64  VALIDATION_BITS;
  uint32  LogToEventlog;
};
```

## <a name="members"></a><span data-ttu-id="b2b1a-110">Members</span><span class="sxs-lookup"><span data-stu-id="b2b1a-110">Members</span></span>

<span data-ttu-id="b2b1a-111">La **classe \_ SMBIOSError di MSMCAEvent** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="b2b1a-111">The **MSMCAEvent\_SMBIOSError** class has these types of members:</span></span>

-   [<span data-ttu-id="b2b1a-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b2b1a-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b2b1a-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b2b1a-113">Properties</span></span>

<span data-ttu-id="b2b1a-114">La **classe \_ SMBIOSError di MSMCAEvent** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="b2b1a-114">The **MSMCAEvent\_SMBIOSError** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b2b1a-115">**Attivo**</span><span class="sxs-lookup"><span data-stu-id="b2b1a-115">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2b1a-116">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="b2b1a-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b2b1a-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b2b1a-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b2b1a-118">**True** se questa istanza della classe è attiva; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="b2b1a-118">**TRUE**, if this instance of the class is active; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="b2b1a-119">**AdditionalErrors**</span><span class="sxs-lookup"><span data-stu-id="b2b1a-119">**AdditionalErrors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2b1a-120">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b2b1a-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b2b1a-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b2b1a-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b2b1a-122">Numero di errori aggiuntivi nel record.</span><span class="sxs-lookup"><span data-stu-id="b2b1a-122">Number of additional errors in the record.</span></span>

</dd> <dt>

<span data-ttu-id="b2b1a-123">**CPU**</span><span class="sxs-lookup"><span data-stu-id="b2b1a-123">**Cpu**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2b1a-124">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b2b1a-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b2b1a-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b2b1a-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b2b1a-126">CPU che ha segnalato l'errore.</span><span class="sxs-lookup"><span data-stu-id="b2b1a-126">CPU that reported the error.</span></span> <span data-ttu-id="b2b1a-127">Questa proprietà si applica solo a un sistema multiprocessore in cui al primo processore viene assegnato il numero 0, al secondo processore viene assegnato il numero 1 e così via.</span><span class="sxs-lookup"><span data-stu-id="b2b1a-127">This property only applies to a multiprocessor system in which the first processor is assigned the number 0, the second processor is assigned the number 1, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="b2b1a-128">**ErrorSeverity**</span><span class="sxs-lookup"><span data-stu-id="b2b1a-128">**ErrorSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2b1a-129">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="b2b1a-129">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="b2b1a-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b2b1a-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b2b1a-131">Livello di gravità dell'errore segnalato.</span><span class="sxs-lookup"><span data-stu-id="b2b1a-131">Severity level of the error reported.</span></span>



| <span data-ttu-id="b2b1a-132">Valore</span><span class="sxs-lookup"><span data-stu-id="b2b1a-132">Value</span></span>                                                                                                | <span data-ttu-id="b2b1a-133">Significato</span><span class="sxs-lookup"><span data-stu-id="b2b1a-133">Meaning</span></span>                |
|------------------------------------------------------------------------------------------------------|------------------------|
| <span id="0"></span><dl> <span data-ttu-id="b2b1a-134"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="b2b1a-134"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="b2b1a-135">Recuperabile</span><span class="sxs-lookup"><span data-stu-id="b2b1a-135">Recoverable</span></span><br/> |
| <span id="1"></span><dl> <span data-ttu-id="b2b1a-136"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="b2b1a-136"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="b2b1a-137">Fatal</span><span class="sxs-lookup"><span data-stu-id="b2b1a-137">Fatal</span></span><br/>       |
| <span id="2"></span><dl> <span data-ttu-id="b2b1a-138"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="b2b1a-138"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="b2b1a-139">Correggibile</span><span class="sxs-lookup"><span data-stu-id="b2b1a-139">Correctable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="b2b1a-140">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="b2b1a-140">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2b1a-141">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2b1a-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2b1a-142">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b2b1a-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b2b1a-143">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b2b1a-143">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b2b1a-144">Identificatore univoco di questa istanza della classe.</span><span class="sxs-lookup"><span data-stu-id="b2b1a-144">Unique identifier of this instance of the class.</span></span>

</dd> <dt>

<span data-ttu-id="b2b1a-145">**LogToEventlog**</span><span class="sxs-lookup"><span data-stu-id="b2b1a-145">**LogToEventlog**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2b1a-146">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b2b1a-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b2b1a-147">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b2b1a-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b2b1a-148">Se è 0 (zero), questo evento non viene registrato nel registro eventi di sistema.</span><span class="sxs-lookup"><span data-stu-id="b2b1a-148">If 0 (zero), then this event is not logged to the system event log.</span></span>

</dd> <dt>

<span data-ttu-id="b2b1a-149">**RawRecord**</span><span class="sxs-lookup"><span data-stu-id="b2b1a-149">**RawRecord**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2b1a-150">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="b2b1a-150">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="b2b1a-151">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b2b1a-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b2b1a-152">Matrice di byte che contiene il record di errore non elaborato.</span><span class="sxs-lookup"><span data-stu-id="b2b1a-152">Array of bytes that contains the raw error record.</span></span> <span data-ttu-id="b2b1a-153">Numero di elementi nella matrice specificata dalla proprietà **size** .</span><span class="sxs-lookup"><span data-stu-id="b2b1a-153">The number of elements in the array that the **Size** property specifies.</span></span>

</dd> <dt>

<span data-ttu-id="b2b1a-154">**RecordId**</span><span class="sxs-lookup"><span data-stu-id="b2b1a-154">**RecordId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2b1a-155">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b2b1a-155">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b2b1a-156">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b2b1a-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b2b1a-157">Identificatore del record di errore per l'errore.</span><span class="sxs-lookup"><span data-stu-id="b2b1a-157">Record identifier of the error record for this error.</span></span>

<span data-ttu-id="b2b1a-158">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b2b1a-158">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="b2b1a-159">**Dimensioni**</span><span class="sxs-lookup"><span data-stu-id="b2b1a-159">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2b1a-160">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b2b1a-160">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b2b1a-161">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b2b1a-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b2b1a-162">Dimensioni del record di errore non elaborato.</span><span class="sxs-lookup"><span data-stu-id="b2b1a-162">Size of the raw error record.</span></span>

</dd> <dt>

<span data-ttu-id="b2b1a-163">**\_tipo di evento SMBIOS \_**</span><span class="sxs-lookup"><span data-stu-id="b2b1a-163">**SMBIOS\_EVENT\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2b1a-164">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="b2b1a-164">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="b2b1a-165">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b2b1a-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b2b1a-166">Tipo di evento.</span><span class="sxs-lookup"><span data-stu-id="b2b1a-166">Event type.</span></span>



| <span data-ttu-id="b2b1a-167">Valore</span><span class="sxs-lookup"><span data-stu-id="b2b1a-167">Value</span></span>                                                                                                  | <span data-ttu-id="b2b1a-168">Significato</span><span class="sxs-lookup"><span data-stu-id="b2b1a-168">Meaning</span></span>                                                                                                                     |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="b2b1a-169"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="b2b1a-169"><dt>**0**</dt></span></span> </dl>   | <span data-ttu-id="b2b1a-170">Riservato.</span><span class="sxs-lookup"><span data-stu-id="b2b1a-170">Reserved.</span></span><br/>                                                                                                        |
| <span id="1"></span><dl> <span data-ttu-id="b2b1a-171"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="b2b1a-171"><dt>**1**</dt></span></span> </dl>   | <span data-ttu-id="b2b1a-172">Errore di memoria ECC a bit singolo.</span><span class="sxs-lookup"><span data-stu-id="b2b1a-172">Single bit ECC memory error.</span></span><br/>                                                                                     |
| <span id="2"></span><dl> <span data-ttu-id="b2b1a-173"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="b2b1a-173"><dt>**2**</dt></span></span> </dl>   | <span data-ttu-id="b2b1a-174">Errore di memoria a più bit ECC.</span><span class="sxs-lookup"><span data-stu-id="b2b1a-174">Multiple bit ECC memory error.</span></span><br/>                                                                                   |
| <span id="3"></span><dl> <span data-ttu-id="b2b1a-175"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="b2b1a-175"><dt>**3**</dt></span></span> </dl>   | <span data-ttu-id="b2b1a-176">Errore di memoria di parità.</span><span class="sxs-lookup"><span data-stu-id="b2b1a-176">Parity Memory error.</span></span><br/>                                                                                             |
| <span id="4"></span><dl> <span data-ttu-id="b2b1a-177"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="b2b1a-177"><dt>**4**</dt></span></span> </dl>   | <span data-ttu-id="b2b1a-178">Timeout del bus.</span><span class="sxs-lookup"><span data-stu-id="b2b1a-178">Bus time out.</span></span><br/>                                                                                                    |
| <span id="5"></span><dl> <span data-ttu-id="b2b1a-179"><dt>**5**</dt></span><span class="sxs-lookup"><span data-stu-id="b2b1a-179"><dt>**5**</dt></span></span> </dl>   | <span data-ttu-id="b2b1a-180">Controllo del canale di I/O.</span><span class="sxs-lookup"><span data-stu-id="b2b1a-180">I/O Channel Check.</span></span><br/>                                                                                               |
| <span id="6"></span><dl> <span data-ttu-id="b2b1a-181"><dt>**6**</dt></span><span class="sxs-lookup"><span data-stu-id="b2b1a-181"><dt>**6**</dt></span></span> </dl>   | <span data-ttu-id="b2b1a-182">NMI software.</span><span class="sxs-lookup"><span data-stu-id="b2b1a-182">Software NMI.</span></span><br/>                                                                                                    |
| <span id="7"></span><dl> <span data-ttu-id="b2b1a-183"><dt>**7**</dt></span><span class="sxs-lookup"><span data-stu-id="b2b1a-183"><dt>**7**</dt></span></span> </dl>   | <span data-ttu-id="b2b1a-184">Ridimensionamento post-memoria.</span><span class="sxs-lookup"><span data-stu-id="b2b1a-184">Post Memory Resize.</span></span><br/>                                                                                              |
| <span id="8"></span><dl> <span data-ttu-id="b2b1a-185"><dt>**8**</dt></span><span class="sxs-lookup"><span data-stu-id="b2b1a-185"><dt>**8**</dt></span></span> </dl>   | <span data-ttu-id="b2b1a-186">MESSAGGIO di errore.</span><span class="sxs-lookup"><span data-stu-id="b2b1a-186">POST Error.</span></span><br/>                                                                                                      |
| <span id="9"></span><dl> <span data-ttu-id="b2b1a-187"><dt>**9**</dt></span><span class="sxs-lookup"><span data-stu-id="b2b1a-187"><dt>**9**</dt></span></span> </dl>   | <span data-ttu-id="b2b1a-188">Errore di parità PCI.</span><span class="sxs-lookup"><span data-stu-id="b2b1a-188">PCI Parity Error.</span></span><br/>                                                                                                |
| <span id="10"></span><dl> <span data-ttu-id="b2b1a-189"><dt>**10**</dt></span><span class="sxs-lookup"><span data-stu-id="b2b1a-189"><dt>**10**</dt></span></span> </dl> | <span data-ttu-id="b2b1a-190">Errore di sistema PCI.</span><span class="sxs-lookup"><span data-stu-id="b2b1a-190">PCI System Error.</span></span><br/>                                                                                                |
| <span id="11"></span><dl> <span data-ttu-id="b2b1a-191"><dt>**11**</dt></span><span class="sxs-lookup"><span data-stu-id="b2b1a-191"><dt>**11**</dt></span></span> </dl> | <span data-ttu-id="b2b1a-192">Errore CPU.</span><span class="sxs-lookup"><span data-stu-id="b2b1a-192">CPU Failure.</span></span><br/>                                                                                                     |
| <span id="12"></span><dl> <span data-ttu-id="b2b1a-193"><dt>**12**</dt></span><span class="sxs-lookup"><span data-stu-id="b2b1a-193"><dt>**12**</dt></span></span> </dl> | <span data-ttu-id="b2b1a-194">Timeout del timer di failsafe per EISA.</span><span class="sxs-lookup"><span data-stu-id="b2b1a-194">EISA Failsafe Timer time out.</span></span><br/>                                                                                    |
| <span id="13"></span><dl> <span data-ttu-id="b2b1a-195"><dt>**13**</dt></span><span class="sxs-lookup"><span data-stu-id="b2b1a-195"><dt>**13**</dt></span></span> </dl> | <span data-ttu-id="b2b1a-196">Registro memoria correggibile disabilitato.</span><span class="sxs-lookup"><span data-stu-id="b2b1a-196">Correctable memory log disabled.</span></span><br/>                                                                                 |
| <span id="14"></span><dl> <span data-ttu-id="b2b1a-197"><dt>**14**</dt></span><span class="sxs-lookup"><span data-stu-id="b2b1a-197"><dt>**14**</dt></span></span> </dl> | <span data-ttu-id="b2b1a-198">Registrazione disabilitata per un tipo di evento specifico.</span><span class="sxs-lookup"><span data-stu-id="b2b1a-198">Logging disabled for a specific event type.</span></span> <span data-ttu-id="b2b1a-199">Troppi errori dello stesso tipo ricevuti in un breve periodo di tempo.</span><span class="sxs-lookup"><span data-stu-id="b2b1a-199">Too many errors of the same type received in a short amount of time.</span></span><br/> |
| <span id="15"></span><dl> <span data-ttu-id="b2b1a-200"><dt>**15**</dt></span><span class="sxs-lookup"><span data-stu-id="b2b1a-200"><dt>**15**</dt></span></span> </dl> | <span data-ttu-id="b2b1a-201">Riservato.</span><span class="sxs-lookup"><span data-stu-id="b2b1a-201">Reserved.</span></span><br/>                                                                                                        |
| <span id="16"></span><dl> <span data-ttu-id="b2b1a-202"><dt>**16**</dt></span><span class="sxs-lookup"><span data-stu-id="b2b1a-202"><dt>**16**</dt></span></span> </dl> | <span data-ttu-id="b2b1a-203">È stato superato il limite di sistema (ad esempio, soglia di tensione o temperatura superata).</span><span class="sxs-lookup"><span data-stu-id="b2b1a-203">System limit exceeded (for example, voltage or temperature threshold exceeded).</span></span><br/>                                  |
| <span id="17"></span><dl> <span data-ttu-id="b2b1a-204"><dt>**17**</dt></span><span class="sxs-lookup"><span data-stu-id="b2b1a-204"><dt>**17**</dt></span></span> </dl> | <span data-ttu-id="b2b1a-205">Timer hardware asincrono scaduto ed è stato emesso un ripristino del sistema.</span><span class="sxs-lookup"><span data-stu-id="b2b1a-205">Asynchronous hardware timer expired and issued a system reset.</span></span><br/>                                                   |
| <span id="18"></span><dl> <span data-ttu-id="b2b1a-206"><dt>**18**</dt></span><span class="sxs-lookup"><span data-stu-id="b2b1a-206"><dt>**18**</dt></span></span> </dl> | <span data-ttu-id="b2b1a-207">Informazioni sulla configurazione di sistema.</span><span class="sxs-lookup"><span data-stu-id="b2b1a-207">System configuration information.</span></span><br/>                                                                                |
| <span id="19"></span><dl> <span data-ttu-id="b2b1a-208"><dt>**19**</dt></span><span class="sxs-lookup"><span data-stu-id="b2b1a-208"><dt>**19**</dt></span></span> </dl> | <span data-ttu-id="b2b1a-209">Informazioni sul disco rigido.</span><span class="sxs-lookup"><span data-stu-id="b2b1a-209">Hard disk information.</span></span><br/>                                                                                           |
| <span id="20"></span><dl> <span data-ttu-id="b2b1a-210"><dt>**20**</dt></span><span class="sxs-lookup"><span data-stu-id="b2b1a-210"><dt>**20**</dt></span></span> </dl> | <span data-ttu-id="b2b1a-211">Sistema riconfigurato.</span><span class="sxs-lookup"><span data-stu-id="b2b1a-211">System reconfigured.</span></span><br/>                                                                                             |
| <span id="21"></span><dl> <span data-ttu-id="b2b1a-212"><dt>**21**</dt></span><span class="sxs-lookup"><span data-stu-id="b2b1a-212"><dt>**21**</dt></span></span> </dl> | <span data-ttu-id="b2b1a-213">Errore complesso della CPU non correggibile.</span><span class="sxs-lookup"><span data-stu-id="b2b1a-213">Uncorrectable CPU-complex error.</span></span><br/>                                                                                 |
| <span id="22"></span><dl> <span data-ttu-id="b2b1a-214"><dt>**22**</dt></span><span class="sxs-lookup"><span data-stu-id="b2b1a-214"><dt>**22**</dt></span></span> </dl> | <span data-ttu-id="b2b1a-215">Reimpostazione o cancellazione dell'area log.</span><span class="sxs-lookup"><span data-stu-id="b2b1a-215">Log Area Reset or Cleared.</span></span><br/>                                                                                       |
| <span id="23"></span><dl> <span data-ttu-id="b2b1a-216"><dt>**23**</dt></span><span class="sxs-lookup"><span data-stu-id="b2b1a-216"><dt>**23**</dt></span></span> </dl> | <span data-ttu-id="b2b1a-217">Avvio del sistema.</span><span class="sxs-lookup"><span data-stu-id="b2b1a-217">System boot.</span></span> <span data-ttu-id="b2b1a-218">Se implementata, questa voce di log è sicuramente la prima scritta in un qualsiasi avvio del sistema.</span><span class="sxs-lookup"><span data-stu-id="b2b1a-218">If implemented, this log entry is guaranteed to be the first one written on any system boot.</span></span><br/>        |



 

</dd> <dt>

<span data-ttu-id="b2b1a-219">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="b2b1a-219">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2b1a-220">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b2b1a-220">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b2b1a-221">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b2b1a-221">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b2b1a-222">Tipo di messaggio del log eventi.</span><span class="sxs-lookup"><span data-stu-id="b2b1a-222">Type of event log message.</span></span> <span data-ttu-id="b2b1a-223">Questi messaggi corrispondono ai codici dei messaggi del registro eventi utilizzati per inserire i messaggi del registro eventi dal provider di consumer del registro eventi di Windows quando riceve uno degli eventi.</span><span class="sxs-lookup"><span data-stu-id="b2b1a-223">These messages correspond to the event log message codes used to insert event log messages by the Windows event log consumer provider when it receives one of the events.</span></span>

</dd> <dt>

<span data-ttu-id="b2b1a-224">**bit di convalida \_**</span><span class="sxs-lookup"><span data-stu-id="b2b1a-224">**VALIDATION\_BITS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2b1a-225">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b2b1a-225">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b2b1a-226">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b2b1a-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b2b1a-227">Bit di convalida usati per indicare la validità dei campi successivi.</span><span class="sxs-lookup"><span data-stu-id="b2b1a-227">Validation bits used to indicate the validity of the subsequent fields.</span></span> <span data-ttu-id="b2b1a-228">Il valore 1 (0x1) indica che l' **\_ evento SMBIOS** è valido.</span><span class="sxs-lookup"><span data-stu-id="b2b1a-228">A value of 1 (0x1) means that the **SMBIOS\_EVENT** is valid.</span></span>

<span data-ttu-id="b2b1a-229">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b2b1a-229">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b2b1a-230">Commenti</span><span class="sxs-lookup"><span data-stu-id="b2b1a-230">Remarks</span></span>

<span data-ttu-id="b2b1a-231">La classe **MSMCAEvent \_ SMBIOSError** è derivata da [**WmiEvent**](wmievent.md).</span><span class="sxs-lookup"><span data-stu-id="b2b1a-231">The **MSMCAEvent\_SMBIOSError** class is derived from [**WMIEvent**](wmievent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b2b1a-232">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b2b1a-232">Requirements</span></span>



| <span data-ttu-id="b2b1a-233">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2b1a-233">Requirement</span></span> | <span data-ttu-id="b2b1a-234">Valore</span><span class="sxs-lookup"><span data-stu-id="b2b1a-234">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b2b1a-235">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b2b1a-235">Minimum supported client</span></span><br/> | <span data-ttu-id="b2b1a-236">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b2b1a-236">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="b2b1a-237">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b2b1a-237">Minimum supported server</span></span><br/> | <span data-ttu-id="b2b1a-238">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b2b1a-238">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="b2b1a-239">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b2b1a-239">Namespace</span></span><br/>                | <span data-ttu-id="b2b1a-240">\\WMI radice</span><span class="sxs-lookup"><span data-stu-id="b2b1a-240">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="b2b1a-241">MOF</span><span class="sxs-lookup"><span data-stu-id="b2b1a-241">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b2b1a-242"><dt>Wmicore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b2b1a-242"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="b2b1a-243">DLL</span><span class="sxs-lookup"><span data-stu-id="b2b1a-243">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b2b1a-244"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b2b1a-244"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2b1a-245">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b2b1a-245">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2b1a-246">Classi MSMCA</span><span class="sxs-lookup"><span data-stu-id="b2b1a-246">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="b2b1a-247">**WMIEvent**</span><span class="sxs-lookup"><span data-stu-id="b2b1a-247">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 

