---
description: Rappresenta un evento di errore della CPU. Questa classe è disponibile solo nei sistemi Windows a 64 bit.
ms.assetid: 4ee4aa51-a965-4569-b53c-0ba21bf42752
title: Classe MSMCAEvent_CPUError
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_CPUError
- MSMCAEvent_CPUError.Active
- MSMCAEvent_CPUError.AdditionalErrors
- MSMCAEvent_CPUError.Cpu
- MSMCAEvent_CPUError.ErrorSeverity
- MSMCAEvent_CPUError.InstanceName
- MSMCAEvent_CPUError.Level
- MSMCAEvent_CPUError.RawRecord
- MSMCAEvent_CPUError.RecordId
- MSMCAEvent_CPUError.Size
- MSMCAEvent_CPUError.Type
- MSMCAEvent_CPUError.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: dff990b46d730a1e8b54ef99a24a686745e3dacf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526107"
---
# <a name="msmcaevent_cpuerror-class"></a><span data-ttu-id="a0e90-104">\_Classe MSMCAEvent CPUError</span><span class="sxs-lookup"><span data-stu-id="a0e90-104">MSMCAEvent\_CPUError class</span></span>

<span data-ttu-id="a0e90-105">La classe **MSMCAEvent \_ CPUError** rappresenta un evento di errore della CPU.</span><span class="sxs-lookup"><span data-stu-id="a0e90-105">The **MSMCAEvent\_CPUError** class represents a CPU error event.</span></span> <span data-ttu-id="a0e90-106">Questa classe è disponibile solo nei sistemi Windows a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="a0e90-106">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="a0e90-107">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="a0e90-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="a0e90-108">Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="a0e90-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0e90-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a0e90-109">Syntax</span></span>

``` syntax
class MSMCAEvent_CPUError : WmiEvent
{
  boolean Active;
  uint32  AdditionalErrors;
  uint32  Cpu;
  uint8   ErrorSeverity;
  string  InstanceName;
  uint32  Level;
  uint8   RawRecord[];
  uint64  RecordId;
  uint32  Size;
  uint32  Type;
  uint32  LogToEventlog;
};
```

## <a name="members"></a><span data-ttu-id="a0e90-110">Members</span><span class="sxs-lookup"><span data-stu-id="a0e90-110">Members</span></span>

<span data-ttu-id="a0e90-111">La **classe \_ CPUError di MSMCAEvent** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="a0e90-111">The **MSMCAEvent\_CPUError** class has these types of members:</span></span>

-   [<span data-ttu-id="a0e90-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a0e90-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a0e90-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a0e90-113">Properties</span></span>

<span data-ttu-id="a0e90-114">La **classe \_ CPUError di MSMCAEvent** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="a0e90-114">The **MSMCAEvent\_CPUError** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a0e90-115">**Attivo**</span><span class="sxs-lookup"><span data-stu-id="a0e90-115">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0e90-116">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="a0e90-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a0e90-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a0e90-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0e90-118">**True** se questa istanza della classe è attiva; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="a0e90-118">**TRUE**, if this instance of the class is active; otherwise **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="a0e90-119">**AdditionalErrors**</span><span class="sxs-lookup"><span data-stu-id="a0e90-119">**AdditionalErrors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0e90-120">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a0e90-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a0e90-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a0e90-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0e90-122">Numero di errori aggiuntivi nel record MCA.</span><span class="sxs-lookup"><span data-stu-id="a0e90-122">Number of additional errors in the MCA record.</span></span>

</dd> <dt>

<span data-ttu-id="a0e90-123">**CPU**</span><span class="sxs-lookup"><span data-stu-id="a0e90-123">**Cpu**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0e90-124">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a0e90-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a0e90-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a0e90-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0e90-126">CPU che ha segnalato l'errore.</span><span class="sxs-lookup"><span data-stu-id="a0e90-126">CPU that reported the error.</span></span> <span data-ttu-id="a0e90-127">Questa proprietà si applica solo a un sistema multiprocessore in cui al primo processore viene assegnato il numero 0, al secondo processore viene assegnato il numero 1 e così via.</span><span class="sxs-lookup"><span data-stu-id="a0e90-127">This property only applies to a multiprocessor system in which the first processor is assigned the number 0, the second processor is assigned the number 1, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="a0e90-128">**ErrorSeverity**</span><span class="sxs-lookup"><span data-stu-id="a0e90-128">**ErrorSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0e90-129">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="a0e90-129">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="a0e90-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a0e90-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0e90-131">Livello di gravità dell'errore segnalato.</span><span class="sxs-lookup"><span data-stu-id="a0e90-131">Severity level of the error reported.</span></span>



| <span data-ttu-id="a0e90-132">Valore</span><span class="sxs-lookup"><span data-stu-id="a0e90-132">Value</span></span>                                                                                                | <span data-ttu-id="a0e90-133">Significato</span><span class="sxs-lookup"><span data-stu-id="a0e90-133">Meaning</span></span>                |
|------------------------------------------------------------------------------------------------------|------------------------|
| <span id="0"></span><dl> <span data-ttu-id="a0e90-134"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="a0e90-134"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="a0e90-135">Recuperabile</span><span class="sxs-lookup"><span data-stu-id="a0e90-135">Recoverable</span></span><br/> |
| <span id="1"></span><dl> <span data-ttu-id="a0e90-136"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="a0e90-136"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="a0e90-137">Fatal</span><span class="sxs-lookup"><span data-stu-id="a0e90-137">Fatal</span></span><br/>       |
| <span id="2"></span><dl> <span data-ttu-id="a0e90-138"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="a0e90-138"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="a0e90-139">Correggibile</span><span class="sxs-lookup"><span data-stu-id="a0e90-139">Correctable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="a0e90-140">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="a0e90-140">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0e90-141">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a0e90-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0e90-142">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a0e90-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0e90-143">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="a0e90-143">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="a0e90-144">Identificatore univoco per questa istanza della classe.</span><span class="sxs-lookup"><span data-stu-id="a0e90-144">Unique identifier for this instance of the class.</span></span>

</dd> <dt>

<span data-ttu-id="a0e90-145">**Level**</span><span class="sxs-lookup"><span data-stu-id="a0e90-145">**Level**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0e90-146">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a0e90-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a0e90-147">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a0e90-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0e90-148">Qualificatori: **WmiMissingData** (-1)</span><span class="sxs-lookup"><span data-stu-id="a0e90-148">Qualifiers: **WmiMissingData** (-1)</span></span>
</dt> </dl>

<span data-ttu-id="a0e90-149">Livello della cache, del buffer di traduzione (TLB) o della struttura micro-architettura in cui si è verificato l'errore.</span><span class="sxs-lookup"><span data-stu-id="a0e90-149">Level of cache, translation buffer (TLB), or micro-architectural structure where the error occurred.</span></span> <span data-ttu-id="a0e90-150">Il valore 0 (zero) indica il primo livello.</span><span class="sxs-lookup"><span data-stu-id="a0e90-150">A value of 0 (zero) indicates the first level.</span></span>

</dd> <dt>

<span data-ttu-id="a0e90-151">**LogToEventlog**</span><span class="sxs-lookup"><span data-stu-id="a0e90-151">**LogToEventlog**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0e90-152">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a0e90-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a0e90-153">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a0e90-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0e90-154">Se è zero, questo evento non viene registrato nel registro eventi di sistema.</span><span class="sxs-lookup"><span data-stu-id="a0e90-154">If zero then this event is not logged to the system event log.</span></span>

</dd> <dt>

<span data-ttu-id="a0e90-155">**RawRecord**</span><span class="sxs-lookup"><span data-stu-id="a0e90-155">**RawRecord**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0e90-156">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="a0e90-156">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="a0e90-157">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a0e90-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0e90-158">Matrice di byte che contiene il record di errore non elaborato.</span><span class="sxs-lookup"><span data-stu-id="a0e90-158">Array of bytes that contains the raw error record.</span></span> <span data-ttu-id="a0e90-159">Numero di elementi nella matrice specificata dalla proprietà **size** .</span><span class="sxs-lookup"><span data-stu-id="a0e90-159">The number of elements in the array that the **Size** property specifies.</span></span>

</dd> <dt>

<span data-ttu-id="a0e90-160">**RecordId**</span><span class="sxs-lookup"><span data-stu-id="a0e90-160">**RecordId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0e90-161">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a0e90-161">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a0e90-162">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a0e90-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0e90-163">Identificatore del record di errore per l'errore.</span><span class="sxs-lookup"><span data-stu-id="a0e90-163">Record identifier of the error record for this error.</span></span>

<span data-ttu-id="a0e90-164">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a0e90-164">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="a0e90-165">**Dimensioni**</span><span class="sxs-lookup"><span data-stu-id="a0e90-165">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0e90-166">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a0e90-166">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a0e90-167">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a0e90-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0e90-168">Dimensioni in byte del record di errore non elaborato.</span><span class="sxs-lookup"><span data-stu-id="a0e90-168">Size of the raw error record in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="a0e90-169">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="a0e90-169">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0e90-170">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a0e90-170">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a0e90-171">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a0e90-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0e90-172">Tipo di messaggio del log eventi.</span><span class="sxs-lookup"><span data-stu-id="a0e90-172">Type of event log message.</span></span> <span data-ttu-id="a0e90-173">Questi messaggi corrispondono ai codici dei messaggi del registro eventi utilizzati per inserire i messaggi del registro eventi dal provider di consumer del registro eventi di Windows quando riceve uno degli eventi.</span><span class="sxs-lookup"><span data-stu-id="a0e90-173">These messages correspond to the event log message codes used to insert event log messages by the Windows event log consumer provider when it receives one of the events.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a0e90-174">Commenti</span><span class="sxs-lookup"><span data-stu-id="a0e90-174">Remarks</span></span>

<span data-ttu-id="a0e90-175">La classe **MSMCAEvent \_ CPUError** è derivata da [**WmiEvent**](wmievent.md).</span><span class="sxs-lookup"><span data-stu-id="a0e90-175">The **MSMCAEvent\_CPUError** class is derived from [**WMIEvent**](wmievent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a0e90-176">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a0e90-176">Requirements</span></span>



| <span data-ttu-id="a0e90-177">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0e90-177">Requirement</span></span> | <span data-ttu-id="a0e90-178">Valore</span><span class="sxs-lookup"><span data-stu-id="a0e90-178">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a0e90-179">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a0e90-179">Minimum supported client</span></span><br/> | <span data-ttu-id="a0e90-180">Windows XP</span><span class="sxs-lookup"><span data-stu-id="a0e90-180">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="a0e90-181">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a0e90-181">Minimum supported server</span></span><br/> | <span data-ttu-id="a0e90-182">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a0e90-182">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="a0e90-183">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a0e90-183">Namespace</span></span><br/>                | <span data-ttu-id="a0e90-184">\\WMI radice</span><span class="sxs-lookup"><span data-stu-id="a0e90-184">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="a0e90-185">MOF</span><span class="sxs-lookup"><span data-stu-id="a0e90-185">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a0e90-186"><dt>Wmicore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a0e90-186"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="a0e90-187">DLL</span><span class="sxs-lookup"><span data-stu-id="a0e90-187">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a0e90-188"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a0e90-188"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0e90-189">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a0e90-189">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0e90-190">Classi MSMCA</span><span class="sxs-lookup"><span data-stu-id="a0e90-190">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="a0e90-191">**WMIEvent**</span><span class="sxs-lookup"><span data-stu-id="a0e90-191">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 

