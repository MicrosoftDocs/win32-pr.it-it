---
description: Contiene un evento MCA (Machine Check Architecture). Questa classe è disponibile solo nei sistemi Windows a 64 bit.
ms.assetid: d1806b91-43a3-4329-8fe5-de1e4755740f
title: Classe MSMCAInfo_RawMCAEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAInfo_RawMCAEvent
- MSMCAInfo_RawMCAEvent.Active
- MSMCAInfo_RawMCAEvent.Count
- MSMCAInfo_RawMCAEvent.InstanceName
- MSMCAInfo_RawMCAEvent.Records
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: e15af79c67265823e0025849e4c2ef27f690265c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968191"
---
# <a name="msmcainfo_rawmcaevent-class"></a><span data-ttu-id="2a066-104">\_Classe MSMCAInfo RawMCAEvent</span><span class="sxs-lookup"><span data-stu-id="2a066-104">MSMCAInfo\_RawMCAEvent class</span></span>

<span data-ttu-id="2a066-105">La **classe \_ RawMCAEvent di MSMCAInfo** contiene un evento MCA (Machine Check Architecture).</span><span class="sxs-lookup"><span data-stu-id="2a066-105">The **MSMCAInfo\_RawMCAEvent** class contains a Machine Check Architecture (MCA) event.</span></span> <span data-ttu-id="2a066-106">Questa classe è disponibile solo nei sistemi Windows a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="2a066-106">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="2a066-107">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="2a066-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="2a066-108">Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="2a066-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a066-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2a066-109">Syntax</span></span>

``` syntax
class MSMCAInfo_RawMCAEvent : WMIEvent
{
  boolean         Active;
  uint32          Count;
  string          InstanceName;
  MSMCAInfo_Entry Records[];
};
```

## <a name="members"></a><span data-ttu-id="2a066-110">Members</span><span class="sxs-lookup"><span data-stu-id="2a066-110">Members</span></span>

<span data-ttu-id="2a066-111">La **classe \_ RawMCAEvent di MSMCAInfo** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="2a066-111">The **MSMCAInfo\_RawMCAEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="2a066-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2a066-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2a066-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2a066-113">Properties</span></span>

<span data-ttu-id="2a066-114">La **classe \_ RawMCAEvent di MSMCAInfo** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="2a066-114">The **MSMCAInfo\_RawMCAEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2a066-115">**Attivo**</span><span class="sxs-lookup"><span data-stu-id="2a066-115">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a066-116">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="2a066-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2a066-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2a066-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a066-118">TRUE se questa istanza della classe è attiva; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="2a066-118">TRUE, if this instance of the class is active; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="2a066-119">**Count**</span><span class="sxs-lookup"><span data-stu-id="2a066-119">**Count**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a066-120">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2a066-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2a066-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2a066-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a066-122">Numero di record degli errori.</span><span class="sxs-lookup"><span data-stu-id="2a066-122">Number of error records.</span></span>

</dd> <dt>

<span data-ttu-id="2a066-123">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="2a066-123">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a066-124">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2a066-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2a066-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2a066-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2a066-126">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2a066-126">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2a066-127">Stringa che identifica in modo univoco questa istanza della classe **MSMCAInfo \_ RawMCAEvent** .</span><span class="sxs-lookup"><span data-stu-id="2a066-127">String that uniquely identifies this instance of the **MSMCAInfo\_RawMCAEvent** class.</span></span>

</dd> <dt>

<span data-ttu-id="2a066-128">**Record**</span><span class="sxs-lookup"><span data-stu-id="2a066-128">**Records**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a066-129">Tipo di dati: **MSMCAInfo \_ entry** Array</span><span class="sxs-lookup"><span data-stu-id="2a066-129">Data type: **MSMCAInfo\_Entry** array</span></span>
</dt> <dt>

<span data-ttu-id="2a066-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2a066-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a066-131">Matrice di record degli errori MCA.</span><span class="sxs-lookup"><span data-stu-id="2a066-131">Array of MCA error records.</span></span> <span data-ttu-id="2a066-132">Il numero di record di errore MCA nella matrice viene specificato dalla proprietà **count** .</span><span class="sxs-lookup"><span data-stu-id="2a066-132">The number of MCA error records in the array is specified by the **Count** property.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2a066-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="2a066-133">Remarks</span></span>

<span data-ttu-id="2a066-134">La classe **MSMCAInfo \_ RawMCAEvent** è derivata da [**WmiEvent**](wmievent.md).</span><span class="sxs-lookup"><span data-stu-id="2a066-134">The **MSMCAInfo\_RawMCAEvent** class is derived from [**WMIEvent**](wmievent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2a066-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2a066-135">Requirements</span></span>



| <span data-ttu-id="2a066-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a066-136">Requirement</span></span> | <span data-ttu-id="2a066-137">Valore</span><span class="sxs-lookup"><span data-stu-id="2a066-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2a066-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2a066-138">Minimum supported client</span></span><br/> | <span data-ttu-id="2a066-139">Windows XP</span><span class="sxs-lookup"><span data-stu-id="2a066-139">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="2a066-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2a066-140">Minimum supported server</span></span><br/> | <span data-ttu-id="2a066-141">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2a066-141">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="2a066-142">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="2a066-142">Namespace</span></span><br/>                | <span data-ttu-id="2a066-143">\\WMI radice</span><span class="sxs-lookup"><span data-stu-id="2a066-143">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="2a066-144">MOF</span><span class="sxs-lookup"><span data-stu-id="2a066-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2a066-145"><dt>Wmicore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2a066-145"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="2a066-146">DLL</span><span class="sxs-lookup"><span data-stu-id="2a066-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2a066-147"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2a066-147"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a066-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2a066-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a066-149">Classi MSMCA</span><span class="sxs-lookup"><span data-stu-id="2a066-149">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="2a066-150">**WMIEvent**</span><span class="sxs-lookup"><span data-stu-id="2a066-150">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 

