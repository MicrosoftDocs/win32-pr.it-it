---
description: Contiene un evento di piattaforma con correzione (CPE). Questa classe è disponibile solo nei sistemi Windows a 64 bit.
ms.assetid: b24a390e-293d-4dd4-b747-33c298a5d45f
title: Classe MSMCAInfo_RawCorrectedPlatformEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAInfo_RawCorrectedPlatformEvent
- MSMCAInfo_RawCorrectedPlatformEvent.Active
- MSMCAInfo_RawCorrectedPlatformEvent.Count
- MSMCAInfo_RawCorrectedPlatformEvent.Records
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 906587ca9ee153eb93542c3e749e8164e6a5ee7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316588"
---
# <a name="msmcainfo_rawcorrectedplatformevent-class"></a><span data-ttu-id="a8209-104">\_Classe MSMCAInfo RawCorrectedPlatformEvent</span><span class="sxs-lookup"><span data-stu-id="a8209-104">MSMCAInfo\_RawCorrectedPlatformEvent class</span></span>

<span data-ttu-id="a8209-105">La **classe \_ RawCorrectedPlatformEvent di MSMCAInfo** contiene un evento di piattaforma corretto (CPE).</span><span class="sxs-lookup"><span data-stu-id="a8209-105">The **MSMCAInfo\_RawCorrectedPlatformEvent** class contains a Corrected Platform Event (CPE).</span></span> <span data-ttu-id="a8209-106">Questa classe è disponibile solo nei sistemi Windows a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="a8209-106">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="a8209-107">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="a8209-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="a8209-108">Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="a8209-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8209-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a8209-109">Syntax</span></span>

``` syntax
class MSMCAInfo_RawCorrectedPlatformEvent : WMIEvent
{
  boolean         Active;
  uint32          Count;
  MSMCAInfo_Entry Records[];
};
```

## <a name="members"></a><span data-ttu-id="a8209-110">Members</span><span class="sxs-lookup"><span data-stu-id="a8209-110">Members</span></span>

<span data-ttu-id="a8209-111">La **classe \_ RawCorrectedPlatformEvent di MSMCAInfo** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="a8209-111">The **MSMCAInfo\_RawCorrectedPlatformEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="a8209-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a8209-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a8209-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a8209-113">Properties</span></span>

<span data-ttu-id="a8209-114">La **classe \_ RawCorrectedPlatformEvent di MSMCAInfo** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="a8209-114">The **MSMCAInfo\_RawCorrectedPlatformEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a8209-115">**Attivo**</span><span class="sxs-lookup"><span data-stu-id="a8209-115">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8209-116">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="a8209-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a8209-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a8209-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a8209-118">TRUE se questa istanza della classe è attiva; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="a8209-118">TRUE, if this instance of the class is active; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="a8209-119">**Count**</span><span class="sxs-lookup"><span data-stu-id="a8209-119">**Count**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8209-120">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a8209-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a8209-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a8209-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a8209-122">Numero di record degli errori.</span><span class="sxs-lookup"><span data-stu-id="a8209-122">Number of error records.</span></span>

</dd> <dt>

<span data-ttu-id="a8209-123">**Record**</span><span class="sxs-lookup"><span data-stu-id="a8209-123">**Records**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8209-124">Tipo di dati: **MSMCAInfo \_ entry** Array</span><span class="sxs-lookup"><span data-stu-id="a8209-124">Data type: **MSMCAInfo\_Entry** array</span></span>
</dt> <dt>

<span data-ttu-id="a8209-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a8209-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a8209-126">Matrice di record degli errori MCA.</span><span class="sxs-lookup"><span data-stu-id="a8209-126">Array of MCA error records.</span></span> <span data-ttu-id="a8209-127">Il numero di record di errore MCA nella matrice viene specificato dalla proprietà **count** .</span><span class="sxs-lookup"><span data-stu-id="a8209-127">The number of MCA error records in the array is specified by the **Count** property.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a8209-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="a8209-128">Remarks</span></span>

<span data-ttu-id="a8209-129">La classe **MSMCAInfo \_ RawCorrectedPlatformEvent** è derivata da [**WmiEvent**](wmievent.md).</span><span class="sxs-lookup"><span data-stu-id="a8209-129">The **MSMCAInfo\_RawCorrectedPlatformEvent** class is derived from [**WMIEvent**](wmievent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a8209-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a8209-130">Requirements</span></span>



| <span data-ttu-id="a8209-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8209-131">Requirement</span></span> | <span data-ttu-id="a8209-132">Valore</span><span class="sxs-lookup"><span data-stu-id="a8209-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a8209-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a8209-133">Minimum supported client</span></span><br/> | <span data-ttu-id="a8209-134">Windows XP</span><span class="sxs-lookup"><span data-stu-id="a8209-134">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="a8209-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a8209-135">Minimum supported server</span></span><br/> | <span data-ttu-id="a8209-136">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a8209-136">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="a8209-137">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a8209-137">Namespace</span></span><br/>                | <span data-ttu-id="a8209-138">\\WMI radice</span><span class="sxs-lookup"><span data-stu-id="a8209-138">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="a8209-139">MOF</span><span class="sxs-lookup"><span data-stu-id="a8209-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a8209-140"><dt>Wmicore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a8209-140"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="a8209-141">DLL</span><span class="sxs-lookup"><span data-stu-id="a8209-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a8209-142"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a8209-142"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8209-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a8209-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8209-144">Classi MSMCA</span><span class="sxs-lookup"><span data-stu-id="a8209-144">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="a8209-145">**WMIEvent**</span><span class="sxs-lookup"><span data-stu-id="a8209-145">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 

 




