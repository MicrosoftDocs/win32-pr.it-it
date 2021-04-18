---
description: Contiene un evento di controllo del computer corretto (CMC). Questa classe è disponibile solo nei sistemi Windows a 64 bit.
ms.assetid: e12efbf7-7d53-415a-bc48-90d33e4ce16d
title: Classe MSMCAInfo_RawCMCEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAInfo_RawCMCEvent
- MSMCAInfo_RawCMCEvent.Active
- MSMCAInfo_RawCMCEvent.Count
- MSMCAInfo_RawCMCEvent.InstanceName
- MSMCAInfo_RawCMCEvent.Records
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 1bb60d5fbcf004b924a91e640d8cd8a8c5ad3c25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316589"
---
# <a name="msmcainfo_rawcmcevent-class"></a><span data-ttu-id="84b31-104">\_Classe MSMCAInfo RawCMCEvent</span><span class="sxs-lookup"><span data-stu-id="84b31-104">MSMCAInfo\_RawCMCEvent class</span></span>

<span data-ttu-id="84b31-105">La **classe \_ RawCMCEvent di MSMCAInfo** contiene un evento di controllo del computer corretto (CMC).</span><span class="sxs-lookup"><span data-stu-id="84b31-105">The **MSMCAInfo\_RawCMCEvent** class contains a Corrected Machine Check (CMC) event.</span></span> <span data-ttu-id="84b31-106">Questa classe è disponibile solo nei sistemi Windows a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="84b31-106">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="84b31-107">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="84b31-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="84b31-108">Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="84b31-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="84b31-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="84b31-109">Syntax</span></span>

``` syntax
class MSMCAInfo_RawCMCEvent : WMIEvent
{
  boolean         Active;
  uint32          Count;
  string          InstanceName;
  MSMCAInfo_Entry Records[];
};
```

## <a name="members"></a><span data-ttu-id="84b31-110">Members</span><span class="sxs-lookup"><span data-stu-id="84b31-110">Members</span></span>

<span data-ttu-id="84b31-111">La **classe \_ RawCMCEvent di MSMCAInfo** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="84b31-111">The **MSMCAInfo\_RawCMCEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="84b31-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="84b31-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="84b31-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="84b31-113">Properties</span></span>

<span data-ttu-id="84b31-114">La **classe \_ RawCMCEvent di MSMCAInfo** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="84b31-114">The **MSMCAInfo\_RawCMCEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="84b31-115">**Attivo**</span><span class="sxs-lookup"><span data-stu-id="84b31-115">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84b31-116">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="84b31-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="84b31-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="84b31-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84b31-118">TRUE se questa istanza della classe è attiva; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="84b31-118">TRUE, if this instance of the class is active; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="84b31-119">**Count**</span><span class="sxs-lookup"><span data-stu-id="84b31-119">**Count**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84b31-120">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="84b31-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="84b31-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="84b31-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84b31-122">Numero di record degli errori.</span><span class="sxs-lookup"><span data-stu-id="84b31-122">Number of error records.</span></span>

</dd> <dt>

<span data-ttu-id="84b31-123">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="84b31-123">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84b31-124">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="84b31-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84b31-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="84b31-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84b31-126">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="84b31-126">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="84b31-127">Identificatore univoco di questa istanza della classe.</span><span class="sxs-lookup"><span data-stu-id="84b31-127">Unique identifier of this instance of the class.</span></span>

</dd> <dt>

<span data-ttu-id="84b31-128">**Record**</span><span class="sxs-lookup"><span data-stu-id="84b31-128">**Records**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84b31-129">Tipo di dati: **MSMCAInfo \_ entry** Array</span><span class="sxs-lookup"><span data-stu-id="84b31-129">Data type: **MSMCAInfo\_Entry** array</span></span>
</dt> <dt>

<span data-ttu-id="84b31-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="84b31-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84b31-131">Matrice di record di errori dell'architettura di controllo del computer (MCA).</span><span class="sxs-lookup"><span data-stu-id="84b31-131">Array of Machine Check Architecture (MCA) error records.</span></span> <span data-ttu-id="84b31-132">Il numero di record di errore MCA nella matrice viene specificato dalla proprietà **count** .</span><span class="sxs-lookup"><span data-stu-id="84b31-132">The number of MCA error records in the array is specified by the **Count** property.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="84b31-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="84b31-133">Remarks</span></span>

<span data-ttu-id="84b31-134">La classe **MSMCAInfo \_ RawCMCEvent** è derivata da [**WmiEvent**](wmievent.md).</span><span class="sxs-lookup"><span data-stu-id="84b31-134">The **MSMCAInfo\_RawCMCEvent** class is derived from [**WMIEvent**](wmievent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="84b31-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="84b31-135">Requirements</span></span>



| <span data-ttu-id="84b31-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="84b31-136">Requirement</span></span> | <span data-ttu-id="84b31-137">Valore</span><span class="sxs-lookup"><span data-stu-id="84b31-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="84b31-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="84b31-138">Minimum supported client</span></span><br/> | <span data-ttu-id="84b31-139">Windows XP</span><span class="sxs-lookup"><span data-stu-id="84b31-139">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="84b31-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="84b31-140">Minimum supported server</span></span><br/> | <span data-ttu-id="84b31-141">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="84b31-141">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="84b31-142">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="84b31-142">Namespace</span></span><br/>                | <span data-ttu-id="84b31-143">\\WMI radice</span><span class="sxs-lookup"><span data-stu-id="84b31-143">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="84b31-144">MOF</span><span class="sxs-lookup"><span data-stu-id="84b31-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="84b31-145"><dt>Wmicore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="84b31-145"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="84b31-146">DLL</span><span class="sxs-lookup"><span data-stu-id="84b31-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="84b31-147"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="84b31-147"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84b31-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="84b31-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84b31-149">Classi MSMCA</span><span class="sxs-lookup"><span data-stu-id="84b31-149">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="84b31-150">**WMIEvent**</span><span class="sxs-lookup"><span data-stu-id="84b31-150">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 

