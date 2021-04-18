---
description: Indica un errore MCA (computer Check Architecture) non valido. Un errore MCA non valido identifica un formato di errore che non è conforme alle specifiche di Windows. Questa classe è disponibile solo nei sistemi Windows a 64 bit.
ms.assetid: 476ea558-2e0e-480f-b4ba-8d73fdef3308
title: Classe MSMCAEvent_InvalidError
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_InvalidError
- MSMCAEvent_InvalidError.Active
- MSMCAEvent_InvalidError.AdditionalErrors
- MSMCAEvent_InvalidError.Cpu
- MSMCAEvent_InvalidError.ErrorSeverity
- MSMCAEvent_InvalidError.InstanceName
- MSMCAEvent_InvalidError.RawRecord
- MSMCAEvent_InvalidError.RecordId
- MSMCAEvent_InvalidError.Size
- MSMCAEvent_InvalidError.Type
- MSMCAEvent_InvalidError.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: abd12cfa7280a1b2f6a718b47b17d4ddf121cc25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306874"
---
# <a name="msmcaevent_invaliderror-class"></a><span data-ttu-id="f0eb6-105">\_Classe MSMCAEvent InvalidError</span><span class="sxs-lookup"><span data-stu-id="f0eb6-105">MSMCAEvent\_InvalidError class</span></span>

<span data-ttu-id="f0eb6-106">La classe **MSMCAEvent \_ InvalidError** indica un errore MCA (Machine Check Architecture) non valido.</span><span class="sxs-lookup"><span data-stu-id="f0eb6-106">The **MSMCAEvent\_InvalidError** class indicates a Machine Check Architecture (MCA) invalid error.</span></span> <span data-ttu-id="f0eb6-107">Un errore MCA non valido identifica un formato di errore che non è conforme alle specifiche di Windows.</span><span class="sxs-lookup"><span data-stu-id="f0eb6-107">An invalid MCA error identifies an error format that does not conform to Windows specifications.</span></span> <span data-ttu-id="f0eb6-108">Questa classe è disponibile solo nei sistemi Windows a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="f0eb6-108">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="f0eb6-109">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="f0eb6-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="f0eb6-110">Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="f0eb6-110">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0eb6-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f0eb6-111">Syntax</span></span>

``` syntax
class MSMCAEvent_InvalidError : WMIEvent
{
  boolean Active;
  uint32  AdditionalErrors;
  uint32  Cpu;
  uint8   ErrorSeverity;
  string  InstanceName;
  uint8   RawRecord[];
  uint64  RecordId;
  uint32  Size;
  uint32  Type;
  uint32  LogToEventlog;
};
```

## <a name="members"></a><span data-ttu-id="f0eb6-112">Members</span><span class="sxs-lookup"><span data-stu-id="f0eb6-112">Members</span></span>

<span data-ttu-id="f0eb6-113">La **classe \_ InvalidError di MSMCAEvent** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="f0eb6-113">The **MSMCAEvent\_InvalidError** class has these types of members:</span></span>

-   [<span data-ttu-id="f0eb6-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f0eb6-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f0eb6-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f0eb6-115">Properties</span></span>

<span data-ttu-id="f0eb6-116">La **classe \_ InvalidError di MSMCAEvent** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="f0eb6-116">The **MSMCAEvent\_InvalidError** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f0eb6-117">**Attivo**</span><span class="sxs-lookup"><span data-stu-id="f0eb6-117">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0eb6-118">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="f0eb6-118">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f0eb6-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f0eb6-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0eb6-120">**True** se questa istanza della classe è attiva; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="f0eb6-120">**TRUE**, if this instance of the class is active; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="f0eb6-121">**AdditionalErrors**</span><span class="sxs-lookup"><span data-stu-id="f0eb6-121">**AdditionalErrors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0eb6-122">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f0eb6-122">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f0eb6-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f0eb6-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0eb6-124">Numero di errori aggiuntivi nel record MCA.</span><span class="sxs-lookup"><span data-stu-id="f0eb6-124">Number of additional errors in the MCA record.</span></span>

</dd> <dt>

<span data-ttu-id="f0eb6-125">**CPU**</span><span class="sxs-lookup"><span data-stu-id="f0eb6-125">**Cpu**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0eb6-126">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f0eb6-126">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f0eb6-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f0eb6-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0eb6-128">CPU che ha segnalato l'errore.</span><span class="sxs-lookup"><span data-stu-id="f0eb6-128">CPU that reported the error.</span></span> <span data-ttu-id="f0eb6-129">Questa proprietà si applica solo a un sistema multiprocessore in cui al primo processore viene assegnato il numero 0, al secondo processore viene assegnato il numero 1 e così via.</span><span class="sxs-lookup"><span data-stu-id="f0eb6-129">This property only applies to a multiprocessor system in which the first processor is assigned the number 0, the second processor is assigned the number 1, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="f0eb6-130">**ErrorSeverity**</span><span class="sxs-lookup"><span data-stu-id="f0eb6-130">**ErrorSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0eb6-131">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="f0eb6-131">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="f0eb6-132">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f0eb6-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0eb6-133">Livello di gravità dell'errore segnalato.</span><span class="sxs-lookup"><span data-stu-id="f0eb6-133">Severity level of the error reported.</span></span>



| <span data-ttu-id="f0eb6-134">Valore</span><span class="sxs-lookup"><span data-stu-id="f0eb6-134">Value</span></span>                                                                                                | <span data-ttu-id="f0eb6-135">Significato</span><span class="sxs-lookup"><span data-stu-id="f0eb6-135">Meaning</span></span>                |
|------------------------------------------------------------------------------------------------------|------------------------|
| <span id="0"></span><dl> <span data-ttu-id="f0eb6-136"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="f0eb6-136"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="f0eb6-137">Recuperabile</span><span class="sxs-lookup"><span data-stu-id="f0eb6-137">Recoverable</span></span><br/> |
| <span id="1"></span><dl> <span data-ttu-id="f0eb6-138"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="f0eb6-138"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="f0eb6-139">Fatal</span><span class="sxs-lookup"><span data-stu-id="f0eb6-139">Fatal</span></span><br/>       |
| <span id="2"></span><dl> <span data-ttu-id="f0eb6-140"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="f0eb6-140"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="f0eb6-141">Correggibile</span><span class="sxs-lookup"><span data-stu-id="f0eb6-141">Correctable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="f0eb6-142">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="f0eb6-142">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0eb6-143">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f0eb6-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0eb6-144">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f0eb6-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f0eb6-145">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="f0eb6-145">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="f0eb6-146">Identificatore univoco di questa istanza della classe.</span><span class="sxs-lookup"><span data-stu-id="f0eb6-146">Unique identifier of this instance of the class.</span></span>

</dd> <dt>

<span data-ttu-id="f0eb6-147">**LogToEventlog**</span><span class="sxs-lookup"><span data-stu-id="f0eb6-147">**LogToEventlog**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0eb6-148">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f0eb6-148">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f0eb6-149">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f0eb6-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0eb6-150">Se è 0 (zero), questo evento non viene registrato nel registro eventi di sistema.</span><span class="sxs-lookup"><span data-stu-id="f0eb6-150">If 0 (zero) then this event is not logged to the system event log.</span></span>

</dd> <dt>

<span data-ttu-id="f0eb6-151">**RawRecord**</span><span class="sxs-lookup"><span data-stu-id="f0eb6-151">**RawRecord**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0eb6-152">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="f0eb6-152">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="f0eb6-153">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f0eb6-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0eb6-154">Matrice di byte che contiene il record di errore non elaborato presentato a Windows da System Abstraction Layer (SAL).</span><span class="sxs-lookup"><span data-stu-id="f0eb6-154">Array of bytes that contains the raw error record as presented to Windows by the system abstraction layer (SAL).</span></span> <span data-ttu-id="f0eb6-155">Il numero di elementi nella matrice è specificato dalla proprietà **size** .</span><span class="sxs-lookup"><span data-stu-id="f0eb6-155">The number of elements in the array is specified by the **Size** property.</span></span>

</dd> <dt>

<span data-ttu-id="f0eb6-156">**RecordId**</span><span class="sxs-lookup"><span data-stu-id="f0eb6-156">**RecordId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0eb6-157">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f0eb6-157">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f0eb6-158">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f0eb6-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0eb6-159">Identificatore del record di errore per l'errore.</span><span class="sxs-lookup"><span data-stu-id="f0eb6-159">Record identifier of the error record for this error.</span></span>

<span data-ttu-id="f0eb6-160">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f0eb6-160">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f0eb6-161">**Dimensioni**</span><span class="sxs-lookup"><span data-stu-id="f0eb6-161">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0eb6-162">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f0eb6-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f0eb6-163">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f0eb6-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0eb6-164">Dimensioni del record di errore non elaborato.</span><span class="sxs-lookup"><span data-stu-id="f0eb6-164">Size of the raw error record.</span></span>

</dd> <dt>

<span data-ttu-id="f0eb6-165">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="f0eb6-165">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0eb6-166">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f0eb6-166">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f0eb6-167">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f0eb6-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0eb6-168">Tipo di messaggio del log eventi.</span><span class="sxs-lookup"><span data-stu-id="f0eb6-168">Type of event log message.</span></span> <span data-ttu-id="f0eb6-169">Questi messaggi corrispondono ai codici dei messaggi del registro eventi utilizzati per inserire i messaggi del registro eventi dal provider di consumer del registro eventi di Windows quando riceve uno degli eventi.</span><span class="sxs-lookup"><span data-stu-id="f0eb6-169">These messages correspond to the event log message codes used to insert event log messages by the Windows event log consumer provider when it receives one of the events.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f0eb6-170">Commenti</span><span class="sxs-lookup"><span data-stu-id="f0eb6-170">Remarks</span></span>

<span data-ttu-id="f0eb6-171">La classe **MSMCAEvent \_ InvalidError** è derivata da [**WmiEvent**](wmievent.md).</span><span class="sxs-lookup"><span data-stu-id="f0eb6-171">The **MSMCAEvent\_InvalidError** class is derived from [**WMIEvent**](wmievent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f0eb6-172">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f0eb6-172">Requirements</span></span>



| <span data-ttu-id="f0eb6-173">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0eb6-173">Requirement</span></span> | <span data-ttu-id="f0eb6-174">Valore</span><span class="sxs-lookup"><span data-stu-id="f0eb6-174">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f0eb6-175">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f0eb6-175">Minimum supported client</span></span><br/> | <span data-ttu-id="f0eb6-176">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f0eb6-176">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="f0eb6-177">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f0eb6-177">Minimum supported server</span></span><br/> | <span data-ttu-id="f0eb6-178">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f0eb6-178">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="f0eb6-179">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f0eb6-179">Namespace</span></span><br/>                | <span data-ttu-id="f0eb6-180">\\WMI radice</span><span class="sxs-lookup"><span data-stu-id="f0eb6-180">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="f0eb6-181">MOF</span><span class="sxs-lookup"><span data-stu-id="f0eb6-181">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f0eb6-182"><dt>Wmicore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f0eb6-182"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="f0eb6-183">DLL</span><span class="sxs-lookup"><span data-stu-id="f0eb6-183">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f0eb6-184"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f0eb6-184"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0eb6-185">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f0eb6-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0eb6-186">Classi MSMCA</span><span class="sxs-lookup"><span data-stu-id="f0eb6-186">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="f0eb6-187">**WMIEvent**</span><span class="sxs-lookup"><span data-stu-id="f0eb6-187">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 

