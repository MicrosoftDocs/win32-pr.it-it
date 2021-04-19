---
description: Rappresenta i parametri di luminosità di un monitor del computer.
ms.assetid: 01fa3efc-2a1d-4405-989f-2c180842c6b9
title: Classe WmiMonitorBrightness
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorBrightness
- WmiMonitorBrightness.Active
- WmiMonitorBrightness.CurrentBrightness
- WmiMonitorBrightness.InstanceName
- WmiMonitorBrightness.Level
- WmiMonitorBrightness.Levels
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: b8d16c8dc20291a03fb205441c8826c85125970c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317606"
---
# <a name="wmimonitorbrightness-class"></a><span data-ttu-id="e8c41-103">Classe WmiMonitorBrightness</span><span class="sxs-lookup"><span data-stu-id="e8c41-103">WmiMonitorBrightness class</span></span>

<span data-ttu-id="e8c41-104">La classe WMI **WmiMonitorBrightness** rappresenta i parametri di luminosità di un monitor del computer.</span><span class="sxs-lookup"><span data-stu-id="e8c41-104">The **WmiMonitorBrightness** WMI class represents the brightness parameters of a computer monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8c41-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e8c41-105">Syntax</span></span>

``` syntax
class WmiMonitorBrightness : MSMonitorClass
{
  boolean Active;
  uint8   CurrentBrightness;
          InstanceName;
  uint8   Level[];
  uint32  Levels;
};
```

## <a name="members"></a><span data-ttu-id="e8c41-106">Members</span><span class="sxs-lookup"><span data-stu-id="e8c41-106">Members</span></span>

<span data-ttu-id="e8c41-107">La classe **WmiMonitorBrightness** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="e8c41-107">The **WmiMonitorBrightness** class has these types of members:</span></span>

-   [<span data-ttu-id="e8c41-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e8c41-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e8c41-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e8c41-109">Properties</span></span>

<span data-ttu-id="e8c41-110">La classe **WmiMonitorBrightness** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="e8c41-110">The **WmiMonitorBrightness** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e8c41-111">**Attivo**</span><span class="sxs-lookup"><span data-stu-id="e8c41-111">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8c41-112">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="e8c41-112">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e8c41-113">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e8c41-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e8c41-114">Indica se il monitoraggio di destinazione è attivo.</span><span class="sxs-lookup"><span data-stu-id="e8c41-114">Indicates if the target monitor is active.</span></span>

</dd> <dt>

<span data-ttu-id="e8c41-115">**CurrentBrightness**</span><span class="sxs-lookup"><span data-stu-id="e8c41-115">**CurrentBrightness**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8c41-116">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="e8c41-116">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="e8c41-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e8c41-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e8c41-118">Luminosità corrente.</span><span class="sxs-lookup"><span data-stu-id="e8c41-118">Current brightness.</span></span> <span data-ttu-id="e8c41-119">Questo valore deve essere un valore tratto dai *livelli*.</span><span class="sxs-lookup"><span data-stu-id="e8c41-119">This value must be a value taken from *Levels*.</span></span>

<span data-ttu-id="e8c41-120">Esempio: 100</span><span class="sxs-lookup"><span data-stu-id="e8c41-120">Example: 100</span></span>

</dd> <dt>

<span data-ttu-id="e8c41-121">InstanceName</span><span class="sxs-lookup"><span data-stu-id="e8c41-121">InstanceName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8c41-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e8c41-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e8c41-123">Qualificatori: chiave</span><span class="sxs-lookup"><span data-stu-id="e8c41-123">Qualifiers: Key</span></span>
</dt> </dl>

<span data-ttu-id="e8c41-124">Nome dell'istanza di monitoraggio specifica.</span><span class="sxs-lookup"><span data-stu-id="e8c41-124">Name of the specific monitor instance.</span></span>

</dd> <dt>

<span data-ttu-id="e8c41-125">**Level**</span><span class="sxs-lookup"><span data-stu-id="e8c41-125">**Level**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8c41-126">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="e8c41-126">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="e8c41-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e8c41-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e8c41-128">Matrice contenente i livelli di luminosità possibili.</span><span class="sxs-lookup"><span data-stu-id="e8c41-128">Array containing the possible brightness levels.</span></span>

<span data-ttu-id="e8c41-129">Esempio: \[ 0, 1, 2,..., 100 \] .</span><span class="sxs-lookup"><span data-stu-id="e8c41-129">Example: \[0, 1, 2, ..., 100\].</span></span>

</dd> <dt>

<span data-ttu-id="e8c41-130">**Livelli**</span><span class="sxs-lookup"><span data-stu-id="e8c41-130">**Levels**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8c41-131">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e8c41-131">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e8c41-132">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e8c41-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e8c41-133">Il numero totale di livelli di luminosità supportati dal monitoraggio, come descritto in *Level*.</span><span class="sxs-lookup"><span data-stu-id="e8c41-133">The total number of brightness levels the monitor supports, as described in *Level*.</span></span>

<span data-ttu-id="e8c41-134">Esempio: 101</span><span class="sxs-lookup"><span data-stu-id="e8c41-134">Example: 101</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="e8c41-135">Esempio</span><span class="sxs-lookup"><span data-stu-id="e8c41-135">Examples</span></span>

<span data-ttu-id="e8c41-136">Per altre informazioni ed esempi di codice sull'uso di questa classe in PowerShell, vedere [usare PowerShell per segnalare e impostare la luminosità del monitoraggio](https://blogs.technet.com/b/heyscriptingguy/archive/2013/07/25/use-powershell-to-report-and-set-monitor-brightness.aspx).</span><span class="sxs-lookup"><span data-stu-id="e8c41-136">For more information and code samples on using this class in PowerShell, see [Use PowerShell to Report and Set Monitor Brightness](https://blogs.technet.com/b/heyscriptingguy/archive/2013/07/25/use-powershell-to-report-and-set-monitor-brightness.aspx).</span></span>

## <a name="requirements"></a><span data-ttu-id="e8c41-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e8c41-137">Requirements</span></span>



| <span data-ttu-id="e8c41-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8c41-138">Requirement</span></span> | <span data-ttu-id="e8c41-139">Valore</span><span class="sxs-lookup"><span data-stu-id="e8c41-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e8c41-140">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e8c41-140">Minimum supported client</span></span><br/> | <span data-ttu-id="e8c41-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e8c41-141">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="e8c41-142">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e8c41-142">Minimum supported server</span></span><br/> | <span data-ttu-id="e8c41-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e8c41-143">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="e8c41-144">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e8c41-144">Namespace</span></span><br/>                | <span data-ttu-id="e8c41-145">\\WMI radice</span><span class="sxs-lookup"><span data-stu-id="e8c41-145">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="e8c41-146">MOF</span><span class="sxs-lookup"><span data-stu-id="e8c41-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e8c41-147"><dt>WmiCore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e8c41-147"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="e8c41-148">DLL</span><span class="sxs-lookup"><span data-stu-id="e8c41-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e8c41-149"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e8c41-149"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8c41-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e8c41-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8c41-151">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="e8c41-151">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




