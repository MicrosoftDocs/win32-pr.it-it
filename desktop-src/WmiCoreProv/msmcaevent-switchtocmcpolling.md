---
description: Rappresenta la gestione del controllo del computer (CMC) corretta da passare dal driver di interrupt al polling. Questa classe è disponibile solo nei sistemi Windows a 64 bit.
ms.assetid: c5e99e13-0f65-40bc-8863-b2ca7ea221df
title: Classe MSMCAEvent_SwitchToCMCPolling
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_SwitchToCMCPolling
- MSMCAEvent_SwitchToCMCPolling.Active
- MSMCAEvent_SwitchToCMCPolling.InstanceName
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: f7d0d543dc36054550d4ddf6cc1a77ce80cf1647
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343446"
---
# <a name="msmcaevent_switchtocmcpolling-class"></a><span data-ttu-id="9212d-104">\_Classe MSMCAEvent SwitchToCMCPolling</span><span class="sxs-lookup"><span data-stu-id="9212d-104">MSMCAEvent\_SwitchToCMCPolling class</span></span>

<span data-ttu-id="9212d-105">La classe **MSMCAEvent \_ SwitchToCMCPolling** rappresenta la gestione del controllo del computer (CMC) corretta da passare dal driver di interrupt al polling.</span><span class="sxs-lookup"><span data-stu-id="9212d-105">The **MSMCAEvent\_SwitchToCMCPolling** class represents the corrected machine check (CMC) handling to be switched from the interrupt driver to polling.</span></span> <span data-ttu-id="9212d-106">In alcuni casi, il kernel esegue il polling di System Abstraction Layer (SAL) per qualsiasi CMC o errore di piattaforma (CPE) corretto che si è verificato nell'intervallo di polling precedente.</span><span class="sxs-lookup"><span data-stu-id="9212d-106">In some cases, the kernel polls the system abstraction layer (SAL) for any CMC or corrected platform error (CPE) that occurred within the previous polling interval.</span></span> <span data-ttu-id="9212d-107">Questa classe è disponibile solo nei sistemi Windows a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="9212d-107">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="9212d-108">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="9212d-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="9212d-109">Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="9212d-109">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9212d-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9212d-110">Syntax</span></span>

``` syntax
class MSMCAEvent_SwitchToCMCPolling : WMIEvent
{
  boolean Active;
  string  InstanceName;
};
```

## <a name="members"></a><span data-ttu-id="9212d-111">Members</span><span class="sxs-lookup"><span data-stu-id="9212d-111">Members</span></span>

<span data-ttu-id="9212d-112">La **classe \_ SwitchToCMCPolling di MSMCAEvent** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="9212d-112">The **MSMCAEvent\_SwitchToCMCPolling** class has these types of members:</span></span>

-   [<span data-ttu-id="9212d-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9212d-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9212d-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9212d-114">Properties</span></span>

<span data-ttu-id="9212d-115">La **classe \_ SwitchToCMCPolling di MSMCAEvent** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="9212d-115">The **MSMCAEvent\_SwitchToCMCPolling** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9212d-116">**Attivo**</span><span class="sxs-lookup"><span data-stu-id="9212d-116">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9212d-117">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="9212d-117">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9212d-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9212d-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9212d-119">**True** se questa istanza della classe è attiva; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="9212d-119">**TRUE**, if this instance of the class is active; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="9212d-120">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="9212d-120">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9212d-121">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9212d-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9212d-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9212d-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9212d-123">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9212d-123">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9212d-124">Identificatore univoco di questa istanza della classe.</span><span class="sxs-lookup"><span data-stu-id="9212d-124">Unique identifier of this instance of the class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9212d-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="9212d-125">Remarks</span></span>

<span data-ttu-id="9212d-126">La classe **MSMCAEvent \_ SwitchToCMCPolling** è derivata da [**WmiEvent**](wmievent.md).</span><span class="sxs-lookup"><span data-stu-id="9212d-126">The **MSMCAEvent\_SwitchToCMCPolling** class is derived from [**WMIEvent**](wmievent.md).</span></span>

<span data-ttu-id="9212d-127">System Abstraction Layer (SAL) è il codice bruciato su ROM che il sistema operativo chiama per eseguire operazioni dipendenti dalla piattaforma.</span><span class="sxs-lookup"><span data-stu-id="9212d-127">The system abstraction layer (SAL) is code burned onto ROM that the operating system calls to perform platform-dependent operations.</span></span> <span data-ttu-id="9212d-128">È simile al BIOS su una piattaforma x86.</span><span class="sxs-lookup"><span data-stu-id="9212d-128">It is similar to the BIOS on an x86 platform.</span></span> <span data-ttu-id="9212d-129">Nei casi in cui la piattaforma non supporta gli interrupt per il polling CMC o CPE, il sistema operativo esegue il polling ogni minuto, controllando se si è verificato un errore in precedenza.</span><span class="sxs-lookup"><span data-stu-id="9212d-129">In cases where the platform does not support interrupts for CMC or CPE polling, the operating system polls every minute, checking if an error occurred previously.</span></span> <span data-ttu-id="9212d-130">Se la piattaforma supporta le interruzioni e il sistema operativo riceve una quantità definita dall'utente di sondaggi CMC o CPE entro un minuto, Disabilita l'interrupt e il polling.</span><span class="sxs-lookup"><span data-stu-id="9212d-130">If the platform does support interrupts and the operating system receives a user defined amount of CMC or CPE polls within one minute, then it disables the interrupt and poll.</span></span> <span data-ttu-id="9212d-131">Se l'utente non definisce il numero di polling entro un minuto, il sistema imposta un valore predefinito di 10 poll al minuto.</span><span class="sxs-lookup"><span data-stu-id="9212d-131">If the user does not define the number of polls within one minute, the system sets a default to 10 polls per minute.</span></span>

## <a name="requirements"></a><span data-ttu-id="9212d-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9212d-132">Requirements</span></span>



| <span data-ttu-id="9212d-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="9212d-133">Requirement</span></span> | <span data-ttu-id="9212d-134">Valore</span><span class="sxs-lookup"><span data-stu-id="9212d-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9212d-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9212d-135">Minimum supported client</span></span><br/> | <span data-ttu-id="9212d-136">Windows XP</span><span class="sxs-lookup"><span data-stu-id="9212d-136">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="9212d-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9212d-137">Minimum supported server</span></span><br/> | <span data-ttu-id="9212d-138">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9212d-138">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="9212d-139">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9212d-139">Namespace</span></span><br/>                | <span data-ttu-id="9212d-140">\\WMI radice</span><span class="sxs-lookup"><span data-stu-id="9212d-140">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="9212d-141">MOF</span><span class="sxs-lookup"><span data-stu-id="9212d-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9212d-142"><dt>Wmicore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9212d-142"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="9212d-143">DLL</span><span class="sxs-lookup"><span data-stu-id="9212d-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9212d-144"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9212d-144"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9212d-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9212d-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9212d-146">Classi MSMCA</span><span class="sxs-lookup"><span data-stu-id="9212d-146">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="9212d-147">**WMIEvent**</span><span class="sxs-lookup"><span data-stu-id="9212d-147">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 

