---
description: Indica che si è verificato un evento di sistema IPMI (Intelligent Platform Management Interface). L'errore viene scritto nel registro eventi di sistema di SMBIOS (SEL). Questa classe è disponibile solo nei sistemi Windows a 64 bit.
ms.assetid: 1964f850-ac55-4639-9205-2eb0996dbaae
title: Classe MSMCAEvent_SystemEventError
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_SystemEventError
- MSMCAEvent_SystemEventError.Active
- MSMCAEvent_SystemEventError.AdditionalErrors
- MSMCAEvent_SystemEventError.Cpu
- MSMCAEvent_SystemEventError.ErrorSeverity
- MSMCAEvent_SystemEventError.InstanceName
- MSMCAEvent_SystemEventError.RawRecord
- MSMCAEvent_SystemEventError.RecordId
- MSMCAEvent_SystemEventError.SEL_DATA1
- MSMCAEvent_SystemEventError.SEL_DATA2
- MSMCAEvent_SystemEventError.SEL_DATA3
- MSMCAEvent_SystemEventError.SEL_EVENT_DIR_TYPE
- MSMCAEvent_SystemEventError.SEL_EVM_REV
- MSMCAEvent_SystemEventError.SEL_GENERATOR_ID
- MSMCAEvent_SystemEventError.SEL_RECORD_ID
- MSMCAEvent_SystemEventError.SEL_RECORD_TYPE
- MSMCAEvent_SystemEventError.SEL_SENSOR_NUM
- MSMCAEvent_SystemEventError.SEL_SENSOR_TYPE
- MSMCAEvent_SystemEventError.SEL_TIME_STAMP
- MSMCAEvent_SystemEventError.Size
- MSMCAEvent_SystemEventError.Type
- MSMCAEvent_SystemEventError.VALIDATION_BITS
- MSMCAEvent_SystemEventError.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: f20f95fb5e1b1bf07b0f70c25d54122642b13569
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316590"
---
# <a name="msmcaevent_systemeventerror-class"></a><span data-ttu-id="b7f1e-105">\_Classe MSMCAEvent SystemEventError</span><span class="sxs-lookup"><span data-stu-id="b7f1e-105">MSMCAEvent\_SystemEventError class</span></span>

<span data-ttu-id="b7f1e-106">La classe **MSMCAEvent \_ SystemEventError** indica che si è verificato un evento di sistema IPMI (Intelligent Platform Management Interface).</span><span class="sxs-lookup"><span data-stu-id="b7f1e-106">The **MSMCAEvent\_SystemEventError** class indicates that an Intelligent Platform Management Interface (IPMI) system event has occurred.</span></span> <span data-ttu-id="b7f1e-107">L'errore viene scritto nel registro eventi di sistema di SMBIOS (SEL).</span><span class="sxs-lookup"><span data-stu-id="b7f1e-107">The error is written to the SMBIOS System Event Log (SEL).</span></span> <span data-ttu-id="b7f1e-108">Questa classe è disponibile solo nei sistemi Windows a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="b7f1e-108">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="b7f1e-109">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="b7f1e-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="b7f1e-110">Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="b7f1e-110">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7f1e-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b7f1e-111">Syntax</span></span>

``` syntax
class MSMCAEvent_SystemEventError : WMIEvent
{
  boolean Active;
  uint32  AdditionalErrors;
  uint32  Cpu;
  uint8   ErrorSeverity;
  string  InstanceName;
  uint8   RawRecord[];
  uint64  RecordId;
  uint8   SEL_DATA1;
  uint8   SEL_DATA2;
  uint8   SEL_DATA3;
  uint8   SEL_EVENT_DIR_TYPE;
  uint8   SEL_EVM_REV;
  uint16  SEL_GENERATOR_ID;
  uint16  SEL_RECORD_ID;
  uint8   SEL_RECORD_TYPE;
  uint8   SEL_SENSOR_NUM;
  uint8   SEL_SENSOR_TYPE;
  uint64  SEL_TIME_STAMP;
  uint32  Size;
  uint32  Type;
  uint64  VALIDATION_BITS;
  uint32  LogToEventlog;
};
```

## <a name="members"></a><span data-ttu-id="b7f1e-112">Members</span><span class="sxs-lookup"><span data-stu-id="b7f1e-112">Members</span></span>

<span data-ttu-id="b7f1e-113">La **classe \_ SystemEventError di MSMCAEvent** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="b7f1e-113">The **MSMCAEvent\_SystemEventError** class has these types of members:</span></span>

-   [<span data-ttu-id="b7f1e-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b7f1e-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b7f1e-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b7f1e-115">Properties</span></span>

<span data-ttu-id="b7f1e-116">La **classe \_ SystemEventError di MSMCAEvent** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="b7f1e-116">The **MSMCAEvent\_SystemEventError** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b7f1e-117">**Attivo**</span><span class="sxs-lookup"><span data-stu-id="b7f1e-117">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7f1e-118">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="b7f1e-118">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b7f1e-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b7f1e-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7f1e-120">**True** se questa istanza della classe è attiva; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="b7f1e-120">**TRUE**, if this instance of the class is active; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="b7f1e-121">**AdditionalErrors**</span><span class="sxs-lookup"><span data-stu-id="b7f1e-121">**AdditionalErrors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7f1e-122">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b7f1e-122">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b7f1e-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b7f1e-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7f1e-124">Numero di errori aggiuntivi nel record.</span><span class="sxs-lookup"><span data-stu-id="b7f1e-124">Number of additional errors in the record.</span></span>

</dd> <dt>

<span data-ttu-id="b7f1e-125">**CPU**</span><span class="sxs-lookup"><span data-stu-id="b7f1e-125">**Cpu**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7f1e-126">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b7f1e-126">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b7f1e-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b7f1e-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7f1e-128">CPU che ha segnalato l'errore.</span><span class="sxs-lookup"><span data-stu-id="b7f1e-128">CPU that reported the error.</span></span> <span data-ttu-id="b7f1e-129">Questa proprietà si applica solo a un sistema multiprocessore in cui al primo processore viene assegnato il numero 0, al secondo processore viene assegnato il numero 1 e così via.</span><span class="sxs-lookup"><span data-stu-id="b7f1e-129">This property only applies to a multiprocessor system in which the first processor is assigned the number 0, the second processor is assigned the number 1, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="b7f1e-130">**ErrorSeverity**</span><span class="sxs-lookup"><span data-stu-id="b7f1e-130">**ErrorSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7f1e-131">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="b7f1e-131">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="b7f1e-132">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b7f1e-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7f1e-133">Livello di gravità dell'errore segnalato.</span><span class="sxs-lookup"><span data-stu-id="b7f1e-133">Severity level of the error reported.</span></span>



| <span data-ttu-id="b7f1e-134">Valore</span><span class="sxs-lookup"><span data-stu-id="b7f1e-134">Value</span></span>                                                                                                | <span data-ttu-id="b7f1e-135">Significato</span><span class="sxs-lookup"><span data-stu-id="b7f1e-135">Meaning</span></span>                |
|------------------------------------------------------------------------------------------------------|------------------------|
| <span id="0"></span><dl> <span data-ttu-id="b7f1e-136"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="b7f1e-136"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="b7f1e-137">Recuperabile</span><span class="sxs-lookup"><span data-stu-id="b7f1e-137">Recoverable</span></span><br/> |
| <span id="1"></span><dl> <span data-ttu-id="b7f1e-138"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="b7f1e-138"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="b7f1e-139">Fatal</span><span class="sxs-lookup"><span data-stu-id="b7f1e-139">Fatal</span></span><br/>       |
| <span id="2"></span><dl> <span data-ttu-id="b7f1e-140"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="b7f1e-140"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="b7f1e-141">Correggibile</span><span class="sxs-lookup"><span data-stu-id="b7f1e-141">Correctable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="b7f1e-142">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="b7f1e-142">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7f1e-143">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b7f1e-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7f1e-144">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b7f1e-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7f1e-145">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b7f1e-145">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b7f1e-146">Identificatore univoco di questa istanza della classe.</span><span class="sxs-lookup"><span data-stu-id="b7f1e-146">Unique identifier of this instance of the class.</span></span>

</dd> <dt>

<span data-ttu-id="b7f1e-147">**LogToEventlog**</span><span class="sxs-lookup"><span data-stu-id="b7f1e-147">**LogToEventlog**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7f1e-148">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b7f1e-148">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b7f1e-149">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b7f1e-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7f1e-150">Se è 0 (zero), questo evento non viene registrato nel registro eventi di sistema.</span><span class="sxs-lookup"><span data-stu-id="b7f1e-150">If 0 (zero) then this event is not logged to the system event log.</span></span>

</dd> <dt>

<span data-ttu-id="b7f1e-151">**RawRecord**</span><span class="sxs-lookup"><span data-stu-id="b7f1e-151">**RawRecord**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7f1e-152">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="b7f1e-152">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="b7f1e-153">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b7f1e-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7f1e-154">Matrice di byte che contiene il record di errore non elaborato.</span><span class="sxs-lookup"><span data-stu-id="b7f1e-154">Array of bytes that contains the raw error record.</span></span> <span data-ttu-id="b7f1e-155">Numero di elementi nella matrice specificata dalla proprietà **size** .</span><span class="sxs-lookup"><span data-stu-id="b7f1e-155">The number of elements in the array that the **Size** property specifies.</span></span>

</dd> <dt>

<span data-ttu-id="b7f1e-156">**RecordId**</span><span class="sxs-lookup"><span data-stu-id="b7f1e-156">**RecordId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7f1e-157">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b7f1e-157">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b7f1e-158">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b7f1e-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7f1e-159">Identificatore del record di errore per l'errore.</span><span class="sxs-lookup"><span data-stu-id="b7f1e-159">Record identifier of the error record for this error.</span></span>

<span data-ttu-id="b7f1e-160">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b7f1e-160">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="b7f1e-161">**\_Data1 SEL**</span><span class="sxs-lookup"><span data-stu-id="b7f1e-161">**SEL\_DATA1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7f1e-162">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="b7f1e-162">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="b7f1e-163">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b7f1e-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7f1e-164">Campo dati evento 1.</span><span class="sxs-lookup"><span data-stu-id="b7f1e-164">Event data field 1.</span></span>

</dd> <dt>

<span data-ttu-id="b7f1e-165">**\_Data2 SEL**</span><span class="sxs-lookup"><span data-stu-id="b7f1e-165">**SEL\_DATA2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7f1e-166">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="b7f1e-166">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="b7f1e-167">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b7f1e-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7f1e-168">Campo dati evento 2.</span><span class="sxs-lookup"><span data-stu-id="b7f1e-168">Event data field 2.</span></span>

</dd> <dt>

<span data-ttu-id="b7f1e-169">**\_Data3 SEL**</span><span class="sxs-lookup"><span data-stu-id="b7f1e-169">**SEL\_DATA3**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7f1e-170">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="b7f1e-170">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="b7f1e-171">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b7f1e-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7f1e-172">Campo dati evento 3.</span><span class="sxs-lookup"><span data-stu-id="b7f1e-172">Event data field 3.</span></span>

</dd> <dt>

<span data-ttu-id="b7f1e-173">**\_ \_ tipo dir evento \_ SEL**</span><span class="sxs-lookup"><span data-stu-id="b7f1e-173">**SEL\_EVENT\_DIR\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7f1e-174">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="b7f1e-174">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="b7f1e-175">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b7f1e-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7f1e-176">Tipo di directory degli eventi.</span><span class="sxs-lookup"><span data-stu-id="b7f1e-176">Event directory type.</span></span>

</dd> <dt>

<span data-ttu-id="b7f1e-177">**SEL \_ EVM \_ REV**</span><span class="sxs-lookup"><span data-stu-id="b7f1e-177">**SEL\_EVM\_REV**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7f1e-178">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="b7f1e-178">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="b7f1e-179">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b7f1e-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7f1e-180">Versione del formato del messaggio di errore.</span><span class="sxs-lookup"><span data-stu-id="b7f1e-180">Format version of the error message.</span></span>

</dd> <dt>

<span data-ttu-id="b7f1e-181">**\_ID generatore \_ SEL**</span><span class="sxs-lookup"><span data-stu-id="b7f1e-181">**SEL\_GENERATOR\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7f1e-182">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b7f1e-182">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b7f1e-183">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b7f1e-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7f1e-184">Identificatore software, se l'evento è stato generato dal software.</span><span class="sxs-lookup"><span data-stu-id="b7f1e-184">Software identifier, if the event was software-generated.</span></span>

</dd> <dt>

<span data-ttu-id="b7f1e-185">**\_ID record \_ SEL**</span><span class="sxs-lookup"><span data-stu-id="b7f1e-185">**SEL\_RECORD\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7f1e-186">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b7f1e-186">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b7f1e-187">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b7f1e-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7f1e-188">Identificatore del record usato per l'accesso al registro eventi di sistema di SMBIOS (SEL).</span><span class="sxs-lookup"><span data-stu-id="b7f1e-188">Record identifier used for SMBIOS system event log (SEL) access.</span></span>

</dd> <dt>

<span data-ttu-id="b7f1e-189">**\_tipo di record SEL \_**</span><span class="sxs-lookup"><span data-stu-id="b7f1e-189">**SEL\_RECORD\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7f1e-190">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="b7f1e-190">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="b7f1e-191">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b7f1e-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7f1e-192">Tipo di record.</span><span class="sxs-lookup"><span data-stu-id="b7f1e-192">Record type.</span></span>

</dd> <dt>

<span data-ttu-id="b7f1e-193">**numero di \_ sensore SEL \_**</span><span class="sxs-lookup"><span data-stu-id="b7f1e-193">**SEL\_SENSOR\_NUM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7f1e-194">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="b7f1e-194">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="b7f1e-195">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b7f1e-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7f1e-196">Numero del sensore che ha generato l'evento.</span><span class="sxs-lookup"><span data-stu-id="b7f1e-196">Sensor number that generated the event.</span></span>

</dd> <dt>

<span data-ttu-id="b7f1e-197">**\_tipo di sensore SEL \_**</span><span class="sxs-lookup"><span data-stu-id="b7f1e-197">**SEL\_SENSOR\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7f1e-198">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="b7f1e-198">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="b7f1e-199">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b7f1e-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7f1e-200">Codice del tipo di sensore del sensore che ha generato l'evento.</span><span class="sxs-lookup"><span data-stu-id="b7f1e-200">Sensor type code of the sensor that generated the event.</span></span>

</dd> <dt>

<span data-ttu-id="b7f1e-201">**\_timestamp SEL \_**</span><span class="sxs-lookup"><span data-stu-id="b7f1e-201">**SEL\_TIME\_STAMP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7f1e-202">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b7f1e-202">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b7f1e-203">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b7f1e-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7f1e-204">Timestamp del log eventi.</span><span class="sxs-lookup"><span data-stu-id="b7f1e-204">Timestamp of the event log.</span></span>

<span data-ttu-id="b7f1e-205">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b7f1e-205">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="b7f1e-206">**Dimensioni**</span><span class="sxs-lookup"><span data-stu-id="b7f1e-206">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7f1e-207">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b7f1e-207">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b7f1e-208">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b7f1e-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7f1e-209">Dimensioni del record di errore non elaborato.</span><span class="sxs-lookup"><span data-stu-id="b7f1e-209">Size of the raw error record.</span></span>

</dd> <dt>

<span data-ttu-id="b7f1e-210">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="b7f1e-210">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7f1e-211">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b7f1e-211">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b7f1e-212">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b7f1e-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7f1e-213">Tipo di messaggio del log eventi.</span><span class="sxs-lookup"><span data-stu-id="b7f1e-213">Type of event log message.</span></span> <span data-ttu-id="b7f1e-214">Questi messaggi corrispondono ai codici dei messaggi del registro eventi utilizzati per inserire i messaggi del registro eventi dal provider di consumer del registro eventi di Windows quando riceve uno degli eventi.</span><span class="sxs-lookup"><span data-stu-id="b7f1e-214">These messages correspond to the event log message codes used to insert event log messages by the Windows event log consumer provider when it receives one of the events.</span></span>

</dd> <dt>

<span data-ttu-id="b7f1e-215">**bit di convalida \_**</span><span class="sxs-lookup"><span data-stu-id="b7f1e-215">**VALIDATION\_BITS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7f1e-216">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b7f1e-216">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b7f1e-217">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b7f1e-217">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7f1e-218">Bit di convalida usati per indicare la validità dei campi successivi.</span><span class="sxs-lookup"><span data-stu-id="b7f1e-218">Validation bits used to indicate the validity of the subsequent fields.</span></span>



| <span data-ttu-id="b7f1e-219">Valore</span><span class="sxs-lookup"><span data-stu-id="b7f1e-219">Value</span></span>                                                                                                                                            | <span data-ttu-id="b7f1e-220">Significato</span><span class="sxs-lookup"><span data-stu-id="b7f1e-220">Meaning</span></span>                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="1_0x1"></span><span id="1_0X1"></span><dl> <span data-ttu-id="b7f1e-221"><dt>**1 0x1**</dt></span><span class="sxs-lookup"><span data-stu-id="b7f1e-221"><dt>**1 0x1**</dt></span></span> </dl>             | <span data-ttu-id="b7f1e-222">**SEL \_ \_ID record** valido.</span><span class="sxs-lookup"><span data-stu-id="b7f1e-222">**SEL\_RECORD\_ID** is valid.</span></span><br/>    |
| <span id="2_0x2"></span><span id="2_0X2"></span><dl> <span data-ttu-id="b7f1e-223"><dt>**2 0x2**</dt></span><span class="sxs-lookup"><span data-stu-id="b7f1e-223"><dt>**2 0x2**</dt></span></span> </dl>             | <span data-ttu-id="b7f1e-224">**SEL \_ Il \_ tipo di record** è valido.</span><span class="sxs-lookup"><span data-stu-id="b7f1e-224">**SEL\_RECORD\_TYPE** is valid.</span></span><br/>  |
| <span id="4_0x4"></span><span id="4_0X4"></span><dl> <span data-ttu-id="b7f1e-225"><dt>**4 0x4**</dt></span><span class="sxs-lookup"><span data-stu-id="b7f1e-225"><dt>**4 0x4**</dt></span></span> </dl>             | <span data-ttu-id="b7f1e-226">**SEL \_ \_ID generatore** valido.</span><span class="sxs-lookup"><span data-stu-id="b7f1e-226">**SEL\_GENERATOR\_ID** is valid.</span></span><br/> |
| <span id="8_0x8"></span><span id="8_0X8"></span><dl> <span data-ttu-id="b7f1e-227"><dt>**8 0x8**</dt></span><span class="sxs-lookup"><span data-stu-id="b7f1e-227"><dt>**8 0x8**</dt></span></span> </dl>             | <span data-ttu-id="b7f1e-228">**SEL \_ EVM \_ REV** è valido.</span><span class="sxs-lookup"><span data-stu-id="b7f1e-228">**SEL\_EVM\_REV** is valid.</span></span><br/>      |
| <span id="16_0x10"></span><span id="16_0X10"></span><dl> <span data-ttu-id="b7f1e-229"><dt>**16 0x10**</dt></span><span class="sxs-lookup"><span data-stu-id="b7f1e-229"><dt>**16 0x10**</dt></span></span> </dl>       | <span data-ttu-id="b7f1e-230">**SEL \_ \_Tipo di sensore** valido.</span><span class="sxs-lookup"><span data-stu-id="b7f1e-230">**SEL\_SENSOR\_TYPE** is valid.</span></span><br/>  |
| <span id="32_0x20"></span><span id="32_0X20"></span><dl> <span data-ttu-id="b7f1e-231"><dt>**32 0x20**</dt></span><span class="sxs-lookup"><span data-stu-id="b7f1e-231"><dt>**32 0x20**</dt></span></span> </dl>       | <span data-ttu-id="b7f1e-232">**SEL \_ \_Num del sensore** valido.</span><span class="sxs-lookup"><span data-stu-id="b7f1e-232">**SEL\_SENSOR\_NUM** is valid.</span></span><br/>   |
| <span id="64_0x40"></span><span id="64_0X40"></span><dl> <span data-ttu-id="b7f1e-233"><dt>**64 0x40**</dt></span><span class="sxs-lookup"><span data-stu-id="b7f1e-233"><dt>**64 0x40**</dt></span></span> </dl>       | <span data-ttu-id="b7f1e-234">**SEL \_ La \_ directory dell'evento** è valida.</span><span class="sxs-lookup"><span data-stu-id="b7f1e-234">**SEL\_EVENT\_DIR** is valid.</span></span><br/>    |
| <span id="128_0x80"></span><span id="128_0X80"></span><dl> <span data-ttu-id="b7f1e-235"><dt>**128 0x80**</dt></span><span class="sxs-lookup"><span data-stu-id="b7f1e-235"><dt>**128 0x80**</dt></span></span> </dl>    | <span data-ttu-id="b7f1e-236">**SEL \_ L'evento \_ Data1** è valido.</span><span class="sxs-lookup"><span data-stu-id="b7f1e-236">**SEL\_EVENT\_DATA1** is valid.</span></span><br/>  |
| <span id="256_0x100"></span><span id="256_0X100"></span><dl> <span data-ttu-id="b7f1e-237"><dt>**256 0x100**</dt></span><span class="sxs-lookup"><span data-stu-id="b7f1e-237"><dt>**256 0x100**</dt></span></span> </dl> | <span data-ttu-id="b7f1e-238">**SEL \_ L'evento \_ data2** è valido.</span><span class="sxs-lookup"><span data-stu-id="b7f1e-238">**SEL\_EVENT\_DATA2** is valid.</span></span><br/>  |
| <span id="512_0x200"></span><span id="512_0X200"></span><dl> <span data-ttu-id="b7f1e-239"><dt>**512 0x200**</dt></span><span class="sxs-lookup"><span data-stu-id="b7f1e-239"><dt>**512 0x200**</dt></span></span> </dl> | <span data-ttu-id="b7f1e-240">**SEL \_ L'evento \_ data3** è valido.</span><span class="sxs-lookup"><span data-stu-id="b7f1e-240">**SEL\_EVENT\_DATA3** is valid.</span></span><br/>  |



 

<span data-ttu-id="b7f1e-241">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b7f1e-241">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b7f1e-242">Commenti</span><span class="sxs-lookup"><span data-stu-id="b7f1e-242">Remarks</span></span>

<span data-ttu-id="b7f1e-243">La classe **MSMCAEvent \_ SystemEventError** è derivata da [**WmiEvent**](wmievent.md).</span><span class="sxs-lookup"><span data-stu-id="b7f1e-243">The **MSMCAEvent\_SystemEventError** class is derived from [**WMIEvent**](wmievent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b7f1e-244">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b7f1e-244">Requirements</span></span>



| <span data-ttu-id="b7f1e-245">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7f1e-245">Requirement</span></span> | <span data-ttu-id="b7f1e-246">Valore</span><span class="sxs-lookup"><span data-stu-id="b7f1e-246">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b7f1e-247">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b7f1e-247">Minimum supported client</span></span><br/> | <span data-ttu-id="b7f1e-248">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b7f1e-248">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="b7f1e-249">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b7f1e-249">Minimum supported server</span></span><br/> | <span data-ttu-id="b7f1e-250">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b7f1e-250">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="b7f1e-251">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b7f1e-251">Namespace</span></span><br/>                | <span data-ttu-id="b7f1e-252">\\WMI radice</span><span class="sxs-lookup"><span data-stu-id="b7f1e-252">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="b7f1e-253">MOF</span><span class="sxs-lookup"><span data-stu-id="b7f1e-253">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b7f1e-254"><dt>Wmicore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b7f1e-254"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="b7f1e-255">DLL</span><span class="sxs-lookup"><span data-stu-id="b7f1e-255">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b7f1e-256"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b7f1e-256"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7f1e-257">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b7f1e-257">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7f1e-258">Classi MSMCA</span><span class="sxs-lookup"><span data-stu-id="b7f1e-258">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="b7f1e-259">**WMIEvent**</span><span class="sxs-lookup"><span data-stu-id="b7f1e-259">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 

