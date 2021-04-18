---
description: Contiene i metodi che gestiscono la luminosità del monitoraggio.
ms.assetid: e7e4139e-b985-4163-9c95-03008a2cc8cb
title: Classe WmiMonitorBrightnessMethods
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorBrightnessMethods
- WmiMonitorBrightnessMethods.Active
- WmiMonitorBrightnessMethods.InstanceName
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 36fe823703d5d5e4f1f6008d02c600828fe2b53f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314609"
---
# <a name="wmimonitorbrightnessmethods-class"></a><span data-ttu-id="94633-103">Classe WmiMonitorBrightnessMethods</span><span class="sxs-lookup"><span data-stu-id="94633-103">WmiMonitorBrightnessMethods class</span></span>

<span data-ttu-id="94633-104">La classe WMI **WmiMonitorBrightnessMethods** contiene metodi che gestiscono la luminosità del monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="94633-104">The **WmiMonitorBrightnessMethods** WMI class contains methods that manage monitor brightness.</span></span>

## <a name="syntax"></a><span data-ttu-id="94633-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="94633-105">Syntax</span></span>

``` syntax
class WmiMonitorBrightnessMethods
{
  boolean Active;
  string  InstanceName;
};
```

## <a name="members"></a><span data-ttu-id="94633-106">Members</span><span class="sxs-lookup"><span data-stu-id="94633-106">Members</span></span>

<span data-ttu-id="94633-107">La classe **WmiMonitorBrightnessMethods** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="94633-107">The **WmiMonitorBrightnessMethods** class has these types of members:</span></span>

-   [<span data-ttu-id="94633-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="94633-108">Methods</span></span>](#wmimonitorbrightnessmethods-class)
-   [<span data-ttu-id="94633-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="94633-109">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="94633-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="94633-110">Methods</span></span>

<span data-ttu-id="94633-111">La classe **WmiMonitorBrightnessMethods** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="94633-111">The **WmiMonitorBrightnessMethods** class has these methods.</span></span>



| <span data-ttu-id="94633-112">Metodo</span><span class="sxs-lookup"><span data-stu-id="94633-112">Method</span></span>                                                                                                         | <span data-ttu-id="94633-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="94633-113">Description</span></span>                                                    |
|:---------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------|
| [<span data-ttu-id="94633-114">**WmiRevertToPolicyBrightness**</span><span class="sxs-lookup"><span data-stu-id="94633-114">**WmiRevertToPolicyBrightness**</span></span>](wmireverttopolicybrightness-method-in-class-wmimonitorbrightnessmethods.md) | <span data-ttu-id="94633-115">Imposta di nuovo la luminosità sull'impostazione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="94633-115">Sets the brightness back to the policy setting.</span></span><br/>     |
| [<span data-ttu-id="94633-116">**WmiSetALSBrightness**</span><span class="sxs-lookup"><span data-stu-id="94633-116">**WmiSetALSBrightness**</span></span>](wmisetalsbrightness-method-in-class-wmimonitorbrightnessmethods.md)                 | <span data-ttu-id="94633-117">Imposta il valore di luminosità del sensore di luce di ambiente.</span><span class="sxs-lookup"><span data-stu-id="94633-117">Sets the ambient light sensor brightness value.</span></span><br/>     |
| [<span data-ttu-id="94633-118">**WmiSetALSBrightnessState**</span><span class="sxs-lookup"><span data-stu-id="94633-118">**WmiSetALSBrightnessState**</span></span>](wmisetalsbrightnessstate-method-in-class-wmimonitorbrightnessmethods.md)       | <span data-ttu-id="94633-119">Controlla lo stato di luminosità del sensore di luce dell'ambiente.</span><span class="sxs-lookup"><span data-stu-id="94633-119">Controls the ambient light sensor brightness state.</span></span><br/> |
| [<span data-ttu-id="94633-120">**WmiSetBrightness**</span><span class="sxs-lookup"><span data-stu-id="94633-120">**WmiSetBrightness**</span></span>](wmisetbrightness-method-in-class-wmimonitorbrightnessmethods.md)                       | <span data-ttu-id="94633-121">Imposta la luminosità del monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="94633-121">Sets the monitor brightness.</span></span><br/>                        |



 

### <a name="properties"></a><span data-ttu-id="94633-122">Proprietà</span><span class="sxs-lookup"><span data-stu-id="94633-122">Properties</span></span>

<span data-ttu-id="94633-123">La classe **WmiMonitorBrightnessMethods** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="94633-123">The **WmiMonitorBrightnessMethods** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="94633-124">**Attivo**</span><span class="sxs-lookup"><span data-stu-id="94633-124">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94633-125">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="94633-125">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="94633-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="94633-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94633-127">Indica il monitoraggio attivo.</span><span class="sxs-lookup"><span data-stu-id="94633-127">Indicates the active monitor.</span></span>

</dd> <dt>

<span data-ttu-id="94633-128">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="94633-128">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94633-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="94633-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94633-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="94633-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="94633-131">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="94633-131">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="94633-132">Nome dell'istanza di monitoraggio specifica.</span><span class="sxs-lookup"><span data-stu-id="94633-132">Name of the specific monitor instance.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="94633-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="94633-133">Requirements</span></span>



| <span data-ttu-id="94633-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="94633-134">Requirement</span></span> | <span data-ttu-id="94633-135">Valore</span><span class="sxs-lookup"><span data-stu-id="94633-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="94633-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="94633-136">Minimum supported client</span></span><br/> | <span data-ttu-id="94633-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="94633-137">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="94633-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="94633-138">Minimum supported server</span></span><br/> | <span data-ttu-id="94633-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="94633-139">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="94633-140">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="94633-140">Namespace</span></span><br/>                | <span data-ttu-id="94633-141">\\WMI radice</span><span class="sxs-lookup"><span data-stu-id="94633-141">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="94633-142">MOF</span><span class="sxs-lookup"><span data-stu-id="94633-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="94633-143"><dt>WmiCore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="94633-143"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="94633-144">DLL</span><span class="sxs-lookup"><span data-stu-id="94633-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="94633-145"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="94633-145"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94633-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="94633-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94633-147">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="94633-147">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




