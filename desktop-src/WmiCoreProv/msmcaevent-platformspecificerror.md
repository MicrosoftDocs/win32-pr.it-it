---
description: Indica un errore specifico della piattaforma MCA (Machine Check Architecture). Questa classe è disponibile solo nei sistemi Windows a 64 bit.
ms.assetid: 409641d5-3451-4d26-88d1-bfd0e55db257
title: Classe MSMCAEvent_PlatformSpecificError
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_PlatformSpecificError
- MSMCAEvent_PlatformSpecificError.Active
- MSMCAEvent_PlatformSpecificError.AdditionalErrors
- MSMCAEvent_PlatformSpecificError.Cpu
- MSMCAEvent_PlatformSpecificError.ErrorSeverity
- MSMCAEvent_PlatformSpecificError.InstanceName
- MSMCAEvent_PlatformSpecificError.OEM_COMPONENT_ID
- MSMCAEvent_PlatformSpecificError.PLATFORM_BUS_SPECIFIC_DATA
- MSMCAEvent_PlatformSpecificError.PLATFORM_ERROR_STATUS
- MSMCAEvent_PlatformSpecificError.PLATFORM_REQUESTOR_ID
- MSMCAEvent_PlatformSpecificError.PLATFORM_RESPONDER_ID
- MSMCAEvent_PlatformSpecificError.PLATFORM_TARGET_ID
- MSMCAEvent_PlatformSpecificError.RawRecord
- MSMCAEvent_PlatformSpecificError.RecordId
- MSMCAEvent_PlatformSpecificError.Size
- MSMCAEvent_PlatformSpecificError.Type
- MSMCAEvent_PlatformSpecificError.VALIDATION_BITS
- MSMCAEvent_PlatformSpecificError.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 51993c8c41206dac8f4c944d24fa59ae7b689f92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484909"
---
# <a name="msmcaevent_platformspecificerror-class"></a><span data-ttu-id="9d156-104">\_Classe MSMCAEvent PlatformSpecificError</span><span class="sxs-lookup"><span data-stu-id="9d156-104">MSMCAEvent\_PlatformSpecificError class</span></span>

<span data-ttu-id="9d156-105">La classe **MSMCAEvent \_ PlatformSpecificError** indica un errore specifico della piattaforma MCA (Machine Check Architecture).</span><span class="sxs-lookup"><span data-stu-id="9d156-105">The **MSMCAEvent\_PlatformSpecificError** class indicates a Machine Check Architecture (MCA) platform-specific error.</span></span> <span data-ttu-id="9d156-106">Questa classe è disponibile solo nei sistemi Windows a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="9d156-106">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="9d156-107">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="9d156-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="9d156-108">Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="9d156-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d156-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9d156-109">Syntax</span></span>

``` syntax
class MSMCAEvent_PlatformSpecificError : WMIEvent
{
  boolean Active;
  uint32  AdditionalErrors;
  uint32  Cpu;
  uint8   ErrorSeverity;
  string  InstanceName;
  uint8   OEM_COMPONENT_ID;
  uint64  PLATFORM_BUS_SPECIFIC_DATA;
  uint64  PLATFORM_ERROR_STATUS;
  uint64  PLATFORM_REQUESTOR_ID;
  uint64  PLATFORM_RESPONDER_ID;
  uint64  PLATFORM_TARGET_ID;
  uint8   RawRecord[];
  uint64  RecordId;
  uint32  Size;
  uint32  Type;
  uint64  VALIDATION_BITS;
  uint32  LogToEventlog;
};
```

## <a name="members"></a><span data-ttu-id="9d156-110">Members</span><span class="sxs-lookup"><span data-stu-id="9d156-110">Members</span></span>

<span data-ttu-id="9d156-111">La **classe \_ PlatformSpecificError di MSMCAEvent** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="9d156-111">The **MSMCAEvent\_PlatformSpecificError** class has these types of members:</span></span>

-   [<span data-ttu-id="9d156-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9d156-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9d156-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9d156-113">Properties</span></span>

<span data-ttu-id="9d156-114">La **classe \_ PlatformSpecificError di MSMCAEvent** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="9d156-114">The **MSMCAEvent\_PlatformSpecificError** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9d156-115">**Attivo**</span><span class="sxs-lookup"><span data-stu-id="9d156-115">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d156-116">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="9d156-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9d156-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9d156-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d156-118">**True** se questa istanza della classe è attiva; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="9d156-118">**TRUE**, if this instance of the class is active; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="9d156-119">**AdditionalErrors**</span><span class="sxs-lookup"><span data-stu-id="9d156-119">**AdditionalErrors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d156-120">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9d156-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d156-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9d156-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d156-122">Numero di errori aggiuntivi nel record.</span><span class="sxs-lookup"><span data-stu-id="9d156-122">Number of additional errors in the record.</span></span>

</dd> <dt>

<span data-ttu-id="9d156-123">**CPU**</span><span class="sxs-lookup"><span data-stu-id="9d156-123">**Cpu**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d156-124">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9d156-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d156-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9d156-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d156-126">CPU che ha segnalato l'errore.</span><span class="sxs-lookup"><span data-stu-id="9d156-126">CPU that reported the error.</span></span> <span data-ttu-id="9d156-127">Questa proprietà si applica solo a un sistema multiprocessore in cui al primo processore viene assegnato il numero 0, al secondo processore viene assegnato il numero 1 e così via.</span><span class="sxs-lookup"><span data-stu-id="9d156-127">This property only applies to a multiprocessor system in which the first processor is assigned the number 0, the second processor is assigned the number 1, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="9d156-128">**ErrorSeverity**</span><span class="sxs-lookup"><span data-stu-id="9d156-128">**ErrorSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d156-129">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="9d156-129">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="9d156-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9d156-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d156-131">Livello di gravità dell'errore segnalato.</span><span class="sxs-lookup"><span data-stu-id="9d156-131">Severity level of the error reported.</span></span>



| <span data-ttu-id="9d156-132">Valore</span><span class="sxs-lookup"><span data-stu-id="9d156-132">Value</span></span>                                                                                                | <span data-ttu-id="9d156-133">Significato</span><span class="sxs-lookup"><span data-stu-id="9d156-133">Meaning</span></span>                |
|------------------------------------------------------------------------------------------------------|------------------------|
| <span id="0"></span><dl> <span data-ttu-id="9d156-134"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="9d156-134"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="9d156-135">Recuperabile</span><span class="sxs-lookup"><span data-stu-id="9d156-135">Recoverable</span></span><br/> |
| <span id="1"></span><dl> <span data-ttu-id="9d156-136"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="9d156-136"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="9d156-137">Fatal</span><span class="sxs-lookup"><span data-stu-id="9d156-137">Fatal</span></span><br/>       |
| <span id="2"></span><dl> <span data-ttu-id="9d156-138"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="9d156-138"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="9d156-139">Correggibile</span><span class="sxs-lookup"><span data-stu-id="9d156-139">Correctable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="9d156-140">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="9d156-140">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d156-141">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9d156-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d156-142">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9d156-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9d156-143">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9d156-143">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9d156-144">Identificatore univoco di questa istanza della classe.</span><span class="sxs-lookup"><span data-stu-id="9d156-144">Unique identifier of this instance of the class.</span></span>

</dd> <dt>

<span data-ttu-id="9d156-145">**LogToEventlog**</span><span class="sxs-lookup"><span data-stu-id="9d156-145">**LogToEventlog**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d156-146">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9d156-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d156-147">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9d156-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d156-148">Se è 0 (zero), questo evento non viene registrato nel registro eventi di sistema.</span><span class="sxs-lookup"><span data-stu-id="9d156-148">If 0 (zero) then this event is not logged to the system event log.</span></span>

</dd> <dt>

<span data-ttu-id="9d156-149">**\_ID componente \_ OEM**</span><span class="sxs-lookup"><span data-stu-id="9d156-149">**OEM\_COMPONENT\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d156-150">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="9d156-150">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="9d156-151">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9d156-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d156-152">Identificatore univoco del componente che segnala l'errore.</span><span class="sxs-lookup"><span data-stu-id="9d156-152">Unique identifier of the component that reports the error.</span></span>

</dd> <dt>

<span data-ttu-id="9d156-153">**\_ \_ dati specifici del bus di piattaforma \_**</span><span class="sxs-lookup"><span data-stu-id="9d156-153">**PLATFORM\_BUS\_SPECIFIC\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d156-154">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9d156-154">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9d156-155">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9d156-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d156-156">Dati dipendenti dal bus specifici dell'OEM.</span><span class="sxs-lookup"><span data-stu-id="9d156-156">OEM-specific, bus-dependent data.</span></span>

<span data-ttu-id="9d156-157">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9d156-157">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="9d156-158">**\_stato di errore della piattaforma \_**</span><span class="sxs-lookup"><span data-stu-id="9d156-158">**PLATFORM\_ERROR\_STATUS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d156-159">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9d156-159">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9d156-160">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9d156-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d156-161">Stato di errore della piattaforma generica.</span><span class="sxs-lookup"><span data-stu-id="9d156-161">Generic platform error status.</span></span>

<span data-ttu-id="9d156-162">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9d156-162">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="9d156-163">**\_ID richiedente \_ piattaforma**</span><span class="sxs-lookup"><span data-stu-id="9d156-163">**PLATFORM\_REQUESTOR\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d156-164">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9d156-164">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9d156-165">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9d156-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d156-166">Identificatore del richiedente al momento dell'evento.</span><span class="sxs-lookup"><span data-stu-id="9d156-166">Requestor identifier at the time of the event.</span></span>

<span data-ttu-id="9d156-167">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9d156-167">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="9d156-168">**\_ID risponditore \_ piattaforma**</span><span class="sxs-lookup"><span data-stu-id="9d156-168">**PLATFORM\_RESPONDER\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d156-169">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9d156-169">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9d156-170">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9d156-170">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d156-171">Identificatore del risponditore al momento dell'evento.</span><span class="sxs-lookup"><span data-stu-id="9d156-171">Responder identifier at the time of the event.</span></span>

<span data-ttu-id="9d156-172">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9d156-172">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="9d156-173">**\_ID di destinazione piattaforma \_**</span><span class="sxs-lookup"><span data-stu-id="9d156-173">**PLATFORM\_TARGET\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d156-174">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9d156-174">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9d156-175">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9d156-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d156-176">Identificatore di destinazione al momento dell'evento.</span><span class="sxs-lookup"><span data-stu-id="9d156-176">Target identifier at the time of the event.</span></span>

<span data-ttu-id="9d156-177">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9d156-177">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="9d156-178">**RawRecord**</span><span class="sxs-lookup"><span data-stu-id="9d156-178">**RawRecord**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d156-179">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="9d156-179">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="9d156-180">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9d156-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d156-181">Matrice di byte che contiene il record di errore non elaborato presentato a Windows da System Abstraction Layer (SAL).</span><span class="sxs-lookup"><span data-stu-id="9d156-181">Array of bytes that contains the raw error record as presented to Windows by the system abstraction layer (SAL).</span></span> <span data-ttu-id="9d156-182">Il numero di elementi nella matrice è specificato dalla proprietà **size** .</span><span class="sxs-lookup"><span data-stu-id="9d156-182">The number of elements in the array is specified by the **Size** property.</span></span>

</dd> <dt>

<span data-ttu-id="9d156-183">**RecordId**</span><span class="sxs-lookup"><span data-stu-id="9d156-183">**RecordId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d156-184">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9d156-184">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9d156-185">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9d156-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d156-186">Identificatore del record di errore per l'errore.</span><span class="sxs-lookup"><span data-stu-id="9d156-186">Record identifier of the error record for this error.</span></span>

<span data-ttu-id="9d156-187">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9d156-187">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="9d156-188">**Dimensioni**</span><span class="sxs-lookup"><span data-stu-id="9d156-188">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d156-189">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9d156-189">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d156-190">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9d156-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d156-191">Dimensioni del record di errore non elaborato.</span><span class="sxs-lookup"><span data-stu-id="9d156-191">Size of the raw error record.</span></span>

</dd> <dt>

<span data-ttu-id="9d156-192">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="9d156-192">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d156-193">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9d156-193">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d156-194">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9d156-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d156-195">Tipo di messaggio del log eventi.</span><span class="sxs-lookup"><span data-stu-id="9d156-195">Type of event log message.</span></span> <span data-ttu-id="9d156-196">Questi messaggi corrispondono ai codici dei messaggi del registro eventi utilizzati per inserire i messaggi del registro eventi dal provider di consumer del registro eventi di Windows quando riceve uno degli eventi.</span><span class="sxs-lookup"><span data-stu-id="9d156-196">These messages correspond to the event log message codes used to insert event log messages by the Windows event log consumer provider when it receives one of the events.</span></span>

</dd> <dt>

<span data-ttu-id="9d156-197">**bit di convalida \_**</span><span class="sxs-lookup"><span data-stu-id="9d156-197">**VALIDATION\_BITS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d156-198">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9d156-198">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9d156-199">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9d156-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d156-200">Bit di convalida usati per indicare la validità dei campi successivi.</span><span class="sxs-lookup"><span data-stu-id="9d156-200">Validation bits used to indicate the validity of the subsequent fields.</span></span>



| <span data-ttu-id="9d156-201">Valore</span><span class="sxs-lookup"><span data-stu-id="9d156-201">Value</span></span>                                                                                                                                         | <span data-ttu-id="9d156-202">Significato</span><span class="sxs-lookup"><span data-stu-id="9d156-202">Meaning</span></span>                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span id="1_0x1"></span><span id="1_0X1"></span><dl> <span data-ttu-id="9d156-203"><dt>**1 0x1**</dt></span><span class="sxs-lookup"><span data-stu-id="9d156-203"><dt>**1 0x1**</dt></span></span> </dl>          | <span data-ttu-id="9d156-204">**Piattaforma \_ \_Lo stato di errore** è valido.</span><span class="sxs-lookup"><span data-stu-id="9d156-204">**PLATFORM\_ERROR\_STATUS** is valid.</span></span><br/>            |
| <span id="2_0x2"></span><span id="2_0X2"></span><dl> <span data-ttu-id="9d156-205"><dt>**2 0x2**</dt></span><span class="sxs-lookup"><span data-stu-id="9d156-205"><dt>**2 0x2**</dt></span></span> </dl>          | <span data-ttu-id="9d156-206">**Piattaforma \_ L' \_ \_ ID del richiedente di errore** è valido.</span><span class="sxs-lookup"><span data-stu-id="9d156-206">**PLATFORM\_ERROR\_REQUESTOR\_ID** is valid.</span></span><br/>     |
| <span id="4_0x4"></span><span id="4_0X4"></span><dl> <span data-ttu-id="9d156-207"><dt>**4 0x4**</dt></span><span class="sxs-lookup"><span data-stu-id="9d156-207"><dt>**4 0x4**</dt></span></span> </dl>          | <span data-ttu-id="9d156-208">**Piattaforma \_ \_ \_ ID risponditore errore** valido.</span><span class="sxs-lookup"><span data-stu-id="9d156-208">**PLATFORM\_ERROR\_RESPONDER\_ID** is valid.</span></span><br/>     |
| <span id="8_0x8"></span><span id="8_0X8"></span><dl> <span data-ttu-id="9d156-209"><dt>**8 0x8**</dt></span><span class="sxs-lookup"><span data-stu-id="9d156-209"><dt>**8 0x8**</dt></span></span> </dl>          | <span data-ttu-id="9d156-210">**Piattaforma \_ L' \_ \_ ID di destinazione dell'errore** è valido.</span><span class="sxs-lookup"><span data-stu-id="9d156-210">**PLATFORM\_ERROR\_TARGET\_ID** is valid.</span></span><br/>        |
| <span id="16_0x10"></span><span id="16_0X10"></span><dl> <span data-ttu-id="9d156-211"><dt>**16 0x10**</dt></span><span class="sxs-lookup"><span data-stu-id="9d156-211"><dt>**16 0x10**</dt></span></span> </dl>    | <span data-ttu-id="9d156-212">**Piattaforma \_ \_ \_ I dati specifici degli errori** sono validi.</span><span class="sxs-lookup"><span data-stu-id="9d156-212">**PLATFORM\_ERROR\_SPECIFIC\_DATA** is valid.</span></span><br/>    |
| <span id="32_0x20"></span><span id="32_0X20"></span><dl> <span data-ttu-id="9d156-213"><dt>**32 0x20**</dt></span><span class="sxs-lookup"><span data-stu-id="9d156-213"><dt>**32 0x20**</dt></span></span> </dl>    | <span data-ttu-id="9d156-214">**Piattaforma \_ ERRORE \_ \_ ID OEM** valido.</span><span class="sxs-lookup"><span data-stu-id="9d156-214">**PLATFORM\_ERROR\_OEM\_ID** is valid.</span></span><br/>           |
| <span id="64_0x40"></span><span id="64_0X40"></span><dl> <span data-ttu-id="9d156-215"><dt>**64 0x40**</dt></span><span class="sxs-lookup"><span data-stu-id="9d156-215"><dt>**64 0x40**</dt></span></span> </dl>    | <span data-ttu-id="9d156-216">**Piattaforma \_ ERRORE \_ \_ \_ struct di dati OEM** valido.</span><span class="sxs-lookup"><span data-stu-id="9d156-216">**PLATFORM\_ERROR\_OEM\_DATA\_STRUCT** is valid.</span></span><br/> |
| <span id="128_0x80"></span><span id="128_0X80"></span><dl> <span data-ttu-id="9d156-217"><dt>**128 0x80**</dt></span><span class="sxs-lookup"><span data-stu-id="9d156-217"><dt>**128 0x80**</dt></span></span> </dl> | <span data-ttu-id="9d156-218">**Piattaforma \_ ERRORE \_ il \_ \_ percorso del dispositivo OEM** è valido.</span><span class="sxs-lookup"><span data-stu-id="9d156-218">**PLATFORM\_ERROR\_OEM\_DEVICE\_PATH** is valid.</span></span><br/> |



 

<span data-ttu-id="9d156-219">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9d156-219">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9d156-220">Commenti</span><span class="sxs-lookup"><span data-stu-id="9d156-220">Remarks</span></span>

<span data-ttu-id="9d156-221">La classe **MSMCAEvent \_ PlatformSpecificError** è derivata da [**WmiEvent**](wmievent.md).</span><span class="sxs-lookup"><span data-stu-id="9d156-221">The **MSMCAEvent\_PlatformSpecificError** class is derived from [**WMIEvent**](wmievent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9d156-222">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9d156-222">Requirements</span></span>



| <span data-ttu-id="9d156-223">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d156-223">Requirement</span></span> | <span data-ttu-id="9d156-224">Valore</span><span class="sxs-lookup"><span data-stu-id="9d156-224">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9d156-225">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9d156-225">Minimum supported client</span></span><br/> | <span data-ttu-id="9d156-226">Windows XP</span><span class="sxs-lookup"><span data-stu-id="9d156-226">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="9d156-227">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9d156-227">Minimum supported server</span></span><br/> | <span data-ttu-id="9d156-228">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9d156-228">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="9d156-229">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9d156-229">Namespace</span></span><br/>                | <span data-ttu-id="9d156-230">\\WMI radice</span><span class="sxs-lookup"><span data-stu-id="9d156-230">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="9d156-231">MOF</span><span class="sxs-lookup"><span data-stu-id="9d156-231">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9d156-232"><dt>Wmicore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9d156-232"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="9d156-233">DLL</span><span class="sxs-lookup"><span data-stu-id="9d156-233">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9d156-234"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9d156-234"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d156-235">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9d156-235">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d156-236">Classi MSMCA</span><span class="sxs-lookup"><span data-stu-id="9d156-236">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="9d156-237">**WMIEvent**</span><span class="sxs-lookup"><span data-stu-id="9d156-237">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 

