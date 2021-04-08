---
description: Rappresenta un errore del bus PCI MCA (Machine Check Architecture). Questa classe è disponibile solo per i computer che eseguono un sistema operativo Windows a 64 bit.
ms.assetid: d8995909-a91b-4fcc-a37f-011d8df95ce8
title: Classe MSMCAEvent_PCIBusError
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_PCIBusError
- MSMCAEvent_PCIBusError.Active
- MSMCAEvent_PCIBusError.AdditionalErrors
- MSMCAEvent_PCIBusError.Cpu
- MSMCAEvent_PCIBusError.ErrorSeverity
- MSMCAEvent_PCIBusError.InstanceName
- MSMCAEvent_PCIBusError.PCI_BUS_ADDRESS
- MSMCAEvent_PCIBusError.PCI_BUS_CMD
- MSMCAEvent_PCIBusError.PCI_BUS_DATA
- MSMCAEvent_PCIBusError.PCI_BUS_ERROR_STATUS
- MSMCAEvent_PCIBusError.PCI_BUS_ERROR_TYPE
- MSMCAEvent_PCIBusError.PCI_BUS_ID_BusNumber
- MSMCAEvent_PCIBusError.PCI_BUS_ID_SegmentNumber
- MSMCAEvent_PCIBusError.PCI_BUS_REQUESTOR_ID
- MSMCAEvent_PCIBusError.PCI_BUS_RESPONDER_ID
- MSMCAEvent_PCIBusError.RawRecord
- MSMCAEvent_PCIBusError.RecordId
- MSMCAEvent_PCIBusError.Size
- MSMCAEvent_PCIBusError.Type
- MSMCAEvent_PCIBusError.VALIDATION_BITS
- MSMCAEvent_PCIBusError.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 7f2b800a07c0b979468a5df5a8be67e6adee39de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751383"
---
# <a name="msmcaevent_pcibuserror-class"></a><span data-ttu-id="7589d-104">\_Classe MSMCAEvent PCIBusError</span><span class="sxs-lookup"><span data-stu-id="7589d-104">MSMCAEvent\_PCIBusError class</span></span>

<span data-ttu-id="7589d-105">La classe **MSMCAEvent \_ PCIBusError** rappresenta un errore del bus PCI MCA (Machine Check Architecture).</span><span class="sxs-lookup"><span data-stu-id="7589d-105">The **MSMCAEvent\_PCIBusError** class represents a Machine Check Architecture (MCA) PCI bus error.</span></span> <span data-ttu-id="7589d-106">Questa classe è disponibile solo per i computer che eseguono un sistema operativo Windows a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="7589d-106">This class is available only for computers running on a 64-bit Windows operating system.</span></span>

<span data-ttu-id="7589d-107">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="7589d-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="7589d-108">Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="7589d-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="7589d-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7589d-109">Syntax</span></span>

``` syntax
class MSMCAEvent_PCIBusError : WMIEvent
{
  boolean Active;
  uint32  AdditionalErrors;
  uint32  Cpu;
  uint8   ErrorSeverity;
  string  InstanceName;
  uint64  PCI_BUS_ADDRESS;
  uint64  PCI_BUS_CMD;
  uint64  PCI_BUS_DATA;
  uint64  PCI_BUS_ERROR_STATUS;
  uint16  PCI_BUS_ERROR_TYPE;
  uint8   PCI_BUS_ID_BusNumber;
  uint8   PCI_BUS_ID_SegmentNumber;
  uint64  PCI_BUS_REQUESTOR_ID;
  uint64  PCI_BUS_RESPONDER_ID;
  uint8   RawRecord[];
  uint64  RecordId;
  uint32  Size;
  uint32  Type;
  uint64  VALIDATION_BITS;
  uint32  LogToEventlog;
};
```

## <a name="members"></a><span data-ttu-id="7589d-110">Members</span><span class="sxs-lookup"><span data-stu-id="7589d-110">Members</span></span>

<span data-ttu-id="7589d-111">La **classe \_ PCIBusError di MSMCAEvent** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="7589d-111">The **MSMCAEvent\_PCIBusError** class has these types of members:</span></span>

-   [<span data-ttu-id="7589d-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7589d-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7589d-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7589d-113">Properties</span></span>

<span data-ttu-id="7589d-114">La **classe \_ PCIBusError di MSMCAEvent** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="7589d-114">The **MSMCAEvent\_PCIBusError** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7589d-115">**Attivo**</span><span class="sxs-lookup"><span data-stu-id="7589d-115">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7589d-116">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="7589d-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7589d-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7589d-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7589d-118">**True** se questa istanza della classe è attiva; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="7589d-118">**TRUE**, if this instance of the class is active; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="7589d-119">**AdditionalErrors**</span><span class="sxs-lookup"><span data-stu-id="7589d-119">**AdditionalErrors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7589d-120">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7589d-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7589d-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7589d-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7589d-122">Numero di errori aggiuntivi nel record.</span><span class="sxs-lookup"><span data-stu-id="7589d-122">Number of additional errors in the record.</span></span>

</dd> <dt>

<span data-ttu-id="7589d-123">**CPU**</span><span class="sxs-lookup"><span data-stu-id="7589d-123">**Cpu**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7589d-124">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7589d-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7589d-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7589d-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7589d-126">CPU che ha segnalato l'errore.</span><span class="sxs-lookup"><span data-stu-id="7589d-126">CPU that reported the error.</span></span> <span data-ttu-id="7589d-127">Questa proprietà si applica solo a un sistema multiprocessore in cui al primo processore viene assegnato il numero 0, al secondo processore viene assegnato il numero 1 e così via.</span><span class="sxs-lookup"><span data-stu-id="7589d-127">This property only applies to a multiprocessor system in which the first processor is assigned the number 0, the second processor is assigned the number 1, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="7589d-128">**ErrorSeverity**</span><span class="sxs-lookup"><span data-stu-id="7589d-128">**ErrorSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7589d-129">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="7589d-129">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="7589d-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7589d-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7589d-131">Livello di gravità dell'errore segnalato.</span><span class="sxs-lookup"><span data-stu-id="7589d-131">Severity level of the error reported.</span></span>



| <span data-ttu-id="7589d-132">Valore</span><span class="sxs-lookup"><span data-stu-id="7589d-132">Value</span></span>                                                                                                | <span data-ttu-id="7589d-133">Significato</span><span class="sxs-lookup"><span data-stu-id="7589d-133">Meaning</span></span>                |
|------------------------------------------------------------------------------------------------------|------------------------|
| <span id="0"></span><dl> <span data-ttu-id="7589d-134"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="7589d-134"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="7589d-135">Recuperabile</span><span class="sxs-lookup"><span data-stu-id="7589d-135">Recoverable</span></span><br/> |
| <span id="1"></span><dl> <span data-ttu-id="7589d-136"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="7589d-136"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="7589d-137">Fatal</span><span class="sxs-lookup"><span data-stu-id="7589d-137">Fatal</span></span><br/>       |
| <span id="2"></span><dl> <span data-ttu-id="7589d-138"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="7589d-138"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="7589d-139">Correggibile</span><span class="sxs-lookup"><span data-stu-id="7589d-139">Correctable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="7589d-140">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="7589d-140">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7589d-141">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7589d-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7589d-142">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7589d-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7589d-143">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="7589d-143">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="7589d-144">Identificatore univoco di questa istanza della classe.</span><span class="sxs-lookup"><span data-stu-id="7589d-144">Unique identifier of this instance of the class.</span></span>

</dd> <dt>

<span data-ttu-id="7589d-145">**LogToEventlog**</span><span class="sxs-lookup"><span data-stu-id="7589d-145">**LogToEventlog**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7589d-146">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7589d-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7589d-147">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7589d-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7589d-148">Se è 0 (zero), questo evento non viene registrato nel registro eventi di sistema.</span><span class="sxs-lookup"><span data-stu-id="7589d-148">If 0 (zero), then this event is not logged to the system event log.</span></span>

</dd> <dt>

<span data-ttu-id="7589d-149">**\_indirizzo bus \_ PCI**</span><span class="sxs-lookup"><span data-stu-id="7589d-149">**PCI\_BUS\_ADDRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7589d-150">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7589d-150">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7589d-151">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7589d-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7589d-152">Memoria o indirizzo di I/O sul bus PCI al momento dell'evento.</span><span class="sxs-lookup"><span data-stu-id="7589d-152">Memory or I/O address on the PCI bus at the time of the event.</span></span>

<span data-ttu-id="7589d-153">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7589d-153">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="7589d-154">**\_cmd bus \_ PCI**</span><span class="sxs-lookup"><span data-stu-id="7589d-154">**PCI\_BUS\_CMD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7589d-155">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7589d-155">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7589d-156">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7589d-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7589d-157">Comando o operazione del bus al momento dell'evento.</span><span class="sxs-lookup"><span data-stu-id="7589d-157">Bus command or operation at the time of the event.</span></span>

<span data-ttu-id="7589d-158">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7589d-158">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="7589d-159">**\_dati bus \_ PCI**</span><span class="sxs-lookup"><span data-stu-id="7589d-159">**PCI\_BUS\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7589d-160">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7589d-160">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7589d-161">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7589d-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7589d-162">Dati sul bus PCI al momento dell'evento.</span><span class="sxs-lookup"><span data-stu-id="7589d-162">Data on the PCI bus at the time of the event.</span></span>

<span data-ttu-id="7589d-163">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7589d-163">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="7589d-164">**\_ \_ stato errore bus \_ PCI**</span><span class="sxs-lookup"><span data-stu-id="7589d-164">**PCI\_BUS\_ERROR\_STATUS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7589d-165">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7589d-165">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7589d-166">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7589d-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7589d-167">Stato del bus al momento dell'errore.</span><span class="sxs-lookup"><span data-stu-id="7589d-167">Bus status at the time of the error.</span></span>

<span data-ttu-id="7589d-168">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7589d-168">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="7589d-169">**\_tipo di \_ errore \_ bus PCI**</span><span class="sxs-lookup"><span data-stu-id="7589d-169">**PCI\_BUS\_ERROR\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7589d-170">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7589d-170">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7589d-171">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7589d-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7589d-172">Tipo di errore del bus PCI.</span><span class="sxs-lookup"><span data-stu-id="7589d-172">Type of PCI bus error.</span></span>



| <span data-ttu-id="7589d-173">Valore</span><span class="sxs-lookup"><span data-stu-id="7589d-173">Value</span></span>                                                                                                | <span data-ttu-id="7589d-174">Significato</span><span class="sxs-lookup"><span data-stu-id="7589d-174">Meaning</span></span>                                                     |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="7589d-175"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="7589d-175"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="7589d-176">Errore specifico di sistema sconosciuto o OEM.</span><span class="sxs-lookup"><span data-stu-id="7589d-176">Unknown or OEM System Specific Error.</span></span><br/>            |
| <span id="1"></span><dl> <span data-ttu-id="7589d-177"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="7589d-177"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="7589d-178">Errore di parità dei dati.</span><span class="sxs-lookup"><span data-stu-id="7589d-178">Data Parity Error.</span></span><br/>                               |
| <span id="2"></span><dl> <span data-ttu-id="7589d-179"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="7589d-179"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="7589d-180">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="7589d-180">System Error.</span></span><br/>                                    |
| <span id="3"></span><dl> <span data-ttu-id="7589d-181"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="7589d-181"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="7589d-182">Interruzione principale.</span><span class="sxs-lookup"><span data-stu-id="7589d-182">Master Abort.</span></span><br/>                                    |
| <span id="4"></span><dl> <span data-ttu-id="7589d-183"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="7589d-183"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="7589d-184">Timeout del bus o nessun dispositivo disponibile (nessun DEVSEL \# ).</span><span class="sxs-lookup"><span data-stu-id="7589d-184">Bus Time Out or No Device Present (NO DEVSEL\#).</span></span><br/> |
| <span id="5"></span><dl> <span data-ttu-id="7589d-185"><dt>**5**</dt></span><span class="sxs-lookup"><span data-stu-id="7589d-185"><dt>**5**</dt></span></span> </dl> | <span data-ttu-id="7589d-186">Errore di parità dei dati master.</span><span class="sxs-lookup"><span data-stu-id="7589d-186">Master Data Parity Error.</span></span><br/>                        |
| <span id="6"></span><dl> <span data-ttu-id="7589d-187"><dt>**6**</dt></span><span class="sxs-lookup"><span data-stu-id="7589d-187"><dt>**6**</dt></span></span> </dl> | <span data-ttu-id="7589d-188">Errore di parità degli indirizzi.</span><span class="sxs-lookup"><span data-stu-id="7589d-188">Address Parity Error.</span></span><br/>                            |
| <span id="7"></span><dl> <span data-ttu-id="7589d-189"><dt>**7**</dt></span><span class="sxs-lookup"><span data-stu-id="7589d-189"><dt>**7**</dt></span></span> </dl> | <span data-ttu-id="7589d-190">Errore di parità del comando.</span><span class="sxs-lookup"><span data-stu-id="7589d-190">Command Parity Error.</span></span><br/>                            |



 

</dd> <dt>

<span data-ttu-id="7589d-191">**\_ID bus \_ PCI \_ BusNumber**</span><span class="sxs-lookup"><span data-stu-id="7589d-191">**PCI\_BUS\_ID\_BusNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7589d-192">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="7589d-192">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="7589d-193">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7589d-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7589d-194">Identificatore designato per il bus PCI che ha rilevato l'errore.</span><span class="sxs-lookup"><span data-stu-id="7589d-194">Designated identifier for the PCI bus that encountered the error.</span></span>

</dd> <dt>

<span data-ttu-id="7589d-195">**\_ID bus \_ PCI \_ SegmentNumber**</span><span class="sxs-lookup"><span data-stu-id="7589d-195">**PCI\_BUS\_ID\_SegmentNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7589d-196">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="7589d-196">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="7589d-197">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7589d-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7589d-198">Identificatore di segmento designato per il bus PCI che ha rilevato l'errore.</span><span class="sxs-lookup"><span data-stu-id="7589d-198">Designated segment identifier for the PCI bus that encountered the error.</span></span>

</dd> <dt>

<span data-ttu-id="7589d-199">**\_ \_ ID richiedente bus \_ PCI**</span><span class="sxs-lookup"><span data-stu-id="7589d-199">**PCI\_BUS\_REQUESTOR\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7589d-200">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7589d-200">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7589d-201">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7589d-201">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7589d-202">Identificatore del richiedente del bus PCI al momento dell'evento.</span><span class="sxs-lookup"><span data-stu-id="7589d-202">PCI Bus requestor identifier at the time of the event.</span></span>

<span data-ttu-id="7589d-203">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7589d-203">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="7589d-204">**\_ \_ ID risponditore bus \_ PCI**</span><span class="sxs-lookup"><span data-stu-id="7589d-204">**PCI\_BUS\_RESPONDER\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7589d-205">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7589d-205">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7589d-206">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7589d-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7589d-207">Identificatore del risponditore del bus PCI al momento dell'evento.</span><span class="sxs-lookup"><span data-stu-id="7589d-207">PCI Bus Responder identifier at the time of the event.</span></span>

<span data-ttu-id="7589d-208">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7589d-208">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="7589d-209">**RawRecord**</span><span class="sxs-lookup"><span data-stu-id="7589d-209">**RawRecord**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7589d-210">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="7589d-210">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="7589d-211">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7589d-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7589d-212">Matrice di byte che contiene il record di errore non elaborato presentato a Windows da System Abstraction Layer (SAL).</span><span class="sxs-lookup"><span data-stu-id="7589d-212">Array of bytes that contains the raw error record as presented to Windows by the system abstraction layer (SAL).</span></span> <span data-ttu-id="7589d-213">Il numero di elementi nella matrice è specificato dalla proprietà **size** .</span><span class="sxs-lookup"><span data-stu-id="7589d-213">The number of elements in the array is specified by the **Size** property.</span></span>

</dd> <dt>

<span data-ttu-id="7589d-214">**RecordId**</span><span class="sxs-lookup"><span data-stu-id="7589d-214">**RecordId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7589d-215">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7589d-215">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7589d-216">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7589d-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7589d-217">Identificatore del record di errore per l'errore.</span><span class="sxs-lookup"><span data-stu-id="7589d-217">Record identifier of the error record for this error.</span></span>

<span data-ttu-id="7589d-218">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7589d-218">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="7589d-219">**Dimensioni**</span><span class="sxs-lookup"><span data-stu-id="7589d-219">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7589d-220">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7589d-220">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7589d-221">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7589d-221">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7589d-222">Dimensioni del record di errore non elaborato.</span><span class="sxs-lookup"><span data-stu-id="7589d-222">Size of the raw error record.</span></span>

</dd> <dt>

<span data-ttu-id="7589d-223">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="7589d-223">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7589d-224">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7589d-224">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7589d-225">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7589d-225">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7589d-226">Tipo di messaggio del log eventi.</span><span class="sxs-lookup"><span data-stu-id="7589d-226">Type of event log message.</span></span> <span data-ttu-id="7589d-227">Questi messaggi corrispondono ai codici dei messaggi del registro eventi utilizzati per inserire i messaggi del registro eventi dal provider di consumer del registro eventi di Windows quando riceve uno degli eventi.</span><span class="sxs-lookup"><span data-stu-id="7589d-227">These messages correspond to the event log message codes used to insert event log messages by the Windows event log consumer provider when it receives one of the events.</span></span>

</dd> <dt>

<span data-ttu-id="7589d-228">**bit di convalida \_**</span><span class="sxs-lookup"><span data-stu-id="7589d-228">**VALIDATION\_BITS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7589d-229">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7589d-229">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7589d-230">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7589d-230">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7589d-231">Bit di convalida usati per indicare la validità dei campi successivi.</span><span class="sxs-lookup"><span data-stu-id="7589d-231">Validation bits used to indicate the validity of the subsequent fields.</span></span>



| <span data-ttu-id="7589d-232">Valori</span><span class="sxs-lookup"><span data-stu-id="7589d-232">Values</span></span>                                                                                  | <span data-ttu-id="7589d-233">Significato</span><span class="sxs-lookup"><span data-stu-id="7589d-233">Meaning</span></span>                                          |
|-----------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="7589d-234"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="7589d-234"><dt>1 (0x1)</dt></span></span> </dl>      | <span data-ttu-id="7589d-235">\_Lo stato di errore del bus PCI \_ \_ è valido.</span><span class="sxs-lookup"><span data-stu-id="7589d-235">PCI\_BUS\_ERROR\_STATUS is valid.</span></span><br/>     |
| <dl> <span data-ttu-id="7589d-236"><dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="7589d-236"><dt>2 (0x2)</dt></span></span> </dl>      | <span data-ttu-id="7589d-237">Il \_ tipo di errore del bus PCI \_ \_ è valido.</span><span class="sxs-lookup"><span data-stu-id="7589d-237">PCI\_BUS\_ERROR\_TYPE is valid.</span></span><br/>       |
| <dl> <span data-ttu-id="7589d-238"><dt>4 (0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="7589d-238"><dt>4 (0x4)</dt></span></span> </dl>      | <span data-ttu-id="7589d-239">\_ID bus PCI \_ valido.</span><span class="sxs-lookup"><span data-stu-id="7589d-239">PCI\_BUS\_ID is valid.</span></span><br/>                |
| <dl> <span data-ttu-id="7589d-240"><dt>8 (0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="7589d-240"><dt>8 (0x8)</dt></span></span> </dl>      | <span data-ttu-id="7589d-241">\_Indirizzo bus PCI \_ valido.</span><span class="sxs-lookup"><span data-stu-id="7589d-241">PCI\_BUS\_ADDRESS is valid.</span></span><br/>           |
| <dl> <span data-ttu-id="7589d-242"><dt>16 (0x10)</dt></span><span class="sxs-lookup"><span data-stu-id="7589d-242"><dt>16 (0x10)</dt></span></span> </dl>    | <span data-ttu-id="7589d-243">\_I dati del bus PCI \_ sono validi.</span><span class="sxs-lookup"><span data-stu-id="7589d-243">PCI\_BUS\_DATA is valid.</span></span><br/>              |
| <dl> <span data-ttu-id="7589d-244"><dt>32 (0x20)</dt></span><span class="sxs-lookup"><span data-stu-id="7589d-244"><dt>32 (0x20)</dt></span></span> </dl>    | <span data-ttu-id="7589d-245">Il valore \_ cmd del bus PCI \_ è valido.</span><span class="sxs-lookup"><span data-stu-id="7589d-245">PCI\_BUS\_CMD is valid.</span></span><br/>               |
| <dl> <span data-ttu-id="7589d-246"><dt>64 (0x40)</dt></span><span class="sxs-lookup"><span data-stu-id="7589d-246"><dt>64 (0x40)</dt></span></span> </dl>    | <span data-ttu-id="7589d-247">\_ \_ ID richiedente bus PCI \_ valido.</span><span class="sxs-lookup"><span data-stu-id="7589d-247">PCI\_BUS\_REQUESTOR\_ID is valid.</span></span><br/>     |
| <dl> <span data-ttu-id="7589d-248"><dt>128 (0x80)</dt></span><span class="sxs-lookup"><span data-stu-id="7589d-248"><dt>128 (0x80)</dt></span></span> </dl>   | <span data-ttu-id="7589d-249">\_ \_ ID risponditore bus PCI \_ valido.</span><span class="sxs-lookup"><span data-stu-id="7589d-249">PCI\_BUS\_RESPONDER\_ID is valid.</span></span><br/>     |
| <dl> <span data-ttu-id="7589d-250"><dt>256 (0x100)</dt></span><span class="sxs-lookup"><span data-stu-id="7589d-250"><dt>256 (0x100)</dt></span></span> </dl>  | <span data-ttu-id="7589d-251">\_ \_ ID destinazione bus PCI \_ valido.</span><span class="sxs-lookup"><span data-stu-id="7589d-251">PCI\_BUS\_TARGET\_ID is valid.</span></span><br/>        |
| <dl> <span data-ttu-id="7589d-252"><dt>512 (0x200)</dt></span><span class="sxs-lookup"><span data-stu-id="7589d-252"><dt>512 (0x200)</dt></span></span> </dl>  | <span data-ttu-id="7589d-253">\_ID OEM del bus PCI \_ \_ valido.</span><span class="sxs-lookup"><span data-stu-id="7589d-253">PCI\_BUS\_OEM\_ID is valid.</span></span><br/>           |
| <dl> <span data-ttu-id="7589d-254"><dt>1024 (0x400)</dt></span><span class="sxs-lookup"><span data-stu-id="7589d-254"><dt>1024 (0x400)</dt></span></span> </dl> | <span data-ttu-id="7589d-255">Lo \_ struct di dati OEM del bus PCI \_ \_ \_ è valido.</span><span class="sxs-lookup"><span data-stu-id="7589d-255">PCI\_BUS\_OEM\_DATA\_STRUCT is valid.</span></span><br/> |



 

<span data-ttu-id="7589d-256">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7589d-256">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7589d-257">Commenti</span><span class="sxs-lookup"><span data-stu-id="7589d-257">Remarks</span></span>

<span data-ttu-id="7589d-258">La classe **MSMCAEvent \_ PCIBusError** è derivata da [**WmiEvent**](wmievent.md).</span><span class="sxs-lookup"><span data-stu-id="7589d-258">The **MSMCAEvent\_PCIBusError** class is derived from [**WMIEvent**](wmievent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7589d-259">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7589d-259">Requirements</span></span>



| <span data-ttu-id="7589d-260">Requisito</span><span class="sxs-lookup"><span data-stu-id="7589d-260">Requirement</span></span> | <span data-ttu-id="7589d-261">Valore</span><span class="sxs-lookup"><span data-stu-id="7589d-261">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7589d-262">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7589d-262">Minimum supported client</span></span><br/> | <span data-ttu-id="7589d-263">Windows XP</span><span class="sxs-lookup"><span data-stu-id="7589d-263">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="7589d-264">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7589d-264">Minimum supported server</span></span><br/> | <span data-ttu-id="7589d-265">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7589d-265">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="7589d-266">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="7589d-266">Namespace</span></span><br/>                | <span data-ttu-id="7589d-267">\\WMI radice</span><span class="sxs-lookup"><span data-stu-id="7589d-267">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="7589d-268">MOF</span><span class="sxs-lookup"><span data-stu-id="7589d-268">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7589d-269"><dt>Wmicore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7589d-269"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="7589d-270">DLL</span><span class="sxs-lookup"><span data-stu-id="7589d-270">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7589d-271"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7589d-271"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7589d-272">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7589d-272">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7589d-273">Classi MSMCA</span><span class="sxs-lookup"><span data-stu-id="7589d-273">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="7589d-274">**WMIEvent**</span><span class="sxs-lookup"><span data-stu-id="7589d-274">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 

