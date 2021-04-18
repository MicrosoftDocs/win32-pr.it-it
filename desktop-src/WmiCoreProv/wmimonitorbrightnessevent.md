---
description: Rappresenta una modifica della luminosità di un monitoraggio.
ms.assetid: c2eb5630-a52f-4ad4-aaee-1cc8afef8c9e
title: Classe WmiMonitorBrightnessEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorBrightnessEvent
- WmiMonitorBrightnessEvent.Active
- WmiMonitorBrightnessEvent.Brightness
- WmiMonitorBrightnessEvent.InstanceName
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 7e53f90627c959db0140b01cf3b3d385afcc6e73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315742"
---
# <a name="wmimonitorbrightnessevent-class"></a><span data-ttu-id="a831d-103">Classe WmiMonitorBrightnessEvent</span><span class="sxs-lookup"><span data-stu-id="a831d-103">WmiMonitorBrightnessEvent class</span></span>

<span data-ttu-id="a831d-104">La classe di evento **WmiMonitorBrightnessEvent** WMI rappresenta una modifica della luminosità di un monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="a831d-104">The **WmiMonitorBrightnessEvent** WMI event class represents a change in the brightness of a monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="a831d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a831d-105">Syntax</span></span>

``` syntax
class WmiMonitorBrightnessEvent : WMIEvent
{
  boolean Active;
  uint8   Brightness;
  string  InstanceName;
};
```

## <a name="members"></a><span data-ttu-id="a831d-106">Members</span><span class="sxs-lookup"><span data-stu-id="a831d-106">Members</span></span>

<span data-ttu-id="a831d-107">La classe **WmiMonitorBrightnessEvent** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="a831d-107">The **WmiMonitorBrightnessEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="a831d-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a831d-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a831d-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a831d-109">Properties</span></span>

<span data-ttu-id="a831d-110">La classe **WmiMonitorBrightnessEvent** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="a831d-110">The **WmiMonitorBrightnessEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a831d-111">**Attivo**</span><span class="sxs-lookup"><span data-stu-id="a831d-111">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a831d-112">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="a831d-112">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a831d-113">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a831d-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a831d-114">Indica il monitoraggio attivo.</span><span class="sxs-lookup"><span data-stu-id="a831d-114">Indicates the active monitor.</span></span>

</dd> <dt>

<span data-ttu-id="a831d-115">**Luminosità**</span><span class="sxs-lookup"><span data-stu-id="a831d-115">**Brightness**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a831d-116">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="a831d-116">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="a831d-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a831d-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a831d-118">Luminosità del monitoraggio corrente come percentuale.</span><span class="sxs-lookup"><span data-stu-id="a831d-118">Current monitor brightness as a percentage.</span></span>

</dd> <dt>

<span data-ttu-id="a831d-119">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="a831d-119">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a831d-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a831d-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a831d-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a831d-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a831d-122">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="a831d-122">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="a831d-123">Nome dell'istanza di monitoraggio specifica.</span><span class="sxs-lookup"><span data-stu-id="a831d-123">Name of the specific monitor instance.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a831d-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a831d-124">Requirements</span></span>



| <span data-ttu-id="a831d-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="a831d-125">Requirement</span></span> | <span data-ttu-id="a831d-126">Valore</span><span class="sxs-lookup"><span data-stu-id="a831d-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a831d-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a831d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="a831d-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a831d-128">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="a831d-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a831d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="a831d-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a831d-130">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="a831d-131">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a831d-131">Namespace</span></span><br/>                | <span data-ttu-id="a831d-132">\\WMI radice</span><span class="sxs-lookup"><span data-stu-id="a831d-132">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="a831d-133">MOF</span><span class="sxs-lookup"><span data-stu-id="a831d-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a831d-134"><dt>WmiCore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a831d-134"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="a831d-135">DLL</span><span class="sxs-lookup"><span data-stu-id="a831d-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a831d-136"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a831d-136"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a831d-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a831d-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a831d-138">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="a831d-138">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> <dt>

[<span data-ttu-id="a831d-139">**WmiMonitorBrightness**</span><span class="sxs-lookup"><span data-stu-id="a831d-139">**WmiMonitorBrightness**</span></span>](wmimonitorbrightness.md)
</dt> <dt>

[<span data-ttu-id="a831d-140">Ricezione di un evento WMI</span><span class="sxs-lookup"><span data-stu-id="a831d-140">Receiving a WMI Event</span></span>](/windows/desktop/WmiSdk/receiving-a-wmi-event)
</dt> </dl>

 

