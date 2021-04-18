---
description: Rappresenta un evento di errore di memoria del computer Check Architecture (MCA). Questa classe è disponibile solo nei sistemi Windows a 64 bit.
ms.assetid: 0db1d526-e2c3-4e48-90c8-cbcd9121040e
title: Classe MSMCAEvent_MemoryError
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_MemoryError
- MSMCAEvent_MemoryError.Active
- MSMCAEvent_MemoryError.AdditionalErrors
- MSMCAEvent_MemoryError.BUS_SPECIFIC_DATA
- MSMCAEvent_MemoryError.Cpu
- MSMCAEvent_MemoryError.ErrorSeverity
- MSMCAEvent_MemoryError.InstanceName
- MSMCAEvent_MemoryError.MEM_BANK
- MSMCAEvent_MemoryError.MEM_BIT_POSITION
- MSMCAEvent_MemoryError.MEM_CARD
- MSMCAEvent_MemoryError.MEM_COLUMN
- MSMCAEvent_MemoryError.MEM_ERROR_STATUS
- MSMCAEvent_MemoryError.MEM_MODULE
- MSMCAEvent_MemoryError.MEM_NODE
- MSMCAEvent_MemoryError.MEM_PHYSICAL_ADDR
- MSMCAEvent_MemoryError.MEM_PHYSICAL_MASK
- MSMCAEvent_MemoryError.MEM_ROW
- MSMCAEvent_MemoryError.RawRecord
- MSMCAEvent_MemoryError.RecordId
- MSMCAEvent_MemoryError.REQUESTOR_ID
- MSMCAEvent_MemoryError.RESPONDER_ID
- MSMCAEvent_MemoryError.Size
- MSMCAEvent_MemoryError.TARGET_ID
- MSMCAEvent_MemoryError.Type
- MSMCAEvent_MemoryError.VALIDATION_BITS
- MSMCAEvent_MemoryError.MEM_DEVICE
- MSMCAEvent_MemoryError.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 8dce82b8fa7a87676c34a9c6f26f43e4db10e227
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316600"
---
# <a name="msmcaevent_memoryerror-class"></a><span data-ttu-id="59ad8-104">\_Classe MSMCAEvent MemoryError</span><span class="sxs-lookup"><span data-stu-id="59ad8-104">MSMCAEvent\_MemoryError class</span></span>

<span data-ttu-id="59ad8-105">La classe **MSMCAEvent \_ MemoryError** rappresenta un evento di errore di memoria del computer Check Architecture (MCA).</span><span class="sxs-lookup"><span data-stu-id="59ad8-105">The **MSMCAEvent\_MemoryError** class represents a Machine Check Architecture (MCA) memory error event.</span></span> <span data-ttu-id="59ad8-106">Questa classe è disponibile solo nei sistemi Windows a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="59ad8-106">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="59ad8-107">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="59ad8-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="59ad8-108">Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="59ad8-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="59ad8-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="59ad8-109">Syntax</span></span>

``` syntax
class MSMCAEvent_MemoryError : WMIEvent
{
  boolean Active;
  uint32  AdditionalErrors;
  uint64  BUS_SPECIFIC_DATA;
  uint32  Cpu;
  uint8   ErrorSeverity;
  string  InstanceName;
  uint16  MEM_BANK;
  uint16  MEM_BIT_POSITION;
  uint16  MEM_CARD;
  uint16  MEM_COLUMN;
  uint64  MEM_ERROR_STATUS;
  uint16  MEM_MODULE;
  uint16  MEM_NODE;
  uint64  MEM_PHYSICAL_ADDR;
  uint64  MEM_PHYSICAL_MASK;
  uint16  MEM_ROW;
  uint8   RawRecord[];
  uint64  RecordId;
  uint64  REQUESTOR_ID;
  uint64  RESPONDER_ID;
  uint32  Size;
  uint64  TARGET_ID;
  uint32  Type;
  uint64  VALIDATION_BITS;
  uint16  MEM_DEVICE;
  uint32  LogToEventlog;
};
```

## <a name="members"></a><span data-ttu-id="59ad8-110">Members</span><span class="sxs-lookup"><span data-stu-id="59ad8-110">Members</span></span>

<span data-ttu-id="59ad8-111">La **classe \_ MemoryError di MSMCAEvent** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="59ad8-111">The **MSMCAEvent\_MemoryError** class has these types of members:</span></span>

-   [<span data-ttu-id="59ad8-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="59ad8-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="59ad8-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="59ad8-113">Properties</span></span>

<span data-ttu-id="59ad8-114">La **classe \_ MemoryError di MSMCAEvent** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="59ad8-114">The **MSMCAEvent\_MemoryError** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="59ad8-115">**Attivo**</span><span class="sxs-lookup"><span data-stu-id="59ad8-115">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59ad8-116">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="59ad8-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="59ad8-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="59ad8-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59ad8-118">**True** se questa istanza della classe è attiva; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="59ad8-118">**TRUE**, if this instance of the class is active; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="59ad8-119">**AdditionalErrors**</span><span class="sxs-lookup"><span data-stu-id="59ad8-119">**AdditionalErrors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59ad8-120">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="59ad8-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="59ad8-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="59ad8-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59ad8-122">Numero di errori aggiuntivi nel record MCA.</span><span class="sxs-lookup"><span data-stu-id="59ad8-122">Number of additional errors in the MCA record.</span></span>

</dd> <dt>

<span data-ttu-id="59ad8-123">**\_dati specifici del bus \_**</span><span class="sxs-lookup"><span data-stu-id="59ad8-123">**BUS\_SPECIFIC\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59ad8-124">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="59ad8-124">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="59ad8-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="59ad8-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59ad8-126">Dati dipendenti dal bus specifici dell'OEM.</span><span class="sxs-lookup"><span data-stu-id="59ad8-126">OEM-specific, bus-dependent data.</span></span>

<span data-ttu-id="59ad8-127">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="59ad8-127">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="59ad8-128">**CPU**</span><span class="sxs-lookup"><span data-stu-id="59ad8-128">**Cpu**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59ad8-129">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="59ad8-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="59ad8-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="59ad8-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59ad8-131">CPU che ha segnalato l'errore.</span><span class="sxs-lookup"><span data-stu-id="59ad8-131">CPU that reported the error.</span></span> <span data-ttu-id="59ad8-132">Questa proprietà si applica solo a un sistema multiprocessore in cui al primo processore viene assegnato il numero 0, al secondo processore viene assegnato il numero 1 e così via.</span><span class="sxs-lookup"><span data-stu-id="59ad8-132">This property only applies to a multiprocessor system in which the first processor is assigned the number 0, the second processor is assigned the number 1, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="59ad8-133">**ErrorSeverity**</span><span class="sxs-lookup"><span data-stu-id="59ad8-133">**ErrorSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59ad8-134">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="59ad8-134">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="59ad8-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="59ad8-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59ad8-136">Livello di gravità dell'errore segnalato.</span><span class="sxs-lookup"><span data-stu-id="59ad8-136">Severity level of the error reported.</span></span>



| <span data-ttu-id="59ad8-137">Valore</span><span class="sxs-lookup"><span data-stu-id="59ad8-137">Value</span></span>                                                                                                | <span data-ttu-id="59ad8-138">Significato</span><span class="sxs-lookup"><span data-stu-id="59ad8-138">Meaning</span></span>                |
|------------------------------------------------------------------------------------------------------|------------------------|
| <span id="0"></span><dl> <span data-ttu-id="59ad8-139"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="59ad8-139"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="59ad8-140">Recuperabile</span><span class="sxs-lookup"><span data-stu-id="59ad8-140">Recoverable</span></span><br/> |
| <span id="1"></span><dl> <span data-ttu-id="59ad8-141"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="59ad8-141"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="59ad8-142">Fatal</span><span class="sxs-lookup"><span data-stu-id="59ad8-142">Fatal</span></span><br/>       |
| <span id="2"></span><dl> <span data-ttu-id="59ad8-143"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="59ad8-143"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="59ad8-144">Correggibile</span><span class="sxs-lookup"><span data-stu-id="59ad8-144">Correctable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="59ad8-145">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="59ad8-145">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59ad8-146">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="59ad8-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="59ad8-147">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="59ad8-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="59ad8-148">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="59ad8-148">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="59ad8-149">Identificatore univoco di questa istanza della classe.</span><span class="sxs-lookup"><span data-stu-id="59ad8-149">Unique identifier of this instance of the class.</span></span>

</dd> <dt>

<span data-ttu-id="59ad8-150">**LogToEventlog**</span><span class="sxs-lookup"><span data-stu-id="59ad8-150">**LogToEventlog**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59ad8-151">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="59ad8-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="59ad8-152">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="59ad8-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59ad8-153">Se è zero, questo evento non viene registrato nel registro eventi di sistema.</span><span class="sxs-lookup"><span data-stu-id="59ad8-153">If zero then this event is not logged to the system event log.</span></span>

</dd> <dt>

<span data-ttu-id="59ad8-154">**\_banca MEM**</span><span class="sxs-lookup"><span data-stu-id="59ad8-154">**MEM\_BANK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59ad8-155">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="59ad8-155">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="59ad8-156">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="59ad8-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59ad8-157">Il modulo o il numero di rango della posizione degli errori di memoria.</span><span class="sxs-lookup"><span data-stu-id="59ad8-157">The Module or RANK number of the memory error location.</span></span>

</dd> <dt>

<span data-ttu-id="59ad8-158">**\_posizione bit \_ MEM**</span><span class="sxs-lookup"><span data-stu-id="59ad8-158">**MEM\_BIT\_POSITION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59ad8-159">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="59ad8-159">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="59ad8-160">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="59ad8-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59ad8-161">Posizione del bit nella parola di memoria che contiene l'errore.</span><span class="sxs-lookup"><span data-stu-id="59ad8-161">Bit position in the memory word that contains the error.</span></span>

</dd> <dt>

<span data-ttu-id="59ad8-162">**\_scheda mem**</span><span class="sxs-lookup"><span data-stu-id="59ad8-162">**MEM\_CARD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59ad8-163">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="59ad8-163">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="59ad8-164">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="59ad8-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59ad8-165">Numero di scheda della posizione degli errori di memoria.</span><span class="sxs-lookup"><span data-stu-id="59ad8-165">Card number of the memory error location.</span></span>

</dd> <dt>

<span data-ttu-id="59ad8-166">**\_colonna MEM**</span><span class="sxs-lookup"><span data-stu-id="59ad8-166">**MEM\_COLUMN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59ad8-167">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="59ad8-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="59ad8-168">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="59ad8-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59ad8-169">Numero di colonna della posizione degli errori di memoria.</span><span class="sxs-lookup"><span data-stu-id="59ad8-169">Column number of the memory error location.</span></span>

</dd> <dt>

<span data-ttu-id="59ad8-170">**\_dispositivo MEM**</span><span class="sxs-lookup"><span data-stu-id="59ad8-170">**MEM\_DEVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59ad8-171">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="59ad8-171">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="59ad8-172">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="59ad8-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59ad8-173">Numero del dispositivo del percorso di errore di memoria.</span><span class="sxs-lookup"><span data-stu-id="59ad8-173">Device number of the memory error location.</span></span>

</dd> <dt>

<span data-ttu-id="59ad8-174">**\_stato di errore di mem \_**</span><span class="sxs-lookup"><span data-stu-id="59ad8-174">**MEM\_ERROR\_STATUS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59ad8-175">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="59ad8-175">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="59ad8-176">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="59ad8-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59ad8-177">Stato di errore della memoria.</span><span class="sxs-lookup"><span data-stu-id="59ad8-177">Memory error status.</span></span>

<span data-ttu-id="59ad8-178">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="59ad8-178">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="59ad8-179">**\_modulo MEM**</span><span class="sxs-lookup"><span data-stu-id="59ad8-179">**MEM\_MODULE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59ad8-180">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="59ad8-180">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="59ad8-181">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="59ad8-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59ad8-182">Numero del modulo o del rango della posizione dell'errore di memoria.</span><span class="sxs-lookup"><span data-stu-id="59ad8-182">Module or rank number of the memory error location.</span></span>

</dd> <dt>

<span data-ttu-id="59ad8-183">**\_nodo MEM**</span><span class="sxs-lookup"><span data-stu-id="59ad8-183">**MEM\_NODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59ad8-184">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="59ad8-184">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="59ad8-185">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="59ad8-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59ad8-186">Nodo che contiene l'errore di memoria.</span><span class="sxs-lookup"><span data-stu-id="59ad8-186">Node that contains the memory error.</span></span> <span data-ttu-id="59ad8-187">Questa proprietà si applica solo in un sistema a più nodi.</span><span class="sxs-lookup"><span data-stu-id="59ad8-187">This property applies only in a multi-node system.</span></span> <span data-ttu-id="59ad8-188">Questa proprietà è specifica del fornitore.</span><span class="sxs-lookup"><span data-stu-id="59ad8-188">This property is vendor-specific.</span></span>

</dd> <dt>

<span data-ttu-id="59ad8-189">**\_indirizzo fisico \_ MEM**</span><span class="sxs-lookup"><span data-stu-id="59ad8-189">**MEM\_PHYSICAL\_ADDR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59ad8-190">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="59ad8-190">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="59ad8-191">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="59ad8-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59ad8-192">Indirizzo fisico dell'errore di memoria.</span><span class="sxs-lookup"><span data-stu-id="59ad8-192">Physical address of the memory error.</span></span>

<span data-ttu-id="59ad8-193">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="59ad8-193">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="59ad8-194">**\_maschera fisica \_ MEM**</span><span class="sxs-lookup"><span data-stu-id="59ad8-194">**MEM\_PHYSICAL\_MASK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59ad8-195">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="59ad8-195">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="59ad8-196">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="59ad8-196">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59ad8-197">Bit di indirizzo validi nell'indirizzo fisico a 64 bit dell'errore di memoria.</span><span class="sxs-lookup"><span data-stu-id="59ad8-197">Valid address bits in the 64-bit physical address of the memory error.</span></span>

> [!Note]  
> <span data-ttu-id="59ad8-198">La maschera fisica specifica la granularità dell'indirizzo fisico.</span><span class="sxs-lookup"><span data-stu-id="59ad8-198">The physical mask specifies the granularity of the physical address.</span></span> <span data-ttu-id="59ad8-199">L'indirizzo fisico dell'errore di memoria dipende dai fattori di implementazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="59ad8-199">The physical address of the memory error is dependent on hardware implementation factors.</span></span>

 

<span data-ttu-id="59ad8-200">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="59ad8-200">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="59ad8-201">**\_riga Mem**</span><span class="sxs-lookup"><span data-stu-id="59ad8-201">**MEM\_ROW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59ad8-202">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="59ad8-202">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="59ad8-203">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="59ad8-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59ad8-204">Numero di riga della posizione degli errori di memoria.</span><span class="sxs-lookup"><span data-stu-id="59ad8-204">Row number of the memory error location.</span></span>

</dd> <dt>

<span data-ttu-id="59ad8-205">**RawRecord**</span><span class="sxs-lookup"><span data-stu-id="59ad8-205">**RawRecord**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59ad8-206">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="59ad8-206">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="59ad8-207">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="59ad8-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59ad8-208">Matrice di byte che contiene il record di errore non elaborato presentato a Windows da System Abstraction Layer (SAL).</span><span class="sxs-lookup"><span data-stu-id="59ad8-208">Array of bytes that contains the raw error record as presented to Windows by the system abstraction layer (SAL).</span></span> <span data-ttu-id="59ad8-209">Il numero di elementi nella matrice è specificato dalla proprietà **size** .</span><span class="sxs-lookup"><span data-stu-id="59ad8-209">The number of elements in the array is specified by the **Size** property.</span></span>

</dd> <dt>

<span data-ttu-id="59ad8-210">**RecordId**</span><span class="sxs-lookup"><span data-stu-id="59ad8-210">**RecordId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59ad8-211">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="59ad8-211">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="59ad8-212">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="59ad8-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59ad8-213">Identificatore del record di errore per l'errore.</span><span class="sxs-lookup"><span data-stu-id="59ad8-213">Record identifier of the error record for this error.</span></span>

<span data-ttu-id="59ad8-214">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="59ad8-214">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="59ad8-215">**ID RICHIEDEnte \_**</span><span class="sxs-lookup"><span data-stu-id="59ad8-215">**REQUESTOR\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59ad8-216">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="59ad8-216">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="59ad8-217">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="59ad8-217">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59ad8-218">Indirizzo hardware del dispositivo o componente che avvia la transazione.</span><span class="sxs-lookup"><span data-stu-id="59ad8-218">Hardware address of the device or component that initiates the transaction.</span></span>

<span data-ttu-id="59ad8-219">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="59ad8-219">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="59ad8-220">**ID RISPONDItore \_**</span><span class="sxs-lookup"><span data-stu-id="59ad8-220">**RESPONDER\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59ad8-221">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="59ad8-221">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="59ad8-222">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="59ad8-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59ad8-223">Indirizzo hardware del risponditore alla transazione.</span><span class="sxs-lookup"><span data-stu-id="59ad8-223">Hardware address of the responder to the transaction.</span></span>

<span data-ttu-id="59ad8-224">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="59ad8-224">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="59ad8-225">**Dimensioni**</span><span class="sxs-lookup"><span data-stu-id="59ad8-225">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59ad8-226">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="59ad8-226">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="59ad8-227">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="59ad8-227">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59ad8-228">Dimensioni in byte del record di errore non elaborato.</span><span class="sxs-lookup"><span data-stu-id="59ad8-228">Size of the raw error record in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="59ad8-229">**\_ID destinazione**</span><span class="sxs-lookup"><span data-stu-id="59ad8-229">**TARGET\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59ad8-230">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="59ad8-230">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="59ad8-231">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="59ad8-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59ad8-232">Indirizzo hardware della destinazione prevista per la transazione.</span><span class="sxs-lookup"><span data-stu-id="59ad8-232">Hardware address of the intended target of the transaction.</span></span>

<span data-ttu-id="59ad8-233">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="59ad8-233">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="59ad8-234">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="59ad8-234">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59ad8-235">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="59ad8-235">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="59ad8-236">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="59ad8-236">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59ad8-237">Tipo di messaggio del log eventi.</span><span class="sxs-lookup"><span data-stu-id="59ad8-237">Type of event log message.</span></span> <span data-ttu-id="59ad8-238">Questi messaggi corrispondono ai codici dei messaggi del registro eventi utilizzati per inserire i messaggi del registro eventi dal provider di consumer del registro eventi di Windows quando riceve uno degli eventi.</span><span class="sxs-lookup"><span data-stu-id="59ad8-238">These messages correspond to the event log message codes used to insert event log messages by the Windows event log consumer provider when it receives one of the events.</span></span>

</dd> <dt>

<span data-ttu-id="59ad8-239">**bit di convalida \_**</span><span class="sxs-lookup"><span data-stu-id="59ad8-239">**VALIDATION\_BITS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59ad8-240">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="59ad8-240">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="59ad8-241">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="59ad8-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59ad8-242">Bit di convalida usati per indicare la validità dei campi successivi.</span><span class="sxs-lookup"><span data-stu-id="59ad8-242">Validation bits used to indicate the validity of the subsequent fields.</span></span>



| <span data-ttu-id="59ad8-243">Valori</span><span class="sxs-lookup"><span data-stu-id="59ad8-243">Values</span></span>                                                                                     | <span data-ttu-id="59ad8-244">Significato</span><span class="sxs-lookup"><span data-stu-id="59ad8-244">Meaning</span></span>                                                 |
|--------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <dl> <span data-ttu-id="59ad8-245"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="59ad8-245"><dt>1 (0x1)</dt></span></span> </dl>         | <span data-ttu-id="59ad8-246">\_Lo stato di errore di mem \_ è valido.</span><span class="sxs-lookup"><span data-stu-id="59ad8-246">MEM\_ERROR\_STATUS is valid.</span></span><br/>                 |
| <dl> <span data-ttu-id="59ad8-247"><dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="59ad8-247"><dt>2 (0x2)</dt></span></span> </dl>         | <span data-ttu-id="59ad8-248">Il valore \_ addr fisico della memoria \_ è valido.</span><span class="sxs-lookup"><span data-stu-id="59ad8-248">MEM\_PHYSICAL\_ADDR is valid.</span></span><br/>                |
| <dl> <span data-ttu-id="59ad8-249"><dt>4 (0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="59ad8-249"><dt>4 (0x4)</dt></span></span> </dl>         | <span data-ttu-id="59ad8-250">\_La maschera della MEM addr \_ è valida.</span><span class="sxs-lookup"><span data-stu-id="59ad8-250">MEM\_ADDR\_MASK is valid.</span></span><br/>                    |
| <dl> <span data-ttu-id="59ad8-251"><dt>8 (0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="59ad8-251"><dt>8 (0x8)</dt></span></span> </dl>         | <span data-ttu-id="59ad8-252">\_Nodo MEM valido.</span><span class="sxs-lookup"><span data-stu-id="59ad8-252">MEM\_NODE is valid.</span></span><br/>                          |
| <dl> <span data-ttu-id="59ad8-253"><dt>16 (0x10)</dt></span><span class="sxs-lookup"><span data-stu-id="59ad8-253"><dt>16 (0x10)</dt></span></span> </dl>       | <span data-ttu-id="59ad8-254">\_La scheda mem è valida.</span><span class="sxs-lookup"><span data-stu-id="59ad8-254">MEM\_CARD is valid.</span></span><br/>                          |
| <dl> <span data-ttu-id="59ad8-255"><dt>32 (0x20)</dt></span><span class="sxs-lookup"><span data-stu-id="59ad8-255"><dt>32 (0x20)</dt></span></span> </dl>       | <span data-ttu-id="59ad8-256">Il \_ modulo MEM è valido.</span><span class="sxs-lookup"><span data-stu-id="59ad8-256">MEM\_MODULE is valid.</span></span><br/>                        |
| <dl> <span data-ttu-id="59ad8-257"><dt>64 (0x40)</dt></span><span class="sxs-lookup"><span data-stu-id="59ad8-257"><dt>64 (0x40)</dt></span></span> </dl>       | <span data-ttu-id="59ad8-258">MEM \_ Bank è valido.</span><span class="sxs-lookup"><span data-stu-id="59ad8-258">MEM\_BANK is valid.</span></span><br/>                          |
| <dl> <span data-ttu-id="59ad8-259"><dt>128 (0x80)</dt></span><span class="sxs-lookup"><span data-stu-id="59ad8-259"><dt>128 (0x80)</dt></span></span> </dl>      | <span data-ttu-id="59ad8-260">Il \_ dispositivo MEM è valido.</span><span class="sxs-lookup"><span data-stu-id="59ad8-260">MEM\_DEVICE is valid.</span></span><br/>                        |
| <dl> <span data-ttu-id="59ad8-261"><dt>256 (0x100)</dt></span><span class="sxs-lookup"><span data-stu-id="59ad8-261"><dt>256 (0x100)</dt></span></span> </dl>     | <span data-ttu-id="59ad8-262">\_La riga di MEM è valida.</span><span class="sxs-lookup"><span data-stu-id="59ad8-262">MEM\_ROW is valid.</span></span><br/>                           |
| <dl> <span data-ttu-id="59ad8-263"><dt>512 (0x200)</dt></span><span class="sxs-lookup"><span data-stu-id="59ad8-263"><dt>512 (0x200)</dt></span></span> </dl>     | <span data-ttu-id="59ad8-264">\_La colonna Mem è valida.</span><span class="sxs-lookup"><span data-stu-id="59ad8-264">MEM\_COLUMN is valid.</span></span><br/>                        |
| <dl> <span data-ttu-id="59ad8-265"><dt>1024 (0x400)</dt></span><span class="sxs-lookup"><span data-stu-id="59ad8-265"><dt>1024 (0x400)</dt></span></span> </dl>    | <span data-ttu-id="59ad8-266">Posizione del bit di MEM \_ \_ valida.</span><span class="sxs-lookup"><span data-stu-id="59ad8-266">MEM\_BIT\_POSITION is valid.</span></span><br/>                 |
| <dl> <span data-ttu-id="59ad8-267"><dt>2048 (0x800)</dt></span><span class="sxs-lookup"><span data-stu-id="59ad8-267"><dt>2048 (0x800)</dt></span></span> </dl>    | <span data-ttu-id="59ad8-268">L' \_ ID del richiedente della piattaforma mem \_ \_ è valido.</span><span class="sxs-lookup"><span data-stu-id="59ad8-268">MEM\_PLATFORM\_REQUESTOR\_ID is valid.</span></span><br/>       |
| <dl> <span data-ttu-id="59ad8-269"><dt>4096 (0x1000)</dt></span><span class="sxs-lookup"><span data-stu-id="59ad8-269"><dt>4096 (0x1000)</dt></span></span> </dl>   | <span data-ttu-id="59ad8-270">L' \_ \_ ID risponditore della piattaforma \_ è valido.</span><span class="sxs-lookup"><span data-stu-id="59ad8-270">MEM\_PLATFORM\_RESPONDER\_ID is valid.</span></span><br/>       |
| <dl> <span data-ttu-id="59ad8-271"><dt>8192 (0x2000)</dt></span><span class="sxs-lookup"><span data-stu-id="59ad8-271"><dt>8192 (0x2000)</dt></span></span> </dl>   | <span data-ttu-id="59ad8-272">\_La destinazione della piattaforma mem \_ è valida.</span><span class="sxs-lookup"><span data-stu-id="59ad8-272">MEM\_PLATFORM\_TARGET is valid.</span></span><br/>              |
| <dl> <span data-ttu-id="59ad8-273"><dt>16384 (0x4000)</dt></span><span class="sxs-lookup"><span data-stu-id="59ad8-273"><dt>16384 (0x4000)</dt></span></span> </dl>  | <span data-ttu-id="59ad8-274">\_ \_ I dati specifici del bus di piattaforma mem \_ \_ sono validi.</span><span class="sxs-lookup"><span data-stu-id="59ad8-274">MEM\_PLATFORM\_BUS\_SPECIFIC\_DATA is valid.</span></span><br/> |
| <dl> <span data-ttu-id="59ad8-275"><dt>32768 (0x8000)</dt></span><span class="sxs-lookup"><span data-stu-id="59ad8-275"><dt>32768 (0x8000)</dt></span></span> </dl>  | <span data-ttu-id="59ad8-276">\_ID OEM della piattaforma mem \_ \_ valido.</span><span class="sxs-lookup"><span data-stu-id="59ad8-276">MEM\_PLATFORM\_OEM\_ID is valid.</span></span><br/>             |
| <dl> <span data-ttu-id="59ad8-277"><dt>65536 (0x10000)</dt></span><span class="sxs-lookup"><span data-stu-id="59ad8-277"><dt>65536 (0x10000)</dt></span></span> </dl> | <span data-ttu-id="59ad8-278">Lo \_ struct di dati OEM della piattaforma mem \_ \_ \_ è valido.</span><span class="sxs-lookup"><span data-stu-id="59ad8-278">MEM\_PLATFORM\_OEM\_DATA\_STRUCT is valid.</span></span><br/>   |



 

<span data-ttu-id="59ad8-279">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="59ad8-279">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="59ad8-280">Commenti</span><span class="sxs-lookup"><span data-stu-id="59ad8-280">Remarks</span></span>

<span data-ttu-id="59ad8-281">La classe **MSMCAEvent \_ MemoryError** è derivata da [**WmiEvent**](wmievent.md).</span><span class="sxs-lookup"><span data-stu-id="59ad8-281">The **MSMCAEvent\_MemoryError** class is derived from [**WMIEvent**](wmievent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="59ad8-282">Requisiti</span><span class="sxs-lookup"><span data-stu-id="59ad8-282">Requirements</span></span>



| <span data-ttu-id="59ad8-283">Requisito</span><span class="sxs-lookup"><span data-stu-id="59ad8-283">Requirement</span></span> | <span data-ttu-id="59ad8-284">Valore</span><span class="sxs-lookup"><span data-stu-id="59ad8-284">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="59ad8-285">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="59ad8-285">Minimum supported client</span></span><br/> | <span data-ttu-id="59ad8-286">Windows XP</span><span class="sxs-lookup"><span data-stu-id="59ad8-286">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="59ad8-287">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="59ad8-287">Minimum supported server</span></span><br/> | <span data-ttu-id="59ad8-288">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="59ad8-288">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="59ad8-289">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="59ad8-289">Namespace</span></span><br/>                | <span data-ttu-id="59ad8-290">\\WMI radice</span><span class="sxs-lookup"><span data-stu-id="59ad8-290">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="59ad8-291">MOF</span><span class="sxs-lookup"><span data-stu-id="59ad8-291">MOF</span></span><br/>                      | <dl> <span data-ttu-id="59ad8-292"><dt>Wmicore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="59ad8-292"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="59ad8-293">DLL</span><span class="sxs-lookup"><span data-stu-id="59ad8-293">DLL</span></span><br/>                      | <dl> <span data-ttu-id="59ad8-294"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="59ad8-294"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59ad8-295">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="59ad8-295">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59ad8-296">Classi MSMCA</span><span class="sxs-lookup"><span data-stu-id="59ad8-296">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="59ad8-297">**WMIEvent**</span><span class="sxs-lookup"><span data-stu-id="59ad8-297">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 

