---
description: Indica un errore del componente PCI MCA (Machine Check Architecture). Questa classe è disponibile solo nei sistemi Windows a 64 bit.
ms.assetid: 2b241333-2ea5-42cb-bdd3-27a10df51f3e
title: Classe MSMCAEvent_PCIComponentError
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_PCIComponentError
- MSMCAEvent_PCIComponentError.Active
- MSMCAEvent_PCIComponentError.AdditionalErrors
- MSMCAEvent_PCIComponentError.Cpu
- MSMCAEvent_PCIComponentError.ErrorSeverity
- MSMCAEvent_PCIComponentError.InstanceName
- MSMCAEvent_PCIComponentError.PCI_COMP_ERROR_STATUS
- MSMCAEvent_PCIComponentError.PCI_COMP_INFO_BusNumber
- MSMCAEvent_PCIComponentError.PCI_COMP_INFO_ClassCodeBaseClass
- MSMCAEvent_PCIComponentError.PCI_COMP_INFO_ClassCodeInterface
- MSMCAEvent_PCIComponentError.PCI_COMP_INFO_ClassCodeSubClass
- MSMCAEvent_PCIComponentError.PCI_COMP_INFO_DeviceId
- MSMCAEvent_PCIComponentError.PCI_COMP_INFO_DeviceNumber
- MSMCAEvent_PCIComponentError.PCI_COMP_INFO_FunctionNumber
- MSMCAEvent_PCIComponentError.PCI_COMP_INFO_SegmentNumber
- MSMCAEvent_PCIComponentError.PCI_COMP_INFO_VendorId
- MSMCAEvent_PCIComponentError.RawRecord
- MSMCAEvent_PCIComponentError.RecordId
- MSMCAEvent_PCIComponentError.Size
- MSMCAEvent_PCIComponentError.Type
- MSMCAEvent_PCIComponentError.VALIDATION_BITS
- MSMCAEvent_PCIComponentError.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: cbcf3ee13e822fd59cdcdd30538d5e369d798aaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316596"
---
# <a name="msmcaevent_pcicomponenterror-class"></a><span data-ttu-id="68989-104">\_Classe MSMCAEvent PCIComponentError</span><span class="sxs-lookup"><span data-stu-id="68989-104">MSMCAEvent\_PCIComponentError class</span></span>

<span data-ttu-id="68989-105">La classe **MSMCAEvent \_ PCIComponentError** indica un errore del componente PCI MCA (Machine Check Architecture).</span><span class="sxs-lookup"><span data-stu-id="68989-105">The **MSMCAEvent\_PCIComponentError** class indicates an Machine Check Architecture (MCA) PCI component error.</span></span> <span data-ttu-id="68989-106">Questa classe è disponibile solo nei sistemi Windows a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="68989-106">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="68989-107">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="68989-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="68989-108">Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="68989-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="68989-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="68989-109">Syntax</span></span>

``` syntax
class MSMCAEvent_PCIComponentError : WMIEvent
{
  boolean Active;
  uint32  AdditionalErrors;
  uint32  Cpu;
  uint8   ErrorSeverity;
  string  InstanceName;
  uint64  PCI_COMP_ERROR_STATUS;
  uint8   PCI_COMP_INFO_BusNumber;
  uint8   PCI_COMP_INFO_ClassCodeBaseClass;
  uint8   PCI_COMP_INFO_ClassCodeInterface;
  uint8   PCI_COMP_INFO_ClassCodeSubClass;
  uint16  PCI_COMP_INFO_DeviceId;
  uint8   PCI_COMP_INFO_DeviceNumber;
  uint8   PCI_COMP_INFO_FunctionNumber;
  uint8   PCI_COMP_INFO_SegmentNumber;
  uint16  PCI_COMP_INFO_VendorId;
  uint8   RawRecord[];
  uint64  RecordId;
  uint32  Size;
  uint32  Type;
  uint64  VALIDATION_BITS;
  uint32  LogToEventlog;
};
```

## <a name="members"></a><span data-ttu-id="68989-110">Members</span><span class="sxs-lookup"><span data-stu-id="68989-110">Members</span></span>

<span data-ttu-id="68989-111">La **classe \_ PCIComponentError di MSMCAEvent** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="68989-111">The **MSMCAEvent\_PCIComponentError** class has these types of members:</span></span>

-   [<span data-ttu-id="68989-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="68989-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="68989-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="68989-113">Properties</span></span>

<span data-ttu-id="68989-114">La **classe \_ PCIComponentError di MSMCAEvent** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="68989-114">The **MSMCAEvent\_PCIComponentError** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="68989-115">**Attivo**</span><span class="sxs-lookup"><span data-stu-id="68989-115">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68989-116">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="68989-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="68989-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="68989-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68989-118">**True** se questa istanza della classe è attiva; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="68989-118">**TRUE**, if this instance of the class is active; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="68989-119">**AdditionalErrors**</span><span class="sxs-lookup"><span data-stu-id="68989-119">**AdditionalErrors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68989-120">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="68989-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="68989-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="68989-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68989-122">Numero di errori aggiuntivi nel record.</span><span class="sxs-lookup"><span data-stu-id="68989-122">Number of additional errors in the record.</span></span>

</dd> <dt>

<span data-ttu-id="68989-123">**CPU**</span><span class="sxs-lookup"><span data-stu-id="68989-123">**Cpu**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68989-124">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="68989-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="68989-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="68989-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68989-126">CPU che ha segnalato l'errore.</span><span class="sxs-lookup"><span data-stu-id="68989-126">CPU that reported the error.</span></span> <span data-ttu-id="68989-127">Questa proprietà si applica solo a un sistema multiprocessore in cui al primo processore viene assegnato il numero 0, al secondo processore viene assegnato il numero 1 e così via.</span><span class="sxs-lookup"><span data-stu-id="68989-127">This property only applies to a multiprocessor system in which the first processor is assigned the number 0, the second processor is assigned the number 1, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="68989-128">**ErrorSeverity**</span><span class="sxs-lookup"><span data-stu-id="68989-128">**ErrorSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68989-129">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="68989-129">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="68989-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="68989-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68989-131">Livello di gravità dell'errore segnalato.</span><span class="sxs-lookup"><span data-stu-id="68989-131">Severity level of the error reported.</span></span>



| <span data-ttu-id="68989-132">Valore</span><span class="sxs-lookup"><span data-stu-id="68989-132">Value</span></span>                                                                                                | <span data-ttu-id="68989-133">Significato</span><span class="sxs-lookup"><span data-stu-id="68989-133">Meaning</span></span>                |
|------------------------------------------------------------------------------------------------------|------------------------|
| <span id="0"></span><dl> <span data-ttu-id="68989-134"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="68989-134"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="68989-135">Recuperabile</span><span class="sxs-lookup"><span data-stu-id="68989-135">Recoverable</span></span><br/> |
| <span id="1"></span><dl> <span data-ttu-id="68989-136"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="68989-136"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="68989-137">Fatal</span><span class="sxs-lookup"><span data-stu-id="68989-137">Fatal</span></span><br/>       |
| <span id="2"></span><dl> <span data-ttu-id="68989-138"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="68989-138"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="68989-139">Correggibile</span><span class="sxs-lookup"><span data-stu-id="68989-139">Correctable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="68989-140">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="68989-140">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68989-141">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="68989-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68989-142">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="68989-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68989-143">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="68989-143">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="68989-144">Identificatore univoco di questa istanza della classe.</span><span class="sxs-lookup"><span data-stu-id="68989-144">Unique identifier of this instance of the class.</span></span>

</dd> <dt>

<span data-ttu-id="68989-145">**LogToEventlog**</span><span class="sxs-lookup"><span data-stu-id="68989-145">**LogToEventlog**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68989-146">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="68989-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="68989-147">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="68989-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68989-148">Se è 0 (zero), questo evento non viene registrato nel registro eventi di sistema.</span><span class="sxs-lookup"><span data-stu-id="68989-148">If 0 (zero) then this event is not logged to the system event log.</span></span>

</dd> <dt>

<span data-ttu-id="68989-149">**\_stato di \_ errore del comp PCI \_**</span><span class="sxs-lookup"><span data-stu-id="68989-149">**PCI\_COMP\_ERROR\_STATUS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68989-150">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="68989-150">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="68989-151">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="68989-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68989-152">Codice di errore interno.</span><span class="sxs-lookup"><span data-stu-id="68989-152">Internal error code.</span></span>

<span data-ttu-id="68989-153">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="68989-153">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="68989-154">**\_ \_ Informazioni BusNumber PCI \_ comp**</span><span class="sxs-lookup"><span data-stu-id="68989-154">**PCI\_COMP\_INFO\_BusNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68989-155">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="68989-155">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="68989-156">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="68989-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68989-157">Numero del bus del componente PCI.</span><span class="sxs-lookup"><span data-stu-id="68989-157">Bus number of the PCI component.</span></span>

</dd> <dt>

<span data-ttu-id="68989-158">**\_ \_ Informazioni ClassCodeBaseClass PCI \_ comp**</span><span class="sxs-lookup"><span data-stu-id="68989-158">**PCI\_COMP\_INFO\_ClassCodeBaseClass**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68989-159">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="68989-159">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="68989-160">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="68989-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68989-161">Codice della classe di base del componente PCI.</span><span class="sxs-lookup"><span data-stu-id="68989-161">Class code of the base class of the PCI component.</span></span>

</dd> <dt>

<span data-ttu-id="68989-162">**\_ \_ Informazioni ClassCodeInterface PCI \_ comp**</span><span class="sxs-lookup"><span data-stu-id="68989-162">**PCI\_COMP\_INFO\_ClassCodeInterface**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68989-163">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="68989-163">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="68989-164">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="68989-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68989-165">Interfaccia del codice di classe del componente PCI.</span><span class="sxs-lookup"><span data-stu-id="68989-165">Class code interface of the PCI component.</span></span>

</dd> <dt>

<span data-ttu-id="68989-166">**\_ \_ Informazioni ClassCodeSubClass PCI \_ comp**</span><span class="sxs-lookup"><span data-stu-id="68989-166">**PCI\_COMP\_INFO\_ClassCodeSubClass**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68989-167">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="68989-167">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="68989-168">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="68989-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68989-169">Sottoclasse di codice della classe del componente PCI.</span><span class="sxs-lookup"><span data-stu-id="68989-169">Class code subclass of the PCI component.</span></span>

</dd> <dt>

<span data-ttu-id="68989-170">**\_ \_ Informazioni DeviceID PCI \_ comp**</span><span class="sxs-lookup"><span data-stu-id="68989-170">**PCI\_COMP\_INFO\_DeviceId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68989-171">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="68989-171">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="68989-172">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="68989-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68989-173">Identificatore del dispositivo del componente PCI.</span><span class="sxs-lookup"><span data-stu-id="68989-173">Device identifier of the PCI component.</span></span>

</dd> <dt>

<span data-ttu-id="68989-174">**\_ \_ Informazioni DeviceNumber PCI \_ comp**</span><span class="sxs-lookup"><span data-stu-id="68989-174">**PCI\_COMP\_INFO\_DeviceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68989-175">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="68989-175">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="68989-176">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="68989-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68989-177">Numero di dispositivo del componente PCI.</span><span class="sxs-lookup"><span data-stu-id="68989-177">Device number of the PCI component.</span></span>

</dd> <dt>

<span data-ttu-id="68989-178">**\_ \_ Informazioni FunctionNumber PCI \_ comp**</span><span class="sxs-lookup"><span data-stu-id="68989-178">**PCI\_COMP\_INFO\_FunctionNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68989-179">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="68989-179">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="68989-180">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="68989-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68989-181">Numero di funzione del componente PCI.</span><span class="sxs-lookup"><span data-stu-id="68989-181">Function number of the PCI component.</span></span>

</dd> <dt>

<span data-ttu-id="68989-182">**\_ \_ Informazioni SegmentNumber PCI \_ comp**</span><span class="sxs-lookup"><span data-stu-id="68989-182">**PCI\_COMP\_INFO\_SegmentNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68989-183">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="68989-183">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="68989-184">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="68989-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68989-185">Numero del segmento del componente PCI.</span><span class="sxs-lookup"><span data-stu-id="68989-185">Segment number of the PCI component.</span></span>

</dd> <dt>

<span data-ttu-id="68989-186">**\_ \_ Informazioni VendorID PCI \_ comp**</span><span class="sxs-lookup"><span data-stu-id="68989-186">**PCI\_COMP\_INFO\_VendorId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68989-187">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="68989-187">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="68989-188">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="68989-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68989-189">Identificatore del fornitore del componente PCI.</span><span class="sxs-lookup"><span data-stu-id="68989-189">Vendor identifier of the PCI Component.</span></span>

</dd> <dt>

<span data-ttu-id="68989-190">**RawRecord**</span><span class="sxs-lookup"><span data-stu-id="68989-190">**RawRecord**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68989-191">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="68989-191">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="68989-192">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="68989-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68989-193">Matrice di byte che contiene il record di errore non elaborato.</span><span class="sxs-lookup"><span data-stu-id="68989-193">Array of bytes that contains the raw error record.</span></span> <span data-ttu-id="68989-194">Numero di elementi nella matrice specificata dalla proprietà **size** .</span><span class="sxs-lookup"><span data-stu-id="68989-194">The number of elements in the array that the **Size** property specifies.</span></span>

</dd> <dt>

<span data-ttu-id="68989-195">**RecordId**</span><span class="sxs-lookup"><span data-stu-id="68989-195">**RecordId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68989-196">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="68989-196">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="68989-197">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="68989-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68989-198">Identificatore del record di errore per l'errore.</span><span class="sxs-lookup"><span data-stu-id="68989-198">Record identifier of the error record for this error.</span></span>

<span data-ttu-id="68989-199">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="68989-199">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="68989-200">**Dimensioni**</span><span class="sxs-lookup"><span data-stu-id="68989-200">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68989-201">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="68989-201">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="68989-202">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="68989-202">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68989-203">Dimensioni del record di errore non elaborato.</span><span class="sxs-lookup"><span data-stu-id="68989-203">Size of the raw error record.</span></span>

</dd> <dt>

<span data-ttu-id="68989-204">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="68989-204">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68989-205">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="68989-205">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="68989-206">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="68989-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68989-207">Tipo di messaggio del log eventi.</span><span class="sxs-lookup"><span data-stu-id="68989-207">Type of event log message.</span></span> <span data-ttu-id="68989-208">Questi messaggi corrispondono ai codici dei messaggi del registro eventi utilizzati per inserire i messaggi del registro eventi dal provider di consumer del registro eventi di Windows quando riceve uno degli eventi.</span><span class="sxs-lookup"><span data-stu-id="68989-208">These messages correspond to the event log message codes used to insert event log messages by the Windows event log consumer provider when it receives one of the events.</span></span>

</dd> <dt>

<span data-ttu-id="68989-209">**bit di convalida \_**</span><span class="sxs-lookup"><span data-stu-id="68989-209">**VALIDATION\_BITS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68989-210">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="68989-210">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="68989-211">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="68989-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68989-212">Bit di convalida usati per indicare la validità dei campi successivi.</span><span class="sxs-lookup"><span data-stu-id="68989-212">Validation bits used to indicate the validity of the subsequent fields.</span></span>



| <span data-ttu-id="68989-213">Valori</span><span class="sxs-lookup"><span data-stu-id="68989-213">Values</span></span>                                                                               | <span data-ttu-id="68989-214">Significato</span><span class="sxs-lookup"><span data-stu-id="68989-214">Meaning</span></span>                                          |
|--------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="68989-215"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="68989-215"><dt>1 (0x1)</dt></span></span> </dl>   | <span data-ttu-id="68989-216">\_Lo stato di errore del comp PCI \_ \_ è valido.</span><span class="sxs-lookup"><span data-stu-id="68989-216">PCI\_COMP\_ERROR\_STATUS is valid.</span></span><br/>    |
| <dl> <span data-ttu-id="68989-217"><dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="68989-217"><dt>2 (0x2)</dt></span></span> </dl>   | <span data-ttu-id="68989-218">Le \_ informazioni di comp PCI \_ sono valide.</span><span class="sxs-lookup"><span data-stu-id="68989-218">PCI\_COMP\_INFO is valid.</span></span><br/>             |
| <dl> <span data-ttu-id="68989-219"><dt>4 (0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="68989-219"><dt>4 (0x4)</dt></span></span> </dl>   | <span data-ttu-id="68989-220">Il numero di \_ MEM comp PCI \_ \_ è valido.</span><span class="sxs-lookup"><span data-stu-id="68989-220">PCI\_COMP\_MEM\_NUM is valid.</span></span><br/>         |
| <dl> <span data-ttu-id="68989-221"><dt>8 (0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="68989-221"><dt>8 (0x8)</dt></span></span> </dl>   | <span data-ttu-id="68989-222">Il numero di i/o \_ comp PCI \_ \_ è valido.</span><span class="sxs-lookup"><span data-stu-id="68989-222">PCI\_COMP\_IO\_NUM is valid.</span></span><br/>          |
| <dl> <span data-ttu-id="68989-223"><dt>16 (0x10)</dt></span><span class="sxs-lookup"><span data-stu-id="68989-223"><dt>16 (0x10)</dt></span></span> </dl> | <span data-ttu-id="68989-224">\_ \_ La coppia di dati REGS di PCI comp \_ \_ è valida.</span><span class="sxs-lookup"><span data-stu-id="68989-224">PCI\_COMP\_REGS\_DATA\_PAIR is valid.</span></span><br/> |



 

<span data-ttu-id="68989-225">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="68989-225">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="68989-226">Commenti</span><span class="sxs-lookup"><span data-stu-id="68989-226">Remarks</span></span>

<span data-ttu-id="68989-227">La classe **MSMCAEvent \_ PCIComponentError** è derivata da [**WmiEvent**](wmievent.md).</span><span class="sxs-lookup"><span data-stu-id="68989-227">The **MSMCAEvent\_PCIComponentError** class is derived from [**WMIEvent**](wmievent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="68989-228">Requisiti</span><span class="sxs-lookup"><span data-stu-id="68989-228">Requirements</span></span>



| <span data-ttu-id="68989-229">Requisito</span><span class="sxs-lookup"><span data-stu-id="68989-229">Requirement</span></span> | <span data-ttu-id="68989-230">Valore</span><span class="sxs-lookup"><span data-stu-id="68989-230">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="68989-231">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="68989-231">Minimum supported client</span></span><br/> | <span data-ttu-id="68989-232">Windows XP</span><span class="sxs-lookup"><span data-stu-id="68989-232">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="68989-233">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="68989-233">Minimum supported server</span></span><br/> | <span data-ttu-id="68989-234">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="68989-234">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="68989-235">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="68989-235">Namespace</span></span><br/>                | <span data-ttu-id="68989-236">\\WMI radice</span><span class="sxs-lookup"><span data-stu-id="68989-236">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="68989-237">MOF</span><span class="sxs-lookup"><span data-stu-id="68989-237">MOF</span></span><br/>                      | <dl> <span data-ttu-id="68989-238"><dt>Wmicore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="68989-238"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="68989-239">DLL</span><span class="sxs-lookup"><span data-stu-id="68989-239">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68989-240"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68989-240"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68989-241">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="68989-241">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68989-242">Classi MSMCA</span><span class="sxs-lookup"><span data-stu-id="68989-242">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="68989-243">**WMIEvent**</span><span class="sxs-lookup"><span data-stu-id="68989-243">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 

