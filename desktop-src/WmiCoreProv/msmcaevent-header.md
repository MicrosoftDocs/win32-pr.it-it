---
description: Rappresenta l'intestazione comune utilizzata da tutte le classi MSMCAEvent. Questa classe è disponibile solo nei sistemi Windows a 64 bit.
ms.assetid: ff20522c-f805-47dc-bef2-4176211de698
title: Classe MSMCAEvent_Header
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_Header
- MSMCAEvent_Header.AdditionalErrors
- MSMCAEvent_Header.Cpu
- MSMCAEvent_Header.ErrorSeverity
- MSMCAEvent_Header.RecordId
- MSMCAEvent_Header.Type
- MSMCAEvent_Header.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 426f943014f3b6cfbdba5a25d331c0ea621048cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315745"
---
# <a name="msmcaevent_header-class"></a><span data-ttu-id="6b0bb-104">\_Classe di intestazione MSMCAEvent</span><span class="sxs-lookup"><span data-stu-id="6b0bb-104">MSMCAEvent\_Header class</span></span>

<span data-ttu-id="6b0bb-105">La classe di **\_ intestazione MSMCAEvent** rappresenta l'intestazione comune utilizzata da tutte le [classi MSMCA](msmca-classes.md) .</span><span class="sxs-lookup"><span data-stu-id="6b0bb-105">The **MSMCAEvent\_Header** class represents the common header that all [MSMCA classes](msmca-classes.md) use.</span></span> <span data-ttu-id="6b0bb-106">I file di intestazione vengono usati in modo che il codice C e C++ possa avere una struttura di dati che descrive l'intestazione comune per tutti gli eventi.</span><span class="sxs-lookup"><span data-stu-id="6b0bb-106">The header files are used so that C and C++ code can have a data structure that describes the common header for all events.</span></span> <span data-ttu-id="6b0bb-107">Questa classe è riservata per uso interno.</span><span class="sxs-lookup"><span data-stu-id="6b0bb-107">This class is reserved for internal use.</span></span> <span data-ttu-id="6b0bb-108">Questa classe è disponibile solo nei sistemi Windows a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="6b0bb-108">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="6b0bb-109">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="6b0bb-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="6b0bb-110">Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="6b0bb-110">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b0bb-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6b0bb-111">Syntax</span></span>

``` syntax
class MSMCAEvent_Header
{
  uint32 AdditionalErrors;
  uint32 Cpu;
  uint8  ErrorSeverity;
  uint64 RecordId;
  uint32 Type;
  uint32 LogToEventlog;
};
```

## <a name="members"></a><span data-ttu-id="6b0bb-112">Members</span><span class="sxs-lookup"><span data-stu-id="6b0bb-112">Members</span></span>

<span data-ttu-id="6b0bb-113">La classe dell' **\_ intestazione MSMCAEvent** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="6b0bb-113">The **MSMCAEvent\_Header** class has these types of members:</span></span>

-   [<span data-ttu-id="6b0bb-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6b0bb-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6b0bb-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6b0bb-115">Properties</span></span>

<span data-ttu-id="6b0bb-116">La classe dell' **\_ intestazione MSMCAEvent** include queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="6b0bb-116">The **MSMCAEvent\_Header** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6b0bb-117">**AdditionalErrors**</span><span class="sxs-lookup"><span data-stu-id="6b0bb-117">**AdditionalErrors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b0bb-118">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6b0bb-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6b0bb-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6b0bb-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b0bb-120">Numero di errori aggiuntivi nel record MCA.</span><span class="sxs-lookup"><span data-stu-id="6b0bb-120">Number of additional errors in the MCA record.</span></span>

</dd> <dt>

<span data-ttu-id="6b0bb-121">**CPU**</span><span class="sxs-lookup"><span data-stu-id="6b0bb-121">**Cpu**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b0bb-122">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6b0bb-122">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6b0bb-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6b0bb-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b0bb-124">CPU che segnala l'errore.</span><span class="sxs-lookup"><span data-stu-id="6b0bb-124">CPU that reports the error.</span></span> <span data-ttu-id="6b0bb-125">Questa proprietà si applica solo a un sistema multiprocessore in cui al primo processore viene assegnato il numero 0, al secondo processore viene assegnato il numero 1 e così via.</span><span class="sxs-lookup"><span data-stu-id="6b0bb-125">This property only applies to a multiprocessor system in which the first processor is assigned the number 0, the second processor is assigned the number 1, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="6b0bb-126">**ErrorSeverity**</span><span class="sxs-lookup"><span data-stu-id="6b0bb-126">**ErrorSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b0bb-127">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="6b0bb-127">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="6b0bb-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6b0bb-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b0bb-129">Livello di gravità dell'errore segnalato.</span><span class="sxs-lookup"><span data-stu-id="6b0bb-129">Severity level of the error reported.</span></span>



| <span data-ttu-id="6b0bb-130">Valore</span><span class="sxs-lookup"><span data-stu-id="6b0bb-130">Value</span></span>                                                                                                | <span data-ttu-id="6b0bb-131">Significato</span><span class="sxs-lookup"><span data-stu-id="6b0bb-131">Meaning</span></span>                |
|------------------------------------------------------------------------------------------------------|------------------------|
| <span id="0"></span><dl> <span data-ttu-id="6b0bb-132"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="6b0bb-132"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="6b0bb-133">Recuperabile</span><span class="sxs-lookup"><span data-stu-id="6b0bb-133">Recoverable</span></span><br/> |
| <span id="1"></span><dl> <span data-ttu-id="6b0bb-134"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="6b0bb-134"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="6b0bb-135">Fatal</span><span class="sxs-lookup"><span data-stu-id="6b0bb-135">Fatal</span></span><br/>       |
| <span id="2"></span><dl> <span data-ttu-id="6b0bb-136"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="6b0bb-136"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="6b0bb-137">Correggibile</span><span class="sxs-lookup"><span data-stu-id="6b0bb-137">Correctable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="6b0bb-138">**LogToEventlog**</span><span class="sxs-lookup"><span data-stu-id="6b0bb-138">**LogToEventlog**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b0bb-139">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6b0bb-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6b0bb-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6b0bb-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b0bb-141">Se è 0 (zero), questo evento non viene registrato nel registro eventi di sistema.</span><span class="sxs-lookup"><span data-stu-id="6b0bb-141">If 0 (zero) then this event is not logged to the system event log.</span></span>

</dd> <dt>

<span data-ttu-id="6b0bb-142">**RecordId**</span><span class="sxs-lookup"><span data-stu-id="6b0bb-142">**RecordId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b0bb-143">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6b0bb-143">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6b0bb-144">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6b0bb-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b0bb-145">Identificatore del record di errore per l'errore.</span><span class="sxs-lookup"><span data-stu-id="6b0bb-145">Record identifier of the error record for this error.</span></span>

<span data-ttu-id="6b0bb-146">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="6b0bb-146">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="6b0bb-147">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="6b0bb-147">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b0bb-148">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6b0bb-148">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6b0bb-149">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6b0bb-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b0bb-150">Tipo di messaggio del log eventi.</span><span class="sxs-lookup"><span data-stu-id="6b0bb-150">Type of event log message.</span></span> <span data-ttu-id="6b0bb-151">Questi messaggi corrispondono ai codici dei messaggi del registro eventi utilizzati per inserire i messaggi del registro eventi dal provider di consumer del registro eventi di Windows quando riceve uno degli eventi.</span><span class="sxs-lookup"><span data-stu-id="6b0bb-151">These messages correspond to the event log message codes used to insert event log messages by the Windows event log consumer provider when it receives one of the events.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6b0bb-152">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6b0bb-152">Requirements</span></span>



| <span data-ttu-id="6b0bb-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b0bb-153">Requirement</span></span> | <span data-ttu-id="6b0bb-154">Valore</span><span class="sxs-lookup"><span data-stu-id="6b0bb-154">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6b0bb-155">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6b0bb-155">Minimum supported client</span></span><br/> | <span data-ttu-id="6b0bb-156">Windows XP</span><span class="sxs-lookup"><span data-stu-id="6b0bb-156">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="6b0bb-157">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6b0bb-157">Minimum supported server</span></span><br/> | <span data-ttu-id="6b0bb-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6b0bb-158">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="6b0bb-159">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6b0bb-159">Namespace</span></span><br/>                | <span data-ttu-id="6b0bb-160">\\WMI radice</span><span class="sxs-lookup"><span data-stu-id="6b0bb-160">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="6b0bb-161">MOF</span><span class="sxs-lookup"><span data-stu-id="6b0bb-161">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6b0bb-162"><dt>Wmicore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6b0bb-162"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="6b0bb-163">DLL</span><span class="sxs-lookup"><span data-stu-id="6b0bb-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6b0bb-164"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b0bb-164"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b0bb-165">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6b0bb-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b0bb-166">Classi MSMCA</span><span class="sxs-lookup"><span data-stu-id="6b0bb-166">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="6b0bb-167">Classi C++ WMI</span><span class="sxs-lookup"><span data-stu-id="6b0bb-167">WMI C++ Classes</span></span>](/windows/desktop/WmiSdk/wmi-c-classes)
</dt> </dl>

 

