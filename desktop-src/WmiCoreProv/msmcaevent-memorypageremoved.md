---
description: Indica che una pagina di memoria è stata rimossa dall'utilizzo del sistema a causa di errori di controllo degli errori hardware e correzione (ECC) eccessivi. Questa classe è disponibile solo nei sistemi Windows a 64 bit.
ms.assetid: 364a2520-8d7c-44f2-95f6-eea9a5531975
title: Classe MSMCAEvent_MemoryPageRemoved
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_MemoryPageRemoved
- MSMCAEvent_MemoryPageRemoved.Active
- MSMCAEvent_MemoryPageRemoved.InstanceName
- MSMCAEvent_MemoryPageRemoved.PhysicalAddress
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: dc29c5b51531e204ab50f062dd08ef8d5abf1bbf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316598"
---
# <a name="msmcaevent_memorypageremoved-class"></a><span data-ttu-id="bbcf9-104">\_Classe MSMCAEvent MemoryPageRemoved</span><span class="sxs-lookup"><span data-stu-id="bbcf9-104">MSMCAEvent\_MemoryPageRemoved class</span></span>

<span data-ttu-id="bbcf9-105">La **classe \_ MemoryPageRemoved di MSMCAEvent** indica che una pagina di memoria è stata rimossa dall'utilizzo del sistema a causa di errori di controllo e correzione degli errori hardware (ecc) eccessivi.</span><span class="sxs-lookup"><span data-stu-id="bbcf9-105">The **MSMCAEvent\_MemoryPageRemoved** class indicates that a memory page has been removed from system use due to excessive hardware Error Checking and Correcting (ECC) errors.</span></span> <span data-ttu-id="bbcf9-106">Questa classe è disponibile solo nei sistemi Windows a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="bbcf9-106">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="bbcf9-107">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="bbcf9-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="bbcf9-108">Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="bbcf9-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbcf9-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bbcf9-109">Syntax</span></span>

``` syntax
class MSMCAEvent_MemoryPageRemoved : WmiEvent
{
  boolean Active;
  string  InstanceName;
  uint64  PhysicalAddress;
};
```

## <a name="members"></a><span data-ttu-id="bbcf9-110">Members</span><span class="sxs-lookup"><span data-stu-id="bbcf9-110">Members</span></span>

<span data-ttu-id="bbcf9-111">La **classe \_ MemoryPageRemoved di MSMCAEvent** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="bbcf9-111">The **MSMCAEvent\_MemoryPageRemoved** class has these types of members:</span></span>

-   [<span data-ttu-id="bbcf9-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="bbcf9-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bbcf9-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="bbcf9-113">Properties</span></span>

<span data-ttu-id="bbcf9-114">La **classe \_ MemoryPageRemoved di MSMCAEvent** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="bbcf9-114">The **MSMCAEvent\_MemoryPageRemoved** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bbcf9-115">**Attivo**</span><span class="sxs-lookup"><span data-stu-id="bbcf9-115">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbcf9-116">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="bbcf9-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bbcf9-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bbcf9-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bbcf9-118">**True** se questa istanza della classe è attiva; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="bbcf9-118">**TRUE**, if this instance of the class is active; otherwise **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="bbcf9-119">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="bbcf9-119">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbcf9-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bbcf9-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bbcf9-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bbcf9-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bbcf9-122">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="bbcf9-122">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="bbcf9-123">Identificatore univoco per questa istanza della classe.</span><span class="sxs-lookup"><span data-stu-id="bbcf9-123">Unique identifier for this instance of the class.</span></span>

</dd> <dt>

<span data-ttu-id="bbcf9-124">**PhysicalAddress**</span><span class="sxs-lookup"><span data-stu-id="bbcf9-124">**PhysicalAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbcf9-125">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="bbcf9-125">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="bbcf9-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bbcf9-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bbcf9-127">Indirizzo della pagina di memoria che è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="bbcf9-127">Address of the page of memory that has been removed.</span></span>

<span data-ttu-id="bbcf9-128">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="bbcf9-128">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bbcf9-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="bbcf9-129">Remarks</span></span>

<span data-ttu-id="bbcf9-130">La classe **MSMCAEvent \_ MemoryPageRemoved** è derivata da [**WmiEvent**](wmievent.md).</span><span class="sxs-lookup"><span data-stu-id="bbcf9-130">The **MSMCAEvent\_MemoryPageRemoved** class is derived from [**WMIEvent**](wmievent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bbcf9-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bbcf9-131">Requirements</span></span>



| <span data-ttu-id="bbcf9-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="bbcf9-132">Requirement</span></span> | <span data-ttu-id="bbcf9-133">Valore</span><span class="sxs-lookup"><span data-stu-id="bbcf9-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bbcf9-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bbcf9-134">Minimum supported client</span></span><br/> | <span data-ttu-id="bbcf9-135">Windows XP</span><span class="sxs-lookup"><span data-stu-id="bbcf9-135">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="bbcf9-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bbcf9-136">Minimum supported server</span></span><br/> | <span data-ttu-id="bbcf9-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="bbcf9-137">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="bbcf9-138">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="bbcf9-138">Namespace</span></span><br/>                | <span data-ttu-id="bbcf9-139">\\WMI radice</span><span class="sxs-lookup"><span data-stu-id="bbcf9-139">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="bbcf9-140">MOF</span><span class="sxs-lookup"><span data-stu-id="bbcf9-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bbcf9-141"><dt>Wmicore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bbcf9-141"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="bbcf9-142">DLL</span><span class="sxs-lookup"><span data-stu-id="bbcf9-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bbcf9-143"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bbcf9-143"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bbcf9-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bbcf9-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbcf9-145">Classi MSMCA</span><span class="sxs-lookup"><span data-stu-id="bbcf9-145">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="bbcf9-146">**WMIEvent**</span><span class="sxs-lookup"><span data-stu-id="bbcf9-146">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 

