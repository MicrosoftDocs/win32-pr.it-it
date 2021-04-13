---
description: Specifica i log MCA (RAW Machine Check Architecture). Questa classe è disponibile solo nei sistemi Windows a 64 bit.
ms.assetid: d465ba8d-14b2-4911-ae19-19ebeb32126e
title: Classe MSMCAInfo_RawMCAData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAInfo_RawMCAData
- MSMCAInfo_RawMCAData.Active
- MSMCAInfo_RawMCAData.Count
- MSMCAInfo_RawMCAData.InstanceName
- MSMCAInfo_RawMCAData.Records
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 6cafc16ddbc91181cc2114def07a193941988228
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526101"
---
# <a name="msmcainfo_rawmcadata-class"></a><span data-ttu-id="bc9ff-104">\_Classe MSMCAInfo RawMCAData</span><span class="sxs-lookup"><span data-stu-id="bc9ff-104">MSMCAInfo\_RawMCAData class</span></span>

<span data-ttu-id="bc9ff-105">Il **\_ RawMCAData MSMCAInfo** specifica i log dell'architettura di controllo del computer (MCA) non elaborati.</span><span class="sxs-lookup"><span data-stu-id="bc9ff-105">The **MSMCAInfo\_RawMCAData** specifies the raw Machine Check Architecture (MCA) logs.</span></span> <span data-ttu-id="bc9ff-106">Questa classe è disponibile solo nei sistemi Windows a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="bc9ff-106">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="bc9ff-107">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="bc9ff-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="bc9ff-108">Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="bc9ff-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc9ff-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bc9ff-109">Syntax</span></span>

``` syntax
class MSMCAInfo_RawMCAData : MSMCAInfo
{
  boolean         Active;
  uint32          Count;
  string          InstanceName;
  MSMCAInfo_Entry Records[];
};
```

## <a name="members"></a><span data-ttu-id="bc9ff-110">Members</span><span class="sxs-lookup"><span data-stu-id="bc9ff-110">Members</span></span>

<span data-ttu-id="bc9ff-111">La **classe \_ RawMCAData di MSMCAInfo** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="bc9ff-111">The **MSMCAInfo\_RawMCAData** class has these types of members:</span></span>

-   [<span data-ttu-id="bc9ff-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="bc9ff-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bc9ff-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="bc9ff-113">Properties</span></span>

<span data-ttu-id="bc9ff-114">La **classe \_ RawMCAData di MSMCAInfo** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="bc9ff-114">The **MSMCAInfo\_RawMCAData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bc9ff-115">**Attivo**</span><span class="sxs-lookup"><span data-stu-id="bc9ff-115">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc9ff-116">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="bc9ff-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bc9ff-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc9ff-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc9ff-118">TRUE se questa istanza della classe è attiva; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="bc9ff-118">TRUE, if this instance of the class is active; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="bc9ff-119">**Count**</span><span class="sxs-lookup"><span data-stu-id="bc9ff-119">**Count**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc9ff-120">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bc9ff-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bc9ff-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc9ff-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc9ff-122">Numero di record degli errori.</span><span class="sxs-lookup"><span data-stu-id="bc9ff-122">Number of error records.</span></span>

</dd> <dt>

<span data-ttu-id="bc9ff-123">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="bc9ff-123">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc9ff-124">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bc9ff-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc9ff-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc9ff-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc9ff-126">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="bc9ff-126">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="bc9ff-127">Identificatore univoco di questa istanza della classe.</span><span class="sxs-lookup"><span data-stu-id="bc9ff-127">Unique identifier of this instance of the class.</span></span>

</dd> <dt>

<span data-ttu-id="bc9ff-128">**Record**</span><span class="sxs-lookup"><span data-stu-id="bc9ff-128">**Records**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc9ff-129">Tipo di dati: **MSMCAInfo \_ entry** Array</span><span class="sxs-lookup"><span data-stu-id="bc9ff-129">Data type: **MSMCAInfo\_Entry** array</span></span>
</dt> <dt>

<span data-ttu-id="bc9ff-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc9ff-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc9ff-131">Matrice di record degli errori MCA.</span><span class="sxs-lookup"><span data-stu-id="bc9ff-131">Array of MCA error records.</span></span> <span data-ttu-id="bc9ff-132">Il numero di record di errore MCA nella matrice viene specificato dalla proprietà **count** .</span><span class="sxs-lookup"><span data-stu-id="bc9ff-132">The number of MCA error records in the array is specified by the **Count** property.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bc9ff-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="bc9ff-133">Remarks</span></span>

<span data-ttu-id="bc9ff-134">La classe **MSMCAInfo \_ RawMCAData** è derivata da [**MSMCAInfo**](msmcainfo.md).</span><span class="sxs-lookup"><span data-stu-id="bc9ff-134">The **MSMCAInfo\_RawMCAData** class is derived from [**MSMCAInfo**](msmcainfo.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bc9ff-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bc9ff-135">Requirements</span></span>



| <span data-ttu-id="bc9ff-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc9ff-136">Requirement</span></span> | <span data-ttu-id="bc9ff-137">Valore</span><span class="sxs-lookup"><span data-stu-id="bc9ff-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bc9ff-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bc9ff-138">Minimum supported client</span></span><br/> | <span data-ttu-id="bc9ff-139">Windows XP</span><span class="sxs-lookup"><span data-stu-id="bc9ff-139">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="bc9ff-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bc9ff-140">Minimum supported server</span></span><br/> | <span data-ttu-id="bc9ff-141">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="bc9ff-141">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="bc9ff-142">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="bc9ff-142">Namespace</span></span><br/>                | <span data-ttu-id="bc9ff-143">\\WMI radice</span><span class="sxs-lookup"><span data-stu-id="bc9ff-143">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="bc9ff-144">MOF</span><span class="sxs-lookup"><span data-stu-id="bc9ff-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bc9ff-145"><dt>Wmicore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bc9ff-145"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="bc9ff-146">DLL</span><span class="sxs-lookup"><span data-stu-id="bc9ff-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bc9ff-147"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bc9ff-147"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc9ff-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bc9ff-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc9ff-149">Classi MSMCA</span><span class="sxs-lookup"><span data-stu-id="bc9ff-149">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="bc9ff-150">**MSMCAInfo**</span><span class="sxs-lookup"><span data-stu-id="bc9ff-150">**MSMCAInfo**</span></span>](msmcainfo.md)
</dt> </dl>

 

