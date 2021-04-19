---
description: Elenca le modalità di origine supportate per un monitor video nel relativo descrittore di monitoraggio, se presente.
ms.assetid: cca59d28-bd93-4df2-989e-0516dd8eae83
title: Classe WmiMonitorListedSupportedSourceModes
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorListedSupportedSourceModes
- WmiMonitorListedSupportedSourceModes.Active
- WmiMonitorListedSupportedSourceModes.InstanceName
- WmiMonitorListedSupportedSourceModes.NumOfMonitorSourceModes
- WmiMonitorListedSupportedSourceModes.PreferredMonitorSourceModeIndex
- WmiMonitorListedSupportedSourceModes.MonitorSourceModes
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 35cb4b3548654c72686a8843cc697f109f661d87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314099"
---
# <a name="wmimonitorlistedsupportedsourcemodes-class"></a><span data-ttu-id="bffe2-103">Classe WmiMonitorListedSupportedSourceModes</span><span class="sxs-lookup"><span data-stu-id="bffe2-103">WmiMonitorListedSupportedSourceModes class</span></span>

<span data-ttu-id="bffe2-104">Il **WmiMonitorListedSupportedSourceModes** elenca le modalità di origine supportate per un monitor video nel relativo descrittore di monitoraggio, se presente.</span><span class="sxs-lookup"><span data-stu-id="bffe2-104">The **WmiMonitorListedSupportedSourceModes** lists the supported source modes for a video monitor in its monitor descriptor, if any exist.</span></span> <span data-ttu-id="bffe2-105">Per i monitoraggi senza descrizione, questo elenco di modalità viene generato in base al tipo di monitoraggio, come specificato dal driver del bus di monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="bffe2-105">For monitors that have no description, this list of modes is generated based on the type of monitor, as specified by the monitor bus driver.</span></span>

## <a name="syntax"></a><span data-ttu-id="bffe2-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bffe2-106">Syntax</span></span>

``` syntax
class WmiMonitorListedSupportedSourceModes : MSMonitorClass
{
  boolean             Active;
  string              InstanceName;
  uint16              NumOfMonitorSourceModes;
  uint16              PreferredMonitorSourceModeIndex;
  VideoModeDescriptor MonitorSourceModes[];
};
```

## <a name="members"></a><span data-ttu-id="bffe2-107">Members</span><span class="sxs-lookup"><span data-stu-id="bffe2-107">Members</span></span>

<span data-ttu-id="bffe2-108">La classe **WmiMonitorListedSupportedSourceModes** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="bffe2-108">The **WmiMonitorListedSupportedSourceModes** class has these types of members:</span></span>

-   [<span data-ttu-id="bffe2-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="bffe2-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bffe2-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="bffe2-110">Properties</span></span>

<span data-ttu-id="bffe2-111">La classe **WmiMonitorListedSupportedSourceModes** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="bffe2-111">The **WmiMonitorListedSupportedSourceModes** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bffe2-112">**Attivo**</span><span class="sxs-lookup"><span data-stu-id="bffe2-112">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bffe2-113">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="bffe2-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bffe2-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bffe2-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bffe2-115">Indica il monitoraggio attivo.</span><span class="sxs-lookup"><span data-stu-id="bffe2-115">Indicates the active monitor.</span></span>

</dd> <dt>

<span data-ttu-id="bffe2-116">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="bffe2-116">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bffe2-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bffe2-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bffe2-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bffe2-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bffe2-119">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="bffe2-119">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="bffe2-120">Nome dell'istanza di monitoraggio specifica.</span><span class="sxs-lookup"><span data-stu-id="bffe2-120">Name of the specific monitor instance.</span></span>

</dd> <dt>

<span data-ttu-id="bffe2-121">**MonitorSourceModes**</span><span class="sxs-lookup"><span data-stu-id="bffe2-121">**MonitorSourceModes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bffe2-122">Tipo di dati: matrice **VideoModeDescriptor**</span><span class="sxs-lookup"><span data-stu-id="bffe2-122">Data type: **VideoModeDescriptor** array</span></span>
</dt> <dt>

<span data-ttu-id="bffe2-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bffe2-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bffe2-124">Elenca le modalità di origine del monitoraggio rappresentate da istanze della classe [**VideoModeDescriptor**](videomodedescriptor.md) .</span><span class="sxs-lookup"><span data-stu-id="bffe2-124">Lists monitor source modes represented by instances of the [**VideoModeDescriptor**](videomodedescriptor.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="bffe2-125">**NumOfMonitorSourceModes**</span><span class="sxs-lookup"><span data-stu-id="bffe2-125">**NumOfMonitorSourceModes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bffe2-126">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bffe2-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bffe2-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bffe2-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bffe2-128">Numero di modalità di origine del monitoraggio supportato elencate.</span><span class="sxs-lookup"><span data-stu-id="bffe2-128">Number of listed supported monitor source mode.</span></span>

</dd> <dt>

<span data-ttu-id="bffe2-129">**PreferredMonitorSourceModeIndex**</span><span class="sxs-lookup"><span data-stu-id="bffe2-129">**PreferredMonitorSourceModeIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bffe2-130">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bffe2-130">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bffe2-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bffe2-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bffe2-132">Indice della modalità origine del monitoraggio preferito.</span><span class="sxs-lookup"><span data-stu-id="bffe2-132">Preferred monitor source mode index.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bffe2-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bffe2-133">Requirements</span></span>



| <span data-ttu-id="bffe2-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="bffe2-134">Requirement</span></span> | <span data-ttu-id="bffe2-135">Valore</span><span class="sxs-lookup"><span data-stu-id="bffe2-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bffe2-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bffe2-136">Minimum supported client</span></span><br/> | <span data-ttu-id="bffe2-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bffe2-137">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="bffe2-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bffe2-138">Minimum supported server</span></span><br/> | <span data-ttu-id="bffe2-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bffe2-139">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="bffe2-140">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="bffe2-140">Namespace</span></span><br/>                | <span data-ttu-id="bffe2-141">\\WMI radice</span><span class="sxs-lookup"><span data-stu-id="bffe2-141">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="bffe2-142">MOF</span><span class="sxs-lookup"><span data-stu-id="bffe2-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bffe2-143"><dt>WmiCore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bffe2-143"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="bffe2-144">DLL</span><span class="sxs-lookup"><span data-stu-id="bffe2-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bffe2-145"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bffe2-145"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bffe2-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bffe2-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bffe2-147">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="bffe2-147">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




